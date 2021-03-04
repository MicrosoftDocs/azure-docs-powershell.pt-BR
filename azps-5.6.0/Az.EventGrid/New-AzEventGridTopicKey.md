---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/new-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
ms.openlocfilehash: aa59b4046a775c41dd3b44142d0a407c94ff1f4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890413"
---
# <span data-ttu-id="d7515-101">New-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="d7515-101">New-AzEventGridTopicKey</span></span>

## <span data-ttu-id="d7515-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7515-102">SYNOPSIS</span></span>
<span data-ttu-id="d7515-103">Regenera a chave de acesso compartilhado para um Tópico de Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d7515-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="d7515-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d7515-104">SYNTAX</span></span>

### <span data-ttu-id="d7515-105">TopicNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d7515-105">TopicNameParameterSet (Default)</span></span>
```
New-AzEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7515-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7515-106">TopicInputObjectParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7515-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7515-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7515-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d7515-108">DESCRIPTION</span></span>
<span data-ttu-id="d7515-109">Regenera a chave de acesso compartilhado para um Tópico de Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d7515-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="d7515-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7515-110">EXAMPLES</span></span>

### <span data-ttu-id="d7515-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d7515-111">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="d7515-112">Regenerar a chave correspondente à chave chave1'\ do tópico De grade de eventos Tópico1 no grupo de recursos \' \` \` \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="d7515-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d7515-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d7515-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="d7515-114">Regenerar a chave correspondente à chave chave1'\ do tópico De grade de eventos Tópico1 no grupo de recursos \' \` \` \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="d7515-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="d7515-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d7515-115">PARAMETERS</span></span>

### <span data-ttu-id="d7515-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7515-116">-DefaultProfile</span></span>
<span data-ttu-id="d7515-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="d7515-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7515-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7515-118">-InputObject</span></span>
<span data-ttu-id="d7515-119">Objeto EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="d7515-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="d7515-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d7515-120">-KeyName</span></span>
<span data-ttu-id="d7515-121">O nome da chave que precisa ser regenerada</span><span class="sxs-lookup"><span data-stu-id="d7515-121">The name of the key that needs to be regenerated</span></span>

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

### <span data-ttu-id="d7515-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7515-122">-ResourceGroupName</span></span>
<span data-ttu-id="d7515-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d7515-123">Resource group name.</span></span>

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

### <span data-ttu-id="d7515-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7515-124">-ResourceId</span></span>
<span data-ttu-id="d7515-125">Identificador de Recurso que representa o Tópico da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="d7515-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="d7515-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="d7515-126">-TopicName</span></span>
<span data-ttu-id="d7515-127">O nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="d7515-127">The name of the topic.</span></span>

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

### <span data-ttu-id="d7515-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7515-128">-Confirm</span></span>
<span data-ttu-id="d7515-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7515-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7515-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7515-130">-WhatIf</span></span>
<span data-ttu-id="d7515-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d7515-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7515-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d7515-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7515-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7515-133">CommonParameters</span></span>
<span data-ttu-id="d7515-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7515-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7515-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7515-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7515-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7515-136">INPUTS</span></span>

### <span data-ttu-id="d7515-137">System.String</span><span class="sxs-lookup"><span data-stu-id="d7515-137">System.String</span></span>

### <span data-ttu-id="d7515-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="d7515-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="d7515-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d7515-139">OUTPUTS</span></span>

### <span data-ttu-id="d7515-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="d7515-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="d7515-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="d7515-141">NOTES</span></span>

## <span data-ttu-id="d7515-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7515-142">RELATED LINKS</span></span>
