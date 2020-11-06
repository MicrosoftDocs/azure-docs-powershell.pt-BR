---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e4600b44943170256d2c8ef999496d2160e369ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432220"
---
# <span data-ttu-id="e0516-101">Set-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e0516-101">Set-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="e0516-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0516-102">SYNOPSIS</span></span>
<span data-ttu-id="e0516-103">Atualiza a regra de autorização especificada em um hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="e0516-103">Updates the specified authorization rule on an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0516-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0516-104">SYNTAX</span></span>

### <span data-ttu-id="e0516-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e0516-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e0516-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e0516-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e0516-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e0516-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Name <String>
 -InputObject <AuthorizationRuleAttributes> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e0516-108">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="e0516-108">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Name <String> -Rights <String[]> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="e0516-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e0516-109">DESCRIPTION</span></span>
<span data-ttu-id="e0516-110">O cmdlet Set-AzureRmEventHubAuthorizationRule atualiza a regra de autorização especificada em um determinado Hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="e0516-110">The Set-AzureRmEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="e0516-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0516-111">EXAMPLES</span></span>

### <span data-ttu-id="e0516-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e0516-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="e0516-113">Atualiza a regra de autorização \` MyAuthRuleName \` para conceder direitos de gerenciamento ao Hub de eventos \` MyEventHubName \` , delimitado pelo namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="e0516-113">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="e0516-114">OS</span><span class="sxs-lookup"><span data-stu-id="e0516-114">PARAMETERS</span></span>

### <span data-ttu-id="e0516-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0516-115">-ResourceGroupName</span></span>
<span data-ttu-id="e0516-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0516-116">Resource group name.</span></span>

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

### <span data-ttu-id="e0516-117">-Direitos</span><span class="sxs-lookup"><span data-stu-id="e0516-117">-Rights</span></span>
<span data-ttu-id="e0516-118">Obrigatório se ' AuthruleObj ' não especificado.</span><span class="sxs-lookup"><span data-stu-id="e0516-118">Required if 'AuthruleObj' not specified.</span></span>
<span data-ttu-id="e0516-119">Direitos por exemplo, @ ("Listen", "enviar", "gerenciar")</span><span class="sxs-lookup"><span data-stu-id="e0516-119">Rights; for example, @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0516-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e0516-120">-Confirm</span></span>
<span data-ttu-id="e0516-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0516-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0516-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0516-122">-WhatIf</span></span>
<span data-ttu-id="e0516-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e0516-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0516-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e0516-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0516-125">-EventHub</span><span class="sxs-lookup"><span data-stu-id="e0516-125">-EventHub</span></span>
<span data-ttu-id="e0516-126">Nome do EventHub.</span><span class="sxs-lookup"><span data-stu-id="e0516-126">EventHub Name.</span></span>

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

### <span data-ttu-id="e0516-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0516-127">-InputObject</span></span>
<span data-ttu-id="e0516-128">{{Fillobject descrição da entrada}}</span><span class="sxs-lookup"><span data-stu-id="e0516-128">{{Fill InputObject Description}}</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0516-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0516-129">-Name</span></span>
<span data-ttu-id="e0516-130">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="e0516-130">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="e0516-131">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e0516-131">-Namespace</span></span>
<span data-ttu-id="e0516-132">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="e0516-132">Namespace Name.</span></span>

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

## <span data-ttu-id="e0516-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e0516-133">INPUTS</span></span>

### <span data-ttu-id="e0516-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e0516-134">System.String</span></span>

## <span data-ttu-id="e0516-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e0516-135">OUTPUTS</span></span>

### <span data-ttu-id="e0516-136">Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e0516-136">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="e0516-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e0516-137">NOTES</span></span>

## <span data-ttu-id="e0516-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0516-138">RELATED LINKS</span></span>

