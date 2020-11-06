---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
ms.openlocfilehash: e2ca0b6902ecc13c9dfe4f418ea5d321b6e36dbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429339"
---
# <span data-ttu-id="495fe-101">New-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="495fe-101">New-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="495fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="495fe-102">SYNOPSIS</span></span>
<span data-ttu-id="495fe-103">Cria um novo tópico de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="495fe-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="495fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="495fe-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>]
 [-SupportOrdering <Boolean>] [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="495fe-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="495fe-105">DESCRIPTION</span></span>
<span data-ttu-id="495fe-106">O cmdlet **New-AzureRmServiceBusTopic** cria um novo tópico de barramento de serviço no namespace de barramento de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="495fe-106">The **New-AzureRmServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="495fe-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="495fe-107">EXAMPLES</span></span>

### <span data-ttu-id="495fe-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="495fe-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 11:51:24 PM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : False
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : True
UpdatedAt                           : 10/11/2018 11:51:24 PM
```

<span data-ttu-id="495fe-109">Cria um novo tópico de barramento `SB-Topic_exampl1` de serviço no namespace de barramento de serviço especificado `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="495fe-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="495fe-110">OS</span><span class="sxs-lookup"><span data-stu-id="495fe-110">PARAMETERS</span></span>

### <span data-ttu-id="495fe-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="495fe-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="495fe-112">Especifica o intervalo de tempo ocioso de [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) após o qual o tópico é excluído automaticamente.</span><span class="sxs-lookup"><span data-stu-id="495fe-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="495fe-113">A duração mínima é de 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="495fe-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="495fe-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="495fe-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="495fe-115">Especifica a duração após a qual a mensagem expira, a partir de quando a mensagem é enviada para o barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="495fe-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

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

### <span data-ttu-id="495fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="495fe-116">-DefaultProfile</span></span>
<span data-ttu-id="495fe-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="495fe-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="495fe-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="495fe-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="495fe-119">Especifica a estrutura [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) que define a duração do histórico de detecção de duplicidades.</span><span class="sxs-lookup"><span data-stu-id="495fe-119">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="495fe-120">O valor padrão é 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="495fe-120">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="495fe-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="495fe-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="495fe-122">Indica se as operações em lote do lado do servidor estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="495fe-122">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="495fe-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="495fe-123">-EnableExpress</span></span>
<span data-ttu-id="495fe-124">Indica se as entidades expressas estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="495fe-124">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="495fe-125">Uma fila expressa armazena uma mensagem em memória temporariamente antes de gravá-la no armazenamento persistente.</span><span class="sxs-lookup"><span data-stu-id="495fe-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="495fe-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="495fe-126">-EnablePartitioning</span></span>
<span data-ttu-id="495fe-127">Especifica se o tópico deve ser habilitado para ser particionado em vários agentes de mensagem.</span><span class="sxs-lookup"><span data-stu-id="495fe-127">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

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

### <span data-ttu-id="495fe-128">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="495fe-128">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="495fe-129">O tamanho máximo do tópico em megabytes, que é o tamanho da memória alocada para o tópico.</span><span class="sxs-lookup"><span data-stu-id="495fe-129">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

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

### <span data-ttu-id="495fe-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="495fe-130">-Name</span></span>
<span data-ttu-id="495fe-131">Nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="495fe-131">Topic Name.</span></span>

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

### <span data-ttu-id="495fe-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="495fe-132">-Namespace</span></span>
<span data-ttu-id="495fe-133">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="495fe-133">Namespace Name.</span></span>

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

### <span data-ttu-id="495fe-134">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="495fe-134">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="495fe-135">Indica se o tópico requer detecção de duplicação.</span><span class="sxs-lookup"><span data-stu-id="495fe-135">Indicates whether the topic requires duplication detection.</span></span>

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

### <span data-ttu-id="495fe-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="495fe-136">-ResourceGroupName</span></span>
<span data-ttu-id="495fe-137">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="495fe-137">The name of the resource group</span></span>

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

### <span data-ttu-id="495fe-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="495fe-138">-SizeInBytes</span></span>
<span data-ttu-id="495fe-139">Especifica o tamanho do tópico em bytes.</span><span class="sxs-lookup"><span data-stu-id="495fe-139">Specifies the size of the topic in bytes.</span></span>

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

### <span data-ttu-id="495fe-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="495fe-140">-SupportOrdering</span></span>
<span data-ttu-id="495fe-141">Indica se o tópico dá suporte a pedidos.</span><span class="sxs-lookup"><span data-stu-id="495fe-141">Indicates whether the topic supports ordering.</span></span>

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

### <span data-ttu-id="495fe-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="495fe-142">-Confirm</span></span>
<span data-ttu-id="495fe-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="495fe-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="495fe-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="495fe-144">-WhatIf</span></span>
<span data-ttu-id="495fe-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="495fe-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="495fe-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="495fe-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="495fe-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="495fe-147">CommonParameters</span></span>
<span data-ttu-id="495fe-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="495fe-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="495fe-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="495fe-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="495fe-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="495fe-150">INPUTS</span></span>

### <span data-ttu-id="495fe-151">System. String</span><span class="sxs-lookup"><span data-stu-id="495fe-151">System.String</span></span>

### <span data-ttu-id="495fe-152">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="495fe-152">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="495fe-153">System. Nullable ' 1 [[System. Int64, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="495fe-153">System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="495fe-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="495fe-154">OUTPUTS</span></span>

### <span data-ttu-id="495fe-155">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="495fe-155">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="495fe-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="495fe-156">NOTES</span></span>

## <span data-ttu-id="495fe-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="495fe-157">RELATED LINKS</span></span>