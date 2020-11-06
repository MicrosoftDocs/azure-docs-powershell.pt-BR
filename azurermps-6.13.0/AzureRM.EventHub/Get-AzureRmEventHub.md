---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
ms.openlocfilehash: 6ae26d1d5061989ac93756812cf48494e9101978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602942"
---
# <span data-ttu-id="29065-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="29065-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="29065-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29065-102">SYNOPSIS</span></span>
<span data-ttu-id="29065-103">Obtém os detalhes de um único Hub de eventos ou obtém uma lista de hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="29065-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29065-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29065-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29065-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29065-105">DESCRIPTION</span></span>
<span data-ttu-id="29065-106">O cmdlet Get-AzureRmEventHub retorna os detalhes de um hub de eventos ou uma lista de todos os hubs de eventos no namespace atual.</span><span class="sxs-lookup"><span data-stu-id="29065-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="29065-107">Se o nome do Hub do evento for fornecido, os detalhes de um único Hub de eventos serão retornados.</span><span class="sxs-lookup"><span data-stu-id="29065-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="29065-108">Se um nome de Hub de eventos não for fornecido, uma lista de todos os hubs de eventos no namespace especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="29065-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="29065-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29065-109">EXAMPLES</span></span>

### <span data-ttu-id="29065-110">Exemplo 1-EventHub especificado</span><span class="sxs-lookup"><span data-stu-id="29065-110">Example 1 - specified EventHub</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="29065-111">Retorna os detalhes do hub de eventos \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="29065-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="29065-112">Exemplo 2-lista de EventHub no namespace especificado</span><span class="sxs-lookup"><span data-stu-id="29065-112">Example 2 - List of EventHub in specified Namespace</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="29065-113">Retorna uma lista de hubs de eventos no namespace \` Mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="29065-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="29065-114">OS</span><span class="sxs-lookup"><span data-stu-id="29065-114">PARAMETERS</span></span>

### <span data-ttu-id="29065-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29065-115">-DefaultProfile</span></span>
<span data-ttu-id="29065-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29065-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29065-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="29065-117">-MaxCount</span></span>
<span data-ttu-id="29065-118">Determine o número máximo de EventHubs a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="29065-118">Determine the maximum number of EventHubs to return.</span></span>

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

### <span data-ttu-id="29065-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="29065-119">-Name</span></span>
<span data-ttu-id="29065-120">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="29065-120">EventHub Name</span></span>

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

### <span data-ttu-id="29065-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="29065-121">-Namespace</span></span>
<span data-ttu-id="29065-122">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="29065-122">Namespace Name</span></span>

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

### <span data-ttu-id="29065-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29065-123">-ResourceGroupName</span></span>
<span data-ttu-id="29065-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="29065-124">Resource Group Name</span></span>

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

### <span data-ttu-id="29065-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29065-125">CommonParameters</span></span>
<span data-ttu-id="29065-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29065-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29065-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29065-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29065-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29065-128">INPUTS</span></span>

### <span data-ttu-id="29065-129">System. String</span><span class="sxs-lookup"><span data-stu-id="29065-129">System.String</span></span>

## <span data-ttu-id="29065-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29065-130">OUTPUTS</span></span>

### <span data-ttu-id="29065-131">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="29065-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="29065-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29065-132">NOTES</span></span>

## <span data-ttu-id="29065-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29065-133">RELATED LINKS</span></span>
