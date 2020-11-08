---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: aaab86d7943072ae861acb71ec5021bb098a48ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117111"
---
# <span data-ttu-id="faf5b-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="faf5b-101">New-AzAksCluster</span></span>

## <span data-ttu-id="faf5b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="faf5b-102">SYNOPSIS</span></span>
<span data-ttu-id="faf5b-103">Crie um novo cluster gerenciado kubernetes.</span><span class="sxs-lookup"><span data-stu-id="faf5b-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="faf5b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="faf5b-104">SYNTAX</span></span>

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

## <span data-ttu-id="faf5b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="faf5b-105">DESCRIPTION</span></span>

<span data-ttu-id="faf5b-106">Crie um novo cluster de serviço do Azure kubernetes (AKS).</span><span class="sxs-lookup"><span data-stu-id="faf5b-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="faf5b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="faf5b-107">EXAMPLES</span></span>

### <span data-ttu-id="faf5b-108">Novo AKS com parâmetros padrão.</span><span class="sxs-lookup"><span data-stu-id="faf5b-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="faf5b-109">Crie um contêiner do Windows Server em um AKS.</span><span class="sxs-lookup"><span data-stu-id="faf5b-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="faf5b-110">Para criar um contêiner do Windows Server em um AKS, você deve especificar pelo menos quatro parâmetros a seguir ao criar AKS, e o valor e `NetworkPlugin` `NodeVmSetType` deve ser `azure` e `VirtualMachineScaleSets` respectivamente.</span><span class="sxs-lookup"><span data-stu-id="faf5b-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword **_ -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="faf5b-111">OS</span><span class="sxs-lookup"><span data-stu-id="faf5b-111">PARAMETERS</span></span>

### <span data-ttu-id="faf5b-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="faf5b-112">-AcrNameToAttach</span></span>
<span data-ttu-id="faf5b-113">Conceda a função "acrpull" do ACR especificado à entidade de serviço AKS, por exemplo, myacr</span><span class="sxs-lookup"><span data-stu-id="faf5b-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

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

### <span data-ttu-id="faf5b-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="faf5b-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="faf5b-115">Nomes de complemento a serem habilitados quando o cluster for criado.</span><span class="sxs-lookup"><span data-stu-id="faf5b-115">Add-on names to be enabled when cluster is created.</span></span>

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

### <span data-ttu-id="faf5b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="faf5b-116">-AsJob</span></span>
<span data-ttu-id="faf5b-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="faf5b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="faf5b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faf5b-118">-DefaultProfile</span></span>
<span data-ttu-id="faf5b-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="faf5b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="faf5b-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="faf5b-120">-DnsNamePrefix</span></span>
<span data-ttu-id="faf5b-121">O prefixo do nome DNS para o cluster.</span><span class="sxs-lookup"><span data-stu-id="faf5b-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="faf5b-122">O comprimento deve ser <= 9 se os usuários planejam adicionar contêiner do Windows.</span><span class="sxs-lookup"><span data-stu-id="faf5b-122">The length must be <= 9 if users plan to add windows container.</span></span>

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

### <span data-ttu-id="faf5b-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="faf5b-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="faf5b-124">Se o dimensionador automático deve ser habilitado</span><span class="sxs-lookup"><span data-stu-id="faf5b-124">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="faf5b-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="faf5b-125">-EnableRbac</span></span>
<span data-ttu-id="faf5b-126">Se deseja habilitar o acesso Role-Based do kubernetes</span><span class="sxs-lookup"><span data-stu-id="faf5b-126">Whether to enable Kubernetes Role-Based Access</span></span>

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

### <span data-ttu-id="faf5b-127">-Force</span><span class="sxs-lookup"><span data-stu-id="faf5b-127">-Force</span></span>
<span data-ttu-id="faf5b-128">Criar cluster mesmo que ele já exista</span><span class="sxs-lookup"><span data-stu-id="faf5b-128">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="faf5b-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="faf5b-129">-GenerateSshKey</span></span>
<span data-ttu-id="faf5b-130">Gerar o arquivo de chave SSH para {HOME}/.ssh/id_rsa.</span><span class="sxs-lookup"><span data-stu-id="faf5b-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

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

### <span data-ttu-id="faf5b-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="faf5b-131">-KubernetesVersion</span></span>
<span data-ttu-id="faf5b-132">A versão do kubernetes a ser usada para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="faf5b-132">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="faf5b-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="faf5b-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="faf5b-134">Nome de usuário para as máquinas virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="faf5b-134">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="faf5b-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="faf5b-135">-LoadBalancerSku</span></span>
<span data-ttu-id="faf5b-136">A SKU do balanceador de carga do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="faf5b-136">The load balancer sku for the managed cluster.</span></span>

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

### <span data-ttu-id="faf5b-137">-Local</span><span class="sxs-lookup"><span data-stu-id="faf5b-137">-Location</span></span>
<span data-ttu-id="faf5b-138">Local do Azure para o cluster.</span><span class="sxs-lookup"><span data-stu-id="faf5b-138">Azure location for the cluster.</span></span>
<span data-ttu-id="faf5b-139">O padrão é o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="faf5b-139">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="faf5b-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="faf5b-140">-Name</span></span>
<span data-ttu-id="faf5b-141">Kubernetes nome do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="faf5b-141">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="faf5b-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="faf5b-142">-NetworkPlugin</span></span>
<span data-ttu-id="faf5b-143">Plugin de rede usado para construir kubernetes rede.</span><span class="sxs-lookup"><span data-stu-id="faf5b-143">Network plugin used for building Kubernetes network.</span></span>

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

### <span data-ttu-id="faf5b-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="faf5b-144">-NodeCount</span></span>
<span data-ttu-id="faf5b-145">O número padrão de nós para os pools de nós.</span><span class="sxs-lookup"><span data-stu-id="faf5b-145">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="faf5b-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="faf5b-146">-NodeMaxCount</span></span>
<span data-ttu-id="faf5b-147">Número máximo de nós para dimensionamento automático</span><span class="sxs-lookup"><span data-stu-id="faf5b-147">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="faf5b-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="faf5b-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="faf5b-149">Número máximo de pods que podem ser executados no nó.</span><span class="sxs-lookup"><span data-stu-id="faf5b-149">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="faf5b-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="faf5b-150">-NodeMinCount</span></span>
<span data-ttu-id="faf5b-151">Número mínimo de nós para dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="faf5b-151">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="faf5b-152">-NodeName</span><span class="sxs-lookup"><span data-stu-id="faf5b-152">-NodeName</span></span>
<span data-ttu-id="faf5b-153">Nome exclusivo do perfil do pool do agente no contexto da assinatura e do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="faf5b-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="faf5b-154">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="faf5b-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="faf5b-155">Tamanho em GB do disco do sistema operacional para cada nó no pool de nós.</span><span class="sxs-lookup"><span data-stu-id="faf5b-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="faf5b-156">Mínimo de 30 GB.</span><span class="sxs-lookup"><span data-stu-id="faf5b-156">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="faf5b-157">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="faf5b-157">-NodePoolMode</span></span>
<span data-ttu-id="faf5b-158">NodePoolMode representa o modo de um pool de nós.</span><span class="sxs-lookup"><span data-stu-id="faf5b-158">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="faf5b-159">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="faf5b-159">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="faf5b-160">ScaleSetEvictionPolicy a ser usado para especificar a política de remoção para conjunto de escala de máquina virtual de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="faf5b-160">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="faf5b-161">Padrão a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="faf5b-161">Default to Delete.</span></span>

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

### <span data-ttu-id="faf5b-162">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="faf5b-162">-NodeSetPriority</span></span>
<span data-ttu-id="faf5b-163">ScaleSetPriority a ser usado para especificar a prioridade do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="faf5b-163">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="faf5b-164">O padrão é normal.</span><span class="sxs-lookup"><span data-stu-id="faf5b-164">Default to regular.</span></span>

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

### <span data-ttu-id="faf5b-165">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="faf5b-165">-NodeVmSetType</span></span>
<span data-ttu-id="faf5b-166">AgentPoolType representa tipos de um pool de agente.</span><span class="sxs-lookup"><span data-stu-id="faf5b-166">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="faf5b-167">Os valores possíveis incluem: ' VirtualMachineScaleSets ', ' Availabilityset '</span><span class="sxs-lookup"><span data-stu-id="faf5b-167">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="faf5b-168">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="faf5b-168">-NodeVmSize</span></span>
<span data-ttu-id="faf5b-169">O tamanho da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="faf5b-169">The size of the Virtual Machine.</span></span> <span data-ttu-id="faf5b-170">O valor padrão é Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="faf5b-170">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="faf5b-171">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="faf5b-171">-NodeVnetSubnetID</span></span>
<span data-ttu-id="faf5b-172">Subnetid VNet especifica o identificador de sub-rede da VNet.</span><span class="sxs-lookup"><span data-stu-id="faf5b-172">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="faf5b-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faf5b-173">-ResourceGroupName</span></span>
<span data-ttu-id="faf5b-174">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="faf5b-174">Resource Group Name.</span></span>

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

### <span data-ttu-id="faf5b-175">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="faf5b-175">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="faf5b-176">A ID do cliente e o segredo do cliente associado à entidade de serviço/aplicativo AAD.</span><span class="sxs-lookup"><span data-stu-id="faf5b-176">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="faf5b-177">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="faf5b-177">-SshKeyValue</span></span>
<span data-ttu-id="faf5b-178">Chave do arquivo de chave SSH ou caminho do arquivo de chave.</span><span class="sxs-lookup"><span data-stu-id="faf5b-178">SSH key file value or key file path.</span></span>
<span data-ttu-id="faf5b-179">O padrão é {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="faf5b-179">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="faf5b-180">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="faf5b-180">-SubnetName</span></span>
<span data-ttu-id="faf5b-181">Nome da sub-rede do VirtualNode addon.</span><span class="sxs-lookup"><span data-stu-id="faf5b-181">Subnet name of VirtualNode addon.</span></span>

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

### <span data-ttu-id="faf5b-182">-Marca</span><span class="sxs-lookup"><span data-stu-id="faf5b-182">-Tag</span></span>
<span data-ttu-id="faf5b-183">Marcas a serem aplicadas ao recurso</span><span class="sxs-lookup"><span data-stu-id="faf5b-183">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="faf5b-184">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="faf5b-184">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="faf5b-185">O nome de usuário do administrador a ser usado para VMs do Windows.</span><span class="sxs-lookup"><span data-stu-id="faf5b-185">The administrator username to use for Windows VMs.</span></span>

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

### <span data-ttu-id="faf5b-186">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="faf5b-186">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="faf5b-187">A senha de administrador para usar para VMs do Windows, o seu comprimento deve ter pelo menos 12, contendo pelo menos um caractere minúsculo, ou seja `[a-z]` , um `[A-Z]` caractere especial e um caractere especial `[!@#$%^&_()]` .</span><span class="sxs-lookup"><span data-stu-id="faf5b-187">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&_()]`.</span></span>

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

### <span data-ttu-id="faf5b-188">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="faf5b-188">-WorkspaceResourceId</span></span>
<span data-ttu-id="faf5b-189">ID do recurso do espaço de trabalho de complemento de monitoração.</span><span class="sxs-lookup"><span data-stu-id="faf5b-189">Resource Id of the workspace of Monitoring addon.</span></span>

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

### <span data-ttu-id="faf5b-190">-Confirme</span><span class="sxs-lookup"><span data-stu-id="faf5b-190">-Confirm</span></span>
<span data-ttu-id="faf5b-191">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faf5b-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faf5b-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faf5b-192">-WhatIf</span></span>
<span data-ttu-id="faf5b-193">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="faf5b-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faf5b-194">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="faf5b-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faf5b-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faf5b-195">CommonParameters</span></span>
<span data-ttu-id="faf5b-196">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faf5b-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faf5b-197">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="faf5b-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faf5b-198">SENSORES</span><span class="sxs-lookup"><span data-stu-id="faf5b-198">INPUTS</span></span>

### <span data-ttu-id="faf5b-199">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="faf5b-199">None</span></span>

## <span data-ttu-id="faf5b-200">EXIBE</span><span class="sxs-lookup"><span data-stu-id="faf5b-200">OUTPUTS</span></span>

### <span data-ttu-id="faf5b-201">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="faf5b-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="faf5b-202">INFORMA</span><span class="sxs-lookup"><span data-stu-id="faf5b-202">NOTES</span></span>

## <span data-ttu-id="faf5b-203">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="faf5b-203">RELATED LINKS</span></span>
