---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: d69e30ff993d2e07c7711d36d8e5ec889bc0f7c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892640"
---
# <span data-ttu-id="7ede4-101">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="7ede4-101">Get-AzEventHub</span></span>

## <span data-ttu-id="7ede4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ede4-102">SYNOPSIS</span></span>
<span data-ttu-id="7ede4-103">Obtém os detalhes de um único Hub de Eventos ou obtém uma lista de Hubs de Eventos.</span><span class="sxs-lookup"><span data-stu-id="7ede4-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

## <span data-ttu-id="7ede4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7ede4-104">SYNTAX</span></span>

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ede4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7ede4-105">DESCRIPTION</span></span>
<span data-ttu-id="7ede4-106">O Get-AzEventHub cmdlet retorna os detalhes de um Hub de Eventos ou uma lista de todos os Hubs de Eventos no namespace atual.</span><span class="sxs-lookup"><span data-stu-id="7ede4-106">The Get-AzEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="7ede4-107">Se o nome do Hub de Eventos for fornecido, os detalhes de um único Hub de Eventos serão retornados.</span><span class="sxs-lookup"><span data-stu-id="7ede4-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="7ede4-108">Se um nome do Hub de Eventos não for fornecido, uma lista de todos os Hubs de Eventos no namespace especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="7ede4-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="7ede4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ede4-109">EXAMPLES</span></span>

### <span data-ttu-id="7ede4-110">Exemplo 1: EventHub especificado</span><span class="sxs-lookup"><span data-stu-id="7ede4-110">Example 1: specified EventHub</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="7ede4-111">Retorna os detalhes do Hub de Eventos \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="7ede4-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="7ede4-112">Exemplo 2: Lista de EventHub no Namespace especificado</span><span class="sxs-lookup"><span data-stu-id="7ede4-112">Example 2: List of EventHub in specified Namespace</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="7ede4-113">Retorna uma lista de Hubs de Eventos no namespace \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="7ede4-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="7ede4-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7ede4-114">PARAMETERS</span></span>

### <span data-ttu-id="7ede4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ede4-115">-DefaultProfile</span></span>
<span data-ttu-id="7ede4-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ede4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ede4-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="7ede4-117">-MaxCount</span></span>
<span data-ttu-id="7ede4-118">Determine o número máximo de EventHubs a ser retornada.</span><span class="sxs-lookup"><span data-stu-id="7ede4-118">Determine the maximum number of EventHubs to return.</span></span>

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

### <span data-ttu-id="7ede4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7ede4-119">-Name</span></span>
<span data-ttu-id="7ede4-120">Nome eventHub</span><span class="sxs-lookup"><span data-stu-id="7ede4-120">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ede4-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7ede4-121">-Namespace</span></span>
<span data-ttu-id="7ede4-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="7ede4-122">Namespace Name</span></span>

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

### <span data-ttu-id="7ede4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ede4-123">-ResourceGroupName</span></span>
<span data-ttu-id="7ede4-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="7ede4-124">Resource Group Name</span></span>

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

### <span data-ttu-id="7ede4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ede4-125">CommonParameters</span></span>
<span data-ttu-id="7ede4-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ede4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ede4-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ede4-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ede4-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ede4-128">INPUTS</span></span>

### <span data-ttu-id="7ede4-129">System.String</span><span class="sxs-lookup"><span data-stu-id="7ede4-129">System.String</span></span>

## <span data-ttu-id="7ede4-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7ede4-130">OUTPUTS</span></span>

### <span data-ttu-id="7ede4-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="7ede4-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="7ede4-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="7ede4-132">NOTES</span></span>

## <span data-ttu-id="7ede4-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ede4-133">RELATED LINKS</span></span>
