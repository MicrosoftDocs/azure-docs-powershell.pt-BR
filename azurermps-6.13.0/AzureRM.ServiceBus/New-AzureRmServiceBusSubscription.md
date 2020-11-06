---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
ms.openlocfilehash: b780af95efcb73d922e326550afd234a50d37929
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430866"
---
# <span data-ttu-id="33249-101">New-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="33249-101">New-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="33249-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33249-102">SYNOPSIS</span></span>
<span data-ttu-id="33249-103">Cria uma assinatura para o tópico de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="33249-103">Creates a subscription to the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33249-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33249-104">SYNTAX</span></span>

```
New-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33249-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="33249-105">DESCRIPTION</span></span>
<span data-ttu-id="33249-106">O cmdlet **New-AzureRmServiceBusSubscription** cria uma nova assinatura para o tópico de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="33249-106">The **New-AzureRmServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="33249-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33249-107">EXAMPLES</span></span>

### <span data-ttu-id="33249-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="33249-108">Example 1</span></span>
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

<span data-ttu-id="33249-109">Cria a assinatura `SB-TopicSubscription-Example1` para o tópico de barramento de serviço especificado `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="33249-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="33249-110">OS</span><span class="sxs-lookup"><span data-stu-id="33249-110">PARAMETERS</span></span>

### <span data-ttu-id="33249-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="33249-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="33249-112">Especifica o intervalo de tempo ocioso de [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , após o qual a assinatura é excluída automaticamente.</span><span class="sxs-lookup"><span data-stu-id="33249-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="33249-113">A duração mínima é de 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="33249-113">The minimum duration is 5 minutes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33249-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="33249-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="33249-115">Valor que indica se uma assinatura tem suporte para carta de inatividade em exceções de avaliação de filtro.</span><span class="sxs-lookup"><span data-stu-id="33249-115">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="33249-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="33249-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="33249-117">Carta inativa no vencimento da mensagem</span><span class="sxs-lookup"><span data-stu-id="33249-117">Dead Lettering On Message Expiration</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33249-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="33249-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="33249-119">Valor de TimeSpan para Live.</span><span class="sxs-lookup"><span data-stu-id="33249-119">Timespan to live value.</span></span>
<span data-ttu-id="33249-120">Essa é a duração após a qual a mensagem expira, a partir de quando a mensagem é enviada para o barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="33249-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="33249-121">Esse é o valor padrão usado quando TimeToLive não está definido na própria mensagem.</span><span class="sxs-lookup"><span data-stu-id="33249-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="33249-122">Para Standard = TimeSpan. Max e Basic = 14 Dyas</span><span class="sxs-lookup"><span data-stu-id="33249-122">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33249-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33249-123">-DefaultProfile</span></span>
<span data-ttu-id="33249-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="33249-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33249-125">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="33249-125">-EnableBatchedOperations</span></span>
<span data-ttu-id="33249-126">Habilitar operações em lote-valor que indica se as operações em lote do lado do servidor estão habilitadas</span><span class="sxs-lookup"><span data-stu-id="33249-126">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33249-127">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="33249-127">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="33249-128">Nome da fila/tópico para encaminhar a mensagem de inatividade</span><span class="sxs-lookup"><span data-stu-id="33249-128">Queue/Topic name to forward the Dead Letter message</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33249-129">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="33249-129">-ForwardTo</span></span>
<span data-ttu-id="33249-130">Nome da fila/tópico para encaminhar as mensagens</span><span class="sxs-lookup"><span data-stu-id="33249-130">Queue/Topic name to forward the messages</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33249-131">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="33249-131">-LockDuration</span></span>
<span data-ttu-id="33249-132">Duração do bloqueio</span><span class="sxs-lookup"><span data-stu-id="33249-132">Lock Duration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33249-133">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="33249-133">-MaxDeliveryCount</span></span>
<span data-ttu-id="33249-134">MaxDeliveryCount-a contagem máxima de entregas.</span><span class="sxs-lookup"><span data-stu-id="33249-134">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="33249-135">Uma mensagem será automaticamente deadletteredda após esse número de entregas.</span><span class="sxs-lookup"><span data-stu-id="33249-135">A message is automatically deadlettered after this number of deliveries.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33249-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="33249-136">-Name</span></span>
<span data-ttu-id="33249-137">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="33249-137">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33249-138">-Namespace</span><span class="sxs-lookup"><span data-stu-id="33249-138">-Namespace</span></span>
<span data-ttu-id="33249-139">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="33249-139">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33249-140">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="33249-140">-RequiresSession</span></span>
<span data-ttu-id="33249-141">RequiresSession-o valor que indica se essa fila requer detecção de duplicidades.</span><span class="sxs-lookup"><span data-stu-id="33249-141">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33249-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33249-142">-ResourceGroupName</span></span>
<span data-ttu-id="33249-143">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="33249-143">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33249-144">-Tópico</span><span class="sxs-lookup"><span data-stu-id="33249-144">-Topic</span></span>
<span data-ttu-id="33249-145">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="33249-145">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33249-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="33249-146">-Confirm</span></span>
<span data-ttu-id="33249-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33249-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33249-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33249-148">-WhatIf</span></span>
<span data-ttu-id="33249-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="33249-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33249-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="33249-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33249-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33249-151">CommonParameters</span></span>
<span data-ttu-id="33249-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33249-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33249-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33249-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33249-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="33249-154">INPUTS</span></span>

### <span data-ttu-id="33249-155">System. String</span><span class="sxs-lookup"><span data-stu-id="33249-155">System.String</span></span>

### <span data-ttu-id="33249-156">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="33249-156">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="33249-157">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="33249-157">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="33249-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="33249-158">OUTPUTS</span></span>

### <span data-ttu-id="33249-159">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="33249-159">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="33249-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="33249-160">NOTES</span></span>

## <span data-ttu-id="33249-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33249-161">RELATED LINKS</span></span>
