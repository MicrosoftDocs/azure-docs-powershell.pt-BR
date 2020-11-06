---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
ms.openlocfilehash: bb9cd92ff614a944c144f056d8d59aa1d4239b25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441107"
---
# <span data-ttu-id="12fff-101">New-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="12fff-101">New-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="12fff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12fff-102">SYNOPSIS</span></span>
<span data-ttu-id="12fff-103">Regenera a chave de acesso compartilhada para um tópico da grade do evento do Azure.</span><span class="sxs-lookup"><span data-stu-id="12fff-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12fff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12fff-104">SYNTAX</span></span>

### <span data-ttu-id="12fff-105">TopicNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="12fff-105">TopicNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12fff-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12fff-106">TopicInputObjectParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12fff-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="12fff-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12fff-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12fff-108">DESCRIPTION</span></span>
<span data-ttu-id="12fff-109">Regenera a chave de acesso compartilhada para um tópico da grade do evento do Azure.</span><span class="sxs-lookup"><span data-stu-id="12fff-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="12fff-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12fff-110">EXAMPLES</span></span>

### <span data-ttu-id="12fff-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="12fff-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="12fff-112">Regenere a chave correspondente à chave \' key1 ' \ do tópico da grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="12fff-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="12fff-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="12fff-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzureRmEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="12fff-114">Regenere a chave correspondente à chave \' key1 ' \ do tópico da grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="12fff-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="12fff-115">OS</span><span class="sxs-lookup"><span data-stu-id="12fff-115">PARAMETERS</span></span>

### <span data-ttu-id="12fff-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12fff-116">-InputObject</span></span>
<span data-ttu-id="12fff-117">Objeto de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="12fff-117">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="12fff-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="12fff-118">-KeyName</span></span>
<span data-ttu-id="12fff-119">O nome da chave que precisa ser regenerada</span><span class="sxs-lookup"><span data-stu-id="12fff-119">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12fff-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12fff-120">-ResourceGroupName</span></span>
<span data-ttu-id="12fff-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="12fff-121">Resource group name.</span></span>

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

### <span data-ttu-id="12fff-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12fff-122">-ResourceId</span></span>
<span data-ttu-id="12fff-123">Identificador de recurso que representa o tópico da grade do evento.</span><span class="sxs-lookup"><span data-stu-id="12fff-123">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="12fff-124">-Topicname</span><span class="sxs-lookup"><span data-stu-id="12fff-124">-TopicName</span></span>
<span data-ttu-id="12fff-125">O nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="12fff-125">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12fff-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="12fff-126">-Confirm</span></span>
<span data-ttu-id="12fff-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12fff-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12fff-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12fff-128">-WhatIf</span></span>
<span data-ttu-id="12fff-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="12fff-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12fff-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="12fff-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12fff-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12fff-131">-DefaultProfile</span></span>
<span data-ttu-id="12fff-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12fff-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12fff-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12fff-133">CommonParameters</span></span>
<span data-ttu-id="12fff-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12fff-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12fff-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12fff-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12fff-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12fff-136">INPUTS</span></span>

### <span data-ttu-id="12fff-137">System. String</span><span class="sxs-lookup"><span data-stu-id="12fff-137">System.String</span></span>

## <span data-ttu-id="12fff-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12fff-138">OUTPUTS</span></span>

### <span data-ttu-id="12fff-139">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="12fff-139">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="12fff-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12fff-140">NOTES</span></span>

## <span data-ttu-id="12fff-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12fff-141">RELATED LINKS</span></span>

