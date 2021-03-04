---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 40ac27339faf2915ccc88c3bbd5f0a39581af743
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885829"
---
# <span data-ttu-id="bdc3a-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="bdc3a-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="bdc3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdc3a-102">SYNOPSIS</span></span>
<span data-ttu-id="bdc3a-103">Atualize a camada de durabilidade ou vmSku de um tipo de nó no cluster.</span><span class="sxs-lookup"><span data-stu-id="bdc3a-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="bdc3a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bdc3a-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdc3a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bdc3a-105">DESCRIPTION</span></span>
<span data-ttu-id="bdc3a-106">Use **Update-AzServiceFabricDurability** para atualizar a durabilidade ou a SKU do cluster.</span><span class="sxs-lookup"><span data-stu-id="bdc3a-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="bdc3a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bdc3a-107">EXAMPLES</span></span>

### <span data-ttu-id="bdc3a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bdc3a-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="bdc3a-109">Este comando altera a camada de durabilidade do NodeType 'nt1' para silver.</span><span class="sxs-lookup"><span data-stu-id="bdc3a-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="bdc3a-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bdc3a-110">PARAMETERS</span></span>

### <span data-ttu-id="bdc3a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdc3a-111">-DefaultProfile</span></span>
<span data-ttu-id="bdc3a-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="bdc3a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdc3a-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="bdc3a-113">-DurabilityLevel</span></span>
<span data-ttu-id="bdc3a-114">Especifique o nível de durabilidade.</span><span class="sxs-lookup"><span data-stu-id="bdc3a-114">Specify durability level.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: Bronze, Silver, Gold

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdc3a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="bdc3a-115">-Name</span></span>
<span data-ttu-id="bdc3a-116">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="bdc3a-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="bdc3a-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="bdc3a-117">-NodeType</span></span>
<span data-ttu-id="bdc3a-118">Especifique o nome do tipo de nó do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="bdc3a-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="bdc3a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdc3a-119">-ResourceGroupName</span></span>
<span data-ttu-id="bdc3a-120">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bdc3a-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bdc3a-121">-Sku</span><span class="sxs-lookup"><span data-stu-id="bdc3a-121">-Sku</span></span>
<span data-ttu-id="bdc3a-122">Especifique o SKU do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="bdc3a-122">Specify the SKU of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdc3a-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bdc3a-123">-Confirm</span></span>
<span data-ttu-id="bdc3a-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdc3a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdc3a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdc3a-125">-WhatIf</span></span>
<span data-ttu-id="bdc3a-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bdc3a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bdc3a-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bdc3a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdc3a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdc3a-128">CommonParameters</span></span>
<span data-ttu-id="bdc3a-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdc3a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdc3a-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdc3a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdc3a-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bdc3a-131">INPUTS</span></span>

### <span data-ttu-id="bdc3a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="bdc3a-132">System.String</span></span>

### <span data-ttu-id="bdc3a-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="bdc3a-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="bdc3a-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bdc3a-134">OUTPUTS</span></span>

### <span data-ttu-id="bdc3a-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="bdc3a-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="bdc3a-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="bdc3a-136">NOTES</span></span>

## <span data-ttu-id="bdc3a-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bdc3a-137">RELATED LINKS</span></span>
