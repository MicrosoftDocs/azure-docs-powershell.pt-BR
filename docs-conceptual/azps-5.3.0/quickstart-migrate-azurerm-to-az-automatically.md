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
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a>Início Rápido: Migrar automaticamente os scripts do PowerShell do AzureRM para o módulo Az do PowerShell

Neste artigo, você aprenderá a usar o módulo Az.Tools.Migration do PowerShell para atualizar automaticamente os scripts do PowerShell e os módulos de script do AzureRM para o módulo Az do PowerShell. Para obter outras opções de migração, confira [Migrar o Azure PowerShell do AzureRM para o Az](/powershell/azure/migrate-from-azurerm-to-az).

## <a name="requirements"></a>Requisitos

* Atualize os scripts do PowerShell existentes para a versão mais recente do [módulo AzureRM do PowerShell (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).
* Instale o módulo Az.Tools.Migration do PowerShell.

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a>Etapa 1: gerar um plano de atualização

Você usa o cmdlet **`New-AzUpgradeModulePlan`** para gerar um plano de atualização a fim de migrar os scripts e módulos para o módulo Az do PowerShell. Esse cmdlet não faz nenhuma alteração em seus scripts existentes. Use o parâmetro **`FilePath`** para direcionar um script específico ou o parâmetro **`DirectoryPath`** para direcionar todos os scripts em uma pasta específica.

> [!NOTE]
> O cmdlet **`New-AzUpgradeModulePlan`** não executa o plano, ele apenas gera as etapas de atualização.

O exemplo a seguir gera um plano para todos os scripts na pasta _`C:\Scripts`_ . O parâmetro **`OutVariable`** é especificado para que os resultados sejam retornados e armazenados simultaneamente em uma variável chamada **`Plan`** .

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 5.2.0 -DirectoryPath 'C:\Scripts' -OutVariable Plan
```

Conforme mostrado na saída a seguir, o plano de atualização detalha o arquivo específico e os pontos de deslocamento que necessitam de alterações ao migrar os cmdlets do AzureRM para o módulo Az do PowerShell.

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

Antes de executar a atualização, você precisa exibir os resultados do plano para ver se há problemas. O exemplo a seguir retorna uma lista de scripts e os itens desses scripts que os impedirão de serem atualizados automaticamente.

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

Os itens mostrados na saída a seguir não serão atualizados automaticamente sem primeiro corrigir manualmente os problemas.

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

## <a name="step-2-perform-the-upgrade"></a>Etapa 2: Realizar a atualização

> [!CAUTION]
> Não há a opção de desfazer. Sempre verifique se você tem uma cópia de backup dos módulos e scripts do PowerShell que está tentando atualizar.

Quando você estiver satisfeito com o plano, a atualização será executada com o cmdlet **`Invoke-AzUpgradeModulePlan`** . Especifique **`SaveChangesToNewFiles`** para o valor do parâmetro **`FileEditMode`** para impedir que as alterações sejam feitas nos scripts originais. Ao usar esse modo, a atualização será executada criando uma cópia de cada script direcionado com _`_az_upgraded`_ acrescentado aos nomes de arquivo.

> [!WARNING]
> O cmdlet **`Invoke-AzUpgradeModulePlan`** é destrutivo quando a opção **`-FileEditMode ModifyExistingFiles`** é especificada. Ele modifica seus scripts e funções em vigor, de acordo com o plano de atualização do módulo gerado pelo cmdlet **`New-AzUpgradeModulePlan`** . Para a opção não destrutiva, especifique **`-FileEditMode SaveChangesToNewFiles`** .

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

Se algum erro for retornado, você poderá examinar mais atentamente os resultados do erro com o seguinte comando:

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

## <a name="limitations"></a>Limitações

* As operações de E/S de arquivo usam a codificação padrão. Situações incomuns de codificação de arquivo podem causar problemas.
* Os cmdlets do AzureRM passados como argumentos para as instruções de simulação de teste de unidade do Pester não foram detectados.
* Atualmente, somente o módulo Az do PowerShell versão 5.2.0 é compatível como destino.

## <a name="how-to-report-issues"></a>Como relatar problemas

Relate comentários e problemas sobre o módulo Az.Tools.Migration do PowerShell por meio de [um problema do GitHub](https://github.com/Azure/azure-powershell-migration/issues) no repositório `azure-powershell-migration`.

## <a name="next-steps"></a>Próximas etapas

Para obter mais informações sobre o módulo Az do PowerShell, confira a [documentação do Azure PowerShell](/powershell/azure/)
