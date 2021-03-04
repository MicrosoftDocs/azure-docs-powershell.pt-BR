---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: ba5400a35939a221b19ba144b35b0f2a53f6dbe9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892331"
---
# <span data-ttu-id="e3623-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="e3623-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="e3623-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3623-102">SYNOPSIS</span></span>
<span data-ttu-id="e3623-103">Remova nós do tipo de nó específico de um cluster.</span><span class="sxs-lookup"><span data-stu-id="e3623-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="e3623-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e3623-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3623-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e3623-105">DESCRIPTION</span></span>
<span data-ttu-id="e3623-106">Use **Remove-AzServiceFabricNode** para remover nós de um tipo de nó específico de um cluster.</span><span class="sxs-lookup"><span data-stu-id="e3623-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="e3623-107">A remoção só prosseguirá se atender às métricas de saúde do cluster.</span><span class="sxs-lookup"><span data-stu-id="e3623-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="e3623-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3623-108">EXAMPLES</span></span>

### <span data-ttu-id="e3623-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e3623-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="e3623-110">Este comando removerá 2 nós do NodeType 'nt1'.</span><span class="sxs-lookup"><span data-stu-id="e3623-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="e3623-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e3623-111">PARAMETERS</span></span>

### <span data-ttu-id="e3623-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3623-112">-DefaultProfile</span></span>
<span data-ttu-id="e3623-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3623-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3623-114">-Name</span><span class="sxs-lookup"><span data-stu-id="e3623-114">-Name</span></span>
<span data-ttu-id="e3623-115">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="e3623-115">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3623-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="e3623-116">-NodeType</span></span>
<span data-ttu-id="e3623-117">Nome do tipo de nó</span><span class="sxs-lookup"><span data-stu-id="e3623-117">Node type name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3623-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="e3623-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="e3623-119">O número de nós a adicionar</span><span class="sxs-lookup"><span data-stu-id="e3623-119">The number of nodes to add</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Number

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3623-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3623-120">-ResourceGroupName</span></span>
<span data-ttu-id="e3623-121">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e3623-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e3623-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3623-122">-Confirm</span></span>
<span data-ttu-id="e3623-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3623-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3623-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3623-124">-WhatIf</span></span>
<span data-ttu-id="e3623-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e3623-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3623-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e3623-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3623-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3623-127">CommonParameters</span></span>
<span data-ttu-id="e3623-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3623-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3623-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3623-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3623-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3623-130">INPUTS</span></span>

### <span data-ttu-id="e3623-131">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e3623-131">System.Int32</span></span>

### <span data-ttu-id="e3623-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e3623-132">System.String</span></span>

## <span data-ttu-id="e3623-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e3623-133">OUTPUTS</span></span>

### <span data-ttu-id="e3623-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="e3623-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="e3623-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="e3623-135">NOTES</span></span>

## <span data-ttu-id="e3623-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3623-136">RELATED LINKS</span></span>

[<span data-ttu-id="e3623-137">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="e3623-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md)
