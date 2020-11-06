---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
ms.openlocfilehash: 0369d6bac19d2d2180c54f3c4244101df3a7bb42
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599156"
---
# <span data-ttu-id="65508-101">Remove-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="65508-101">Remove-AzServiceBusSubscription</span></span>

## <span data-ttu-id="65508-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65508-102">SYNOPSIS</span></span>
<span data-ttu-id="65508-103">Remove a assinatura de um tópico do namespace especificado de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="65508-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="65508-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65508-104">SYNTAX</span></span>

### <span data-ttu-id="65508-105">SubscriptionPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="65508-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65508-106">SubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="65508-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65508-107">SubscriptionResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="65508-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65508-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="65508-108">DESCRIPTION</span></span>
<span data-ttu-id="65508-109">O cmdlet **Remove-AzServiceBusSubscription** remove a assinatura de um tópico do namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="65508-109">The **Remove-AzServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="65508-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65508-110">EXAMPLES</span></span>

### <span data-ttu-id="65508-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="65508-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="65508-112">Remove a assinatura do `SB-TopicSubscription-Example1` tópico `SB-Topic_exampl1` no namespace de barramento de serviço especificado `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="65508-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="65508-113">Exemplo 2,1-InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="65508-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="65508-114">Exemplo 2,2-InputObject-usando o encanamento:</span><span class="sxs-lookup"><span data-stu-id="65508-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\>Get-AzServiceBusSubscription <params> |Remove-AzServiceBusSubscription
```

### <span data-ttu-id="65508-115">Exemplo 3,1-ResourceId-usando variável:</span><span class="sxs-lookup"><span data-stu-id="65508-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="65508-116">Exemplo 3,2-ResourceId-usando valor de cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="65508-116">Example 3.2 - ResourceId - Using string value:</span></span>
```
PS C:\> Remove-AzServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="65508-117">Remove a assinatura fornecida por meio da ID do ARM no parâmetro $resourceid/String para-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65508-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="65508-118">OS</span><span class="sxs-lookup"><span data-stu-id="65508-118">PARAMETERS</span></span>

### <span data-ttu-id="65508-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65508-119">-AsJob</span></span>
<span data-ttu-id="65508-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="65508-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65508-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65508-121">-DefaultProfile</span></span>
<span data-ttu-id="65508-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="65508-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65508-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65508-123">-InputObject</span></span>
<span data-ttu-id="65508-124">Objeto de assinatura do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="65508-124">Service Bus Subscription Object</span></span>

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

### <span data-ttu-id="65508-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="65508-125">-Name</span></span>
<span data-ttu-id="65508-126">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="65508-126">Subscription Name</span></span>

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

### <span data-ttu-id="65508-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="65508-127">-Namespace</span></span>
<span data-ttu-id="65508-128">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="65508-128">Namespace Name</span></span>

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

### <span data-ttu-id="65508-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65508-129">-PassThru</span></span>
<span data-ttu-id="65508-130">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="65508-130">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="65508-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65508-131">-ResourceGroupName</span></span>
<span data-ttu-id="65508-132">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="65508-132">The name of the resource group</span></span>

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

### <span data-ttu-id="65508-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65508-133">-ResourceId</span></span>
<span data-ttu-id="65508-134">ID do recurso de assinatura do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="65508-134">Service Bus Subscription Resource Id</span></span>

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

### <span data-ttu-id="65508-135">-Tópico</span><span class="sxs-lookup"><span data-stu-id="65508-135">-Topic</span></span>
<span data-ttu-id="65508-136">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="65508-136">Topic Name</span></span>

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

### <span data-ttu-id="65508-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="65508-137">-Confirm</span></span>
<span data-ttu-id="65508-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65508-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65508-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65508-139">-WhatIf</span></span>
<span data-ttu-id="65508-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="65508-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65508-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="65508-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65508-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65508-142">CommonParameters</span></span>
<span data-ttu-id="65508-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65508-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65508-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65508-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65508-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="65508-145">INPUTS</span></span>

### <span data-ttu-id="65508-146">System. String</span><span class="sxs-lookup"><span data-stu-id="65508-146">System.String</span></span>

### <span data-ttu-id="65508-147">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="65508-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="65508-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="65508-148">OUTPUTS</span></span>

### <span data-ttu-id="65508-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="65508-149">System.Boolean</span></span>

## <span data-ttu-id="65508-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="65508-150">NOTES</span></span>

## <span data-ttu-id="65508-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65508-151">RELATED LINKS</span></span>
