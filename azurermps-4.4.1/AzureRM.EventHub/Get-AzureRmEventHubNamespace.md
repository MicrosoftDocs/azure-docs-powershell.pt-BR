---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 971312367815c8dc9c8c4f3f8fb6f2face0b7408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439945"
---
# <span data-ttu-id="02695-101">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="02695-101">Get-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="02695-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02695-102">SYNOPSIS</span></span>
<span data-ttu-id="02695-103">Obtém os detalhes de um namespace de hubs de eventos ou obtém uma lista de todos os namespaces de hubs de eventos na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="02695-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02695-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02695-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespace [[-ResourceGroupName] <String>] [-Name <String>]
```

## <span data-ttu-id="02695-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02695-105">DESCRIPTION</span></span>
<span data-ttu-id="02695-106">O cmdlet Get-AzureRmEventHubNamespace Obtém os detalhes de um namespace de hubs de eventos especificado ou uma lista de todos os namespaces de hubs de eventos na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="02695-106">The Get-AzureRmEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="02695-107">Se o nome do namespace for fornecido, os detalhes de um único namespace de hubs de eventos serão retornados.</span><span class="sxs-lookup"><span data-stu-id="02695-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="02695-108">Se o nome do namespace não for fornecido, uma lista de namespaces será retornada.</span><span class="sxs-lookup"><span data-stu-id="02695-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="02695-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02695-109">EXAMPLES</span></span>

### <span data-ttu-id="02695-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="02695-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="02695-111">Obtém os detalhes do namespace de hubs de evento \` Mynamespacename \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="02695-111">Gets the details of the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="02695-112">OS</span><span class="sxs-lookup"><span data-stu-id="02695-112">PARAMETERS</span></span>

### <span data-ttu-id="02695-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02695-113">-ResourceGroupName</span></span>
<span data-ttu-id="02695-114">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="02695-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02695-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="02695-115">-Name</span></span>
<span data-ttu-id="02695-116">Nome do namespace do EventHub.</span><span class="sxs-lookup"><span data-stu-id="02695-116">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="02695-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02695-117">INPUTS</span></span>

### <span data-ttu-id="02695-118">System. String</span><span class="sxs-lookup"><span data-stu-id="02695-118">System.String</span></span>

## <span data-ttu-id="02695-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02695-119">OUTPUTS</span></span>

### <span data-ttu-id="02695-120">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. EventHub. Models. Namespaceattributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="02695-120">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="02695-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02695-121">NOTES</span></span>

## <span data-ttu-id="02695-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02695-122">RELATED LINKS</span></span>

