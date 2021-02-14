---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
ms.openlocfilehash: 77125022002f09233154ba468f22a28228219e04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116677"
---
# <span data-ttu-id="857b9-101">New-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="857b9-101">New-AzAksNodePool</span></span>

## <span data-ttu-id="857b9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="857b9-102">SYNOPSIS</span></span>
<span data-ttu-id="857b9-103">Criar um novo pool de nó no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="857b9-103">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="857b9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="857b9-104">SYNTAX</span></span>

### <span data-ttu-id="857b9-105">defaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="857b9-105">defaultParameterSet</span></span>
```
New-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-Count <Int32>]
 [-OsDiskSize <Int32>] [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="857b9-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="857b9-106">ParentObjectParameterSet</span></span>
```
New-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-Count <Int32>] [-OsDiskSize <Int32>]
 [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="857b9-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="857b9-107">DESCRIPTION</span></span>
<span data-ttu-id="857b9-108">Criar um novo pool de nó no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="857b9-108">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="857b9-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="857b9-109">EXAMPLES</span></span>

### <span data-ttu-id="857b9-110">Criar pool de nó com parâmetros padrão</span><span class="sxs-lookup"><span data-stu-id="857b9-110">Create node pool with default parameters</span></span>
```powershell
PS C:\> New-AzAksNodePool -ResourceGroupName myResouceGroup -ClusterName myCluster -Name mydefault
```

### <span data-ttu-id="857b9-111">Criar contêiner do Windows Server em um AKS</span><span class="sxs-lookup"><span data-stu-id="857b9-111">Create Windows Server container on an AKS</span></span>
```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="857b9-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="857b9-112">PARAMETERS</span></span>

### <span data-ttu-id="857b9-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="857b9-113">-ClusterName</span></span>
<span data-ttu-id="857b9-114">O nome do recurso de cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="857b9-114">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="857b9-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="857b9-115">-ClusterObject</span></span>
<span data-ttu-id="857b9-116">Especifique o objeto de cluster no qual criar pool de nó.</span><span class="sxs-lookup"><span data-stu-id="857b9-116">Specify cluster object in which to create node pool.</span></span>

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

### <span data-ttu-id="857b9-117">-Contagem</span><span class="sxs-lookup"><span data-stu-id="857b9-117">-Count</span></span>
<span data-ttu-id="857b9-118">O número padrão de nós para os pools de nó.</span><span class="sxs-lookup"><span data-stu-id="857b9-118">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="857b9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="857b9-119">-DefaultProfile</span></span>
<span data-ttu-id="857b9-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="857b9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="857b9-121">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="857b9-121">-EnableAutoScaling</span></span>
<span data-ttu-id="857b9-122">Se você quer habilitar o dimensionador automático</span><span class="sxs-lookup"><span data-stu-id="857b9-122">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="857b9-123">-Forçar</span><span class="sxs-lookup"><span data-stu-id="857b9-123">-Force</span></span>
<span data-ttu-id="857b9-124">Criar pool de nó mesmo que ele já exista</span><span class="sxs-lookup"><span data-stu-id="857b9-124">Create node pool even if it already exists</span></span>

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

### <span data-ttu-id="857b9-125">-LtdernetesVersion</span><span class="sxs-lookup"><span data-stu-id="857b9-125">-KubernetesVersion</span></span>
<span data-ttu-id="857b9-126">A versão do Queernetes a ser usada para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="857b9-126">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="857b9-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="857b9-127">-MaxCount</span></span>
<span data-ttu-id="857b9-128">Número máximo de nós para dimensionamento automático</span><span class="sxs-lookup"><span data-stu-id="857b9-128">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="857b9-129">-MaxPodCount</span><span class="sxs-lookup"><span data-stu-id="857b9-129">-MaxPodCount</span></span>
<span data-ttu-id="857b9-130">Número máximo de vagens que podem ser executados no nó.</span><span class="sxs-lookup"><span data-stu-id="857b9-130">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="857b9-131">-MinCount</span><span class="sxs-lookup"><span data-stu-id="857b9-131">-MinCount</span></span>
<span data-ttu-id="857b9-132">Número mínimo de nós para dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="857b9-132">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="857b9-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="857b9-133">-Name</span></span>
<span data-ttu-id="857b9-134">O nome do pool de nó.</span><span class="sxs-lookup"><span data-stu-id="857b9-134">The name of the node pool.</span></span>

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

### <span data-ttu-id="857b9-135">-OsDiskSize</span><span class="sxs-lookup"><span data-stu-id="857b9-135">-OsDiskSize</span></span>
<span data-ttu-id="857b9-136">O número padrão de nós para os pools de nó.</span><span class="sxs-lookup"><span data-stu-id="857b9-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="857b9-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="857b9-137">-OsType</span></span>
<span data-ttu-id="857b9-138">OsType a ser usado para especificar o tipo do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="857b9-138">OsType to be used to specify os type.</span></span>
<span data-ttu-id="857b9-139">Escolha no Linux e no Windows.</span><span class="sxs-lookup"><span data-stu-id="857b9-139">Choose from Linux and Windows.</span></span>
<span data-ttu-id="857b9-140">Padrão para o Linux.</span><span class="sxs-lookup"><span data-stu-id="857b9-140">Default to Linux.</span></span>

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

### <span data-ttu-id="857b9-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="857b9-141">-ResourceGroupName</span></span>
<span data-ttu-id="857b9-142">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="857b9-142">The name of the resource group.</span></span>

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

### <span data-ttu-id="857b9-143">-ScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="857b9-143">-ScaleSetEvictionPolicy</span></span>
<span data-ttu-id="857b9-144">ScaleSetEvictionPolicy a ser usado para especificar a política de desagregação para conjunto de escala de máquina virtual de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="857b9-144">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span>
<span data-ttu-id="857b9-145">Padrão para Excluir.</span><span class="sxs-lookup"><span data-stu-id="857b9-145">Default to Delete.</span></span>

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

### <span data-ttu-id="857b9-146">-ScaleSetPriority</span><span class="sxs-lookup"><span data-stu-id="857b9-146">-ScaleSetPriority</span></span>
<span data-ttu-id="857b9-147">ScaleSetPriority a ser usado para especificar a prioridade de conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="857b9-147">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span>
<span data-ttu-id="857b9-148">Padrão para regular.</span><span class="sxs-lookup"><span data-stu-id="857b9-148">Default to regular.</span></span>

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

### <span data-ttu-id="857b9-149">-VmSetType</span><span class="sxs-lookup"><span data-stu-id="857b9-149">-VmSetType</span></span>
<span data-ttu-id="857b9-150">Representa os tipos de um pool de nó.</span><span class="sxs-lookup"><span data-stu-id="857b9-150">Represents types of an node pool.</span></span>
<span data-ttu-id="857b9-151">Os valores possíveis incluem: 'VirtualMachineScaleSets', 'AvailabilitySet'</span><span class="sxs-lookup"><span data-stu-id="857b9-151">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="857b9-152">-VmSize</span><span class="sxs-lookup"><span data-stu-id="857b9-152">-VmSize</span></span>
<span data-ttu-id="857b9-153">O tamanho da Máquina Virtual.</span><span class="sxs-lookup"><span data-stu-id="857b9-153">The size of the Virtual Machine.</span></span> <span data-ttu-id="857b9-154">O valor padrão é Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="857b9-154">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="857b9-155">-VnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="857b9-155">-VnetSubnetID</span></span>
<span data-ttu-id="857b9-156">O VNet SubnetID especifica o identificador de sub-rede do VNet.</span><span class="sxs-lookup"><span data-stu-id="857b9-156">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="857b9-157">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="857b9-157">-Confirm</span></span>
<span data-ttu-id="857b9-158">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="857b9-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="857b9-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="857b9-159">-WhatIf</span></span>
<span data-ttu-id="857b9-160">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="857b9-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="857b9-161">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="857b9-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="857b9-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="857b9-162">CommonParameters</span></span>
<span data-ttu-id="857b9-163">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="857b9-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="857b9-164">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="857b9-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="857b9-165">Entradas</span><span class="sxs-lookup"><span data-stu-id="857b9-165">INPUTS</span></span>

### <span data-ttu-id="857b9-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="857b9-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="857b9-167">Saídas</span><span class="sxs-lookup"><span data-stu-id="857b9-167">OUTPUTS</span></span>

### <span data-ttu-id="857b9-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="857b9-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="857b9-169">Notas</span><span class="sxs-lookup"><span data-stu-id="857b9-169">NOTES</span></span>

## <span data-ttu-id="857b9-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="857b9-170">RELATED LINKS</span></span>
