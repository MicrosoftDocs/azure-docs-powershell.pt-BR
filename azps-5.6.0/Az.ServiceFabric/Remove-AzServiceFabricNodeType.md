---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: 8d0bd6f046bbff99d93b0ed5dc7385d8ec772811
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892330"
---
# <span data-ttu-id="dd745-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="dd745-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="dd745-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd745-102">SYNOPSIS</span></span>
<span data-ttu-id="dd745-103">Remova um tipo de nó completo de um cluster.</span><span class="sxs-lookup"><span data-stu-id="dd745-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="dd745-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dd745-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd745-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dd745-105">DESCRIPTION</span></span>
<span data-ttu-id="dd745-106">Use o **Remove-AzServiceFabricNodeType** para remover todos os nós de um tipo de nó específico e o tipo de nó de um cluster.</span><span class="sxs-lookup"><span data-stu-id="dd745-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="dd745-107">Esse comando não pode ser usado para excluir o tipo de nó principal.</span><span class="sxs-lookup"><span data-stu-id="dd745-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="dd745-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd745-108">EXAMPLES</span></span>

### <span data-ttu-id="dd745-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dd745-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="dd745-110">Este comando removerá NodeType 'nt1' do cluster.</span><span class="sxs-lookup"><span data-stu-id="dd745-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="dd745-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dd745-111">PARAMETERS</span></span>

### <span data-ttu-id="dd745-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd745-112">-DefaultProfile</span></span>
<span data-ttu-id="dd745-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dd745-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd745-114">-Name</span><span class="sxs-lookup"><span data-stu-id="dd745-114">-Name</span></span>
<span data-ttu-id="dd745-115">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="dd745-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="dd745-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="dd745-116">-NodeType</span></span>
<span data-ttu-id="dd745-117">O nome do tipo de nó</span><span class="sxs-lookup"><span data-stu-id="dd745-117">The node type name</span></span>

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

### <span data-ttu-id="dd745-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd745-118">-ResourceGroupName</span></span>
<span data-ttu-id="dd745-119">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dd745-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="dd745-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd745-120">-Confirm</span></span>
<span data-ttu-id="dd745-121">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd745-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd745-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd745-122">-WhatIf</span></span>
<span data-ttu-id="dd745-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dd745-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd745-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dd745-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd745-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd745-125">CommonParameters</span></span>
<span data-ttu-id="dd745-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd745-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd745-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd745-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd745-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd745-128">INPUTS</span></span>

### <span data-ttu-id="dd745-129">System.String</span><span class="sxs-lookup"><span data-stu-id="dd745-129">System.String</span></span>

## <span data-ttu-id="dd745-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dd745-130">OUTPUTS</span></span>

### <span data-ttu-id="dd745-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="dd745-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="dd745-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="dd745-132">NOTES</span></span>

## <span data-ttu-id="dd745-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd745-133">RELATED LINKS</span></span>
