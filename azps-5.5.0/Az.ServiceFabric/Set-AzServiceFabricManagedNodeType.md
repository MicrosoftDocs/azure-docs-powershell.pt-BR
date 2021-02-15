---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: b0d22b0cb017c40dc0d1b0328f540b7774ca991b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114502"
---
# <span data-ttu-id="a6406-101">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="a6406-101">Set-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="a6406-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6406-102">SYNOPSIS</span></span>
<span data-ttu-id="a6406-103">Define propriedades de recurso de tipo de nó ou executar ações de reimagem em ndes específicos do tipo de nó com o parâmetro -Reimage.</span><span class="sxs-lookup"><span data-stu-id="a6406-103">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

## <span data-ttu-id="a6406-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6406-104">SYNTAX</span></span>

### <span data-ttu-id="a6406-105">ByObj (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a6406-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6406-106">WithParamsByName</span><span class="sxs-lookup"><span data-stu-id="a6406-106">WithParamsByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-AsJob] [-InstanceCount <Int32>] [-ApplicationStartPort <Int32>] [-ApplicationEndPort <Int32>]
 [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-Capacity <Hashtable>]
 [-PlacementProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6406-107">ReimageByName</span><span class="sxs-lookup"><span data-stu-id="a6406-107">ReimageByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-Reimage] [-ForceReimage] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6406-108">WithParamsById</span><span class="sxs-lookup"><span data-stu-id="a6406-108">WithParamsById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6406-109">ReimageById</span><span class="sxs-lookup"><span data-stu-id="a6406-109">ReimageById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-Reimage] [-ForceReimage]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6406-110">ReimageByObj</span><span class="sxs-lookup"><span data-stu-id="a6406-110">ReimageByObj</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]> [-Reimage]
 [-ForceReimage] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6406-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="a6406-111">DESCRIPTION</span></span>
<span data-ttu-id="a6406-112">Define propriedades de recurso de tipo de nó ou executar ações de reimagem em ndes específicos do tipo de nó com o parâmetro -Reimage.</span><span class="sxs-lookup"><span data-stu-id="a6406-112">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span> <span data-ttu-id="a6406-113">Na operação reimgae, os nós de malha de serviço serão desabilitados antes de reabilitar os vms e voltar a habilita-los novamente quando eles retornarem.</span><span class="sxs-lookup"><span data-stu-id="a6406-113">On reimgae operation the service fabric nodes will be disabled before reimaging the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="a6406-114">Se isso for feito em tipos de nó principal, pode demorar um pouco, pois pode não reimager todos os nós ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="a6406-114">If this is done on primary node types it might take a while as it might not reimage all the nodes at the same time.</span></span> <span data-ttu-id="a6406-115">Use -ForceReimage force a operação mesmo que a malha de serviço não seja capaz de desabilitar os nós, mas use com cuidado, pois isso pode causar perda de dados se cargas de trabalho de estado estão em execução no nó.</span><span class="sxs-lookup"><span data-stu-id="a6406-115">Use -ForceReimage force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="a6406-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a6406-116">EXAMPLES</span></span>

### <span data-ttu-id="a6406-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a6406-117">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -InstanceCount 6 -Verbose
```

<span data-ttu-id="a6406-118">Atualize a contagem de instâncias do tipo nó.</span><span class="sxs-lookup"><span data-stu-id="a6406-118">Update the instance count of the node type.</span></span>

### <span data-ttu-id="a6406-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a6406-119">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -PlacementProperty @{NodeColor="Red";SomeProperty="6";} -Verbose
```

<span data-ttu-id="a6406-120">Atualize os properites de posicionamento do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="a6406-120">Update placement properites of the node type.</span></span> <span data-ttu-id="a6406-121">Isso substituirá os properites de posicionamento mais antigos, se algum.</span><span class="sxs-lookup"><span data-stu-id="a6406-121">This will overwrite older placement properites if any.</span></span>

### <span data-ttu-id="a6406-122">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a6406-122">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -Reimage -NodeName nt1_0, nt1_3
```

<span data-ttu-id="a6406-123">Reimage node 0 and 3 on the node type.</span><span class="sxs-lookup"><span data-stu-id="a6406-123">Reimage node 0 and 3 on the node type.</span></span>

### <span data-ttu-id="a6406-124">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="a6406-124">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType.VmInstanceCount = 6
$nodeType | Set-AzServiceFabricManagedNodeType
```

<span data-ttu-id="a6406-125">Atualize a contagem de instâncias do tipo nó, com canos.</span><span class="sxs-lookup"><span data-stu-id="a6406-125">Update the instance count of the node type, with piping.</span></span>

## <span data-ttu-id="a6406-126">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6406-126">PARAMETERS</span></span>

### <span data-ttu-id="a6406-127">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="a6406-127">-ApplicationEndPort</span></span>
<span data-ttu-id="a6406-128">Porta final do aplicativo de um intervalo de portas.</span><span class="sxs-lookup"><span data-stu-id="a6406-128">Application End port of a range of ports.</span></span>

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

### <span data-ttu-id="a6406-129">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="a6406-129">-ApplicationStartPort</span></span>
<span data-ttu-id="a6406-130">Porta de início de aplicativo de um intervalo de portas.</span><span class="sxs-lookup"><span data-stu-id="a6406-130">Application start port of a range of ports.</span></span>

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

### <span data-ttu-id="a6406-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6406-131">-AsJob</span></span>
<span data-ttu-id="a6406-132">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o andamento.</span><span class="sxs-lookup"><span data-stu-id="a6406-132">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a6406-133">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="a6406-133">-Capacity</span></span>
<span data-ttu-id="a6406-134">Marcas de capacidade aplicadas aos nós no tipo de nó como pares de chave/valor, o gerenciador de recursos de cluster usa essas marcas para entender quanto recurso um nó tem.</span><span class="sxs-lookup"><span data-stu-id="a6406-134">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span> <span data-ttu-id="a6406-135">A atualização substituirá os valores atuais.</span><span class="sxs-lookup"><span data-stu-id="a6406-135">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="a6406-136">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a6406-136">-ClusterName</span></span>
<span data-ttu-id="a6406-137">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="a6406-137">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a6406-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6406-138">-DefaultProfile</span></span>
<span data-ttu-id="a6406-139">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6406-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6406-140">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="a6406-140">-EphemeralEndPort</span></span>
<span data-ttu-id="a6406-141">Porta final efêmera de um intervalo de portas.</span><span class="sxs-lookup"><span data-stu-id="a6406-141">Ephemeral end port of a range of ports.</span></span>

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

### <span data-ttu-id="a6406-142">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="a6406-142">-EphemeralStartPort</span></span>
<span data-ttu-id="a6406-143">Porta inicial efêmera de um intervalo de portas.</span><span class="sxs-lookup"><span data-stu-id="a6406-143">Ephemeral start port of a range of ports.</span></span>

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

### <span data-ttu-id="a6406-144">-ForceReimage</span><span class="sxs-lookup"><span data-stu-id="a6406-144">-ForceReimage</span></span>
<span data-ttu-id="a6406-145">Usar esse sinalizador forçará a remoção mesmo que a malha de serviço não consiga desabilitar os nós.</span><span class="sxs-lookup"><span data-stu-id="a6406-145">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="a6406-146">Use com cuidado, pois isso pode causar perda de dados se cargas de trabalho estado em execução no nó.</span><span class="sxs-lookup"><span data-stu-id="a6406-146">Use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

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

### <span data-ttu-id="a6406-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6406-147">-InputObject</span></span>
<span data-ttu-id="a6406-148">Recurso de tipo nó</span><span class="sxs-lookup"><span data-stu-id="a6406-148">Node type resource</span></span>

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

### <span data-ttu-id="a6406-149">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="a6406-149">-InstanceCount</span></span>
<span data-ttu-id="a6406-150">O número de nós no tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="a6406-150">The number of nodes in the node type.</span></span>

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

### <span data-ttu-id="a6406-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6406-151">-Name</span></span>
<span data-ttu-id="a6406-152">Especifique o nome do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="a6406-152">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="a6406-153">-NodeName</span><span class="sxs-lookup"><span data-stu-id="a6406-153">-NodeName</span></span>
<span data-ttu-id="a6406-154">Lista de nomes de nó para a operação.</span><span class="sxs-lookup"><span data-stu-id="a6406-154">List of node names for the operation.</span></span>

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

### <span data-ttu-id="a6406-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6406-155">-PassThru</span></span>
<span data-ttu-id="a6406-156">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="a6406-156">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="a6406-157">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="a6406-157">-PlacementProperty</span></span>
<span data-ttu-id="a6406-158">Marcas de posicionamento aplicadas aos nós no tipo de nó como pares de chave/valor, que podem ser usados para indicar onde determinados serviços (carga de trabalho) devem ser executados.</span><span class="sxs-lookup"><span data-stu-id="a6406-158">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span> <span data-ttu-id="a6406-159">A atualização substituirá os valores atuais.</span><span class="sxs-lookup"><span data-stu-id="a6406-159">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="a6406-160">-Reimage</span><span class="sxs-lookup"><span data-stu-id="a6406-160">-Reimage</span></span>
<span data-ttu-id="a6406-161">Especifique para reaginar nós no tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="a6406-161">Specify to reimage nodes on the node type.</span></span>

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

### <span data-ttu-id="a6406-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6406-162">-ResourceGroupName</span></span>
<span data-ttu-id="a6406-163">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a6406-163">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a6406-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6406-164">-ResourceId</span></span>
<span data-ttu-id="a6406-165">ID do recurso de tipo nó</span><span class="sxs-lookup"><span data-stu-id="a6406-165">Node type resource id</span></span>

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

### <span data-ttu-id="a6406-166">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a6406-166">-Confirm</span></span>
<span data-ttu-id="a6406-167">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6406-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6406-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6406-168">-WhatIf</span></span>
<span data-ttu-id="a6406-169">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a6406-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6406-170">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a6406-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6406-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6406-171">CommonParameters</span></span>
<span data-ttu-id="a6406-172">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6406-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6406-173">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6406-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6406-174">Entradas</span><span class="sxs-lookup"><span data-stu-id="a6406-174">INPUTS</span></span>

### <span data-ttu-id="a6406-175">System.String</span><span class="sxs-lookup"><span data-stu-id="a6406-175">System.String</span></span>

## <span data-ttu-id="a6406-176">Saídas</span><span class="sxs-lookup"><span data-stu-id="a6406-176">OUTPUTS</span></span>

### <span data-ttu-id="a6406-177">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a6406-177">System.Boolean</span></span>

## <span data-ttu-id="a6406-178">Notas</span><span class="sxs-lookup"><span data-stu-id="a6406-178">NOTES</span></span>

## <span data-ttu-id="a6406-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6406-179">RELATED LINKS</span></span>
