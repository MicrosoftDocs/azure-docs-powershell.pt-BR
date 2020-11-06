---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 4a980edd1833b37b358f86d2e3ccb6a9efc8d836
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603120"
---
# <span data-ttu-id="5b5bb-101">Remove-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5b5bb-101">Remove-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="5b5bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5b5bb-102">SYNOPSIS</span></span>
<span data-ttu-id="5b5bb-103">Exclui a regra de autorização especificada no namespace de hubs de eventos específico.</span><span class="sxs-lookup"><span data-stu-id="5b5bb-103">Deletes the specified authorization rule on the given Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b5bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b5bb-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="5b5bb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5b5bb-105">DESCRIPTION</span></span>
<span data-ttu-id="5b5bb-106">O cmdlet Remove-AzureRmEventHubNamespaceAuthorizationRule remove e exclui a regra de autorização especificada no namespace determinado de hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="5b5bb-106">The Remove-AzureRmEventHubNamespaceAuthorizationRule cmdlet removes and deletes the specified authorization rule on the given Event Hubs namespace.</span></span>

## <span data-ttu-id="5b5bb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5b5bb-107">EXAMPLES</span></span>

### <span data-ttu-id="5b5bb-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5b5bb-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="5b5bb-109">Remove a regra de autorização \` MyAuthRuleName \` do namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="5b5bb-109">Removes the authorization rule \`MyAuthRuleName\` from the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="5b5bb-110">OS</span><span class="sxs-lookup"><span data-stu-id="5b5bb-110">PARAMETERS</span></span>

### <span data-ttu-id="5b5bb-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="5b5bb-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="5b5bb-112">O nome da regra de autorização do namespace de hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="5b5bb-112">The Event Hubs namespace authorization rule name.</span></span>

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

### <span data-ttu-id="5b5bb-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="5b5bb-113">-NamespaceName</span></span>
<span data-ttu-id="5b5bb-114">O nome do namespace dos hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="5b5bb-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="5b5bb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b5bb-115">-ResourceGroupName</span></span>
<span data-ttu-id="5b5bb-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5b5bb-116">Resource group name.</span></span>

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

### <span data-ttu-id="5b5bb-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5b5bb-117">-Confirm</span></span>
<span data-ttu-id="5b5bb-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b5bb-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b5bb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b5bb-119">-WhatIf</span></span>
<span data-ttu-id="5b5bb-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5b5bb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b5bb-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5b5bb-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="5b5bb-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5b5bb-122">INPUTS</span></span>

### <span data-ttu-id="5b5bb-123">System. String</span><span class="sxs-lookup"><span data-stu-id="5b5bb-123">System.String</span></span>

## <span data-ttu-id="5b5bb-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5b5bb-124">OUTPUTS</span></span>

### <span data-ttu-id="5b5bb-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5b5bb-125">System.Boolean</span></span>

## <span data-ttu-id="5b5bb-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5b5bb-126">NOTES</span></span>

## <span data-ttu-id="5b5bb-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b5bb-127">RELATED LINKS</span></span>

