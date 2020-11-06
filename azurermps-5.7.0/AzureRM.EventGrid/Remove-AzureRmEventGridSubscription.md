---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/remove-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
ms.openlocfilehash: 681f831ba93943676b6aadb59378efcdd4e79579
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426707"
---
# <span data-ttu-id="8cffb-101">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="8cffb-101">Remove-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="8cffb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8cffb-102">SYNOPSIS</span></span>
<span data-ttu-id="8cffb-103">Remove uma assinatura de evento de grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="8cffb-103">Removes an Azure Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cffb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8cffb-104">SYNTAX</span></span>

### <span data-ttu-id="8cffb-105">ResourceGroupNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8cffb-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cffb-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cffb-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cffb-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8cffb-107">EventSubscriptionInputObjectSet</span></span>
```
Remove-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cffb-108">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cffb-108">TopicNameParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8cffb-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8cffb-109">DESCRIPTION</span></span>
<span data-ttu-id="8cffb-110">Remove uma assinatura de evento de grade de eventos do Azure para um tópico de grade de eventos do Azure, um recurso, uma assinatura do Azure ou um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8cffb-110">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="8cffb-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8cffb-111">EXAMPLES</span></span>

### <span data-ttu-id="8cffb-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8cffb-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="8cffb-113">Remove a assinatura de evento \` EventSubscription1 \` para um tópico de Tópico1 de grade de eventos do Azure \` \` no MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="8cffb-113">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="8cffb-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8cffb-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="8cffb-115">Remove a assinatura de evento \` EventSubscription1 \` a um grupo de MyResourceGroupName de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="8cffb-115">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="8cffb-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="8cffb-116">Example 3</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="8cffb-117">Remove a assinatura de evento \` EventSubscription1 \` para a assinatura padrão do Azure.</span><span class="sxs-lookup"><span data-stu-id="8cffb-117">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="8cffb-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="8cffb-118">Example 4</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="8cffb-119">Remove a assinatura de evento \` EventSubscription1 \` para um namespace de Hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="8cffb-119">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="8cffb-120">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="8cffb-120">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="8cffb-121">Remove a assinatura de evento \` EventSubscription1 \` para um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="8cffb-121">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="8cffb-122">OS</span><span class="sxs-lookup"><span data-stu-id="8cffb-122">PARAMETERS</span></span>

### <span data-ttu-id="8cffb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cffb-123">-DefaultProfile</span></span>
<span data-ttu-id="8cffb-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8cffb-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8cffb-125">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="8cffb-125">-EventSubscriptionName</span></span>
<span data-ttu-id="8cffb-126">Nome da assinatura de evento que precisa ser removida.</span><span class="sxs-lookup"><span data-stu-id="8cffb-126">Name of the event subscription that needs to be removed.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cffb-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cffb-127">-InputObject</span></span>
<span data-ttu-id="8cffb-128">Objeto EventSubscription EventGrid.</span><span class="sxs-lookup"><span data-stu-id="8cffb-128">EventGrid EventSubscription object.</span></span>

```yaml
Type: PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cffb-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8cffb-129">-PassThru</span></span>
<span data-ttu-id="8cffb-130">Retorna o status da operação de remoção.</span><span class="sxs-lookup"><span data-stu-id="8cffb-130">Returns the status of the Remove operation.</span></span> <span data-ttu-id="8cffb-131">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="8cffb-131">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cffb-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cffb-132">-ResourceGroupName</span></span>
<span data-ttu-id="8cffb-133">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8cffb-133">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cffb-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cffb-134">-ResourceId</span></span>
<span data-ttu-id="8cffb-135">Identificador do recurso cuja assinatura de evento precisa ser removida.</span><span class="sxs-lookup"><span data-stu-id="8cffb-135">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="8cffb-136">-Topicname</span><span class="sxs-lookup"><span data-stu-id="8cffb-136">-TopicName</span></span>
<span data-ttu-id="8cffb-137">Nome do tópico da grade do evento.</span><span class="sxs-lookup"><span data-stu-id="8cffb-137">Event Grid Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cffb-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8cffb-138">-Confirm</span></span>
<span data-ttu-id="8cffb-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cffb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cffb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cffb-140">-WhatIf</span></span>
<span data-ttu-id="8cffb-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8cffb-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cffb-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8cffb-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cffb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cffb-143">CommonParameters</span></span>
<span data-ttu-id="8cffb-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cffb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cffb-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cffb-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cffb-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8cffb-146">INPUTS</span></span>

### <span data-ttu-id="8cffb-147">System. String</span><span class="sxs-lookup"><span data-stu-id="8cffb-147">System.String</span></span>
<span data-ttu-id="8cffb-148">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="8cffb-148">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="8cffb-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8cffb-149">OUTPUTS</span></span>

### <span data-ttu-id="8cffb-150">System. Object</span><span class="sxs-lookup"><span data-stu-id="8cffb-150">System.Object</span></span>

## <span data-ttu-id="8cffb-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8cffb-151">NOTES</span></span>

## <span data-ttu-id="8cffb-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8cffb-152">RELATED LINKS</span></span>

