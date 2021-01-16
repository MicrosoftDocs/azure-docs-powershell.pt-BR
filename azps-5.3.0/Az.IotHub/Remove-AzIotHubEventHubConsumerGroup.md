---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 9fa0a9d85dc9c7b1a6cc56c3c329b1810cceaa18
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272820"
---
# <span data-ttu-id="69e4a-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="69e4a-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="69e4a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69e4a-102">SYNOPSIS</span></span>
<span data-ttu-id="69e4a-103">Exclui um userconsumer do eventhub.</span><span class="sxs-lookup"><span data-stu-id="69e4a-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="69e4a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69e4a-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69e4a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69e4a-105">DESCRIPTION</span></span>
<span data-ttu-id="69e4a-106">Exclui um userconsumer do eventhub.</span><span class="sxs-lookup"><span data-stu-id="69e4a-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="69e4a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69e4a-107">EXAMPLES</span></span>

### <span data-ttu-id="69e4a-108">Exemplo 1 remover o meu consumidor do eventhub do eventhub de telemetria</span><span class="sxs-lookup"><span data-stu-id="69e4a-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="69e4a-109">Remove o nome de cliente do IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="69e4a-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="69e4a-110">OS</span><span class="sxs-lookup"><span data-stu-id="69e4a-110">PARAMETERS</span></span>

### <span data-ttu-id="69e4a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69e4a-111">-DefaultProfile</span></span>
<span data-ttu-id="69e4a-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="69e4a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69e4a-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="69e4a-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="69e4a-114">Nome do o seu consumidor do EventHub.</span><span class="sxs-lookup"><span data-stu-id="69e4a-114">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="69e4a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="69e4a-115">-Name</span></span>
<span data-ttu-id="69e4a-116">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="69e4a-116">Name of the IotHub</span></span>

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

### <span data-ttu-id="69e4a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69e4a-117">-ResourceGroupName</span></span>
<span data-ttu-id="69e4a-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="69e4a-118">Resource Group Name</span></span>

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

### <span data-ttu-id="69e4a-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="69e4a-119">-Confirm</span></span>
<span data-ttu-id="69e4a-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69e4a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69e4a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69e4a-121">-WhatIf</span></span>
<span data-ttu-id="69e4a-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="69e4a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69e4a-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="69e4a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69e4a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69e4a-124">CommonParameters</span></span>
<span data-ttu-id="69e4a-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69e4a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69e4a-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69e4a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69e4a-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69e4a-127">INPUTS</span></span>

### <span data-ttu-id="69e4a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="69e4a-128">System.String</span></span>

## <span data-ttu-id="69e4a-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69e4a-129">OUTPUTS</span></span>

### <span data-ttu-id="69e4a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="69e4a-130">System.String</span></span>

## <span data-ttu-id="69e4a-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69e4a-131">NOTES</span></span>

## <span data-ttu-id="69e4a-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69e4a-132">RELATED LINKS</span></span>
