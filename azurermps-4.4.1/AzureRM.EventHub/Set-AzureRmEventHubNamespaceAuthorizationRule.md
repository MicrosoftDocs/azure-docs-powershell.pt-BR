---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 52bf68f1105ea6aa6ec0a78fac1a75defa1d865a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441556"
---
# <span data-ttu-id="dcc15-101">Set-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="dcc15-101">Set-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="dcc15-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dcc15-102">SYNOPSIS</span></span>
<span data-ttu-id="dcc15-103">Atualiza a regra de autorização no namespace de hubs de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="dcc15-103">Updates the authorization rule on the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcc15-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dcc15-104">SYNTAX</span></span>

```
Set-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthRuleObj] <AuthorizationRuleAttributes> [[-AuthorizationRuleName] <String>] [-Rights <String[]>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="dcc15-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dcc15-105">DESCRIPTION</span></span>
<span data-ttu-id="dcc15-106">O cmdlet Set-AzureRmEventHubNamespaceAuthorizationRule atualiza a regra de autorização no namespace de hubs de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="dcc15-106">The Set-AzureRmEventHubNamespaceAuthorizationRule cmdlet updates the authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="dcc15-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dcc15-107">EXAMPLES</span></span>

### <span data-ttu-id="dcc15-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dcc15-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="dcc15-109">Atualiza a regra de autorização \` MyAuthRuleName \` para conceder direitos de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="dcc15-109">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights.</span></span>

## <span data-ttu-id="dcc15-110">OS</span><span class="sxs-lookup"><span data-stu-id="dcc15-110">PARAMETERS</span></span>

### <span data-ttu-id="dcc15-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="dcc15-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="dcc15-112">O nome da regra de autorização.</span><span class="sxs-lookup"><span data-stu-id="dcc15-112">The authorization rule name.</span></span>
<span data-ttu-id="dcc15-113">Obrigatório se-AuthruleObj não for especificado.</span><span class="sxs-lookup"><span data-stu-id="dcc15-113">Required if -AuthruleObj is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcc15-114">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="dcc15-114">-AuthRuleObj</span></span>
<span data-ttu-id="dcc15-115">O objeto de regra de autorização de namespace de hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="dcc15-115">The Event Hubs namespace authorization rule object.</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc15-116">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="dcc15-116">-NamespaceName</span></span>
<span data-ttu-id="dcc15-117">O nome do namespace dos hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="dcc15-117">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="dcc15-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcc15-118">-ResourceGroupName</span></span>
<span data-ttu-id="dcc15-119">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dcc15-119">Resource group name.</span></span>

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

### <span data-ttu-id="dcc15-120">-Direitos</span><span class="sxs-lookup"><span data-stu-id="dcc15-120">-Rights</span></span>
<span data-ttu-id="dcc15-121">Obrigatório se-AuthruleObj não for especificado.</span><span class="sxs-lookup"><span data-stu-id="dcc15-121">Required if -AuthruleObj is not specified.</span></span>
<span data-ttu-id="dcc15-122">Direitos por exemplo, @ ("Listen", "enviar", "gerenciar")</span><span class="sxs-lookup"><span data-stu-id="dcc15-122">Rights; for example,  @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcc15-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dcc15-123">-Confirm</span></span>
<span data-ttu-id="dcc15-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcc15-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcc15-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcc15-125">-WhatIf</span></span>
<span data-ttu-id="dcc15-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dcc15-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcc15-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dcc15-127">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="dcc15-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dcc15-128">INPUTS</span></span>

### <span data-ttu-id="dcc15-129">System. String</span><span class="sxs-lookup"><span data-stu-id="dcc15-129">System.String</span></span>

## <span data-ttu-id="dcc15-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dcc15-130">OUTPUTS</span></span>

### <span data-ttu-id="dcc15-131">Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="dcc15-131">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="dcc15-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dcc15-132">NOTES</span></span>

## <span data-ttu-id="dcc15-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dcc15-133">RELATED LINKS</span></span>

