---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 54753001be0a754cf9416e1b2ec53fd81647d8d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603217"
---
# <span data-ttu-id="b707b-101">New-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="b707b-101">New-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="b707b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b707b-102">SYNOPSIS</span></span>
<span data-ttu-id="b707b-103">Cria uma assinatura para o tópico de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="b707b-103">Creates a subscription to the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b707b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b707b-104">SYNTAX</span></span>

```
New-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b707b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b707b-105">DESCRIPTION</span></span>
<span data-ttu-id="b707b-106">O cmdlet **New-AzureRmServiceBusSubscription** cria uma nova assinatura para o tópico de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="b707b-106">The **New-AzureRmServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="b707b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b707b-107">EXAMPLES</span></span>

### <span data-ttu-id="b707b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b707b-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
CreatedAt                                 : 1/20/2017 3:18:52 AM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : False
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 10
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 3:18:54 AM
```
<span data-ttu-id="b707b-109">Cria a assinatura `SB-TopicSubscription-Example1` para o tópico de barramento de serviço especificado `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="b707b-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="b707b-110">OS</span><span class="sxs-lookup"><span data-stu-id="b707b-110">PARAMETERS</span></span>

### <span data-ttu-id="b707b-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="b707b-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="b707b-112">Especifica o intervalo de tempo ocioso de [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , após o qual a assinatura é excluída automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b707b-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="b707b-113">A duração mínima é de 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="b707b-113">The minimum duration is 5 minutes.</span></span>


```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b707b-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b707b-114">-Confirm</span></span>
<span data-ttu-id="b707b-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b707b-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b707b-116">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="b707b-116">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="b707b-117">Valor que indica se uma assinatura tem suporte para carta de inatividade em exceções de avaliação de filtro.</span><span class="sxs-lookup"><span data-stu-id="b707b-117">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="b707b-118">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="b707b-118">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="b707b-119">Carta inativa no vencimento da mensagem</span><span class="sxs-lookup"><span data-stu-id="b707b-119">Dead Lettering On Message Expiration</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b707b-120">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="b707b-120">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="b707b-121">Valor de TimeSpan para Live.</span><span class="sxs-lookup"><span data-stu-id="b707b-121">Timespan to live value.</span></span>
<span data-ttu-id="b707b-122">Essa é a duração após a qual a mensagem expira, a partir de quando a mensagem é enviada para o barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="b707b-122">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="b707b-123">Esse é o valor padrão usado quando TimeToLive não está definido na própria mensagem.</span><span class="sxs-lookup"><span data-stu-id="b707b-123">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="b707b-124">Para Standard = TimeSpan. Max e Basic = 14 Dyas</span><span class="sxs-lookup"><span data-stu-id="b707b-124">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b707b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b707b-125">-DefaultProfile</span></span>
<span data-ttu-id="b707b-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b707b-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b707b-127">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="b707b-127">-EnableBatchedOperations</span></span>
<span data-ttu-id="b707b-128">Habilitar operações em lote-valor que indica se as operações em lote do lado do servidor estão habilitadas</span><span class="sxs-lookup"><span data-stu-id="b707b-128">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b707b-129">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="b707b-129">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="b707b-130">Nome da fila/tópico para encaminhar a mensagem de inatividade</span><span class="sxs-lookup"><span data-stu-id="b707b-130">Queue/Topic name to forward the Dead Letter message</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b707b-131">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="b707b-131">-ForwardTo</span></span>
<span data-ttu-id="b707b-132">Nome da fila/tópico para encaminhar as mensagens</span><span class="sxs-lookup"><span data-stu-id="b707b-132">Queue/Topic name to forward the messages</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b707b-133">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="b707b-133">-LockDuration</span></span>
<span data-ttu-id="b707b-134">Duração do bloqueio</span><span class="sxs-lookup"><span data-stu-id="b707b-134">Lock Duration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b707b-135">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="b707b-135">-MaxDeliveryCount</span></span>
<span data-ttu-id="b707b-136">MaxDeliveryCount-a contagem máxima de entregas.</span><span class="sxs-lookup"><span data-stu-id="b707b-136">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="b707b-137">Uma mensagem será automaticamente deadletteredda após esse número de entregas.</span><span class="sxs-lookup"><span data-stu-id="b707b-137">A message is automatically deadlettered after this number of deliveries.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b707b-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="b707b-138">-Name</span></span>
<span data-ttu-id="b707b-139">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="b707b-139">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b707b-140">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b707b-140">-Namespace</span></span>
<span data-ttu-id="b707b-141">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="b707b-141">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b707b-142">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="b707b-142">-RequiresSession</span></span>
<span data-ttu-id="b707b-143">RequiresSession-o valor que indica se essa fila requer detecção de duplicidades.</span><span class="sxs-lookup"><span data-stu-id="b707b-143">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b707b-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b707b-144">-ResourceGroupName</span></span>
<span data-ttu-id="b707b-145">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b707b-145">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b707b-146">-Tópico</span><span class="sxs-lookup"><span data-stu-id="b707b-146">-Topic</span></span>
<span data-ttu-id="b707b-147">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="b707b-147">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b707b-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b707b-148">-WhatIf</span></span>
<span data-ttu-id="b707b-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b707b-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b707b-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b707b-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b707b-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b707b-151">CommonParameters</span></span>
<span data-ttu-id="b707b-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b707b-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b707b-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b707b-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b707b-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b707b-154">INPUTS</span></span>

### <span data-ttu-id="b707b-155">-Resource</span><span class="sxs-lookup"><span data-stu-id="b707b-155">-ResourceGroup</span></span>
 <span data-ttu-id="b707b-156">System. String</span><span class="sxs-lookup"><span data-stu-id="b707b-156">System.String</span></span>
 

### <span data-ttu-id="b707b-157">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b707b-157">-NamespaceName</span></span>
 <span data-ttu-id="b707b-158">System. String</span><span class="sxs-lookup"><span data-stu-id="b707b-158">System.String</span></span>
 

### <span data-ttu-id="b707b-159">-Topicname</span><span class="sxs-lookup"><span data-stu-id="b707b-159">-TopicName</span></span>
 <span data-ttu-id="b707b-160">System. String</span><span class="sxs-lookup"><span data-stu-id="b707b-160">System.String</span></span>
 

### <span data-ttu-id="b707b-161">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="b707b-161">-SubscriptionName</span></span>
 <span data-ttu-id="b707b-162">System. String</span><span class="sxs-lookup"><span data-stu-id="b707b-162">System.String</span></span>


## <span data-ttu-id="b707b-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b707b-163">OUTPUTS</span></span>

### <span data-ttu-id="b707b-164">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="b707b-164">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>


## <span data-ttu-id="b707b-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b707b-165">NOTES</span></span>

## <span data-ttu-id="b707b-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b707b-166">RELATED LINKS</span></span>
