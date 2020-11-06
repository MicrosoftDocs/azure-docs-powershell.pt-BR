---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 5b88ce6edc92cb6483b8d6df95599fcea854f805
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430494"
---
# <span data-ttu-id="6bdaa-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="6bdaa-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="6bdaa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6bdaa-102">SYNOPSIS</span></span>
<span data-ttu-id="6bdaa-103">Exclui o grupo de consumidores dos hubs de eventos especificados.</span><span class="sxs-lookup"><span data-stu-id="6bdaa-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bdaa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6bdaa-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bdaa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6bdaa-105">DESCRIPTION</span></span>
<span data-ttu-id="6bdaa-106">O cmdlet Remove-AzureRmEventHubConsumerGroup remove e exclui o grupo consumidor especificado do hub de eventos fornecido.</span><span class="sxs-lookup"><span data-stu-id="6bdaa-106">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="6bdaa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6bdaa-107">EXAMPLES</span></span>

### <span data-ttu-id="6bdaa-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6bdaa-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="6bdaa-109">Exclui o \` MyConsumerGroupName do grupo \` do consumidor do MyEventHubName do hub de eventos \` \` , escopo do \` namespace mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="6bdaa-109">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

## <span data-ttu-id="6bdaa-110">OS</span><span class="sxs-lookup"><span data-stu-id="6bdaa-110">PARAMETERS</span></span>

### <span data-ttu-id="6bdaa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bdaa-111">-DefaultProfile</span></span>
<span data-ttu-id="6bdaa-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6bdaa-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bdaa-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="6bdaa-113">-EventHub</span></span>
<span data-ttu-id="6bdaa-114">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="6bdaa-114">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdaa-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6bdaa-115">-Name</span></span>
<span data-ttu-id="6bdaa-116">Nome do nome do consumidor</span><span class="sxs-lookup"><span data-stu-id="6bdaa-116">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdaa-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6bdaa-117">-Namespace</span></span>
<span data-ttu-id="6bdaa-118">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="6bdaa-118">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdaa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bdaa-119">-ResourceGroupName</span></span>
<span data-ttu-id="6bdaa-120">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6bdaa-120">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdaa-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6bdaa-121">-Confirm</span></span>
<span data-ttu-id="6bdaa-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bdaa-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bdaa-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bdaa-123">-WhatIf</span></span>
<span data-ttu-id="6bdaa-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6bdaa-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bdaa-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6bdaa-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bdaa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bdaa-126">CommonParameters</span></span>
<span data-ttu-id="6bdaa-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bdaa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6bdaa-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bdaa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bdaa-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6bdaa-129">INPUTS</span></span>

### <span data-ttu-id="6bdaa-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6bdaa-130">System.String</span></span>


## <span data-ttu-id="6bdaa-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6bdaa-131">OUTPUTS</span></span>

### <span data-ttu-id="6bdaa-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="6bdaa-132">System.Object</span></span>

## <span data-ttu-id="6bdaa-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6bdaa-133">NOTES</span></span>

## <span data-ttu-id="6bdaa-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6bdaa-134">RELATED LINKS</span></span>