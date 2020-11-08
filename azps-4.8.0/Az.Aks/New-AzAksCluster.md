---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: f7a3479fb7fd70c47d5d4d3b80004cb25d9baa0c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110695"
---
# <span data-ttu-id="943da-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="943da-101">New-AzAksCluster</span></span>

## <span data-ttu-id="943da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="943da-102">SYNOPSIS</span></span>
<span data-ttu-id="943da-103">Crie um novo cluster gerenciado kubernetes.</span><span class="sxs-lookup"><span data-stu-id="943da-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="943da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="943da-104">SYNTAX</span></span>

```
New-AzAksCluster [-Force] [-GenerateSshKey] [-NodeVmSetType <String>] [-NodeVnetSubnetID <String>]
 [-NodeMaxPodCount <Int32>] [-NodeOsType <String>] [-NodeSetPriority <String>] [-NodePoolMode <String>]
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

## <span data-ttu-id="943da-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="943da-105">DESCRIPTION</span></span>

<span data-ttu-id="943da-106">Crie um novo cluster de serviço do Azure kubernetes (AKS).</span><span class="sxs-lookup"><span data-stu-id="943da-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="943da-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="943da-107">EXAMPLES</span></span>

### <span data-ttu-id="943da-108">Novo AKS com parâmetros padrão.</span><span class="sxs-lookup"><span data-stu-id="943da-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="943da-109">Crie um contêiner do Windows Server em um AKS.</span><span class="sxs-lookup"><span data-stu-id="943da-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="943da-110">Para criar um contêiner do Windows Server em um AKS, você deve especificar pelo menos quatro parâmetros a seguir ao criar AKS, e o valor e `NetworkPlugin` `NodeVmSetType` deve ser `azure` e `VirtualMachineScaleSets` respectivamente.</span><span class="sxs-lookup"><span data-stu-id="943da-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword *** -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="943da-111">OS</span><span class="sxs-lookup"><span data-stu-id="943da-111">PARAMETERS</span></span>

### <span data-ttu-id="943da-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="943da-112">-AcrNameToAttach</span></span>
<span data-ttu-id="943da-113">Conceda a função "acrpull" do ACR especificado à entidade de serviço AKS, por exemplo, myacr</span><span class="sxs-lookup"><span data-stu-id="943da-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

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

### <span data-ttu-id="943da-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="943da-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="943da-115">Nomes de complemento a serem habilitados quando o cluster for criado.</span><span class="sxs-lookup"><span data-stu-id="943da-115">Add-on names to be enabled when cluster is created.</span></span>

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

### <span data-ttu-id="943da-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="943da-116">-AsJob</span></span>
<span data-ttu-id="943da-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="943da-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="943da-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="943da-118">-DefaultProfile</span></span>
<span data-ttu-id="943da-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="943da-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="943da-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="943da-120">-DnsNamePrefix</span></span>
<span data-ttu-id="943da-121">O prefixo do nome DNS para o cluster.</span><span class="sxs-lookup"><span data-stu-id="943da-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="943da-122">O comprimento deve ser <= 9 se os usuários planejam adicionar contêiner do Windows.</span><span class="sxs-lookup"><span data-stu-id="943da-122">The length must be <= 9 if users plan to add windows container.</span></span>

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

### <span data-ttu-id="943da-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="943da-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="943da-124">Se o dimensionador automático deve ser habilitado</span><span class="sxs-lookup"><span data-stu-id="943da-124">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="943da-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="943da-125">-EnableRbac</span></span>
<span data-ttu-id="943da-126">Se deseja habilitar o acesso Role-Based do kubernetes</span><span class="sxs-lookup"><span data-stu-id="943da-126">Whether to enable Kubernetes Role-Based Access</span></span>

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

### <span data-ttu-id="943da-127">-Force</span><span class="sxs-lookup"><span data-stu-id="943da-127">-Force</span></span>
<span data-ttu-id="943da-128">Criar cluster mesmo que ele já exista</span><span class="sxs-lookup"><span data-stu-id="943da-128">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="943da-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="943da-129">-GenerateSshKey</span></span>
<span data-ttu-id="943da-130">Gerar o arquivo de chave SSH para {HOME}/.ssh/id_rsa.</span><span class="sxs-lookup"><span data-stu-id="943da-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

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

### <span data-ttu-id="943da-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="943da-131">-KubernetesVersion</span></span>
<span data-ttu-id="943da-132">A versão do kubernetes a ser usada para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="943da-132">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="943da-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="943da-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="943da-134">Nome de usuário para as máquinas virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="943da-134">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="943da-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="943da-135">-LoadBalancerSku</span></span>
<span data-ttu-id="943da-136">A SKU do balanceador de carga do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="943da-136">The load balancer sku for the managed cluster.</span></span>

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

### <span data-ttu-id="943da-137">-Local</span><span class="sxs-lookup"><span data-stu-id="943da-137">-Location</span></span>
<span data-ttu-id="943da-138">Local do Azure para o cluster.</span><span class="sxs-lookup"><span data-stu-id="943da-138">Azure location for the cluster.</span></span>
<span data-ttu-id="943da-139">O padrão é o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="943da-139">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="943da-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="943da-140">-Name</span></span>
<span data-ttu-id="943da-141">Kubernetes nome do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="943da-141">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="943da-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="943da-142">-NetworkPlugin</span></span>
<span data-ttu-id="943da-143">Plugin de rede usado para construir kubernetes rede.</span><span class="sxs-lookup"><span data-stu-id="943da-143">Network plugin used for building Kubernetes network.</span></span>

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

### <span data-ttu-id="943da-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="943da-144">-NodeCount</span></span>
<span data-ttu-id="943da-145">O número padrão de nós para os pools de nós.</span><span class="sxs-lookup"><span data-stu-id="943da-145">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="943da-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="943da-146">-NodeMaxCount</span></span>
<span data-ttu-id="943da-147">Número máximo de nós para dimensionamento automático</span><span class="sxs-lookup"><span data-stu-id="943da-147">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="943da-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="943da-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="943da-149">Número máximo de pods que podem ser executados no nó.</span><span class="sxs-lookup"><span data-stu-id="943da-149">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="943da-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="943da-150">-NodeMinCount</span></span>
<span data-ttu-id="943da-151">Número mínimo de nós para dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="943da-151">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="943da-152">-NodeName</span><span class="sxs-lookup"><span data-stu-id="943da-152">-NodeName</span></span>
<span data-ttu-id="943da-153">Nome exclusivo do perfil do pool do agente no contexto da assinatura e do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="943da-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="943da-154">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="943da-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="943da-155">Tamanho em GB do disco do sistema operacional para cada nó no pool de nós.</span><span class="sxs-lookup"><span data-stu-id="943da-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="943da-156">Mínimo de 30 GB.</span><span class="sxs-lookup"><span data-stu-id="943da-156">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="943da-157">-NodeOsType</span><span class="sxs-lookup"><span data-stu-id="943da-157">-NodeOsType</span></span>
<span data-ttu-id="943da-158">OsType a ser usado para especificar o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="943da-158">OsType to be used to specify os type.</span></span> <span data-ttu-id="943da-159">Escolha entre Linux e Windows.</span><span class="sxs-lookup"><span data-stu-id="943da-159">Choose from Linux and Windows.</span></span> <span data-ttu-id="943da-160">Padrão para Linux.</span><span class="sxs-lookup"><span data-stu-id="943da-160">Default to Linux.</span></span>

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

### <span data-ttu-id="943da-161">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="943da-161">-NodePoolMode</span></span>
<span data-ttu-id="943da-162">NodePoolMode representa o modo de um pool de nós.</span><span class="sxs-lookup"><span data-stu-id="943da-162">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="943da-163">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="943da-163">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="943da-164">ScaleSetEvictionPolicy a ser usado para especificar a política de remoção para conjunto de escala de máquina virtual de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="943da-164">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="943da-165">Padrão a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="943da-165">Default to Delete.</span></span>

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

### <span data-ttu-id="943da-166">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="943da-166">-NodeSetPriority</span></span>
<span data-ttu-id="943da-167">ScaleSetPriority a ser usado para especificar a prioridade do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="943da-167">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="943da-168">O padrão é normal.</span><span class="sxs-lookup"><span data-stu-id="943da-168">Default to regular.</span></span>

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

### <span data-ttu-id="943da-169">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="943da-169">-NodeVmSetType</span></span>
<span data-ttu-id="943da-170">AgentPoolType representa tipos de um pool de agente.</span><span class="sxs-lookup"><span data-stu-id="943da-170">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="943da-171">Os valores possíveis incluem: ' VirtualMachineScaleSets ', ' Availabilityset '</span><span class="sxs-lookup"><span data-stu-id="943da-171">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="943da-172">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="943da-172">-NodeVmSize</span></span>
<span data-ttu-id="943da-173">O tamanho da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="943da-173">The size of the Virtual Machine.</span></span> <span data-ttu-id="943da-174">O valor padrão é Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="943da-174">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="943da-175">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="943da-175">-NodeVnetSubnetID</span></span>
<span data-ttu-id="943da-176">Subnetid VNet especifica o identificador de sub-rede da VNet.</span><span class="sxs-lookup"><span data-stu-id="943da-176">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="943da-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="943da-177">-ResourceGroupName</span></span>
<span data-ttu-id="943da-178">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="943da-178">Resource Group Name.</span></span>

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

### <span data-ttu-id="943da-179">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="943da-179">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="943da-180">A ID do cliente e o segredo do cliente associado à entidade de serviço/aplicativo AAD.</span><span class="sxs-lookup"><span data-stu-id="943da-180">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClientIdAndSecret

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="943da-181">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="943da-181">-SshKeyValue</span></span>
<span data-ttu-id="943da-182">Chave do arquivo de chave SSH ou caminho do arquivo de chave.</span><span class="sxs-lookup"><span data-stu-id="943da-182">SSH key file value or key file path.</span></span>
<span data-ttu-id="943da-183">O padrão é {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="943da-183">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="943da-184">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="943da-184">-SubnetName</span></span>
<span data-ttu-id="943da-185">Nome da sub-rede do VirtualNode addon.</span><span class="sxs-lookup"><span data-stu-id="943da-185">Subnet name of VirtualNode addon.</span></span>

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

### <span data-ttu-id="943da-186">-Marca</span><span class="sxs-lookup"><span data-stu-id="943da-186">-Tag</span></span>
<span data-ttu-id="943da-187">Marcas a serem aplicadas ao recurso</span><span class="sxs-lookup"><span data-stu-id="943da-187">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="943da-188">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="943da-188">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="943da-189">O nome de usuário do administrador a ser usado para VMs do Windows.</span><span class="sxs-lookup"><span data-stu-id="943da-189">The administrator username to use for Windows VMs.</span></span>

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

### <span data-ttu-id="943da-190">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="943da-190">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="943da-191">A senha de administrador para usar para VMs do Windows, o seu comprimento deve ter pelo menos 12, contendo pelo menos um caractere minúsculo, ou seja `[a-z]` , um `[A-Z]` caractere especial e um caractere especial `[!@#$%^&*()]` .</span><span class="sxs-lookup"><span data-stu-id="943da-191">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&*()]`.</span></span>

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

### <span data-ttu-id="943da-192">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="943da-192">-WorkspaceResourceId</span></span>
<span data-ttu-id="943da-193">ID do recurso do espaço de trabalho de complemento de monitoração.</span><span class="sxs-lookup"><span data-stu-id="943da-193">Resource Id of the workspace of Monitoring addon.</span></span>

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

### <span data-ttu-id="943da-194">-Confirme</span><span class="sxs-lookup"><span data-stu-id="943da-194">-Confirm</span></span>
<span data-ttu-id="943da-195">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="943da-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="943da-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="943da-196">-WhatIf</span></span>
<span data-ttu-id="943da-197">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="943da-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="943da-198">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="943da-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="943da-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="943da-199">CommonParameters</span></span>
<span data-ttu-id="943da-200">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="943da-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="943da-201">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="943da-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="943da-202">SENSORES</span><span class="sxs-lookup"><span data-stu-id="943da-202">INPUTS</span></span>

### <span data-ttu-id="943da-203">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="943da-203">None</span></span>

## <span data-ttu-id="943da-204">EXIBE</span><span class="sxs-lookup"><span data-stu-id="943da-204">OUTPUTS</span></span>

### <span data-ttu-id="943da-205">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="943da-205">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="943da-206">INFORMA</span><span class="sxs-lookup"><span data-stu-id="943da-206">NOTES</span></span>

## <span data-ttu-id="943da-207">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="943da-207">RELATED LINKS</span></span>
