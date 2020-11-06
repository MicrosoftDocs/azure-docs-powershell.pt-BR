---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: c8684e9af0bca55dca52f336a458f4c428ca67a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432224"
---
# <span data-ttu-id="39293-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="39293-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="39293-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="39293-102">SYNOPSIS</span></span>
<span data-ttu-id="39293-103">Exclui o grupo de consumidores dos hubs de eventos especificados.</span><span class="sxs-lookup"><span data-stu-id="39293-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39293-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39293-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="39293-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="39293-105">DESCRIPTION</span></span>
<span data-ttu-id="39293-106">O cmdlet Remove-AzureRmEventHubConsumerGroup remove e exclui o grupo consumidor especificado do hub de eventos fornecido.</span><span class="sxs-lookup"><span data-stu-id="39293-106">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="39293-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="39293-107">EXAMPLES</span></span>

### <span data-ttu-id="39293-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="39293-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="39293-109">Exclui o \` MyConsumerGroupName do grupo \` do consumidor do MyEventHubName do hub de eventos \` \` , escopo do \` namespace mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="39293-109">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

## <span data-ttu-id="39293-110">OS</span><span class="sxs-lookup"><span data-stu-id="39293-110">PARAMETERS</span></span>

### <span data-ttu-id="39293-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39293-111">-ResourceGroupName</span></span>
<span data-ttu-id="39293-112">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="39293-112">Resource group name.</span></span>

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

### <span data-ttu-id="39293-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="39293-113">-Confirm</span></span>
<span data-ttu-id="39293-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39293-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39293-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39293-115">-WhatIf</span></span>
<span data-ttu-id="39293-116">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="39293-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39293-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="39293-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39293-118">-EventHub</span><span class="sxs-lookup"><span data-stu-id="39293-118">-EventHub</span></span>
<span data-ttu-id="39293-119">Nome do EventHub.</span><span class="sxs-lookup"><span data-stu-id="39293-119">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39293-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="39293-120">-Name</span></span>
<span data-ttu-id="39293-121">Nome do consumível.</span><span class="sxs-lookup"><span data-stu-id="39293-121">ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39293-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="39293-122">-Namespace</span></span>
<span data-ttu-id="39293-123">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="39293-123">Namespace Name.</span></span>

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

## <span data-ttu-id="39293-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="39293-124">INPUTS</span></span>

### <span data-ttu-id="39293-125">System. String</span><span class="sxs-lookup"><span data-stu-id="39293-125">System.String</span></span>

## <span data-ttu-id="39293-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="39293-126">OUTPUTS</span></span>

### <span data-ttu-id="39293-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="39293-127">System.Object</span></span>

## <span data-ttu-id="39293-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="39293-128">NOTES</span></span>

## <span data-ttu-id="39293-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="39293-129">RELATED LINKS</span></span>

