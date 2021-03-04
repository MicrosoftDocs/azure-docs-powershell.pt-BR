---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 9acaa8a562ffe88631a587703a3300ac13f73224
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888033"
---
# Módulo Az.StorageSync
## Descrição
Os cmdlets no módulo de Sincronização de Armazenamento permitem gerenciar operações relacionadas à Sincronização de Arquivos do Azure no PowerShell.

## Az.StorageSync Cmdlets
### [Get-AzStorageSyncCloudEndpoint](Get-AzStorageSyncCloudEndpoint.md)
Este comando lista todos os pontos de extremidade da nuvem em um determinado grupo de sincronização.

### [Get-AzStorageSyncGroup](Get-AzStorageSyncGroup.md)
Este comando lista todos os grupos de sincronização em um determinado serviço de sincronização de armazenamento.

### [Get-AzStorageSyncServer](Get-AzStorageSyncServer.md)
Este comando lista todos os servidores registrados em um determinado serviço de sincronização de armazenamento.

### [Get-AzStorageSyncServerEndpoint](Get-AzStorageSyncServerEndpoint.md)
Este comando lista todos os pontos de extremidade do servidor em um determinado grupo de sincronização.

### [Get-AzStorageSyncService](Get-AzStorageSyncService.md)
Este comando lista todos os serviços de sincronização de armazenamento dentro de um determinado escopo de grupo de assinatura/recurso.

### [Invoke-AzStorageSyncChangeDetection](Invoke-AzStorageSyncChangeDetection.md)
Esse comando pode ser usado para iniciar manualmente a detecção de alterações de namespaces. Ele pode ser direcionado para todo o compartilhamento, subpasta ou conjunto de arquivos. No máximo 10.000 alterações podem ser detectadas. Se o escopo das alterações for conhecido para você, limite a execução deste comando a partes do namespace, para que a detecção de alterações possa ser finalização rápida e dentro de um limite de 10.000 alterações.

### [Invoke-AzStorageSyncCompatibilityCheck](Invoke-AzStorageSyncCompatibilityCheck.md)
Verifica se há possíveis problemas de compatibilidade entre seu sistema e a Sincronização de Arquivos do Azure.

### [Invoke-AzStorageSyncFileRecall](Invoke-AzStorageSyncFileRecall.md)
Este comando relembra todos os arquivos hierárquiquios de volta para o disco local.

### [New-AzStorageSyncCloudEndpoint](New-AzStorageSyncCloudEndpoint.md)
Este comando cria um ponto de extremidade de nuvem de sincronização de arquivos do Azure em um grupo de sincronização.

### [New-AzStorageSyncGroup](New-AzStorageSyncGroup.md)
Este comando cria um novo grupo de sincronização dentro de um serviço de sincronização de armazenamento especificado.

### [New-AzStorageSyncServerEndpoint](New-AzStorageSyncServerEndpoint.md)
Este comando cria um novo ponto de extremidade de servidor em um servidor registrado. Isso permite que o caminho especificado no servidor comece a sincronizar os arquivos com outros pontos de extremidade no grupo de sincronização.

### [New-AzStorageSyncService](New-AzStorageSyncService.md)
Este comando cria um novo serviço de sincronização de armazenamento em um grupo de recursos.

### [Set-AzStorageSyncService](New-AzStorageSyncService.md)
Este comando define um serviço de sincronização de armazenamento em um grupo de recursos.

### [Register-AzStorageSyncServer](Register-AzStorageSyncServer.md)
Esse comando registra um servidor em um serviço de sincronização de armazenamento que cria uma relação de confiança. O PowerShell ou o portal do Azure podem ser usados para configurar a sincronização neste servidor.

### [Remove-AzStorageSyncCloudEndpoint](Remove-AzStorageSyncCloudEndpoint.md)
Este comando excluirá o ponto de extremidade de nuvem especificado de um grupo de sincronização. Sem pelo menos um ponto de extremidade de nuvem, nenhum outro ponto de extremidade de servidor neste grupo de sincronização pode sincronizar.

### [Remove-AzStorageSyncGroup](Remove-AzStorageSyncGroup.md)
Este comando excluirá o grupo de sincronização especificado.

### [Remove-AzStorageSyncServerEndpoint](Remove-AzStorageSyncServerEndpoint.md)
Este comando excluirá o ponto de extremidade do servidor especificado. A sincronização com esse local será parada imediatamente.

### [Remove-AzStorageSyncService](Remove-AzStorageSyncService.md)
Este comando excluirá o serviço de sincronização de armazenamento especificado.

### [Reset-AzStorageSyncServerCertificate](Reset-AzStorageSyncServerCertificate.md)
Use apenas para solução de problemas. Esse comando rolará o certificado do servidor de sincronização de armazenamento usado para descrever a identidade do servidor para o serviço de sincronização de armazenamento.

### [Set-AzStorageSyncServerEndpoint](Set-AzStorageSyncServerEndpoint.md)
Este comando permite alterações nos parâmetros ajustáveis de um ponto de extremidade do servidor.

### [Unregister-AzStorageSyncServer](Unregister-AzStorageSyncServer.md)
Aviso: o não registro de um servidor resultará em exclusões em cascata de todos os pontos de extremidade do servidor neste servidor. Esse comando desacreva um servidor do serviço de sincronização de armazenamento.

