---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
ms.openlocfilehash: ef71b8ce2f90fb6275c3bd658289f4e32579cd69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892171"
---
# <span data-ttu-id="4ab70-101">Set-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4ab70-101">Set-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="4ab70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ab70-102">SYNOPSIS</span></span>
<span data-ttu-id="4ab70-103">Atualiza a regra de autorização especificada em um Hub de Eventos.</span><span class="sxs-lookup"><span data-stu-id="4ab70-103">Updates the specified authorization rule on an Event Hub.</span></span>

## <span data-ttu-id="4ab70-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4ab70-104">SYNTAX</span></span>

### <span data-ttu-id="4ab70-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4ab70-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ab70-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="4ab70-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ab70-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4ab70-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ab70-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4ab70-108">DESCRIPTION</span></span>
<span data-ttu-id="4ab70-109">O Set-AzEventHubAuthorizationRule cmdlet atualiza a regra de autorização especificada no Hub de Eventos determinado.</span><span class="sxs-lookup"><span data-stu-id="4ab70-109">The Set-AzEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="4ab70-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ab70-110">EXAMPLES</span></span>

### <span data-ttu-id="4ab70-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4ab70-111">Example 1</span></span>
```
PS C:\> Set-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="4ab70-112">Atualiza a regra de autorização MyAuthRuleName para conceder direitos de Gerenciar para o Hub de \` Eventos MyEventHubName , com escopo pelo \` \` \` namespace \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="4ab70-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="4ab70-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4ab70-113">PARAMETERS</span></span>

### <span data-ttu-id="4ab70-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ab70-114">-DefaultProfile</span></span>
<span data-ttu-id="4ab70-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4ab70-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ab70-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="4ab70-116">-EventHub</span></span>
<span data-ttu-id="4ab70-117">Nome eventHub</span><span class="sxs-lookup"><span data-stu-id="4ab70-117">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ab70-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ab70-118">-InputObject</span></span>
<span data-ttu-id="4ab70-119">Objeto AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4ab70-119">AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ab70-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4ab70-120">-Name</span></span>
<span data-ttu-id="4ab70-121">Nome authorizationRule</span><span class="sxs-lookup"><span data-stu-id="4ab70-121">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ab70-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4ab70-122">-Namespace</span></span>
<span data-ttu-id="4ab70-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="4ab70-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ab70-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ab70-124">-ResourceGroupName</span></span>
<span data-ttu-id="4ab70-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="4ab70-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ab70-126">-Rights</span><span class="sxs-lookup"><span data-stu-id="4ab70-126">-Rights</span></span>
<span data-ttu-id="4ab70-127">Direitos, por exemplo, @("Listen","Send","Manage")</span><span class="sxs-lookup"><span data-stu-id="4ab70-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ab70-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ab70-128">-Confirm</span></span>
<span data-ttu-id="4ab70-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ab70-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ab70-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ab70-130">-WhatIf</span></span>
<span data-ttu-id="4ab70-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4ab70-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ab70-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4ab70-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ab70-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ab70-133">CommonParameters</span></span>
<span data-ttu-id="4ab70-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ab70-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ab70-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ab70-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ab70-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ab70-136">INPUTS</span></span>

### <span data-ttu-id="4ab70-137">System.String</span><span class="sxs-lookup"><span data-stu-id="4ab70-137">System.String</span></span>

### <span data-ttu-id="4ab70-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="4ab70-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="4ab70-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4ab70-139">System.String[]</span></span>

## <span data-ttu-id="4ab70-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4ab70-140">OUTPUTS</span></span>

### <span data-ttu-id="4ab70-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="4ab70-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="4ab70-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="4ab70-142">NOTES</span></span>

## <span data-ttu-id="4ab70-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ab70-143">RELATED LINKS</span></span>
