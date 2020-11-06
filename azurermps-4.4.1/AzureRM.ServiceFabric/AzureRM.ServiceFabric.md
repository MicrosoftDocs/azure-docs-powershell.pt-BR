---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 9c71788abd7707931df2c25279c265bbe9967bbf
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93425422"
---
# <span data-ttu-id="ad914-101">Módulo AzureRM. emfabric</span><span class="sxs-lookup"><span data-stu-id="ad914-101">AzureRM.ServiceFabric Module</span></span>
## <span data-ttu-id="ad914-102">Descritivo</span><span class="sxs-lookup"><span data-stu-id="ad914-102">Description</span></span>
<span data-ttu-id="ad914-103">Módulo do Azure Service Fabric que você pode usar para automatizar as operações de fim-2, como a criação de um cluster seguro, a transferência de certificados de cluster, a adição ou remoção de nós do cluster, etc. A lista completa de todas as operações estão listadas abaixo.</span><span class="sxs-lookup"><span data-stu-id="ad914-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="ad914-104">Cmdlets do AzureRM. infabric</span><span class="sxs-lookup"><span data-stu-id="ad914-104">AzureRM.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="ad914-105">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="ad914-105">Add-AzureRmServiceFabricApplicationCertificate</span></span>](Add-AzureRmServiceFabricApplicationCertificate.md)
<span data-ttu-id="ad914-106">Adicionar um certificado que será usado como certificado do aplicativo</span><span class="sxs-lookup"><span data-stu-id="ad914-106">Add a certificate that will be used as application certificate</span></span>

### [<span data-ttu-id="ad914-107">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ad914-107">Add-AzureRmServiceFabricClientCertificate</span></span>](Add-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="ad914-108">Adicionar nome comum ou impressão digital às configurações do cluster para autenticação do cliente</span><span class="sxs-lookup"><span data-stu-id="ad914-108">Add common name or thumbprint to the cluster settings for client authentication</span></span>

### [<span data-ttu-id="ad914-109">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="ad914-109">Add-AzureRmServiceFabricClusterCertificate</span></span>](Add-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="ad914-110">Adicionar um certificado de cluster secundário ao cluster para a substituição do certificado existente</span><span class="sxs-lookup"><span data-stu-id="ad914-110">Add a secondary cluster certificate to the cluster for rolling over the existing certificate</span></span> 

### [<span data-ttu-id="ad914-111">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="ad914-111">Add-AzureRmServiceFabricNode</span></span>](Add-AzureRmServiceFabricNode.md)
<span data-ttu-id="ad914-112">Adicionar nós/VMs a um tipo de nó específico a um cluster</span><span class="sxs-lookup"><span data-stu-id="ad914-112">Add nodes/VMs to a specific node type to a cluster</span></span>

### [<span data-ttu-id="ad914-113">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="ad914-113">Add-AzureRmServiceFabricNodeType</span></span>](Add-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="ad914-114">Adicionar um tipo de nó/VMs a um cluster existente</span><span class="sxs-lookup"><span data-stu-id="ad914-114">Add a node type/VMs to an existing cluster</span></span>

### [<span data-ttu-id="ad914-115">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="ad914-115">Get-AzureRmServiceFabricCluster</span></span>](Get-AzureRmServiceFabricCluster.md)
<span data-ttu-id="ad914-116">Obter os detalhes do recurso de cluster</span><span class="sxs-lookup"><span data-stu-id="ad914-116">Get the details of the cluster resource</span></span> 

### [<span data-ttu-id="ad914-117">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="ad914-117">New-AzureRmServiceFabricCluster</span></span>](New-AzureRmServiceFabricCluster.md)
<span data-ttu-id="ad914-118">Crie um novo cluster do enfabric.</span><span class="sxs-lookup"><span data-stu-id="ad914-118">Create an new ServiceFabric cluster.</span></span> <span data-ttu-id="ad914-119">Esse comando tem muitas sobrecargas para cobrir vários cenários</span><span class="sxs-lookup"><span data-stu-id="ad914-119">This command has many overloads to cover various scenarios</span></span>

### [<span data-ttu-id="ad914-120">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ad914-120">Remove-AzureRmServiceFabricClientCertificate</span></span>](Remove-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="ad914-121">Remover o certificado do cliente de ser usado para acessar o cluster</span><span class="sxs-lookup"><span data-stu-id="ad914-121">Remove client certificate from being used to access the cluster</span></span>

### [<span data-ttu-id="ad914-122">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="ad914-122">Remove-AzureRmServiceFabricClusterCertificate</span></span>](Remove-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="ad914-123">Remover o certificado do cluster de ser usado para segurança do cluster</span><span class="sxs-lookup"><span data-stu-id="ad914-123">Remove cluster certificate from being used for cluster security</span></span>

### [<span data-ttu-id="ad914-124">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="ad914-124">Remove-AzureRmServiceFabricNode</span></span>](Remove-AzureRmServiceFabricNode.md)
<span data-ttu-id="ad914-125">Remover nós do tipo de nó específico de um cluster</span><span class="sxs-lookup"><span data-stu-id="ad914-125">Remove nodes from the specific node type from a cluster</span></span>

### [<span data-ttu-id="ad914-126">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="ad914-126">Remove-AzureRmServiceFabricNodeType</span></span>](Remove-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="ad914-127">Remover um tipo de nó de um cluster</span><span class="sxs-lookup"><span data-stu-id="ad914-127">Remove a node type from a cluster</span></span>

### [<span data-ttu-id="ad914-128">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="ad914-128">Remove-AzureRmServiceFabricSetting</span></span>](Remove-AzureRmServiceFabricSetting.md)
<span data-ttu-id="ad914-129">Remover uma ou mais configurações do refabric do cluster</span><span class="sxs-lookup"><span data-stu-id="ad914-129">Remove one or more ServiceFabric settings from the cluster</span></span>

### [<span data-ttu-id="ad914-130">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="ad914-130">Set-AzureRmServiceFabricSetting</span></span>](Set-AzureRmServiceFabricSetting.md)
<span data-ttu-id="ad914-131">Adicionar ou atualizar uma ou mais configurações do enfabric para o cluster</span><span class="sxs-lookup"><span data-stu-id="ad914-131">Add or update one or more ServiceFabric settings to the cluster</span></span>

### [<span data-ttu-id="ad914-132">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="ad914-132">Set-AzureRmServiceFabricUpgradeType</span></span>](Set-AzureRmServiceFabricUpgradeType.md)
<span data-ttu-id="ad914-133">Alterar o tipo de atualização do Outfabric de um cluster</span><span class="sxs-lookup"><span data-stu-id="ad914-133">Change the ServiceFabric upgrade type of a cluster</span></span>

### [<span data-ttu-id="ad914-134">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="ad914-134">Update-AzureRmServiceFabricDurability</span></span>](Update-AzureRmServiceFabricDurability.md)
<span data-ttu-id="ad914-135">Alterar a camada de durabilidade de um cluster</span><span class="sxs-lookup"><span data-stu-id="ad914-135">Change the durability tier of a cluster</span></span>

### [<span data-ttu-id="ad914-136">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="ad914-136">Update-AzureRmServiceFabricReliability</span></span>](Update-AzureRmServiceFabricReliability.md)
<span data-ttu-id="ad914-137">Alterar a camada de confiabilidade de um cluster</span><span class="sxs-lookup"><span data-stu-id="ad914-137">Change the reliability tier of a cluster</span></span>
