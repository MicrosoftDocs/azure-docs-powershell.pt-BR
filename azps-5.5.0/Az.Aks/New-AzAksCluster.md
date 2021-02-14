---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: c0eeaedfc98f8225b097345908638d52bb4ed297
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116679"
---
# <span data-ttu-id="0a46c-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="0a46c-101">New-AzAksCluster</span></span>

## <span data-ttu-id="0a46c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a46c-102">SYNOPSIS</span></span>
<span data-ttu-id="0a46c-103">Crie um novo cluster gerenciado Desernetes.</span><span class="sxs-lookup"><span data-stu-id="0a46c-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="0a46c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a46c-104">SYNTAX</span></span>

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

## <span data-ttu-id="0a46c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a46c-105">DESCRIPTION</span></span>

<span data-ttu-id="0a46c-106">Crie um novo cluster de Azure Queernetes Service(AKS).</span><span class="sxs-lookup"><span data-stu-id="0a46c-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="0a46c-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0a46c-107">EXAMPLES</span></span>

### <span data-ttu-id="0a46c-108">Novo AKS com params padrão.</span><span class="sxs-lookup"><span data-stu-id="0a46c-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="0a46c-109">Criar contêiner do Windows Server em um AKS.</span><span class="sxs-lookup"><span data-stu-id="0a46c-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="0a46c-110">Para criar um contêiner do Windows Server em um AKS, você deve especificar pelo menos quatro parâmetros a seguir ao criar as AKS e o valor para e deve ser `NetworkPlugin` `NodeVmSetType` e `azure` `VirtualMachineScaleSets` respectivamente.</span><span class="sxs-lookup"><span data-stu-id="0a46c-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword *** -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="0a46c-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a46c-111">PARAMETERS</span></span>

### <span data-ttu-id="0a46c-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="0a46c-112">-AcrNameToAttach</span></span>
<span data-ttu-id="0a46c-113">Conceda a função "acrpull" do ACR especificado à Entidade de Serviços AKS, por exemplo, myacr</span><span class="sxs-lookup"><span data-stu-id="0a46c-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

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

### <span data-ttu-id="0a46c-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="0a46c-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="0a46c-115">Nomes de complemento a serem habilitados quando o cluster é criado.</span><span class="sxs-lookup"><span data-stu-id="0a46c-115">Add-on names to be enabled when cluster is created.</span></span>

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

### <span data-ttu-id="0a46c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a46c-116">-AsJob</span></span>
<span data-ttu-id="0a46c-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0a46c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a46c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a46c-118">-DefaultProfile</span></span>
<span data-ttu-id="0a46c-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0a46c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a46c-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="0a46c-120">-DnsNamePrefix</span></span>
<span data-ttu-id="0a46c-121">O prefixo de nome DNS do cluster.</span><span class="sxs-lookup"><span data-stu-id="0a46c-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="0a46c-122">O comprimento deve ser <= 9 se os usuários planejam adicionar contêiner do Windows.</span><span class="sxs-lookup"><span data-stu-id="0a46c-122">The length must be <= 9 if users plan to add windows container.</span></span>

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

### <span data-ttu-id="0a46c-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="0a46c-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="0a46c-124">Se você quer habilitar o dimensionador automático</span><span class="sxs-lookup"><span data-stu-id="0a46c-124">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="0a46c-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="0a46c-125">-EnableRbac</span></span>
<span data-ttu-id="0a46c-126">Se você quer habilitar o Recurso Role-Based Access</span><span class="sxs-lookup"><span data-stu-id="0a46c-126">Whether to enable Kubernetes Role-Based Access</span></span>

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

### <span data-ttu-id="0a46c-127">-Forçar</span><span class="sxs-lookup"><span data-stu-id="0a46c-127">-Force</span></span>
<span data-ttu-id="0a46c-128">Criar cluster mesmo que ele já exista</span><span class="sxs-lookup"><span data-stu-id="0a46c-128">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="0a46c-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="0a46c-129">-GenerateSshKey</span></span>
<span data-ttu-id="0a46c-130">Gere o arquivo de chave SSH para {HOME}/.ssh/id_rsa.</span><span class="sxs-lookup"><span data-stu-id="0a46c-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

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

### <span data-ttu-id="0a46c-131">-LtdernetesVersion</span><span class="sxs-lookup"><span data-stu-id="0a46c-131">-KubernetesVersion</span></span>
<span data-ttu-id="0a46c-132">A versão do Queernetes a ser usada para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="0a46c-132">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="0a46c-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="0a46c-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="0a46c-134">Nome de usuário para as Máquinas Virtuais do Linux.</span><span class="sxs-lookup"><span data-stu-id="0a46c-134">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="0a46c-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="0a46c-135">-LoadBalancerSku</span></span>
<span data-ttu-id="0a46c-136">A SKU do balanceador de carga para o cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="0a46c-136">The load balancer sku for the managed cluster.</span></span>

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

### <span data-ttu-id="0a46c-137">-Local</span><span class="sxs-lookup"><span data-stu-id="0a46c-137">-Location</span></span>
<span data-ttu-id="0a46c-138">Local do Azure para o cluster.</span><span class="sxs-lookup"><span data-stu-id="0a46c-138">Azure location for the cluster.</span></span>
<span data-ttu-id="0a46c-139">Padrões para o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0a46c-139">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="0a46c-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a46c-140">-Name</span></span>
<span data-ttu-id="0a46c-141">Nome de cluster gerenciado da Rede Desavenda.</span><span class="sxs-lookup"><span data-stu-id="0a46c-141">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="0a46c-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="0a46c-142">-NetworkPlugin</span></span>
<span data-ttu-id="0a46c-143">Plug-in de rede usado para a criação de rede Desernetes.</span><span class="sxs-lookup"><span data-stu-id="0a46c-143">Network plugin used for building Kubernetes network.</span></span>

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

### <span data-ttu-id="0a46c-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="0a46c-144">-NodeCount</span></span>
<span data-ttu-id="0a46c-145">O número padrão de nós para os pools de nó.</span><span class="sxs-lookup"><span data-stu-id="0a46c-145">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="0a46c-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="0a46c-146">-NodeMaxCount</span></span>
<span data-ttu-id="0a46c-147">Número máximo de nós para dimensionamento automático</span><span class="sxs-lookup"><span data-stu-id="0a46c-147">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="0a46c-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="0a46c-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="0a46c-149">Número máximo de vagens que podem ser executados no nó.</span><span class="sxs-lookup"><span data-stu-id="0a46c-149">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="0a46c-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="0a46c-150">-NodeMinCount</span></span>
<span data-ttu-id="0a46c-151">Número mínimo de nós para dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="0a46c-151">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="0a46c-152">-NodeName</span><span class="sxs-lookup"><span data-stu-id="0a46c-152">-NodeName</span></span>
<span data-ttu-id="0a46c-153">Nome exclusivo do perfil de pool do agente no contexto da assinatura e do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0a46c-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="0a46c-154">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="0a46c-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="0a46c-155">Tamanho em GB do disco do sistema operacional para cada nó no pool de nó.</span><span class="sxs-lookup"><span data-stu-id="0a46c-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="0a46c-156">Mínimo de 30 GB.</span><span class="sxs-lookup"><span data-stu-id="0a46c-156">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="0a46c-157">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="0a46c-157">-NodePoolMode</span></span>
<span data-ttu-id="0a46c-158">NodePoolMode representa o modo de um pool de nó.</span><span class="sxs-lookup"><span data-stu-id="0a46c-158">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="0a46c-159">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="0a46c-159">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="0a46c-160">ScaleSetEvictionPolicy a ser usado para especificar a política de desagregação para conjunto de escala de máquina virtual de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="0a46c-160">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="0a46c-161">Padrão para Excluir.</span><span class="sxs-lookup"><span data-stu-id="0a46c-161">Default to Delete.</span></span>

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

### <span data-ttu-id="0a46c-162">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="0a46c-162">-NodeSetPriority</span></span>
<span data-ttu-id="0a46c-163">ScaleSetPriority a ser usado para especificar a prioridade de conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0a46c-163">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="0a46c-164">Padrão para regular.</span><span class="sxs-lookup"><span data-stu-id="0a46c-164">Default to regular.</span></span>

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

### <span data-ttu-id="0a46c-165">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="0a46c-165">-NodeVmSetType</span></span>
<span data-ttu-id="0a46c-166">AgentPoolType representa os tipos de um pool de agentes.</span><span class="sxs-lookup"><span data-stu-id="0a46c-166">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="0a46c-167">Os valores possíveis incluem: 'VirtualMachineScaleSets', 'AvailabilitySet'</span><span class="sxs-lookup"><span data-stu-id="0a46c-167">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="0a46c-168">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="0a46c-168">-NodeVmSize</span></span>
<span data-ttu-id="0a46c-169">O tamanho da Máquina Virtual.</span><span class="sxs-lookup"><span data-stu-id="0a46c-169">The size of the Virtual Machine.</span></span> <span data-ttu-id="0a46c-170">O valor padrão é Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="0a46c-170">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="0a46c-171">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="0a46c-171">-NodeVnetSubnetID</span></span>
<span data-ttu-id="0a46c-172">O VNet SubnetID especifica o identificador de sub-rede do VNet.</span><span class="sxs-lookup"><span data-stu-id="0a46c-172">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="0a46c-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a46c-173">-ResourceGroupName</span></span>
<span data-ttu-id="0a46c-174">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0a46c-174">Resource Group Name.</span></span>

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

### <span data-ttu-id="0a46c-175">-ServicePrincipalIdAndSecsecsec</span><span class="sxs-lookup"><span data-stu-id="0a46c-175">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="0a46c-176">A ID do cliente e o segredo do cliente associados à entidade de serviço/aplicativo do AAD.</span><span class="sxs-lookup"><span data-stu-id="0a46c-176">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="0a46c-177">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="0a46c-177">-SshKeyValue</span></span>
<span data-ttu-id="0a46c-178">O valor de arquivo da chave SSH ou o caminho do arquivo-chave.</span><span class="sxs-lookup"><span data-stu-id="0a46c-178">SSH key file value or key file path.</span></span>
<span data-ttu-id="0a46c-179">Padrões para {HOME}/.ssh/id_rsa.pub.</span><span class="sxs-lookup"><span data-stu-id="0a46c-179">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="0a46c-180">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="0a46c-180">-SubnetName</span></span>
<span data-ttu-id="0a46c-181">Nome da sub-rede do complemento VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="0a46c-181">Subnet name of VirtualNode addon.</span></span>

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

### <span data-ttu-id="0a46c-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="0a46c-182">-Tag</span></span>
<span data-ttu-id="0a46c-183">Marcas a serem aplicadas ao recurso</span><span class="sxs-lookup"><span data-stu-id="0a46c-183">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="0a46c-184">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="0a46c-184">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="0a46c-185">O nome de usuário do administrador a ser usado para VMs do Windows.</span><span class="sxs-lookup"><span data-stu-id="0a46c-185">The administrator username to use for Windows VMs.</span></span>

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

### <span data-ttu-id="0a46c-186">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="0a46c-186">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="0a46c-187">A senha de administrador a ser usada para VMs do Windows, seu comprimento deve ser de pelo menos 12, contendo pelo menos um caractere de caso inferior, ou seja, um e um `[a-z]` `[A-Z]` caractere `[!@#$%^&*()]` especial.</span><span class="sxs-lookup"><span data-stu-id="0a46c-187">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&*()]`.</span></span>

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

### <span data-ttu-id="0a46c-188">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="0a46c-188">-WorkspaceResourceId</span></span>
<span data-ttu-id="0a46c-189">ID do recurso do espaço de trabalho do complemento Monitoramento.</span><span class="sxs-lookup"><span data-stu-id="0a46c-189">Resource Id of the workspace of Monitoring addon.</span></span>

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

### <span data-ttu-id="0a46c-190">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0a46c-190">-Confirm</span></span>
<span data-ttu-id="0a46c-191">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a46c-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a46c-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a46c-192">-WhatIf</span></span>
<span data-ttu-id="0a46c-193">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0a46c-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a46c-194">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0a46c-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a46c-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a46c-195">CommonParameters</span></span>
<span data-ttu-id="0a46c-196">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a46c-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a46c-197">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a46c-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a46c-198">Entradas</span><span class="sxs-lookup"><span data-stu-id="0a46c-198">INPUTS</span></span>

### <span data-ttu-id="0a46c-199">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0a46c-199">None</span></span>

## <span data-ttu-id="0a46c-200">Saídas</span><span class="sxs-lookup"><span data-stu-id="0a46c-200">OUTPUTS</span></span>

### <span data-ttu-id="0a46c-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="0a46c-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="0a46c-202">Notas</span><span class="sxs-lookup"><span data-stu-id="0a46c-202">NOTES</span></span>

## <span data-ttu-id="0a46c-203">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a46c-203">RELATED LINKS</span></span>
