---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
ms.openlocfilehash: 15704f90530c332eddfeaf4a9e13fe2d7767bfa4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113825"
---
# <span data-ttu-id="7711c-101">Set-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="7711c-101">Set-AzEventHub</span></span>

## <span data-ttu-id="7711c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7711c-102">SYNOPSIS</span></span>
<span data-ttu-id="7711c-103">Atualiza o Hub de Eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="7711c-103">Updates the specified Event Hub.</span></span>

## <span data-ttu-id="7711c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7711c-104">SYNTAX</span></span>

### <span data-ttu-id="7711c-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7711c-105">EventhubInputObjectSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7711c-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="7711c-106">EventhubPropertiesSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7711c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7711c-107">DESCRIPTION</span></span>
<span data-ttu-id="7711c-108">O Set-AzEventHub cmdlet atualiza as propriedades do Hub de Eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="7711c-108">The Set-AzEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="7711c-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7711c-109">EXAMPLES</span></span>

### <span data-ttu-id="7711c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7711c-110">Example 1</span></span>
<span data-ttu-id="7711c-111">Para atualizar o Eventhub com propriedades de descrição de captura, siga as etapas abaixo.</span><span class="sxs-lookup"><span data-stu-id="7711c-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
PS C:\> $createdEventHub = Get-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyCreatedEventHub
PS C:\> $ceatedEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.PSCaptureDescriptionAttributes
PS C:\> $createdEventHub.CaptureDescription.Enabled = $true
PS C:\> $createdEventHub.CaptureDescription.IntervalInSeconds  = 120
PS C:\> $createdEventHub.CaptureDescription.Encoding  = "Avro"
PS C:\> $createdEventHub.CaptureDescription.SizeLimitInBytes = 10485763
PS C:\> $createdEventHub.CaptureDescription.Destination.Name = "EventHubArchive.AzureBlockBlob"
PS C:\> $createdEventHub.CaptureDescription.Destination.BlobContainer = "container"
PS C:\> $createdEventHub.CaptureDescription.Destination.ArchiveNameFormat = "{Namespace}/{EventHub}/{PartitionId}/{Year}/{Month}/{Day}/{Hour}/{Minute}/{Second}"
PS C:\> $createdEventHub.CaptureDescription.Destination.StorageAccountResourceId = "/subscriptions/{SubscriptionId}/resourceGroups/MyResourceGroupName/providers/Microsoft.ClassicStorage/storageAccounts/arjunteststorage"
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject $createdEventHub 
```

<span data-ttu-id="7711c-112">Atualiza o Hub de Eventos MyEventHubName representado pelo objeto \` \` \` MyCreatedEventHub, configurando as \` propriedades CaptureDescription</span><span class="sxs-lookup"><span data-stu-id="7711c-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the CaptureDescription properties</span></span>

### <span data-ttu-id="7711c-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7711c-113">Example 2</span></span>
```
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="7711c-114">Atualiza o Hub de Eventos MyEventHubName representado pelo objeto \` \` \` MyCreatedEventHub, definindo o período de retenção da mensagem como 4 dias e o número de partições como \` 2.</span><span class="sxs-lookup"><span data-stu-id="7711c-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="7711c-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7711c-115">PARAMETERS</span></span>

### <span data-ttu-id="7711c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7711c-116">-DefaultProfile</span></span>
<span data-ttu-id="7711c-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7711c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7711c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7711c-118">-InputObject</span></span>
<span data-ttu-id="7711c-119">Objeto EventHub</span><span class="sxs-lookup"><span data-stu-id="7711c-119">EventHub object</span></span>

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

### <span data-ttu-id="7711c-120">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7711c-120">-messageRetentionInDays</span></span>
<span data-ttu-id="7711c-121">Retenção de mensagens eventhub em dias</span><span class="sxs-lookup"><span data-stu-id="7711c-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="7711c-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="7711c-122">-Name</span></span>
<span data-ttu-id="7711c-123">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="7711c-123">Namespace Name</span></span>

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

### <span data-ttu-id="7711c-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7711c-124">-Namespace</span></span>
<span data-ttu-id="7711c-125">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="7711c-125">Namespace Name</span></span>

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

### <span data-ttu-id="7711c-126">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="7711c-126">-partitionCount</span></span>
<span data-ttu-id="7711c-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="7711c-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="7711c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7711c-128">-ResourceGroupName</span></span>
<span data-ttu-id="7711c-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="7711c-129">Resource Group Name</span></span>

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

### <span data-ttu-id="7711c-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7711c-130">-Confirm</span></span>
<span data-ttu-id="7711c-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7711c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7711c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7711c-132">-WhatIf</span></span>
<span data-ttu-id="7711c-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7711c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7711c-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7711c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7711c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7711c-135">CommonParameters</span></span>
<span data-ttu-id="7711c-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7711c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7711c-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7711c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7711c-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="7711c-138">INPUTS</span></span>

### <span data-ttu-id="7711c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7711c-139">System.String</span></span>

### <span data-ttu-id="7711c-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="7711c-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="7711c-141">System.Nullable'1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7711c-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7711c-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="7711c-142">OUTPUTS</span></span>

### <span data-ttu-id="7711c-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="7711c-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="7711c-144">Notas</span><span class="sxs-lookup"><span data-stu-id="7711c-144">NOTES</span></span>

## <span data-ttu-id="7711c-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7711c-145">RELATED LINKS</span></span>
