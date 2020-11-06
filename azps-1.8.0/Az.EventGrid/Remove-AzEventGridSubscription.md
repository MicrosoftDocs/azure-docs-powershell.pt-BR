---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: fd872830f82f1d75f0b3c5f60ba6b129d7edd6f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600866"
---
# <span data-ttu-id="44324-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="44324-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="44324-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44324-102">SYNOPSIS</span></span>
<span data-ttu-id="44324-103">Remove uma assinatura de evento de grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="44324-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="44324-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44324-104">SYNTAX</span></span>

### <span data-ttu-id="44324-105">ResourceGroupNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="44324-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44324-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="44324-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44324-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44324-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44324-108">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="44324-108">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44324-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44324-109">DESCRIPTION</span></span>
<span data-ttu-id="44324-110">Remove uma assinatura de evento de grade de eventos do Azure para um tópico de grade de eventos do Azure, um recurso, uma assinatura do Azure ou um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="44324-110">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="44324-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44324-111">EXAMPLES</span></span>

### <span data-ttu-id="44324-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="44324-112">Example 1</span></span>
```
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="44324-113">Remove a assinatura de evento \` EventSubscription1 \` para um tópico de Tópico1 de grade de eventos do Azure \` \` no MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="44324-113">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="44324-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="44324-114">Example 2</span></span>
```
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="44324-115">Remove a assinatura de evento \` EventSubscription1 \` a um grupo de MyResourceGroupName de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="44324-115">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="44324-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="44324-116">Example 3</span></span>
```
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="44324-117">Remove a assinatura de evento \` EventSubscription1 \` para a assinatura padrão do Azure.</span><span class="sxs-lookup"><span data-stu-id="44324-117">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="44324-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="44324-118">Example 4</span></span>
```
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="44324-119">Remove a assinatura de evento \` EventSubscription1 \` para um namespace de Hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="44324-119">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="44324-120">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="44324-120">Example 5</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="44324-121">Remove a assinatura de evento \` EventSubscription1 \` para um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="44324-121">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="44324-122">OS</span><span class="sxs-lookup"><span data-stu-id="44324-122">PARAMETERS</span></span>

### <span data-ttu-id="44324-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44324-123">-DefaultProfile</span></span>
<span data-ttu-id="44324-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="44324-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44324-125">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="44324-125">-EventSubscriptionName</span></span>
<span data-ttu-id="44324-126">Nome da assinatura de evento que precisa ser removida.</span><span class="sxs-lookup"><span data-stu-id="44324-126">Name of the event subscription that needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44324-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44324-127">-InputObject</span></span>
<span data-ttu-id="44324-128">Objeto de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="44324-128">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="44324-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44324-129">-PassThru</span></span>
<span data-ttu-id="44324-130">Retorna o status da operação de remoção.</span><span class="sxs-lookup"><span data-stu-id="44324-130">Returns the status of the Remove operation.</span></span> <span data-ttu-id="44324-131">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="44324-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="44324-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44324-132">-ResourceGroupName</span></span>
<span data-ttu-id="44324-133">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="44324-133">Resource Group Name.</span></span>

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
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44324-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44324-134">-ResourceId</span></span>
<span data-ttu-id="44324-135">Identificador do recurso cuja assinatura de evento precisa ser removida.</span><span class="sxs-lookup"><span data-stu-id="44324-135">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="44324-136">-Topicname</span><span class="sxs-lookup"><span data-stu-id="44324-136">-TopicName</span></span>
<span data-ttu-id="44324-137">Nome do tópico da grade do evento.</span><span class="sxs-lookup"><span data-stu-id="44324-137">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="44324-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="44324-138">-Confirm</span></span>
<span data-ttu-id="44324-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44324-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44324-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44324-140">-WhatIf</span></span>
<span data-ttu-id="44324-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="44324-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44324-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44324-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44324-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44324-143">CommonParameters</span></span>
<span data-ttu-id="44324-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44324-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44324-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44324-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44324-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44324-146">INPUTS</span></span>

### <span data-ttu-id="44324-147">System. String</span><span class="sxs-lookup"><span data-stu-id="44324-147">System.String</span></span>

### <span data-ttu-id="44324-148">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="44324-148">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="44324-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44324-149">OUTPUTS</span></span>

### <span data-ttu-id="44324-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="44324-150">System.Boolean</span></span>

## <span data-ttu-id="44324-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44324-151">NOTES</span></span>

## <span data-ttu-id="44324-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44324-152">RELATED LINKS</span></span>
