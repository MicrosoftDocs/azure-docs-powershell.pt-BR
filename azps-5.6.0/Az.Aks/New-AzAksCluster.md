---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: 806c3a17dcfc470e01801548013d0d8c6ea58ae4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892672"
---
# <span data-ttu-id="d18c7-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="d18c7-101">New-AzAksCluster</span></span>

## <span data-ttu-id="d18c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d18c7-102">SYNOPSIS</span></span>
<span data-ttu-id="d18c7-103">Crie um novo cluster kubernetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="d18c7-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="d18c7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d18c7-104">SYNTAX</span></span>

```
New-AzAksCluster [-Force] [-GenerateSshKey] [-NodeVmSetType <String>] [-NodeVnetSubnetID <String>]
 [-NodeMaxPodCount <Int32>] [-NodeSetPriority <String>] [-NodePoolMode <String>]
 [-NodeScaleSetEvictionPolicy <String>] [-AddOnNameToBeEnabled <String[]>] [-WorkspaceResourceId <String>]
 [-SubnetName <String>] [-AcrNameToAttach <String>] [-EnableRbac] [-WindowsProfileAdminUserName <String>]
 [-WindowsProfileAdminUserPassword <SecureString>] [-NetworkPlugin <String>] [-LoadBalancerSku <String>]
 [-ResourceGroupName] <String> [-Name] <String> [[-ServicePrincipalIdAndSecret] <PSCredential>]
 [-Location <String>] [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>]
 [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d18c7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d18c7-105">DESCRIPTION</span></span>

<span data-ttu-id="d18c7-106">Crie um novo cluster do Azure Kubernetes Service(AKS).</span><span class="sxs-lookup"><span data-stu-id="d18c7-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="d18c7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d18c7-107">EXAMPLES</span></span>

### <span data-ttu-id="d18c7-108">Novo um AKS com params padrão.</span><span class="sxs-lookup"><span data-stu-id="d18c7-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="d18c7-109">Criar contêiner do Windows Server em um AKS.</span><span class="sxs-lookup"><span data-stu-id="d18c7-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="d18c7-110">Para criar o contêiner do Windows Server em um AKS, você deve especificar pelo menos quatro parâmetros a seguir ao criar o AKS, e o valor para e deve ser `NetworkPlugin` `NodeVmSetType` e `azure` `VirtualMachineScaleSets` respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d18c7-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword *** -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="d18c7-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d18c7-111">PARAMETERS</span></span>

### <span data-ttu-id="d18c7-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="d18c7-112">-AcrNameToAttach</span></span>
<span data-ttu-id="d18c7-113">Conceda a função 'acrpull' do ACR especificado à Entidade de Serviço do AKS, por exemplo, myacr</span><span class="sxs-lookup"><span data-stu-id="d18c7-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="d18c7-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="d18c7-115">Nomes de complemento a serem habilitados quando o cluster é criado.</span><span class="sxs-lookup"><span data-stu-id="d18c7-115">Add-on names to be enabled when cluster is created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d18c7-116">-AsJob</span></span>
<span data-ttu-id="d18c7-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d18c7-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d18c7-118">-DefaultProfile</span></span>
<span data-ttu-id="d18c7-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d18c7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="d18c7-120">-DnsNamePrefix</span></span>
<span data-ttu-id="d18c7-121">O prefixo de nome DNS para o cluster.</span><span class="sxs-lookup"><span data-stu-id="d18c7-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="d18c7-122">O comprimento deve ser <= 9 se os usuários planejam adicionar contêiner do Windows.</span><span class="sxs-lookup"><span data-stu-id="d18c7-122">The length must be <= 9 if users plan to add windows container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="d18c7-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="d18c7-124">Se deve habilitar o dimensionador automático</span><span class="sxs-lookup"><span data-stu-id="d18c7-124">Whether to enable auto-scaler</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="d18c7-125">-EnableRbac</span></span>
<span data-ttu-id="d18c7-126">Se habilitar o Kubernetes Role-Based Access</span><span class="sxs-lookup"><span data-stu-id="d18c7-126">Whether to enable Kubernetes Role-Based Access</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-127">-Force</span><span class="sxs-lookup"><span data-stu-id="d18c7-127">-Force</span></span>
<span data-ttu-id="d18c7-128">Criar cluster mesmo que ele já exista</span><span class="sxs-lookup"><span data-stu-id="d18c7-128">Create cluster even if it already exists</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="d18c7-129">-GenerateSshKey</span></span>
<span data-ttu-id="d18c7-130">Gerar arquivo de chave ssh para {HOME}/.ssh/id_rsa.</span><span class="sxs-lookup"><span data-stu-id="d18c7-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="d18c7-131">-KubernetesVersion</span></span>
<span data-ttu-id="d18c7-132">A versão do Kubernetes a ser usada para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="d18c7-132">The version of Kubernetes to use for creating the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="d18c7-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="d18c7-134">Nome de usuário para as Máquinas Virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="d18c7-134">User name for the Linux Virtual Machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AdminUserName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="d18c7-135">-LoadBalancerSku</span></span>
<span data-ttu-id="d18c7-136">O sku do balanceador de carga para o cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="d18c7-136">The load balancer sku for the managed cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-137">-Location</span><span class="sxs-lookup"><span data-stu-id="d18c7-137">-Location</span></span>
<span data-ttu-id="d18c7-138">Local do Azure para o cluster.</span><span class="sxs-lookup"><span data-stu-id="d18c7-138">Azure location for the cluster.</span></span>
<span data-ttu-id="d18c7-139">Padrão para o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d18c7-139">Defaults to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-140">-Name</span><span class="sxs-lookup"><span data-stu-id="d18c7-140">-Name</span></span>
<span data-ttu-id="d18c7-141">Nome do cluster gerenciado do Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="d18c7-141">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="d18c7-142">-NetworkPlugin</span></span>
<span data-ttu-id="d18c7-143">Plug-in de rede usado para a criação de rede Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="d18c7-143">Network plugin used for building Kubernetes network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: azure
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="d18c7-144">-NodeCount</span></span>
<span data-ttu-id="d18c7-145">O número padrão de nós para os pools de nós.</span><span class="sxs-lookup"><span data-stu-id="d18c7-145">The default number of nodes for the node pools.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="d18c7-146">-NodeMaxCount</span></span>
<span data-ttu-id="d18c7-147">Número máximo de nós para dimensionamento automático</span><span class="sxs-lookup"><span data-stu-id="d18c7-147">Maximum number of nodes for auto-scaling</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="d18c7-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="d18c7-149">Número máximo de pods que podem ser executados no nó.</span><span class="sxs-lookup"><span data-stu-id="d18c7-149">Maximum number of pods that can run on node.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="d18c7-150">-NodeMinCount</span></span>
<span data-ttu-id="d18c7-151">Número mínimo de nós para dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="d18c7-151">Minimum number of nodes for auto-scaling.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-152">-NodeName</span><span class="sxs-lookup"><span data-stu-id="d18c7-152">-NodeName</span></span>
<span data-ttu-id="d18c7-153">Nome exclusivo do perfil do pool de agentes no contexto da assinatura e do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d18c7-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-154">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="d18c7-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="d18c7-155">Tamanho em GB do disco do sistema operacional para cada nó no pool de nós.</span><span class="sxs-lookup"><span data-stu-id="d18c7-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="d18c7-156">Mínimo de 30 GB.</span><span class="sxs-lookup"><span data-stu-id="d18c7-156">Minimum 30 GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-157">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="d18c7-157">-NodePoolMode</span></span>
<span data-ttu-id="d18c7-158">NodePoolMode representa o modo de um pool de nós.</span><span class="sxs-lookup"><span data-stu-id="d18c7-158">NodePoolMode represents mode of an node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-159">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="d18c7-159">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="d18c7-160">ScaleSetEvictionPolicy a ser usado para especificar política de despejo para conjunto de escala de máquina virtual de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="d18c7-160">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="d18c7-161">Padrão para Excluir.</span><span class="sxs-lookup"><span data-stu-id="d18c7-161">Default to Delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-162">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="d18c7-162">-NodeSetPriority</span></span>
<span data-ttu-id="d18c7-163">ScaleSetPriority a ser usado para especificar prioridade de conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d18c7-163">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="d18c7-164">Padrão para regular.</span><span class="sxs-lookup"><span data-stu-id="d18c7-164">Default to regular.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-165">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="d18c7-165">-NodeVmSetType</span></span>
<span data-ttu-id="d18c7-166">AgentPoolType representa tipos de um pool de agentes.</span><span class="sxs-lookup"><span data-stu-id="d18c7-166">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="d18c7-167">Os valores possíveis incluem: 'VirtualMachineScaleSets', 'AvailabilitySet'</span><span class="sxs-lookup"><span data-stu-id="d18c7-167">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: VirtualMachineScaleSets
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-168">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="d18c7-168">-NodeVmSize</span></span>
<span data-ttu-id="d18c7-169">O tamanho da Máquina Virtual.</span><span class="sxs-lookup"><span data-stu-id="d18c7-169">The size of the Virtual Machine.</span></span> <span data-ttu-id="d18c7-170">O valor padrão é Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="d18c7-170">Default value is Standard_D2_v2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-171">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="d18c7-171">-NodeVnetSubnetID</span></span>
<span data-ttu-id="d18c7-172">A VNet SubnetID especifica o identificador de sub-rede da VNet.</span><span class="sxs-lookup"><span data-stu-id="d18c7-172">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d18c7-173">-ResourceGroupName</span></span>
<span data-ttu-id="d18c7-174">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="d18c7-174">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-175">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="d18c7-175">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="d18c7-176">A ID do cliente e o segredo do cliente associados à entidade de serviço/aplicativo AAD.</span><span class="sxs-lookup"><span data-stu-id="d18c7-176">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-177">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="d18c7-177">-SshKeyValue</span></span>
<span data-ttu-id="d18c7-178">Valor do arquivo de chave SSH ou caminho do arquivo de chave.</span><span class="sxs-lookup"><span data-stu-id="d18c7-178">SSH key file value or key file path.</span></span>
<span data-ttu-id="d18c7-179">O padrão é {HOME}/.ssh/id_rsa.pub.</span><span class="sxs-lookup"><span data-stu-id="d18c7-179">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-180">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="d18c7-180">-SubnetName</span></span>
<span data-ttu-id="d18c7-181">Nome da sub-rede do addon VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="d18c7-181">Subnet name of VirtualNode addon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="d18c7-182">-Tag</span></span>
<span data-ttu-id="d18c7-183">Marcas a serem aplicadas ao recurso</span><span class="sxs-lookup"><span data-stu-id="d18c7-183">Tags to be applied to the resource</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-184">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="d18c7-184">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="d18c7-185">O nome de usuário do administrador a ser usado para VMs do Windows.</span><span class="sxs-lookup"><span data-stu-id="d18c7-185">The administrator username to use for Windows VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-186">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="d18c7-186">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="d18c7-187">A senha do administrador a ser usada para VMs do Windows, seu comprimento deve ter pelo menos 12, contendo pelo menos um caractere de caso inferior, ou seja, um e um `[a-z]` `[A-Z]` caractere especial `[!@#$%^&*()]` .</span><span class="sxs-lookup"><span data-stu-id="d18c7-187">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&*()]`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-188">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="d18c7-188">-WorkspaceResourceId</span></span>
<span data-ttu-id="d18c7-189">ID de recurso do espaço de trabalho do addon monitoring.</span><span class="sxs-lookup"><span data-stu-id="d18c7-189">Resource Id of the workspace of Monitoring addon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-190">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d18c7-190">-Confirm</span></span>
<span data-ttu-id="d18c7-191">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d18c7-191">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d18c7-192">-WhatIf</span></span>
<span data-ttu-id="d18c7-193">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d18c7-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d18c7-194">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d18c7-194">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18c7-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d18c7-195">CommonParameters</span></span>
<span data-ttu-id="d18c7-196">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d18c7-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d18c7-197">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d18c7-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d18c7-198">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d18c7-198">INPUTS</span></span>

### <span data-ttu-id="d18c7-199">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d18c7-199">None</span></span>

## <span data-ttu-id="d18c7-200">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d18c7-200">OUTPUTS</span></span>

### <span data-ttu-id="d18c7-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="d18c7-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="d18c7-202">NOTES</span><span class="sxs-lookup"><span data-stu-id="d18c7-202">NOTES</span></span>

## <span data-ttu-id="d18c7-203">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d18c7-203">RELATED LINKS</span></span>
