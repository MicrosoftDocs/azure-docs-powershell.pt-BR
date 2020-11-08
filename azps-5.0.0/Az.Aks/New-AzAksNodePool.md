---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
ms.openlocfilehash: 77125022002f09233154ba468f22a28228219e04
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117112"
---
# <span data-ttu-id="c4831-101">New-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="c4831-101">New-AzAksNodePool</span></span>

## <span data-ttu-id="c4831-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c4831-102">SYNOPSIS</span></span>
<span data-ttu-id="c4831-103">Crie um novo pool de nós no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="c4831-103">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="c4831-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4831-104">SYNTAX</span></span>

### <span data-ttu-id="c4831-105">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4831-105">defaultParameterSet</span></span>
```
New-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-Count <Int32>]
 [-OsDiskSize <Int32>] [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4831-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4831-106">ParentObjectParameterSet</span></span>
```
New-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-Count <Int32>] [-OsDiskSize <Int32>]
 [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4831-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c4831-107">DESCRIPTION</span></span>
<span data-ttu-id="c4831-108">Crie um novo pool de nós no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="c4831-108">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="c4831-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c4831-109">EXAMPLES</span></span>

### <span data-ttu-id="c4831-110">Criar pool de nós com parâmetros padrão</span><span class="sxs-lookup"><span data-stu-id="c4831-110">Create node pool with default parameters</span></span>
```powershell
PS C:\> New-AzAksNodePool -ResourceGroupName myResouceGroup -ClusterName myCluster -Name mydefault
```

### <span data-ttu-id="c4831-111">Criar contêiner do Windows Server em um AKS</span><span class="sxs-lookup"><span data-stu-id="c4831-111">Create Windows Server container on an AKS</span></span>
```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="c4831-112">OS</span><span class="sxs-lookup"><span data-stu-id="c4831-112">PARAMETERS</span></span>

### <span data-ttu-id="c4831-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c4831-113">-ClusterName</span></span>
<span data-ttu-id="c4831-114">O nome do recurso de cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="c4831-114">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4831-115">-Clusterobject</span><span class="sxs-lookup"><span data-stu-id="c4831-115">-ClusterObject</span></span>
<span data-ttu-id="c4831-116">Especifique o objeto de cluster no qual criar o pool de nós.</span><span class="sxs-lookup"><span data-stu-id="c4831-116">Specify cluster object in which to create node pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4831-117">-Contagem</span><span class="sxs-lookup"><span data-stu-id="c4831-117">-Count</span></span>
<span data-ttu-id="c4831-118">O número padrão de nós para os pools de nós.</span><span class="sxs-lookup"><span data-stu-id="c4831-118">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="c4831-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4831-119">-DefaultProfile</span></span>
<span data-ttu-id="c4831-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c4831-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4831-121">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="c4831-121">-EnableAutoScaling</span></span>
<span data-ttu-id="c4831-122">Se o dimensionador automático deve ser habilitado</span><span class="sxs-lookup"><span data-stu-id="c4831-122">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="c4831-123">-Force</span><span class="sxs-lookup"><span data-stu-id="c4831-123">-Force</span></span>
<span data-ttu-id="c4831-124">Crie um pool de nós mesmo se ele já existir</span><span class="sxs-lookup"><span data-stu-id="c4831-124">Create node pool even if it already exists</span></span>

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

### <span data-ttu-id="c4831-125">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="c4831-125">-KubernetesVersion</span></span>
<span data-ttu-id="c4831-126">A versão do kubernetes a ser usada para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="c4831-126">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="c4831-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c4831-127">-MaxCount</span></span>
<span data-ttu-id="c4831-128">Número máximo de nós para dimensionamento automático</span><span class="sxs-lookup"><span data-stu-id="c4831-128">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="c4831-129">-MaxPodCount</span><span class="sxs-lookup"><span data-stu-id="c4831-129">-MaxPodCount</span></span>
<span data-ttu-id="c4831-130">Número máximo de pods que podem ser executados no nó.</span><span class="sxs-lookup"><span data-stu-id="c4831-130">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="c4831-131">-MinCount</span><span class="sxs-lookup"><span data-stu-id="c4831-131">-MinCount</span></span>
<span data-ttu-id="c4831-132">Número mínimo de nós para dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="c4831-132">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="c4831-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="c4831-133">-Name</span></span>
<span data-ttu-id="c4831-134">O nome do pool de nós.</span><span class="sxs-lookup"><span data-stu-id="c4831-134">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4831-135">-OsDiskSize</span><span class="sxs-lookup"><span data-stu-id="c4831-135">-OsDiskSize</span></span>
<span data-ttu-id="c4831-136">O número padrão de nós para os pools de nós.</span><span class="sxs-lookup"><span data-stu-id="c4831-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="c4831-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="c4831-137">-OsType</span></span>
<span data-ttu-id="c4831-138">OsType a ser usado para especificar o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c4831-138">OsType to be used to specify os type.</span></span>
<span data-ttu-id="c4831-139">Escolha entre Linux e Windows.</span><span class="sxs-lookup"><span data-stu-id="c4831-139">Choose from Linux and Windows.</span></span>
<span data-ttu-id="c4831-140">Padrão para Linux.</span><span class="sxs-lookup"><span data-stu-id="c4831-140">Default to Linux.</span></span>

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

### <span data-ttu-id="c4831-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4831-141">-ResourceGroupName</span></span>
<span data-ttu-id="c4831-142">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c4831-142">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4831-143">-ScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="c4831-143">-ScaleSetEvictionPolicy</span></span>
<span data-ttu-id="c4831-144">ScaleSetEvictionPolicy a ser usado para especificar a política de remoção para conjunto de escala de máquina virtual de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="c4831-144">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span>
<span data-ttu-id="c4831-145">Padrão a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="c4831-145">Default to Delete.</span></span>

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

### <span data-ttu-id="c4831-146">-ScaleSetPriority</span><span class="sxs-lookup"><span data-stu-id="c4831-146">-ScaleSetPriority</span></span>
<span data-ttu-id="c4831-147">ScaleSetPriority a ser usado para especificar a prioridade do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c4831-147">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span>
<span data-ttu-id="c4831-148">O padrão é normal.</span><span class="sxs-lookup"><span data-stu-id="c4831-148">Default to regular.</span></span>

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

### <span data-ttu-id="c4831-149">-VmSetType</span><span class="sxs-lookup"><span data-stu-id="c4831-149">-VmSetType</span></span>
<span data-ttu-id="c4831-150">Representa tipos de um pool de nós.</span><span class="sxs-lookup"><span data-stu-id="c4831-150">Represents types of an node pool.</span></span>
<span data-ttu-id="c4831-151">Os valores possíveis incluem: ' VirtualMachineScaleSets ', ' Availabilityset '</span><span class="sxs-lookup"><span data-stu-id="c4831-151">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="c4831-152">-VmSize</span><span class="sxs-lookup"><span data-stu-id="c4831-152">-VmSize</span></span>
<span data-ttu-id="c4831-153">O tamanho da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c4831-153">The size of the Virtual Machine.</span></span> <span data-ttu-id="c4831-154">O valor padrão é Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="c4831-154">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="c4831-155">-VnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="c4831-155">-VnetSubnetID</span></span>
<span data-ttu-id="c4831-156">Subnetid VNet especifica o identificador de sub-rede da VNet.</span><span class="sxs-lookup"><span data-stu-id="c4831-156">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="c4831-157">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c4831-157">-Confirm</span></span>
<span data-ttu-id="c4831-158">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4831-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4831-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4831-159">-WhatIf</span></span>
<span data-ttu-id="c4831-160">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c4831-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4831-161">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c4831-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4831-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4831-162">CommonParameters</span></span>
<span data-ttu-id="c4831-163">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4831-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4831-164">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4831-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4831-165">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c4831-165">INPUTS</span></span>

### <span data-ttu-id="c4831-166">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="c4831-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="c4831-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c4831-167">OUTPUTS</span></span>

### <span data-ttu-id="c4831-168">Microsoft. Azure. Commands. AKs. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="c4831-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="c4831-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c4831-169">NOTES</span></span>

## <span data-ttu-id="c4831-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4831-170">RELATED LINKS</span></span>
