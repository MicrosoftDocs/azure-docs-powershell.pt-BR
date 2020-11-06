---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 3bfdc9c488f02794e82388741e7103417878c9f6
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/15/2019
ms.locfileid: "93595558"
---
# Módulo AZ. StorageSync
## Descritivo
Os cmdlets no módulo de sincronização de armazenamento permitem que você gerencie as operações pertinentes à sincronização do Azure File no PowerShell.

## Cmdlets AZ. StorageSync
### [Get-AzStorageSyncCloudEndpoint](Get-AzStorageSyncCloudEndpoint.md)
Esse comando lista todos os pontos de extremidade da nuvem em um determinado grupo de sincronização.

### [Get-AzStorageSyncGroup](Get-AzStorageSyncGroup.md)
Esse comando lista todos os grupos de sincronização em um determinado serviço de sincronização de armazenamento.

### [Get-AzStorageSyncServer](Get-AzStorageSyncServer.md)
Esse comando lista todos os servidores registrados para um determinado serviço de sincronização de armazenamento.

### [Get-AzStorageSyncServerEndpoint](Get-AzStorageSyncServerEndpoint.md)
Esse comando lista todos os pontos de extremidade do servidor dentro de um determinado grupo de sincronização.

### [Get-AzStorageSyncService](Get-AzStorageSyncService.md)
Esse comando lista todos os serviços de sincronização de armazenamento em um determinado escopo de grupo de assinaturas/recursos.

### [Invoke-AzStorageSyncChangeDetection](Invoke-AzStorageSyncChangeDetection.md)
Esse comando pode ser usado para iniciar manualmente a detecção de alterações de namespaces. Ele pode ser direcionado para todo o compartilhamento, subpasta ou conjunto de arquivos. No máximo 10.000 alterações podem ser detectadas. Se o escopo das alterações for conhecido, limite a execução desse comando para partes do namespace, para que a detecção de alteração possa terminar rapidamente e dentro de um limite de alterações do 10.000.

### [Invoke-AzStorageSyncCompatibilityCheck](Invoke-AzStorageSyncCompatibilityCheck.md)
Verifica possíveis problemas de compatibilidade entre o sistema e a sincronização de arquivos do Azure.

### [Invoke-AzStorageSyncFileRecall](Invoke-AzStorageSyncFileRecall.md)
Esse comando recupera novamente todos os arquivos em camadas para o disco local.

### [New-AzStorageSyncCloudEndpoint](New-AzStorageSyncCloudEndpoint.md)
Esse comando cria um ponto de extremidade da nuvem do Azure File Sync em um grupo de sincronização.

### [New-AzStorageSyncGroup](New-AzStorageSyncGroup.md)
Esse comando cria um novo grupo de sincronização dentro de um serviço de sincronização de armazenamento especificado.

### [New-AzStorageSyncServerEndpoint](New-AzStorageSyncServerEndpoint.md)
Esse comando cria um novo ponto de extremidade de servidor em um servidor registrado. Isso permite que o caminho especificado no servidor comece a sincronizar os arquivos com outros pontos de extremidade no grupo de sincronização.

### [New-AzStorageSyncService](New-AzStorageSyncService.md)
Esse comando cria um novo serviço de sincronização de armazenamento em um grupo de recursos.

### [Register-AzStorageSyncServer](Register-AzStorageSyncServer.md)
Esse comando registra um servidor em um serviço de sincronização de armazenamento que cria uma relação de confiança. O PowerShell ou o portal do Azure pode ser usado para configurar a sincronização neste servidor.

### [Remove-AzStorageSyncCloudEndpoint](Remove-AzStorageSyncCloudEndpoint.md)
Esse comando excluirá o ponto de extremidade de nuvem especificado de um grupo de sincronização. Sem pelo menos um ponto de extremidade de nuvem, nenhum outro ponto de extremidade do servidor neste grupo de sincronização pode sincronizar.

### [Remove-AzStorageSyncGroup](Remove-AzStorageSyncGroup.md)
Esse comando excluirá o grupo de sincronização especificado.

### [Remove-AzStorageSyncServerEndpoint](Remove-AzStorageSyncServerEndpoint.md)
Esse comando excluirá o ponto de extremidade do servidor especificado. A sincronização com este local será interrompida imediatamente.

### [Remove-AzStorageSyncService](Remove-AzStorageSyncService.md)
Esse comando excluirá o serviço de sincronização de armazenamento especificado.

### [Reset-AzStorageSyncServerCertificate](Reset-AzStorageSyncServerCertificate.md)
Use somente para solução de problemas. Esse comando irá reverter o certificado do servidor de sincronização de armazenamento usado para descrever a identidade do servidor para o serviço de sincronização de armazenamento.

### [Set-AzStorageSyncServerEndpoint](Set-AzStorageSyncServerEndpoint.md)
Esse comando permite alterações nos parâmetros ajustáveis de um ponto de extremidade do servidor.

### [Cancelar registro-AzStorageSyncServer](Unregister-AzStorageSyncServer.md)
Aviso: o cancelamento do registro de um servidor resultará em exclusões em cascata de todos os pontos de extremidade do servidor neste servidor. Esse comando cancelará o registro de um servidor do serviço de sincronização de armazenamento.

