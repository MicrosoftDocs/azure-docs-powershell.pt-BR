---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
ms.openlocfilehash: 1d197683e1459173d96958199ad08b437d1d9e04
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891624"
---
# <span data-ttu-id="23480-101">New-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="23480-101">New-AzServiceBusQueue</span></span>

## <span data-ttu-id="23480-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23480-102">SYNOPSIS</span></span>
<span data-ttu-id="23480-103">Cria uma fila de Barramento de Serviço no namespace de Barramento de Serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="23480-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="23480-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="23480-104">SYNTAX</span></span>

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

## <span data-ttu-id="23480-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="23480-105">DESCRIPTION</span></span>
<span data-ttu-id="23480-106">O cmdlet **New-AzServiceBusQueue** cria uma fila de Barramento de Serviço no namespace de Barramento de Serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="23480-106">The **New-AzServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="23480-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23480-107">EXAMPLES</span></span>

### <span data-ttu-id="23480-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="23480-108">Example 1</span></span>
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

<span data-ttu-id="23480-109">Cria uma nova fila de Barramento de `SB-Queue_example1` Serviço no namespace de Barramento de Serviço `SB-Example1` especificado.</span><span class="sxs-lookup"><span data-stu-id="23480-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="23480-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="23480-110">Example 2</span></span>

<span data-ttu-id="23480-111">Cria uma fila de Barramento de Serviço no namespace de Barramento de Serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="23480-111">Creates a Service Bus queue in the specified Service Bus namespace.</span></span> <span data-ttu-id="23480-112">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="23480-112">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzServiceBusQueue -EnablePartitioning $true -MaxSizeInMegabytes <Int64> -Name SB-Queue_example1 -Namespace SB-Example1 -ResourceGroupName Default-ServiceBus-WestUS
```

## <span data-ttu-id="23480-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="23480-113">PARAMETERS</span></span>

### <span data-ttu-id="23480-114">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="23480-114">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="23480-115">Especifica o intervalo [ocioso TimeSpan,](https://msdn.microsoft.com/library/system.timespan.aspx) após o qual a fila é excluída automaticamente.</span><span class="sxs-lookup"><span data-stu-id="23480-115">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="23480-116">A duração mínima é de 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="23480-116">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="23480-117">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="23480-117">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="23480-118">Texto morto na expiração da mensagem</span><span class="sxs-lookup"><span data-stu-id="23480-118">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="23480-119">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="23480-119">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="23480-120">Timespan como valor de vida.</span><span class="sxs-lookup"><span data-stu-id="23480-120">Timespan to live value.</span></span>
<span data-ttu-id="23480-121">Esta é a duração após a qual a mensagem expira, começando a partir de quando a mensagem é enviada para o Barramento de Serviço.</span><span class="sxs-lookup"><span data-stu-id="23480-121">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="23480-122">Esse é o valor padrão usado quando TimeToLive não é definido em uma mensagem em si.</span><span class="sxs-lookup"><span data-stu-id="23480-122">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="23480-123">Para Standard = Timespan.Max e Basic = 14 dias</span><span class="sxs-lookup"><span data-stu-id="23480-123">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="23480-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23480-124">-DefaultProfile</span></span>
<span data-ttu-id="23480-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23480-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23480-126">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="23480-126">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="23480-127">Especifica a janela de tempo do histórico de detecção duplicado, um [valor TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) que define a duração do histórico de detecção duplicado.</span><span class="sxs-lookup"><span data-stu-id="23480-127">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) value that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="23480-128">O valor padrão é 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="23480-128">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="23480-129">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="23480-129">-EnableBatchedOperations</span></span>
<span data-ttu-id="23480-130">Habilitar operações em lotes - valor que indica se as operações em lotes do lado do servidor estão habilitadas</span><span class="sxs-lookup"><span data-stu-id="23480-130">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="23480-131">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="23480-131">-EnableExpress</span></span>
<span data-ttu-id="23480-132">EnableExpress - um valor que indica se As Entidades Expressas estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="23480-132">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="23480-133">Uma fila expressa mantém uma mensagem na memória temporariamente antes de escrevê-la no armazenamento persistente.</span><span class="sxs-lookup"><span data-stu-id="23480-133">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="23480-134">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="23480-134">-EnablePartitioning</span></span>
<span data-ttu-id="23480-135">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="23480-135">EnablePartitioning</span></span>

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

### <span data-ttu-id="23480-136">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="23480-136">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="23480-137">Nome da fila/tópico para encaminhar a mensagem Carta Morta</span><span class="sxs-lookup"><span data-stu-id="23480-137">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="23480-138">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="23480-138">-ForwardTo</span></span>
<span data-ttu-id="23480-139">Nome da fila/tópico para encaminhar as mensagens</span><span class="sxs-lookup"><span data-stu-id="23480-139">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="23480-140">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="23480-140">-LockDuration</span></span>
<span data-ttu-id="23480-141">Duração do bloqueio</span><span class="sxs-lookup"><span data-stu-id="23480-141">Lock Duration</span></span>

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

### <span data-ttu-id="23480-142">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="23480-142">-MaxDeliveryCount</span></span>
<span data-ttu-id="23480-143">MaxDeliveryCount - a contagem máxima de entrega.</span><span class="sxs-lookup"><span data-stu-id="23480-143">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="23480-144">Uma mensagem é automaticamente morta após esse número de entregas.</span><span class="sxs-lookup"><span data-stu-id="23480-144">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="23480-145">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="23480-145">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="23480-146">MaxSizeInMegabytes - o tamanho máximo da fila em megabytes, que é o tamanho da memória alocada para a fila. O padrão é 1024.</span><span class="sxs-lookup"><span data-stu-id="23480-146">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.Default is 1024.</span></span> <span data-ttu-id="23480-147">Max para SKU padrão é 5120 e para SKU Premium é 81920, valores permitidos : 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span><span class="sxs-lookup"><span data-stu-id="23480-147">Max for Standard SKU is 5120 and for Premium SKU is 81920, Allowed values : 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span></span>

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

### <span data-ttu-id="23480-148">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="23480-148">-MessageCount</span></span>
<span data-ttu-id="23480-149">MessageCount - o número de mensagens na fila</span><span class="sxs-lookup"><span data-stu-id="23480-149">MessageCount - the number of messages in the queue</span></span>

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

### <span data-ttu-id="23480-150">-Name</span><span class="sxs-lookup"><span data-stu-id="23480-150">-Name</span></span>
<span data-ttu-id="23480-151">Nome da Fila</span><span class="sxs-lookup"><span data-stu-id="23480-151">Queue Name</span></span>

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

### <span data-ttu-id="23480-152">-Namespace</span><span class="sxs-lookup"><span data-stu-id="23480-152">-Namespace</span></span>
<span data-ttu-id="23480-153">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="23480-153">Namespace Name</span></span>

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

### <span data-ttu-id="23480-154">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="23480-154">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="23480-155">RequiresDuplicateDetection - um valor que indica se a fila dá suporte ao conceito de sessão</span><span class="sxs-lookup"><span data-stu-id="23480-155">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

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

### <span data-ttu-id="23480-156">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="23480-156">-RequiresSession</span></span>
<span data-ttu-id="23480-157">RequiresSession - o valor que indica se essa fila usa sessões</span><span class="sxs-lookup"><span data-stu-id="23480-157">RequiresSession - the value indicating if this queue uses sessions</span></span>

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

### <span data-ttu-id="23480-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23480-158">-ResourceGroupName</span></span>
<span data-ttu-id="23480-159">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="23480-159">The name of the resource group</span></span>

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

### <span data-ttu-id="23480-160">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="23480-160">-SizeInBytes</span></span>
<span data-ttu-id="23480-161">SizeInBytes - o tamanho da fila em bytes</span><span class="sxs-lookup"><span data-stu-id="23480-161">SizeInBytes - the size of the queue in bytes</span></span>

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

### <span data-ttu-id="23480-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23480-162">-Confirm</span></span>
<span data-ttu-id="23480-163">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23480-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23480-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23480-164">-WhatIf</span></span>
<span data-ttu-id="23480-165">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="23480-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23480-166">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="23480-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23480-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23480-167">CommonParameters</span></span>
<span data-ttu-id="23480-168">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23480-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23480-169">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23480-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23480-170">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23480-170">INPUTS</span></span>

### <span data-ttu-id="23480-171">System.String</span><span class="sxs-lookup"><span data-stu-id="23480-171">System.String</span></span>

### <span data-ttu-id="23480-172">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="23480-172">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="23480-173">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="23480-173">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="23480-174">System.Nullable'1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="23480-174">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="23480-175">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="23480-175">OUTPUTS</span></span>

### <span data-ttu-id="23480-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="23480-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="23480-177">NOTES</span><span class="sxs-lookup"><span data-stu-id="23480-177">NOTES</span></span>

## <span data-ttu-id="23480-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23480-178">RELATED LINKS</span></span>
