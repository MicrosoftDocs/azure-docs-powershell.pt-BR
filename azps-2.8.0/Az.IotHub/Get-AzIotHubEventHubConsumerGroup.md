---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 3905111a0855eef6421a587bc7151b411106d13a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596282"
---
# <span data-ttu-id="9f54c-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="9f54c-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="9f54c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f54c-102">SYNOPSIS</span></span>
<span data-ttu-id="9f54c-103">Obtém todas as consumergroups do eventhub.</span><span class="sxs-lookup"><span data-stu-id="9f54c-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="9f54c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f54c-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f54c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9f54c-105">DESCRIPTION</span></span>
<span data-ttu-id="9f54c-106">Obtém todos os consumergroups do eventhub para os diferentes EventHubs usados pelo IotHub.</span><span class="sxs-lookup"><span data-stu-id="9f54c-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="9f54c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f54c-107">EXAMPLES</span></span>

### <span data-ttu-id="9f54c-108">O exemplo 1 Obtém todos os consumergroups do eventhub para o eventhub de telemetria</span><span class="sxs-lookup"><span data-stu-id="9f54c-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="9f54c-109">Obtém todos os consumergroups do eventhub para o eventhub do iothub chamado myiothub</span><span class="sxs-lookup"><span data-stu-id="9f54c-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="9f54c-110">OS</span><span class="sxs-lookup"><span data-stu-id="9f54c-110">PARAMETERS</span></span>

### <span data-ttu-id="9f54c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f54c-111">-DefaultProfile</span></span>
<span data-ttu-id="9f54c-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9f54c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f54c-113">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="9f54c-113">-EventHubEndpointName</span></span>
<span data-ttu-id="9f54c-114">Nome do ponto de extremidade do Hub do evento.</span><span class="sxs-lookup"><span data-stu-id="9f54c-114">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="9f54c-115">Valores possíveis eventos, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="9f54c-115">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="9f54c-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f54c-116">-Name</span></span>
<span data-ttu-id="9f54c-117">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="9f54c-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="9f54c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f54c-118">-ResourceGroupName</span></span>
<span data-ttu-id="9f54c-119">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9f54c-119">Resource Group Name</span></span>

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

### <span data-ttu-id="9f54c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f54c-120">CommonParameters</span></span>
<span data-ttu-id="9f54c-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f54c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f54c-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f54c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f54c-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9f54c-123">INPUTS</span></span>

### <span data-ttu-id="9f54c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="9f54c-124">System.String</span></span>

## <span data-ttu-id="9f54c-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9f54c-125">OUTPUTS</span></span>

### <span data-ttu-id="9f54c-126">Microsoft. Azure. Commands. Management. IotHub. Models. PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="9f54c-126">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="9f54c-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9f54c-127">NOTES</span></span>

## <span data-ttu-id="9f54c-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f54c-128">RELATED LINKS</span></span>
