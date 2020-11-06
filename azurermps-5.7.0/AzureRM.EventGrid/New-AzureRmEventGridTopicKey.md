---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/new-azurermeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 3600d7523e95b937f20d9d0b97d677c5cf02ca0f
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93441591"
---
# <span data-ttu-id="c0b11-101">New-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="c0b11-101">New-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="c0b11-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c0b11-102">SYNOPSIS</span></span>
<span data-ttu-id="c0b11-103">Regenera a chave de acesso compartilhada para um tópico da grade do evento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c0b11-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0b11-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0b11-104">SYNTAX</span></span>

### <span data-ttu-id="c0b11-105">TopicNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c0b11-105">TopicNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0b11-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0b11-106">TopicInputObjectParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0b11-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0b11-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0b11-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c0b11-108">DESCRIPTION</span></span>
<span data-ttu-id="c0b11-109">Regenera a chave de acesso compartilhada para um tópico da grade do evento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c0b11-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="c0b11-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0b11-110">EXAMPLES</span></span>

### <span data-ttu-id="c0b11-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c0b11-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="c0b11-112">Regenere a chave correspondente à chave \' key1 ' \ do tópico da grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="c0b11-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c0b11-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c0b11-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzureRmEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="c0b11-114">Regenere a chave correspondente à chave \' key1 ' \ do tópico da grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="c0b11-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="c0b11-115">OS</span><span class="sxs-lookup"><span data-stu-id="c0b11-115">PARAMETERS</span></span>

### <span data-ttu-id="c0b11-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0b11-116">-DefaultProfile</span></span>
<span data-ttu-id="c0b11-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c0b11-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0b11-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0b11-118">-InputObject</span></span>
<span data-ttu-id="c0b11-119">Objeto de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c0b11-119">EventGrid Topic object.</span></span>

```yaml
Type: PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0b11-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="c0b11-120">-KeyName</span></span>
<span data-ttu-id="c0b11-121">O nome da chave que precisa ser regenerada</span><span class="sxs-lookup"><span data-stu-id="c0b11-121">The name of the key that needs to be regenerated</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0b11-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0b11-122">-ResourceGroupName</span></span>
<span data-ttu-id="c0b11-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c0b11-123">Resource group name.</span></span>

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

### <span data-ttu-id="c0b11-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0b11-124">-ResourceId</span></span>
<span data-ttu-id="c0b11-125">Identificador de recurso que representa o tópico da grade do evento.</span><span class="sxs-lookup"><span data-stu-id="c0b11-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="c0b11-126">-Topicname</span><span class="sxs-lookup"><span data-stu-id="c0b11-126">-TopicName</span></span>
<span data-ttu-id="c0b11-127">O nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="c0b11-127">The name of the topic.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0b11-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c0b11-128">-Confirm</span></span>
<span data-ttu-id="c0b11-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0b11-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0b11-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0b11-130">-WhatIf</span></span>
<span data-ttu-id="c0b11-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c0b11-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0b11-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c0b11-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0b11-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0b11-133">CommonParameters</span></span>
<span data-ttu-id="c0b11-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0b11-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0b11-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0b11-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0b11-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c0b11-136">INPUTS</span></span>

### <span data-ttu-id="c0b11-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c0b11-137">System.String</span></span>

## <span data-ttu-id="c0b11-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c0b11-138">OUTPUTS</span></span>

### <span data-ttu-id="c0b11-139">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="c0b11-139">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="c0b11-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c0b11-140">NOTES</span></span>

## <span data-ttu-id="c0b11-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0b11-141">RELATED LINKS</span></span>

