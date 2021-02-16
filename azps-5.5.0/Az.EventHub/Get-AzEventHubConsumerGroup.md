---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
ms.openlocfilehash: fc108c633b70cc1eed32bcc0574ad25109a065fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113203"
---
# <span data-ttu-id="07987-101">Get-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="07987-101">Get-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="07987-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07987-102">SYNOPSIS</span></span>
<span data-ttu-id="07987-103">Obtém os detalhes de um grupo de consumidores de Hubs de Eventos especificados ou obtém uma lista de grupos de consumidores em um Hub de Eventos.</span><span class="sxs-lookup"><span data-stu-id="07987-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

## <span data-ttu-id="07987-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07987-104">SYNTAX</span></span>

```
Get-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07987-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="07987-105">DESCRIPTION</span></span>
<span data-ttu-id="07987-106">O Get-AzEventHubConsumerGroup cmdlet obtém os detalhes de um grupo de consumidores de Hubs de Eventos especificado ou uma lista de grupos de consumidores em um determinado Hub de Eventos.</span><span class="sxs-lookup"><span data-stu-id="07987-106">The Get-AzEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="07987-107">Se o nome de um grupo de consumidores for fornecido, os detalhes de um único grupo de consumidores serão retornados.</span><span class="sxs-lookup"><span data-stu-id="07987-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="07987-108">Se o nome de um grupo de consumidores não for fornecido, uma lista de grupos de consumidores no Hub de Eventos especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="07987-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="07987-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="07987-109">EXAMPLES</span></span>

### <span data-ttu-id="07987-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="07987-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="07987-111">Obtém o grupo de consumidor MyConsumerGroupName no Hub de Eventos MyEventHubName, que existe no namespace MyNamespaceName com o grupo de recursos \` \` \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="07987-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="07987-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="07987-112">Example 2</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="07987-113">Obtém uma lista de grupos de consumidores no Hub de Eventos MyEventHubName, que existe no namespace MyNamespaceName com o grupo de recursos \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="07987-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="07987-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07987-114">PARAMETERS</span></span>

### <span data-ttu-id="07987-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07987-115">-DefaultProfile</span></span>
<span data-ttu-id="07987-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07987-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07987-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="07987-117">-EventHub</span></span>
<span data-ttu-id="07987-118">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="07987-118">EventHub Name</span></span>

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

### <span data-ttu-id="07987-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="07987-119">-MaxCount</span></span>
<span data-ttu-id="07987-120">Determine o número máximo de ConsumerGroups a retornar.</span><span class="sxs-lookup"><span data-stu-id="07987-120">Determine the maximum number of ConsumerGroups  to return.</span></span>

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

### <span data-ttu-id="07987-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="07987-121">-Name</span></span>
<span data-ttu-id="07987-122">Nome do Grupo do Consumidor</span><span class="sxs-lookup"><span data-stu-id="07987-122">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="07987-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="07987-123">-Namespace</span></span>
<span data-ttu-id="07987-124">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="07987-124">Namespace Name</span></span>

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

### <span data-ttu-id="07987-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07987-125">-ResourceGroupName</span></span>
<span data-ttu-id="07987-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="07987-126">Resource Group Name</span></span>

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

### <span data-ttu-id="07987-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07987-127">CommonParameters</span></span>
<span data-ttu-id="07987-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07987-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07987-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07987-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07987-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="07987-130">INPUTS</span></span>

### <span data-ttu-id="07987-131">System.String</span><span class="sxs-lookup"><span data-stu-id="07987-131">System.String</span></span>

## <span data-ttu-id="07987-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="07987-132">OUTPUTS</span></span>

### <span data-ttu-id="07987-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="07987-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="07987-134">Notas</span><span class="sxs-lookup"><span data-stu-id="07987-134">NOTES</span></span>

## <span data-ttu-id="07987-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07987-135">RELATED LINKS</span></span>
