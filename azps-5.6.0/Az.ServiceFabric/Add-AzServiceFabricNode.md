---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
ms.openlocfilehash: 34b55a5da226a3985cb6fe3bede244ee1e054726
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889394"
---
# <span data-ttu-id="0599c-101">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="0599c-101">Add-AzServiceFabricNode</span></span>

## <span data-ttu-id="0599c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0599c-102">SYNOPSIS</span></span>
<span data-ttu-id="0599c-103">Adicione nós ao tipo de nó específico no cluster.</span><span class="sxs-lookup"><span data-stu-id="0599c-103">Add nodes to the specific node type in the cluster.</span></span>

## <span data-ttu-id="0599c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0599c-104">SYNTAX</span></span>

```
Add-AzServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0599c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0599c-105">DESCRIPTION</span></span>
<span data-ttu-id="0599c-106">Use **Add-AzServiceFabricNode** para adicionar nós ao tipo de nó específico.</span><span class="sxs-lookup"><span data-stu-id="0599c-106">Use **Add-AzServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="0599c-107">Você só precisa especificar o número de nós que deseja adicionar a um tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="0599c-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="0599c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0599c-108">EXAMPLES</span></span>

### <span data-ttu-id="0599c-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0599c-109">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="0599c-110">Este comando adicionará 2 nós ao tipo de nó 'n1'.</span><span class="sxs-lookup"><span data-stu-id="0599c-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="0599c-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0599c-111">PARAMETERS</span></span>

### <span data-ttu-id="0599c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0599c-112">-DefaultProfile</span></span>
<span data-ttu-id="0599c-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0599c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0599c-114">-Name</span><span class="sxs-lookup"><span data-stu-id="0599c-114">-Name</span></span>
<span data-ttu-id="0599c-115">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="0599c-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="0599c-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="0599c-116">-NodeType</span></span>
<span data-ttu-id="0599c-117">Nome do tipo de nó</span><span class="sxs-lookup"><span data-stu-id="0599c-117">Node type name</span></span>

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

### <span data-ttu-id="0599c-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="0599c-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="0599c-119">O número de nós a adicionar</span><span class="sxs-lookup"><span data-stu-id="0599c-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="0599c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0599c-120">-ResourceGroupName</span></span>
<span data-ttu-id="0599c-121">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0599c-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="0599c-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0599c-122">-Confirm</span></span>
<span data-ttu-id="0599c-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0599c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0599c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0599c-124">-WhatIf</span></span>
<span data-ttu-id="0599c-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0599c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0599c-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0599c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0599c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0599c-127">CommonParameters</span></span>
<span data-ttu-id="0599c-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0599c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0599c-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0599c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0599c-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0599c-130">INPUTS</span></span>

### <span data-ttu-id="0599c-131">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0599c-131">System.Int32</span></span>

### <span data-ttu-id="0599c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="0599c-132">System.String</span></span>

## <span data-ttu-id="0599c-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0599c-133">OUTPUTS</span></span>

### <span data-ttu-id="0599c-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="0599c-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="0599c-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="0599c-135">NOTES</span></span>

## <span data-ttu-id="0599c-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0599c-136">RELATED LINKS</span></span>

[<span data-ttu-id="0599c-137">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="0599c-137">Remove-AzServiceFabricNode</span></span>](./Remove-AzServiceFabricNode.md)
