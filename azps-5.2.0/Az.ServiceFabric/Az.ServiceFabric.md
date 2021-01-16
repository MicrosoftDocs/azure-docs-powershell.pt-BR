---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 6c58f25209a0acd227e2f04e7ca808916f283d46
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260686"
---
# Módulo AZ. Superfabric
## Descritivo
Módulo do Azure Service Fabric que você pode usar para automatizar as operações de fim-2, como a criação de um cluster seguro, a transferência de certificados de cluster, a adição ou remoção de nós do cluster, etc. A lista completa de todas as operações estão listadas abaixo.

## Cmdlets do AZ. infabric
### [Add-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
Adicione um nome comum ou impressão digital ao cluster para fins de autenticação do cliente.

### [Add-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
Adicione um certificado de cluster secundário ao cluster.

### [Add-AzServiceFabricManagedClusterClientCertificate](Add-AzServiceFabricManagedClusterClientCertificate.md)
Adicione o nome comum ou a impressão digital do certificado ao cluster. Isso registrará o certificado novamente no cluster para fins de autenticação de cliente.

### [Add-AzServiceFabricManagedNodeTypeVMExtension](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
Adicionar extensão de VM ao tipo de nó.

### [Add-AzServiceFabricManagedNodeTypeVMSecret](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
Adicione o segredo do certificado ao tipo de nó.

### [Add-AzServiceFabricNode](Add-AzServiceFabricNode.md)
Adicione nós ao tipo de nó específico no cluster.

### [Add-AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
Adicione um novo tipo de nó ao cluster existente.

### [Get-AzServiceFabricApplication](Get-AzServiceFabricApplication.md)
Obter detalhes do aplicativo do Service Fabric.

### [Get-AzServiceFabricApplicationType](Get-AzServiceFabricApplicationType.md)
Obter detalhes do tipo de aplicativo Service Fabric.

### [Get-AzServiceFabricApplicationTypeVersion](Get-AzServiceFabricApplicationTypeVersion.md)
Obter detalhes da versão do tipo de aplicativo Service Fabric.

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
Obter os detalhes do recurso de cluster.

### [Get-AzServiceFabricManagedCluster](Get-AzServiceFabricManagedCluster.md)
Obter os detalhes do recurso de cluster gerenciado.

### [Get-AzServiceFabricManagedNodeType](Get-AzServiceFabricManagedNodeType.md)
Obter os detalhes do recurso de tipo de nó gerenciado.

### [Get-AzServiceFabricService](Get-AzServiceFabricService.md)
Obter detalhes do serviço do Service Fabric no aplicativo e no cluster especificados.

### [New-AzServiceFabricApplication](New-AzServiceFabricApplication.md)
Criar novo aplicativo Service Fabric no grupo de recursos e no cluster especificado.

### [New-AzServiceFabricApplicationType](New-AzServiceFabricApplicationType.md)
Criar novo tipo de aplicativo Service Fabric no grupo de recursos e no cluster especificado.

### [New-AzServiceFabricApplicationTypeVersion](New-AzServiceFabricApplicationTypeVersion.md)
Crie uma nova versão do tipo de aplicativo no grupo de recursos e no cluster especificado.

### [New-AzServiceFabricCluster](New-AzServiceFabricCluster.md)
Esse comando usa certificados que você fornece ou certificados autoassinados gerados pelo sistema para configurar um novo cluster de Service Fabric. Ele pode usar um modelo padrão ou um modelo personalizado fornecido por você. Você tem a opção de especificar uma pasta para exportar os certificados autoassinados ou para extraí-los mais tarde do cofre de chaves.

### [New-AzServiceFabricManagedCluster](New-AzServiceFabricManagedCluster.md)
Criar novo cluster gerenciado.

### [New-AzServiceFabricManagedNodeType](New-AzServiceFabricManagedNodeType.md)
Criar novo recurso de tipo de nó.

### [New-AzServiceFabricService](New-AzServiceFabricService.md)
Criar novo serviço Service Fabric no aplicativo e no cluster especificados.

### [Remove-AzServiceFabricApplication](Remove-AzServiceFabricApplication.md)
Remover um aplicativo do cluster. Isso removerá todos os serviços do aplicativo.

### [Remove-AzServiceFabricApplicationType](Remove-AzServiceFabricApplicationType.md)
Remover a malha de serviços um tipo de aplicativo do cluster. Isso removerá todas as versões de tipo desse recurso.

### [Remove-AzServiceFabricApplicationTypeVersion](Remove-AzServiceFabricApplicationTypeVersion.md)
Remover a malha de serviços uma versão do tipo de aplicativo do cluster.

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
Remova o (s) certificado (s) do (s) certificado (s) de cliente ou nome (s) dos (s) nome (s) da sua utilização para autenticação de cliente

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
Remover um certificado de cluster de ser usado para a segurança do cluster.

### [Remove-AzServiceFabricManagedCluster](Remove-AzServiceFabricManagedCluster.md)
Remover recurso de cluster.

### [Remove-AzServiceFabricManagedClusterClientCertificate](Remove-AzServiceFabricManagedClusterClientCertificate.md)
Remvoe o certificado do cliente por impressão digital ou nome comum.

### [Remove-AzServiceFabricManagedNodeType](Remove-AzServiceFabricManagedNodeType.md)
Remova o tipo de nó ou nós específicos dentro do tipo de nó.

### [Remove-AzServiceFabricManagedNodeTypeVMExtension](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
Remova a extensão de VM do tipo de nó.

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
Remover nós do tipo de nó específico de um cluster.

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
Remover um tipo de nó completo de um cluster.

### [Remove-AzServiceFabricService](Remove-AzServiceFabricService.md)
Remover um serviço do cluster.

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
Remova uma ou várias configurações da malha de serviço do cluster.

### [Restart-AzServiceFabricManagedNodeType](Restart-AzServiceFabricManagedNodeType.md)
Reinicie os nós específicos do tipo de nó.

### [Set-AzServiceFabricManagedCluster](Set-AzServiceFabricManagedCluster.md)
Definir propriedades de recurso de cluster.

### [Set-AzServiceFabricManagedNodeType](Set-AzServiceFabricManagedNodeType.md)
Define as propriedades de recurso do tipo de nó ou executar ações de reimagem em NDES específicas do tipo de nó com o parâmetro-reimage.

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
Adicione ou atualize uma ou várias configurações do Service Fabric para o cluster.

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
Altere o tipo de atualização do Service Fabric do cluster.

### [Update-AzServiceFabricApplication](Update-AzServiceFabricApplication.md)
Atualize um aplicativo do Service Fabric. Isso permite atualizar os parâmetros do aplicativo e/ou atualizar a versão do tipo de aplicativo, que acionará uma atualização do aplicativo.

### [Update-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
Atualize a camada de durabilidade ou o VmSku de um tipo de nó no cluster.

### [Update-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
Atualize a camada de confiabilidade do tipo de nó primário em um cluster.

