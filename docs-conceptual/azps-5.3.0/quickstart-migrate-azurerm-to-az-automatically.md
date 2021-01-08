---
title: Migrar automaticamente os scripts do PowerShell do AzureRM para o módulo Az do PowerShell
description: Saiba como migrar automaticamente os scripts do PowerShell do AzureRM para o módulo Az do PowerShell.
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 12/18/2020
ms.openlocfilehash: 57218c130f172bc359334b83db16e5790fa5562c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "97893458"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a><span data-ttu-id="b738c-103">Início Rápido: Migrar automaticamente os scripts do PowerShell do AzureRM para o módulo Az do PowerShell</span><span class="sxs-lookup"><span data-stu-id="b738c-103">Quickstart: Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module</span></span>

<span data-ttu-id="b738c-104">Neste artigo, você aprenderá a usar o módulo Az.Tools.Migration do PowerShell para atualizar automaticamente os scripts do PowerShell e os módulos de script do AzureRM para o módulo Az do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b738c-104">In this article, you'll learn how to use the Az.Tools.Migration PowerShell module to automatically upgrade your PowerShell scripts and script modules from AzureRM to the Az PowerShell module.</span></span> <span data-ttu-id="b738c-105">Para obter outras opções de migração, confira [Migrar o Azure PowerShell do AzureRM para o Az](/powershell/azure/migrate-from-azurerm-to-az).</span><span class="sxs-lookup"><span data-stu-id="b738c-105">For additional migration options, see [Migrate Azure PowerShell from AzureRM to Az](/powershell/azure/migrate-from-azurerm-to-az).</span></span>

## <a name="requirements"></a><span data-ttu-id="b738c-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b738c-106">Requirements</span></span>

* <span data-ttu-id="b738c-107">Atualize os scripts do PowerShell existentes para a versão mais recente do [módulo AzureRM do PowerShell (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span><span class="sxs-lookup"><span data-stu-id="b738c-107">Update your existing PowerShell scripts to the latest version of the [AzureRM PowerShell module (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span>
* <span data-ttu-id="b738c-108">Instale o módulo Az.Tools.Migration do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b738c-108">Install the Az.Tools.Migration PowerShell module.</span></span>

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a><span data-ttu-id="b738c-109">Etapa 1: gerar um plano de atualização</span><span class="sxs-lookup"><span data-stu-id="b738c-109">Step 1: Generate an upgrade plan</span></span>

<span data-ttu-id="b738c-110">Você usa o cmdlet **`New-AzUpgradeModulePlan`** para gerar um plano de atualização a fim de migrar os scripts e módulos para o módulo Az do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b738c-110">You use the **`New-AzUpgradeModulePlan`** cmdlet to generate an upgrade plan for migrating your scripts and modules to the Az PowerShell module.</span></span> <span data-ttu-id="b738c-111">Esse cmdlet não faz nenhuma alteração em seus scripts existentes.</span><span class="sxs-lookup"><span data-stu-id="b738c-111">This cmdlet doesn’t make any changes to your existing scripts.</span></span> <span data-ttu-id="b738c-112">Use o parâmetro **`FilePath`** para direcionar um script específico ou o parâmetro **`DirectoryPath`** para direcionar todos os scripts em uma pasta específica.</span><span class="sxs-lookup"><span data-stu-id="b738c-112">Use the **`FilePath`** parameter for targeting a specific script or the **`DirectoryPath`** parameter for targeting all scripts in a specific folder.</span></span>

> [!NOTE]
> <span data-ttu-id="b738c-113">O cmdlet **`New-AzUpgradeModulePlan`** não executa o plano, ele apenas gera as etapas de atualização.</span><span class="sxs-lookup"><span data-stu-id="b738c-113">The **`New-AzUpgradeModulePlan`** cmdlet doesn't execute the plan, it only generates the upgrade steps.</span></span>

<span data-ttu-id="b738c-114">O exemplo a seguir gera um plano para todos os scripts na pasta _`C:\Scripts`_ .</span><span class="sxs-lookup"><span data-stu-id="b738c-114">The following example generates a plan for all the scripts in the _`C:\Scripts`_ folder.</span></span> <span data-ttu-id="b738c-115">O parâmetro **`OutVariable`** é especificado para que os resultados sejam retornados e armazenados simultaneamente em uma variável chamada **`Plan`** .</span><span class="sxs-lookup"><span data-stu-id="b738c-115">The **`OutVariable`** parameter is specified so the results are returned and simultaneously stored in a variable named **`Plan`**.</span></span>

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 5.2.0 -DirectoryPath 'C:\Scripts' -OutVariable Plan
```

<span data-ttu-id="b738c-116">Conforme mostrado na saída a seguir, o plano de atualização detalha o arquivo específico e os pontos de deslocamento que necessitam de alterações ao migrar os cmdlets do AzureRM para o módulo Az do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b738c-116">As shown in the following output, the upgrade plan details the specific file and offset points that require changes when moving from AzureRM to the Az PowerShell cmdlets.</span></span>

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

<span data-ttu-id="b738c-117">Antes de executar a atualização, você precisa exibir os resultados do plano para ver se há problemas.</span><span class="sxs-lookup"><span data-stu-id="b738c-117">Before performing the upgrade, you need to view the results of the plan for problems.</span></span> <span data-ttu-id="b738c-118">O exemplo a seguir retorna uma lista de scripts e os itens desses scripts que os impedirão de serem atualizados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b738c-118">The following example returns a list of scripts and the items in those scripts that will prevent them from being upgraded automatically.</span></span>

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

<span data-ttu-id="b738c-119">Os itens mostrados na saída a seguir não serão atualizados automaticamente sem primeiro corrigir manualmente os problemas.</span><span class="sxs-lookup"><span data-stu-id="b738c-119">The items shown in the following output will not be upgraded automatically without manually correcting the issues first.</span></span>

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

## <a name="step-2-perform-the-upgrade"></a><span data-ttu-id="b738c-120">Etapa 2: Realizar a atualização</span><span class="sxs-lookup"><span data-stu-id="b738c-120">Step 2: Perform the upgrade</span></span>

> [!CAUTION]
> <span data-ttu-id="b738c-121">Não há a opção de desfazer.</span><span class="sxs-lookup"><span data-stu-id="b738c-121">There is no undo operation.</span></span> <span data-ttu-id="b738c-122">Sempre verifique se você tem uma cópia de backup dos módulos e scripts do PowerShell que está tentando atualizar.</span><span class="sxs-lookup"><span data-stu-id="b738c-122">Always ensure that you have a backup copy of your PowerShell scripts and modules that you're attempting to upgrade.</span></span>

<span data-ttu-id="b738c-123">Quando você estiver satisfeito com o plano, a atualização será executada com o cmdlet **`Invoke-AzUpgradeModulePlan`** .</span><span class="sxs-lookup"><span data-stu-id="b738c-123">After you’re satisfied with the plan, the upgrade is performed with the **`Invoke-AzUpgradeModulePlan`** cmdlet.</span></span> <span data-ttu-id="b738c-124">Especifique **`SaveChangesToNewFiles`** para o valor do parâmetro **`FileEditMode`** para impedir que as alterações sejam feitas nos scripts originais.</span><span class="sxs-lookup"><span data-stu-id="b738c-124">Specify **`SaveChangesToNewFiles`** for the **`FileEditMode`** parameter value to prevent changes from being made to your original scripts.</span></span> <span data-ttu-id="b738c-125">Ao usar esse modo, a atualização será executada criando uma cópia de cada script direcionado com _`_az_upgraded`_ acrescentado aos nomes de arquivo.</span><span class="sxs-lookup"><span data-stu-id="b738c-125">When using this mode, the upgrade is performed by creating a copy of each script targeted with _`_az_upgraded`_ appended to the filenames.</span></span>

> [!WARNING]
> <span data-ttu-id="b738c-126">O cmdlet **`Invoke-AzUpgradeModulePlan`** é destrutivo quando a opção **`-FileEditMode ModifyExistingFiles`** é especificada.</span><span class="sxs-lookup"><span data-stu-id="b738c-126">The **`Invoke-AzUpgradeModulePlan`** cmdlet is destructive when the **`-FileEditMode ModifyExistingFiles`** option is specified!</span></span> <span data-ttu-id="b738c-127">Ele modifica seus scripts e funções em vigor, de acordo com o plano de atualização do módulo gerado pelo cmdlet **`New-AzUpgradeModulePlan`** .</span><span class="sxs-lookup"><span data-stu-id="b738c-127">It modifies your scripts and functions in place according to the module upgrade plan generated by the **`New-AzUpgradeModulePlan`** cmdlet.</span></span> <span data-ttu-id="b738c-128">Para a opção não destrutiva, especifique **`-FileEditMode SaveChangesToNewFiles`** .</span><span class="sxs-lookup"><span data-stu-id="b738c-128">For the non-destructive option specify **`-FileEditMode SaveChangesToNewFiles`** instead.</span></span>

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

<span data-ttu-id="b738c-129">Se algum erro for retornado, você poderá examinar mais atentamente os resultados do erro com o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="b738c-129">If any errors are returned, you can take a closer look at the error results with the following command:</span></span>

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

## <a name="limitations"></a><span data-ttu-id="b738c-130">Limitações</span><span class="sxs-lookup"><span data-stu-id="b738c-130">Limitations</span></span>

* <span data-ttu-id="b738c-131">As operações de E/S de arquivo usam a codificação padrão.</span><span class="sxs-lookup"><span data-stu-id="b738c-131">File I/O operations use default encoding.</span></span> <span data-ttu-id="b738c-132">Situações incomuns de codificação de arquivo podem causar problemas.</span><span class="sxs-lookup"><span data-stu-id="b738c-132">Unusual file encoding situations may cause problems.</span></span>
* <span data-ttu-id="b738c-133">Os cmdlets do AzureRM passados como argumentos para as instruções de simulação de teste de unidade do Pester não foram detectados.</span><span class="sxs-lookup"><span data-stu-id="b738c-133">AzureRM cmdlets passed as arguments to Pester unit test mock statements aren't detected.</span></span>
* <span data-ttu-id="b738c-134">Atualmente, somente o módulo Az do PowerShell versão 5.2.0 é compatível como destino.</span><span class="sxs-lookup"><span data-stu-id="b738c-134">Currently, only Az PowerShell module version 5.2.0 is supported as a target.</span></span>

## <a name="how-to-report-issues"></a><span data-ttu-id="b738c-135">Como relatar problemas</span><span class="sxs-lookup"><span data-stu-id="b738c-135">How to report issues</span></span>

<span data-ttu-id="b738c-136">Relate comentários e problemas sobre o módulo Az.Tools.Migration do PowerShell por meio de [um problema do GitHub](https://github.com/Azure/azure-powershell-migration/issues) no repositório `azure-powershell-migration`.</span><span class="sxs-lookup"><span data-stu-id="b738c-136">Report feedback and issues about the Az.Tools.Migration PowerShell module via [a GitHub issue](https://github.com/Azure/azure-powershell-migration/issues) in the `azure-powershell-migration` repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b738c-137">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="b738c-137">Next steps</span></span>

<span data-ttu-id="b738c-138">Para obter mais informações sobre o módulo Az do PowerShell, confira a [documentação do Azure PowerShell](/powershell/azure/)</span><span class="sxs-lookup"><span data-stu-id="b738c-138">To learn more about the Az PowerShell module, see the [Azure PowerShell documentation](/powershell/azure/)</span></span>
