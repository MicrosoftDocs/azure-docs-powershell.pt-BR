---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 5f5509da60351216a5ea004eae59e551a74e601a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112583"
---
# <span data-ttu-id="0b08e-101">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="0b08e-101">Remove-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="0b08e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b08e-102">SYNOPSIS</span></span>
<span data-ttu-id="0b08e-103">Remova o tipo de nó ou nós específicos dentro do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="0b08e-103">Remove the node type or specific nodes within the node type.</span></span>

## <span data-ttu-id="0b08e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b08e-104">SYNTAX</span></span>

### <span data-ttu-id="0b08e-105">DeleteNodeTypeByObj (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0b08e-105">DeleteNodeTypeByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b08e-106">DeleteNodeTypeByName</span><span class="sxs-lookup"><span data-stu-id="0b08e-106">DeleteNodeTypeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b08e-107">DeleteNodeByName</span><span class="sxs-lookup"><span data-stu-id="0b08e-107">DeleteNodeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b08e-108">DeleteNodeByObj</span><span class="sxs-lookup"><span data-stu-id="0b08e-108">DeleteNodeByObj</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]>
 [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b08e-109">DeleteNodeTypeById</span><span class="sxs-lookup"><span data-stu-id="0b08e-109">DeleteNodeTypeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b08e-110">DeleteNodeById</span><span class="sxs-lookup"><span data-stu-id="0b08e-110">DeleteNodeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-ForceRemoveNode]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b08e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b08e-111">DESCRIPTION</span></span>
<span data-ttu-id="0b08e-112">Remova o tipo de nó ou nós específicos dentro do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="0b08e-112">Remove the node type or specific nodes within the node type.</span></span> <span data-ttu-id="0b08e-113">Se o nome do grupo -NodeName for usado, somente os nós especificados serão removidos.</span><span class="sxs-lookup"><span data-stu-id="0b08e-113">If the paremter -NodeName is used then only nodes specified will be removed.</span></span>

## <span data-ttu-id="0b08e-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0b08e-114">EXAMPLES</span></span>

### <span data-ttu-id="0b08e-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0b08e-115">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName
```

<span data-ttu-id="0b08e-116">Remover tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="0b08e-116">Remove node type.</span></span>

### <span data-ttu-id="0b08e-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0b08e-117">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType
```

<span data-ttu-id="0b08e-118">Remover o tipo de nó, com canos.</span><span class="sxs-lookup"><span data-stu-id="0b08e-118">Remove node type, with piping.</span></span>

### <span data-ttu-id="0b08e-119">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0b08e-119">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="0b08e-120">Remover 2 nós do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="0b08e-120">Remove 2 nodes from the node type.</span></span>

### <span data-ttu-id="0b08e-121">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="0b08e-121">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType -NodeName nt1_0, nt1_3
```

<span data-ttu-id="0b08e-122">Remover 2 nós do tipo de nó, com canos.</span><span class="sxs-lookup"><span data-stu-id="0b08e-122">Remove 2 nodes from the node type, with piping.</span></span>

## <span data-ttu-id="0b08e-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b08e-123">PARAMETERS</span></span>

### <span data-ttu-id="0b08e-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b08e-124">-AsJob</span></span>
<span data-ttu-id="0b08e-125">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o andamento.</span><span class="sxs-lookup"><span data-stu-id="0b08e-125">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0b08e-126">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0b08e-126">-ClusterName</span></span>
<span data-ttu-id="0b08e-127">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="0b08e-127">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b08e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b08e-128">-DefaultProfile</span></span>
<span data-ttu-id="0b08e-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b08e-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b08e-130">-ForceRemoveNode</span><span class="sxs-lookup"><span data-stu-id="0b08e-130">-ForceRemoveNode</span></span>
<span data-ttu-id="0b08e-131">Usar esse sinalizador forçará a remoção mesmo que a malha de serviço não consiga desabilitar os nós.</span><span class="sxs-lookup"><span data-stu-id="0b08e-131">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="0b08e-132">Use com cuidado, pois isso pode causar perda de dados se cargas de trabalho estado em execução nos nós ou pode trazer o cluster para baixo se não houver nós de seed suficientes após a opearion.</span><span class="sxs-lookup"><span data-stu-id="0b08e-132">Use with caution as this might cause data loss if stateful workloads are running on the nodes, or might bring the cluster down if there are not enough seed nodes after the opearion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DeleteNodeByName, DeleteNodeByObj, DeleteNodeById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b08e-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b08e-133">-InputObject</span></span>
<span data-ttu-id="0b08e-134">Recurso de tipo nó</span><span class="sxs-lookup"><span data-stu-id="0b08e-134">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: DeleteNodeTypeByObj, DeleteNodeByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b08e-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b08e-135">-Name</span></span>
<span data-ttu-id="0b08e-136">Especifique o nome do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="0b08e-136">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b08e-137">-NodeName</span><span class="sxs-lookup"><span data-stu-id="0b08e-137">-NodeName</span></span>
<span data-ttu-id="0b08e-138">Lista de nomes de nó para a operação.</span><span class="sxs-lookup"><span data-stu-id="0b08e-138">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: DeleteNodeByName, DeleteNodeByObj, DeleteNodeById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b08e-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b08e-139">-PassThru</span></span>
<span data-ttu-id="0b08e-140">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="0b08e-140">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="0b08e-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b08e-141">-ResourceGroupName</span></span>
<span data-ttu-id="0b08e-142">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0b08e-142">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b08e-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b08e-143">-ResourceId</span></span>
<span data-ttu-id="0b08e-144">ID do recurso de tipo nó</span><span class="sxs-lookup"><span data-stu-id="0b08e-144">Node type resource id</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeById, DeleteNodeById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b08e-145">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0b08e-145">-Confirm</span></span>
<span data-ttu-id="0b08e-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b08e-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b08e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b08e-147">-WhatIf</span></span>
<span data-ttu-id="0b08e-148">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0b08e-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b08e-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0b08e-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b08e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b08e-150">CommonParameters</span></span>
<span data-ttu-id="0b08e-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b08e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b08e-152">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b08e-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b08e-153">Entradas</span><span class="sxs-lookup"><span data-stu-id="0b08e-153">INPUTS</span></span>

### <span data-ttu-id="0b08e-154">System.String</span><span class="sxs-lookup"><span data-stu-id="0b08e-154">System.String</span></span>

## <span data-ttu-id="0b08e-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="0b08e-155">OUTPUTS</span></span>

### <span data-ttu-id="0b08e-156">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0b08e-156">System.Boolean</span></span>

## <span data-ttu-id="0b08e-157">Notas</span><span class="sxs-lookup"><span data-stu-id="0b08e-157">NOTES</span></span>

## <span data-ttu-id="0b08e-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b08e-158">RELATED LINKS</span></span>
