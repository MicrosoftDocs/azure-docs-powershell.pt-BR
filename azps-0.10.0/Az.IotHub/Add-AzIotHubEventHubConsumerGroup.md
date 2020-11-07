---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 2592284be483793ea246d30e95a4c9065fdd6e3c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776719"
---
# <span data-ttu-id="05eeb-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="05eeb-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="05eeb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="05eeb-102">SYNOPSIS</span></span>
<span data-ttu-id="05eeb-103">Cria um grupo de consumidores do eventhub.</span><span class="sxs-lookup"><span data-stu-id="05eeb-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="05eeb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05eeb-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05eeb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="05eeb-105">DESCRIPTION</span></span>
<span data-ttu-id="05eeb-106">Cria um grupo de consumidores no Eventhub associado ao IotHub especificado.</span><span class="sxs-lookup"><span data-stu-id="05eeb-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="05eeb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="05eeb-107">EXAMPLES</span></span>

### <span data-ttu-id="05eeb-108">Exemplo 1: adicionar um grupo de consumidores ao eventhub de telemetria</span><span class="sxs-lookup"><span data-stu-id="05eeb-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="05eeb-109">Adiciona um novo nome de consumidor chamado "myconsumero" ao eventhub para eventos de telemetria no iothub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="05eeb-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="05eeb-110">OS</span><span class="sxs-lookup"><span data-stu-id="05eeb-110">PARAMETERS</span></span>

### <span data-ttu-id="05eeb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05eeb-111">-DefaultProfile</span></span>
<span data-ttu-id="05eeb-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="05eeb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05eeb-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="05eeb-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="05eeb-114">Nome do meu consumidor do EventHub que você deseja adicionar.</span><span class="sxs-lookup"><span data-stu-id="05eeb-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

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

### <span data-ttu-id="05eeb-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="05eeb-115">-Name</span></span>
<span data-ttu-id="05eeb-116">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="05eeb-116">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="05eeb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05eeb-117">-ResourceGroupName</span></span>
<span data-ttu-id="05eeb-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="05eeb-118">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="05eeb-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="05eeb-119">-Confirm</span></span>
<span data-ttu-id="05eeb-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05eeb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05eeb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05eeb-121">-WhatIf</span></span>
<span data-ttu-id="05eeb-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="05eeb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05eeb-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="05eeb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05eeb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05eeb-124">CommonParameters</span></span>
<span data-ttu-id="05eeb-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05eeb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05eeb-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05eeb-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05eeb-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="05eeb-127">INPUTS</span></span>

### <span data-ttu-id="05eeb-128">System. String</span><span class="sxs-lookup"><span data-stu-id="05eeb-128">System.String</span></span>

## <span data-ttu-id="05eeb-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="05eeb-129">OUTPUTS</span></span>

### <span data-ttu-id="05eeb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="05eeb-130">System.String</span></span>

## <span data-ttu-id="05eeb-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="05eeb-131">NOTES</span></span>

## <span data-ttu-id="05eeb-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05eeb-132">RELATED LINKS</span></span>