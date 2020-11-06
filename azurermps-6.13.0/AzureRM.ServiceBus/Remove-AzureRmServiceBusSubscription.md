---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
ms.openlocfilehash: b8b2b9f6bb8a082647a14285a907465e8e12348f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430863"
---
# <span data-ttu-id="11ddd-101">Remove-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="11ddd-101">Remove-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="11ddd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="11ddd-103">Remove a assinatura de um tópico do namespace especificado de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="11ddd-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11ddd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11ddd-104">SYNTAX</span></span>

### <span data-ttu-id="11ddd-105">SubscriptionPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="11ddd-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11ddd-106">SubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="11ddd-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzureRmServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11ddd-107">SubscriptionResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="11ddd-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzureRmServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11ddd-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="11ddd-108">DESCRIPTION</span></span>
<span data-ttu-id="11ddd-109">O cmdlet **Remove-AzureRmServiceBusSubscription** remove a assinatura de um tópico do namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="11ddd-109">The **Remove-AzureRmServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="11ddd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11ddd-110">EXAMPLES</span></span>

### <span data-ttu-id="11ddd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="11ddd-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="11ddd-112">Remove a assinatura do `SB-TopicSubscription-Example1` tópico `SB-Topic_exampl1` no namespace de barramento de serviço especificado `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="11ddd-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="11ddd-113">Exemplo 2,1-InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="11ddd-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusSubscription <params>
PS C:\> Remove-AzureRmServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="11ddd-114">Exemplo 2,2-InputObject-usando o encanamento:</span><span class="sxs-lookup"><span data-stu-id="11ddd-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\>Get-AzureRmServiceBusSubscription <params> |Remove-AzureRmServiceBusSubscription
```

### <span data-ttu-id="11ddd-115">Exemplo 3,1-ResourceId-usando variável:</span><span class="sxs-lookup"><span data-stu-id="11ddd-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzureRmServiceBusSubscription <params>
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="11ddd-116">Exemplo 3,2-ResourceId-usando valor de cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="11ddd-116">Example 3.2 - ResourceId - Using string value:</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="11ddd-117">Remove a assinatura fornecida por meio da ID do ARM no parâmetro $resourceid/String para-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11ddd-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="11ddd-118">OS</span><span class="sxs-lookup"><span data-stu-id="11ddd-118">PARAMETERS</span></span>

### <span data-ttu-id="11ddd-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11ddd-119">-AsJob</span></span>
<span data-ttu-id="11ddd-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="11ddd-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11ddd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11ddd-121">-DefaultProfile</span></span>
<span data-ttu-id="11ddd-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11ddd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11ddd-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11ddd-123">-InputObject</span></span>
<span data-ttu-id="11ddd-124">Objeto de assinatura do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="11ddd-124">Service Bus Subscription Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: SubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11ddd-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="11ddd-125">-Name</span></span>
<span data-ttu-id="11ddd-126">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="11ddd-126">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ddd-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="11ddd-127">-Namespace</span></span>
<span data-ttu-id="11ddd-128">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="11ddd-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ddd-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11ddd-129">-PassThru</span></span>
<span data-ttu-id="11ddd-130">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="11ddd-130">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="11ddd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11ddd-131">-ResourceGroupName</span></span>
<span data-ttu-id="11ddd-132">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="11ddd-132">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ddd-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11ddd-133">-ResourceId</span></span>
<span data-ttu-id="11ddd-134">ID do recurso de assinatura do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="11ddd-134">Service Bus Subscription Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ddd-135">-Tópico</span><span class="sxs-lookup"><span data-stu-id="11ddd-135">-Topic</span></span>
<span data-ttu-id="11ddd-136">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="11ddd-136">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ddd-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="11ddd-137">-Confirm</span></span>
<span data-ttu-id="11ddd-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11ddd-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11ddd-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11ddd-139">-WhatIf</span></span>
<span data-ttu-id="11ddd-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="11ddd-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11ddd-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="11ddd-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11ddd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11ddd-142">CommonParameters</span></span>
<span data-ttu-id="11ddd-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11ddd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11ddd-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11ddd-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11ddd-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="11ddd-145">INPUTS</span></span>

### <span data-ttu-id="11ddd-146">System. String</span><span class="sxs-lookup"><span data-stu-id="11ddd-146">System.String</span></span>

### <span data-ttu-id="11ddd-147">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="11ddd-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>
<span data-ttu-id="11ddd-148">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="11ddd-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="11ddd-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="11ddd-149">OUTPUTS</span></span>

### <span data-ttu-id="11ddd-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="11ddd-150">System.Boolean</span></span>

## <span data-ttu-id="11ddd-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="11ddd-151">NOTES</span></span>

## <span data-ttu-id="11ddd-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11ddd-152">RELATED LINKS</span></span>
