---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
ms.openlocfilehash: 366bb4879b2db8bbb4a4335442a4abc6f07a5221
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886033"
---
# <span data-ttu-id="f7fe1-101">New-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="f7fe1-101">New-AzEventHub</span></span>

## <span data-ttu-id="f7fe1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7fe1-102">SYNOPSIS</span></span>
<span data-ttu-id="f7fe1-103">Cria um novo Hub de Eventos.</span><span class="sxs-lookup"><span data-stu-id="f7fe1-103">Creates a new Event Hub.</span></span>

## <span data-ttu-id="f7fe1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f7fe1-104">SYNTAX</span></span>

### <span data-ttu-id="f7fe1-105">EventhubPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f7fe1-105">EventhubPropertiesSet (Default)</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7fe1-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f7fe1-106">EventhubInputObjectSet</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7fe1-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f7fe1-107">DESCRIPTION</span></span>
<span data-ttu-id="f7fe1-108">O New-AzEventHub cmdlet cria um novo Hub de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f7fe1-108">The New-AzEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="f7fe1-109">Para criar Eventhub com propriedades de descrição de Captura, siga as etapas abaixo (Exemplos 2).</span><span class="sxs-lookup"><span data-stu-id="f7fe1-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="f7fe1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7fe1-110">EXAMPLES</span></span>

### <span data-ttu-id="f7fe1-111">Exemplo 1: - Criar novo EventHub</span><span class="sxs-lookup"><span data-stu-id="f7fe1-111">Example 1: - Create new EventHub</span></span>
```powershell
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="f7fe1-112">Cria um Hub de Eventos chamado MyEventHubName com um período de retenção de mensagens de 3 dias e duas partições, no local do WestUS, com o grupo de recursos \` \` \` \` \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="f7fe1-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="f7fe1-113">Exemplo 2: Atualizar Eventhub com 'CaptureDescription'</span><span class="sxs-lookup"><span data-stu-id="f7fe1-113">Example 2: Update Eventhub with 'CaptureDescription'</span></span>
```powershell
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

<span data-ttu-id="f7fe1-114">Cria um Hub de Eventos chamado MyEventHubName com um período de retenção de mensagens de 3 dias, 2 partições e propriedades CaptureDescription no local do WestUS, com o grupo de recursos \` \` \` \` \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="f7fe1-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="f7fe1-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f7fe1-115">PARAMETERS</span></span>

### <span data-ttu-id="f7fe1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7fe1-116">-DefaultProfile</span></span>
<span data-ttu-id="f7fe1-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f7fe1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7fe1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7fe1-118">-InputObject</span></span>
<span data-ttu-id="f7fe1-119">Objeto EventHub Input</span><span class="sxs-lookup"><span data-stu-id="f7fe1-119">EventHub Input object</span></span>

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

### <span data-ttu-id="f7fe1-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="f7fe1-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="f7fe1-121">Retenção de mensagens eventhub em dias</span><span class="sxs-lookup"><span data-stu-id="f7fe1-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="f7fe1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f7fe1-122">-Name</span></span>
<span data-ttu-id="f7fe1-123">Nome eventhub</span><span class="sxs-lookup"><span data-stu-id="f7fe1-123">Eventhub Name</span></span>

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

### <span data-ttu-id="f7fe1-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f7fe1-124">-Namespace</span></span>
<span data-ttu-id="f7fe1-125">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="f7fe1-125">Namespace Name</span></span>

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

### <span data-ttu-id="f7fe1-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="f7fe1-126">-PartitionCount</span></span>
<span data-ttu-id="f7fe1-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="f7fe1-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="f7fe1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7fe1-128">-ResourceGroupName</span></span>
<span data-ttu-id="f7fe1-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="f7fe1-129">Resource Group Name</span></span>

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

### <span data-ttu-id="f7fe1-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7fe1-130">-Confirm</span></span>
<span data-ttu-id="f7fe1-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7fe1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7fe1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7fe1-132">-WhatIf</span></span>
<span data-ttu-id="f7fe1-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f7fe1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7fe1-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f7fe1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7fe1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7fe1-135">CommonParameters</span></span>
<span data-ttu-id="f7fe1-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7fe1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7fe1-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7fe1-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7fe1-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7fe1-138">INPUTS</span></span>

### <span data-ttu-id="f7fe1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f7fe1-139">System.String</span></span>

### <span data-ttu-id="f7fe1-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="f7fe1-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="f7fe1-141">System.Nullable'1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f7fe1-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f7fe1-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f7fe1-142">OUTPUTS</span></span>

### <span data-ttu-id="f7fe1-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="f7fe1-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="f7fe1-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="f7fe1-144">NOTES</span></span>

## <span data-ttu-id="f7fe1-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7fe1-145">RELATED LINKS</span></span>
