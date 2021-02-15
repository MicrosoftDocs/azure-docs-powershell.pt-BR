---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: a25535e3aef21894091197d816c61f2aa5131df9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114593"
---
# <span data-ttu-id="0312d-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0312d-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="0312d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0312d-102">SYNOPSIS</span></span>
<span data-ttu-id="0312d-103">Remove uma regra de autorização de um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="0312d-103">Removes an authorization rule from a notification hub namespace.</span></span>

## <span data-ttu-id="0312d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0312d-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0312d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0312d-105">DESCRIPTION</span></span>
<span data-ttu-id="0312d-106">O cmdlet **Remove-AzNotificationHubsNamespaceAuthorizationRule** remove uma regra de autorização de Assinatura de Acesso Compartilhado (SAS) de um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="0312d-106">The **Remove-AzNotificationHubsNamespaceAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>
<span data-ttu-id="0312d-107">As regras de autorização gerenciam o acesso a um namespace.</span><span class="sxs-lookup"><span data-stu-id="0312d-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="0312d-108">Isso é feito por meio da criação de links, como URIs, com base em diferentes níveis de permissão.</span><span class="sxs-lookup"><span data-stu-id="0312d-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="0312d-109">Os níveis de permissão podem ser dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="0312d-109">Permission levels can be of the following:</span></span> 
- <span data-ttu-id="0312d-110">Escute</span><span class="sxs-lookup"><span data-stu-id="0312d-110">Listen</span></span>
- <span data-ttu-id="0312d-111">Enviar</span><span class="sxs-lookup"><span data-stu-id="0312d-111">Send</span></span>
- <span data-ttu-id="0312d-112">Gerenciar Clientes são direcionados para uma dessas URIs com base no nível de permissão apropriado.</span><span class="sxs-lookup"><span data-stu-id="0312d-112">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="0312d-113">Por exemplo, um cliente com a permissão Ouvir é direcionado para o URI para essa permissão.</span><span class="sxs-lookup"><span data-stu-id="0312d-113">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>
<span data-ttu-id="0312d-114">Remover uma regra de autorização também remove a permissão do usuário correspondente.</span><span class="sxs-lookup"><span data-stu-id="0312d-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="0312d-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0312d-115">EXAMPLES</span></span>

### <span data-ttu-id="0312d-116">Exemplo 1: Remover uma regra de autorização de um namespace</span><span class="sxs-lookup"><span data-stu-id="0312d-116">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzNotificationHubNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="0312d-117">Este comando remove a regra de autorização chamada ListenRule do namespace chamado ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="0312d-117">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="0312d-118">Ao executar esse comando, você deve especificar o grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="0312d-118">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="0312d-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0312d-119">PARAMETERS</span></span>

### <span data-ttu-id="0312d-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0312d-120">-AuthorizationRule</span></span>
<span data-ttu-id="0312d-121">Especifica o nome da regra de autenticação SAS a ser removida.</span><span class="sxs-lookup"><span data-stu-id="0312d-121">Specifies the name of the SAS authentication rule to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0312d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0312d-122">-DefaultProfile</span></span>
<span data-ttu-id="0312d-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="0312d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0312d-124">-Forçar</span><span class="sxs-lookup"><span data-stu-id="0312d-124">-Force</span></span>
<span data-ttu-id="0312d-125">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="0312d-125">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0312d-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0312d-126">-Namespace</span></span>
<span data-ttu-id="0312d-127">Especifica o namespace ao qual as regras de autorização são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="0312d-127">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="0312d-128">Os namespaces oferecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="0312d-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0312d-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0312d-129">-ResourceGroup</span></span>
<span data-ttu-id="0312d-130">Especifica o grupo de recursos ao qual o namespace é atribuído.</span><span class="sxs-lookup"><span data-stu-id="0312d-130">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="0312d-131">Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente o gerenciamento de estoque e a administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="0312d-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="0312d-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0312d-132">-Confirm</span></span>
<span data-ttu-id="0312d-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0312d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0312d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0312d-134">-WhatIf</span></span>
<span data-ttu-id="0312d-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0312d-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0312d-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0312d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0312d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0312d-137">CommonParameters</span></span>
<span data-ttu-id="0312d-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0312d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0312d-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0312d-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0312d-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="0312d-140">INPUTS</span></span>

### <span data-ttu-id="0312d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0312d-141">System.String</span></span>

## <span data-ttu-id="0312d-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="0312d-142">OUTPUTS</span></span>

### <span data-ttu-id="0312d-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0312d-143">System.Boolean</span></span>

## <span data-ttu-id="0312d-144">Notas</span><span class="sxs-lookup"><span data-stu-id="0312d-144">NOTES</span></span>

## <span data-ttu-id="0312d-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0312d-145">RELATED LINKS</span></span>

[<span data-ttu-id="0312d-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0312d-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="0312d-147">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0312d-147">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="0312d-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0312d-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Set-AzNotificationHubsNamespaceAuthorizationRule.md)


