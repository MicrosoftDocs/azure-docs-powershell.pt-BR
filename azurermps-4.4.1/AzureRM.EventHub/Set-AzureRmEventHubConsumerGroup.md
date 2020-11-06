---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: c871036c6f3113bd40e17fb5bbc201fa6297573c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433132"
---
# <span data-ttu-id="0372b-101">Set-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="0372b-101">Set-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="0372b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0372b-102">SYNOPSIS</span></span>
<span data-ttu-id="0372b-103">Atualiza o grupo de consumidores dos hubs de eventos especificados.</span><span class="sxs-lookup"><span data-stu-id="0372b-103">Updates the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0372b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0372b-104">SYNTAX</span></span>

```
Set-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [[-UserMetadata] <String>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="0372b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0372b-105">DESCRIPTION</span></span>
<span data-ttu-id="0372b-106">O cmdlet Set-AzureRmEventHubConsumerGroup atualiza o grupo de consumidores dos hubs de eventos especificados.</span><span class="sxs-lookup"><span data-stu-id="0372b-106">The Set-AzureRmEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="0372b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0372b-107">EXAMPLES</span></span>

### <span data-ttu-id="0372b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0372b-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="0372b-109">Define os metadados do usuário do grupo de consumidores \` MyConsumerGroupName \` para "Testing".</span><span class="sxs-lookup"><span data-stu-id="0372b-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="0372b-110">OS</span><span class="sxs-lookup"><span data-stu-id="0372b-110">PARAMETERS</span></span>

### <span data-ttu-id="0372b-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0372b-111">-ResourceGroupName</span></span>
<span data-ttu-id="0372b-112">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0372b-112">Resource group name.</span></span>

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

### <span data-ttu-id="0372b-113">-Metadata usermetadata</span><span class="sxs-lookup"><span data-stu-id="0372b-113">-UserMetadata</span></span>
<span data-ttu-id="0372b-114">Metadados do usuário para o grupo de consumidores (opcional).</span><span class="sxs-lookup"><span data-stu-id="0372b-114">User metadata for the consumer group (optional).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0372b-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0372b-115">-Confirm</span></span>
<span data-ttu-id="0372b-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0372b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0372b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0372b-117">-WhatIf</span></span>
<span data-ttu-id="0372b-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0372b-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0372b-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0372b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0372b-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="0372b-120">-EventHub</span></span>
<span data-ttu-id="0372b-121">Nome do EventHub.</span><span class="sxs-lookup"><span data-stu-id="0372b-121">EventHub Name.</span></span>

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

### <span data-ttu-id="0372b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="0372b-122">-Name</span></span>
<span data-ttu-id="0372b-123">Nome do consumível.</span><span class="sxs-lookup"><span data-stu-id="0372b-123">ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="0372b-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0372b-124">-Namespace</span></span>
<span data-ttu-id="0372b-125">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="0372b-125">Namespace Name.</span></span>

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

## <span data-ttu-id="0372b-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0372b-126">INPUTS</span></span>

### <span data-ttu-id="0372b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="0372b-127">System.String</span></span>

## <span data-ttu-id="0372b-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0372b-128">OUTPUTS</span></span>

### <span data-ttu-id="0372b-129">Microsoft. Azure. Commands. EventHub. Models. ConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="0372b-129">Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes</span></span>

## <span data-ttu-id="0372b-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0372b-130">NOTES</span></span>

## <span data-ttu-id="0372b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0372b-131">RELATED LINKS</span></span>

