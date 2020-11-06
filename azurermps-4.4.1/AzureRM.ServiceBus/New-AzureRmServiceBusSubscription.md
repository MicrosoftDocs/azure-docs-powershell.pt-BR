---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
ms.openlocfilehash: ea305b334e6efd4cb1c5af47db2a1b8817e7cab6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430627"
---
# <span data-ttu-id="6cc77-101">New-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="6cc77-101">New-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="6cc77-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6cc77-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc77-103">Cria uma assinatura para o tópico de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="6cc77-103">Creates a subscription to the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cc77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6cc77-104">SYNTAX</span></span>

```
New-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -Name <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnFilterEvaluationExceptions <Boolean>] [-DeadLetteringOnMessageExpiration <Boolean>]
 [-EnableBatchedOperations <Boolean>] [-IsReadOnly <Boolean>] [-LockDuration <String>]
 [-MaxDeliveryCount <Int32>] [-RequiresSession <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cc77-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6cc77-105">DESCRIPTION</span></span>
<span data-ttu-id="6cc77-106">O cmdlet **New-AzureRmServiceBusSubscription** cria uma nova assinatura para o tópico de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="6cc77-106">The **New-AzureRmServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="6cc77-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6cc77-107">EXAMPLES</span></span>

### <span data-ttu-id="6cc77-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6cc77-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="6cc77-109">Cria a assinatura `SB-TopicSubscription-Example1` para o tópico de barramento de serviço especificado `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="6cc77-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="6cc77-110">OS</span><span class="sxs-lookup"><span data-stu-id="6cc77-110">PARAMETERS</span></span>

### <span data-ttu-id="6cc77-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="6cc77-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="6cc77-112">Especifica o intervalo de tempo ocioso de [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , após o qual a assinatura é excluída automaticamente.</span><span class="sxs-lookup"><span data-stu-id="6cc77-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="6cc77-113">A duração mínima é de 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="6cc77-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="6cc77-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="6cc77-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="6cc77-115">Indica se uma assinatura tem suporte para carta de inatividade em exceções de avaliação de filtro.</span><span class="sxs-lookup"><span data-stu-id="6cc77-115">Indicates if a subscription has dead letter support on Filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="6cc77-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="6cc77-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="6cc77-117">Indica se uma assinatura tem suporte a mensagens mortas quando uma mensagem expira.</span><span class="sxs-lookup"><span data-stu-id="6cc77-117">Indicates if a subscription has deadletter support when a message expires.</span></span>

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

### <span data-ttu-id="6cc77-118">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="6cc77-118">-EnableBatchedOperations</span></span>
<span data-ttu-id="6cc77-119">Indica se as operações em lote do lado do servidor estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="6cc77-119">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="6cc77-120">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="6cc77-120">-IsReadOnly</span></span>
<span data-ttu-id="6cc77-121">Indica se a descrição da entidade é somente leitura</span><span class="sxs-lookup"><span data-stu-id="6cc77-121">Indicates whether the entity description is read-only</span></span>

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

### <span data-ttu-id="6cc77-122">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="6cc77-122">-LockDuration</span></span>
<span data-ttu-id="6cc77-123">Especifica o período de tempo da duração do bloqueio para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="6cc77-123">Specifies the lock duration time span for the subscription.</span></span>

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

### <span data-ttu-id="6cc77-124">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="6cc77-124">-MaxDeliveryCount</span></span>
<span data-ttu-id="6cc77-125">Especifica o número máximo de entregas.</span><span class="sxs-lookup"><span data-stu-id="6cc77-125">Specifies the number of maximum deliveries.</span></span> <span data-ttu-id="6cc77-126">Uma mensagem será automaticamente deadletteredda após esse número de entregas.</span><span class="sxs-lookup"><span data-stu-id="6cc77-126">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="6cc77-127">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="6cc77-127">-RequiresSession</span></span>
<span data-ttu-id="6cc77-128">Especifica se uma assinatura dá suporte ao conceito de sessões.</span><span class="sxs-lookup"><span data-stu-id="6cc77-128">Specifies whether a subscription supports the concept of sessions.</span></span>

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

### <span data-ttu-id="6cc77-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6cc77-129">-Confirm</span></span>
<span data-ttu-id="6cc77-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cc77-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cc77-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cc77-131">-WhatIf</span></span>
<span data-ttu-id="6cc77-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6cc77-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cc77-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6cc77-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cc77-134">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="6cc77-134">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="6cc77-135">Valor de TimeSpan para Live.</span><span class="sxs-lookup"><span data-stu-id="6cc77-135">Timespan to live value.</span></span> <span data-ttu-id="6cc77-136">Essa é a duração após a qual a mensagem expira, a partir de quando a mensagem é enviada para o barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="6cc77-136">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span> <span data-ttu-id="6cc77-137">Esse é o valor padrão usado quando TimeToLive não está definido na própria mensagem.</span><span class="sxs-lookup"><span data-stu-id="6cc77-137">This is the default value used when TimeToLive is not set on a message itself.</span></span> <span data-ttu-id="6cc77-138">Para Standard = TimeSpan. Max e Basic = 14 Dyas</span><span class="sxs-lookup"><span data-stu-id="6cc77-138">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="6cc77-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cc77-139">-DefaultProfile</span></span>
<span data-ttu-id="6cc77-140">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6cc77-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cc77-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="6cc77-141">-Name</span></span>
<span data-ttu-id="6cc77-142">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="6cc77-142">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc77-143">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6cc77-143">-Namespace</span></span>
<span data-ttu-id="6cc77-144">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="6cc77-144">Namespace Name.</span></span>

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

### <span data-ttu-id="6cc77-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cc77-145">-ResourceGroupName</span></span>
<span data-ttu-id="6cc77-146">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6cc77-146">The name of the resource group</span></span>

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

### <span data-ttu-id="6cc77-147">-Tópico</span><span class="sxs-lookup"><span data-stu-id="6cc77-147">-Topic</span></span>
<span data-ttu-id="6cc77-148">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="6cc77-148">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc77-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc77-149">CommonParameters</span></span>
<span data-ttu-id="6cc77-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cc77-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc77-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cc77-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc77-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6cc77-152">INPUTS</span></span>

### <span data-ttu-id="6cc77-153">-Resource</span><span class="sxs-lookup"><span data-stu-id="6cc77-153">-ResourceGroup</span></span>
 <span data-ttu-id="6cc77-154">System. String</span><span class="sxs-lookup"><span data-stu-id="6cc77-154">System.String</span></span>
 

### <span data-ttu-id="6cc77-155">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="6cc77-155">-NamespaceName</span></span>
 <span data-ttu-id="6cc77-156">System. String</span><span class="sxs-lookup"><span data-stu-id="6cc77-156">System.String</span></span>
 

### <span data-ttu-id="6cc77-157">-Topicname</span><span class="sxs-lookup"><span data-stu-id="6cc77-157">-TopicName</span></span>
 <span data-ttu-id="6cc77-158">System. String</span><span class="sxs-lookup"><span data-stu-id="6cc77-158">System.String</span></span>
 

### <span data-ttu-id="6cc77-159">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="6cc77-159">-SubscriptionName</span></span>
 <span data-ttu-id="6cc77-160">System. String</span><span class="sxs-lookup"><span data-stu-id="6cc77-160">System.String</span></span>

## <span data-ttu-id="6cc77-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6cc77-161">OUTPUTS</span></span>

### <span data-ttu-id="6cc77-162">Microsoft. Azure. Commands. ServiceBus. Models. Subscriptionattributes</span><span class="sxs-lookup"><span data-stu-id="6cc77-162">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="6cc77-163">Nome: SB-TopicSubscription-example1 local: West US AccessedAt: 1/20/2017 3:18:54 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 CountDetails: Microsoft. Azure. Management. ServiceBus. Models. MessageCountDetails CreatedAt: 1/20/2017 3:18:52 AM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions: true DeadLetteringOnMessageExpiration: 10 EnableBatchedOperations: 0 EntityAvailabilityStatus: false status: LockDuration: 00:01:00 MaxDeliveryCount: 10 MessageCount: 0 RequiresSession: false status: de UpdatedAt: 1/20/2017 3:18:54</span><span class="sxs-lookup"><span data-stu-id="6cc77-163">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails CreatedAt                                 : 1/20/2017 3:18:52 AM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : False EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 10 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 3:18:54 AM</span></span>

## <span data-ttu-id="6cc77-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6cc77-164">NOTES</span></span>

## <span data-ttu-id="6cc77-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6cc77-165">RELATED LINKS</span></span>

