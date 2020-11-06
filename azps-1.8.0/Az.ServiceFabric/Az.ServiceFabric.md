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
# <span data-ttu-id="72be5-101">Módulo AZ. Superfabric</span><span class="sxs-lookup"><span data-stu-id="72be5-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="72be5-102">Descritivo</span><span class="sxs-lookup"><span data-stu-id="72be5-102">Description</span></span>
<span data-ttu-id="72be5-103">Módulo do Azure Service Fabric que você pode usar para automatizar as operações de fim-2, como a criação de um cluster seguro, a transferência de certificados de cluster, a adição ou remoção de nós do cluster, etc. A lista completa de todas as operações estão listadas abaixo.</span><span class="sxs-lookup"><span data-stu-id="72be5-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="72be5-104">Cmdlets do AZ. infabric</span><span class="sxs-lookup"><span data-stu-id="72be5-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="72be5-105">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="72be5-105">Add-AzServiceFabricApplicationCertificate</span></span>](Add-AzServiceFabricApplicationCertificate.md)
<span data-ttu-id="72be5-106">Adicione um novo certificado ao (s) conjunto (s) de escala da máquina virtual que compõe o cluster.</span><span class="sxs-lookup"><span data-stu-id="72be5-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="72be5-107">O certificado deve ser usado como um certificado de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="72be5-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="72be5-108">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="72be5-108">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="72be5-109">Adicione um nome comum ou impressão digital ao cluster para fins de autenticação do cliente.</span><span class="sxs-lookup"><span data-stu-id="72be5-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="72be5-110">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="72be5-110">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="72be5-111">Adicione um certificado de cluster secundário ao cluster.</span><span class="sxs-lookup"><span data-stu-id="72be5-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="72be5-112">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="72be5-112">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="72be5-113">Adicione nós ao tipo de nó específico no cluster.</span><span class="sxs-lookup"><span data-stu-id="72be5-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="72be5-114">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="72be5-114">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="72be5-115">Adicione um novo tipo de nó ao cluster existente.</span><span class="sxs-lookup"><span data-stu-id="72be5-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="72be5-116">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="72be5-116">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="72be5-117">Obter os detalhes do recurso de cluster.</span><span class="sxs-lookup"><span data-stu-id="72be5-117">Get the cluster resource details.</span></span>

### [<span data-ttu-id="72be5-118">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="72be5-118">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="72be5-119">Esse comando usa certificados que você fornece ou certificados autoassinados gerados pelo sistema para configurar um novo cluster de Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="72be5-119">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="72be5-120">Ele pode usar um modelo padrão ou um modelo personalizado fornecido por você.</span><span class="sxs-lookup"><span data-stu-id="72be5-120">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="72be5-121">Você tem a opção de especificar uma pasta para exportar os certificados autoassinados ou para extraí-los mais tarde do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="72be5-121">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="72be5-122">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="72be5-122">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="72be5-123">Remova o (s) certificado (s) do (s) certificado (s) de cliente ou nome (s) dos (s) nome (s) da sua utilização para autenticação de cliente</span><span class="sxs-lookup"><span data-stu-id="72be5-123">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="72be5-124">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="72be5-124">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="72be5-125">Remover um certificado de cluster de ser usado para a segurança do cluster.</span><span class="sxs-lookup"><span data-stu-id="72be5-125">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="72be5-126">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="72be5-126">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="72be5-127">Remover nós do tipo de nó específico de um cluster.</span><span class="sxs-lookup"><span data-stu-id="72be5-127">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="72be5-128">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="72be5-128">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="72be5-129">Remover um tipo de nó completo de um cluster.</span><span class="sxs-lookup"><span data-stu-id="72be5-129">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="72be5-130">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="72be5-130">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="72be5-131">Remova uma ou várias configurações da malha de serviço do cluster.</span><span class="sxs-lookup"><span data-stu-id="72be5-131">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="72be5-132">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="72be5-132">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="72be5-133">Adicione ou atualize uma ou várias configurações do Service Fabric para o cluster.</span><span class="sxs-lookup"><span data-stu-id="72be5-133">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="72be5-134">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="72be5-134">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="72be5-135">Altere o tipo de atualização do Service Fabric do cluster.</span><span class="sxs-lookup"><span data-stu-id="72be5-135">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="72be5-136">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="72be5-136">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="72be5-137">Atualize a camada de durabilidade ou o VmSku de um tipo de nó no cluster.</span><span class="sxs-lookup"><span data-stu-id="72be5-137">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="72be5-138">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="72be5-138">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="72be5-139">Atualize a camada de confiabilidade do tipo de nó primário em um cluster.</span><span class="sxs-lookup"><span data-stu-id="72be5-139">Update the reliability tier of the primary node type in a cluster.</span></span>

