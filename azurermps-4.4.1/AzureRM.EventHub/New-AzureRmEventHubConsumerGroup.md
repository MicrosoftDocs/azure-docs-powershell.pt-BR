---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bcd20fc9c6f0c08af2ae735558a6fccc6c9814d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610797"
---
# <span data-ttu-id="2044a-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="2044a-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="2044a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2044a-102">SYNOPSIS</span></span>
<span data-ttu-id="2044a-103">Cria um novo grupo de consumidores para o Hub de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="2044a-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2044a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2044a-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [[-UserMetadata] <String>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="2044a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2044a-105">DESCRIPTION</span></span>
<span data-ttu-id="2044a-106">O cmdlet New-AzureRmEventHubConsumerGroup cria um novo grupo de consumidores para o Hub de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="2044a-106">The New-AzureRmEventHubConsumerGroup cmdlet creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="2044a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2044a-107">EXAMPLES</span></span>

### <span data-ttu-id="2044a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2044a-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="2044a-109">Cria o grupo \` MyConsumerGroupName \` no Hub de eventos \` MyEventHubName \` , cujo escopo é o namespace \` mynamespacename \` , com MyResourceGroupName de grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="2044a-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="2044a-110">OS</span><span class="sxs-lookup"><span data-stu-id="2044a-110">PARAMETERS</span></span>

### <span data-ttu-id="2044a-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2044a-111">-ResourceGroupName</span></span>
<span data-ttu-id="2044a-112">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2044a-112">Resource group name.</span></span>

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

### <span data-ttu-id="2044a-113">-Metadata usermetadata</span><span class="sxs-lookup"><span data-stu-id="2044a-113">-UserMetadata</span></span>
<span data-ttu-id="2044a-114">Metadados do usuário para o grupo de consumidores.</span><span class="sxs-lookup"><span data-stu-id="2044a-114">User metadata for the consumer group.</span></span>

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

### <span data-ttu-id="2044a-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2044a-115">-Confirm</span></span>
<span data-ttu-id="2044a-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2044a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2044a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2044a-117">-WhatIf</span></span>
<span data-ttu-id="2044a-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2044a-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2044a-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2044a-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2044a-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="2044a-120">-EventHub</span></span>
<span data-ttu-id="2044a-121">Nome do EventHub.</span><span class="sxs-lookup"><span data-stu-id="2044a-121">EventHub Name.</span></span>

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

### <span data-ttu-id="2044a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="2044a-122">-Name</span></span>
<span data-ttu-id="2044a-123">Nome do consumível.</span><span class="sxs-lookup"><span data-stu-id="2044a-123">ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="2044a-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2044a-124">-Namespace</span></span>
<span data-ttu-id="2044a-125">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="2044a-125">Namespace Name.</span></span>

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

## <span data-ttu-id="2044a-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2044a-126">INPUTS</span></span>

### <span data-ttu-id="2044a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2044a-127">System.String</span></span>

## <span data-ttu-id="2044a-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2044a-128">OUTPUTS</span></span>

### <span data-ttu-id="2044a-129">Microsoft. Azure. Commands. EventHub. Models. ConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="2044a-129">Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes</span></span>

## <span data-ttu-id="2044a-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2044a-130">NOTES</span></span>

## <span data-ttu-id="2044a-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2044a-131">RELATED LINKS</span></span>

