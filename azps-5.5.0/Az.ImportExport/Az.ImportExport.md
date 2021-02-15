---
Module Name: Az.ImportExport
Module Guid: 47cfc32b-a3bc-46e1-935e-11a63032bb86
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.importexport
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
ms.openlocfilehash: 2da6d45b7bc8107e70a672962a6bc57ccb9f17a0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115296"
---
# Módulo Az.ImportExport
## Descrição
Microsoft Azure PowerShell: cmdlets ImportExport

## Az.ImportExport Cmdlets
### [Get-AzImportExport](Get-AzImportExport.md)
Obtém informações sobre um trabalho existente.

### [Get-AzImportExportBitLockerKey](Get-AzImportExportBitLockerKey.md)
Retorna as Teclas BitLocker para todas as unidades no trabalho especificado.

### [Get-AzImportExportLocation](Get-AzImportExportLocation.md)
Retorna os detalhes sobre um local para o qual você pode enviar os discos associados a um trabalho de importação ou exportação.
Um local é uma região do Azure.

### [New-AzImportExport](New-AzImportExport.md)
Cria um novo trabalho ou atualiza um trabalho existente na assinatura especificada.

### [New-AzImportExportDriveListObject](New-AzImportExportDriveListObject.md)
Criar um Objeto de Lista de Driver para ImportExport.

### [Remove-AzImportExport](Remove-AzImportExport.md)
Exclui um trabalho existente.
Somente trabalhos nos estados Criar ou Concluído podem ser excluídos.

### [Update-AzImportExport](Update-AzImportExport.md)
Atualiza as propriedades específicas de um trabalho.
Você pode ligar para esta operação para notificar o serviço Importar/Exportar de que os discos rígidos compõem o trabalho de importação ou exportação que foram enviados para o data center da Microsoft.
Ele também pode ser usado para cancelar um trabalho existente.

