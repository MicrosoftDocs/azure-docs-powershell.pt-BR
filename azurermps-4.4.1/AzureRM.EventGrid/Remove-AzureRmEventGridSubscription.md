---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
ms.openlocfilehash: a15cb222108d79544d38ce730897e03fa61066ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441106"
---
# <span data-ttu-id="538ab-101">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="538ab-101">Remove-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="538ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="538ab-102">SYNOPSIS</span></span>
<span data-ttu-id="538ab-103">Remove uma assinatura de evento de grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="538ab-103">Removes an Azure Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="538ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="538ab-104">SYNTAX</span></span>

### <span data-ttu-id="538ab-105">ResourceGroupNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="538ab-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="538ab-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="538ab-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="538ab-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="538ab-107">EventSubscriptionInputObjectSet</span></span>
```
Remove-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="538ab-108">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="538ab-108">TopicNameParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="538ab-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="538ab-109">DESCRIPTION</span></span>
<span data-ttu-id="538ab-110">Remove uma assinatura de evento de grade de eventos do Azure para um tópico de grade de eventos do Azure, um recurso, uma assinatura do Azure ou um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="538ab-110">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="538ab-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="538ab-111">EXAMPLES</span></span>

### <span data-ttu-id="538ab-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="538ab-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="538ab-113">Remove a assinatura de evento \` EventSubscription1 \` para um tópico de Tópico1 de grade de eventos do Azure \` \` no MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="538ab-113">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="538ab-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="538ab-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="538ab-115">Remove a assinatura de evento \` EventSubscription1 \` a um grupo de MyResourceGroupName de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="538ab-115">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="538ab-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="538ab-116">Example 3</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="538ab-117">Remove a assinatura de evento \` EventSubscription1 \` para a assinatura padrão do Azure.</span><span class="sxs-lookup"><span data-stu-id="538ab-117">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="538ab-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="538ab-118">Example 4</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="538ab-119">Remove a assinatura de evento \` EventSubscription1 \` para um namespace de Hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="538ab-119">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="538ab-120">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="538ab-120">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="538ab-121">Remove a assinatura de evento \` EventSubscription1 \` para um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="538ab-121">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="538ab-122">OS</span><span class="sxs-lookup"><span data-stu-id="538ab-122">PARAMETERS</span></span>

### <span data-ttu-id="538ab-123">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="538ab-123">-EventSubscriptionName</span></span>
<span data-ttu-id="538ab-124">Nome da assinatura de evento que precisa ser removida.</span><span class="sxs-lookup"><span data-stu-id="538ab-124">Name of the event subscription that needs to be removed.</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="538ab-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="538ab-125">-InputObject</span></span>
<span data-ttu-id="538ab-126">Objeto EventSubscription EventGrid.</span><span class="sxs-lookup"><span data-stu-id="538ab-126">EventGrid EventSubscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="538ab-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="538ab-127">-PassThru</span></span>
<span data-ttu-id="538ab-128">Retorna o status da operação de remoção.</span><span class="sxs-lookup"><span data-stu-id="538ab-128">Returns the status of the Remove operation.</span></span> <span data-ttu-id="538ab-129">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="538ab-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="538ab-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="538ab-130">-ResourceGroupName</span></span>
<span data-ttu-id="538ab-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="538ab-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="538ab-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="538ab-132">-ResourceId</span></span>
<span data-ttu-id="538ab-133">Identificador do recurso cuja assinatura de evento precisa ser removida.</span><span class="sxs-lookup"><span data-stu-id="538ab-133">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="538ab-134">-Topicname</span><span class="sxs-lookup"><span data-stu-id="538ab-134">-TopicName</span></span>
<span data-ttu-id="538ab-135">Nome do tópico da grade do evento.</span><span class="sxs-lookup"><span data-stu-id="538ab-135">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="538ab-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="538ab-136">-Confirm</span></span>
<span data-ttu-id="538ab-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="538ab-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="538ab-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="538ab-138">-WhatIf</span></span>
<span data-ttu-id="538ab-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="538ab-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="538ab-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="538ab-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="538ab-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="538ab-141">-DefaultProfile</span></span>
<span data-ttu-id="538ab-142">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="538ab-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="538ab-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="538ab-143">CommonParameters</span></span>
<span data-ttu-id="538ab-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="538ab-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="538ab-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="538ab-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="538ab-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="538ab-146">INPUTS</span></span>

### <span data-ttu-id="538ab-147">System. String</span><span class="sxs-lookup"><span data-stu-id="538ab-147">System.String</span></span>
<span data-ttu-id="538ab-148">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="538ab-148">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="538ab-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="538ab-149">OUTPUTS</span></span>

### <span data-ttu-id="538ab-150">System. Object</span><span class="sxs-lookup"><span data-stu-id="538ab-150">System.Object</span></span>

## <span data-ttu-id="538ab-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="538ab-151">NOTES</span></span>

## <span data-ttu-id="538ab-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="538ab-152">RELATED LINKS</span></span>

