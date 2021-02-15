---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 7a7c70dc9cf106aebc44df4733c4f8f9abaa78a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111888"
---
# <span data-ttu-id="cdd0a-101">New-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cdd0a-101">New-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="cdd0a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cdd0a-102">SYNOPSIS</span></span>
<span data-ttu-id="cdd0a-103">Cria uma nova regra de autorização de Hubs de Eventos para namespace ou eventhub.</span><span class="sxs-lookup"><span data-stu-id="cdd0a-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

## <span data-ttu-id="cdd0a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cdd0a-104">SYNTAX</span></span>

### <span data-ttu-id="cdd0a-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cdd0a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdd0a-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="cdd0a-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cdd0a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="cdd0a-107">DESCRIPTION</span></span>
<span data-ttu-id="cdd0a-108">O New-AzEventHubAuthorizationRule cmdlet cria uma nova regra de autorização do Hub de Eventos.</span><span class="sxs-lookup"><span data-stu-id="cdd0a-108">The New-AzEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="cdd0a-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cdd0a-109">EXAMPLES</span></span>

### <span data-ttu-id="cdd0a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cdd0a-110">Example 1</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="cdd0a-111">Cria uma regra de autorização MyAuthRuleName concedendo direitos de Ouvir e Enviar para o namespace MyNamespaceName, com o grupo de recursos \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="cdd0a-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="cdd0a-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cdd0a-112">Example 2</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="cdd0a-113">Cria uma regra de autorização MyAuthRuleName concedendo direitos de Ouvir e Enviar para o Hub de Eventos \` \` MyEventHubName no namespace MyNamespaceName, com o grupo de recursos \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="cdd0a-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="cdd0a-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cdd0a-114">PARAMETERS</span></span>

### <span data-ttu-id="cdd0a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdd0a-115">-DefaultProfile</span></span>
<span data-ttu-id="cdd0a-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cdd0a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdd0a-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="cdd0a-117">-EventHub</span></span>
<span data-ttu-id="cdd0a-118">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="cdd0a-118">EventHub Name</span></span>

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

### <span data-ttu-id="cdd0a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="cdd0a-119">-Name</span></span>
<span data-ttu-id="cdd0a-120">Nome de AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cdd0a-120">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="cdd0a-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cdd0a-121">-Namespace</span></span>
<span data-ttu-id="cdd0a-122">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="cdd0a-122">Namespace Name</span></span>

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

### <span data-ttu-id="cdd0a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdd0a-123">-ResourceGroupName</span></span>
<span data-ttu-id="cdd0a-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="cdd0a-124">Resource Group Name</span></span>

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

### <span data-ttu-id="cdd0a-125">-Direitos</span><span class="sxs-lookup"><span data-stu-id="cdd0a-125">-Rights</span></span>
<span data-ttu-id="cdd0a-126">Direitos, por exemplo, "Ouvir","Enviar","Gerenciar"</span><span class="sxs-lookup"><span data-stu-id="cdd0a-126">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="cdd0a-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="cdd0a-127">-Confirm</span></span>
<span data-ttu-id="cdd0a-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdd0a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdd0a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdd0a-129">-WhatIf</span></span>
<span data-ttu-id="cdd0a-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="cdd0a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdd0a-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cdd0a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdd0a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdd0a-132">CommonParameters</span></span>
<span data-ttu-id="cdd0a-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdd0a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdd0a-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdd0a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdd0a-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="cdd0a-135">INPUTS</span></span>

### <span data-ttu-id="cdd0a-136">System.String</span><span class="sxs-lookup"><span data-stu-id="cdd0a-136">System.String</span></span>

### <span data-ttu-id="cdd0a-137">System.String[]</span><span class="sxs-lookup"><span data-stu-id="cdd0a-137">System.String[]</span></span>

## <span data-ttu-id="cdd0a-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="cdd0a-138">OUTPUTS</span></span>

### <span data-ttu-id="cdd0a-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="cdd0a-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="cdd0a-140">Notas</span><span class="sxs-lookup"><span data-stu-id="cdd0a-140">NOTES</span></span>

## <span data-ttu-id="cdd0a-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cdd0a-141">RELATED LINKS</span></span>
