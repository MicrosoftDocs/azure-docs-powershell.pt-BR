---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 29e2c0f04dff07e76907ee67c3e012c2b67c1582
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431898"
---
# <span data-ttu-id="7b6e2-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="7b6e2-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="7b6e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b6e2-102">SYNOPSIS</span></span>
<span data-ttu-id="7b6e2-103">Cria uma fila de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="7b6e2-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b6e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b6e2-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-EnablePartitioning <Boolean>] [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableBatchedOperations] [-EnableExpress <Boolean>]
 [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>] [-MessageCount <Int64>]
 [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>] [-SizeInBytes <Int64>]
 [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b6e2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7b6e2-105">DESCRIPTION</span></span>
<span data-ttu-id="7b6e2-106">O cmdlet **New-AzureRmServiceBusQueue** cria uma fila de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="7b6e2-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="7b6e2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b6e2-107">EXAMPLES</span></span>

### <span data-ttu-id="7b6e2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7b6e2-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -EnablePartitioning $True

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_example1
Name                                : SB-Queue_example1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 12:37:11 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : False
MaxDeliveryCount                    : 10
MaxSizeInMegabytes                  : 81920
MessageCount                        : 0
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 0
Status                              : Active
UpdatedAt                           : 10/11/2018 12:37:12 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="7b6e2-109">Cria uma nova fila de barramento `SB-Queue_example1` de serviço no namespace de barramento de serviço especificado `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="7b6e2-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="7b6e2-110">OS</span><span class="sxs-lookup"><span data-stu-id="7b6e2-110">PARAMETERS</span></span>

### <span data-ttu-id="7b6e2-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="7b6e2-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="7b6e2-112">Especifica o intervalo de tempo ocioso de [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , após o qual a fila é excluída automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7b6e2-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="7b6e2-113">A duração mínima é de 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="7b6e2-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="7b6e2-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="7b6e2-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="7b6e2-115">Carta inativa no vencimento da mensagem</span><span class="sxs-lookup"><span data-stu-id="7b6e2-115">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="7b6e2-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="7b6e2-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="7b6e2-117">Valor de TimeSpan para Live.</span><span class="sxs-lookup"><span data-stu-id="7b6e2-117">Timespan to live value.</span></span>
<span data-ttu-id="7b6e2-118">Essa é a duração após a qual a mensagem expira, a partir de quando a mensagem é enviada para o barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="7b6e2-118">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="7b6e2-119">Esse é o valor padrão usado quando TimeToLive não está definido na própria mensagem.</span><span class="sxs-lookup"><span data-stu-id="7b6e2-119">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="7b6e2-120">Para Standard = TimeSpan. Max e Basic = 14 Dyas</span><span class="sxs-lookup"><span data-stu-id="7b6e2-120">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="7b6e2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b6e2-121">-DefaultProfile</span></span>
<span data-ttu-id="7b6e2-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7b6e2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b6e2-123">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="7b6e2-123">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="7b6e2-124">Especifica a janela de tempo do histórico de detecção duplicada, um [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) Valuethat define a duração do histórico de detecção de duplicidades.</span><span class="sxs-lookup"><span data-stu-id="7b6e2-124">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="7b6e2-125">O valor padrão é 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="7b6e2-125">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="7b6e2-126">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="7b6e2-126">-EnableBatchedOperations</span></span>
<span data-ttu-id="7b6e2-127">Habilitar operações em lote-valor que indica se as operações em lote do lado do servidor estão habilitadas</span><span class="sxs-lookup"><span data-stu-id="7b6e2-127">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="7b6e2-128">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="7b6e2-128">-EnableExpress</span></span>
<span data-ttu-id="7b6e2-129">EnableExpress-um valor que indica se as entidades expressas estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="7b6e2-129">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="7b6e2-130">Uma fila expressa armazena uma mensagem em memória temporariamente antes de gravá-la no armazenamento persistente.</span><span class="sxs-lookup"><span data-stu-id="7b6e2-130">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="7b6e2-131">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="7b6e2-131">-EnablePartitioning</span></span>
<span data-ttu-id="7b6e2-132">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="7b6e2-132">EnablePartitioning</span></span>

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

### <span data-ttu-id="7b6e2-133">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="7b6e2-133">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="7b6e2-134">Nome da fila/tópico para encaminhar a mensagem de inatividade</span><span class="sxs-lookup"><span data-stu-id="7b6e2-134">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="7b6e2-135">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="7b6e2-135">-ForwardTo</span></span>
<span data-ttu-id="7b6e2-136">Nome da fila/tópico para encaminhar as mensagens</span><span class="sxs-lookup"><span data-stu-id="7b6e2-136">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="7b6e2-137">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="7b6e2-137">-LockDuration</span></span>
<span data-ttu-id="7b6e2-138">Duração do bloqueio</span><span class="sxs-lookup"><span data-stu-id="7b6e2-138">Lock Duration</span></span>

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

### <span data-ttu-id="7b6e2-139">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="7b6e2-139">-MaxDeliveryCount</span></span>
<span data-ttu-id="7b6e2-140">MaxDeliveryCount-a contagem máxima de entregas.</span><span class="sxs-lookup"><span data-stu-id="7b6e2-140">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="7b6e2-141">Uma mensagem será automaticamente deadletteredda após esse número de entregas.</span><span class="sxs-lookup"><span data-stu-id="7b6e2-141">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="7b6e2-142">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="7b6e2-142">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="7b6e2-143">MaxSizeInMegabytes-o tamanho máximo da fila em megabytes, que é o tamanho da memória alocada para a fila.</span><span class="sxs-lookup"><span data-stu-id="7b6e2-143">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b6e2-144">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="7b6e2-144">-MessageCount</span></span>
<span data-ttu-id="7b6e2-145">MessageCount-o número de mensagens na fila</span><span class="sxs-lookup"><span data-stu-id="7b6e2-145">MessageCount - the number of messages in the queue</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b6e2-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b6e2-146">-Name</span></span>
<span data-ttu-id="7b6e2-147">Nome da fila</span><span class="sxs-lookup"><span data-stu-id="7b6e2-147">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b6e2-148">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7b6e2-148">-Namespace</span></span>
<span data-ttu-id="7b6e2-149">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="7b6e2-149">Namespace Name</span></span>

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

### <span data-ttu-id="7b6e2-150">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="7b6e2-150">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="7b6e2-151">RequiresDuplicateDetection-um valor que indica se a fila dá suporte ao conceito de sessão</span><span class="sxs-lookup"><span data-stu-id="7b6e2-151">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

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

### <span data-ttu-id="7b6e2-152">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="7b6e2-152">-RequiresSession</span></span>
<span data-ttu-id="7b6e2-153">RequiresSession-o valor que indica se essa fila requer detecção de duplicidades</span><span class="sxs-lookup"><span data-stu-id="7b6e2-153">RequiresSession - the value indicating if this queue requires duplicate detection</span></span>

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

### <span data-ttu-id="7b6e2-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b6e2-154">-ResourceGroupName</span></span>
<span data-ttu-id="7b6e2-155">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7b6e2-155">The name of the resource group</span></span>

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

### <span data-ttu-id="7b6e2-156">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="7b6e2-156">-SizeInBytes</span></span>
<span data-ttu-id="7b6e2-157">SizeInBytes-o tamanho da fila em bytes</span><span class="sxs-lookup"><span data-stu-id="7b6e2-157">SizeInBytes - the size of the queue in bytes</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b6e2-158">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7b6e2-158">-Confirm</span></span>
<span data-ttu-id="7b6e2-159">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b6e2-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b6e2-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b6e2-160">-WhatIf</span></span>
<span data-ttu-id="7b6e2-161">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7b6e2-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b6e2-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7b6e2-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b6e2-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b6e2-163">CommonParameters</span></span>
<span data-ttu-id="7b6e2-164">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b6e2-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b6e2-165">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b6e2-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b6e2-166">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7b6e2-166">INPUTS</span></span>

### <span data-ttu-id="7b6e2-167">System. String</span><span class="sxs-lookup"><span data-stu-id="7b6e2-167">System.String</span></span>

### <span data-ttu-id="7b6e2-168">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7b6e2-168">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7b6e2-169">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7b6e2-169">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7b6e2-170">System. Nullable ' 1 [[System. Int64, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7b6e2-170">System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="7b6e2-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7b6e2-171">OUTPUTS</span></span>

### <span data-ttu-id="7b6e2-172">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="7b6e2-172">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="7b6e2-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7b6e2-173">NOTES</span></span>

## <span data-ttu-id="7b6e2-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b6e2-174">RELATED LINKS</span></span>