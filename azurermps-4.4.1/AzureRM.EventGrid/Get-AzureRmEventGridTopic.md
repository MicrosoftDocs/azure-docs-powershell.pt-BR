---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
ms.openlocfilehash: 8ea4fc7674af247ffded2c6c4317f07a831adf2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433134"
---
# <span data-ttu-id="e0f1f-101">Get-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="e0f1f-101">Get-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="e0f1f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0f1f-102">SYNOPSIS</span></span>
<span data-ttu-id="e0f1f-103">Obtém os detalhes de um tópico de grade de evento ou obtém uma lista de todos os tópicos de grade de eventos na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0f1f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0f1f-104">SYNTAX</span></span>

### <span data-ttu-id="e0f1f-105">ResourceGroupNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e0f1f-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0f1f-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0f1f-106">TopicNameParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0f1f-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0f1f-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0f1f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e0f1f-108">DESCRIPTION</span></span>
<span data-ttu-id="e0f1f-109">O cmdlet Get-AzureRmEventGridTopic Obtém os detalhes de um tópico de grade de evento especificado ou uma lista de todos os tópicos de grade de eventos na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-109">The Get-AzureRmEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="e0f1f-110">Se o nome do tópico for fornecido, os detalhes de um único tópico da grade do evento serão retornados.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-110">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="e0f1f-111">Se o nome do tópico não for fornecido, uma lista de tópicos será retornada.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-111">If the topic name is not provided, a list of topics is returned.</span></span>

## <span data-ttu-id="e0f1f-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0f1f-112">EXAMPLES</span></span>

### <span data-ttu-id="e0f1f-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e0f1f-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="e0f1f-114">Obtém os detalhes do tópico de grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="e0f1f-114">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e0f1f-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e0f1f-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="e0f1f-116">Obtém os detalhes do tópico de grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="e0f1f-116">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e0f1f-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e0f1f-117">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="e0f1f-118">Listar todos os tópicos da grade de eventos no grupo de MyResourceGroupName de grupo \` \` .</span><span class="sxs-lookup"><span data-stu-id="e0f1f-118">List all the Event Grid topics in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e0f1f-119">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="e0f1f-119">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridTopic
```

<span data-ttu-id="e0f1f-120">Listar todos os tópicos da grade de eventos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-120">List all the Event Grid topics in the subscription.</span></span>

## <span data-ttu-id="e0f1f-121">OS</span><span class="sxs-lookup"><span data-stu-id="e0f1f-121">PARAMETERS</span></span>

### <span data-ttu-id="e0f1f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0f1f-122">-Name</span></span>
<span data-ttu-id="e0f1f-123">Nome do tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-123">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f1f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0f1f-124">-ResourceGroupName</span></span>
<span data-ttu-id="e0f1f-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f1f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0f1f-126">-ResourceId</span></span>
<span data-ttu-id="e0f1f-127">Identificador de recurso que representa o tópico da grade do evento.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-127">Resource Identifier representing the Event Grid Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f1f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0f1f-128">-DefaultProfile</span></span>
<span data-ttu-id="e0f1f-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0f1f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0f1f-130">CommonParameters</span></span>
<span data-ttu-id="e0f1f-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0f1f-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0f1f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0f1f-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e0f1f-133">INPUTS</span></span>

### <span data-ttu-id="e0f1f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e0f1f-134">System.String</span></span>
<span data-ttu-id="e0f1f-135">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="e0f1f-135">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="e0f1f-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e0f1f-136">OUTPUTS</span></span>

### <span data-ttu-id="e0f1f-137">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="e0f1f-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="e0f1f-138">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventGrid. Models. PSTopicListInstance, Microsoft. Azure. Commands. EventGrid, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e0f1f-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e0f1f-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e0f1f-139">NOTES</span></span>

## <span data-ttu-id="e0f1f-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0f1f-140">RELATED LINKS</span></span>

