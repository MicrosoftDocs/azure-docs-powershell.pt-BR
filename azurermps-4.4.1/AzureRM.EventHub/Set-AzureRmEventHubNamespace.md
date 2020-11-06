---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/6911f050bfba3248a3fd992fbc2645e3a1a8641d
ms.openlocfilehash: 05f0c3cd3947a1955689a7359b40d59052863ce1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427933"
---
# <span data-ttu-id="23d9f-101">Set-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="23d9f-101">Set-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="23d9f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23d9f-102">SYNOPSIS</span></span>
<span data-ttu-id="23d9f-103">Atualiza o namespace de hubs de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="23d9f-103">Updates the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23d9f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23d9f-104">SYNTAX</span></span>

### <span data-ttu-id="23d9f-105">NamespaceParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="23d9f-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="23d9f-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="23d9f-106">AutoInflateParameterSet</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="23d9f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23d9f-107">DESCRIPTION</span></span>
<span data-ttu-id="23d9f-108">O cmdlet Set-AzureRmEventHubNamespace atualiza as propriedades do namespace de hubs de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="23d9f-108">The Set-AzureRmEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="23d9f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23d9f-109">EXAMPLES</span></span>

### <span data-ttu-id="23d9f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="23d9f-110">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="23d9f-111">Atualiza o estado do namespace \` Mynamespacename \` a ser criado.</span><span class="sxs-lookup"><span data-stu-id="23d9f-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="23d9f-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="23d9f-112">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="23d9f-113">Atualiza o estado do namespace \` Mynamespacename \` com autoinflate = Enabled e MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="23d9f-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="23d9f-114">OS</span><span class="sxs-lookup"><span data-stu-id="23d9f-114">PARAMETERS</span></span>

### <span data-ttu-id="23d9f-115">-Local</span><span class="sxs-lookup"><span data-stu-id="23d9f-115">-Location</span></span>
<span data-ttu-id="23d9f-116">Localização geográfica do namespace dos hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="23d9f-116">Event Hubs namespace geo-location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d9f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23d9f-117">-ResourceGroupName</span></span>
<span data-ttu-id="23d9f-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="23d9f-118">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d9f-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="23d9f-119">-SkuCapacity</span></span>
<span data-ttu-id="23d9f-120">As unidades de produtividade do hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="23d9f-120">The Event Hub throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d9f-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="23d9f-121">-SkuName</span></span>
<span data-ttu-id="23d9f-122">Nome SKU do namespace.</span><span class="sxs-lookup"><span data-stu-id="23d9f-122">Namespace Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d9f-123">-Estado</span><span class="sxs-lookup"><span data-stu-id="23d9f-123">-State</span></span>
<span data-ttu-id="23d9f-124">Especifica o estado (desabilitado ou habilitado) do namespace.</span><span class="sxs-lookup"><span data-stu-id="23d9f-124">Specifies the state (disabled or enabled) of the namespace.</span></span>

```yaml
Type: NamespaceState
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, Creating, Created, Activating, Enabling, Active, Disabling, Disabled, SoftDeleting, SoftDeleted, Removing, Removed, Failed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d9f-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="23d9f-125">-Tag</span></span>
<span data-ttu-id="23d9f-126">Hashtables que representam marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="23d9f-126">Hashtables that represent resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d9f-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="23d9f-127">-Confirm</span></span>
<span data-ttu-id="23d9f-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23d9f-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d9f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23d9f-129">-WhatIf</span></span>
<span data-ttu-id="23d9f-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="23d9f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23d9f-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="23d9f-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d9f-132">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="23d9f-132">-EnableAutoInflate</span></span>
<span data-ttu-id="23d9f-133">Indica se o autoinflar está habilitado</span><span class="sxs-lookup"><span data-stu-id="23d9f-133">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: NamespaceParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d9f-134">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="23d9f-134">-MaximumThroughputUnits</span></span>
<span data-ttu-id="23d9f-135">Limite superior de unidades de produtividade quando o autoinflar está habilitado, o vaule deve estar dentro de 0 a 20 unidades de produtividade.</span><span class="sxs-lookup"><span data-stu-id="23d9f-135">Upper limit of throughput units when AutoInflate is enabled, vaule should be within 0 to 20 throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d9f-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="23d9f-136">-Name</span></span>
<span data-ttu-id="23d9f-137">Nome do namespace do EventHub.</span><span class="sxs-lookup"><span data-stu-id="23d9f-137">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="23d9f-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23d9f-138">INPUTS</span></span>

### <span data-ttu-id="23d9f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="23d9f-139">System.String</span></span>

### <span data-ttu-id="23d9f-140">System. Int32</span><span class="sxs-lookup"><span data-stu-id="23d9f-140">System.Int32</span></span>

### <span data-ttu-id="23d9f-141">Microsoft. Azure. Management. EventHub. Models. Namespacestate</span><span class="sxs-lookup"><span data-stu-id="23d9f-141">Microsoft.Azure.Management.EventHub.Models.NamespaceState</span></span>

### <span data-ttu-id="23d9f-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="23d9f-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="23d9f-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23d9f-143">OUTPUTS</span></span>

### <span data-ttu-id="23d9f-144">Microsoft. Azure. Commands. EventHub. Models. Namespaceattributes</span><span class="sxs-lookup"><span data-stu-id="23d9f-144">Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="23d9f-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23d9f-145">NOTES</span></span>

## <span data-ttu-id="23d9f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23d9f-146">RELATED LINKS</span></span>

