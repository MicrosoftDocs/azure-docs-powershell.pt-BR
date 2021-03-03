---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 1a0da9869ccfdc6b8344240a8367a4c8dfcd2350
ms.sourcegitcommit: 608289d079b819df2b8d1a2f7935cc500367a312
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "101684884"
---
# <span data-ttu-id="15fe5-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="15fe5-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="15fe5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="15fe5-103">Atualize a camada de durabilidade ou vmSku de um tipo de nó no cluster.</span><span class="sxs-lookup"><span data-stu-id="15fe5-103">Update the durability tier or VmSku of a node type in the cluster.</span></span> <span data-ttu-id="15fe5-104">Ele também atualizará a camada de durabilidade na extensão VM do Service Fabric no Conjunto de Escala de Máquina Virtual associado.</span><span class="sxs-lookup"><span data-stu-id="15fe5-104">It will also update the durability tier in the Service Fabric VM extension on the associated Virtual Machine Scale Set.</span></span>

## <span data-ttu-id="15fe5-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="15fe5-105">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15fe5-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="15fe5-106">DESCRIPTION</span></span>
<span data-ttu-id="15fe5-107">Use **Update-AzServiceFabricDurability** para atualizar a durabilidade ou a SKU do cluster.</span><span class="sxs-lookup"><span data-stu-id="15fe5-107">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="15fe5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15fe5-108">EXAMPLES</span></span>

### <span data-ttu-id="15fe5-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="15fe5-109">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="15fe5-110">Este comando altera a camada de durabilidade do NodeType 'nt1' para silver.</span><span class="sxs-lookup"><span data-stu-id="15fe5-110">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="15fe5-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="15fe5-111">PARAMETERS</span></span>

### <span data-ttu-id="15fe5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15fe5-112">-DefaultProfile</span></span>
<span data-ttu-id="15fe5-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="15fe5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15fe5-114">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="15fe5-114">-DurabilityLevel</span></span>
<span data-ttu-id="15fe5-115">Especifique o nível de durabilidade.</span><span class="sxs-lookup"><span data-stu-id="15fe5-115">Specify durability level.</span></span>

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

### <span data-ttu-id="15fe5-116">-Name</span><span class="sxs-lookup"><span data-stu-id="15fe5-116">-Name</span></span>
<span data-ttu-id="15fe5-117">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="15fe5-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="15fe5-118">-NodeType</span><span class="sxs-lookup"><span data-stu-id="15fe5-118">-NodeType</span></span>
<span data-ttu-id="15fe5-119">Especifique o nome do tipo de nó do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="15fe5-119">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="15fe5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15fe5-120">-ResourceGroupName</span></span>
<span data-ttu-id="15fe5-121">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="15fe5-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="15fe5-122">-Sku</span><span class="sxs-lookup"><span data-stu-id="15fe5-122">-Sku</span></span>
<span data-ttu-id="15fe5-123">Especifique o SKU do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="15fe5-123">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="15fe5-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15fe5-124">-Confirm</span></span>
<span data-ttu-id="15fe5-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15fe5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15fe5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15fe5-126">-WhatIf</span></span>
<span data-ttu-id="15fe5-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="15fe5-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15fe5-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="15fe5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15fe5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15fe5-129">CommonParameters</span></span>
<span data-ttu-id="15fe5-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15fe5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15fe5-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15fe5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15fe5-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="15fe5-132">INPUTS</span></span>

### <span data-ttu-id="15fe5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="15fe5-133">System.String</span></span>

### <span data-ttu-id="15fe5-134">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="15fe5-134">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="15fe5-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="15fe5-135">OUTPUTS</span></span>

### <span data-ttu-id="15fe5-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="15fe5-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="15fe5-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="15fe5-137">NOTES</span></span>

## <span data-ttu-id="15fe5-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15fe5-138">RELATED LINKS</span></span>
