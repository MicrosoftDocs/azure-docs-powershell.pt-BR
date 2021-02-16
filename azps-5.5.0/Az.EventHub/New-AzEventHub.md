---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
ms.openlocfilehash: eec7294a15217be85b4c2248dac6506d54c2e6aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117666"
---
# <span data-ttu-id="b9bb4-101">New-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="b9bb4-101">New-AzEventHub</span></span>

## <span data-ttu-id="b9bb4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9bb4-102">SYNOPSIS</span></span>
<span data-ttu-id="b9bb4-103">Cria um novo Hub de Eventos.</span><span class="sxs-lookup"><span data-stu-id="b9bb4-103">Creates a new Event Hub.</span></span>

## <span data-ttu-id="b9bb4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9bb4-104">SYNTAX</span></span>

### <span data-ttu-id="b9bb4-105">EventhubPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b9bb4-105">EventhubPropertiesSet (Default)</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9bb4-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b9bb4-106">EventhubInputObjectSet</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9bb4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9bb4-107">DESCRIPTION</span></span>
<span data-ttu-id="b9bb4-108">O New-AzEventHub cmdlet cria um novo Hub de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b9bb4-108">The New-AzEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="b9bb4-109">Para criar o Eventhub com propriedades de descrição de captura, siga as etapas abaixo (Exemplos 2).</span><span class="sxs-lookup"><span data-stu-id="b9bb4-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="b9bb4-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b9bb4-110">EXAMPLES</span></span>

### <span data-ttu-id="b9bb4-111">Exemplo 1: - Criar novo EventHub</span><span class="sxs-lookup"><span data-stu-id="b9bb4-111">Example 1: - Create new EventHub</span></span>
```powershell
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="b9bb4-112">Cria um Hub de Eventos chamado MyEventHubName com um período de retenção de mensagem de 3 dias e duas partições, no local do WestUS, com o grupo de recursos \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="b9bb4-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b9bb4-113">Exemplo 2: Atualizar o Eventhub com 'CaptureDescription'</span><span class="sxs-lookup"><span data-stu-id="b9bb4-113">Example 2: Update Eventhub with 'CaptureDescription'</span></span>
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

<span data-ttu-id="b9bb4-114">Cria um Hub de Eventos chamado MyEventHubName com um período de retenção de mensagem de 3 dias, 2 partições e propriedades CaptureDescription no local do WestUS, com o grupo de recursos \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="b9bb4-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="b9bb4-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9bb4-115">PARAMETERS</span></span>

### <span data-ttu-id="b9bb4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9bb4-116">-DefaultProfile</span></span>
<span data-ttu-id="b9bb4-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9bb4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9bb4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9bb4-118">-InputObject</span></span>
<span data-ttu-id="b9bb4-119">Objeto de entrada eventHub</span><span class="sxs-lookup"><span data-stu-id="b9bb4-119">EventHub Input object</span></span>

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

### <span data-ttu-id="b9bb4-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="b9bb4-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="b9bb4-121">Retenção de mensagens eventhub em dias</span><span class="sxs-lookup"><span data-stu-id="b9bb4-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="b9bb4-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9bb4-122">-Name</span></span>
<span data-ttu-id="b9bb4-123">Nome eventhub</span><span class="sxs-lookup"><span data-stu-id="b9bb4-123">Eventhub Name</span></span>

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

### <span data-ttu-id="b9bb4-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b9bb4-124">-Namespace</span></span>
<span data-ttu-id="b9bb4-125">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="b9bb4-125">Namespace Name</span></span>

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

### <span data-ttu-id="b9bb4-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="b9bb4-126">-PartitionCount</span></span>
<span data-ttu-id="b9bb4-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="b9bb4-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="b9bb4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9bb4-128">-ResourceGroupName</span></span>
<span data-ttu-id="b9bb4-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="b9bb4-129">Resource Group Name</span></span>

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

### <span data-ttu-id="b9bb4-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b9bb4-130">-Confirm</span></span>
<span data-ttu-id="b9bb4-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9bb4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9bb4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9bb4-132">-WhatIf</span></span>
<span data-ttu-id="b9bb4-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b9bb4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9bb4-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b9bb4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9bb4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9bb4-135">CommonParameters</span></span>
<span data-ttu-id="b9bb4-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9bb4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9bb4-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9bb4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9bb4-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="b9bb4-138">INPUTS</span></span>

### <span data-ttu-id="b9bb4-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b9bb4-139">System.String</span></span>

### <span data-ttu-id="b9bb4-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="b9bb4-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="b9bb4-141">System.Nullable'1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b9bb4-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b9bb4-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="b9bb4-142">OUTPUTS</span></span>

### <span data-ttu-id="b9bb4-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="b9bb4-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="b9bb4-144">Notas</span><span class="sxs-lookup"><span data-stu-id="b9bb4-144">NOTES</span></span>

## <span data-ttu-id="b9bb4-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9bb4-145">RELATED LINKS</span></span>
