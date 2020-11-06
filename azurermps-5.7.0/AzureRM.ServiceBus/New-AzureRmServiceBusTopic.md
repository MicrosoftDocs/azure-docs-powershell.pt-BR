---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
ms.openlocfilehash: a79afdbba1293c3340e499387b5df745d8b76228
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602838"
---
# <span data-ttu-id="b37e7-101">New-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="b37e7-101">New-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="b37e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b37e7-102">SYNOPSIS</span></span>
<span data-ttu-id="b37e7-103">Cria um novo tópico de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="b37e7-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b37e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b37e7-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>]
 [-SupportOrdering <Boolean>] [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b37e7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b37e7-105">DESCRIPTION</span></span>
<span data-ttu-id="b37e7-106">O cmdlet **New-AzureRmServiceBusTopic** cria um novo tópico de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="b37e7-106">The **New-AzureRmServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="b37e7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b37e7-107">EXAMPLES</span></span>

### <span data-ttu-id="b37e7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b37e7-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True

Name                                : SB-Topic_exampl1
Id                                  : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S
                                      B-Topic_exampl1
Type                                : Microsoft.ServiceBus/Topic
AccessedAt                          : 
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 3:16:42 AM
CountDetails                        : 
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 16384
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 
SupportOrdering                     : False
UpdatedAt                           : 1/20/2017 3:16:43 AM

```
<span data-ttu-id="b37e7-109">Cria um novo tópico de barramento `SB-Topic_exampl1` de serviço no namespace de barramento de serviço especificado `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="b37e7-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="b37e7-110">OS</span><span class="sxs-lookup"><span data-stu-id="b37e7-110">PARAMETERS</span></span>

### <span data-ttu-id="b37e7-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="b37e7-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="b37e7-112">Especifica o intervalo de tempo ocioso de [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) após o qual o tópico é excluído automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b37e7-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="b37e7-113">A duração mínima é de 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="b37e7-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="b37e7-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="b37e7-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="b37e7-115">Especifica a duração após a qual a mensagem expira, a partir de quando a mensagem é enviada para o barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="b37e7-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

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

### <span data-ttu-id="b37e7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b37e7-116">-DefaultProfile</span></span>
<span data-ttu-id="b37e7-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b37e7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b37e7-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="b37e7-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="b37e7-119">Especifica a estrutura [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) que define a duração do histórico de detecção de duplicidades.</span><span class="sxs-lookup"><span data-stu-id="b37e7-119">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="b37e7-120">O valor padrão é 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="b37e7-120">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="b37e7-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="b37e7-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="b37e7-122">Indica se as operações em lote do lado do servidor estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="b37e7-122">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="b37e7-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="b37e7-123">-EnableExpress</span></span>
<span data-ttu-id="b37e7-124">Indica se as entidades expressas estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="b37e7-124">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="b37e7-125">Uma fila expressa armazena uma mensagem em memória temporariamente antes de gravá-la no armazenamento persistente.</span><span class="sxs-lookup"><span data-stu-id="b37e7-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="b37e7-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="b37e7-126">-EnablePartitioning</span></span>
<span data-ttu-id="b37e7-127">Especifica se o tópico deve ser habilitado para ser particionado em vários agentes de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b37e7-127">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b37e7-128">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="b37e7-128">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="b37e7-129">O tamanho máximo do tópico em megabytes, que é o tamanho da memória alocada para o tópico.</span><span class="sxs-lookup"><span data-stu-id="b37e7-129">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

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

### <span data-ttu-id="b37e7-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="b37e7-130">-Name</span></span>
<span data-ttu-id="b37e7-131">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="b37e7-131">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b37e7-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b37e7-132">-Namespace</span></span>
<span data-ttu-id="b37e7-133">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="b37e7-133">Namespace Name.</span></span>

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

### <span data-ttu-id="b37e7-134">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="b37e7-134">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="b37e7-135">Indica se o tópico requer detecção de duplicação.</span><span class="sxs-lookup"><span data-stu-id="b37e7-135">Indicates whether the topic requires duplication detection.</span></span>

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

### <span data-ttu-id="b37e7-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b37e7-136">-ResourceGroupName</span></span>
<span data-ttu-id="b37e7-137">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b37e7-137">The name of the resource group</span></span>

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

### <span data-ttu-id="b37e7-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="b37e7-138">-SizeInBytes</span></span>
<span data-ttu-id="b37e7-139">Especifica o tamanho do tópico em bytes.</span><span class="sxs-lookup"><span data-stu-id="b37e7-139">Specifies the size of the topic in bytes.</span></span>

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

### <span data-ttu-id="b37e7-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="b37e7-140">-SupportOrdering</span></span>
<span data-ttu-id="b37e7-141">Indica se o tópico dá suporte a pedidos.</span><span class="sxs-lookup"><span data-stu-id="b37e7-141">Indicates whether the topic supports ordering.</span></span>

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

### <span data-ttu-id="b37e7-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b37e7-142">-Confirm</span></span>
<span data-ttu-id="b37e7-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b37e7-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b37e7-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b37e7-144">-WhatIf</span></span>
<span data-ttu-id="b37e7-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b37e7-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b37e7-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b37e7-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b37e7-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b37e7-147">CommonParameters</span></span>
<span data-ttu-id="b37e7-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b37e7-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b37e7-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b37e7-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b37e7-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b37e7-150">INPUTS</span></span>

### <span data-ttu-id="b37e7-151">System. String</span><span class="sxs-lookup"><span data-stu-id="b37e7-151">System.String</span></span>
<span data-ttu-id="b37e7-152">System. Nullable \` 1 \[ \[ System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = B77a5c561934e089 \] \] System. Nullable \` 1 \[ \[ System. Int64, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="b37e7-152">System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

### <span data-ttu-id="b37e7-153">-Resource</span><span class="sxs-lookup"><span data-stu-id="b37e7-153">-ResourceGroup</span></span>
 <span data-ttu-id="b37e7-154">System. String</span><span class="sxs-lookup"><span data-stu-id="b37e7-154">System.String</span></span>

### <span data-ttu-id="b37e7-155">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b37e7-155">-NamespaceName</span></span>
 <span data-ttu-id="b37e7-156">System. String</span><span class="sxs-lookup"><span data-stu-id="b37e7-156">System.String</span></span>

### <span data-ttu-id="b37e7-157">-Topicname</span><span class="sxs-lookup"><span data-stu-id="b37e7-157">-TopicName</span></span>
 <span data-ttu-id="b37e7-158">System. String</span><span class="sxs-lookup"><span data-stu-id="b37e7-158">System.String</span></span>

### <span data-ttu-id="b37e7-159">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="b37e7-159">-EnablePartitioning</span></span>
 <span data-ttu-id="b37e7-160">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="b37e7-160">System.Boolean?</span></span>

## <span data-ttu-id="b37e7-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b37e7-161">OUTPUTS</span></span>

### <span data-ttu-id="b37e7-162">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="b37e7-162">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="b37e7-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b37e7-163">NOTES</span></span>

## <span data-ttu-id="b37e7-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b37e7-164">RELATED LINKS</span></span>

