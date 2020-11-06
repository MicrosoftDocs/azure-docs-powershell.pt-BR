---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
ms.openlocfilehash: 099088bb560606990baa4f1774d8f46c5f68f04b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429117"
---
# <span data-ttu-id="abde0-101">New-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="abde0-101">New-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="abde0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="abde0-102">SYNOPSIS</span></span>
<span data-ttu-id="abde0-103">Cria um novo tópico de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="abde0-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abde0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="abde0-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> -Name <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-EnableSubscriptionPartitioning <Boolean>]
 [-FilteringMessagesBeforePublishing <Boolean>] [-IsAnonymousAccessible <Boolean>] [-IsExpress <Boolean>]
 [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>] [-SupportOrdering <Boolean>]
 [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abde0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="abde0-105">DESCRIPTION</span></span>
<span data-ttu-id="abde0-106">O cmdlet **New-AzureRmServiceBusTopic** cria um novo tópico de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="abde0-106">The **New-AzureRmServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="abde0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="abde0-107">EXAMPLES</span></span>

### <span data-ttu-id="abde0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="abde0-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True
```

<span data-ttu-id="abde0-109">Cria um novo tópico de barramento `SB-Topic_exampl1` de serviço no namespace de barramento de serviço especificado `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="abde0-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="abde0-110">OS</span><span class="sxs-lookup"><span data-stu-id="abde0-110">PARAMETERS</span></span>

### <span data-ttu-id="abde0-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="abde0-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="abde0-112">Especifica o intervalo de tempo ocioso de [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) após o qual o tópico é excluído automaticamente.</span><span class="sxs-lookup"><span data-stu-id="abde0-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="abde0-113">A duração mínima é de 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="abde0-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="abde0-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="abde0-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="abde0-115">Especifica a duração após a qual a mensagem expira, a partir de quando a mensagem é enviada para o barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="abde0-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

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

### <span data-ttu-id="abde0-116">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="abde0-116">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="abde0-117">Especifica a estrutura [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) que define a duração do histórico de detecção de duplicidades.</span><span class="sxs-lookup"><span data-stu-id="abde0-117">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="abde0-118">O valor padrão é 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="abde0-118">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="abde0-119">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="abde0-119">-EnableBatchedOperations</span></span>
<span data-ttu-id="abde0-120">Indica se as operações em lote do lado do servidor estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="abde0-120">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="abde0-121">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="abde0-121">-EnableExpress</span></span>
<span data-ttu-id="abde0-122">Indica se as entidades expressas estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="abde0-122">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="abde0-123">Uma fila expressa armazena uma mensagem em memória temporariamente antes de gravá-la no armazenamento persistente.</span><span class="sxs-lookup"><span data-stu-id="abde0-123">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="abde0-124">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="abde0-124">-EnablePartitioning</span></span>
<span data-ttu-id="abde0-125">Especifica se o tópico deve ser habilitado para ser particionado em vários agentes de mensagem.</span><span class="sxs-lookup"><span data-stu-id="abde0-125">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

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

### <span data-ttu-id="abde0-126">-EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="abde0-126">-EnableSubscriptionPartitioning</span></span>
<span data-ttu-id="abde0-127">Especifica se o particionamento de assinatura deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="abde0-127">Specifies whether to enable subscription partitioning.</span></span>

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

### <span data-ttu-id="abde0-128">-FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="abde0-128">-FilteringMessagesBeforePublishing</span></span>
<span data-ttu-id="abde0-129">Indica se a filtragem está habilitada para mensagens antes da publicação.</span><span class="sxs-lookup"><span data-stu-id="abde0-129">Indicates whether filtering is enabled for messages before publishing.</span></span>

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

### <span data-ttu-id="abde0-130">-IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="abde0-130">-IsAnonymousAccessible</span></span>
<span data-ttu-id="abde0-131">Indica se a mensagem permite acesso anônimo.</span><span class="sxs-lookup"><span data-stu-id="abde0-131">Indicates whether the message allows anonymous access.</span></span>

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

### <span data-ttu-id="abde0-132">-Isexpress</span><span class="sxs-lookup"><span data-stu-id="abde0-132">-IsExpress</span></span>
<span data-ttu-id="abde0-133">Indica se o tópico está Express habilitado.</span><span class="sxs-lookup"><span data-stu-id="abde0-133">Indicates whether the topic is express enabled.</span></span>

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

### <span data-ttu-id="abde0-134">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="abde0-134">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="abde0-135">O tamanho máximo do tópico em megabytes, que é o tamanho da memória alocada para o tópico.</span><span class="sxs-lookup"><span data-stu-id="abde0-135">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

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

### <span data-ttu-id="abde0-136">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="abde0-136">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="abde0-137">Indica se o tópico requer detecção de duplicação.</span><span class="sxs-lookup"><span data-stu-id="abde0-137">Indicates whether the topic requires duplication detection.</span></span>

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

### <span data-ttu-id="abde0-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="abde0-138">-SizeInBytes</span></span>
<span data-ttu-id="abde0-139">Especifica o tamanho do tópico em bytes.</span><span class="sxs-lookup"><span data-stu-id="abde0-139">Specifies the size of the topic in bytes.</span></span>

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

### <span data-ttu-id="abde0-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="abde0-140">-SupportOrdering</span></span>
<span data-ttu-id="abde0-141">Indica se o tópico dá suporte a pedidos.</span><span class="sxs-lookup"><span data-stu-id="abde0-141">Indicates whether the topic supports ordering.</span></span>

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

### <span data-ttu-id="abde0-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="abde0-142">-Confirm</span></span>
<span data-ttu-id="abde0-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abde0-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abde0-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abde0-144">-WhatIf</span></span>
<span data-ttu-id="abde0-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="abde0-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abde0-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="abde0-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abde0-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abde0-147">-DefaultProfile</span></span>
<span data-ttu-id="abde0-148">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="abde0-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abde0-149">-Nome</span><span class="sxs-lookup"><span data-stu-id="abde0-149">-Name</span></span>
<span data-ttu-id="abde0-150">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="abde0-150">Topic Name.</span></span>

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

### <span data-ttu-id="abde0-151">-Namespace</span><span class="sxs-lookup"><span data-stu-id="abde0-151">-Namespace</span></span>
<span data-ttu-id="abde0-152">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="abde0-152">Namespace Name.</span></span>

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

### <span data-ttu-id="abde0-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abde0-153">-ResourceGroupName</span></span>
<span data-ttu-id="abde0-154">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="abde0-154">The name of the resource group</span></span>

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

### <span data-ttu-id="abde0-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abde0-155">CommonParameters</span></span>
<span data-ttu-id="abde0-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abde0-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abde0-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abde0-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abde0-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="abde0-158">INPUTS</span></span>

### <span data-ttu-id="abde0-159">System. String</span><span class="sxs-lookup"><span data-stu-id="abde0-159">System.String</span></span>
<span data-ttu-id="abde0-160">System. Nullable \` 1 \[ \[ System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = B77a5c561934e089 \] \] System. Nullable \` 1 \[ \[ System. Int64, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="abde0-160">System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

### <span data-ttu-id="abde0-161">-Resource</span><span class="sxs-lookup"><span data-stu-id="abde0-161">-ResourceGroup</span></span>
 <span data-ttu-id="abde0-162">System. String</span><span class="sxs-lookup"><span data-stu-id="abde0-162">System.String</span></span>

### <span data-ttu-id="abde0-163">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="abde0-163">-NamespaceName</span></span>
 <span data-ttu-id="abde0-164">System. String</span><span class="sxs-lookup"><span data-stu-id="abde0-164">System.String</span></span>

### <span data-ttu-id="abde0-165">-Topicname</span><span class="sxs-lookup"><span data-stu-id="abde0-165">-TopicName</span></span>
 <span data-ttu-id="abde0-166">System. String</span><span class="sxs-lookup"><span data-stu-id="abde0-166">System.String</span></span>

### <span data-ttu-id="abde0-167">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="abde0-167">-EnablePartitioning</span></span>
 <span data-ttu-id="abde0-168">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="abde0-168">System.Boolean?</span></span>

## <span data-ttu-id="abde0-169">EXIBE</span><span class="sxs-lookup"><span data-stu-id="abde0-169">OUTPUTS</span></span>

### <span data-ttu-id="abde0-170">Microsoft. Azure. Commands. ServiceBus. Models. Topicattributes</span><span class="sxs-lookup"><span data-stu-id="abde0-170">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>
<span data-ttu-id="abde0-171">Nome: local do SB-Topic_exampl1: identificação do oeste dos EUA:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-tipo de Topic_exampl1: Microsoft. ServiceBus/tópico AccessedAt: AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 3:16:42 AM CountDetails: DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true EnableExpress: false EnablePartitioning: true EnableSubscriptionPartitioning: FilteringMessagesBeforePublishing: false IsAnonymousAccessible: false isexpress MaxSizeInMegabytes: RequiresDuplicateDetection: false sizeInBytes: SubscriptionCount: false SupportOrdering: 0 status: active UpdatedAt: 16384: false: 1/20/2017 3:16:43 AM</span><span class="sxs-lookup"><span data-stu-id="abde0-171">Name                                : SB-Topic_exampl1 Location                            : West US Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 Type                                : Microsoft.ServiceBus/Topic AccessedAt                          : AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 3:16:42 AM CountDetails                        : DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True EnableExpress                       : False EnablePartitioning                  : True EnableSubscriptionPartitioning      : False FilteringMessagesBeforePublishing   : False IsAnonymousAccessible               : False IsExpress                           : False MaxSizeInMegabytes                  : 16384 RequiresDuplicateDetection          : False SizeInBytes                         : 0 Status                              : Active SubscriptionCount                   : SupportOrdering                     : False UpdatedAt                           : 1/20/2017 3:16:43 AM</span></span>

## <span data-ttu-id="abde0-172">INFORMA</span><span class="sxs-lookup"><span data-stu-id="abde0-172">NOTES</span></span>

## <span data-ttu-id="abde0-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="abde0-173">RELATED LINKS</span></span>
