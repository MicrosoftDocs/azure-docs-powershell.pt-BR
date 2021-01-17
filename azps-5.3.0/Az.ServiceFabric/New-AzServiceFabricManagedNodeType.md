---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 3e89e807acfb2507834686574931011bf398c76c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433042"
---
# <span data-ttu-id="6d615-101">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="6d615-101">New-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="6d615-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d615-102">SYNOPSIS</span></span>
<span data-ttu-id="6d615-103">Criar novo recurso de tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="6d615-103">Create new node type resource.</span></span>

## <span data-ttu-id="6d615-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d615-104">SYNTAX</span></span>

```
New-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -InstanceCount <Int32> [-Primary] [-DiskSize <Int32>] [-ApplicationStartPort <Int32>]
 [-ApplicationEndPort <Int32>] [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-VmSize <String>]
 [-VmImagePublisher <String>] [-VmImageOffer <String>] [-VmImageSku <String>] [-VmImageVersion <String>]
 [-Capacity <Hashtable>] [-PlacementProperty <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d615-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d615-105">DESCRIPTION</span></span>
<span data-ttu-id="6d615-106">Criar novo recurso de tipo de nó para um cluster específico.</span><span class="sxs-lookup"><span data-stu-id="6d615-106">Create new node type resource for an specific cluster.</span></span>

## <span data-ttu-id="6d615-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d615-107">EXAMPLES</span></span>

### <span data-ttu-id="6d615-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6d615-108">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -Primary -InstanceCount 3
```

<span data-ttu-id="6d615-109">Crie o tipo de nó principal com 3 nós.</span><span class="sxs-lookup"><span data-stu-id="6d615-109">Create primary node type with 3 nodes.</span></span>

### <span data-ttu-id="6d615-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6d615-110">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -InstanceCount 5 -Primary -PlacementProperty @{NodeColor="Green";SomeProperty="5";} -Capacity @{ClientConnections="65536";} -ApplicationStartPort 20575 -ApplicationEndPort 20605 -EphemeralStartPort 20606 -EphemeralEndPort 20861
```

<span data-ttu-id="6d615-111">Crie o tipo de nó principal com 5 nós e especifique propriedades de posicionamento, capacidades, aplicativos e portas efêmeras.</span><span class="sxs-lookup"><span data-stu-id="6d615-111">Create primary node type with 5 nodes and specifying placement properties, capacities, application and ephemeral ports.</span></span>

## <span data-ttu-id="6d615-112">OS</span><span class="sxs-lookup"><span data-stu-id="6d615-112">PARAMETERS</span></span>

### <span data-ttu-id="6d615-113">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="6d615-113">-ApplicationEndPort</span></span>
<span data-ttu-id="6d615-114">Porta final do aplicativo de um intervalo de portas.</span><span class="sxs-lookup"><span data-stu-id="6d615-114">Application End port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d615-115">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="6d615-115">-ApplicationStartPort</span></span>
<span data-ttu-id="6d615-116">Porta inicial do aplicativo de um intervalo de portas.</span><span class="sxs-lookup"><span data-stu-id="6d615-116">Application start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d615-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d615-117">-AsJob</span></span>
<span data-ttu-id="6d615-118">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="6d615-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6d615-119">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="6d615-119">-Capacity</span></span>
<span data-ttu-id="6d615-120">As marcas de capacidade são aplicadas aos nós no tipo de nó como pares chave/valor, o Gerenciador de recursos de cluster usa essas marcas para entender a quantidade de recursos que um nó tem.</span><span class="sxs-lookup"><span data-stu-id="6d615-120">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span>
<span data-ttu-id="6d615-121">Atualizar, isso substituirá os valores atuais.</span><span class="sxs-lookup"><span data-stu-id="6d615-121">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="6d615-122">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6d615-122">-ClusterName</span></span>
<span data-ttu-id="6d615-123">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="6d615-123">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d615-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d615-124">-DefaultProfile</span></span>
<span data-ttu-id="6d615-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d615-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d615-126">-Disco de</span><span class="sxs-lookup"><span data-stu-id="6d615-126">-DiskSize</span></span>
<span data-ttu-id="6d615-127">Tamanho do disco para cada VM no tipo de nó em GBs.</span><span class="sxs-lookup"><span data-stu-id="6d615-127">Disk size for each vm in the node type in GBs.</span></span>
<span data-ttu-id="6d615-128">100 padrão.</span><span class="sxs-lookup"><span data-stu-id="6d615-128">Default 100.</span></span>

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

### <span data-ttu-id="6d615-129">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="6d615-129">-EphemeralEndPort</span></span>
<span data-ttu-id="6d615-130">Porta final efêmera de um intervalo de portas.</span><span class="sxs-lookup"><span data-stu-id="6d615-130">Ephemeral end port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d615-131">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="6d615-131">-EphemeralStartPort</span></span>
<span data-ttu-id="6d615-132">Porta inicial efêmera de um intervalo de portas.</span><span class="sxs-lookup"><span data-stu-id="6d615-132">Ephemeral start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d615-133">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="6d615-133">-InstanceCount</span></span>
<span data-ttu-id="6d615-134">O número de nós no tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="6d615-134">The number of nodes in the node type.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d615-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d615-135">-Name</span></span>
<span data-ttu-id="6d615-136">Especifique o nome do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="6d615-136">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeTypeName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d615-137">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="6d615-137">-PlacementProperty</span></span>
<span data-ttu-id="6d615-138">Marcas de posicionamento aplicadas a nós no tipo de nó como pares chave/valor, que podem ser usados para indicar onde determinados serviços (carga de trabalho) devem ser executados.</span><span class="sxs-lookup"><span data-stu-id="6d615-138">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span>
<span data-ttu-id="6d615-139">Atualizar, isso substituirá os valores atuais.</span><span class="sxs-lookup"><span data-stu-id="6d615-139">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="6d615-140">-Principal</span><span class="sxs-lookup"><span data-stu-id="6d615-140">-Primary</span></span>
<span data-ttu-id="6d615-141">Especifique se o tipo de nó é primário.</span><span class="sxs-lookup"><span data-stu-id="6d615-141">Specify if the node type is primary.</span></span>
<span data-ttu-id="6d615-142">Nesse tipo de nó, executará serviços do sistema.</span><span class="sxs-lookup"><span data-stu-id="6d615-142">On this node type will run system services.</span></span>
<span data-ttu-id="6d615-143">Somente um tipo de nó deve ser marcado como principal.</span><span class="sxs-lookup"><span data-stu-id="6d615-143">Only one node type should be marked as primary.</span></span>
<span data-ttu-id="6d615-144">O tipo de nó primário não pode ser excluído ou alterado para clusters existentes.</span><span class="sxs-lookup"><span data-stu-id="6d615-144">Primary node type cannot be deleted or changed for existing clusters.</span></span>

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

### <span data-ttu-id="6d615-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d615-145">-ResourceGroupName</span></span>
<span data-ttu-id="6d615-146">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6d615-146">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d615-147">-VmImageOffer</span><span class="sxs-lookup"><span data-stu-id="6d615-147">-VmImageOffer</span></span>
<span data-ttu-id="6d615-148">O tipo de oferta da imagem do Marketplace de máquinas virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d615-148">The offer type of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="6d615-149">Padrão: WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="6d615-149">Default: WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "WindowsServer"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d615-150">-VmImagePublisher</span><span class="sxs-lookup"><span data-stu-id="6d615-150">-VmImagePublisher</span></span>
<span data-ttu-id="6d615-151">O fornecedor da imagem do Marketplace de máquinas virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d615-151">The publisher of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="6d615-152">Padrão: MicrosoftWindowsServer.</span><span class="sxs-lookup"><span data-stu-id="6d615-152">Default: MicrosoftWindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "MicrosoftWindowsServer"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d615-153">-VmImageSku</span><span class="sxs-lookup"><span data-stu-id="6d615-153">-VmImageSku</span></span>
<span data-ttu-id="6d615-154">A SKU da imagem do Marketplace de máquinas virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d615-154">The SKU of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="6d615-155">Padrão: 2019-datacenter.</span><span class="sxs-lookup"><span data-stu-id="6d615-155">Default: 2019-Datacenter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "2019-Datacenter"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d615-156">-VmImageVersion</span><span class="sxs-lookup"><span data-stu-id="6d615-156">-VmImageVersion</span></span>
<span data-ttu-id="6d615-157">A versão da imagem do Marketplace de máquinas virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d615-157">The version of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="6d615-158">Padrão: mais recente.</span><span class="sxs-lookup"><span data-stu-id="6d615-158">Default: latest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "latest"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d615-159">-VmSize</span><span class="sxs-lookup"><span data-stu-id="6d615-159">-VmSize</span></span>
<span data-ttu-id="6d615-160">O tamanho das máquinas virtuais no pool.</span><span class="sxs-lookup"><span data-stu-id="6d615-160">The size of virtual machines in the pool.</span></span>
<span data-ttu-id="6d615-161">Todas as máquinas virtuais em um pool são do mesmo tamanho.</span><span class="sxs-lookup"><span data-stu-id="6d615-161">All virtual machines in a pool are the same size.</span></span>
<span data-ttu-id="6d615-162">Padrão: Standard_D2.</span><span class="sxs-lookup"><span data-stu-id="6d615-162">Default: Standard_D2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "Standard_D2"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d615-163">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6d615-163">-Confirm</span></span>
<span data-ttu-id="6d615-164">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d615-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d615-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d615-165">-WhatIf</span></span>
<span data-ttu-id="6d615-166">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6d615-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d615-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6d615-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d615-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d615-168">CommonParameters</span></span>
<span data-ttu-id="6d615-169">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d615-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d615-170">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d615-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d615-171">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d615-171">INPUTS</span></span>

### <span data-ttu-id="6d615-172">System. String</span><span class="sxs-lookup"><span data-stu-id="6d615-172">System.String</span></span>

## <span data-ttu-id="6d615-173">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d615-173">OUTPUTS</span></span>

### <span data-ttu-id="6d615-174">Microsoft. Azure. Commands. imfabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="6d615-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="6d615-175">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d615-175">NOTES</span></span>

## <span data-ttu-id="6d615-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d615-176">RELATED LINKS</span></span>
