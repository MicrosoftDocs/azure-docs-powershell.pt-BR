---
title: Executar os cmdlets em paralelo usando trabalhos do PowerShell
description: Como executar os cmdlets em paralelo usando o parâmetro -AsJob.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: d312812ff3c9e4934ed2bfa7371a9e420668e852
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "83384973"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a><span data-ttu-id="c29bf-103">Executar os cmdlets em paralelo usando trabalhos do PowerShell</span><span class="sxs-lookup"><span data-stu-id="c29bf-103">Running cmdlets in parallel using PowerShell jobs</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="c29bf-104">PowerShell dá suporte à ação assíncrona com os [trabalhos do PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="c29bf-104">PowerShell supports asynchronous action with [PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>
<span data-ttu-id="c29bf-105">O Azure PowerShell está altamente dependente de fazer e aguardar chamadas de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="c29bf-105">Azure PowerShell is heavily dependent on making, and waiting for, network calls to Azure.</span></span> <span data-ttu-id="c29bf-106">Muitas vezes você verá que será necessário fazer chamadas sem bloqueio.</span><span class="sxs-lookup"><span data-stu-id="c29bf-106">You may often find yourself needing to make non-blocking calls.</span></span> <span data-ttu-id="c29bf-107">Para atender a essa necessidade, o Azure PowerShell fornece suporte ao [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) de primeira classe.</span><span class="sxs-lookup"><span data-stu-id="c29bf-107">To address this need, Azure PowerShell provides first-class [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) support.</span></span>

## <a name="context-persistence-and-psjobs"></a><span data-ttu-id="c29bf-108">Persistência de Contexto e PSJobs</span><span class="sxs-lookup"><span data-stu-id="c29bf-108">Context Persistence and PSJobs</span></span>

<span data-ttu-id="c29bf-109">Como os PSJobs são executados como processos separados, a sua conexão do Azure deve ser compartilhada com eles.</span><span class="sxs-lookup"><span data-stu-id="c29bf-109">Since PSJobs are run as separate processes, your Azure connection must be shared with them.</span></span> <span data-ttu-id="c29bf-110">Após entrar na sua conta do Azure com `Connect-AzureRmAccount`, passe o contexto para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="c29bf-110">After signing in to your Azure account with `Connect-AzureRmAccount`, pass the context to a job.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzureRmVM -Name MyVm -AzureRmContext $context -Credential $vmadmin} -Arguments (Get-AzureRmContext),$creds
```

<span data-ttu-id="c29bf-111">No entanto, se você tiver optado por ter seu contexto automaticamente salvo com `Enable-AzureRmContextAutosave`, o contexto é automaticamente compartilhado com qualquer trabalho que você criar.</span><span class="sxs-lookup"><span data-stu-id="c29bf-111">However, if you have chosen to have your context automatically saved with `Enable-AzureRmContextAutosave`, the context is automatically shared with any jobs you create.</span></span>

```azurepowershell-interactive
Enable-AzureRmContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzureRmVM -Name MyVm -Credential $vmadmin} -Arguments $creds
```

## <a name="automatic-jobs-with--asjob"></a><span data-ttu-id="c29bf-112">Trabalhos Automáticos com`-AsJob`</span><span class="sxs-lookup"><span data-stu-id="c29bf-112">Automatic Jobs with `-AsJob`</span></span>

<span data-ttu-id="c29bf-113">Como uma conveniência, o Azure PowerShell também fornece um alternador `-AsJob` em alguns cmdlets de execução longa.</span><span class="sxs-lookup"><span data-stu-id="c29bf-113">As a convenience, Azure PowerShell also provides an `-AsJob` switch on some long-running cmdlets.</span></span>
<span data-ttu-id="c29bf-114">O alternador `-AsJob` torna a criação de PSJobs ainda mais fácil.</span><span class="sxs-lookup"><span data-stu-id="c29bf-114">The `-AsJob` switch makes creating PSJobs even easier.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzureRmVM -Name MyVm -Credential $creds -AsJob
```

<span data-ttu-id="c29bf-115">Você pode inspecionar o trabalho e o andamento a qualquer momento com `Get-Job` e `Get-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="c29bf-115">You can inspect the job and progress at any time with `Get-Job` and `Get-AzureRmVM`.</span></span>

```azurepowershell-interactive
Get-Job $job
Get-AzureRmVM MyVm
```

```output
Id Name                                       PSJobTypeName         State   HasMoreData Location  Command
-- ----                                       -------------         -----   ----------- --------  -------
1  Long Running Operation for 'New-AzureRmVM' AzureLongRunningJob`1 Running True        localhost New-AzureRmVM

ResourceGroupName    Name Location          VmSize  OsType     NIC ProvisioningState Zone
-----------------    ---- --------          ------  ------     --- ----------------- ----
MyVm                 MyVm   eastus Standard_DS1_v2 Windows    MyVm          Creating
```

<span data-ttu-id="c29bf-116">Quando o trabalho for concluído, obtenha o resultado do trabalho com `Receive-Job`.</span><span class="sxs-lookup"><span data-stu-id="c29bf-116">When the job completes, get the result of the job with `Receive-Job`.</span></span>

> [!NOTE]
> <span data-ttu-id="c29bf-117">`Receive-Job` retorna o resultado do cmdlet como se o sinalizador `-AsJob` não estivesse presente.</span><span class="sxs-lookup"><span data-stu-id="c29bf-117">`Receive-Job` returns the result from the cmdlet as if the `-AsJob` flag were not present.</span></span>
> <span data-ttu-id="c29bf-118">Por exemplo, o resultado `Receive-Job` de `Do-Action -AsJob` é do mesmo tipo de resultado de `Do-Action`.</span><span class="sxs-lookup"><span data-stu-id="c29bf-118">For example, the `Receive-Job` result of `Do-Action -AsJob` is of the same type as the result of `Do-Action`.</span></span>

```azurepowershell-interactive
$vm = Receive-Job $job
$vm
```

```output
ResourceGroupName        : MyVm
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyVm/providers/Microsoft.Compute/virtualMachines/MyVm
VmId                     : dff1f79e-a8f7-4664-ab72-0ec28b9fbb5b
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvmmyvm.eastus.cloudapp.azure.com
```

## <a name="example-scenarios"></a><span data-ttu-id="c29bf-119">Cenários de Exemplo</span><span class="sxs-lookup"><span data-stu-id="c29bf-119">Example Scenarios</span></span>

<span data-ttu-id="c29bf-120">Criar várias VMs ao mesmo tempo:</span><span class="sxs-lookup"><span data-stu-id="c29bf-120">Create several VMs at once:</span></span>

```azurepowershell-interactive
$creds = Get-Credential
# Create 10 jobs.
for($k = 0; $k -lt 10; $k++) {
    New-AzureRmVm -Name MyVm$k  -Credential $creds -AsJob
}

# Get all jobs and wait on them.
Get-Job | Wait-Job
"All jobs completed"
Get-AzureRmVM
```

<span data-ttu-id="c29bf-121">Nesse exemplo, o cmdlet `Wait-Job` faz com que o script pause enquanto os trabalhos são executados.</span><span class="sxs-lookup"><span data-stu-id="c29bf-121">In this example, the `Wait-Job` cmdlet causes the script to pause while jobs run.</span></span> <span data-ttu-id="c29bf-122">O script continuará depois que concluir todos os trabalhos em execução.</span><span class="sxs-lookup"><span data-stu-id="c29bf-122">The script continues executing once all of the jobs have completed.</span></span> <span data-ttu-id="c29bf-123">Vários trabalhos estão sendo executados em paralelo, então o script aguarda a conclusão antes de prosseguir.</span><span class="sxs-lookup"><span data-stu-id="c29bf-123">Several jobs run in parallel then the script waits for completion before continuing.</span></span>

```output
Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
3      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
4      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
5      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
6      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
7      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
8      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
9      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
10     Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
11     Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
2      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
3      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
4      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
5      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
6      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
7      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
8      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
9      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
10     Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
11     Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
All Jobs completed.

ResourceGroupName        Name   Location          VmSize  OsType           NIC ProvisioningState Zone
-----------------        ----   --------          ------  ------           --- ----------------- ----
MYVM                     MyVm     eastus Standard_DS1_v2 Windows          MyVm         Succeeded
MYVM0                   MyVm0     eastus Standard_DS1_v2 Windows         MyVm0         Succeeded
MYVM1                   MyVm1     eastus Standard_DS1_v2 Windows         MyVm1         Succeeded
MYVM2                   MyVm2     eastus Standard_DS1_v2 Windows         MyVm2         Succeeded
MYVM3                   MyVm3     eastus Standard_DS1_v2 Windows         MyVm3         Succeeded
MYVM4                   MyVm4     eastus Standard_DS1_v2 Windows         MyVm4         Succeeded
MYVM5                   MyVm5     eastus Standard_DS1_v2 Windows         MyVm5         Succeeded
MYVM6                   MyVm6     eastus Standard_DS1_v2 Windows         MyVm6         Succeeded
MYVM7                   MyVm7     eastus Standard_DS1_v2 Windows         MyVm7         Succeeded
MYVM8                   MyVm8     eastus Standard_DS1_v2 Windows         MyVm8         Succeeded
MYVM9                   MyVm9     eastus Standard_DS1_v2 Windows         MyVm9         Succeeded
```
