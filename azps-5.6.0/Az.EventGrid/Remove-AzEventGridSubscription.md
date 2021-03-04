---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: 1625e3325164156b1809640c54d4b75698ae7363
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890407"
---
# <span data-ttu-id="a9cc3-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a9cc3-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="a9cc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9cc3-102">SYNOPSIS</span></span>
<span data-ttu-id="a9cc3-103">Remove uma assinatura de evento da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="a9cc3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a9cc3-104">SYNTAX</span></span>

### <span data-ttu-id="a9cc3-105">ResourceGroupNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a9cc3-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9cc3-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9cc3-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9cc3-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9cc3-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9cc3-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9cc3-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9cc3-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9cc3-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9cc3-110">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9cc3-110">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9cc3-111">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9cc3-111">DomainNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9cc3-112">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9cc3-112">DomainEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9cc3-113">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9cc3-113">DomainTopicEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9cc3-114">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a9cc3-114">DESCRIPTION</span></span>
<span data-ttu-id="a9cc3-115">Remove uma assinatura de evento grade de eventos do Azure para um tópico grade de eventos do Azure, um recurso, uma assinatura do Azure ou um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-115">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="a9cc3-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9cc3-116">EXAMPLES</span></span>

### <span data-ttu-id="a9cc3-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a9cc3-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a9cc3-118">Remove a assinatura do evento EventSubscription1 para um tópico da Grade de Eventos do Azure1 no grupo de recursos \` \` \` \` \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a9cc3-118">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a9cc3-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a9cc3-119">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a9cc3-120">Remove a assinatura de evento \` EventSubscription1 \` para um grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a9cc3-120">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a9cc3-121">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a9cc3-121">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a9cc3-122">Remove a assinatura de evento \` EventSubscription1 \` para a assinatura padrão do Azure.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-122">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="a9cc3-123">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="a9cc3-123">Example 4</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a9cc3-124">Remove a assinatura de evento \` EventSubscription1 \` para um namespace do Hub de Eventos.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-124">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="a9cc3-125">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="a9cc3-125">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a9cc3-126">Remove a assinatura do \` evento EventSubscription1 \` para um Tópico de Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-126">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="a9cc3-127">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a9cc3-127">PARAMETERS</span></span>

### <span data-ttu-id="a9cc3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9cc3-128">-DefaultProfile</span></span>
<span data-ttu-id="a9cc3-129">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a9cc3-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9cc3-130">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="a9cc3-130">-DomainInputObject</span></span>
<span data-ttu-id="a9cc3-131">Objeto EventGrid Domain.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-131">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9cc3-132">-DomainName</span><span class="sxs-lookup"><span data-stu-id="a9cc3-132">-DomainName</span></span>
<span data-ttu-id="a9cc3-133">Nome de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-133">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9cc3-134">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="a9cc3-134">-DomainTopicInputObject</span></span>
<span data-ttu-id="a9cc3-135">Objeto EventGrid Domain Topic.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-135">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9cc3-136">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="a9cc3-136">-DomainTopicName</span></span>
<span data-ttu-id="a9cc3-137">Nome do tópico do domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-137">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9cc3-138">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a9cc3-138">-EventSubscriptionName</span></span>
<span data-ttu-id="a9cc3-139">Nome da assinatura de evento que precisa ser removida.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-139">Name of the event subscription that needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet, DomainNameParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9cc3-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9cc3-140">-InputObject</span></span>
<span data-ttu-id="a9cc3-141">Objeto EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-141">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9cc3-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9cc3-142">-PassThru</span></span>
<span data-ttu-id="a9cc3-143">Retorna o status da operação Remover.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-143">Returns the status of the Remove operation.</span></span> <span data-ttu-id="a9cc3-144">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-144">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9cc3-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9cc3-145">-ResourceGroupName</span></span>
<span data-ttu-id="a9cc3-146">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-146">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9cc3-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9cc3-147">-ResourceId</span></span>
<span data-ttu-id="a9cc3-148">Identificador do recurso cuja assinatura de evento precisa ser removida.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-148">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="a9cc3-149">-TopicName</span><span class="sxs-lookup"><span data-stu-id="a9cc3-149">-TopicName</span></span>
<span data-ttu-id="a9cc3-150">Nome do tópico da grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-150">Event Grid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9cc3-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9cc3-151">-Confirm</span></span>
<span data-ttu-id="a9cc3-152">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9cc3-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9cc3-153">-WhatIf</span></span>
<span data-ttu-id="a9cc3-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9cc3-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9cc3-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9cc3-156">CommonParameters</span></span>
<span data-ttu-id="a9cc3-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9cc3-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9cc3-158">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9cc3-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9cc3-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9cc3-159">INPUTS</span></span>

### <span data-ttu-id="a9cc3-160">System.String</span><span class="sxs-lookup"><span data-stu-id="a9cc3-160">System.String</span></span>

### <span data-ttu-id="a9cc3-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="a9cc3-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="a9cc3-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="a9cc3-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="a9cc3-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="a9cc3-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="a9cc3-164">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a9cc3-164">OUTPUTS</span></span>

### <span data-ttu-id="a9cc3-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a9cc3-165">System.Boolean</span></span>

## <span data-ttu-id="a9cc3-166">NOTES</span><span class="sxs-lookup"><span data-stu-id="a9cc3-166">NOTES</span></span>

## <span data-ttu-id="a9cc3-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9cc3-167">RELATED LINKS</span></span>
