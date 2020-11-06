---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
ms.openlocfilehash: 2c5bf49245da7ecac0f9d4351f5a66a39a663b98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439868"
---
# <span data-ttu-id="2ad69-101">New-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="2ad69-101">New-AzureRmEventHub</span></span>

## <span data-ttu-id="2ad69-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2ad69-102">SYNOPSIS</span></span>
<span data-ttu-id="2ad69-103">Cria um novo hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="2ad69-103">Creates a new Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ad69-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ad69-104">SYNTAX</span></span>

### <span data-ttu-id="2ad69-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2ad69-105">EventhubInputObjectSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ad69-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="2ad69-106">EventhubPropertiesSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ad69-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2ad69-107">DESCRIPTION</span></span>
<span data-ttu-id="2ad69-108">O cmdlet New-AzureRmEventHub cria um novo hub de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="2ad69-108">The New-AzureRmEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="2ad69-109">Para criar o Eventhub com as propriedades de descrição de captura, siga as etapas abaixo (exemplos 2).</span><span class="sxs-lookup"><span data-stu-id="2ad69-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="2ad69-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2ad69-110">EXAMPLES</span></span>

### <span data-ttu-id="2ad69-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2ad69-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2
```

<span data-ttu-id="2ad69-112">Cria um hub de eventos chamado \` MyEventHubName \` com um período de retenção de 3 dias e duas partições, no \` local westus \` , com o grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="2ad69-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="2ad69-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2ad69-113">Example 2</span></span>
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

<span data-ttu-id="2ad69-114">Cria um hub de eventos chamado \` MyEventHubName \` com um período de retenção de 3 dias, 2 partições e propriedades CaptureDescription no \` local da westus \` , com MyResourceGroupName de grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="2ad69-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="2ad69-115">OS</span><span class="sxs-lookup"><span data-stu-id="2ad69-115">PARAMETERS</span></span>

### <span data-ttu-id="2ad69-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ad69-116">-DefaultProfile</span></span>
<span data-ttu-id="2ad69-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2ad69-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ad69-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ad69-118">-InputObject</span></span>
<span data-ttu-id="2ad69-119">Objeto de entrada do EventHub</span><span class="sxs-lookup"><span data-stu-id="2ad69-119">EventHub Input object</span></span>

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

### <span data-ttu-id="2ad69-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="2ad69-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="2ad69-121">Retenção de mensagem do Eventhub em dias</span><span class="sxs-lookup"><span data-stu-id="2ad69-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="2ad69-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="2ad69-122">-Name</span></span>
<span data-ttu-id="2ad69-123">Nome do Eventhub</span><span class="sxs-lookup"><span data-stu-id="2ad69-123">Eventhub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ad69-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2ad69-124">-Namespace</span></span>
<span data-ttu-id="2ad69-125">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="2ad69-125">Namespace Name</span></span>

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

### <span data-ttu-id="2ad69-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="2ad69-126">-PartitionCount</span></span>
<span data-ttu-id="2ad69-127">PartitionCount do Eventhub</span><span class="sxs-lookup"><span data-stu-id="2ad69-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="2ad69-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ad69-128">-ResourceGroupName</span></span>
<span data-ttu-id="2ad69-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2ad69-129">Resource Group Name</span></span>

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

### <span data-ttu-id="2ad69-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2ad69-130">-Confirm</span></span>
<span data-ttu-id="2ad69-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ad69-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ad69-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ad69-132">-WhatIf</span></span>
<span data-ttu-id="2ad69-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2ad69-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ad69-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2ad69-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ad69-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ad69-135">CommonParameters</span></span>
<span data-ttu-id="2ad69-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ad69-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2ad69-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ad69-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ad69-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2ad69-138">INPUTS</span></span>

### <span data-ttu-id="2ad69-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2ad69-139">System.String</span></span>
<span data-ttu-id="2ad69-140">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes System. Nullable ' 1 [[System. Int64, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2ad69-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="2ad69-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2ad69-141">OUTPUTS</span></span>

### <span data-ttu-id="2ad69-142">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="2ad69-142">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>


## <span data-ttu-id="2ad69-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2ad69-143">NOTES</span></span>

## <span data-ttu-id="2ad69-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ad69-144">RELATED LINKS</span></span>
