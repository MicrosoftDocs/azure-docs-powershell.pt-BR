---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 2ff36708ba9b8303c8b8763146c81ee4e4d8b209
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432221"
---
# <span data-ttu-id="c3d60-101">Set-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="c3d60-101">Set-AzureRmEventHub</span></span>

## <span data-ttu-id="c3d60-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3d60-102">SYNOPSIS</span></span>
<span data-ttu-id="c3d60-103">Atualiza o Hub de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="c3d60-103">Updates the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3d60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3d60-104">SYNTAX</span></span>

### <span data-ttu-id="c3d60-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c3d60-105">EventhubInputObjectSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-InputObject <EventHubAttributes>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="c3d60-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="c3d60-106">EventhubPropertiesSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="c3d60-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3d60-107">DESCRIPTION</span></span>
<span data-ttu-id="c3d60-108">O cmdlet Set-AzureRmEventHub atualiza as propriedades do hub de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="c3d60-108">The Set-AzureRmEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="c3d60-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3d60-109">EXAMPLES</span></span>

### <span data-ttu-id="c3d60-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c3d60-110">Example 1</span></span>
<span data-ttu-id="c3d60-111">Para atualizar o Eventhub com as propriedades de descrição de captura, siga as etapas abaixo.</span><span class="sxs-lookup"><span data-stu-id="c3d60-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
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

<span data-ttu-id="c3d60-112">Atualiza o MyEventHubName do hub de eventos \` \` representado \` pelo \` objeto MyCreatedEventHub, definindo o período de retenção da mensagem como 4 dias, o número de partições para 2 e propriedades de CaptureDescription</span><span class="sxs-lookup"><span data-stu-id="c3d60-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="c3d60-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c3d60-113">Example 2</span></span>

```
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="c3d60-114">Atualiza o MyEventHubName do hub de eventos \` \` representado \` pelo \` objeto MyCreatedEventHub, definindo o período de retenção da mensagem como 4 dias e o número de partições para 2.</span><span class="sxs-lookup"><span data-stu-id="c3d60-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="c3d60-115">OS</span><span class="sxs-lookup"><span data-stu-id="c3d60-115">PARAMETERS</span></span>

### <span data-ttu-id="c3d60-116">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="c3d60-116">-messageRetentionInDays</span></span>
<span data-ttu-id="c3d60-117">Período de retenção da mensagem do hub de eventos em dias.</span><span class="sxs-lookup"><span data-stu-id="c3d60-117">Event Hub message retention period, in days.</span></span>

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

### <span data-ttu-id="c3d60-118">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="c3d60-118">-partitionCount</span></span>
<span data-ttu-id="c3d60-119">Número de partições nesse Hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="c3d60-119">Number of partitions on this Event Hub.</span></span>

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

### <span data-ttu-id="c3d60-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3d60-120">-ResourceGroupName</span></span>
<span data-ttu-id="c3d60-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c3d60-121">Resource group name.</span></span>

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

### <span data-ttu-id="c3d60-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c3d60-122">-Confirm</span></span>
<span data-ttu-id="c3d60-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3d60-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3d60-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3d60-124">-WhatIf</span></span>
<span data-ttu-id="c3d60-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c3d60-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3d60-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c3d60-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3d60-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3d60-127">-InputObject</span></span>
<span data-ttu-id="c3d60-128">Objeto do EventHub.</span><span class="sxs-lookup"><span data-stu-id="c3d60-128">EventHub object.</span></span>

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

### <span data-ttu-id="c3d60-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3d60-129">-Name</span></span>
<span data-ttu-id="c3d60-130">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="c3d60-130">Namespace Name.</span></span>

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

### <span data-ttu-id="c3d60-131">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c3d60-131">-Namespace</span></span>
<span data-ttu-id="c3d60-132">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="c3d60-132">Namespace Name.</span></span>

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

## <span data-ttu-id="c3d60-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3d60-133">INPUTS</span></span>

### <span data-ttu-id="c3d60-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c3d60-134">System.String</span></span>

## <span data-ttu-id="c3d60-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3d60-135">OUTPUTS</span></span>

### <span data-ttu-id="c3d60-136">Microsoft. Azure. Commands. EventHub. Models. EventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="c3d60-136">Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes</span></span>

## <span data-ttu-id="c3d60-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3d60-137">NOTES</span></span>

## <span data-ttu-id="c3d60-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3d60-138">RELATED LINKS</span></span>

