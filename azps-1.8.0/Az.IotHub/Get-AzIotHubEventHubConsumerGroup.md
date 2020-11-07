---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 065c2e185be1a9cdc0f495b61104f659076b54b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770729"
---
# <span data-ttu-id="2df4a-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="2df4a-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="2df4a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2df4a-102">SYNOPSIS</span></span>
<span data-ttu-id="2df4a-103">Obtém todas as consumergroups do eventhub.</span><span class="sxs-lookup"><span data-stu-id="2df4a-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="2df4a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2df4a-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2df4a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2df4a-105">DESCRIPTION</span></span>
<span data-ttu-id="2df4a-106">Obtém todos os consumergroups do eventhub para os diferentes EventHubs usados pelo IotHub.</span><span class="sxs-lookup"><span data-stu-id="2df4a-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="2df4a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2df4a-107">EXAMPLES</span></span>

### <span data-ttu-id="2df4a-108">O exemplo 1 Obtém todos os consumergroups do eventhub para o eventhub de telemetria</span><span class="sxs-lookup"><span data-stu-id="2df4a-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="2df4a-109">Obtém todos os consumergroups do eventhub para o eventhub do iothub chamado myiothub</span><span class="sxs-lookup"><span data-stu-id="2df4a-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

### <span data-ttu-id="2df4a-110">O exemplo 2 Obtém todos os consumergroups do eventhub para o operationsmonitoring eventhub</span><span class="sxs-lookup"><span data-stu-id="2df4a-110">Example 2 Gets all the eventhub consumergroups for the operationsmonitoring eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents"
```

<span data-ttu-id="2df4a-111">Obtém todos os consumergroups do eventhub do eventhub do operationsMonitoringEvents para o iothub nomeado myiothub</span><span class="sxs-lookup"><span data-stu-id="2df4a-111">Gets all the eventhub consumergroups for the operationsMonitoringEvents eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="2df4a-112">OS</span><span class="sxs-lookup"><span data-stu-id="2df4a-112">PARAMETERS</span></span>

### <span data-ttu-id="2df4a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2df4a-113">-DefaultProfile</span></span>
<span data-ttu-id="2df4a-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2df4a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2df4a-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="2df4a-115">-EventHubEndpointName</span></span>
<span data-ttu-id="2df4a-116">Nome do ponto de extremidade do Hub do evento.</span><span class="sxs-lookup"><span data-stu-id="2df4a-116">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="2df4a-117">Valores possíveis eventos, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="2df4a-117">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df4a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="2df4a-118">-Name</span></span>
<span data-ttu-id="2df4a-119">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="2df4a-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="2df4a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2df4a-120">-ResourceGroupName</span></span>
<span data-ttu-id="2df4a-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2df4a-121">Resource Group Name</span></span>

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

### <span data-ttu-id="2df4a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2df4a-122">CommonParameters</span></span>
<span data-ttu-id="2df4a-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2df4a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2df4a-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2df4a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2df4a-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2df4a-125">INPUTS</span></span>

### <span data-ttu-id="2df4a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2df4a-126">System.String</span></span>

## <span data-ttu-id="2df4a-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2df4a-127">OUTPUTS</span></span>

### <span data-ttu-id="2df4a-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="2df4a-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="2df4a-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2df4a-129">NOTES</span></span>

## <span data-ttu-id="2df4a-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2df4a-130">RELATED LINKS</span></span>
