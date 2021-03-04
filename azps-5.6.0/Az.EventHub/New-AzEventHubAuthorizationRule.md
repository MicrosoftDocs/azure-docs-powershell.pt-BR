---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
ms.openlocfilehash: fde71fed26c074efa705d0b1dc181dfb46bae44e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886030"
---
# <span data-ttu-id="ce7aa-101">New-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ce7aa-101">New-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="ce7aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce7aa-102">SYNOPSIS</span></span>
<span data-ttu-id="ce7aa-103">Cria uma nova regra de autorização de Hubs de Eventos para namespace ou eventhub.</span><span class="sxs-lookup"><span data-stu-id="ce7aa-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

## <span data-ttu-id="ce7aa-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ce7aa-104">SYNTAX</span></span>

### <span data-ttu-id="ce7aa-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ce7aa-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce7aa-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ce7aa-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce7aa-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ce7aa-107">DESCRIPTION</span></span>
<span data-ttu-id="ce7aa-108">O New-AzEventHubAuthorizationRule cmdlet cria uma nova regra de autorização de Hubs de Eventos.</span><span class="sxs-lookup"><span data-stu-id="ce7aa-108">The New-AzEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="ce7aa-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce7aa-109">EXAMPLES</span></span>

### <span data-ttu-id="ce7aa-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ce7aa-110">Example 1</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="ce7aa-111">Cria uma regra de autorização MyAuthRuleName concedendo direitos de Escuta e Envio para o namespace MyNamespaceName , com o grupo de recursos \` \` \` \` \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ce7aa-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ce7aa-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ce7aa-112">Example 2</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="ce7aa-113">Cria uma regra de autorização MyAuthRuleName concedendo direitos de Escuta e Envio para o Hub de Eventos \` \` MyEventHubName no namespace MyNamespaceName , com o grupo de recursos \` \` \` \` \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ce7aa-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="ce7aa-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ce7aa-114">PARAMETERS</span></span>

### <span data-ttu-id="ce7aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce7aa-115">-DefaultProfile</span></span>
<span data-ttu-id="ce7aa-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ce7aa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce7aa-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="ce7aa-117">-EventHub</span></span>
<span data-ttu-id="ce7aa-118">Nome eventHub</span><span class="sxs-lookup"><span data-stu-id="ce7aa-118">EventHub Name</span></span>

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

### <span data-ttu-id="ce7aa-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ce7aa-119">-Name</span></span>
<span data-ttu-id="ce7aa-120">Nome authorizationRule</span><span class="sxs-lookup"><span data-stu-id="ce7aa-120">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="ce7aa-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ce7aa-121">-Namespace</span></span>
<span data-ttu-id="ce7aa-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="ce7aa-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce7aa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce7aa-123">-ResourceGroupName</span></span>
<span data-ttu-id="ce7aa-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="ce7aa-124">Resource Group Name</span></span>

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

### <span data-ttu-id="ce7aa-125">-Rights</span><span class="sxs-lookup"><span data-stu-id="ce7aa-125">-Rights</span></span>
<span data-ttu-id="ce7aa-126">Direitos, por exemplo, "Listen","Send","Manage"</span><span class="sxs-lookup"><span data-stu-id="ce7aa-126">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce7aa-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce7aa-127">-Confirm</span></span>
<span data-ttu-id="ce7aa-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce7aa-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce7aa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce7aa-129">-WhatIf</span></span>
<span data-ttu-id="ce7aa-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ce7aa-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce7aa-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ce7aa-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce7aa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce7aa-132">CommonParameters</span></span>
<span data-ttu-id="ce7aa-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce7aa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce7aa-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce7aa-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce7aa-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ce7aa-135">INPUTS</span></span>

### <span data-ttu-id="ce7aa-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ce7aa-136">System.String</span></span>

### <span data-ttu-id="ce7aa-137">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ce7aa-137">System.String[]</span></span>

## <span data-ttu-id="ce7aa-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ce7aa-138">OUTPUTS</span></span>

### <span data-ttu-id="ce7aa-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="ce7aa-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="ce7aa-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="ce7aa-140">NOTES</span></span>

## <span data-ttu-id="ce7aa-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce7aa-141">RELATED LINKS</span></span>
