---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 205dc883f8f6e0481f88438137ca45ad7a99c4ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602939"
---
# <span data-ttu-id="465cd-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="465cd-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="465cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="465cd-102">SYNOPSIS</span></span>
<span data-ttu-id="465cd-103">Obtém os detalhes de um grupo de consumidores de hubs de eventos especificado ou obtém uma lista de grupos de consumidores em um hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="465cd-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="465cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="465cd-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="465cd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="465cd-105">DESCRIPTION</span></span>
<span data-ttu-id="465cd-106">O cmdlet Get-AzureRmEventHubConsumerGroup Obtém os detalhes de um grupo de consumidores de hubs de eventos especificado ou uma lista de grupos de consumidores em um determinado Hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="465cd-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="465cd-107">Se o nome de um grupo de consumidores for fornecido, os detalhes dos detalhes de um único grupo de consumidores serão retornados.</span><span class="sxs-lookup"><span data-stu-id="465cd-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="465cd-108">Se o nome de um grupo de consumidores não for fornecido, uma lista de grupos de consumidores no Hub de eventos especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="465cd-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="465cd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="465cd-109">EXAMPLES</span></span>

### <span data-ttu-id="465cd-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="465cd-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="465cd-111">Obtém o grupo do consumidor \` MyConsumerGroupName \` no Hub de eventos \` MyEventHubName \` , que existe no namespace \` mynamespacename \` com o grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="465cd-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="465cd-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="465cd-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="465cd-113">Obtém uma lista de grupos de consumidores no Hub de eventos \` MyEventHubName \` , que existe no namespace \` mynamespacename \` com o grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="465cd-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="465cd-114">OS</span><span class="sxs-lookup"><span data-stu-id="465cd-114">PARAMETERS</span></span>

### <span data-ttu-id="465cd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="465cd-115">-DefaultProfile</span></span>
<span data-ttu-id="465cd-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="465cd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="465cd-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="465cd-117">-EventHub</span></span>
<span data-ttu-id="465cd-118">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="465cd-118">EventHub Name</span></span>

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

### <span data-ttu-id="465cd-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="465cd-119">-MaxCount</span></span>
<span data-ttu-id="465cd-120">Determine o número máximo de ConsumerGroups a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="465cd-120">Determine the maximum number of ConsumerGroups  to return.</span></span>

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

### <span data-ttu-id="465cd-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="465cd-121">-Name</span></span>
<span data-ttu-id="465cd-122">Nome do nome do consumidor</span><span class="sxs-lookup"><span data-stu-id="465cd-122">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="465cd-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="465cd-123">-Namespace</span></span>
<span data-ttu-id="465cd-124">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="465cd-124">Namespace Name</span></span>

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

### <span data-ttu-id="465cd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="465cd-125">-ResourceGroupName</span></span>
<span data-ttu-id="465cd-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="465cd-126">Resource Group Name</span></span>

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

### <span data-ttu-id="465cd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="465cd-127">CommonParameters</span></span>
<span data-ttu-id="465cd-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="465cd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="465cd-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="465cd-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="465cd-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="465cd-130">INPUTS</span></span>

### <span data-ttu-id="465cd-131">System. String</span><span class="sxs-lookup"><span data-stu-id="465cd-131">System.String</span></span>

## <span data-ttu-id="465cd-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="465cd-132">OUTPUTS</span></span>

### <span data-ttu-id="465cd-133">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="465cd-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="465cd-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="465cd-134">NOTES</span></span>

## <span data-ttu-id="465cd-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="465cd-135">RELATED LINKS</span></span>
