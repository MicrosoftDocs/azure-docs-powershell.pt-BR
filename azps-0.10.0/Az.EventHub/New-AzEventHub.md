---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHub.md
ms.openlocfilehash: 8f850b8b3d4bee54ac4927668ab9a0de1895a248
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775889"
---
# <span data-ttu-id="84b58-101">New-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="84b58-101">New-AzEventHub</span></span>

## <span data-ttu-id="84b58-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="84b58-102">SYNOPSIS</span></span>
<span data-ttu-id="84b58-103">Cria um novo hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="84b58-103">Creates a new Event Hub.</span></span>

## <span data-ttu-id="84b58-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84b58-104">SYNTAX</span></span>

### <span data-ttu-id="84b58-105">EventhubPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="84b58-105">EventhubPropertiesSet (Default)</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84b58-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="84b58-106">EventhubInputObjectSet</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84b58-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="84b58-107">DESCRIPTION</span></span>
<span data-ttu-id="84b58-108">O cmdlet New-AzEventHub cria um novo hub de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="84b58-108">The New-AzEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="84b58-109">Para criar o Eventhub com as propriedades de descrição de captura, siga as etapas abaixo (exemplos 2).</span><span class="sxs-lookup"><span data-stu-id="84b58-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="84b58-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="84b58-110">EXAMPLES</span></span>

### <span data-ttu-id="84b58-111">Exemplo 1-criar novo EventHub</span><span class="sxs-lookup"><span data-stu-id="84b58-111">Example 1  - Create new EventHub</span></span>
```
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="84b58-112">Cria um hub de eventos chamado \` MyEventHubName \` com um período de retenção de 3 dias e duas partições, no \` local westus \` , com o grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="84b58-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="84b58-113">Exemplo 2 atualizar o Eventhub com "CaptureDescription"</span><span class="sxs-lookup"><span data-stu-id="84b58-113">Example 2 Update Eventhub with 'CaptureDescription'</span></span>
```
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

PS C:\> $CreatedEventHub = Get-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName

PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.PSCaptureDescriptionAttributes

PS C:\> $createdEventHub.CaptureDescription.Enabled = $true
PS C:\> $createdEventHub.CaptureDescription.IntervalInSeconds  = 120
PS C:\> $createdEventHub.CaptureDescription.Encoding  = "Avro"
PS C:\> $createdEventHub.CaptureDescription.SizeLimitInBytes = 10485763
PS C:\> $createdEventHub.CaptureDescription.Destination.Name = "EventHubArchive.AzureBlockBlob"
PS C:\> $createdEventHub.CaptureDescription.Destination.BlobContainer = "container"
PS C:\> $createdEventHub.CaptureDescription.Destination.ArchiveNameFormat = "{Namespace}/{EventHub}/{PartitionId}/{Year}/{Month}/{Day}/{Hour}/{Minute}/{Second}"
PS C:\> $createdEventHub.CaptureDescription.Destination.StorageAccountResourceId = "/subscriptions/{SubscriptionId}/resourceGroups/MyResourceGroupName/providers/Microsoft.ClassicStorage/storageAccounts/arjunteststorage"
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="84b58-114">Cria um hub de eventos chamado \` MyEventHubName \` com um período de retenção de 3 dias, 2 partições e propriedades CaptureDescription no \` local da westus \` , com MyResourceGroupName de grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="84b58-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="84b58-115">OS</span><span class="sxs-lookup"><span data-stu-id="84b58-115">PARAMETERS</span></span>

### <span data-ttu-id="84b58-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84b58-116">-DefaultProfile</span></span>
<span data-ttu-id="84b58-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="84b58-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b58-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84b58-118">-InputObject</span></span>
<span data-ttu-id="84b58-119">Objeto de entrada do EventHub</span><span class="sxs-lookup"><span data-stu-id="84b58-119">EventHub Input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84b58-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="84b58-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="84b58-121">Retenção de mensagem do Eventhub em dias</span><span class="sxs-lookup"><span data-stu-id="84b58-121">Eventhub Message Retention In Days</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: EventhubPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84b58-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="84b58-122">-Name</span></span>
<span data-ttu-id="84b58-123">Nome do Eventhub</span><span class="sxs-lookup"><span data-stu-id="84b58-123">Eventhub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84b58-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="84b58-124">-Namespace</span></span>
<span data-ttu-id="84b58-125">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="84b58-125">Namespace Name</span></span>

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

### <span data-ttu-id="84b58-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="84b58-126">-PartitionCount</span></span>
<span data-ttu-id="84b58-127">PartitionCount do Eventhub</span><span class="sxs-lookup"><span data-stu-id="84b58-127">Eventhub PartitionCount</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: EventhubPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84b58-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84b58-128">-ResourceGroupName</span></span>
<span data-ttu-id="84b58-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="84b58-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84b58-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="84b58-130">-Confirm</span></span>
<span data-ttu-id="84b58-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84b58-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84b58-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84b58-132">-WhatIf</span></span>
<span data-ttu-id="84b58-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="84b58-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84b58-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="84b58-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84b58-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84b58-135">CommonParameters</span></span>
<span data-ttu-id="84b58-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84b58-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84b58-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84b58-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84b58-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="84b58-138">INPUTS</span></span>

### <span data-ttu-id="84b58-139">System. String</span><span class="sxs-lookup"><span data-stu-id="84b58-139">System.String</span></span>

### <span data-ttu-id="84b58-140">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="84b58-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="84b58-141">System. Nullable ' 1 [[System. Int64, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="84b58-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="84b58-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="84b58-142">OUTPUTS</span></span>

### <span data-ttu-id="84b58-143">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="84b58-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="84b58-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="84b58-144">NOTES</span></span>

## <span data-ttu-id="84b58-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84b58-145">RELATED LINKS</span></span>