---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 01bf8c630f4fc4d137e98be5b1996eaf47ea3363
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93595413"
---
# Módulo AZ. Superfabric
## Descritivo
Módulo do Azure Service Fabric que você pode usar para automatizar as operações de fim-2, como a criação de um cluster seguro, a transferência de certificados de cluster, a adição ou remoção de nós do cluster, etc. A lista completa de todas as operações estão listadas abaixo.

## Cmdlets do AZ. infabric
### [Add-AzServiceFabricApplicationCertificate](Add-AzServiceFabricApplicationCertificate.md)
Adicione um novo certificado ao (s) conjunto (s) de escala da máquina virtual que compõe o cluster. O certificado deve ser usado como um certificado de aplicativo.

### [Add-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
Adicione um nome comum ou impressão digital ao cluster para fins de autenticação do cliente.

### [Add-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
Adicione um certificado de cluster secundário ao cluster.

### [Add-AzServiceFabricNode](Add-AzServiceFabricNode.md)
Adicione nós ao tipo de nó específico no cluster.

### [Add-AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
Adicione um novo tipo de nó ao cluster existente.

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
Obter os detalhes do recurso de cluster.

### [New-AzServiceFabricCluster](New-AzServiceFabricCluster.md)
Esse comando usa certificados que você fornece ou certificados autoassinados gerados pelo sistema para configurar um novo cluster de Service Fabric. Ele pode usar um modelo padrão ou um modelo personalizado fornecido por você. Você tem a opção de especificar uma pasta para exportar os certificados autoassinados ou para extraí-los mais tarde do cofre de chaves. 

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
Remova o (s) certificado (s) do (s) certificado (s) de cliente ou nome (s) dos (s) nome (s) da sua utilização para autenticação de cliente

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
Remover um certificado de cluster de ser usado para a segurança do cluster.

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
Remover nós do tipo de nó específico de um cluster.

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
Remover um tipo de nó completo de um cluster.

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
Remova uma ou várias configurações da malha de serviço do cluster.

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
Adicione ou atualize uma ou várias configurações do Service Fabric para o cluster.

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
Altere o tipo de atualização do Service Fabric do cluster.

### [Update-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
Atualize a camada de durabilidade ou o VmSku de um tipo de nó no cluster.

### [Update-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
Atualize a camada de confiabilidade do tipo de nó primário em um cluster.

