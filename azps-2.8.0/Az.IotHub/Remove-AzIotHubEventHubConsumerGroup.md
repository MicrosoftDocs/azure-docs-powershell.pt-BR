---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: d321892ef2ebbe8e50908a5d519f1990ebb875ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596247"
---
# <span data-ttu-id="c9015-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="c9015-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="c9015-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9015-102">SYNOPSIS</span></span>
<span data-ttu-id="c9015-103">Exclui um userconsumer do eventhub.</span><span class="sxs-lookup"><span data-stu-id="c9015-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="c9015-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9015-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9015-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c9015-105">DESCRIPTION</span></span>
<span data-ttu-id="c9015-106">Exclui um userconsumer do eventhub.</span><span class="sxs-lookup"><span data-stu-id="c9015-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="c9015-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c9015-107">EXAMPLES</span></span>

### <span data-ttu-id="c9015-108">Exemplo 1 remover o meu consumidor do eventhub do eventhub de telemetria</span><span class="sxs-lookup"><span data-stu-id="c9015-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="c9015-109">Remove o nome de cliente do IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="c9015-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="c9015-110">OS</span><span class="sxs-lookup"><span data-stu-id="c9015-110">PARAMETERS</span></span>

### <span data-ttu-id="c9015-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9015-111">-DefaultProfile</span></span>
<span data-ttu-id="c9015-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c9015-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9015-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="c9015-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="c9015-114">Nome do o seu consumidor do EventHub.</span><span class="sxs-lookup"><span data-stu-id="c9015-114">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9015-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="c9015-115">-EventHubEndpointName</span></span>
<span data-ttu-id="c9015-116">Nome do ponto de extremidade do EventHub.</span><span class="sxs-lookup"><span data-stu-id="c9015-116">EventHub Endpoint Name.</span></span>
<span data-ttu-id="c9015-117">Valores possíveis eventos, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="c9015-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="c9015-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9015-118">-Name</span></span>
<span data-ttu-id="c9015-119">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="c9015-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="c9015-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9015-120">-ResourceGroupName</span></span>
<span data-ttu-id="c9015-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c9015-121">Resource Group Name</span></span>

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

### <span data-ttu-id="c9015-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c9015-122">-Confirm</span></span>
<span data-ttu-id="c9015-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9015-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9015-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9015-124">-WhatIf</span></span>
<span data-ttu-id="c9015-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c9015-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9015-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c9015-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9015-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9015-127">CommonParameters</span></span>
<span data-ttu-id="c9015-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9015-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9015-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9015-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9015-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c9015-130">INPUTS</span></span>

### <span data-ttu-id="c9015-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c9015-131">System.String</span></span>

## <span data-ttu-id="c9015-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c9015-132">OUTPUTS</span></span>

### <span data-ttu-id="c9015-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c9015-133">System.String</span></span>

## <span data-ttu-id="c9015-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c9015-134">NOTES</span></span>

## <span data-ttu-id="c9015-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9015-135">RELATED LINKS</span></span>
