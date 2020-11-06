---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
ms.openlocfilehash: e87300af80c38fa0f7989836c992fd1baa53ba6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429793"
---
# <span data-ttu-id="bad31-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="bad31-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="bad31-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bad31-102">SYNOPSIS</span></span>
<span data-ttu-id="bad31-103">Obtém os detalhes de um único Hub de eventos ou obtém uma lista de hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="bad31-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bad31-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bad31-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bad31-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bad31-105">DESCRIPTION</span></span>
<span data-ttu-id="bad31-106">O cmdlet Get-AzureRmEventHub retorna os detalhes de um hub de eventos ou uma lista de todos os hubs de eventos no namespace atual.</span><span class="sxs-lookup"><span data-stu-id="bad31-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="bad31-107">Se o nome do Hub do evento for fornecido, os detalhes de um único Hub de eventos serão retornados.</span><span class="sxs-lookup"><span data-stu-id="bad31-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="bad31-108">Se um nome de Hub de eventos não for fornecido, uma lista de todos os hubs de eventos no namespace especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="bad31-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="bad31-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bad31-109">EXAMPLES</span></span>

### <span data-ttu-id="bad31-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bad31-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="bad31-111">Retorna os detalhes do hub de eventos \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="bad31-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="bad31-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bad31-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="bad31-113">Retorna uma lista de hubs de eventos no namespace \` Mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="bad31-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="bad31-114">OS</span><span class="sxs-lookup"><span data-stu-id="bad31-114">PARAMETERS</span></span>

### <span data-ttu-id="bad31-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bad31-115">-DefaultProfile</span></span>
<span data-ttu-id="bad31-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bad31-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bad31-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="bad31-117">-Name</span></span>
<span data-ttu-id="bad31-118">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="bad31-118">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bad31-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bad31-119">-Namespace</span></span>
<span data-ttu-id="bad31-120">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="bad31-120">Namespace Name</span></span>

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

### <span data-ttu-id="bad31-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bad31-121">-ResourceGroupName</span></span>
<span data-ttu-id="bad31-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="bad31-122">Resource Group Name</span></span>

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

### <span data-ttu-id="bad31-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bad31-123">CommonParameters</span></span>
<span data-ttu-id="bad31-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bad31-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bad31-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bad31-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bad31-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bad31-126">INPUTS</span></span>

### <span data-ttu-id="bad31-127">System. String</span><span class="sxs-lookup"><span data-stu-id="bad31-127">System.String</span></span>


## <span data-ttu-id="bad31-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bad31-128">OUTPUTS</span></span>

### <span data-ttu-id="bad31-129">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bad31-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="bad31-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bad31-130">NOTES</span></span>

## <span data-ttu-id="bad31-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bad31-131">RELATED LINKS</span></span>
