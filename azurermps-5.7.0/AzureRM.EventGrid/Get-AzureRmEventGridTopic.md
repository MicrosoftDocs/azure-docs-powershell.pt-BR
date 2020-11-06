---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
ms.openlocfilehash: e71c479624cd77e25adbd4fbfdc609cfa89918b3
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93611157"
---
# <span data-ttu-id="48417-101">Get-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="48417-101">Get-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="48417-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48417-102">SYNOPSIS</span></span>
<span data-ttu-id="48417-103">Obtém os detalhes de um tópico de grade de evento ou obtém uma lista de todos os tópicos de grade de eventos na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="48417-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48417-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48417-104">SYNTAX</span></span>

### <span data-ttu-id="48417-105">ResourceGroupNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="48417-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="48417-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="48417-106">TopicNameParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48417-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="48417-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="48417-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="48417-108">DESCRIPTION</span></span>
<span data-ttu-id="48417-109">O cmdlet Get-AzureRmEventGridTopic Obtém os detalhes de um tópico de grade de evento especificado ou uma lista de todos os tópicos de grade de eventos na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="48417-109">The Get-AzureRmEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="48417-110">Se o nome do tópico for fornecido, os detalhes de um único tópico da grade do evento serão retornados.</span><span class="sxs-lookup"><span data-stu-id="48417-110">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="48417-111">Se o nome do tópico não for fornecido, uma lista de tópicos será retornada.</span><span class="sxs-lookup"><span data-stu-id="48417-111">If the topic name is not provided, a list of topics is returned.</span></span>

## <span data-ttu-id="48417-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48417-112">EXAMPLES</span></span>

### <span data-ttu-id="48417-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="48417-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="48417-114">Obtém os detalhes do tópico de grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="48417-114">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="48417-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="48417-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="48417-116">Obtém os detalhes do tópico de grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="48417-116">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="48417-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="48417-117">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="48417-118">Listar todos os tópicos da grade de eventos no grupo de MyResourceGroupName de grupo \` \` .</span><span class="sxs-lookup"><span data-stu-id="48417-118">List all the Event Grid topics in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="48417-119">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="48417-119">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridTopic
```

<span data-ttu-id="48417-120">Listar todos os tópicos da grade de eventos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="48417-120">List all the Event Grid topics in the subscription.</span></span>

## <span data-ttu-id="48417-121">OS</span><span class="sxs-lookup"><span data-stu-id="48417-121">PARAMETERS</span></span>

### <span data-ttu-id="48417-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48417-122">-DefaultProfile</span></span>
<span data-ttu-id="48417-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="48417-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48417-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="48417-124">-Name</span></span>
<span data-ttu-id="48417-125">Nome do tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="48417-125">EventGrid Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48417-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48417-126">-ResourceGroupName</span></span>
<span data-ttu-id="48417-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="48417-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48417-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48417-128">-ResourceId</span></span>
<span data-ttu-id="48417-129">Identificador de recurso que representa o tópico da grade do evento.</span><span class="sxs-lookup"><span data-stu-id="48417-129">Resource Identifier representing the Event Grid Topic.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48417-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48417-130">CommonParameters</span></span>
<span data-ttu-id="48417-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48417-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48417-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48417-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48417-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="48417-133">INPUTS</span></span>

### <span data-ttu-id="48417-134">System. String</span><span class="sxs-lookup"><span data-stu-id="48417-134">System.String</span></span>
<span data-ttu-id="48417-135">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="48417-135">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="48417-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="48417-136">OUTPUTS</span></span>

### <span data-ttu-id="48417-137">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="48417-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="48417-138">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventGrid. Models. PSTopicListInstance, Microsoft. Azure. Commands. EventGrid, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="48417-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="48417-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="48417-139">NOTES</span></span>

## <span data-ttu-id="48417-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48417-140">RELATED LINKS</span></span>

