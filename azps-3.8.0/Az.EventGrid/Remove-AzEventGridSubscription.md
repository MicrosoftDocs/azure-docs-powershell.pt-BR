---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: 59cf723d976d8f16d2e810ba2a8fbb924c822137
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940942"
---
# <span data-ttu-id="7372f-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="7372f-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="7372f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7372f-102">SYNOPSIS</span></span>
<span data-ttu-id="7372f-103">Remove uma assinatura de evento de grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="7372f-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="7372f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7372f-104">SYNTAX</span></span>

### <span data-ttu-id="7372f-105">ResourceGroupNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7372f-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7372f-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7372f-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7372f-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7372f-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7372f-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7372f-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7372f-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7372f-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7372f-110">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7372f-110">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7372f-111">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7372f-111">DomainNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7372f-112">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7372f-112">DomainEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7372f-113">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7372f-113">DomainTopicEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7372f-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7372f-114">DESCRIPTION</span></span>
<span data-ttu-id="7372f-115">Remove uma assinatura de evento de grade de eventos do Azure para um tópico de grade de eventos do Azure, um recurso, uma assinatura do Azure ou um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7372f-115">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="7372f-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7372f-116">EXAMPLES</span></span>

### <span data-ttu-id="7372f-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7372f-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="7372f-118">Remove a assinatura de evento \` EventSubscription1 \` para um tópico de Tópico1 de grade de eventos do Azure \` \` no MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="7372f-118">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="7372f-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7372f-119">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="7372f-120">Remove a assinatura de evento \` EventSubscription1 \` a um grupo de MyResourceGroupName de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="7372f-120">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="7372f-121">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="7372f-121">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="7372f-122">Remove a assinatura de evento \` EventSubscription1 \` para a assinatura padrão do Azure.</span><span class="sxs-lookup"><span data-stu-id="7372f-122">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="7372f-123">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="7372f-123">Example 4</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="7372f-124">Remove a assinatura de evento \` EventSubscription1 \` para um namespace de Hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="7372f-124">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="7372f-125">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="7372f-125">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="7372f-126">Remove a assinatura de evento \` EventSubscription1 \` para um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="7372f-126">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="7372f-127">OS</span><span class="sxs-lookup"><span data-stu-id="7372f-127">PARAMETERS</span></span>

### <span data-ttu-id="7372f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7372f-128">-DefaultProfile</span></span>
<span data-ttu-id="7372f-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7372f-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7372f-130">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="7372f-130">-DomainInputObject</span></span>
<span data-ttu-id="7372f-131">Objeto de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="7372f-131">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="7372f-132">-DomainName</span><span class="sxs-lookup"><span data-stu-id="7372f-132">-DomainName</span></span>
<span data-ttu-id="7372f-133">Nome de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="7372f-133">EventGrid domain name.</span></span>

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

### <span data-ttu-id="7372f-134">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="7372f-134">-DomainTopicInputObject</span></span>
<span data-ttu-id="7372f-135">Objeto de tópico do domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="7372f-135">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="7372f-136">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="7372f-136">-DomainTopicName</span></span>
<span data-ttu-id="7372f-137">Nome do tópico do domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="7372f-137">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="7372f-138">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="7372f-138">-EventSubscriptionName</span></span>
<span data-ttu-id="7372f-139">Nome da assinatura de evento que precisa ser removida.</span><span class="sxs-lookup"><span data-stu-id="7372f-139">Name of the event subscription that needs to be removed.</span></span>

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

### <span data-ttu-id="7372f-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7372f-140">-InputObject</span></span>
<span data-ttu-id="7372f-141">Objeto de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="7372f-141">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="7372f-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7372f-142">-PassThru</span></span>
<span data-ttu-id="7372f-143">Retorna o status da operação de remoção.</span><span class="sxs-lookup"><span data-stu-id="7372f-143">Returns the status of the Remove operation.</span></span> <span data-ttu-id="7372f-144">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="7372f-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7372f-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7372f-145">-ResourceGroupName</span></span>
<span data-ttu-id="7372f-146">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7372f-146">Resource Group Name.</span></span>

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

### <span data-ttu-id="7372f-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7372f-147">-ResourceId</span></span>
<span data-ttu-id="7372f-148">Identificador do recurso cuja assinatura de evento precisa ser removida.</span><span class="sxs-lookup"><span data-stu-id="7372f-148">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="7372f-149">-Topicname</span><span class="sxs-lookup"><span data-stu-id="7372f-149">-TopicName</span></span>
<span data-ttu-id="7372f-150">Nome do tópico da grade do evento.</span><span class="sxs-lookup"><span data-stu-id="7372f-150">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="7372f-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7372f-151">-Confirm</span></span>
<span data-ttu-id="7372f-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7372f-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7372f-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7372f-153">-WhatIf</span></span>
<span data-ttu-id="7372f-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7372f-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7372f-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7372f-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7372f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7372f-156">CommonParameters</span></span>
<span data-ttu-id="7372f-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7372f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7372f-158">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7372f-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7372f-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7372f-159">INPUTS</span></span>

### <span data-ttu-id="7372f-160">System. String</span><span class="sxs-lookup"><span data-stu-id="7372f-160">System.String</span></span>

### <span data-ttu-id="7372f-161">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="7372f-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="7372f-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="7372f-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="7372f-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="7372f-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="7372f-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7372f-164">OUTPUTS</span></span>

### <span data-ttu-id="7372f-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7372f-165">System.Boolean</span></span>

## <span data-ttu-id="7372f-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7372f-166">NOTES</span></span>

## <span data-ttu-id="7372f-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7372f-167">RELATED LINKS</span></span>
