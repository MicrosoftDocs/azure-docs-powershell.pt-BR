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
ms.sourcegitcommit: d0045e283ef062c74a223258fd4d5d6432bac531
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "92021127"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a>Início Rápido: Migrar automaticamente os scripts do PowerShell do AzureRM para o módulo Az do PowerShell

Neste artigo, você aprenderá a usar o módulo Az.Tools.Migration do PowerShell para atualizar automaticamente os scripts do PowerShell e os módulos de script do AzureRM para o módulo Az do PowerShell.

> [!IMPORTANT]
> O módulo Az.Tools.Migration do PowerShell está atualmente em versão prévia pública. A versão prévia é fornecida sem um contrato de nível de serviço. Ela não é recomendada para cargas de trabalho de produção. Alguns recursos podem não ter suporte ou podem ter restrição de recursos. Para obter mais informações, consulte [Termos de Uso Complementares de Versões Prévias do Microsoft Azure](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).

Relate comentários e problemas sobre o módulo Az.Tools.Migration do PowerShell por meio de [um problema do GitHub](https://github.com/Azure/azure-powershell-migration/issues) no repositório `azure-powershell-migration`.

## <a name="requirements"></a>Requisitos

* Atualize os scripts do PowerShell existentes para a versão mais recente do [módulo AzureRM do PowerShell (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).
* Instale o módulo Az.Tools.Migration do PowerShell.

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a>Etapa 1: gerar um plano de atualização

Use o cmdlet `New-AzUpgradeModulePlan` para gerar um plano de atualização a fim de migrar os scripts e módulos para o módulo Az do PowerShell. O plano de atualização detalha o arquivo específico e os pontos de deslocamento que necessitam de alterações ao migrar os cmdlets do AzureRM para o módulo Az do PowerShell.

> [!NOTE]
> O cmdlet `New-AzUpgradeModulePlan` não executa o plano, ele apenas gera as etapas de atualização.

```powershell
#  Generate an upgrade plan for the specified PowerShell script and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -FilePath 'C:\Scripts\my-azure-script.ps1'
```

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts'
```

Revise os resultados do plano de atualização.

```powershell
# Show the entire upgrade plan
$Plan
```

Execute o comando a seguir para filtrar os resultados de comandos que tenham avisos ou erros. Isso pode ser útil em grandes conjuntos de resultados para identificar rapidamente os erros antes de executar a atualização.

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

## <a name="step-2-perform-the-upgrade"></a>Etapa 2: Realizar a atualização

O plano de atualização é executado quando você executa o cmdlet `Invoke-AzUpgradeModulePlan`. Esse comando executa uma atualização do arquivo ou das pastas especificadas, exceto os erros identificados pelo cmdlet `New-AzUpgradeModulePlan`.

Esse comando exige que você especifique se os arquivos devem ser modificados no local ou se novos arquivos devem ser salvos junto com os arquivos originais (deixando os originais inalterados).

> [!CAUTION]
> Não há a opção de desfazer. Sempre verifique se você tem uma cópia de backup dos módulos e scripts do PowerShell que está tentando atualizar.

> [!WARNING]
> O cmdlet `Invoke-AzUpgradeModulePlan` é destrutivo quando a opção `-FileEditMode ModifyExistingFiles` é especificada. Ele modifica os scripts e as funções em vigor, de acordo com o plano de atualização do módulo gerado pelo cmdlet `New-AzUpgradeModulePlan`. Para a opção não destrutiva, especifique `-FileEditMode SaveChangesToNewFiles`.

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
$Results = Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles
```

Revise os resultados da operação de atualização.

```powershell
# Show the results for the entire upgrade operation
$Results
```

Se algum erro for retornado, você poderá examinar mais atentamente os resultados do erro com o seguinte comando:

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

## <a name="limitations"></a>Limitações

* Não há suporte para atualizações de nome de parâmetro automatizadas para conjuntos de parâmetros com splatting. Se algum for encontrado durante a geração do plano de atualização, um aviso será retornado.
* As operações de E/S de arquivo usam a codificação padrão. Situações incomuns de codificação de arquivo podem causar problemas.
* Os cmdlets do AzureRM passados como argumentos para as instruções de simulação de teste de unidade do Pester não foram detectados.
* Atualmente, somente o módulo Az do PowerShell versão 4.6.1 tem suporte como destino.

## <a name="next-steps"></a>Próximas etapas

Para obter mais informações sobre o módulo Az do PowerShell, confira a [documentação do Azure PowerShell](https://docs.microsoft.com/powershell/azure/)