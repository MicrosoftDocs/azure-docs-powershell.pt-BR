---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/restart-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 8b68175be91b3669c42a67259f5095b567e7905e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892323"
---
# <span data-ttu-id="99866-101">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="99866-101">Restart-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="99866-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99866-102">SYNOPSIS</span></span>
<span data-ttu-id="99866-103">Reinicie nós específicos do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="99866-103">Restart specific nodes from the node type.</span></span>

## <span data-ttu-id="99866-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="99866-104">SYNTAX</span></span>

```
Restart-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRestart] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99866-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="99866-105">DESCRIPTION</span></span>
<span data-ttu-id="99866-106">Reinicie nós específicos do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="99866-106">Restart specific nodes from the node type.</span></span> <span data-ttu-id="99866-107">Ele desabilita os nós de malha de serviço antes de reiniciar as vms e os habilita novamente quando eles voltarem.</span><span class="sxs-lookup"><span data-stu-id="99866-107">It will disabled the service fabric nodes before restarting the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="99866-108">Se isso for feito em tipos de nó primários, pode demorar um pouco, pois pode não reiniciar todos os nós ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="99866-108">If this is done on primary node types it might take a while as it might not restart all the nodes at the same time.</span></span> <span data-ttu-id="99866-109">Use -ForceRestart force a operação, mesmo que a malha de serviço não consiga desabilitar os nós, mas use com cautela, pois isso pode causar perda de dados se cargas de trabalho de estado estão sendo executados no nó.</span><span class="sxs-lookup"><span data-stu-id="99866-109">Use -ForceRestart force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="99866-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99866-110">EXAMPLES</span></span>

### <span data-ttu-id="99866-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="99866-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Restart-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="99866-112">Reinicie o nó 0 e 3 no tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="99866-112">Restart node 0 and 3 on the node type.</span></span>

## <span data-ttu-id="99866-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="99866-113">PARAMETERS</span></span>

### <span data-ttu-id="99866-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99866-114">-AsJob</span></span>
<span data-ttu-id="99866-115">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.</span><span class="sxs-lookup"><span data-stu-id="99866-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="99866-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="99866-116">-ClusterName</span></span>
<span data-ttu-id="99866-117">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="99866-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="99866-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99866-118">-DefaultProfile</span></span>
<span data-ttu-id="99866-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="99866-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99866-120">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="99866-120">-ForceRestart</span></span>
<span data-ttu-id="99866-121">O uso desse sinalizador força o nó a reiniciar, mesmo que a malha de serviço não consiga desabilitar os nós.</span><span class="sxs-lookup"><span data-stu-id="99866-121">Using this flag will force the node to restart even if service fabric is unable to disable the nodes.</span></span>

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

### <span data-ttu-id="99866-122">-Name</span><span class="sxs-lookup"><span data-stu-id="99866-122">-Name</span></span>
<span data-ttu-id="99866-123">Especifique o nome do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="99866-123">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99866-124">-NodeName</span><span class="sxs-lookup"><span data-stu-id="99866-124">-NodeName</span></span>
<span data-ttu-id="99866-125">Lista de nomes de nós para a operação.</span><span class="sxs-lookup"><span data-stu-id="99866-125">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99866-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99866-126">-PassThru</span></span>
<span data-ttu-id="99866-127">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="99866-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="99866-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99866-128">-ResourceGroupName</span></span>
<span data-ttu-id="99866-129">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="99866-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="99866-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99866-130">-Confirm</span></span>
<span data-ttu-id="99866-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99866-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99866-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99866-132">-WhatIf</span></span>
<span data-ttu-id="99866-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="99866-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99866-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="99866-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99866-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99866-135">CommonParameters</span></span>
<span data-ttu-id="99866-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99866-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99866-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99866-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99866-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="99866-138">INPUTS</span></span>

### <span data-ttu-id="99866-139">System.String</span><span class="sxs-lookup"><span data-stu-id="99866-139">System.String</span></span>

## <span data-ttu-id="99866-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="99866-140">OUTPUTS</span></span>

### <span data-ttu-id="99866-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="99866-141">System.Boolean</span></span>

## <span data-ttu-id="99866-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="99866-142">NOTES</span></span>

## <span data-ttu-id="99866-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99866-143">RELATED LINKS</span></span>
