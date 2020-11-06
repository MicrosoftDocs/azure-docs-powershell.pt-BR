---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 656e010a05ce1272355f689be8513ecadd330e7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441091"
---
# <span data-ttu-id="157e6-101">New-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="157e6-101">New-AzureRmEventHub</span></span>

## <span data-ttu-id="157e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="157e6-102">SYNOPSIS</span></span>
<span data-ttu-id="157e6-103">Cria um novo hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="157e6-103">Creates a new Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="157e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="157e6-104">SYNTAX</span></span>

### <span data-ttu-id="157e6-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="157e6-105">EventhubInputObjectSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [[-Location] <String>] -Name <String>
 [-InputObject <EventHubAttributes>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="157e6-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="157e6-106">EventhubPropertiesSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [[-Location] <String>] -Name <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="157e6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="157e6-107">DESCRIPTION</span></span>
<span data-ttu-id="157e6-108">O cmdlet New-AzureRmEventHub cria um novo hub de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="157e6-108">The New-AzureRmEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="157e6-109">Para criar o Eventhub com as propriedades de descrição de captura, siga as etapas abaixo (exemplos 2).</span><span class="sxs-lookup"><span data-stu-id="157e6-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 


## <span data-ttu-id="157e6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="157e6-110">EXAMPLES</span></span>

### <span data-ttu-id="157e6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="157e6-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2
```

<span data-ttu-id="157e6-112">Cria um hub de eventos chamado \` MyEventHubName \` com um período de retenção de 3 dias e duas partições, no \` local westus \` , com o grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="157e6-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="157e6-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="157e6-113">Example 2</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

PS C:\> $CreatedEventHub = Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName

PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.CaptureDescriptionAttributes

PS C:\> $createdEventHub.CaptureDescription.Enabled = $true
PS C:\> $createdEventHub.CaptureDescription.IntervalInSeconds  = 120
PS C:\> $createdEventHub.CaptureDescription.Encoding  = "Avro"
PS C:\> $createdEventHub.CaptureDescription.SizeLimitInBytes = 10485763
PS C:\> $createdEventHub.CaptureDescription.Destination.Name = "EventHubArchive.AzureBlockBlob"
PS C:\> $createdEventHub.CaptureDescription.Destination.BlobContainer = "container"
PS C:\> $createdEventHub.CaptureDescription.Destination.ArchiveNameFormat = "{Namespace}/{EventHub}/{PartitionId}/{Year}/{Month}/{Day}/{Hour}/{Minute}/{Second}"
PS C:\> $createdEventHub.CaptureDescription.Destination.StorageAccountResourceId = "/subscriptions/{SubscriptionId}/resourceGroups/MyResourceGroupName/providers/Microsoft.ClassicStorage/storageAccounts/arjunteststorage"
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="157e6-114">Cria um hub de eventos chamado \` MyEventHubName \` com um período de retenção de 3 dias, 2 partições e propriedades CaptureDescription no \` local da westus \` , com MyResourceGroupName de grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="157e6-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="157e6-115">OS</span><span class="sxs-lookup"><span data-stu-id="157e6-115">PARAMETERS</span></span>

### <span data-ttu-id="157e6-116">-Local</span><span class="sxs-lookup"><span data-stu-id="157e6-116">-Location</span></span>
<span data-ttu-id="157e6-117">Localização geográfica do namespace.</span><span class="sxs-lookup"><span data-stu-id="157e6-117">Namespace geographic location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="157e6-118">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="157e6-118">-MessageRetentionInDays</span></span>
<span data-ttu-id="157e6-119">Tempo de retenção da mensagem dos hubs de evento em dias.</span><span class="sxs-lookup"><span data-stu-id="157e6-119">Event Hubs message retention time in days.</span></span>

```yaml
Type: Int64
Parameter Sets: EventhubPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="157e6-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="157e6-120">-PartitionCount</span></span>
<span data-ttu-id="157e6-121">Número de partições no Hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="157e6-121">Number of partitions in the Event Hub.</span></span>

```yaml
Type: Int64
Parameter Sets: EventhubPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="157e6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="157e6-122">-ResourceGroupName</span></span>
<span data-ttu-id="157e6-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="157e6-123">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="157e6-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="157e6-124">-Confirm</span></span>
<span data-ttu-id="157e6-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="157e6-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="157e6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="157e6-126">-WhatIf</span></span>
<span data-ttu-id="157e6-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="157e6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="157e6-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="157e6-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="157e6-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="157e6-129">-InputObject</span></span>
<span data-ttu-id="157e6-130">Objeto de entrada do EventHub.</span><span class="sxs-lookup"><span data-stu-id="157e6-130">EventHub Input object.</span></span>

```yaml
Type: EventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="157e6-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="157e6-131">-Name</span></span>
<span data-ttu-id="157e6-132">Nome do Eventhub.</span><span class="sxs-lookup"><span data-stu-id="157e6-132">Eventhub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="157e6-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="157e6-133">-Namespace</span></span>
<span data-ttu-id="157e6-134">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="157e6-134">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="157e6-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="157e6-135">INPUTS</span></span>

### <span data-ttu-id="157e6-136">System. String</span><span class="sxs-lookup"><span data-stu-id="157e6-136">System.String</span></span>

## <span data-ttu-id="157e6-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="157e6-137">OUTPUTS</span></span>

### <span data-ttu-id="157e6-138">Microsoft. Azure. Commands. EventHub. Models. EventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="157e6-138">Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes</span></span>

## <span data-ttu-id="157e6-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="157e6-139">NOTES</span></span>

## <span data-ttu-id="157e6-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="157e6-140">RELATED LINKS</span></span>

