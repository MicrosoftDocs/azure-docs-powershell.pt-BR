---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 84da4142bdc1b5435ca895be1995c6b48b5881fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433116"
---
# <span data-ttu-id="7f3a4-101">Get-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="7f3a4-101">Get-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="7f3a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f3a4-102">SYNOPSIS</span></span>
<span data-ttu-id="7f3a4-103">Obtém todas as consumergroups do eventhub.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-103">Gets all the eventhub consumergroups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f3a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f3a4-104">SYNTAX</span></span>

```
Get-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f3a4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f3a4-105">DESCRIPTION</span></span>
<span data-ttu-id="7f3a4-106">Obtém todos os consumergroups do eventhub para os diferentes EventHubs usados pelo IotHub.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="7f3a4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f3a4-107">EXAMPLES</span></span>

### <span data-ttu-id="7f3a4-108">O exemplo 1 Obtém todos os consumergroups do eventhub para o eventhub de telemetria</span><span class="sxs-lookup"><span data-stu-id="7f3a4-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="7f3a4-109">Obtém todos os consumergroups do eventhub para o eventhub do iothub chamado myiothub</span><span class="sxs-lookup"><span data-stu-id="7f3a4-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

### <span data-ttu-id="7f3a4-110">O exemplo 2 Obtém todos os consumergroups do eventhub para o operationsmonitoring eventhub</span><span class="sxs-lookup"><span data-stu-id="7f3a4-110">Example 2 Gets all the eventhub consumergroups for the operationsmonitoring eventhub</span></span>
```
PS C:\> Get-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents"
```

<span data-ttu-id="7f3a4-111">Obtém todos os consumergroups do eventhub do eventhub do operationsMonitoringEvents para o iothub nomeado myiothub</span><span class="sxs-lookup"><span data-stu-id="7f3a4-111">Gets all the eventhub consumergroups for the operationsMonitoringEvents eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="7f3a4-112">OS</span><span class="sxs-lookup"><span data-stu-id="7f3a4-112">PARAMETERS</span></span>

### <span data-ttu-id="7f3a4-113">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="7f3a4-113">-EventHubEndpointName</span></span>
<span data-ttu-id="7f3a4-114">Nome do ponto de extremidade do Hub do evento.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-114">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="7f3a4-115">Valores possíveis eventos, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="7f3a4-115">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f3a4-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f3a4-116">-Name</span></span>
<span data-ttu-id="7f3a4-117">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="7f3a4-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="7f3a4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f3a4-118">-ResourceGroupName</span></span>
<span data-ttu-id="7f3a4-119">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7f3a4-119">Resource Group Name</span></span>

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

### <span data-ttu-id="7f3a4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f3a4-120">-DefaultProfile</span></span>
<span data-ttu-id="7f3a4-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f3a4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f3a4-122">CommonParameters</span></span>
<span data-ttu-id="7f3a4-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f3a4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f3a4-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f3a4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f3a4-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f3a4-125">INPUTS</span></span>

### <span data-ttu-id="7f3a4-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7f3a4-126">System.String</span></span>

## <span data-ttu-id="7f3a4-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f3a4-127">OUTPUTS</span></span>

### <span data-ttu-id="7f3a4-128">System. Collections. Generic. IEnumerable ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7f3a4-128">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="7f3a4-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f3a4-129">NOTES</span></span>

## <span data-ttu-id="7f3a4-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f3a4-130">RELATED LINKS</span></span>

