---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 6d93775a028e7a590a8da9cc008640fb8484bdf2
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93425315"
---
# <span data-ttu-id="6cad8-101">Módulo AzureRM. emfabric</span><span class="sxs-lookup"><span data-stu-id="6cad8-101">AzureRM.ServiceFabric Module</span></span>
## <span data-ttu-id="6cad8-102">Descritivo</span><span class="sxs-lookup"><span data-stu-id="6cad8-102">Description</span></span>
<span data-ttu-id="6cad8-103">Módulo do Azure Service Fabric que você pode usar para automatizar as operações de fim-2, como a criação de um cluster seguro, a transferência de certificados de cluster, a adição ou remoção de nós do cluster, etc. A lista completa de todas as operações estão listadas abaixo.</span><span class="sxs-lookup"><span data-stu-id="6cad8-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="6cad8-104">Cmdlets do AzureRM. infabric</span><span class="sxs-lookup"><span data-stu-id="6cad8-104">AzureRM.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="6cad8-105">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="6cad8-105">Add-AzureRmServiceFabricApplicationCertificate</span></span>](Add-AzureRmServiceFabricApplicationCertificate.md)
<span data-ttu-id="6cad8-106">Adicione um novo certificado ao (s) conjunto (s) de escala da máquina virtual que compõe o cluster.</span><span class="sxs-lookup"><span data-stu-id="6cad8-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="6cad8-107">O certificado deve ser usado como um certificado de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6cad8-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="6cad8-108">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6cad8-108">Add-AzureRmServiceFabricClientCertificate</span></span>](Add-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="6cad8-109">Adicione um nome comum ou impressão digital ao cluster para fins de autenticação do cliente.</span><span class="sxs-lookup"><span data-stu-id="6cad8-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="6cad8-110">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="6cad8-110">Add-AzureRmServiceFabricClusterCertificate</span></span>](Add-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="6cad8-111">Adicione um certificado de cluster secundário ao cluster.</span><span class="sxs-lookup"><span data-stu-id="6cad8-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="6cad8-112">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="6cad8-112">Add-AzureRmServiceFabricNode</span></span>](Add-AzureRmServiceFabricNode.md)
<span data-ttu-id="6cad8-113">Adicione nós ao tipo de nó específico no cluster.</span><span class="sxs-lookup"><span data-stu-id="6cad8-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="6cad8-114">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="6cad8-114">Add-AzureRmServiceFabricNodeType</span></span>](Add-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="6cad8-115">Adicione um novo tipo de nó ao cluster existente.</span><span class="sxs-lookup"><span data-stu-id="6cad8-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="6cad8-116">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="6cad8-116">Get-AzureRmServiceFabricCluster</span></span>](Get-AzureRmServiceFabricCluster.md)
<span data-ttu-id="6cad8-117">Obter os detalhes do recurso de cluster.</span><span class="sxs-lookup"><span data-stu-id="6cad8-117">Get the cluster resource details.</span></span>

### [<span data-ttu-id="6cad8-118">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="6cad8-118">New-AzureRmServiceFabricCluster</span></span>](New-AzureRmServiceFabricCluster.md)
<span data-ttu-id="6cad8-119">Esse comando usa certificados que você fornece ou certificados autoassinados gerados pelo sistema para configurar um novo cluster de Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="6cad8-119">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="6cad8-120">Ele pode usar um modelo padrão ou um modelo personalizado fornecido por você.</span><span class="sxs-lookup"><span data-stu-id="6cad8-120">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="6cad8-121">Você tem a opção de especificar uma pasta para exportar os certificados autoassinados ou para extraí-los mais tarde do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="6cad8-121">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="6cad8-122">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6cad8-122">Remove-AzureRmServiceFabricClientCertificate</span></span>](Remove-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="6cad8-123">Remova o (s) certificado (s) do (s) certificado (s) de cliente ou nome (s) dos (s) nome (s) da sua utilização para autenticação de cliente</span><span class="sxs-lookup"><span data-stu-id="6cad8-123">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="6cad8-124">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="6cad8-124">Remove-AzureRmServiceFabricClusterCertificate</span></span>](Remove-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="6cad8-125">Remover um certificado de cluster de ser usado para a segurança do cluster.</span><span class="sxs-lookup"><span data-stu-id="6cad8-125">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="6cad8-126">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="6cad8-126">Remove-AzureRmServiceFabricNode</span></span>](Remove-AzureRmServiceFabricNode.md)
<span data-ttu-id="6cad8-127">Remover nós do tipo de nó específico de um cluster.</span><span class="sxs-lookup"><span data-stu-id="6cad8-127">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="6cad8-128">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="6cad8-128">Remove-AzureRmServiceFabricNodeType</span></span>](Remove-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="6cad8-129">Remover um tipo de nó completo de um cluster.</span><span class="sxs-lookup"><span data-stu-id="6cad8-129">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="6cad8-130">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="6cad8-130">Remove-AzureRmServiceFabricSetting</span></span>](Remove-AzureRmServiceFabricSetting.md)
<span data-ttu-id="6cad8-131">Remova uma ou várias configurações da malha de serviço do cluster.</span><span class="sxs-lookup"><span data-stu-id="6cad8-131">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="6cad8-132">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="6cad8-132">Set-AzureRmServiceFabricSetting</span></span>](Set-AzureRmServiceFabricSetting.md)
<span data-ttu-id="6cad8-133">Adicione ou atualize uma ou várias configurações do Service Fabric para o cluster.</span><span class="sxs-lookup"><span data-stu-id="6cad8-133">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="6cad8-134">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="6cad8-134">Set-AzureRmServiceFabricUpgradeType</span></span>](Set-AzureRmServiceFabricUpgradeType.md)
<span data-ttu-id="6cad8-135">Altere o tipo de atualização do Service Fabric do cluster.</span><span class="sxs-lookup"><span data-stu-id="6cad8-135">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="6cad8-136">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="6cad8-136">Update-AzureRmServiceFabricDurability</span></span>](Update-AzureRmServiceFabricDurability.md)
<span data-ttu-id="6cad8-137">Atualize a camada de durabilidade ou o VmSku de um tipo de nó no cluster.</span><span class="sxs-lookup"><span data-stu-id="6cad8-137">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="6cad8-138">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="6cad8-138">Update-AzureRmServiceFabricReliability</span></span>](Update-AzureRmServiceFabricReliability.md)
<span data-ttu-id="6cad8-139">Atualize a camada de confiabilidade do tipo de nó primário em um cluster.</span><span class="sxs-lookup"><span data-stu-id="6cad8-139">Update the reliability tier of the primary node type in a cluster.</span></span>

