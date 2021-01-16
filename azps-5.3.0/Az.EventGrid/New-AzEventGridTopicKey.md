---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
ms.openlocfilehash: ab9c9401b0f8d929be1a4aa244f407957d886e4c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271406"
---
# <span data-ttu-id="e17f8-101">New-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="e17f8-101">New-AzEventGridTopicKey</span></span>

## <span data-ttu-id="e17f8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e17f8-102">SYNOPSIS</span></span>
<span data-ttu-id="e17f8-103">Regenera a chave de acesso compartilhada para um tópico da grade do evento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e17f8-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="e17f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e17f8-104">SYNTAX</span></span>

### <span data-ttu-id="e17f8-105">TopicNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e17f8-105">TopicNameParameterSet (Default)</span></span>
```
New-AzEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e17f8-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e17f8-106">TopicInputObjectParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e17f8-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e17f8-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e17f8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e17f8-108">DESCRIPTION</span></span>
<span data-ttu-id="e17f8-109">Regenera a chave de acesso compartilhada para um tópico da grade do evento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e17f8-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="e17f8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e17f8-110">EXAMPLES</span></span>

### <span data-ttu-id="e17f8-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e17f8-111">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="e17f8-112">Regenere a chave correspondente à chave \' key1 ' \ do tópico da grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="e17f8-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e17f8-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e17f8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="e17f8-114">Regenere a chave correspondente à chave \' key1 ' \ do tópico da grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="e17f8-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e17f8-115">OS</span><span class="sxs-lookup"><span data-stu-id="e17f8-115">PARAMETERS</span></span>

### <span data-ttu-id="e17f8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e17f8-116">-DefaultProfile</span></span>
<span data-ttu-id="e17f8-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e17f8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e17f8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e17f8-118">-InputObject</span></span>
<span data-ttu-id="e17f8-119">Objeto de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="e17f8-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="e17f8-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e17f8-120">-KeyName</span></span>
<span data-ttu-id="e17f8-121">O nome da chave que precisa ser regenerada</span><span class="sxs-lookup"><span data-stu-id="e17f8-121">The name of the key that needs to be regenerated</span></span>

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

### <span data-ttu-id="e17f8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e17f8-122">-ResourceGroupName</span></span>
<span data-ttu-id="e17f8-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e17f8-123">Resource group name.</span></span>

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

### <span data-ttu-id="e17f8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e17f8-124">-ResourceId</span></span>
<span data-ttu-id="e17f8-125">Identificador de recurso que representa o tópico da grade do evento.</span><span class="sxs-lookup"><span data-stu-id="e17f8-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="e17f8-126">-Topicname</span><span class="sxs-lookup"><span data-stu-id="e17f8-126">-TopicName</span></span>
<span data-ttu-id="e17f8-127">O nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="e17f8-127">The name of the topic.</span></span>

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

### <span data-ttu-id="e17f8-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e17f8-128">-Confirm</span></span>
<span data-ttu-id="e17f8-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e17f8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e17f8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e17f8-130">-WhatIf</span></span>
<span data-ttu-id="e17f8-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e17f8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e17f8-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e17f8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e17f8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e17f8-133">CommonParameters</span></span>
<span data-ttu-id="e17f8-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e17f8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e17f8-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e17f8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e17f8-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e17f8-136">INPUTS</span></span>

### <span data-ttu-id="e17f8-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e17f8-137">System.String</span></span>

### <span data-ttu-id="e17f8-138">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="e17f8-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="e17f8-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e17f8-139">OUTPUTS</span></span>

### <span data-ttu-id="e17f8-140">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="e17f8-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="e17f8-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e17f8-141">NOTES</span></span>

## <span data-ttu-id="e17f8-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e17f8-142">RELATED LINKS</span></span>
