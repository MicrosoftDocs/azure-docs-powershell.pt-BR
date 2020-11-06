---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
ms.openlocfilehash: 4de16b04151daa1c3e64dc6ea93b171c38fdb96a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430490"
---
# <span data-ttu-id="6b732-101">Set-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="6b732-101">Set-AzureRmEventHub</span></span>

## <span data-ttu-id="6b732-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b732-102">SYNOPSIS</span></span>
<span data-ttu-id="6b732-103">Atualiza o Hub de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="6b732-103">Updates the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b732-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b732-104">SYNTAX</span></span>

### <span data-ttu-id="6b732-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6b732-105">EventhubInputObjectSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b732-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="6b732-106">EventhubPropertiesSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b732-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b732-107">DESCRIPTION</span></span>
<span data-ttu-id="6b732-108">O cmdlet Set-AzureRmEventHub atualiza as propriedades do hub de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="6b732-108">The Set-AzureRmEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="6b732-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b732-109">EXAMPLES</span></span>

### <span data-ttu-id="6b732-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6b732-110">Example 1</span></span>
<span data-ttu-id="6b732-111">Para atualizar o Eventhub com as propriedades de descrição de captura, siga as etapas abaixo.</span><span class="sxs-lookup"><span data-stu-id="6b732-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 



```
PS C:\> $CreatedEventHub = Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.PSCaptureDescriptionAttributes
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

<span data-ttu-id="6b732-112">Atualiza o MyEventHubName do hub de eventos \` \` representado \` pelo \` objeto MyCreatedEventHub, definindo o período de retenção da mensagem como 4 dias, o número de partições para 2 e propriedades de CaptureDescription</span><span class="sxs-lookup"><span data-stu-id="6b732-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="6b732-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6b732-113">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="6b732-114">Atualiza o MyEventHubName do hub de eventos \` \` representado \` pelo \` objeto MyCreatedEventHub, definindo o período de retenção da mensagem como 4 dias e o número de partições para 2.</span><span class="sxs-lookup"><span data-stu-id="6b732-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="6b732-115">OS</span><span class="sxs-lookup"><span data-stu-id="6b732-115">PARAMETERS</span></span>

### <span data-ttu-id="6b732-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b732-116">-DefaultProfile</span></span>
<span data-ttu-id="6b732-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6b732-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b732-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b732-118">-InputObject</span></span>
<span data-ttu-id="6b732-119">Objeto do EventHub</span><span class="sxs-lookup"><span data-stu-id="6b732-119">EventHub object</span></span>

```yaml
Type: PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b732-120">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="6b732-120">-messageRetentionInDays</span></span>
<span data-ttu-id="6b732-121">Retenção de mensagem do Eventhub em dias</span><span class="sxs-lookup"><span data-stu-id="6b732-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="6b732-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b732-122">-Name</span></span>
<span data-ttu-id="6b732-123">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="6b732-123">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b732-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6b732-124">-Namespace</span></span>
<span data-ttu-id="6b732-125">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="6b732-125">Namespace Name</span></span>

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

### <span data-ttu-id="6b732-126">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="6b732-126">-partitionCount</span></span>
<span data-ttu-id="6b732-127">PartitionCount do Eventhub</span><span class="sxs-lookup"><span data-stu-id="6b732-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="6b732-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b732-128">-ResourceGroupName</span></span>
<span data-ttu-id="6b732-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6b732-129">Resource Group Name</span></span>

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

### <span data-ttu-id="6b732-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6b732-130">-Confirm</span></span>
<span data-ttu-id="6b732-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b732-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b732-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b732-132">-WhatIf</span></span>
<span data-ttu-id="6b732-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6b732-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b732-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6b732-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b732-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b732-135">CommonParameters</span></span>
<span data-ttu-id="6b732-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b732-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6b732-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b732-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b732-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b732-138">INPUTS</span></span>

### <span data-ttu-id="6b732-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6b732-139">System.String</span></span>
<span data-ttu-id="6b732-140">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes System. Nullable ' 1 [[System. Int64, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6b732-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="6b732-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b732-141">OUTPUTS</span></span>

### <span data-ttu-id="6b732-142">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="6b732-142">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>


## <span data-ttu-id="6b732-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b732-143">NOTES</span></span>

## <span data-ttu-id="6b732-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b732-144">RELATED LINKS</span></span>
