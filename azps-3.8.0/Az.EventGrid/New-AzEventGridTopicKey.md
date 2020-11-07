---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
ms.openlocfilehash: 8749f5ad542d55f167f866e436acf72aacf3bc14
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941431"
---
# <span data-ttu-id="53c9c-101">New-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="53c9c-101">New-AzEventGridTopicKey</span></span>

## <span data-ttu-id="53c9c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="53c9c-103">Regenera a chave de acesso compartilhada para um tópico da grade do evento do Azure.</span><span class="sxs-lookup"><span data-stu-id="53c9c-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="53c9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53c9c-104">SYNTAX</span></span>

### <span data-ttu-id="53c9c-105">TopicNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="53c9c-105">TopicNameParameterSet (Default)</span></span>
```
New-AzEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53c9c-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="53c9c-106">TopicInputObjectParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53c9c-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="53c9c-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53c9c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53c9c-108">DESCRIPTION</span></span>
<span data-ttu-id="53c9c-109">Regenera a chave de acesso compartilhada para um tópico da grade do evento do Azure.</span><span class="sxs-lookup"><span data-stu-id="53c9c-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="53c9c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53c9c-110">EXAMPLES</span></span>

### <span data-ttu-id="53c9c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="53c9c-111">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="53c9c-112">Regenere a chave correspondente à chave \' key1 ' \ do tópico da grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="53c9c-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="53c9c-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="53c9c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="53c9c-114">Regenere a chave correspondente à chave \' key1 ' \ do tópico da grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="53c9c-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="53c9c-115">OS</span><span class="sxs-lookup"><span data-stu-id="53c9c-115">PARAMETERS</span></span>

### <span data-ttu-id="53c9c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53c9c-116">-DefaultProfile</span></span>
<span data-ttu-id="53c9c-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="53c9c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53c9c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53c9c-118">-InputObject</span></span>
<span data-ttu-id="53c9c-119">Objeto de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="53c9c-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="53c9c-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="53c9c-120">-KeyName</span></span>
<span data-ttu-id="53c9c-121">O nome da chave que precisa ser regenerada</span><span class="sxs-lookup"><span data-stu-id="53c9c-121">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53c9c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53c9c-122">-ResourceGroupName</span></span>
<span data-ttu-id="53c9c-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="53c9c-123">Resource group name.</span></span>

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

### <span data-ttu-id="53c9c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53c9c-124">-ResourceId</span></span>
<span data-ttu-id="53c9c-125">Identificador de recurso que representa o tópico da grade do evento.</span><span class="sxs-lookup"><span data-stu-id="53c9c-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="53c9c-126">-Topicname</span><span class="sxs-lookup"><span data-stu-id="53c9c-126">-TopicName</span></span>
<span data-ttu-id="53c9c-127">O nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="53c9c-127">The name of the topic.</span></span>

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

### <span data-ttu-id="53c9c-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="53c9c-128">-Confirm</span></span>
<span data-ttu-id="53c9c-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53c9c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53c9c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53c9c-130">-WhatIf</span></span>
<span data-ttu-id="53c9c-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="53c9c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53c9c-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="53c9c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53c9c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53c9c-133">CommonParameters</span></span>
<span data-ttu-id="53c9c-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53c9c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53c9c-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53c9c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53c9c-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53c9c-136">INPUTS</span></span>

### <span data-ttu-id="53c9c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="53c9c-137">System.String</span></span>

### <span data-ttu-id="53c9c-138">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="53c9c-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="53c9c-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53c9c-139">OUTPUTS</span></span>

### <span data-ttu-id="53c9c-140">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="53c9c-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="53c9c-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53c9c-141">NOTES</span></span>

## <span data-ttu-id="53c9c-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53c9c-142">RELATED LINKS</span></span>
