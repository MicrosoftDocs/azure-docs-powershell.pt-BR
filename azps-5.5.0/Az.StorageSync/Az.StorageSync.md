---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: bc3704c3594826f19399c1967bbe86ed7f1e8773
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112499"
---
# Módulo Az.StorageSync
## Descrição
Os cmdlets no módulo sincronização de armazenamento permitem gerenciar as operações referentes à Sincronização de Arquivos do Azure no PowerShell.

## Az.StorageSync Cmdlets
### [Get-AzStorageSyncCloudEndpoint](Get-AzStorageSyncCloudEndpoint.md)
Esse comando lista todos os pontos de extremidade de nuvem dentro de um determinado grupo de sincronização.

### [Get-AzStorageSyncGroup](Get-AzStorageSyncGroup.md)
Esse comando lista todos os grupos de sincronização dentro de um determinado serviço de sincronização de armazenamento.

### [Get-AzStorageSyncServer](Get-AzStorageSyncServer.md)
Esse comando lista todos os servidores registrados em um determinado serviço de sincronização de armazenamento.

### [Get-AzStorageSyncServerEndpoint](Get-AzStorageSyncServerEndpoint.md)
Esse comando lista todos os pontos de extremidade do servidor dentro de um determinado grupo de sincronização.

### [Get-AzStorageSyncService](Get-AzStorageSyncService.md)
Esse comando lista todos os serviços de sincronização de armazenamento dentro de um determinado escopo de assinatura/grupo de recursos.

### [Invoke-AzStorageSyncChangeDetection](Invoke-AzStorageSyncChangeDetection.md)
Esse comando pode ser usado para iniciar manualmente a detecção de alterações de namespaces. Ele pode ser direcionado para todo o compartilhamento, subpasta ou conjunto de arquivos. É possível detectar no máximo 10.000 alterações. Se o escopo das alterações for conhecido para você, limite a execução desse comando a partes do namespace, para que a detecção de alterações possa terminar rapidamente e dentro de um limite de 10.000 alterações.

### [Invoke-AzStorageSyncCompatibilityCheck](Invoke-AzStorageSyncCompatibilityCheck.md)
Verifica se há possíveis problemas de compatibilidade entre seu sistema e a Sincronização de Arquivos do Azure.

### [Invoke-AzStorageSyncFileRecall](Invoke-AzStorageSyncFileRecall.md)
Esse comando faz com que todos os arquivos em camadas voltem para o disco local.

### [New-AzStorageSyncCloudEndpoint](New-AzStorageSyncCloudEndpoint.md)
Esse comando cria um ponto de extremidade de nuvem de Sincronização de Arquivos do Azure em um grupo de sincronização.

### [New-AzStorageSyncGroup](New-AzStorageSyncGroup.md)
Esse comando cria um novo grupo de sincronização dentro de um serviço de sincronização de armazenamento especificado.

### [New-AzStorageSyncServerEndpoint](New-AzStorageSyncServerEndpoint.md)
Esse comando cria um novo ponto de extremidade de servidor em um servidor registrado. Isso permite que o caminho especificado no servidor comece a sincronizar os arquivos com outros pontos de extremidade no grupo de sincronização.

### [New-AzStorageSyncService](New-AzStorageSyncService.md)
Esse comando cria um novo serviço de sincronização de armazenamento em um grupo de recursos.

### [Set-AzStorageSyncService](New-AzStorageSyncService.md)
Esse comando define um serviço de sincronização de armazenamento em um grupo de recursos.

### [Register-AzStorageSyncServer](Register-AzStorageSyncServer.md)
Esse comando registra um servidor em um serviço de sincronização de armazenamento que cria uma relação de confiança. O PowerShell ou o portal do Azure podem ser usados para configurar a sincronização neste servidor.

### [Remove-AzStorageSyncCloudEndpoint](Remove-AzStorageSyncCloudEndpoint.md)
Esse comando excluirá o ponto de extremidade de nuvem especificado de um grupo de sincronização. Sem pelo menos um ponto de extremidade de nuvem, nenhum outro ponto de extremidade de servidor neste grupo de sincronização pode sincronizar.

### [Remove-AzStorageSyncGroup](Remove-AzStorageSyncGroup.md)
Esse comando excluirá o grupo de sincronização especificado.

### [Remove-AzStorageSyncServerEndpoint](Remove-AzStorageSyncServerEndpoint.md)
Esse comando excluirá o ponto de extremidade do servidor especificado. A sincronização com esse local será parada imediatamente.

### [Remove-AzStorageSyncService](Remove-AzStorageSyncService.md)
Esse comando excluirá o serviço de sincronização de armazenamento especificado.

### [Reset-AzStorageSyncServerCertificate](Reset-AzStorageSyncServerCertificate.md)
Use apenas para solução de problemas. Esse comando rolará o certificado do servidor de sincronização de armazenamento usado para descrever a identidade do servidor para o serviço de sincronização de armazenamento.

### [Set-AzStorageSyncServerEndpoint](Set-AzStorageSyncServerEndpoint.md)
Esse comando permite alterações nos parâmetros ajustáveis de um ponto de extremidade do servidor.

### [Unregister-AzStorageSyncServer](Unregister-AzStorageSyncServer.md)
Aviso: a não registro de um servidor resultará em exclusões em cascata de todos os pontos de extremidade do servidor neste servidor. Esse comando não fará o registro de um servidor do serviço de sincronização de armazenamento.

