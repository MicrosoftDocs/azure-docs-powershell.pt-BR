---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 00342fddd1a8755f22f925e25595ec36b9326c09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430247"
---
# <span data-ttu-id="41cca-101">Add-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="41cca-101">Add-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="41cca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41cca-102">SYNOPSIS</span></span>
<span data-ttu-id="41cca-103">Cria um grupo de consumidores do eventhub.</span><span class="sxs-lookup"><span data-stu-id="41cca-103">Creates an eventhub consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41cca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41cca-104">SYNTAX</span></span>

```
Add-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41cca-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41cca-105">DESCRIPTION</span></span>
<span data-ttu-id="41cca-106">Cria um grupo de consumidores no Eventhub associado ao IotHub especificado.</span><span class="sxs-lookup"><span data-stu-id="41cca-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="41cca-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41cca-107">EXAMPLES</span></span>

### <span data-ttu-id="41cca-108">Exemplo 1: adicionar um grupo de consumidores ao eventhub de telemetria</span><span class="sxs-lookup"><span data-stu-id="41cca-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="41cca-109">Adiciona um novo nome de consumidor chamado "myconsumero" ao eventhub para eventos de telemetria no iothub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="41cca-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

### <span data-ttu-id="41cca-110">Exemplo 2: adicionar um grupo de consumidores às operações que monitoram o eventhub</span><span class="sxs-lookup"><span data-stu-id="41cca-110">Example 2: Add a consumer group to the operations monitoring eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="41cca-111">Adiciona um novo nome de consumidor chamado "myconsumero" ao eventhub para eventos de monitoramento de operações no iothub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="41cca-111">Adds a new consumergroup named "myconsumergroup" to the eventhub for operations monitoring events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="41cca-112">OS</span><span class="sxs-lookup"><span data-stu-id="41cca-112">PARAMETERS</span></span>

### <span data-ttu-id="41cca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41cca-113">-DefaultProfile</span></span>
<span data-ttu-id="41cca-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="41cca-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41cca-115">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="41cca-115">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="41cca-116">Nome do meu consumidor do EventHub que você deseja adicionar.</span><span class="sxs-lookup"><span data-stu-id="41cca-116">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41cca-117">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="41cca-117">-EventHubEndpointName</span></span>
<span data-ttu-id="41cca-118">Nome do ponto de extremidade do EventHub.</span><span class="sxs-lookup"><span data-stu-id="41cca-118">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="41cca-119">Valores possíveis eventos, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="41cca-119">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41cca-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="41cca-120">-Name</span></span>
<span data-ttu-id="41cca-121">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="41cca-121">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41cca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41cca-122">-ResourceGroupName</span></span>
<span data-ttu-id="41cca-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="41cca-123">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="41cca-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="41cca-124">-Confirm</span></span>
<span data-ttu-id="41cca-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41cca-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41cca-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41cca-126">-WhatIf</span></span>
<span data-ttu-id="41cca-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="41cca-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41cca-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="41cca-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41cca-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41cca-129">CommonParameters</span></span>
<span data-ttu-id="41cca-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41cca-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41cca-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41cca-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41cca-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41cca-132">INPUTS</span></span>

### <span data-ttu-id="41cca-133">System. String</span><span class="sxs-lookup"><span data-stu-id="41cca-133">System.String</span></span>

## <span data-ttu-id="41cca-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41cca-134">OUTPUTS</span></span>

### <span data-ttu-id="41cca-135">System. String</span><span class="sxs-lookup"><span data-stu-id="41cca-135">System.String</span></span>

## <span data-ttu-id="41cca-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41cca-136">NOTES</span></span>

## <span data-ttu-id="41cca-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41cca-137">RELATED LINKS</span></span>
