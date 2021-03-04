---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 1e563126bb57986bed752184340808991f7e2a00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888242"
---
# <span data-ttu-id="5115d-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5115d-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="5115d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5115d-102">SYNOPSIS</span></span>
<span data-ttu-id="5115d-103">Exclui um grupo de consumidores eventhub.</span><span class="sxs-lookup"><span data-stu-id="5115d-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="5115d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5115d-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5115d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5115d-105">DESCRIPTION</span></span>
<span data-ttu-id="5115d-106">Exclui um grupo de consumidores eventhub.</span><span class="sxs-lookup"><span data-stu-id="5115d-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="5115d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5115d-107">EXAMPLES</span></span>

### <span data-ttu-id="5115d-108">Exemplo 1 Remover eventhub consumergroup do eventhub de telemetria</span><span class="sxs-lookup"><span data-stu-id="5115d-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="5115d-109">Remove o grupo de consumo chamado myconsumergroup do IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="5115d-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="5115d-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5115d-110">PARAMETERS</span></span>

### <span data-ttu-id="5115d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5115d-111">-DefaultProfile</span></span>
<span data-ttu-id="5115d-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5115d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5115d-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="5115d-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="5115d-114">Nome do EventHub ConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="5115d-114">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="5115d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5115d-115">-Name</span></span>
<span data-ttu-id="5115d-116">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="5115d-116">Name of the IotHub</span></span>

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

### <span data-ttu-id="5115d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5115d-117">-ResourceGroupName</span></span>
<span data-ttu-id="5115d-118">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="5115d-118">Resource Group Name</span></span>

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

### <span data-ttu-id="5115d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5115d-119">-Confirm</span></span>
<span data-ttu-id="5115d-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5115d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5115d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5115d-121">-WhatIf</span></span>
<span data-ttu-id="5115d-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5115d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5115d-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5115d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5115d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5115d-124">CommonParameters</span></span>
<span data-ttu-id="5115d-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5115d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5115d-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5115d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5115d-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5115d-127">INPUTS</span></span>

### <span data-ttu-id="5115d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5115d-128">System.String</span></span>

## <span data-ttu-id="5115d-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5115d-129">OUTPUTS</span></span>

### <span data-ttu-id="5115d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5115d-130">System.String</span></span>

## <span data-ttu-id="5115d-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="5115d-131">NOTES</span></span>

## <span data-ttu-id="5115d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5115d-132">RELATED LINKS</span></span>
