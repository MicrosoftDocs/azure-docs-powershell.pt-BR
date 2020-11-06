---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 91e3acd227acd8a83dcd5ccb0beb2ed12d1cca99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610804"
---
# <span data-ttu-id="75fa4-101">Get-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="75fa4-101">Get-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="75fa4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75fa4-102">SYNOPSIS</span></span>
<span data-ttu-id="75fa4-103">Obtém as chaves de acesso compartilhado usadas para publicar eventos em um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="75fa4-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75fa4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75fa4-104">SYNTAX</span></span>

### <span data-ttu-id="75fa4-105">TopicNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="75fa4-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75fa4-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75fa4-106">TopicInputObjectParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="75fa4-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="75fa4-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75fa4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75fa4-108">DESCRIPTION</span></span>
<span data-ttu-id="75fa4-109">Obtém as chaves de acesso compartilhado usadas para publicar eventos em um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="75fa4-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="75fa4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75fa4-110">EXAMPLES</span></span>

### <span data-ttu-id="75fa4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="75fa4-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="75fa4-112">Obtém as chaves de acesso compartilhado do tópico de grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="75fa4-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="75fa4-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="75fa4-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzureRmEventGridTopicKey
```

<span data-ttu-id="75fa4-114">Obtém as chaves de acesso compartilhado do tópico de grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="75fa4-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="75fa4-115">OS</span><span class="sxs-lookup"><span data-stu-id="75fa4-115">PARAMETERS</span></span>

### <span data-ttu-id="75fa4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75fa4-116">-InputObject</span></span>
<span data-ttu-id="75fa4-117">Objeto de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="75fa4-117">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="75fa4-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="75fa4-118">-Name</span></span>
<span data-ttu-id="75fa4-119">Nome do tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="75fa4-119">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="75fa4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75fa4-120">-ResourceGroupName</span></span>
<span data-ttu-id="75fa4-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="75fa4-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="75fa4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75fa4-122">-ResourceId</span></span>
<span data-ttu-id="75fa4-123">Identificador de recurso que representa o tópico da grade do evento.</span><span class="sxs-lookup"><span data-stu-id="75fa4-123">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="75fa4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75fa4-124">-DefaultProfile</span></span>
<span data-ttu-id="75fa4-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75fa4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75fa4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75fa4-126">CommonParameters</span></span>
<span data-ttu-id="75fa4-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75fa4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75fa4-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75fa4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75fa4-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75fa4-129">INPUTS</span></span>

### <span data-ttu-id="75fa4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="75fa4-130">System.String</span></span>

## <span data-ttu-id="75fa4-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75fa4-131">OUTPUTS</span></span>

### <span data-ttu-id="75fa4-132">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="75fa4-132">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="75fa4-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75fa4-133">NOTES</span></span>

## <span data-ttu-id="75fa4-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75fa4-134">RELATED LINKS</span></span>

