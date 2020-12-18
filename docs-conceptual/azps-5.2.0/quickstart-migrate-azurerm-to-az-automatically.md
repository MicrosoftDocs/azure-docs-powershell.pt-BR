---
title: Migrar automaticamente os scripts do PowerShell do AzureRM para o módulo Az do PowerShell
description: Saiba como migrar automaticamente os scripts do PowerShell do AzureRM para o módulo Az do PowerShell.
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 12/10/2020
ms.openlocfilehash: 6752fa0376c2f8887511455f56add0859f8961c8
ms.sourcegitcommit: 076ff98abc48e072eb1727532817487bac7507c6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/15/2020
ms.locfileid: "97488522"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a><span data-ttu-id="3d436-103">Início Rápido: Migrar automaticamente os scripts do PowerShell do AzureRM para o módulo Az do PowerShell</span><span class="sxs-lookup"><span data-stu-id="3d436-103">Quickstart: Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module</span></span>

<span data-ttu-id="3d436-104">Neste artigo, você aprenderá a usar o módulo Az.Tools.Migration do PowerShell para atualizar automaticamente os scripts do PowerShell e os módulos de script do AzureRM para o módulo Az do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3d436-104">In this article, you'll learn how to use the Az.Tools.Migration PowerShell module to automatically upgrade your PowerShell scripts and script modules from AzureRM to the Az PowerShell module.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3d436-105">O módulo Az.Tools.Migration do PowerShell está atualmente em versão prévia pública.</span><span class="sxs-lookup"><span data-stu-id="3d436-105">The Az.Tools.Migration PowerShell module is currently in public preview.</span></span> <span data-ttu-id="3d436-106">A versão prévia é fornecida sem um contrato de nível de serviço.</span><span class="sxs-lookup"><span data-stu-id="3d436-106">This preview version is provided without a service level agreement.</span></span> <span data-ttu-id="3d436-107">Ela não é recomendada para cargas de trabalho de produção.</span><span class="sxs-lookup"><span data-stu-id="3d436-107">It's not recommended for production workloads.</span></span> <span data-ttu-id="3d436-108">Alguns recursos podem não ter suporte ou podem ter restrição de recursos.</span><span class="sxs-lookup"><span data-stu-id="3d436-108">Certain features might not be supported or might have constrained capabilities.</span></span> <span data-ttu-id="3d436-109">Para obter mais informações, consulte [Termos de Uso Complementares de Versões Prévias do Microsoft Azure](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span><span class="sxs-lookup"><span data-stu-id="3d436-109">For more information, see [Supplemental Terms of Use for Microsoft Azure Previews](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span></span>

## <a name="requirements"></a><span data-ttu-id="3d436-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d436-110">Requirements</span></span>

* <span data-ttu-id="3d436-111">Atualize os scripts do PowerShell existentes para a versão mais recente do [módulo AzureRM do PowerShell (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span><span class="sxs-lookup"><span data-stu-id="3d436-111">Update your existing PowerShell scripts to the latest version of the [AzureRM PowerShell module (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span>
* <span data-ttu-id="3d436-112">Instale o módulo Az.Tools.Migration do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3d436-112">Install the Az.Tools.Migration PowerShell module.</span></span>

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a><span data-ttu-id="3d436-113">Etapa 1: gerar um plano de atualização</span><span class="sxs-lookup"><span data-stu-id="3d436-113">Step 1: Generate an upgrade plan</span></span>

<span data-ttu-id="3d436-114">Você usa o cmdlet **`New-AzUpgradeModulePlan`** para gerar um plano de atualização a fim de migrar os scripts e módulos para o módulo Az do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3d436-114">You use the **`New-AzUpgradeModulePlan`** cmdlet to generate an upgrade plan for migrating your scripts and modules to the Az PowerShell module.</span></span> <span data-ttu-id="3d436-115">Esse cmdlet não faz nenhuma alteração em seus scripts existentes.</span><span class="sxs-lookup"><span data-stu-id="3d436-115">This cmdlet doesn’t make any changes to your existing scripts.</span></span> <span data-ttu-id="3d436-116">Use o parâmetro **`FilePath`** para direcionar um script específico ou o parâmetro **`DirectoryPath`** para direcionar todos os scripts em uma pasta específica.</span><span class="sxs-lookup"><span data-stu-id="3d436-116">Use the **`FilePath`** parameter for targeting a specific script or the **`DirectoryPath`** parameter for targeting all scripts in a specific folder.</span></span>

> [!NOTE]
> <span data-ttu-id="3d436-117">O cmdlet **`New-AzUpgradeModulePlan`** não executa o plano, ele apenas gera as etapas de atualização.</span><span class="sxs-lookup"><span data-stu-id="3d436-117">The **`New-AzUpgradeModulePlan`** cmdlet doesn't execute the plan, it only generates the upgrade steps.</span></span>

<span data-ttu-id="3d436-118">O exemplo a seguir gera um plano para todos os scripts na pasta _`C:\Scripts`_ .</span><span class="sxs-lookup"><span data-stu-id="3d436-118">The following example generates a plan for all the scripts in the _`C:\Scripts`_ folder.</span></span> <span data-ttu-id="3d436-119">O parâmetro **`OutVariable`** é especificado para que os resultados sejam retornados e armazenados simultaneamente em uma variável chamada **`Plan`** .</span><span class="sxs-lookup"><span data-stu-id="3d436-119">The **`OutVariable`** parameter is specified so the results are returned and simultaneously stored in a variable named **`Plan`**.</span></span>

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts' -OutVariable Plan
```

<span data-ttu-id="3d436-120">Conforme mostrado na saída a seguir, o plano de atualização detalha o arquivo específico e os pontos de deslocamento que necessitam de alterações ao migrar os cmdlets do AzureRM para o módulo Az do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3d436-120">As shown in the following output, the upgrade plan details the specific file and offset points that require changes when moving from AzureRM to the Az PowerShell cmdlets.</span></span>

```Output
Order Location                                                   UpgradeType     PlanResult             Original
----- --------                                                   -----------     ----------             --------
1     compute-create-dockerhost.ps1:59:24                        CmdletParameter ReadyToUpgrade         ExtensionName
2     compute-create-dockerhost.ps1:59:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
3     compute-create-dockerhost.ps1:54:1                         Cmdlet          ReadyToUpgrade         New-AzureRmVM
4     compute-create-dockerhost.ps1:51:1                         Cmdlet          ReadyToUpgrade         Add-AzureRmVM...
5     compute-create-dockerhost.ps1:47:1                         Cmdlet          ReadyToUpgrade         Add-AzureRmVM...
6     compute-create-dockerhost.ps1:46:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
7     compute-create-dockerhost.ps1:45:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
8     compute-create-dockerhost.ps1:44:13                        Cmdlet          ReadyToUpgrade         New-AzureRmVM...
9     compute-create-dockerhost.ps1:40:8                         Cmdlet          ReadyToUpgrade         New-AzureRmNe...
10    compute-create-dockerhost.ps1:36:8                         Cmdlet          ReadyToUpgrade         New-AzureRmNe...
11    compute-create-dockerhost.ps1:31:16                        Cmdlet          ReadyToUpgrade         New-AzureRmNe...
12    compute-create-dockerhost.ps1:26:15                        Cmdlet          ReadyToUpgrade         New-AzureRmNe...
13    compute-create-dockerhost.ps1:22:8                         Cmdlet          ReadyToUpgrade         New-AzureRmPu...
14    compute-create-dockerhost.ps1:18:9                         Cmdlet          ReadyToUpgrade         New-AzureRmVi...
15    compute-create-dockerhost.ps1:15:17                        Cmdlet          ReadyToUpgrade         New-AzureRmVi...
16    compute-create-dockerhost.ps1:12:1                         Cmdlet          ReadyToUpgrade         New-AzureRmRe...
17    compute-create-windowsvm-quick.ps1:18:3                    CmdletParameter ReadyToUpgrade         ImageName
18    compute-create-windowsvm-quick.ps1:14:1                    Cmdlet          ReadyToUpgrade         New-AzureRmVM
19    compute-create-windowsvm-quick.ps1:11:1                    Cmdlet          ReadyToUpgrade         New-AzureRmRe...
20    compute-create-wordpress-mysql.ps1:59:24                   CmdletParameter ReadyToUpgrade         ExtensionName
...
```

<span data-ttu-id="3d436-121">Antes de executar a atualização, você precisa exibir os resultados do plano para ver se há problemas.</span><span class="sxs-lookup"><span data-stu-id="3d436-121">Before performing the upgrade, you need to view the results of the plan for problems.</span></span> <span data-ttu-id="3d436-122">O exemplo a seguir retorna uma lista de scripts e os itens desses scripts que os impedirão de serem atualizados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3d436-122">The following example returns a list of scripts and the items in those scripts that will prevent them from being upgraded automatically.</span></span>

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

<span data-ttu-id="3d436-123">Os itens mostrados na saída a seguir não serão atualizados automaticamente sem primeiro corrigir manualmente os problemas.</span><span class="sxs-lookup"><span data-stu-id="3d436-123">The items shown in the following output will not be upgraded automatically without manually correcting the issues first.</span></span> <span data-ttu-id="3d436-124">Os problemas conhecidos que não podem ser atualizados automaticamente incluem comandos que usam nivelamento.</span><span class="sxs-lookup"><span data-stu-id="3d436-124">Known issues that can’t be upgraded automatically include any commands that use splatting.</span></span>

```Output
Order                  : 42
UpgradeType            : CmdletParameter
PlanResult             : ErrorParameterNotFound
PlanSeverity           : Error
PlanResultReason       : Parameter was not found in Get-AzResource or it's aliases.
SourceCommand          : CommandReference
SourceCommandParameter : CommandReferenceParameter
Location               : devtestlab-add-marketplace-image-to-lab.ps1:14:74
FullPath               : C:\Scripts\devtestlab-add-marketplace-image-to-lab.ps1
StartOffset            : 556
Original               : ResourceNameEquals
Replacement            :
```

## <a name="step-2-perform-the-upgrade"></a><span data-ttu-id="3d436-125">Etapa 2: Realizar a atualização</span><span class="sxs-lookup"><span data-stu-id="3d436-125">Step 2: Perform the upgrade</span></span>

> [!CAUTION]
> <span data-ttu-id="3d436-126">Não há a opção de desfazer.</span><span class="sxs-lookup"><span data-stu-id="3d436-126">There is no undo operation.</span></span> <span data-ttu-id="3d436-127">Sempre verifique se você tem uma cópia de backup dos módulos e scripts do PowerShell que está tentando atualizar.</span><span class="sxs-lookup"><span data-stu-id="3d436-127">Always ensure that you have a backup copy of your PowerShell scripts and modules that you're attempting to upgrade.</span></span>

<span data-ttu-id="3d436-128">Quando você estiver satisfeito com o plano, a atualização será executada com o cmdlet **`Invoke-AzUpgradeModulePlan`** .</span><span class="sxs-lookup"><span data-stu-id="3d436-128">After you’re satisfied with the plan, the upgrade is performed with the **`Invoke-AzUpgradeModulePlan`** cmdlet.</span></span> <span data-ttu-id="3d436-129">Especifique **`SaveChangesToNewFiles`** para o valor do parâmetro **`FileEditMode`** para impedir que as alterações sejam feitas nos scripts originais.</span><span class="sxs-lookup"><span data-stu-id="3d436-129">Specify **`SaveChangesToNewFiles`** for the **`FileEditMode`** parameter value to prevent changes from being made to your original scripts.</span></span> <span data-ttu-id="3d436-130">Ao usar esse modo, a atualização será executada criando uma cópia de cada script direcionado com _`_az_upgraded`_ acrescentado aos nomes de arquivo.</span><span class="sxs-lookup"><span data-stu-id="3d436-130">When using this mode, the upgrade is performed by creating a copy of each script targeted with _`_az_upgraded`_ appended to the filenames.</span></span>

> [!WARNING]
> <span data-ttu-id="3d436-131">O cmdlet **`Invoke-AzUpgradeModulePlan`** é destrutivo quando a opção **`-FileEditMode ModifyExistingFiles`** é especificada.</span><span class="sxs-lookup"><span data-stu-id="3d436-131">The **`Invoke-AzUpgradeModulePlan`** cmdlet is destructive when the **`-FileEditMode ModifyExistingFiles`** option is specified!</span></span> <span data-ttu-id="3d436-132">Ele modifica seus scripts e funções em vigor, de acordo com o plano de atualização do módulo gerado pelo cmdlet **`New-AzUpgradeModulePlan`** .</span><span class="sxs-lookup"><span data-stu-id="3d436-132">It modifies your scripts and functions in place according to the module upgrade plan generated by the **`New-AzUpgradeModulePlan`** cmdlet.</span></span> <span data-ttu-id="3d436-133">Para a opção não destrutiva, especifique **`-FileEditMode SaveChangesToNewFiles`** .</span><span class="sxs-lookup"><span data-stu-id="3d436-133">For the non-destructive option specify **`-FileEditMode SaveChangesToNewFiles`** instead.</span></span>

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles -OutVariable Results
```

```Output
Order Location                                                   UpgradeType     UpgradeResult    Original
----- --------                                                   -----------     -------------    --------
1     compute-create-dockerhost.ps1:59:24                        CmdletParameter UpgradeCompleted ExtensionName
2     compute-create-dockerhost.ps1:59:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMExtens...
3     compute-create-dockerhost.ps1:54:1                         Cmdlet          UpgradeCompleted New-AzureRmVM
4     compute-create-dockerhost.ps1:51:1                         Cmdlet          UpgradeCompleted Add-AzureRmVMSshPub...
5     compute-create-dockerhost.ps1:47:1                         Cmdlet          UpgradeCompleted Add-AzureRmVMNetwor...
6     compute-create-dockerhost.ps1:46:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMSource...
7     compute-create-dockerhost.ps1:45:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMOperat...
8     compute-create-dockerhost.ps1:44:13                        Cmdlet          UpgradeCompleted New-AzureRmVMConfig
9     compute-create-dockerhost.ps1:40:8                         Cmdlet          UpgradeCompleted New-AzureRmNetworkI...
10    compute-create-dockerhost.ps1:36:8                         Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
11    compute-create-dockerhost.ps1:31:16                        Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
12    compute-create-dockerhost.ps1:26:15                        Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
13    compute-create-dockerhost.ps1:22:8                         Cmdlet          UpgradeCompleted New-AzureRmPublicIp...
14    compute-create-dockerhost.ps1:18:9                         Cmdlet          UpgradeCompleted New-AzureRmVirtualN...
15    compute-create-dockerhost.ps1:15:17                        Cmdlet          UpgradeCompleted New-AzureRmVirtualN...
16    compute-create-dockerhost.ps1:12:1                         Cmdlet          UpgradeCompleted New-AzureRmResource...
17    compute-create-windowsvm-quick.ps1:18:3                    CmdletParameter UpgradeCompleted ImageName
18    compute-create-windowsvm-quick.ps1:14:1                    Cmdlet          UpgradeCompleted New-AzureRmVM
19    compute-create-windowsvm-quick.ps1:11:1                    Cmdlet          UpgradeCompleted New-AzureRmResource...
20    compute-create-wordpress-mysql.ps1:59:24                   CmdletParameter UpgradeCompleted ExtensionName
...
```

<span data-ttu-id="3d436-134">Se algum erro for retornado, você poderá examinar mais atentamente os resultados do erro com o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="3d436-134">If any errors are returned, you can take a closer look at the error results with the following command:</span></span>

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

```Output
Order                  : 42
UpgradeType            : CmdletParameter
UpgradeResult          : UnableToUpgrade
UpgradeSeverity        : Error
UpgradeResultReason    : Parameter was not found in Get-AzResource or it's aliases.
SourceCommand          : CommandReference
SourceCommandParameter : CommandReferenceParameter
Location               : devtestlab-add-marketplace-image-to-lab.ps1:14:74
FullPath               : C:\Scripts\devtestlab-add-marketplace-image-to-lab.ps1
StartOffset            : 556
Original               : ResourceNameEquals
Replacement            :
```

## <a name="limitations"></a><span data-ttu-id="3d436-135">Limitações</span><span class="sxs-lookup"><span data-stu-id="3d436-135">Limitations</span></span>

* <span data-ttu-id="3d436-136">Não há suporte para atualizações de nome de parâmetro automatizadas para conjuntos de parâmetros com splatting.</span><span class="sxs-lookup"><span data-stu-id="3d436-136">Automated parameter name updates to splatted parameter sets aren't supported.</span></span> <span data-ttu-id="3d436-137">Se algum for encontrado durante a geração do plano de atualização, um aviso será retornado.</span><span class="sxs-lookup"><span data-stu-id="3d436-137">If any are found during upgrade plan generation, a warning is returned.</span></span>
* <span data-ttu-id="3d436-138">As operações de E/S de arquivo usam a codificação padrão.</span><span class="sxs-lookup"><span data-stu-id="3d436-138">File I/O operations use default encoding.</span></span> <span data-ttu-id="3d436-139">Situações incomuns de codificação de arquivo podem causar problemas.</span><span class="sxs-lookup"><span data-stu-id="3d436-139">Unusual file encoding situations may cause problems.</span></span>
* <span data-ttu-id="3d436-140">Os cmdlets do AzureRM passados como argumentos para as instruções de simulação de teste de unidade do Pester não foram detectados.</span><span class="sxs-lookup"><span data-stu-id="3d436-140">AzureRM cmdlets passed as arguments to Pester unit test mock statements aren't detected.</span></span>
* <span data-ttu-id="3d436-141">Atualmente, somente o módulo Az do PowerShell versão 4.6.1 tem suporte como destino.</span><span class="sxs-lookup"><span data-stu-id="3d436-141">Currently, only Az PowerShell module version 4.6.1 is supported as a target.</span></span>

## <a name="how-to-report-issues"></a><span data-ttu-id="3d436-142">Como relatar problemas</span><span class="sxs-lookup"><span data-stu-id="3d436-142">How to report issues</span></span>

<span data-ttu-id="3d436-143">Relate comentários e problemas sobre o módulo Az.Tools.Migration do PowerShell por meio de [um problema do GitHub](https://github.com/Azure/azure-powershell-migration/issues) no repositório `azure-powershell-migration`.</span><span class="sxs-lookup"><span data-stu-id="3d436-143">Report feedback and issues about the Az.Tools.Migration PowerShell module via [a GitHub issue](https://github.com/Azure/azure-powershell-migration/issues) in the `azure-powershell-migration` repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="3d436-144">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="3d436-144">Next steps</span></span>

<span data-ttu-id="3d436-145">Para obter mais informações sobre o módulo Az do PowerShell, confira a [documentação do Azure PowerShell](/powershell/azure/)</span><span class="sxs-lookup"><span data-stu-id="3d436-145">To learn more about the Az PowerShell module, see the [Azure PowerShell documentation](/powershell/azure/)</span></span>