---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 4a2608ee3d3f874183a35fe6b81f7cd169123416
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441096"
---
# <span data-ttu-id="cdded-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="cdded-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="cdded-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cdded-102">SYNOPSIS</span></span>
<span data-ttu-id="cdded-103">Obtém os detalhes de um grupo de consumidores de hubs de eventos especificado ou obtém uma lista de grupos de consumidores em um hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="cdded-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdded-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cdded-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 [-Name <String>]
```

## <span data-ttu-id="cdded-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cdded-105">DESCRIPTION</span></span>
<span data-ttu-id="cdded-106">O cmdlet Get-AzureRmEventHubConsumerGroup Obtém os detalhes de um grupo de consumidores de hubs de eventos especificado ou uma lista de grupos de consumidores em um determinado Hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="cdded-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="cdded-107">Se o nome de um grupo de consumidores for fornecido, os detalhes dos detalhes de um único grupo de consumidores serão retornados.</span><span class="sxs-lookup"><span data-stu-id="cdded-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="cdded-108">Se o nome de um grupo de consumidores não for fornecido, uma lista de grupos de consumidores no Hub de eventos especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="cdded-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="cdded-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cdded-109">EXAMPLES</span></span>

### <span data-ttu-id="cdded-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cdded-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="cdded-111">Obtém o grupo do consumidor \` MyConsumerGroupName \` no Hub de eventos \` MyEventHubName \` , que existe no namespace \` mynamespacename \` com o grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="cdded-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="cdded-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cdded-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="cdded-113">Obtém uma lista de grupos de consumidores no Hub de eventos \` MyEventHubName \` , que existe no namespace \` mynamespacename \` com o grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="cdded-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="cdded-114">OS</span><span class="sxs-lookup"><span data-stu-id="cdded-114">PARAMETERS</span></span>

### <span data-ttu-id="cdded-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdded-115">-ResourceGroupName</span></span>
<span data-ttu-id="cdded-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cdded-116">Resource group name.</span></span>

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

### <span data-ttu-id="cdded-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="cdded-117">-EventHub</span></span>
<span data-ttu-id="cdded-118">Nome do EventHub.</span><span class="sxs-lookup"><span data-stu-id="cdded-118">EventHub Name.</span></span>

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

### <span data-ttu-id="cdded-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="cdded-119">-Name</span></span>
<span data-ttu-id="cdded-120">Nome do consumível.</span><span class="sxs-lookup"><span data-stu-id="cdded-120">ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdded-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cdded-121">-Namespace</span></span>
<span data-ttu-id="cdded-122">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="cdded-122">Namespace Name.</span></span>

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

## <span data-ttu-id="cdded-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cdded-123">INPUTS</span></span>

### <span data-ttu-id="cdded-124">System. String</span><span class="sxs-lookup"><span data-stu-id="cdded-124">System.String</span></span>

## <span data-ttu-id="cdded-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cdded-125">OUTPUTS</span></span>

### <span data-ttu-id="cdded-126">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventHub. Models. ConsumerGroupAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="cdded-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="cdded-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cdded-127">NOTES</span></span>

## <span data-ttu-id="cdded-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cdded-128">RELATED LINKS</span></span>

