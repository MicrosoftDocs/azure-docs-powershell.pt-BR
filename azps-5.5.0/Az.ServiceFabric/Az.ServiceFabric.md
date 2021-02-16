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
# <span data-ttu-id="0bbf9-101">Módulo Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0bbf9-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="0bbf9-102">Descrição</span><span class="sxs-lookup"><span data-stu-id="0bbf9-102">Description</span></span>
<span data-ttu-id="0bbf9-103">Módulo de Malha de Serviço do Azure que você pode usar para automatizar as operações de ponta a ponta, como criar um cluster seguro, rolar por certificados de cluster, adicionar ou remover nós do cluster, etc. A lista completa de todas as operações está listada abaixo.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="0bbf9-104">Az.ServiceFabric Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0bbf9-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="0bbf9-105">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0bbf9-105">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="0bbf9-106">Adicione um nome comum ou uma impressão digital ao cluster para fins de autenticação do cliente.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-106">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="0bbf9-107">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="0bbf9-107">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="0bbf9-108">Adicione um certificado de cluster secundário ao cluster.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-108">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="0bbf9-109">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0bbf9-109">Add-AzServiceFabricManagedClusterClientCertificate</span></span>](Add-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="0bbf9-110">Adicione o nome comum do certificado ou a impressão digital ao cluster.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-110">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="0bbf9-111">Isso registrará o certificado novamente no cluster para fins de autenticação do cliente.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-111">This will register the certificate agains the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="0bbf9-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="0bbf9-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="0bbf9-113">Adicione a extensão vm ao tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-113">Add vm extension to the node type.</span></span>

### [<span data-ttu-id="0bbf9-114">Add-AzServiceFabricManagedNodeTypeVMSecduto</span><span class="sxs-lookup"><span data-stu-id="0bbf9-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
<span data-ttu-id="0bbf9-115">Adicione um segredo de certificado ao tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-115">Add certificate secret to the node type.</span></span>

### [<span data-ttu-id="0bbf9-116">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="0bbf9-116">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="0bbf9-117">Adicione nós ao tipo de nó específico no cluster.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-117">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="0bbf9-118">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="0bbf9-118">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="0bbf9-119">Adicione um novo tipo de nó ao cluster existente.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-119">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="0bbf9-120">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0bbf9-120">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="0bbf9-121">Obter detalhes do aplicativo Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-121">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="0bbf9-122">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0bbf9-122">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="0bbf9-123">Obter detalhes do tipo de aplicativo Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-123">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="0bbf9-124">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0bbf9-124">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="0bbf9-125">Obter detalhes da versão do tipo de aplicativo Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-125">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="0bbf9-126">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="0bbf9-126">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="0bbf9-127">Obter os detalhes do recurso de cluster.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-127">Get the cluster resource details.</span></span>

### [<span data-ttu-id="0bbf9-128">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="0bbf9-128">Get-AzServiceFabricManagedCluster</span></span>](Get-AzServiceFabricManagedCluster.md)
<span data-ttu-id="0bbf9-129">Obter os detalhes do recurso de cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-129">Get the managed cluster resource details.</span></span>

### [<span data-ttu-id="0bbf9-130">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="0bbf9-130">Get-AzServiceFabricManagedNodeType</span></span>](Get-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="0bbf9-131">Obter detalhes do recurso de tipo de nó gerenciado.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-131">Get the managed node type resource details.</span></span>

### [<span data-ttu-id="0bbf9-132">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="0bbf9-132">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="0bbf9-133">Obter detalhes do serviço de Malha de Serviço sob o aplicativo e o cluster especificados.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-133">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="0bbf9-134">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0bbf9-134">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="0bbf9-135">Crie um novo aplicativo de malha de serviço sob o grupo de recursos e cluster especificados.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-135">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="0bbf9-136">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0bbf9-136">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="0bbf9-137">Crie um novo tipo de aplicativo de malha de serviço sob o grupo e o cluster de recursos especificados.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-137">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="0bbf9-138">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0bbf9-138">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="0bbf9-139">Crie uma nova versão de tipo de aplicativo sob o grupo de recursos e cluster especificados.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-139">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="0bbf9-140">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="0bbf9-140">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="0bbf9-141">Esse comando usa certificados que você fornece ou que o sistema gera certificados auto-assinados para configurar um novo cluster de malha de serviço.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-141">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="0bbf9-142">Ele pode usar um modelo padrão ou um modelo personalizado que você fornecer.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-142">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="0bbf9-143">Você tem a opção de especificar uma pasta para exportar os certificados auto-assinados ou busca-los mais tarde no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-143">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

### [<span data-ttu-id="0bbf9-144">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="0bbf9-144">New-AzServiceFabricManagedCluster</span></span>](New-AzServiceFabricManagedCluster.md)
<span data-ttu-id="0bbf9-145">Criar novo cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-145">Create new managed cluster.</span></span>

### [<span data-ttu-id="0bbf9-146">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="0bbf9-146">New-AzServiceFabricManagedNodeType</span></span>](New-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="0bbf9-147">Criar novo recurso de tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-147">Create new node type resource.</span></span>

### [<span data-ttu-id="0bbf9-148">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="0bbf9-148">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="0bbf9-149">Crie um novo serviço de malha de serviço sob o aplicativo e cluster especificados.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-149">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="0bbf9-150">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0bbf9-150">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="0bbf9-151">Remover um aplicativo do cluster.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-151">Remove an application from the cluster.</span></span> <span data-ttu-id="0bbf9-152">Isso removerá todos os serviços sob o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-152">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="0bbf9-153">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0bbf9-153">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="0bbf9-154">Remover malha de serviço de um tipo de aplicativo do cluster.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-154">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="0bbf9-155">Isso removerá todas as versões do tipo sob esse recurso.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-155">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="0bbf9-156">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0bbf9-156">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="0bbf9-157">Remova a malha de serviço de uma versão de tipo de aplicativo do cluster.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-157">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="0bbf9-158">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0bbf9-158">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="0bbf9-159">Remova um(s) certificado(s) cliente(s) ou (s) nome(s) de certificado(s) de ser usado para autenticação do cliente para o cluster.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-159">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="0bbf9-160">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="0bbf9-160">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="0bbf9-161">Remova um certificado de cluster de ser usado para segurança de cluster.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-161">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="0bbf9-162">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="0bbf9-162">Remove-AzServiceFabricManagedCluster</span></span>](Remove-AzServiceFabricManagedCluster.md)
<span data-ttu-id="0bbf9-163">Remover recurso de cluster.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-163">Remove cluster resource.</span></span>

### [<span data-ttu-id="0bbf9-164">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0bbf9-164">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>](Remove-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="0bbf9-165">Revogar o certificado do cliente por impressão digital ou nome comum.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-165">Remvoe client certificate by thumbprint or common name.</span></span>

### [<span data-ttu-id="0bbf9-166">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="0bbf9-166">Remove-AzServiceFabricManagedNodeType</span></span>](Remove-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="0bbf9-167">Remova o tipo de nó ou nós específicos dentro do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-167">Remove the node type or specific nodes within the node type.</span></span>

### [<span data-ttu-id="0bbf9-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="0bbf9-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="0bbf9-169">Remova a extensão vm do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-169">Remove vm extension from the node type.</span></span>

### [<span data-ttu-id="0bbf9-170">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="0bbf9-170">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="0bbf9-171">Remover nós do tipo de nó específico de um cluster.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-171">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="0bbf9-172">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="0bbf9-172">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="0bbf9-173">Remover um tipo de nó completo de um cluster.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-173">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="0bbf9-174">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="0bbf9-174">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="0bbf9-175">Remover um serviço do cluster.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-175">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="0bbf9-176">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="0bbf9-176">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="0bbf9-177">Remova uma ou várias configurações de Malha de Serviço do cluster.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-177">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="0bbf9-178">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="0bbf9-178">Restart-AzServiceFabricManagedNodeType</span></span>](Restart-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="0bbf9-179">Reinicie nós específicos do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-179">Restart specific nodes from the node type.</span></span>

### [<span data-ttu-id="0bbf9-180">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="0bbf9-180">Set-AzServiceFabricManagedCluster</span></span>](Set-AzServiceFabricManagedCluster.md)
<span data-ttu-id="0bbf9-181">Definir propriedades de recurso de cluster.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-181">Set cluster resource properties.</span></span>

### [<span data-ttu-id="0bbf9-182">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="0bbf9-182">Set-AzServiceFabricManagedNodeType</span></span>](Set-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="0bbf9-183">Define propriedades de recurso de tipo de nó ou executar ações de reimagem em ndes específicos do tipo de nó com o parâmetro -Reimage.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-183">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

### [<span data-ttu-id="0bbf9-184">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="0bbf9-184">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="0bbf9-185">Adicione ou atualize uma ou várias configurações de Malha de Serviço ao cluster.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-185">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="0bbf9-186">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="0bbf9-186">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="0bbf9-187">Altere o tipo de atualização de Malha de Serviço do cluster.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-187">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="0bbf9-188">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0bbf9-188">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="0bbf9-189">Atualizar um aplicativo de malha de serviço.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-189">Update a service fabric application.</span></span> <span data-ttu-id="0bbf9-190">Isso permite atualizar os parâmetros do aplicativo e/ou atualizar a versão do tipo de aplicativo que disparará uma atualização de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-190">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="0bbf9-191">Update-AzServiceFabric Rastreaability</span><span class="sxs-lookup"><span data-stu-id="0bbf9-191">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="0bbf9-192">Atualize o nível de durabilidade ou vmSku de um tipo de nó no cluster.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-192">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="0bbf9-193">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="0bbf9-193">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="0bbf9-194">Atualize o nível de confiabilidade do tipo de nó principal em um cluster.</span><span class="sxs-lookup"><span data-stu-id="0bbf9-194">Update the reliability tier of the primary node type in a cluster.</span></span>

