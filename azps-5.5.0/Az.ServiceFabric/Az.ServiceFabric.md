---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 6c58f25209a0acd227e2f04e7ca808916f283d46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118652"
---
# Módulo Az.ServiceFabric
## Descrição
Módulo de Malha de Serviço do Azure que você pode usar para automatizar as operações de ponta a ponta, como criar um cluster seguro, rolar por certificados de cluster, adicionar ou remover nós do cluster, etc. A lista completa de todas as operações está listada abaixo.

## Az.ServiceFabric Cmdlets
### [Add-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
Adicione um nome comum ou uma impressão digital ao cluster para fins de autenticação do cliente.

### [Add-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
Adicione um certificado de cluster secundário ao cluster.

### [Add-AzServiceFabricManagedClusterClientCertificate](Add-AzServiceFabricManagedClusterClientCertificate.md)
Adicione o nome comum do certificado ou a impressão digital ao cluster. Isso registrará o certificado novamente no cluster para fins de autenticação do cliente.

### [Add-AzServiceFabricManagedNodeTypeVMExtension](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
Adicione a extensão vm ao tipo de nó.

### [Add-AzServiceFabricManagedNodeTypeVMSecduto](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
Adicione um segredo de certificado ao tipo de nó.

### [Add-AzServiceFabricNode](Add-AzServiceFabricNode.md)
Adicione nós ao tipo de nó específico no cluster.

### [Add-AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
Adicione um novo tipo de nó ao cluster existente.

### [Get-AzServiceFabricApplication](Get-AzServiceFabricApplication.md)
Obter detalhes do aplicativo Service Fabric.

### [Get-AzServiceFabricApplicationType](Get-AzServiceFabricApplicationType.md)
Obter detalhes do tipo de aplicativo Service Fabric.

### [Get-AzServiceFabricApplicationTypeVersion](Get-AzServiceFabricApplicationTypeVersion.md)
Obter detalhes da versão do tipo de aplicativo Service Fabric.

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
Obter os detalhes do recurso de cluster.

### [Get-AzServiceFabricManagedCluster](Get-AzServiceFabricManagedCluster.md)
Obter os detalhes do recurso de cluster gerenciado.

### [Get-AzServiceFabricManagedNodeType](Get-AzServiceFabricManagedNodeType.md)
Obter detalhes do recurso de tipo de nó gerenciado.

### [Get-AzServiceFabricService](Get-AzServiceFabricService.md)
Obter detalhes do serviço de Malha de Serviço sob o aplicativo e o cluster especificados.

### [New-AzServiceFabricApplication](New-AzServiceFabricApplication.md)
Crie um novo aplicativo de malha de serviço sob o grupo de recursos e cluster especificados.

### [New-AzServiceFabricApplicationType](New-AzServiceFabricApplicationType.md)
Crie um novo tipo de aplicativo de malha de serviço sob o grupo e o cluster de recursos especificados.

### [New-AzServiceFabricApplicationTypeVersion](New-AzServiceFabricApplicationTypeVersion.md)
Crie uma nova versão de tipo de aplicativo sob o grupo de recursos e cluster especificados.

### [New-AzServiceFabricCluster](New-AzServiceFabricCluster.md)
Esse comando usa certificados que você fornece ou que o sistema gera certificados auto-assinados para configurar um novo cluster de malha de serviço. Ele pode usar um modelo padrão ou um modelo personalizado que você fornecer. Você tem a opção de especificar uma pasta para exportar os certificados auto-assinados ou busca-los mais tarde no cofre de chaves.

### [New-AzServiceFabricManagedCluster](New-AzServiceFabricManagedCluster.md)
Criar novo cluster gerenciado.

### [New-AzServiceFabricManagedNodeType](New-AzServiceFabricManagedNodeType.md)
Criar novo recurso de tipo de nó.

### [New-AzServiceFabricService](New-AzServiceFabricService.md)
Crie um novo serviço de malha de serviço sob o aplicativo e cluster especificados.

### [Remove-AzServiceFabricApplication](Remove-AzServiceFabricApplication.md)
Remover um aplicativo do cluster. Isso removerá todos os serviços sob o aplicativo.

### [Remove-AzServiceFabricApplicationType](Remove-AzServiceFabricApplicationType.md)
Remover malha de serviço de um tipo de aplicativo do cluster. Isso removerá todas as versões do tipo sob esse recurso.

### [Remove-AzServiceFabricApplicationTypeVersion](Remove-AzServiceFabricApplicationTypeVersion.md)
Remova a malha de serviço de uma versão de tipo de aplicativo do cluster.

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
Remova um(s) certificado(s) cliente(s) ou (s) nome(s) de certificado(s) de ser usado para autenticação do cliente para o cluster.

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
Remova um certificado de cluster de ser usado para segurança de cluster.

### [Remove-AzServiceFabricManagedCluster](Remove-AzServiceFabricManagedCluster.md)
Remover recurso de cluster.

### [Remove-AzServiceFabricManagedClusterClientCertificate](Remove-AzServiceFabricManagedClusterClientCertificate.md)
Revogar o certificado do cliente por impressão digital ou nome comum.

### [Remove-AzServiceFabricManagedNodeType](Remove-AzServiceFabricManagedNodeType.md)
Remova o tipo de nó ou nós específicos dentro do tipo de nó.

### [Remove-AzServiceFabricManagedNodeTypeVMExtension](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
Remova a extensão vm do tipo de nó.

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
Remover nós do tipo de nó específico de um cluster.

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
Remover um tipo de nó completo de um cluster.

### [Remove-AzServiceFabricService](Remove-AzServiceFabricService.md)
Remover um serviço do cluster.

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
Remova uma ou várias configurações de Malha de Serviço do cluster.

### [Restart-AzServiceFabricManagedNodeType](Restart-AzServiceFabricManagedNodeType.md)
Reinicie nós específicos do tipo de nó.

### [Set-AzServiceFabricManagedCluster](Set-AzServiceFabricManagedCluster.md)
Definir propriedades de recurso de cluster.

### [Set-AzServiceFabricManagedNodeType](Set-AzServiceFabricManagedNodeType.md)
Define propriedades de recurso de tipo de nó ou executar ações de reimagem em ndes específicos do tipo de nó com o parâmetro -Reimage.

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
Adicione ou atualize uma ou várias configurações de Malha de Serviço ao cluster.

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
Altere o tipo de atualização de Malha de Serviço do cluster.

### [Update-AzServiceFabricApplication](Update-AzServiceFabricApplication.md)
Atualizar um aplicativo de malha de serviço. Isso permite atualizar os parâmetros do aplicativo e/ou atualizar a versão do tipo de aplicativo que disparará uma atualização de aplicativo.

### [Update-AzServiceFabric Rastreaability](Update-AzServiceFabricDurability.md)
Atualize o nível de durabilidade ou vmSku de um tipo de nó no cluster.

### [Update-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
Atualize o nível de confiabilidade do tipo de nó principal em um cluster.

