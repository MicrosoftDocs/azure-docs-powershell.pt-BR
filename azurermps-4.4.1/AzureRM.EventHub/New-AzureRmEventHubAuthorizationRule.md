---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 3085479125219450368322ddb64fee4c06cdce2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603377"
---
# <span data-ttu-id="866c1-101">New-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="866c1-101">New-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="866c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="866c1-102">SYNOPSIS</span></span>
<span data-ttu-id="866c1-103">Cria uma nova regra de autorização de hubs de eventos para namespace ou eventhub.</span><span class="sxs-lookup"><span data-stu-id="866c1-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="866c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="866c1-104">SYNTAX</span></span>

### <span data-ttu-id="866c1-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="866c1-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 -Rights <String[]> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="866c1-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="866c1-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> -Rights <String[]> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="866c1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="866c1-107">DESCRIPTION</span></span>
<span data-ttu-id="866c1-108">O cmdlet New-AzureRmEventHubAuthorizationRule cria uma nova regra de autorização de hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="866c1-108">The New-AzureRmEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="866c1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="866c1-109">EXAMPLES</span></span>

### <span data-ttu-id="866c1-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="866c1-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="866c1-111">Cria uma regra de autorização \` MyAuthRuleName \` concedendo os direitos de escuta e envio ao namespace \` mynamespacename \` , com o grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="866c1-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="866c1-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="866c1-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="866c1-113">Cria uma regra de autorização \` MyAuthRuleName \` concedendo os direitos de escuta e envio ao Hub de eventos \` MyEventHubName \` no namespace \` mynamespacename \` , com o grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="866c1-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="866c1-114">OS</span><span class="sxs-lookup"><span data-stu-id="866c1-114">PARAMETERS</span></span>

### <span data-ttu-id="866c1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="866c1-115">-ResourceGroupName</span></span>
<span data-ttu-id="866c1-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="866c1-116">Resource group name.</span></span>

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

### <span data-ttu-id="866c1-117">-Direitos</span><span class="sxs-lookup"><span data-stu-id="866c1-117">-Rights</span></span>
<span data-ttu-id="866c1-118">Direitos por exemplo, @ ("Listen", "enviar", "gerenciar").</span><span class="sxs-lookup"><span data-stu-id="866c1-118">Rights; for example @("Listen","Send","Manage").</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="866c1-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="866c1-119">-Confirm</span></span>
<span data-ttu-id="866c1-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="866c1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="866c1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="866c1-121">-WhatIf</span></span>
<span data-ttu-id="866c1-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="866c1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="866c1-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="866c1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="866c1-124">-EventHub</span><span class="sxs-lookup"><span data-stu-id="866c1-124">-EventHub</span></span>
<span data-ttu-id="866c1-125">Nome do EventHub.</span><span class="sxs-lookup"><span data-stu-id="866c1-125">EventHub Name.</span></span>

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

### <span data-ttu-id="866c1-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="866c1-126">-Name</span></span>
<span data-ttu-id="866c1-127">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="866c1-127">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="866c1-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="866c1-128">-Namespace</span></span>
<span data-ttu-id="866c1-129">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="866c1-129">Namespace Name.</span></span>

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

## <span data-ttu-id="866c1-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="866c1-130">INPUTS</span></span>

### <span data-ttu-id="866c1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="866c1-131">System.String</span></span>

## <span data-ttu-id="866c1-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="866c1-132">OUTPUTS</span></span>

### <span data-ttu-id="866c1-133">Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="866c1-133">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="866c1-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="866c1-134">NOTES</span></span>

## <span data-ttu-id="866c1-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="866c1-135">RELATED LINKS</span></span>

