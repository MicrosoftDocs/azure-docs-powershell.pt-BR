---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 4538bb39c085a2e7152a146d5e93e08a0c09f5de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427784"
---
# <span data-ttu-id="3271d-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="3271d-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="3271d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3271d-102">SYNOPSIS</span></span>
<span data-ttu-id="3271d-103">Cria uma fila de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="3271d-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3271d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3271d-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> -Name <String>
 -EnablePartitioning <Boolean> [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-EnableBatchedOperations <Boolean>] [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableExpress <Boolean>]
 [-IsAnonymousAccessible <Boolean>] [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>]
 [-MessageCount <Int64>] [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>]
 [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3271d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3271d-105">DESCRIPTION</span></span>
<span data-ttu-id="3271d-106">O cmdlet **New-AzureRmServiceBusQueue** cria uma fila de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="3271d-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="3271d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3271d-107">EXAMPLES</span></span>

### <span data-ttu-id="3271d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3271d-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -EnablePartitioning $True
```

<span data-ttu-id="3271d-109">Cria uma nova fila de barramento `SB-Queue_exampl1` de serviço no namespace de barramento de serviço especificado `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="3271d-109">Creates a new Service Bus queue `SB-Queue_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="3271d-110">OS</span><span class="sxs-lookup"><span data-stu-id="3271d-110">PARAMETERS</span></span>

### <span data-ttu-id="3271d-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="3271d-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="3271d-112">Especifica o intervalo de tempo ocioso de [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , após o qual a fila é excluída automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3271d-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="3271d-113">A duração mínima é de 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="3271d-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="3271d-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="3271d-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="3271d-115">Especifica se as mensagens são deadlettereddas na expiração.</span><span class="sxs-lookup"><span data-stu-id="3271d-115">Specifies whether messages are deadlettered on expiration.</span></span>

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

### <span data-ttu-id="3271d-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="3271d-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="3271d-117">Especifica o tempo de vida útil (TTL) da mensagem padrão.</span><span class="sxs-lookup"><span data-stu-id="3271d-117">Specifies the default message time-to-live (TTL).</span></span>

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

### <span data-ttu-id="3271d-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="3271d-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="3271d-119">Especifica a janela de tempo do histórico de detecção duplicada, um [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) Valuethat define a duração do histórico de detecção de duplicidades.</span><span class="sxs-lookup"><span data-stu-id="3271d-119">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="3271d-120">O valor padrão é 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="3271d-120">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="3271d-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="3271d-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="3271d-122">Especifica se as operações em lote do lado do servidor estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="3271d-122">Specifies whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="3271d-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="3271d-123">-EnableExpress</span></span>
<span data-ttu-id="3271d-124">Especifica se as entidades expressas estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="3271d-124">Specifies whether Express Entities are enabled.</span></span> <span data-ttu-id="3271d-125">Uma fila expressa armazena uma mensagem em memória temporariamente antes de gravá-la no armazenamento persistente.</span><span class="sxs-lookup"><span data-stu-id="3271d-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="3271d-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="3271d-126">-EnablePartitioning</span></span>
<span data-ttu-id="3271d-127">Especifica se o EnablePartitioning está habilitado.</span><span class="sxs-lookup"><span data-stu-id="3271d-127">Specifies whether EnablePartitioning is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3271d-128">-IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="3271d-128">-IsAnonymousAccessible</span></span>
<span data-ttu-id="3271d-129">Especifica se a mensagem está acessível anonimamente.</span><span class="sxs-lookup"><span data-stu-id="3271d-129">Specifies whether the message is anonymously accessible.</span></span>

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

### <span data-ttu-id="3271d-130">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="3271d-130">-LockDuration</span></span>
<span data-ttu-id="3271d-131">Especifica a duração do bloqueio.</span><span class="sxs-lookup"><span data-stu-id="3271d-131">Specifies the lock duration.</span></span>

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

### <span data-ttu-id="3271d-132">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="3271d-132">-MaxDeliveryCount</span></span>
<span data-ttu-id="3271d-133">Especifica o número máximo de entregas.</span><span class="sxs-lookup"><span data-stu-id="3271d-133">Specifies the maximum delivery count.</span></span> <span data-ttu-id="3271d-134">Uma mensagem será automaticamente deadletteredda após esse número de entregas.</span><span class="sxs-lookup"><span data-stu-id="3271d-134">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="3271d-135">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="3271d-135">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="3271d-136">Especifica o tamanho máximo da fila em megabytes, que é o tamanho da memória alocada para a fila.</span><span class="sxs-lookup"><span data-stu-id="3271d-136">Specifies the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

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

### <span data-ttu-id="3271d-137">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="3271d-137">-MessageCount</span></span>
<span data-ttu-id="3271d-138">Especifica o número de mensagens na fila.</span><span class="sxs-lookup"><span data-stu-id="3271d-138">Specifies the number of messages in the queue.</span></span>

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

### <span data-ttu-id="3271d-139">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="3271d-139">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="3271d-140">Especifica se a fila requer detecção de duplicidades.</span><span class="sxs-lookup"><span data-stu-id="3271d-140">Specifies whether the queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="3271d-141">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="3271d-141">-RequiresSession</span></span>
<span data-ttu-id="3271d-142">Especifica se essa fila oferece suporte a sessões.</span><span class="sxs-lookup"><span data-stu-id="3271d-142">Specifies whether this queue supports sessions.</span></span>

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

### <span data-ttu-id="3271d-143">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="3271d-143">-SizeInBytes</span></span>
<span data-ttu-id="3271d-144">O tamanho da fila em bytes.</span><span class="sxs-lookup"><span data-stu-id="3271d-144">The size of the queue in bytes.</span></span>

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

### <span data-ttu-id="3271d-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3271d-145">-Confirm</span></span>
<span data-ttu-id="3271d-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3271d-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3271d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3271d-147">-WhatIf</span></span>
<span data-ttu-id="3271d-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3271d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3271d-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3271d-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3271d-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3271d-150">-DefaultProfile</span></span>
<span data-ttu-id="3271d-151">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3271d-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3271d-152">-Nome</span><span class="sxs-lookup"><span data-stu-id="3271d-152">-Name</span></span>
<span data-ttu-id="3271d-153">Nome da fila.</span><span class="sxs-lookup"><span data-stu-id="3271d-153">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3271d-154">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3271d-154">-Namespace</span></span>
<span data-ttu-id="3271d-155">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="3271d-155">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3271d-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3271d-156">-ResourceGroupName</span></span>
<span data-ttu-id="3271d-157">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3271d-157">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3271d-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3271d-158">CommonParameters</span></span>
<span data-ttu-id="3271d-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3271d-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3271d-160">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3271d-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3271d-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3271d-161">INPUTS</span></span>

### <span data-ttu-id="3271d-162">-Resource</span><span class="sxs-lookup"><span data-stu-id="3271d-162">-ResourceGroup</span></span>
 <span data-ttu-id="3271d-163">System. String</span><span class="sxs-lookup"><span data-stu-id="3271d-163">System.String</span></span>

### <span data-ttu-id="3271d-164">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="3271d-164">-NamespaceName</span></span>
 <span data-ttu-id="3271d-165">System. String</span><span class="sxs-lookup"><span data-stu-id="3271d-165">System.String</span></span>

### <span data-ttu-id="3271d-166">-QueueName</span><span class="sxs-lookup"><span data-stu-id="3271d-166">-QueueName</span></span>
 <span data-ttu-id="3271d-167">System. String</span><span class="sxs-lookup"><span data-stu-id="3271d-167">System.String</span></span>

### <span data-ttu-id="3271d-168">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="3271d-168">-EnablePartitioning</span></span>
 <span data-ttu-id="3271d-169">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="3271d-169">System.Boolean?</span></span>

## <span data-ttu-id="3271d-170">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3271d-170">OUTPUTS</span></span>

### <span data-ttu-id="3271d-171">Microsoft. Azure. Commands. ServiceBus. Models. QueueAttributes</span><span class="sxs-lookup"><span data-stu-id="3271d-171">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>
<span data-ttu-id="3271d-172">Nome: SB-Queue_exampl1 local: West US LockDuration: AccessedAt: AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 2:51:36 AM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true DeadLetteringOnMessageExpiration: 16384 false EnableExpress: EnablePartitioning: IsAnonymousAccessible: false MaxDeliveryCount: false MaxSizeInMegabytes: status: active MessageCount: false CountDetails: RequiresDuplicateDetection: RequiresSession: false sizeInBytes: false SupportOrdering: status: ativo UpdatedAt: false: 1/20/2017 2:51:37</span><span class="sxs-lookup"><span data-stu-id="3271d-172">Name                                : SB-Queue_exampl1 Location                            : West US LockDuration                        : AccessedAt                          : AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 2:51:36 AM DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True DeadLetteringOnMessageExpiration    : False EnableExpress                       : False EnablePartitioning                  : True IsAnonymousAccessible               : False MaxDeliveryCount                    : MaxSizeInMegabytes                  : 16384 MessageCount                        : CountDetails                        : RequiresDuplicateDetection          : False RequiresSession                     : False SizeInBytes                         : Status                              : Active SupportOrdering                     : False UpdatedAt                           : 1/20/2017 2:51:37 AM</span></span>

## <span data-ttu-id="3271d-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3271d-173">NOTES</span></span>

## <span data-ttu-id="3271d-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3271d-174">RELATED LINKS</span></span>

