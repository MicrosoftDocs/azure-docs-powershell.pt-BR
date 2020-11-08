---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: b0d22b0cb017c40dc0d1b0328f540b7774ca991b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113304"
---
# <span data-ttu-id="737a4-101">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="737a4-101">Set-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="737a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="737a4-102">SYNOPSIS</span></span>
<span data-ttu-id="737a4-103">Define as propriedades de recurso do tipo de nó ou executar ações de reimagem em NDES específicas do tipo de nó com o parâmetro-reimage.</span><span class="sxs-lookup"><span data-stu-id="737a4-103">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

## <span data-ttu-id="737a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="737a4-104">SYNTAX</span></span>

### <span data-ttu-id="737a4-105">ByObj (padrão)</span><span class="sxs-lookup"><span data-stu-id="737a4-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="737a4-106">WithParamsByName</span><span class="sxs-lookup"><span data-stu-id="737a4-106">WithParamsByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-AsJob] [-InstanceCount <Int32>] [-ApplicationStartPort <Int32>] [-ApplicationEndPort <Int32>]
 [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-Capacity <Hashtable>]
 [-PlacementProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="737a4-107">ReimageByName</span><span class="sxs-lookup"><span data-stu-id="737a4-107">ReimageByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-Reimage] [-ForceReimage] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="737a4-108">WithParamsById</span><span class="sxs-lookup"><span data-stu-id="737a4-108">WithParamsById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="737a4-109">ReimageById</span><span class="sxs-lookup"><span data-stu-id="737a4-109">ReimageById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-Reimage] [-ForceReimage]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="737a4-110">ReimageByObj</span><span class="sxs-lookup"><span data-stu-id="737a4-110">ReimageByObj</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]> [-Reimage]
 [-ForceReimage] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="737a4-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="737a4-111">DESCRIPTION</span></span>
<span data-ttu-id="737a4-112">Define as propriedades de recurso do tipo de nó ou executar ações de reimagem em NDES específicas do tipo de nó com o parâmetro-reimage.</span><span class="sxs-lookup"><span data-stu-id="737a4-112">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span> <span data-ttu-id="737a4-113">Na operação reimgae, os nós do Service Fabric serão desabilitados antes de fazer a nova geração de imagens das VMs e habilitá-las novamente depois que elas forem retornadas.</span><span class="sxs-lookup"><span data-stu-id="737a4-113">On reimgae operation the service fabric nodes will be disabled before reimaging the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="737a4-114">Se isso for feito nos tipos de nós primários, pode demorar um pouco, pois ele pode não renovar todos os nós ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="737a4-114">If this is done on primary node types it might take a while as it might not reimage all the nodes at the same time.</span></span> <span data-ttu-id="737a4-115">Use-ForceReimage force a operação mesmo que o Service Fabric não consiga desabilitar os nós, mas use com cuidado, pois isso pode causar perda de dados se cargas de trabalho com estado estiverem em execução no nó.</span><span class="sxs-lookup"><span data-stu-id="737a4-115">Use -ForceReimage force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="737a4-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="737a4-116">EXAMPLES</span></span>

### <span data-ttu-id="737a4-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="737a4-117">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -InstanceCount 6 -Verbose
```

<span data-ttu-id="737a4-118">Atualize a contagem de instâncias do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="737a4-118">Update the instance count of the node type.</span></span>

### <span data-ttu-id="737a4-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="737a4-119">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -PlacementProperty @{NodeColor="Red";SomeProperty="6";} -Verbose
```

<span data-ttu-id="737a4-120">Atualize o properites de posicionamento do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="737a4-120">Update placement properites of the node type.</span></span> <span data-ttu-id="737a4-121">Isso substituirá o posicionamento mais antigo properites, se houver.</span><span class="sxs-lookup"><span data-stu-id="737a4-121">This will overwrite older placement properites if any.</span></span>

### <span data-ttu-id="737a4-122">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="737a4-122">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -Reimage -NodeName nt1_0, nt1_3
```

<span data-ttu-id="737a4-123">Reimagem do nó 0 e 3 no tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="737a4-123">Reimage node 0 and 3 on the node type.</span></span>

### <span data-ttu-id="737a4-124">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="737a4-124">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType.VmInstanceCount = 6
$nodeType | Set-AzServiceFabricManagedNodeType
```

<span data-ttu-id="737a4-125">Atualize a contagem de instâncias do tipo de nó com tubulação.</span><span class="sxs-lookup"><span data-stu-id="737a4-125">Update the instance count of the node type, with piping.</span></span>

## <span data-ttu-id="737a4-126">OS</span><span class="sxs-lookup"><span data-stu-id="737a4-126">PARAMETERS</span></span>

### <span data-ttu-id="737a4-127">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="737a4-127">-ApplicationEndPort</span></span>
<span data-ttu-id="737a4-128">Porta final do aplicativo de um intervalo de portas.</span><span class="sxs-lookup"><span data-stu-id="737a4-128">Application End port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737a4-129">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="737a4-129">-ApplicationStartPort</span></span>
<span data-ttu-id="737a4-130">Porta inicial do aplicativo de um intervalo de portas.</span><span class="sxs-lookup"><span data-stu-id="737a4-130">Application start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737a4-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="737a4-131">-AsJob</span></span>
<span data-ttu-id="737a4-132">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="737a4-132">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="737a4-133">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="737a4-133">-Capacity</span></span>
<span data-ttu-id="737a4-134">As marcas de capacidade são aplicadas aos nós no tipo de nó como pares chave/valor, o Gerenciador de recursos de cluster usa essas marcas para entender a quantidade de recursos que um nó tem.</span><span class="sxs-lookup"><span data-stu-id="737a4-134">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span> <span data-ttu-id="737a4-135">Atualizar, isso substituirá os valores atuais.</span><span class="sxs-lookup"><span data-stu-id="737a4-135">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737a4-136">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="737a4-136">-ClusterName</span></span>
<span data-ttu-id="737a4-137">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="737a4-137">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="737a4-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="737a4-138">-DefaultProfile</span></span>
<span data-ttu-id="737a4-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="737a4-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="737a4-140">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="737a4-140">-EphemeralEndPort</span></span>
<span data-ttu-id="737a4-141">Porta final efêmera de um intervalo de portas.</span><span class="sxs-lookup"><span data-stu-id="737a4-141">Ephemeral end port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737a4-142">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="737a4-142">-EphemeralStartPort</span></span>
<span data-ttu-id="737a4-143">Porta inicial efêmera de um intervalo de portas.</span><span class="sxs-lookup"><span data-stu-id="737a4-143">Ephemeral start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737a4-144">-ForceReimage</span><span class="sxs-lookup"><span data-stu-id="737a4-144">-ForceReimage</span></span>
<span data-ttu-id="737a4-145">Usar esse sinalizador forçará a remoção mesmo que o Service Fabric não consiga desabilitar os nós.</span><span class="sxs-lookup"><span data-stu-id="737a4-145">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="737a4-146">Use com cuidado, pois isso pode causar perda de dados se cargas de trabalho com estado estiverem em execução no nó.</span><span class="sxs-lookup"><span data-stu-id="737a4-146">Use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737a4-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="737a4-147">-InputObject</span></span>
<span data-ttu-id="737a4-148">Recurso de tipo de nó</span><span class="sxs-lookup"><span data-stu-id="737a4-148">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj, ReimageByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="737a4-149">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="737a4-149">-InstanceCount</span></span>
<span data-ttu-id="737a4-150">O número de nós no tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="737a4-150">The number of nodes in the node type.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737a4-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="737a4-151">-Name</span></span>
<span data-ttu-id="737a4-152">Especifique o nome do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="737a4-152">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="737a4-153">-NodeName</span><span class="sxs-lookup"><span data-stu-id="737a4-153">-NodeName</span></span>
<span data-ttu-id="737a4-154">Lista de nomes de nó para a operação.</span><span class="sxs-lookup"><span data-stu-id="737a4-154">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737a4-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="737a4-155">-PassThru</span></span>
<span data-ttu-id="737a4-156">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="737a4-156">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737a4-157">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="737a4-157">-PlacementProperty</span></span>
<span data-ttu-id="737a4-158">Marcas de posicionamento aplicadas a nós no tipo de nó como pares chave/valor, que podem ser usados para indicar onde determinados serviços (carga de trabalho) devem ser executados.</span><span class="sxs-lookup"><span data-stu-id="737a4-158">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span> <span data-ttu-id="737a4-159">Atualizar, isso substituirá os valores atuais.</span><span class="sxs-lookup"><span data-stu-id="737a4-159">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737a4-160">-Nova imagem</span><span class="sxs-lookup"><span data-stu-id="737a4-160">-Reimage</span></span>
<span data-ttu-id="737a4-161">Especifique para refazer a imagem dos nós no tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="737a4-161">Specify to reimage nodes on the node type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737a4-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="737a4-162">-ResourceGroupName</span></span>
<span data-ttu-id="737a4-163">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="737a4-163">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="737a4-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="737a4-164">-ResourceId</span></span>
<span data-ttu-id="737a4-165">ID do recurso do tipo de nó</span><span class="sxs-lookup"><span data-stu-id="737a4-165">Node type resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsById, ReimageById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="737a4-166">-Confirme</span><span class="sxs-lookup"><span data-stu-id="737a4-166">-Confirm</span></span>
<span data-ttu-id="737a4-167">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="737a4-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="737a4-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="737a4-168">-WhatIf</span></span>
<span data-ttu-id="737a4-169">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="737a4-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="737a4-170">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="737a4-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="737a4-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="737a4-171">CommonParameters</span></span>
<span data-ttu-id="737a4-172">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="737a4-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="737a4-173">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="737a4-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="737a4-174">SENSORES</span><span class="sxs-lookup"><span data-stu-id="737a4-174">INPUTS</span></span>

### <span data-ttu-id="737a4-175">System. String</span><span class="sxs-lookup"><span data-stu-id="737a4-175">System.String</span></span>

## <span data-ttu-id="737a4-176">EXIBE</span><span class="sxs-lookup"><span data-stu-id="737a4-176">OUTPUTS</span></span>

### <span data-ttu-id="737a4-177">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="737a4-177">System.Boolean</span></span>

## <span data-ttu-id="737a4-178">INFORMA</span><span class="sxs-lookup"><span data-stu-id="737a4-178">NOTES</span></span>

## <span data-ttu-id="737a4-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="737a4-179">RELATED LINKS</span></span>
