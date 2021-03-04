---
Module Name: Az.ImportExport
Module Guid: 47cfc32b-a3bc-46e1-935e-11a63032bb86
Download Help Link: https://docs.microsoft.com/powershell/module/az.importexport
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
ms.openlocfilehash: cce265bc3d61f445c6843b0c1ca340ad921e1089
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888359"
---
# Módulo Az.ImportExport
## Descrição
Microsoft Azure PowerShell: cmdlets ImportExport

## Az.ImportExport Cmdlets
### [Get-AzImportExport](Get-AzImportExport.md)
Obtém informações sobre um trabalho existente.

### [Get-AzImportExportBitLockerKey](Get-AzImportExportBitLockerKey.md)
Retorna as Chaves do BitLocker para todas as unidades no trabalho especificado.

### [Get-AzImportExportLocation](Get-AzImportExportLocation.md)
Retorna os detalhes sobre um local para o qual você pode enviar os discos associados a um trabalho de importação ou exportação.
Um local é uma região do Azure.

### [New-AzImportExport](New-AzImportExport.md)
Cria um novo trabalho ou atualiza um trabalho existente na assinatura especificada.

### [New-AzImportExportDriveListObject](New-AzImportExportDriveListObject.md)
Crie um objeto DriverList para ImportExport.

### [Remove-AzImportExport](Remove-AzImportExport.md)
Exclui um trabalho existente.
Somente trabalhos nos estados Criando ou Concluído podem ser excluídos.

### [Update-AzImportExport](Update-AzImportExport.md)
Atualiza propriedades específicas de um trabalho.
Você pode chamar essa operação para notificar o serviço de Importação/Exportação de que os discos rígidos que compõem o trabalho de importação ou exportação foram enviados para o data center da Microsoft.
Ele também pode ser usado para cancelar um trabalho existente.

