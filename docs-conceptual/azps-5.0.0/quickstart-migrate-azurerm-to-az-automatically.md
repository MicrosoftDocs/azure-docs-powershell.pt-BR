---
title: Migrar automaticamente os scripts do PowerShell do AzureRM para o módulo Az do PowerShell
description: Saiba como migrar automaticamente os scripts do PowerShell do AzureRM para o módulo Az do PowerShell.
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 09/11/2020
ms.openlocfilehash: d342ca65baf7664f430de3b7d294c0fc9815c0a0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92753337"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a><span data-ttu-id="5811b-103">Início Rápido: Migrar automaticamente os scripts do PowerShell do AzureRM para o módulo Az do PowerShell</span><span class="sxs-lookup"><span data-stu-id="5811b-103">Quickstart: Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module</span></span>

<span data-ttu-id="5811b-104">Neste artigo, você aprenderá a usar o módulo Az.Tools.Migration do PowerShell para atualizar automaticamente os scripts do PowerShell e os módulos de script do AzureRM para o módulo Az do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5811b-104">In this article, you'll learn how to use the Az.Tools.Migration PowerShell module to automatically upgrade your PowerShell scripts and script modules from AzureRM to the Az PowerShell module.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5811b-105">O módulo Az.Tools.Migration do PowerShell está atualmente em versão prévia pública.</span><span class="sxs-lookup"><span data-stu-id="5811b-105">The Az.Tools.Migration PowerShell module is currently in public preview.</span></span> <span data-ttu-id="5811b-106">A versão prévia é fornecida sem um contrato de nível de serviço.</span><span class="sxs-lookup"><span data-stu-id="5811b-106">This preview version is provided without a service level agreement.</span></span> <span data-ttu-id="5811b-107">Ela não é recomendada para cargas de trabalho de produção.</span><span class="sxs-lookup"><span data-stu-id="5811b-107">It's not recommended for production workloads.</span></span> <span data-ttu-id="5811b-108">Alguns recursos podem não ter suporte ou podem ter restrição de recursos.</span><span class="sxs-lookup"><span data-stu-id="5811b-108">Certain features might not be supported or might have constrained capabilities.</span></span> <span data-ttu-id="5811b-109">Para obter mais informações, consulte [Termos de Uso Complementares de Versões Prévias do Microsoft Azure](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span><span class="sxs-lookup"><span data-stu-id="5811b-109">For more information, see [Supplemental Terms of Use for Microsoft Azure Previews](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span></span>

<span data-ttu-id="5811b-110">Relate comentários e problemas sobre o módulo Az.Tools.Migration do PowerShell por meio de [um problema do GitHub](https://github.com/Azure/azure-powershell-migration/issues) no repositório `azure-powershell-migration`.</span><span class="sxs-lookup"><span data-stu-id="5811b-110">Report feedback and issues about the Az.Tools.Migration PowerShell module via [a GitHub issue](https://github.com/Azure/azure-powershell-migration/issues) in the `azure-powershell-migration` repository.</span></span>

## <a name="requirements"></a><span data-ttu-id="5811b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5811b-111">Requirements</span></span>

* <span data-ttu-id="5811b-112">Atualize os scripts do PowerShell existentes para a versão mais recente do [módulo AzureRM do PowerShell (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span><span class="sxs-lookup"><span data-stu-id="5811b-112">Update your existing PowerShell scripts to the latest version of the [AzureRM PowerShell module (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span>
* <span data-ttu-id="5811b-113">Instale o módulo Az.Tools.Migration do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5811b-113">Install the Az.Tools.Migration PowerShell module.</span></span>

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a><span data-ttu-id="5811b-114">Etapa 1: gerar um plano de atualização</span><span class="sxs-lookup"><span data-stu-id="5811b-114">Step 1: Generate an upgrade plan</span></span>

<span data-ttu-id="5811b-115">Use o cmdlet `New-AzUpgradeModulePlan` para gerar um plano de atualização a fim de migrar os scripts e módulos para o módulo Az do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5811b-115">You use the `New-AzUpgradeModulePlan` cmdlet to generate an upgrade plan for migrating your scripts and modules to the Az PowerShell module.</span></span> <span data-ttu-id="5811b-116">O plano de atualização detalha o arquivo específico e os pontos de deslocamento que necessitam de alterações ao migrar os cmdlets do AzureRM para o módulo Az do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5811b-116">The upgrade plan details the specific file and offset points that require changes when moving from AzureRM to the Az PowerShell cmdlets.</span></span>

> [!NOTE]
> <span data-ttu-id="5811b-117">O cmdlet `New-AzUpgradeModulePlan` não executa o plano, ele apenas gera as etapas de atualização.</span><span class="sxs-lookup"><span data-stu-id="5811b-117">The `New-AzUpgradeModulePlan` cmdlet doesn't execute the plan, it only generates the upgrade steps.</span></span>

```powershell
#  Generate an upgrade plan for the specified PowerShell script and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -FilePath 'C:\Scripts\my-azure-script.ps1'
```

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts'
```

<span data-ttu-id="5811b-118">Revise os resultados do plano de atualização.</span><span class="sxs-lookup"><span data-stu-id="5811b-118">Review the results of the upgrade plan.</span></span>

```powershell
# Show the entire upgrade plan
$Plan
```

<span data-ttu-id="5811b-119">Execute o comando a seguir para filtrar os resultados de comandos que tenham avisos ou erros.</span><span class="sxs-lookup"><span data-stu-id="5811b-119">Run the following command to filter the results to commands that have warnings or errors.</span></span> <span data-ttu-id="5811b-120">Isso pode ser útil em grandes conjuntos de resultados para identificar rapidamente os erros antes de executar a atualização.</span><span class="sxs-lookup"><span data-stu-id="5811b-120">This may be helpful on large result sets to quickly identify errors before performing the upgrade.</span></span>

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

## <a name="step-2-perform-the-upgrade"></a><span data-ttu-id="5811b-121">Etapa 2: Realizar a atualização</span><span class="sxs-lookup"><span data-stu-id="5811b-121">Step 2: Perform the upgrade</span></span>

<span data-ttu-id="5811b-122">O plano de atualização é executado quando você executa o cmdlet `Invoke-AzUpgradeModulePlan`.</span><span class="sxs-lookup"><span data-stu-id="5811b-122">The upgrade plan is executed when you run the `Invoke-AzUpgradeModulePlan` cmdlet.</span></span> <span data-ttu-id="5811b-123">Esse comando executa uma atualização do arquivo ou das pastas especificadas, exceto os erros identificados pelo cmdlet `New-AzUpgradeModulePlan`.</span><span class="sxs-lookup"><span data-stu-id="5811b-123">This command performs an upgrade of the specified file or folders except for any errors that were identified by the `New-AzUpgradeModulePlan` cmdlet.</span></span>

<span data-ttu-id="5811b-124">Esse comando exige que você especifique se os arquivos devem ser modificados no local ou se novos arquivos devem ser salvos junto com os arquivos originais (deixando os originais inalterados).</span><span class="sxs-lookup"><span data-stu-id="5811b-124">This command requires you to specify if the files should be modified in place or if new files should be saved alongside your original files (leaving originals unmodified).</span></span>

> [!CAUTION]
> <span data-ttu-id="5811b-125">Não há a opção de desfazer.</span><span class="sxs-lookup"><span data-stu-id="5811b-125">There is no undo operation.</span></span> <span data-ttu-id="5811b-126">Sempre verifique se você tem uma cópia de backup dos módulos e scripts do PowerShell que está tentando atualizar.</span><span class="sxs-lookup"><span data-stu-id="5811b-126">Always ensure that you have a backup copy of your PowerShell scripts and modules that you're attempting to upgrade.</span></span>

> [!WARNING]
> <span data-ttu-id="5811b-127">O cmdlet `Invoke-AzUpgradeModulePlan` é destrutivo quando a opção `-FileEditMode ModifyExistingFiles` é especificada.</span><span class="sxs-lookup"><span data-stu-id="5811b-127">The `Invoke-AzUpgradeModulePlan` cmdlet is destructive when the `-FileEditMode ModifyExistingFiles` option is specified!</span></span> <span data-ttu-id="5811b-128">Ele modifica os scripts e as funções em vigor, de acordo com o plano de atualização do módulo gerado pelo cmdlet `New-AzUpgradeModulePlan`.</span><span class="sxs-lookup"><span data-stu-id="5811b-128">It modifies your scripts and functions in place according to the module upgrade plan generated by the `New-AzUpgradeModulePlan` cmdlet.</span></span> <span data-ttu-id="5811b-129">Para a opção não destrutiva, especifique `-FileEditMode SaveChangesToNewFiles`.</span><span class="sxs-lookup"><span data-stu-id="5811b-129">For the non-destructive option specify `-FileEditMode SaveChangesToNewFiles` instead.</span></span>

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
$Results = Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles
```

<span data-ttu-id="5811b-130">Revise os resultados da operação de atualização.</span><span class="sxs-lookup"><span data-stu-id="5811b-130">Review the results of the upgrade operation.</span></span>

```powershell
# Show the results for the entire upgrade operation
$Results
```

<span data-ttu-id="5811b-131">Se algum erro for retornado, você poderá examinar mais atentamente os resultados do erro com o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="5811b-131">If any errors are returned, you can take a closer look at the error results with the following command:</span></span>

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

## <a name="limitations"></a><span data-ttu-id="5811b-132">Limitações</span><span class="sxs-lookup"><span data-stu-id="5811b-132">Limitations</span></span>

* <span data-ttu-id="5811b-133">Não há suporte para atualizações de nome de parâmetro automatizadas para conjuntos de parâmetros com splatting.</span><span class="sxs-lookup"><span data-stu-id="5811b-133">Automated parameter name updates to splatted parameter sets aren't supported.</span></span> <span data-ttu-id="5811b-134">Se algum for encontrado durante a geração do plano de atualização, um aviso será retornado.</span><span class="sxs-lookup"><span data-stu-id="5811b-134">If any are found during upgrade plan generation, a warning is returned.</span></span>
* <span data-ttu-id="5811b-135">As operações de E/S de arquivo usam a codificação padrão.</span><span class="sxs-lookup"><span data-stu-id="5811b-135">File I/O operations use default encoding.</span></span> <span data-ttu-id="5811b-136">Situações incomuns de codificação de arquivo podem causar problemas.</span><span class="sxs-lookup"><span data-stu-id="5811b-136">Unusual file encoding situations may cause problems.</span></span>
* <span data-ttu-id="5811b-137">Os cmdlets do AzureRM passados como argumentos para as instruções de simulação de teste de unidade do Pester não foram detectados.</span><span class="sxs-lookup"><span data-stu-id="5811b-137">AzureRM cmdlets passed as arguments to Pester unit test mock statements aren't detected.</span></span>
* <span data-ttu-id="5811b-138">Atualmente, somente o módulo Az do PowerShell versão 4.6.1 tem suporte como destino.</span><span class="sxs-lookup"><span data-stu-id="5811b-138">Currently, only Az PowerShell module version 4.6.1 is supported as a target.</span></span>

## <a name="next-steps"></a><span data-ttu-id="5811b-139">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="5811b-139">Next steps</span></span>

<span data-ttu-id="5811b-140">Para obter mais informações sobre o módulo Az do PowerShell, confira a [documentação do Azure PowerShell](https://docs.microsoft.com/powershell/azure/)</span><span class="sxs-lookup"><span data-stu-id="5811b-140">To learn more about the Az PowerShell module, see the [Azure PowerShell documentation](https://docs.microsoft.com/powershell/azure/)</span></span>