---
title: Executar cmdlets do Azure PowerShell nos Trabalhos do PowerShell
description: Saiba como executar os cmdlets do Azure PowerShell em paralelo ou como tarefas em segundo plano, usando -AsJob e Start-Job.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.openlocfilehash: d74d3681794398534fe2c75a0c8fc314767ffa85
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/05/2020
ms.locfileid: "72791491"
---
# <a name="run-azure-powershell-cmdlets-in-powershell-jobs"></a><span data-ttu-id="2043c-103">Executar cmdlets do Azure PowerShell nos Trabalhos do PowerShell</span><span class="sxs-lookup"><span data-stu-id="2043c-103">Run Azure PowerShell cmdlets in PowerShell Jobs</span></span>

<span data-ttu-id="2043c-104">O Azure PowerShell depende da conexão com uma nuvem do Azure e da espera de respostas. Portanto, a maioria desses cmdlets bloqueia a sessão do PowerShell até receber uma resposta da nuvem.</span><span class="sxs-lookup"><span data-stu-id="2043c-104">Azure PowerShell depends on connecting to an Azure cloud and waiting for responses, so most of these cmdlets block your PowerShell session until they get a response from the cloud.</span></span>
<span data-ttu-id="2043c-105">Os Trabalhos do Powershell permitem que você execute cmdlets no segundo plano ou realize várias tarefas no Azure de uma só vez, de dentro de uma única sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2043c-105">Powershell Jobs let you run cmdlets in the background or do multiple tasks on Azure at once, from inside a single PowerShell session.</span></span>

<span data-ttu-id="2043c-106">Este artigo é uma breve visão geral de como executar cmdlets do Azure PowerShell como Trabalhos do PowerShell e verificar a conclusão.</span><span class="sxs-lookup"><span data-stu-id="2043c-106">This article is a brief overview of how to run Azure PowerShell cmdlets as PowerShell Jobs and check for completion.</span></span> <span data-ttu-id="2043c-107">A execução de comandos no Azure PowerShell requer o uso de contextos do Azure PowerShell, abordados detalhadamente em [contextos e credenciais de entrada do Azure](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="2043c-107">Running commands in Azure PowerShell requires the use of Azure PowerShell contexts, which are covered in detail in [Azure contexts and sign-in credentials](context-persistence.md).</span></span>
<span data-ttu-id="2043c-108">Para saber mais sobre Trabalhos do PowerShell, confira [Sobre Trabalhos do PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="2043c-108">To learn more about PowerShell Jobs, see [About PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="azure-contexts-with-powershell-jobs"></a><span data-ttu-id="2043c-109">Contextos do Azure com trabalhos do PowerShell</span><span class="sxs-lookup"><span data-stu-id="2043c-109">Azure contexts with PowerShell jobs</span></span>

<span data-ttu-id="2043c-110">Os Trabalhos do PowerShell são executados como processos separados sem uma sessão do PowerShell anexada, portanto, suas credenciais do Azure devem ser compartilhadas com eles.</span><span class="sxs-lookup"><span data-stu-id="2043c-110">PowerShell Jobs are run as separate processes without an attached PowerShell session, so your Azure credentials must be shared with them.</span></span> <span data-ttu-id="2043c-111">As credenciais são passadas como objetos de contexto do Azure, usando um destes métodos:</span><span class="sxs-lookup"><span data-stu-id="2043c-111">Credentials are passed as Azure context objects, using one of these methods:</span></span>

* <span data-ttu-id="2043c-112">Persistência de contexto automática.</span><span class="sxs-lookup"><span data-stu-id="2043c-112">Automatic context persistence.</span></span> <span data-ttu-id="2043c-113">A persistência de contexto é habilitada por padrão e preserva suas informações de conexão em várias sessões.</span><span class="sxs-lookup"><span data-stu-id="2043c-113">Context persistence is enabled by default and preserves your sign-in information across multiple sessions.</span></span> <span data-ttu-id="2043c-114">Com a persistência de contexto habilitada, o contexto do Azure atual é passado para o novo processo:</span><span class="sxs-lookup"><span data-stu-id="2043c-114">With context persistence enabled, the current Azure context is passed to the new process:</span></span>

  ```azurepowershell-interactive
  Enable-AzContextAutosave # Enables context autosave if not already on
  $creds = Get-Credential
  $job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin } -ArgumentList $creds
  ```

* <span data-ttu-id="2043c-115">Use o parâmetro `-AzContext` com cmdlets do Azure PowerShell para fornecer um objeto de contexto do Azure:</span><span class="sxs-lookup"><span data-stu-id="2043c-115">Use the `-AzContext` parameter with any Azure PowerShell cmdlets to provide an Azure context object:</span></span>

  ```azurepowershell-interactive
  $context = Get-AzContext -Name 'mycontext' # Get an Azure context object
  $creds = Get-Credential
  $job = Start-Job { param($context, $vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList $context,$creds }
  ```

  <span data-ttu-id="2043c-116">Se a persistência de contexto estiver desabilitada, o argumento `-AzContext` será necessário.</span><span class="sxs-lookup"><span data-stu-id="2043c-116">If context persistence is disabled, the `-AzContext` argument is required.</span></span>

* <span data-ttu-id="2043c-117">Use a opção `-AsJob` fornecida por alguns cmdlets do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2043c-117">Use the `-AsJob` switch provided by some Azure PowerShell cmdlets.</span></span> <span data-ttu-id="2043c-118">Essa opção inicia automaticamente o cmdlet como um Trabalho do PowerShell, usando o contexto do Azure ativo no momento:</span><span class="sxs-lookup"><span data-stu-id="2043c-118">This switch automatically starts the cmdlet as a PowerShell Job, using the currently active Azure context:</span></span>

  ```azurepowershell-interactive
  $creds = Get-Credential
  $job = New-AzVM -Name MyVm -Credential $creds -AsJob
  ```

  <span data-ttu-id="2043c-119">Para ver se um cmdlet dá suporte ao `-AsJob`, confira sua documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="2043c-119">To see if a cmdlet supports `-AsJob`, check its reference documentation.</span></span> <span data-ttu-id="2043c-120">A opção `-AsJob` não requer que o salvamento automático de contexto seja habilitado.</span><span class="sxs-lookup"><span data-stu-id="2043c-120">The `-AsJob` switch doesn't require context autosave to be enabled.</span></span>

<span data-ttu-id="2043c-121">Você pode verificar o status de um trabalho em execução com o cmdlet [Get-Job](/powershell/module/microsoft.powershell.core/get-job).</span><span class="sxs-lookup"><span data-stu-id="2043c-121">You can check the status of a running job with the [Get-Job](/powershell/module/microsoft.powershell.core/get-job) cmdlet.</span></span> <span data-ttu-id="2043c-122">Para obter a saída de um trabalho até o momento, use o cmdlet [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job).</span><span class="sxs-lookup"><span data-stu-id="2043c-122">To get the output from a job so far, use the [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job) cmdlet.</span></span>

<span data-ttu-id="2043c-123">Para verificar o progresso de uma operação remotamente no Azure, use os cmdlets `Get-` associados ao tipo de recurso que está sendo modificado pelo trabalho:</span><span class="sxs-lookup"><span data-stu-id="2043c-123">To check an operation's progress remotely on Azure, use the `Get-` cmdlets associated with the type of resource being modified by the job:</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$context = Get-AzContext -Name 'mycontext'
$vmName = "MyVm"

$job = Start-Job { param($context, $vmName, $vmadmin) New-AzVM -Name $vmName -AzContext $context -Credential $vmadmin} -ArgumentList $context,$vmName,$creds }

Get-Job $job
Get-AzVM -Name $vmName
```

## <a name="see-also"></a><span data-ttu-id="2043c-124">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="2043c-124">See Also</span></span>

* [<span data-ttu-id="2043c-125">Contextos do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="2043c-125">Azure PowerShell contexts</span></span>](context-persistence.md)
* [<span data-ttu-id="2043c-126">Sobre Trabalhos do PowerShell</span><span class="sxs-lookup"><span data-stu-id="2043c-126">About PowerShell Jobs</span></span>](/powershell/module/microsoft.powershell.core/about/about_jobs)
* [<span data-ttu-id="2043c-127">Referência Get-Job</span><span class="sxs-lookup"><span data-stu-id="2043c-127">Get-Job reference</span></span>](/powershell/module/microsoft.powershell.core/get-job)
* [<span data-ttu-id="2043c-128">Referência Receive-Job</span><span class="sxs-lookup"><span data-stu-id="2043c-128">Receive-Job reference</span></span>](/powershell/module/microsoft.powershell.core/receive-job)
