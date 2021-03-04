---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
ms.openlocfilehash: 4b34731c0cd0c2d49a7c26112d370d8d4a2f948e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886045"
---
# <span data-ttu-id="95c58-101">Get-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="95c58-101">Get-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="95c58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95c58-102">SYNOPSIS</span></span>
<span data-ttu-id="95c58-103">Obtém os detalhes de um grupo de consumidores de Hubs de Eventos especificados ou obtém uma lista de grupos de consumidores em um Hub de Eventos.</span><span class="sxs-lookup"><span data-stu-id="95c58-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

## <span data-ttu-id="95c58-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="95c58-104">SYNTAX</span></span>

```
Get-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95c58-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="95c58-105">DESCRIPTION</span></span>
<span data-ttu-id="95c58-106">O Get-AzEventHubConsumerGroup cmdlet obtém os detalhes de um grupo de consumidores de Hubs de Eventos especificado ou uma lista de grupos de consumidores em um determinado Hub de Eventos.</span><span class="sxs-lookup"><span data-stu-id="95c58-106">The Get-AzEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="95c58-107">Se o nome de um grupo de consumidores for fornecido, os detalhes de um único grupo de consumidores serão retornados.</span><span class="sxs-lookup"><span data-stu-id="95c58-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="95c58-108">Se o nome de um grupo de consumidores não for fornecido, uma lista de grupos de consumidores no Hub de Eventos especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="95c58-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="95c58-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95c58-109">EXAMPLES</span></span>

### <span data-ttu-id="95c58-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="95c58-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="95c58-111">Obtém o grupo de consumidores MyConsumerGroupName no Hub de Eventos MyEventHubName , que existe no namespace MyNamespaceName com o grupo de recursos \` \` \` \` \` \` \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="95c58-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="95c58-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="95c58-112">Example 2</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="95c58-113">Obtém uma lista de grupos de consumidores no Hub de Eventos MyEventHubName , que existe no namespace MyNamespaceName com o grupo de recursos \` \` \` \` \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="95c58-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="95c58-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="95c58-114">PARAMETERS</span></span>

### <span data-ttu-id="95c58-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95c58-115">-DefaultProfile</span></span>
<span data-ttu-id="95c58-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="95c58-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95c58-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="95c58-117">-EventHub</span></span>
<span data-ttu-id="95c58-118">Nome eventHub</span><span class="sxs-lookup"><span data-stu-id="95c58-118">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95c58-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="95c58-119">-MaxCount</span></span>
<span data-ttu-id="95c58-120">Determine o número máximo de ConsumerGroups a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="95c58-120">Determine the maximum number of ConsumerGroups  to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95c58-121">-Name</span><span class="sxs-lookup"><span data-stu-id="95c58-121">-Name</span></span>
<span data-ttu-id="95c58-122">Nome do ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="95c58-122">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95c58-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="95c58-123">-Namespace</span></span>
<span data-ttu-id="95c58-124">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="95c58-124">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95c58-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95c58-125">-ResourceGroupName</span></span>
<span data-ttu-id="95c58-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="95c58-126">Resource Group Name</span></span>

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

### <span data-ttu-id="95c58-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95c58-127">CommonParameters</span></span>
<span data-ttu-id="95c58-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95c58-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95c58-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95c58-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95c58-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95c58-130">INPUTS</span></span>

### <span data-ttu-id="95c58-131">System.String</span><span class="sxs-lookup"><span data-stu-id="95c58-131">System.String</span></span>

## <span data-ttu-id="95c58-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="95c58-132">OUTPUTS</span></span>

### <span data-ttu-id="95c58-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="95c58-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="95c58-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="95c58-134">NOTES</span></span>

## <span data-ttu-id="95c58-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95c58-135">RELATED LINKS</span></span>
