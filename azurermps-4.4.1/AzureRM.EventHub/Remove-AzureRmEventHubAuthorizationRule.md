---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 439d4ea871d70fa830bb5a0f327cbc0f75d137df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441083"
---
# <span data-ttu-id="3ff27-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3ff27-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="3ff27-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ff27-102">SYNOPSIS</span></span>
<span data-ttu-id="3ff27-103">Remove a regra de autorização do hub de eventos especificada.</span><span class="sxs-lookup"><span data-stu-id="3ff27-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ff27-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ff27-104">SYNTAX</span></span>

### <span data-ttu-id="3ff27-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3ff27-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="3ff27-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3ff27-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="3ff27-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3ff27-107">DESCRIPTION</span></span>
<span data-ttu-id="3ff27-108">O cmdlet Remove-AzureRmEventHubAuthorizationRule remove e exclui a regra de autorização especificada do hub de eventos fornecido.</span><span class="sxs-lookup"><span data-stu-id="3ff27-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="3ff27-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ff27-109">EXAMPLES</span></span>

### <span data-ttu-id="3ff27-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3ff27-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

### <span data-ttu-id="3ff27-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3ff27-111">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="3ff27-112">Remove a regra de autorização \` MyAuthRuleName \` da MyEventHubName do hub de eventos \` \` .</span><span class="sxs-lookup"><span data-stu-id="3ff27-112">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="3ff27-113">OS</span><span class="sxs-lookup"><span data-stu-id="3ff27-113">PARAMETERS</span></span>

### <span data-ttu-id="3ff27-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ff27-114">-ResourceGroupName</span></span>
<span data-ttu-id="3ff27-115">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3ff27-115">Resource group name.</span></span>

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

### <span data-ttu-id="3ff27-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3ff27-116">-Confirm</span></span>
<span data-ttu-id="3ff27-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ff27-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ff27-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ff27-118">-WhatIf</span></span>
<span data-ttu-id="3ff27-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3ff27-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ff27-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3ff27-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ff27-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="3ff27-121">-EventHub</span></span>
<span data-ttu-id="3ff27-122">Nome do EventHub.</span><span class="sxs-lookup"><span data-stu-id="3ff27-122">EventHub Name.</span></span>

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

### <span data-ttu-id="3ff27-123">-Force</span><span class="sxs-lookup"><span data-stu-id="3ff27-123">-Force</span></span>
<span data-ttu-id="3ff27-124">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="3ff27-124">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ff27-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ff27-125">-Name</span></span>
<span data-ttu-id="3ff27-126">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="3ff27-126">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="3ff27-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3ff27-127">-Namespace</span></span>
<span data-ttu-id="3ff27-128">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="3ff27-128">Namespace Name.</span></span>

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

### <span data-ttu-id="3ff27-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ff27-129">-PassThru</span></span>
<span data-ttu-id="3ff27-130">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="3ff27-130">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="3ff27-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3ff27-131">INPUTS</span></span>

### <span data-ttu-id="3ff27-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3ff27-132">System.String</span></span>

## <span data-ttu-id="3ff27-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3ff27-133">OUTPUTS</span></span>

### <span data-ttu-id="3ff27-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3ff27-134">System.Boolean</span></span>

## <span data-ttu-id="3ff27-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3ff27-135">NOTES</span></span>

## <span data-ttu-id="3ff27-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ff27-136">RELATED LINKS</span></span>

