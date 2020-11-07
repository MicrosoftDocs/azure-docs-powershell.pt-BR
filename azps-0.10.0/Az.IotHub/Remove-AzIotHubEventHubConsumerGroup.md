---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: e2b6bb4c58be90b205fc4a50ddab9c84c0d1ee20
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775825"
---
# <span data-ttu-id="a7c04-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="a7c04-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="a7c04-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7c04-102">SYNOPSIS</span></span>
<span data-ttu-id="a7c04-103">Exclui um userconsumer do eventhub.</span><span class="sxs-lookup"><span data-stu-id="a7c04-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="a7c04-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7c04-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7c04-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a7c04-105">DESCRIPTION</span></span>
<span data-ttu-id="a7c04-106">Exclui um userconsumer do eventhub.</span><span class="sxs-lookup"><span data-stu-id="a7c04-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="a7c04-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7c04-107">EXAMPLES</span></span>

### <span data-ttu-id="a7c04-108">Exemplo 1 remover o meu consumidor do eventhub do eventhub de telemetria</span><span class="sxs-lookup"><span data-stu-id="a7c04-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="a7c04-109">Remove o nome de cliente do IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="a7c04-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="a7c04-110">OS</span><span class="sxs-lookup"><span data-stu-id="a7c04-110">PARAMETERS</span></span>

### <span data-ttu-id="a7c04-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7c04-111">-DefaultProfile</span></span>
<span data-ttu-id="a7c04-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a7c04-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7c04-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="a7c04-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="a7c04-114">Nome do o seu consumidor do EventHub.</span><span class="sxs-lookup"><span data-stu-id="a7c04-114">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="a7c04-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7c04-115">-Name</span></span>
<span data-ttu-id="a7c04-116">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="a7c04-116">Name of the IotHub</span></span>

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

### <span data-ttu-id="a7c04-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7c04-117">-ResourceGroupName</span></span>
<span data-ttu-id="a7c04-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a7c04-118">Resource Group Name</span></span>

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

### <span data-ttu-id="a7c04-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a7c04-119">-Confirm</span></span>
<span data-ttu-id="a7c04-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7c04-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7c04-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7c04-121">-WhatIf</span></span>
<span data-ttu-id="a7c04-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a7c04-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7c04-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a7c04-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7c04-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7c04-124">CommonParameters</span></span>
<span data-ttu-id="a7c04-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7c04-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7c04-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7c04-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7c04-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a7c04-127">INPUTS</span></span>

### <span data-ttu-id="a7c04-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a7c04-128">System.String</span></span>

## <span data-ttu-id="a7c04-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a7c04-129">OUTPUTS</span></span>

### <span data-ttu-id="a7c04-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a7c04-130">System.String</span></span>

## <span data-ttu-id="a7c04-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a7c04-131">NOTES</span></span>

## <span data-ttu-id="a7c04-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7c04-132">RELATED LINKS</span></span>
