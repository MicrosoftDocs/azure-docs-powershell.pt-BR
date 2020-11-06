---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 0bd157b8df4cca37c92a4d4f2984011dbd924e34
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93425286"
---
# Módulo AzureRM. emfabric
## Descritivo
Módulo do Azure Service Fabric que você pode usar para automatizar as operações de fim-2, como a criação de um cluster seguro, a transferência de certificados de cluster, a adição ou remoção de nós do cluster, etc. A lista completa de todas as operações estão listadas abaixo.

## Cmdlets do AzureRM. infabric
### [Add-AzureRmServiceFabricApplicationCertificate](Add-AzureRmServiceFabricApplicationCertificate.md)
Adicione um novo certificado ao (s) conjunto (s) de escala da máquina virtual que compõe o cluster. O certificado deve ser usado como um certificado de aplicativo.

### [Add-AzureRmServiceFabricClientCertificate](Add-AzureRmServiceFabricClientCertificate.md)
Adicione um nome comum ou impressão digital ao cluster para fins de autenticação do cliente.

### [Add-AzureRmServiceFabricClusterCertificate](Add-AzureRmServiceFabricClusterCertificate.md)
Adicione um certificado de cluster secundário ao cluster.

### [Add-AzureRmServiceFabricNode](Add-AzureRmServiceFabricNode.md)
Adicione nós ao tipo de nó específico no cluster.

### [Add-AzureRmServiceFabricNodeType](Add-AzureRmServiceFabricNodeType.md)
Adicione um novo tipo de nó ao cluster existente.

### [Get-AzureRmServiceFabricCluster](Get-AzureRmServiceFabricCluster.md)
Obter os detalhes do recurso de cluster.

### [New-AzureRmServiceFabricCluster](New-AzureRmServiceFabricCluster.md)
Esse comando usa certificados que você fornece ou certificados autoassinados gerados pelo sistema para configurar um novo cluster de Service Fabric. Ele pode usar um modelo padrão ou um modelo personalizado fornecido por você. Você tem a opção de especificar uma pasta para exportar os certificados autoassinados ou para extraí-los mais tarde do cofre de chaves. 

### [Remove-AzureRmServiceFabricClientCertificate](Remove-AzureRmServiceFabricClientCertificate.md)
Remova o (s) certificado (s) do (s) certificado (s) de cliente ou nome (s) dos (s) nome (s) da sua utilização para autenticação de cliente

### [Remove-AzureRmServiceFabricClusterCertificate](Remove-AzureRmServiceFabricClusterCertificate.md)
Remover um certificado de cluster de ser usado para a segurança do cluster.

### [Remove-AzureRmServiceFabricNode](Remove-AzureRmServiceFabricNode.md)
Remover nós do tipo de nó específico de um cluster.

### [Remove-AzureRmServiceFabricNodeType](Remove-AzureRmServiceFabricNodeType.md)
Remover um tipo de nó completo de um cluster.

### [Remove-AzureRmServiceFabricSetting](Remove-AzureRmServiceFabricSetting.md)
Remova uma ou várias configurações da malha de serviço do cluster.

### [Set-AzureRmServiceFabricSetting](Set-AzureRmServiceFabricSetting.md)
Adicione ou atualize uma ou várias configurações do Service Fabric para o cluster.

### [Set-AzureRmServiceFabricUpgradeType](Set-AzureRmServiceFabricUpgradeType.md)
Altere o tipo de atualização do Service Fabric do cluster.

### [Update-AzureRmServiceFabricDurability](Update-AzureRmServiceFabricDurability.md)
Atualize a camada de durabilidade ou o VmSku de um tipo de nó no cluster.

### [Update-AzureRmServiceFabricReliability](Update-AzureRmServiceFabricReliability.md)
Atualize a camada de confiabilidade do tipo de nó primário em um cluster.

