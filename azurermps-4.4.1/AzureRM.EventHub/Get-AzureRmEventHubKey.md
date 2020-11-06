---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: f4f28ee3f07127803e6187f00565ee8d4caf3084
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441097"
---
# <span data-ttu-id="5a088-101">Get-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="5a088-101">Get-AzureRmEventHubKey</span></span>

## <span data-ttu-id="5a088-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5a088-102">SYNOPSIS</span></span>
<span data-ttu-id="5a088-103">Obtém os detalhes da chave primária da regra de autorização dos hubs de eventos especificados.</span><span class="sxs-lookup"><span data-stu-id="5a088-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a088-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a088-104">SYNTAX</span></span>

### <span data-ttu-id="5a088-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5a088-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> -Namespace <String> -Name <String>
```

### <span data-ttu-id="5a088-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5a088-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String> -Name <String>
```

## <span data-ttu-id="5a088-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5a088-107">DESCRIPTION</span></span>
<span data-ttu-id="5a088-108">O cmdlet Get-AzureRmEventHubKey retorna connectionStrings primárias e secundárias e detalhes de chaves da regra de autorização de hubs de eventos especificados.</span><span class="sxs-lookup"><span data-stu-id="5a088-108">The Get-AzureRmEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="5a088-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5a088-109">EXAMPLES</span></span>

### <span data-ttu-id="5a088-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5a088-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="5a088-111">Obtém detalhes de connectionStrings primárias e secundárias e chaves para a regra de autorização \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="5a088-111">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="5a088-112">OS</span><span class="sxs-lookup"><span data-stu-id="5a088-112">PARAMETERS</span></span>

### <span data-ttu-id="5a088-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a088-113">-ResourceGroupName</span></span>
<span data-ttu-id="5a088-114">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5a088-114">Resource group name.</span></span>

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

### <span data-ttu-id="5a088-115">-EventHub</span><span class="sxs-lookup"><span data-stu-id="5a088-115">-EventHub</span></span>
<span data-ttu-id="5a088-116">Nome do EventHub.</span><span class="sxs-lookup"><span data-stu-id="5a088-116">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a088-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a088-117">-Name</span></span>
<span data-ttu-id="5a088-118">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="5a088-118">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a088-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5a088-119">-Namespace</span></span>
<span data-ttu-id="5a088-120">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="5a088-120">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="5a088-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5a088-121">INPUTS</span></span>

### <span data-ttu-id="5a088-122">System. String</span><span class="sxs-lookup"><span data-stu-id="5a088-122">System.String</span></span>

## <span data-ttu-id="5a088-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5a088-123">OUTPUTS</span></span>

### <span data-ttu-id="5a088-124">Microsoft. Azure. Commands. EventHub. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="5a088-124">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="5a088-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5a088-125">NOTES</span></span>

## <span data-ttu-id="5a088-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a088-126">RELATED LINKS</span></span>

