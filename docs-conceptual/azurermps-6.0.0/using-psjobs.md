---
title: Executar os cmdlets em paralelo usando trabalhos do PowerShell
description: Como executar os cmdlets em paralelo usando o parâmetro -AsJob.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/11/2017
ms.openlocfilehash: dfc1efa752c9c9fa42ad5904adacd83c2dc333b8
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/08/2018
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a><span data-ttu-id="30c3b-103">Executar os cmdlets em paralelo usando trabalhos do PowerShell</span><span class="sxs-lookup"><span data-stu-id="30c3b-103">Running cmdlets in parallel using PowerShell jobs</span></span>

<span data-ttu-id="30c3b-104">PowerShell dá suporte à ação assíncrona com os [trabalhos do PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="30c3b-104">PowerShell supports asynchronous action with [PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>
<span data-ttu-id="30c3b-105">O Azure PowerShell está altamente dependente de fazer e aguardar chamadas de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="30c3b-105">Azure PowerShell is heavily dependent on making, and waiting for, network calls to Azure.</span></span> <span data-ttu-id="30c3b-106">Como desenvolvedor, você pode geralmente perceber que está tentando fazer várias chamadas sem bloqueio para o Azure em um script ou pode desejar criar recursos do Azure no REPL sem bloquear a sessão atual.</span><span class="sxs-lookup"><span data-stu-id="30c3b-106">As a developer, you may often find yourself looking to make multiple non-blocking calls to Azure in a script, or you may find that you want to create Azure resources in the REPL without blocking the current session.</span></span> <span data-ttu-id="30c3b-107">Para atender a essas necessidades, o Azure PowerShell fornece suporte ao [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) de primeira classe.</span><span class="sxs-lookup"><span data-stu-id="30c3b-107">To address these needs, Azure PowerShell provides first-class [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) support.</span></span>

## <a name="context-persistence-and-psjobs"></a><span data-ttu-id="30c3b-108">Persistência de Contexto e PSJobs</span><span class="sxs-lookup"><span data-stu-id="30c3b-108">Context Persistence and PSJobs</span></span>

<span data-ttu-id="30c3b-109">Os PSJobs são executados em processos separados, o que significa que as informações sobre a conexão do Azure devem ser compartilhadas corretamente com os trabalhos que você criar.</span><span class="sxs-lookup"><span data-stu-id="30c3b-109">PSJobs are run in separate processes, which means that information about your Azure connection must be properly shared with the jobs you create.</span></span> <span data-ttu-id="30c3b-110">Ao conectar sua conta do Azure à sua sessão do PowerShell com `Connect-AzureRmAccount`, você pode passar o contexto para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="30c3b-110">Upon connecting your Azure account to your PowerShell session with `Connect-AzureRmAccount`, you can pass the context to a job.</span></span>

```powershell
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzureRmVM -Name MyVm -AzureRmContext $context -Credential $vmadmin} -Arguments (Get-AzureRmContext),$creds
```

<span data-ttu-id="30c3b-111">No entanto, se você tiver optado por ter seu contexto automaticamente salvo com `Enable-AzureRmContextAutosave`, o contexto é automaticamente compartilhado com qualquer trabalho que você criar.</span><span class="sxs-lookup"><span data-stu-id="30c3b-111">However, if you have chosen to have your context automatically saved with `Enable-AzureRmContextAutosave`, the context is automatically shared with any jobs you create.</span></span>

```powershell
Enable-AzureRmContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzureRmVM -Name MyVm -Credential $vmadmin} -Arguments $creds
```

## <a name="automatic-jobs-with--asjob"></a><span data-ttu-id="30c3b-112">Trabalhos Automáticos com`-AsJob`</span><span class="sxs-lookup"><span data-stu-id="30c3b-112">Automatic Jobs with `-AsJob`</span></span>

<span data-ttu-id="30c3b-113">Como uma conveniência, o Azure PowerShell também fornece um alternador `-AsJob` em alguns cmdlets de execução longa.</span><span class="sxs-lookup"><span data-stu-id="30c3b-113">As a convenience, Azure PowerShell also provides an `-AsJob` switch on some long-running cmdlets.</span></span>
<span data-ttu-id="30c3b-114">O alternador `-AsJob` torna a criação de PSJobs ainda mais fácil.</span><span class="sxs-lookup"><span data-stu-id="30c3b-114">The `-AsJob` switch makes creating PSJobs even easier.</span></span>

```powershell
$creds = Get-Credential
$job = New-AzureRmVM -Name MyVm -Credential $creds -AsJob
```

<span data-ttu-id="30c3b-115">Você pode inspecionar o trabalho e o andamento a qualquer momento com `Get-Job` e `Get-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="30c3b-115">You can inspect the job and progress at any time with `Get-Job` and `Get-AzureRmVM`.</span></span>

```powershell
Get-Job $job
Get-AzureRmVM MyVm
```

```Output
Id Name                                       PSJobTypeName         State   HasMoreData Location  Command
-- ----                                       -------------         -----   ----------- --------  -------
1  Long Running Operation for 'New-AzureRmVM' AzureLongRunningJob`1 Running True        localhost New-AzureRmVM

ResourceGroupName    Name Location          VmSize  OsType     NIC ProvisioningState Zone
-----------------    ---- --------          ------  ------     --- ----------------- ----
MyVm                 MyVm   eastus Standard_DS1_v2 Windows    MyVm          Creating
```

<span data-ttu-id="30c3b-116">Em seguida, após a conclusão, você pode obter o resultado do trabalho com `Receive-Job`.</span><span class="sxs-lookup"><span data-stu-id="30c3b-116">Subsequently, upon completion, you can obtain the result of the job with `Receive-Job`.</span></span>

> [!NOTE]
> <span data-ttu-id="30c3b-117">`Receive-Job` retorna o resultado do cmdlet como se o sinalizador `-AsJob` não estivesse presente.</span><span class="sxs-lookup"><span data-stu-id="30c3b-117">`Receive-Job` returns the result from the cmdlet as if the `-AsJob` flag were not present.</span></span>
> <span data-ttu-id="30c3b-118">Por exemplo, o resultado `Receive-Job` de `Do-Action -AsJob` é do mesmo tipo de resultado de `Do-Action`.</span><span class="sxs-lookup"><span data-stu-id="30c3b-118">For example, the `Receive-Job` result of `Do-Action -AsJob` is of the same type as the result of `Do-Action`.</span></span>

```powershell
$vm = Receive-Job $job
$vm
```

```Output
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

## <a name="example-scenarios"></a><span data-ttu-id="30c3b-119">Cenários de Exemplo</span><span class="sxs-lookup"><span data-stu-id="30c3b-119">Example Scenarios</span></span>

<span data-ttu-id="30c3b-120">Criar múltiplas VMs de uma vez.</span><span class="sxs-lookup"><span data-stu-id="30c3b-120">Create multiple VMs at once.</span></span>

```powershell
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

<span data-ttu-id="30c3b-121">Nesse exemplo, o cmdlet `Wait-Job` faz com que o script pause enquanto os trabalhos são executados.</span><span class="sxs-lookup"><span data-stu-id="30c3b-121">In this example, the `Wait-Job` cmdlet causes the script to pause while jobs run.</span></span> <span data-ttu-id="30c3b-122">O script continuará depois que concluir todos os trabalhos em execução.</span><span class="sxs-lookup"><span data-stu-id="30c3b-122">The script continues executing once all of the jobs have completed.</span></span> <span data-ttu-id="30c3b-123">Isso permite que você crie vários trabalhos em execução em paralelo e aguardar a conclusão antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="30c3b-123">This allows you to create several jobs running in parallel then wait for completion before continuing.</span></span>

```Output
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
