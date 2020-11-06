---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: 3454a3aad2276384588c0ccc550a1b0ef6df7cfc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600877"
---
# <span data-ttu-id="31568-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="31568-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="31568-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="31568-102">SYNOPSIS</span></span>
<span data-ttu-id="31568-103">Obtém as chaves de acesso compartilhado usadas para publicar eventos em um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="31568-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="31568-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31568-104">SYNTAX</span></span>

### <span data-ttu-id="31568-105">TopicNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="31568-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31568-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31568-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31568-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="31568-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31568-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="31568-108">DESCRIPTION</span></span>
<span data-ttu-id="31568-109">Obtém as chaves de acesso compartilhado usadas para publicar eventos em um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="31568-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="31568-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="31568-110">EXAMPLES</span></span>

### <span data-ttu-id="31568-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="31568-111">Example 1</span></span>
```
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="31568-112">Obtém as chaves de acesso compartilhado do tópico de grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="31568-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="31568-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="31568-113">Example 2</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="31568-114">Obtém as chaves de acesso compartilhado do tópico de grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="31568-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="31568-115">OS</span><span class="sxs-lookup"><span data-stu-id="31568-115">PARAMETERS</span></span>

### <span data-ttu-id="31568-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31568-116">-DefaultProfile</span></span>
<span data-ttu-id="31568-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="31568-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31568-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31568-118">-InputObject</span></span>
<span data-ttu-id="31568-119">Objeto de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="31568-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="31568-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="31568-120">-Name</span></span>
<span data-ttu-id="31568-121">Nome do tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="31568-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="31568-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31568-122">-ResourceGroupName</span></span>
<span data-ttu-id="31568-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="31568-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="31568-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31568-124">-ResourceId</span></span>
<span data-ttu-id="31568-125">Identificador de recurso que representa o tópico da grade do evento.</span><span class="sxs-lookup"><span data-stu-id="31568-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="31568-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31568-126">CommonParameters</span></span>
<span data-ttu-id="31568-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31568-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31568-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31568-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31568-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="31568-129">INPUTS</span></span>

### <span data-ttu-id="31568-130">System. String</span><span class="sxs-lookup"><span data-stu-id="31568-130">System.String</span></span>

### <span data-ttu-id="31568-131">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="31568-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="31568-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="31568-132">OUTPUTS</span></span>

### <span data-ttu-id="31568-133">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="31568-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="31568-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="31568-134">NOTES</span></span>

## <span data-ttu-id="31568-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31568-135">RELATED LINKS</span></span>
