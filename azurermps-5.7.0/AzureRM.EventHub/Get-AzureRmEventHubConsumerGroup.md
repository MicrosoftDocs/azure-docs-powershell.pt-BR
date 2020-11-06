---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 445d20453b9f3d99e4ff5c72e118b287f0a83898
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439876"
---
# <span data-ttu-id="28834-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="28834-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="28834-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="28834-102">SYNOPSIS</span></span>
<span data-ttu-id="28834-103">Obtém os detalhes de um grupo de consumidores de hubs de eventos especificado ou obtém uma lista de grupos de consumidores em um hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="28834-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28834-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28834-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28834-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="28834-105">DESCRIPTION</span></span>
<span data-ttu-id="28834-106">O cmdlet Get-AzureRmEventHubConsumerGroup Obtém os detalhes de um grupo de consumidores de hubs de eventos especificado ou uma lista de grupos de consumidores em um determinado Hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="28834-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="28834-107">Se o nome de um grupo de consumidores for fornecido, os detalhes dos detalhes de um único grupo de consumidores serão retornados.</span><span class="sxs-lookup"><span data-stu-id="28834-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="28834-108">Se o nome de um grupo de consumidores não for fornecido, uma lista de grupos de consumidores no Hub de eventos especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="28834-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="28834-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28834-109">EXAMPLES</span></span>

### <span data-ttu-id="28834-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="28834-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="28834-111">Obtém o grupo do consumidor \` MyConsumerGroupName \` no Hub de eventos \` MyEventHubName \` , que existe no namespace \` mynamespacename \` com o grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="28834-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="28834-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="28834-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="28834-113">Obtém uma lista de grupos de consumidores no Hub de eventos \` MyEventHubName \` , que existe no namespace \` mynamespacename \` com o grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="28834-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="28834-114">OS</span><span class="sxs-lookup"><span data-stu-id="28834-114">PARAMETERS</span></span>

### <span data-ttu-id="28834-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28834-115">-DefaultProfile</span></span>
<span data-ttu-id="28834-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="28834-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28834-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="28834-117">-EventHub</span></span>
<span data-ttu-id="28834-118">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="28834-118">EventHub Name</span></span>

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

### <span data-ttu-id="28834-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="28834-119">-Name</span></span>
<span data-ttu-id="28834-120">Nome do nome do consumidor</span><span class="sxs-lookup"><span data-stu-id="28834-120">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28834-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="28834-121">-Namespace</span></span>
<span data-ttu-id="28834-122">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="28834-122">Namespace Name</span></span>

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

### <span data-ttu-id="28834-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28834-123">-ResourceGroupName</span></span>
<span data-ttu-id="28834-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="28834-124">Resource Group Name</span></span>

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

### <span data-ttu-id="28834-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28834-125">CommonParameters</span></span>
<span data-ttu-id="28834-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28834-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="28834-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28834-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28834-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="28834-128">INPUTS</span></span>

### <span data-ttu-id="28834-129">System. String</span><span class="sxs-lookup"><span data-stu-id="28834-129">System.String</span></span>


## <span data-ttu-id="28834-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="28834-130">OUTPUTS</span></span>

### <span data-ttu-id="28834-131">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="28834-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="28834-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="28834-132">NOTES</span></span>

## <span data-ttu-id="28834-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28834-133">RELATED LINKS</span></span>
