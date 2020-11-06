---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: dc384ca6056ef13d5517241d550bacddf2e7d0d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441088"
---
# <span data-ttu-id="7ba67-101">New-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7ba67-101">New-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="7ba67-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ba67-102">SYNOPSIS</span></span>
<span data-ttu-id="7ba67-103">Cria uma nova regra de autorização no namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="7ba67-103">Creates a new authorization rule on the specified namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ba67-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ba67-104">SYNTAX</span></span>

```
New-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-Rights] <String[]> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="7ba67-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ba67-105">DESCRIPTION</span></span>
<span data-ttu-id="7ba67-106">O cmdlet New-AzureRmEventHubNamespaceAuthorizationRule cria uma nova regra de autorização no namespace de hubs de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="7ba67-106">The New-AzureRmEventHubNamespaceAuthorizationRule cmdlet creates a new authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="7ba67-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ba67-107">EXAMPLES</span></span>

### <span data-ttu-id="7ba67-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7ba67-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="7ba67-109">Cria a regra de autorização \` MyAuthRuleName \` com os direitos de escuta e envio, para namespace de hubs de evento \` mynamespacename \` , no grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="7ba67-109">Creates the authorization rule \`MyAuthRuleName\` with Listen and Send rights, for Event Hubs namespace \`MyNamespaceName\`, in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="7ba67-110">OS</span><span class="sxs-lookup"><span data-stu-id="7ba67-110">PARAMETERS</span></span>

### <span data-ttu-id="7ba67-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="7ba67-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="7ba67-112">Nome da regra de autorização.</span><span class="sxs-lookup"><span data-stu-id="7ba67-112">Authorization rule name.</span></span>

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

### <span data-ttu-id="7ba67-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="7ba67-113">-NamespaceName</span></span>
<span data-ttu-id="7ba67-114">O nome do namespace dos hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="7ba67-114">The Event Hubs namespace name.</span></span>

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

### <span data-ttu-id="7ba67-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ba67-115">-ResourceGroupName</span></span>
<span data-ttu-id="7ba67-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7ba67-116">Resource group name.</span></span>

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

### <span data-ttu-id="7ba67-117">-Direitos</span><span class="sxs-lookup"><span data-stu-id="7ba67-117">-Rights</span></span>
<span data-ttu-id="7ba67-118">Direitos; por exemplo, @ ("Listen", "enviar", "gerenciar")</span><span class="sxs-lookup"><span data-stu-id="7ba67-118">Rights;for example,  @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ba67-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7ba67-119">-Confirm</span></span>
<span data-ttu-id="7ba67-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ba67-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ba67-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ba67-121">-WhatIf</span></span>
<span data-ttu-id="7ba67-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7ba67-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ba67-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7ba67-123">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="7ba67-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ba67-124">INPUTS</span></span>

### <span data-ttu-id="7ba67-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7ba67-125">System.String</span></span>

## <span data-ttu-id="7ba67-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ba67-126">OUTPUTS</span></span>

### <span data-ttu-id="7ba67-127">Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="7ba67-127">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="7ba67-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ba67-128">NOTES</span></span>

## <span data-ttu-id="7ba67-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ba67-129">RELATED LINKS</span></span>

