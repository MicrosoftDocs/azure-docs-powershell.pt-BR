---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 07b5de12e042c81bb5f27c844d1fc8962453310a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610796"
---
# <span data-ttu-id="f9d33-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="f9d33-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="f9d33-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9d33-102">SYNOPSIS</span></span>
<span data-ttu-id="f9d33-103">Cria um namespace de hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="f9d33-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9d33-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9d33-104">SYNTAX</span></span>

### <span data-ttu-id="f9d33-105">NamespaceParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f9d33-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f9d33-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9d33-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-EnableAutoInflate]
 [-MaximumThroughputUnits] <Int32> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f9d33-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f9d33-107">DESCRIPTION</span></span>
<span data-ttu-id="f9d33-108">O cmdlet New-AzureRmEventHubNamespace cria um novo namespace de hubs de eventos de tipo.</span><span class="sxs-lookup"><span data-stu-id="f9d33-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="f9d33-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9d33-109">EXAMPLES</span></span>

### <span data-ttu-id="f9d33-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f9d33-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation 
```

<span data-ttu-id="f9d33-111">Cria um namespace de hubs \` de evento Mynamespacename \` na localização geográfica especificada \` MyLocation \` , na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="f9d33-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="f9d33-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f9d33-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="f9d33-113">Cria um namespace de hubs de evento \` Mynamespacename \` na localização geográfica especificada \` MyLocation \` , no grupo de recursos \` MyResourceGroupName \` e autoinflate são habilitados com MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="f9d33-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

## <span data-ttu-id="f9d33-114">OS</span><span class="sxs-lookup"><span data-stu-id="f9d33-114">PARAMETERS</span></span>

### <span data-ttu-id="f9d33-115">-Local</span><span class="sxs-lookup"><span data-stu-id="f9d33-115">-Location</span></span>
<span data-ttu-id="f9d33-116">Localização geográfica do namespace dos hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="f9d33-116">Event Hubs namespace geo-location.</span></span>

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

### <span data-ttu-id="f9d33-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9d33-117">-ResourceGroupName</span></span>
<span data-ttu-id="f9d33-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f9d33-118">Resource group name.</span></span>

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

### <span data-ttu-id="f9d33-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="f9d33-119">-SkuCapacity</span></span>
<span data-ttu-id="f9d33-120">As unidades de produtividade do hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="f9d33-120">The Event Hub throughput units.</span></span>

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

### <span data-ttu-id="f9d33-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f9d33-121">-SkuName</span></span>
<span data-ttu-id="f9d33-122">Nome SKU do namespace.</span><span class="sxs-lookup"><span data-stu-id="f9d33-122">Namespace Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d33-123">-Marca</span><span class="sxs-lookup"><span data-stu-id="f9d33-123">-Tag</span></span>
<span data-ttu-id="f9d33-124">Hashtables que representam marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="f9d33-124">Hashtables that represent resource tags.</span></span>

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

### <span data-ttu-id="f9d33-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f9d33-125">-Confirm</span></span>
<span data-ttu-id="f9d33-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9d33-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9d33-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9d33-127">-WhatIf</span></span>
<span data-ttu-id="f9d33-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f9d33-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9d33-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f9d33-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9d33-130">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="f9d33-130">-EnableAutoInflate</span></span>
<span data-ttu-id="f9d33-131">Indica se o autoinflar está habilitado</span><span class="sxs-lookup"><span data-stu-id="f9d33-131">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="f9d33-132">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="f9d33-132">-MaximumThroughputUnits</span></span>
<span data-ttu-id="f9d33-133">Limite superior de unidades de produtividade quando o autoinflar está habilitado, o vaule deve estar dentro de 0 a 20 unidades de produtividade.</span><span class="sxs-lookup"><span data-stu-id="f9d33-133">Upper limit of throughput units when AutoInflate is enabled, vaule should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="f9d33-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9d33-134">-Name</span></span>
<span data-ttu-id="f9d33-135">Nome do namespace do EventHub.</span><span class="sxs-lookup"><span data-stu-id="f9d33-135">EventHub Namespace Name.</span></span>

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

## <span data-ttu-id="f9d33-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f9d33-136">INPUTS</span></span>

### <span data-ttu-id="f9d33-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f9d33-137">System.String</span></span>
<span data-ttu-id="f9d33-138">System. Nullable \` 1 \[ \[ System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = B77a5c561934e089 \] \] System. Nullable \` 1 \[ \[ System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089 \] \] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f9d33-138">System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Collections.Hashtable</span></span>

## <span data-ttu-id="f9d33-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f9d33-139">OUTPUTS</span></span>

### <span data-ttu-id="f9d33-140">Microsoft. Azure. Commands. EventHub. Models. Namespaceattributes</span><span class="sxs-lookup"><span data-stu-id="f9d33-140">Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="f9d33-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f9d33-141">NOTES</span></span>

## <span data-ttu-id="f9d33-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9d33-142">RELATED LINKS</span></span>

