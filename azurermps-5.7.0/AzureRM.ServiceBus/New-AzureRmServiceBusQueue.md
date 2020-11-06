---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 8e1b1cd39e30bcbe2ccc9f46b5ab39511e4de58f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603218"
---
# <span data-ttu-id="2e6a9-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="2e6a9-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="2e6a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e6a9-102">SYNOPSIS</span></span>
<span data-ttu-id="2e6a9-103">Cria uma fila de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="2e6a9-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e6a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e6a9-104">SYNTAX</span></span>

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

## <span data-ttu-id="2e6a9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e6a9-105">DESCRIPTION</span></span>
<span data-ttu-id="2e6a9-106">O cmdlet **New-AzureRmServiceBusQueue** cria uma fila de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="2e6a9-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="2e6a9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e6a9-107">EXAMPLES</span></span>

### <span data-ttu-id="2e6a9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2e6a9-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -EnablePartitioning $True

Name                                : SB-Queue_exampl1
LockDuration                        : 
AccessedAt                          : 
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:36 AM
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : True
MaxDeliveryCount                    : 
MaxSizeInMegabytes                  : 16384
MessageCount                        : 
CountDetails                        : 
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 
Status                              : Active
UpdatedAt                           : 1/20/2017 2:51:37 AM
```
<span data-ttu-id="2e6a9-109">Cria uma nova fila de barramento `SB-Queue_exampl1` de serviço no namespace de barramento de serviço especificado `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="2e6a9-109">Creates a new Service Bus queue `SB-Queue_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="2e6a9-110">OS</span><span class="sxs-lookup"><span data-stu-id="2e6a9-110">PARAMETERS</span></span>

### <span data-ttu-id="2e6a9-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="2e6a9-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="2e6a9-112">Especifica o intervalo de tempo ocioso de [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , após o qual a fila é excluída automaticamente.</span><span class="sxs-lookup"><span data-stu-id="2e6a9-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="2e6a9-113">A duração mínima é de 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="2e6a9-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="2e6a9-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2e6a9-114">-Confirm</span></span>
<span data-ttu-id="2e6a9-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e6a9-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e6a9-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="2e6a9-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="2e6a9-117">Carta inativa no vencimento da mensagem</span><span class="sxs-lookup"><span data-stu-id="2e6a9-117">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="2e6a9-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="2e6a9-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="2e6a9-119">Valor de TimeSpan para Live.</span><span class="sxs-lookup"><span data-stu-id="2e6a9-119">Timespan to live value.</span></span>
<span data-ttu-id="2e6a9-120">Essa é a duração após a qual a mensagem expira, a partir de quando a mensagem é enviada para o barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="2e6a9-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="2e6a9-121">Esse é o valor padrão usado quando TimeToLive não está definido na própria mensagem.</span><span class="sxs-lookup"><span data-stu-id="2e6a9-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="2e6a9-122">Para Standard = TimeSpan. Max e Basic = 14 Dyas</span><span class="sxs-lookup"><span data-stu-id="2e6a9-122">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="2e6a9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e6a9-123">-DefaultProfile</span></span>
<span data-ttu-id="2e6a9-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e6a9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e6a9-125">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="2e6a9-125">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="2e6a9-126">Especifica a janela de tempo do histórico de detecção duplicada, um [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) Valuethat define a duração do histórico de detecção de duplicidades.</span><span class="sxs-lookup"><span data-stu-id="2e6a9-126">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="2e6a9-127">O valor padrão é 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="2e6a9-127">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="2e6a9-128">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="2e6a9-128">-EnableBatchedOperations</span></span>
<span data-ttu-id="2e6a9-129">Habilitar operações em lote-valor que indica se as operações em lote do lado do servidor estão habilitadas</span><span class="sxs-lookup"><span data-stu-id="2e6a9-129">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="2e6a9-130">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="2e6a9-130">-EnableExpress</span></span>
<span data-ttu-id="2e6a9-131">EnableExpress-um valor que indica se as entidades expressas estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="2e6a9-131">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="2e6a9-132">Uma fila expressa armazena uma mensagem em memória temporariamente antes de gravá-la no armazenamento persistente.</span><span class="sxs-lookup"><span data-stu-id="2e6a9-132">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="2e6a9-133">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="2e6a9-133">-EnablePartitioning</span></span>
<span data-ttu-id="2e6a9-134">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="2e6a9-134">EnablePartitioning</span></span>

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

### <span data-ttu-id="2e6a9-135">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="2e6a9-135">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="2e6a9-136">Nome da fila/tópico para encaminhar a mensagem de inatividade</span><span class="sxs-lookup"><span data-stu-id="2e6a9-136">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="2e6a9-137">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="2e6a9-137">-ForwardTo</span></span>
<span data-ttu-id="2e6a9-138">Nome da fila/tópico para encaminhar as mensagens</span><span class="sxs-lookup"><span data-stu-id="2e6a9-138">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="2e6a9-139">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="2e6a9-139">-LockDuration</span></span>
<span data-ttu-id="2e6a9-140">Duração do bloqueio</span><span class="sxs-lookup"><span data-stu-id="2e6a9-140">Lock Duration</span></span>

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

### <span data-ttu-id="2e6a9-141">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="2e6a9-141">-MaxDeliveryCount</span></span>
<span data-ttu-id="2e6a9-142">MaxDeliveryCount-a contagem máxima de entregas.</span><span class="sxs-lookup"><span data-stu-id="2e6a9-142">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="2e6a9-143">Uma mensagem será automaticamente deadletteredda após esse número de entregas.</span><span class="sxs-lookup"><span data-stu-id="2e6a9-143">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="2e6a9-144">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="2e6a9-144">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="2e6a9-145">MaxSizeInMegabytes-o tamanho máximo da fila em megabytes, que é o tamanho da memória alocada para a fila.</span><span class="sxs-lookup"><span data-stu-id="2e6a9-145">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6a9-146">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="2e6a9-146">-MessageCount</span></span>
<span data-ttu-id="2e6a9-147">MessageCount-o número de mensagens na fila</span><span class="sxs-lookup"><span data-stu-id="2e6a9-147">MessageCount - the number of messages in the queue</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6a9-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e6a9-148">-Name</span></span>
<span data-ttu-id="2e6a9-149">Nome da fila</span><span class="sxs-lookup"><span data-stu-id="2e6a9-149">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6a9-150">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2e6a9-150">-Namespace</span></span>
<span data-ttu-id="2e6a9-151">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="2e6a9-151">Namespace Name</span></span>

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

### <span data-ttu-id="2e6a9-152">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="2e6a9-152">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="2e6a9-153">RequiresDuplicateDetection-um valor que indica se a fila dá suporte ao conceito de sessão</span><span class="sxs-lookup"><span data-stu-id="2e6a9-153">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

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

### <span data-ttu-id="2e6a9-154">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="2e6a9-154">-RequiresSession</span></span>
<span data-ttu-id="2e6a9-155">RequiresSession-o valor que indica se essa fila requer detecção de duplicidades</span><span class="sxs-lookup"><span data-stu-id="2e6a9-155">RequiresSession - the value indicating if this queue requires duplicate detection</span></span>

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

### <span data-ttu-id="2e6a9-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e6a9-156">-ResourceGroupName</span></span>
<span data-ttu-id="2e6a9-157">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2e6a9-157">The name of the resource group</span></span>

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

### <span data-ttu-id="2e6a9-158">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="2e6a9-158">-SizeInBytes</span></span>
<span data-ttu-id="2e6a9-159">SizeInBytes-o tamanho da fila em bytes</span><span class="sxs-lookup"><span data-stu-id="2e6a9-159">SizeInBytes - the size of the queue in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6a9-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e6a9-160">-WhatIf</span></span>
<span data-ttu-id="2e6a9-161">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2e6a9-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e6a9-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2e6a9-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e6a9-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e6a9-163">CommonParameters</span></span>
<span data-ttu-id="2e6a9-164">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e6a9-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2e6a9-165">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e6a9-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e6a9-166">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e6a9-166">INPUTS</span></span>

### <span data-ttu-id="2e6a9-167">-Resource</span><span class="sxs-lookup"><span data-stu-id="2e6a9-167">-ResourceGroup</span></span>
 <span data-ttu-id="2e6a9-168">System. String</span><span class="sxs-lookup"><span data-stu-id="2e6a9-168">System.String</span></span>

### <span data-ttu-id="2e6a9-169">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="2e6a9-169">-NamespaceName</span></span>
 <span data-ttu-id="2e6a9-170">System. String</span><span class="sxs-lookup"><span data-stu-id="2e6a9-170">System.String</span></span>

### <span data-ttu-id="2e6a9-171">-QueueName</span><span class="sxs-lookup"><span data-stu-id="2e6a9-171">-QueueName</span></span>
 <span data-ttu-id="2e6a9-172">System. String</span><span class="sxs-lookup"><span data-stu-id="2e6a9-172">System.String</span></span>

### <span data-ttu-id="2e6a9-173">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="2e6a9-173">-EnablePartitioning</span></span>
 <span data-ttu-id="2e6a9-174">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="2e6a9-174">System.Boolean?</span></span>


## <span data-ttu-id="2e6a9-175">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e6a9-175">OUTPUTS</span></span>

### <span data-ttu-id="2e6a9-176">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="2e6a9-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>


## <span data-ttu-id="2e6a9-177">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e6a9-177">NOTES</span></span>

## <span data-ttu-id="2e6a9-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e6a9-178">RELATED LINKS</span></span>
