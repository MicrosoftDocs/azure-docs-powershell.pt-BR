---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: b326f7228a60f7549fc6dcd227b9bad947f22add
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440647"
---
# <span data-ttu-id="71699-101">Remove-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="71699-101">Remove-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="71699-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71699-102">SYNOPSIS</span></span>
<span data-ttu-id="71699-103">Exclui um userconsumer do eventhub.</span><span class="sxs-lookup"><span data-stu-id="71699-103">Deletes an eventhub consumergroup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71699-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71699-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71699-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71699-105">DESCRIPTION</span></span>
<span data-ttu-id="71699-106">Exclui um userconsumer do eventhub.</span><span class="sxs-lookup"><span data-stu-id="71699-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="71699-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71699-107">EXAMPLES</span></span>

### <span data-ttu-id="71699-108">Exemplo 1 remover o meu consumidor do eventhub do eventhub de telemetria</span><span class="sxs-lookup"><span data-stu-id="71699-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName events -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="71699-109">Remove o nome de cliente do IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="71699-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="71699-110">OS</span><span class="sxs-lookup"><span data-stu-id="71699-110">PARAMETERS</span></span>

### <span data-ttu-id="71699-111">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="71699-111">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="71699-112">Nome do o seu consumidor do EventHub.</span><span class="sxs-lookup"><span data-stu-id="71699-112">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="71699-113">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="71699-113">-EventHubEndpointName</span></span>
<span data-ttu-id="71699-114">Nome do ponto de extremidade do EventHub.</span><span class="sxs-lookup"><span data-stu-id="71699-114">EventHub Endpoint Name.</span></span>
<span data-ttu-id="71699-115">Valores possíveis eventos, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="71699-115">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71699-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="71699-116">-Name</span></span>
<span data-ttu-id="71699-117">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="71699-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="71699-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71699-118">-ResourceGroupName</span></span>
<span data-ttu-id="71699-119">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="71699-119">Resource Group Name</span></span>

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

### <span data-ttu-id="71699-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="71699-120">-Confirm</span></span>
<span data-ttu-id="71699-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71699-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71699-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71699-122">-WhatIf</span></span>
<span data-ttu-id="71699-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="71699-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71699-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71699-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71699-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71699-125">-DefaultProfile</span></span>
<span data-ttu-id="71699-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71699-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71699-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71699-127">CommonParameters</span></span>
<span data-ttu-id="71699-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71699-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71699-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71699-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71699-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71699-130">INPUTS</span></span>

### <span data-ttu-id="71699-131">System. String</span><span class="sxs-lookup"><span data-stu-id="71699-131">System.String</span></span>

## <span data-ttu-id="71699-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71699-132">OUTPUTS</span></span>

### <span data-ttu-id="71699-133">System. Collections. Generic. IEnumerable ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="71699-133">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="71699-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71699-134">NOTES</span></span>

## <span data-ttu-id="71699-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71699-135">RELATED LINKS</span></span>

