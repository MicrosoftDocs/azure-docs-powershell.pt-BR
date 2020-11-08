---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
ms.openlocfilehash: 16a7de817250170cf39a02200cee67c028249e1f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125319"
---
# <span data-ttu-id="17e76-101">New-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="17e76-101">New-AzServiceBusQueue</span></span>

## <span data-ttu-id="17e76-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="17e76-102">SYNOPSIS</span></span>
<span data-ttu-id="17e76-103">Cria uma fila de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="17e76-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="17e76-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17e76-104">SYNTAX</span></span>

```
New-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-EnablePartitioning <Boolean>] [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableBatchedOperations] [-EnableExpress <Boolean>]
 [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>] [-MessageCount <Int64>]
 [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>] [-SizeInBytes <Int64>]
 [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17e76-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="17e76-105">DESCRIPTION</span></span>
<span data-ttu-id="17e76-106">O cmdlet **New-AzServiceBusQueue** cria uma fila de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="17e76-106">The **New-AzServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="17e76-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17e76-107">EXAMPLES</span></span>

### <span data-ttu-id="17e76-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="17e76-108">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -EnablePartitioning $True

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

<span data-ttu-id="17e76-109">Cria uma nova fila de barramento `SB-Queue_example1` de serviço no namespace de barramento de serviço especificado `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="17e76-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="17e76-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="17e76-110">Example 2</span></span>

<span data-ttu-id="17e76-111">Cria uma fila de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="17e76-111">Creates a Service Bus queue in the specified Service Bus namespace.</span></span> <span data-ttu-id="17e76-112">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="17e76-112">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzServiceBusQueue -EnablePartitioning $true -MaxSizeInMegabytes <Int64> -Name SB-Queue_example1 -Namespace SB-Example1 -ResourceGroupName Default-ServiceBus-WestUS
```

## <span data-ttu-id="17e76-113">OS</span><span class="sxs-lookup"><span data-stu-id="17e76-113">PARAMETERS</span></span>

### <span data-ttu-id="17e76-114">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="17e76-114">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="17e76-115">Especifica o intervalo de tempo ocioso de [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , após o qual a fila é excluída automaticamente.</span><span class="sxs-lookup"><span data-stu-id="17e76-115">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="17e76-116">A duração mínima é de 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="17e76-116">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="17e76-117">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="17e76-117">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="17e76-118">Carta inativa no vencimento da mensagem</span><span class="sxs-lookup"><span data-stu-id="17e76-118">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="17e76-119">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="17e76-119">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="17e76-120">Valor de TimeSpan para Live.</span><span class="sxs-lookup"><span data-stu-id="17e76-120">Timespan to live value.</span></span>
<span data-ttu-id="17e76-121">Essa é a duração após a qual a mensagem expira, a partir de quando a mensagem é enviada para o barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="17e76-121">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="17e76-122">Esse é o valor padrão usado quando TimeToLive não está definido na própria mensagem.</span><span class="sxs-lookup"><span data-stu-id="17e76-122">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="17e76-123">Para Standard = TimeSpan. Max e Basic = 14 dias</span><span class="sxs-lookup"><span data-stu-id="17e76-123">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="17e76-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17e76-124">-DefaultProfile</span></span>
<span data-ttu-id="17e76-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17e76-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17e76-126">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="17e76-126">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="17e76-127">Especifica a janela de tempo do histórico de detecção duplicada, um valor [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) que define a duração do histórico de detecção de duplicidades.</span><span class="sxs-lookup"><span data-stu-id="17e76-127">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) value that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="17e76-128">O valor padrão é 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="17e76-128">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="17e76-129">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="17e76-129">-EnableBatchedOperations</span></span>
<span data-ttu-id="17e76-130">Habilitar operações em lote-valor que indica se as operações em lote do lado do servidor estão habilitadas</span><span class="sxs-lookup"><span data-stu-id="17e76-130">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="17e76-131">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="17e76-131">-EnableExpress</span></span>
<span data-ttu-id="17e76-132">EnableExpress-um valor que indica se as entidades expressas estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="17e76-132">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="17e76-133">Uma fila expressa armazena uma mensagem em memória temporariamente antes de gravá-la no armazenamento persistente.</span><span class="sxs-lookup"><span data-stu-id="17e76-133">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="17e76-134">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="17e76-134">-EnablePartitioning</span></span>
<span data-ttu-id="17e76-135">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="17e76-135">EnablePartitioning</span></span>

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

### <span data-ttu-id="17e76-136">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="17e76-136">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="17e76-137">Nome da fila/tópico para encaminhar a mensagem de inatividade</span><span class="sxs-lookup"><span data-stu-id="17e76-137">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="17e76-138">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="17e76-138">-ForwardTo</span></span>
<span data-ttu-id="17e76-139">Nome da fila/tópico para encaminhar as mensagens</span><span class="sxs-lookup"><span data-stu-id="17e76-139">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="17e76-140">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="17e76-140">-LockDuration</span></span>
<span data-ttu-id="17e76-141">Duração do bloqueio</span><span class="sxs-lookup"><span data-stu-id="17e76-141">Lock Duration</span></span>

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

### <span data-ttu-id="17e76-142">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="17e76-142">-MaxDeliveryCount</span></span>
<span data-ttu-id="17e76-143">MaxDeliveryCount-a contagem máxima de entregas.</span><span class="sxs-lookup"><span data-stu-id="17e76-143">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="17e76-144">Uma mensagem será automaticamente deadletteredda após esse número de entregas.</span><span class="sxs-lookup"><span data-stu-id="17e76-144">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="17e76-145">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="17e76-145">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="17e76-146">MaxSizeInMegabytes-o tamanho máximo da fila em megabytes, que é o tamanho da memória alocada para a fila. O padrão é 1024.</span><span class="sxs-lookup"><span data-stu-id="17e76-146">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.Default is 1024.</span></span> <span data-ttu-id="17e76-147">O máximo para SKU padrão é o 5120 e o SKU Premium é 81920, valores permitidos: 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span><span class="sxs-lookup"><span data-stu-id="17e76-147">Max for Standard SKU is 5120 and for Premium SKU is 81920, Allowed values : 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span></span>

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

### <span data-ttu-id="17e76-148">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="17e76-148">-MessageCount</span></span>
<span data-ttu-id="17e76-149">MessageCount-o número de mensagens na fila</span><span class="sxs-lookup"><span data-stu-id="17e76-149">MessageCount - the number of messages in the queue</span></span>

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

### <span data-ttu-id="17e76-150">-Nome</span><span class="sxs-lookup"><span data-stu-id="17e76-150">-Name</span></span>
<span data-ttu-id="17e76-151">Nome da fila</span><span class="sxs-lookup"><span data-stu-id="17e76-151">Queue Name</span></span>

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

### <span data-ttu-id="17e76-152">-Namespace</span><span class="sxs-lookup"><span data-stu-id="17e76-152">-Namespace</span></span>
<span data-ttu-id="17e76-153">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="17e76-153">Namespace Name</span></span>

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

### <span data-ttu-id="17e76-154">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="17e76-154">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="17e76-155">RequiresDuplicateDetection-um valor que indica se a fila dá suporte ao conceito de sessão</span><span class="sxs-lookup"><span data-stu-id="17e76-155">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

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

### <span data-ttu-id="17e76-156">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="17e76-156">-RequiresSession</span></span>
<span data-ttu-id="17e76-157">RequiresSession-o valor que indica se essa fila usa sessões</span><span class="sxs-lookup"><span data-stu-id="17e76-157">RequiresSession - the value indicating if this queue uses sessions</span></span>

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

### <span data-ttu-id="17e76-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17e76-158">-ResourceGroupName</span></span>
<span data-ttu-id="17e76-159">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="17e76-159">The name of the resource group</span></span>

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

### <span data-ttu-id="17e76-160">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="17e76-160">-SizeInBytes</span></span>
<span data-ttu-id="17e76-161">SizeInBytes-o tamanho da fila em bytes</span><span class="sxs-lookup"><span data-stu-id="17e76-161">SizeInBytes - the size of the queue in bytes</span></span>

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

### <span data-ttu-id="17e76-162">-Confirme</span><span class="sxs-lookup"><span data-stu-id="17e76-162">-Confirm</span></span>
<span data-ttu-id="17e76-163">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17e76-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17e76-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17e76-164">-WhatIf</span></span>
<span data-ttu-id="17e76-165">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="17e76-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17e76-166">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="17e76-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17e76-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17e76-167">CommonParameters</span></span>
<span data-ttu-id="17e76-168">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17e76-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17e76-169">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17e76-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17e76-170">SENSORES</span><span class="sxs-lookup"><span data-stu-id="17e76-170">INPUTS</span></span>

### <span data-ttu-id="17e76-171">System. String</span><span class="sxs-lookup"><span data-stu-id="17e76-171">System.String</span></span>

### <span data-ttu-id="17e76-172">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="17e76-172">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="17e76-173">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="17e76-173">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="17e76-174">System. Nullable ' 1 [[System. Int64, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="17e76-174">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="17e76-175">EXIBE</span><span class="sxs-lookup"><span data-stu-id="17e76-175">OUTPUTS</span></span>

### <span data-ttu-id="17e76-176">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="17e76-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="17e76-177">INFORMA</span><span class="sxs-lookup"><span data-stu-id="17e76-177">NOTES</span></span>

## <span data-ttu-id="17e76-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17e76-178">RELATED LINKS</span></span>
