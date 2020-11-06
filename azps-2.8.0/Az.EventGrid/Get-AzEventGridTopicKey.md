---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: b39f9c3c3c1d72624c612d2743b32d306eefa131
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596531"
---
# <span data-ttu-id="117fa-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="117fa-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="117fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="117fa-102">SYNOPSIS</span></span>
<span data-ttu-id="117fa-103">Obtém as chaves de acesso compartilhado usadas para publicar eventos em um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="117fa-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="117fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="117fa-104">SYNTAX</span></span>

### <span data-ttu-id="117fa-105">TopicNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="117fa-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="117fa-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="117fa-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="117fa-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="117fa-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="117fa-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="117fa-108">DESCRIPTION</span></span>
<span data-ttu-id="117fa-109">Obtém as chaves de acesso compartilhado usadas para publicar eventos em um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="117fa-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="117fa-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="117fa-110">EXAMPLES</span></span>

### <span data-ttu-id="117fa-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="117fa-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="117fa-112">Obtém as chaves de acesso compartilhado do tópico de grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="117fa-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="117fa-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="117fa-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="117fa-114">Obtém as chaves de acesso compartilhado do tópico de grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="117fa-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="117fa-115">OS</span><span class="sxs-lookup"><span data-stu-id="117fa-115">PARAMETERS</span></span>

### <span data-ttu-id="117fa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="117fa-116">-DefaultProfile</span></span>
<span data-ttu-id="117fa-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="117fa-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="117fa-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="117fa-118">-InputObject</span></span>
<span data-ttu-id="117fa-119">Objeto de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="117fa-119">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="117fa-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="117fa-120">-Name</span></span>
<span data-ttu-id="117fa-121">Nome do tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="117fa-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="117fa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="117fa-122">-ResourceGroupName</span></span>
<span data-ttu-id="117fa-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="117fa-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="117fa-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="117fa-124">-ResourceId</span></span>
<span data-ttu-id="117fa-125">Identificador de recurso que representa o tópico da grade do evento.</span><span class="sxs-lookup"><span data-stu-id="117fa-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="117fa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="117fa-126">CommonParameters</span></span>
<span data-ttu-id="117fa-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="117fa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="117fa-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="117fa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="117fa-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="117fa-129">INPUTS</span></span>

### <span data-ttu-id="117fa-130">System. String</span><span class="sxs-lookup"><span data-stu-id="117fa-130">System.String</span></span>

### <span data-ttu-id="117fa-131">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="117fa-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="117fa-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="117fa-132">OUTPUTS</span></span>

### <span data-ttu-id="117fa-133">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="117fa-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="117fa-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="117fa-134">NOTES</span></span>

## <span data-ttu-id="117fa-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="117fa-135">RELATED LINKS</span></span>
