---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
ms.openlocfilehash: 39cd0759f18c84f78a2e6a75f8e1c9b257fb9da9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610713"
---
# <span data-ttu-id="360c9-101">New-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="360c9-101">New-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="360c9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="360c9-102">SYNOPSIS</span></span>
<span data-ttu-id="360c9-103">Cria uma nova regra para uma determinada assinatura de tópico.</span><span class="sxs-lookup"><span data-stu-id="360c9-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="360c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="360c9-104">SYNTAX</span></span>

```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="360c9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="360c9-105">DESCRIPTION</span></span>
<span data-ttu-id="360c9-106">O cmdlet **New-AzureRmServiceBusRule** cria uma nova regra para a assinatura determinada.</span><span class="sxs-lookup"><span data-stu-id="360c9-106">The **New-AzureRmServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="360c9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="360c9-107">EXAMPLES</span></span>

### <span data-ttu-id="360c9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="360c9-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="360c9-109">O cmdlet **New-AzureRmServiceBusRule** cria uma nova regra para a assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="360c9-109">The **New-AzureRmServiceBusRule** cmdlet creates a new rule for the specified Subscription.</span></span>

## <span data-ttu-id="360c9-110">OS</span><span class="sxs-lookup"><span data-stu-id="360c9-110">PARAMETERS</span></span>

### <span data-ttu-id="360c9-111">-Confirme</span><span class="sxs-lookup"><span data-stu-id="360c9-111">-Confirm</span></span>
<span data-ttu-id="360c9-112">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="360c9-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="360c9-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="360c9-113">-Name</span></span>
<span data-ttu-id="360c9-114">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="360c9-114">Rule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="360c9-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="360c9-115">-Namespace</span></span>
<span data-ttu-id="360c9-116">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="360c9-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="360c9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="360c9-117">-ResourceGroupName</span></span>
<span data-ttu-id="360c9-118">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="360c9-118">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="360c9-119">-Sqlexpression</span><span class="sxs-lookup"><span data-stu-id="360c9-119">-SqlExpression</span></span>
<span data-ttu-id="360c9-120">Expressão filtrar SQL</span><span class="sxs-lookup"><span data-stu-id="360c9-120">Sql Fillter Expression</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="360c9-121">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="360c9-121">-Subscription</span></span>
<span data-ttu-id="360c9-122">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="360c9-122">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="360c9-123">-Tópico</span><span class="sxs-lookup"><span data-stu-id="360c9-123">-Topic</span></span>
<span data-ttu-id="360c9-124">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="360c9-124">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="360c9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="360c9-125">-WhatIf</span></span>
<span data-ttu-id="360c9-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="360c9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="360c9-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="360c9-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="360c9-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="360c9-128">INPUTS</span></span>

### <span data-ttu-id="360c9-129">System. String</span><span class="sxs-lookup"><span data-stu-id="360c9-129">System.String</span></span>


## <span data-ttu-id="360c9-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="360c9-130">OUTPUTS</span></span>

### <span data-ttu-id="360c9-131">Microsoft. Azure. Commands. ServiceBus. Models. Rules</span><span class="sxs-lookup"><span data-stu-id="360c9-131">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>


## <span data-ttu-id="360c9-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="360c9-132">NOTES</span></span>

## <span data-ttu-id="360c9-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="360c9-133">RELATED LINKS</span></span>

