---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bbe600feb7618bef94a0d1799e1d2709ce7f0157
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441102"
---
# <span data-ttu-id="6a970-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="6a970-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="6a970-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6a970-102">SYNOPSIS</span></span>
<span data-ttu-id="6a970-103">Obtém os detalhes de um único Hub de eventos ou obtém uma lista de hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="6a970-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a970-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a970-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [-Name <String>]
```

## <span data-ttu-id="6a970-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6a970-105">DESCRIPTION</span></span>
<span data-ttu-id="6a970-106">O cmdlet Get-AzureRmEventHub retorna os detalhes de um hub de eventos ou uma lista de todos os hubs de eventos no namespace atual.</span><span class="sxs-lookup"><span data-stu-id="6a970-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="6a970-107">Se o nome do Hub do evento for fornecido, os detalhes de um único Hub de eventos serão retornados.</span><span class="sxs-lookup"><span data-stu-id="6a970-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="6a970-108">Se um nome de Hub de eventos não for fornecido, uma lista de todos os hubs de eventos no namespace especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="6a970-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="6a970-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6a970-109">EXAMPLES</span></span>

### <span data-ttu-id="6a970-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6a970-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="6a970-111">Retorna os detalhes do hub de eventos \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="6a970-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="6a970-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6a970-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="6a970-113">Retorna uma lista de hubs de eventos no namespace \` Mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="6a970-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="6a970-114">OS</span><span class="sxs-lookup"><span data-stu-id="6a970-114">PARAMETERS</span></span>

### <span data-ttu-id="6a970-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a970-115">-ResourceGroupName</span></span>
<span data-ttu-id="6a970-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6a970-116">Resource group name.</span></span>

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

### <span data-ttu-id="6a970-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a970-117">-Name</span></span>
<span data-ttu-id="6a970-118">Nome do EventHub.</span><span class="sxs-lookup"><span data-stu-id="6a970-118">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a970-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6a970-119">-Namespace</span></span>
<span data-ttu-id="6a970-120">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="6a970-120">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="6a970-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6a970-121">INPUTS</span></span>

### <span data-ttu-id="6a970-122">System. String</span><span class="sxs-lookup"><span data-stu-id="6a970-122">System.String</span></span>

## <span data-ttu-id="6a970-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6a970-123">OUTPUTS</span></span>

### <span data-ttu-id="6a970-124">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventHub. Models. EventHubAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6a970-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6a970-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6a970-125">NOTES</span></span>

## <span data-ttu-id="6a970-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6a970-126">RELATED LINKS</span></span>

