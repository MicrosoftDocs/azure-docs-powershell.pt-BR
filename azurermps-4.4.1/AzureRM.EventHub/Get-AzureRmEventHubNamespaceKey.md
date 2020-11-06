---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e91b7edacc575ac98eb78ae44c88be4f6873f34c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441092"
---
# <span data-ttu-id="a600f-101">Get-AzureRmEventHubNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="a600f-101">Get-AzureRmEventHubNamespaceKey</span></span>

## <span data-ttu-id="a600f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a600f-102">SYNOPSIS</span></span>
<span data-ttu-id="a600f-103">Obtém detalhes das chaves e connectionStrings primárias e secundárias da regra de autorização da regra de autorização de namespace dos hubs de eventos especificados.</span><span class="sxs-lookup"><span data-stu-id="a600f-103">Gets details of Primary, Secondary connectionstrings and keys for the authorization rule of the specified Event Hubs namespace authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a600f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a600f-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespaceKey [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String>
```

## <span data-ttu-id="a600f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a600f-105">DESCRIPTION</span></span>
<span data-ttu-id="a600f-106">O cmdlet Get-AzureRmEventHubNamespaceKey retorna os connectionStrings primário e secundário e os detalhes de chaves da regra de autorização especificada no namespace de hubs de eventos fornecido.</span><span class="sxs-lookup"><span data-stu-id="a600f-106">The Get-AzureRmEventHubNamespaceKey cmdlet returns the Primary and Secondary connectionstrings and keys details of the specified authorization rule in the given Event Hubs namespace.</span></span>

## <span data-ttu-id="a600f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a600f-107">EXAMPLES</span></span>

### <span data-ttu-id="a600f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a600f-108">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="a600f-109">Obtém detalhes das chaves e connectionStrings primárias e secundárias da regra de autorização \` MyAuthRuleName \` no namespace de hubs de evento \` mynamespacename \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="a600f-109">Gets details of Primary, Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\` on the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="a600f-110">OS</span><span class="sxs-lookup"><span data-stu-id="a600f-110">PARAMETERS</span></span>

### <span data-ttu-id="a600f-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="a600f-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="a600f-112">O nome da regra de autorização no namespace de hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="a600f-112">The name of the authorization rule on the Event Hubs namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a600f-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="a600f-113">-NamespaceName</span></span>
<span data-ttu-id="a600f-114">O nome do namespace dos hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="a600f-114">The Event Hubs namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a600f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a600f-115">-ResourceGroupName</span></span>
<span data-ttu-id="a600f-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a600f-116">Resource group name.</span></span>

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

## <span data-ttu-id="a600f-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a600f-117">INPUTS</span></span>

### <span data-ttu-id="a600f-118">System. String</span><span class="sxs-lookup"><span data-stu-id="a600f-118">System.String</span></span>

## <span data-ttu-id="a600f-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a600f-119">OUTPUTS</span></span>

### <span data-ttu-id="a600f-120">Microsoft. Azure. Commands. EventHub. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="a600f-120">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="a600f-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a600f-121">NOTES</span></span>

## <span data-ttu-id="a600f-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a600f-122">RELATED LINKS</span></span>

