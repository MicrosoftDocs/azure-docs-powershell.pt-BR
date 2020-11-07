---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHub.md
ms.openlocfilehash: 2b1f3c0cd30b9f0ebc67a0b11f5b42a35b7e3394
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775857"
---
# <span data-ttu-id="710a0-101">Set-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="710a0-101">Set-AzEventHub</span></span>

## <span data-ttu-id="710a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="710a0-102">SYNOPSIS</span></span>
<span data-ttu-id="710a0-103">Atualiza o Hub de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="710a0-103">Updates the specified Event Hub.</span></span>

## <span data-ttu-id="710a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="710a0-104">SYNTAX</span></span>

### <span data-ttu-id="710a0-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="710a0-105">EventhubInputObjectSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="710a0-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="710a0-106">EventhubPropertiesSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="710a0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="710a0-107">DESCRIPTION</span></span>
<span data-ttu-id="710a0-108">O cmdlet Set-AzEventHub atualiza as propriedades do hub de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="710a0-108">The Set-AzEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="710a0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="710a0-109">EXAMPLES</span></span>

### <span data-ttu-id="710a0-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="710a0-110">Example 1</span></span>
<span data-ttu-id="710a0-111">Para atualizar o Eventhub com as propriedades de descrição de captura, siga as etapas abaixo.</span><span class="sxs-lookup"><span data-stu-id="710a0-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
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

<span data-ttu-id="710a0-112">Atualiza o MyEventHubName do hub de eventos \` \` representado \` pelo \` objeto MyCreatedEventHub, definindo o período de retenção da mensagem como 4 dias, o número de partições para 2 e propriedades de CaptureDescription</span><span class="sxs-lookup"><span data-stu-id="710a0-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="710a0-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="710a0-113">Example 2</span></span>
```
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="710a0-114">Atualiza o MyEventHubName do hub de eventos \` \` representado \` pelo \` objeto MyCreatedEventHub, definindo o período de retenção da mensagem como 4 dias e o número de partições para 2.</span><span class="sxs-lookup"><span data-stu-id="710a0-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="710a0-115">OS</span><span class="sxs-lookup"><span data-stu-id="710a0-115">PARAMETERS</span></span>

### <span data-ttu-id="710a0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="710a0-116">-DefaultProfile</span></span>
<span data-ttu-id="710a0-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="710a0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="710a0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="710a0-118">-InputObject</span></span>
<span data-ttu-id="710a0-119">Objeto do EventHub</span><span class="sxs-lookup"><span data-stu-id="710a0-119">EventHub object</span></span>

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

### <span data-ttu-id="710a0-120">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="710a0-120">-messageRetentionInDays</span></span>
<span data-ttu-id="710a0-121">Retenção de mensagem do Eventhub em dias</span><span class="sxs-lookup"><span data-stu-id="710a0-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="710a0-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="710a0-122">-Name</span></span>
<span data-ttu-id="710a0-123">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="710a0-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="710a0-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="710a0-124">-Namespace</span></span>
<span data-ttu-id="710a0-125">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="710a0-125">Namespace Name</span></span>

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

### <span data-ttu-id="710a0-126">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="710a0-126">-partitionCount</span></span>
<span data-ttu-id="710a0-127">PartitionCount do Eventhub</span><span class="sxs-lookup"><span data-stu-id="710a0-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="710a0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="710a0-128">-ResourceGroupName</span></span>
<span data-ttu-id="710a0-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="710a0-129">Resource Group Name</span></span>

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

### <span data-ttu-id="710a0-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="710a0-130">-Confirm</span></span>
<span data-ttu-id="710a0-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="710a0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="710a0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="710a0-132">-WhatIf</span></span>
<span data-ttu-id="710a0-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="710a0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="710a0-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="710a0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="710a0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="710a0-135">CommonParameters</span></span>
<span data-ttu-id="710a0-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="710a0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="710a0-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="710a0-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="710a0-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="710a0-138">INPUTS</span></span>

### <span data-ttu-id="710a0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="710a0-139">System.String</span></span>

### <span data-ttu-id="710a0-140">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="710a0-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="710a0-141">System. Nullable ' 1 [[System. Int64, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="710a0-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="710a0-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="710a0-142">OUTPUTS</span></span>

### <span data-ttu-id="710a0-143">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="710a0-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="710a0-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="710a0-144">NOTES</span></span>

## <span data-ttu-id="710a0-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="710a0-145">RELATED LINKS</span></span>