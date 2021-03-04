---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 0b16a7feb2d0cba7355b6064c1a0e1e6fb327066
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885277"
---
# <span data-ttu-id="f4d0c-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f4d0c-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="f4d0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4d0c-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d0c-103">Remove uma regra de autorização de um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-103">Removes an authorization rule from a notification hub namespace.</span></span>

## <span data-ttu-id="f4d0c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f4d0c-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4d0c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f4d0c-105">DESCRIPTION</span></span>
<span data-ttu-id="f4d0c-106">O cmdlet **Remove-AzNotificationHubsNamespaceAuthorizationRule** remove uma regra de autorização SAS (Assinatura de Acesso Compartilhado) de um namespace de hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-106">The **Remove-AzNotificationHubsNamespaceAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>
<span data-ttu-id="f4d0c-107">As regras de autorização gerenciam o acesso a um namespace.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="f4d0c-108">Isso é feito por meio da criação de links, como URIs, com base em diferentes níveis de permissão.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="f4d0c-109">Os níveis de permissão podem ser os seguintes:</span><span class="sxs-lookup"><span data-stu-id="f4d0c-109">Permission levels can be of the following:</span></span> 
- <span data-ttu-id="f4d0c-110">Ouvir</span><span class="sxs-lookup"><span data-stu-id="f4d0c-110">Listen</span></span>
- <span data-ttu-id="f4d0c-111">Enviar</span><span class="sxs-lookup"><span data-stu-id="f4d0c-111">Send</span></span>
- <span data-ttu-id="f4d0c-112">Gerenciar Clientes são direcionados para uma dessas URIs com base no nível de permissão apropriado.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-112">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="f4d0c-113">Por exemplo, um cliente com a permissão Ouvir é direcionado para o URI para essa permissão.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-113">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>
<span data-ttu-id="f4d0c-114">Remover uma regra de autorização também remove a permissão de usuário correspondente.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="f4d0c-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f4d0c-115">EXAMPLES</span></span>

### <span data-ttu-id="f4d0c-116">Exemplo 1: Remover uma regra de autorização de um namespace</span><span class="sxs-lookup"><span data-stu-id="f4d0c-116">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzNotificationHubNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="f4d0c-117">Este comando remove a regra de autorização chamada ListenRule do namespace chamado ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-117">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="f4d0c-118">Ao executar esse comando, você deve especificar o grupo de recursos ao qual o namespace é atribuído.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-118">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="f4d0c-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f4d0c-119">PARAMETERS</span></span>

### <span data-ttu-id="f4d0c-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f4d0c-120">-AuthorizationRule</span></span>
<span data-ttu-id="f4d0c-121">Especifica o nome da regra de autenticação SAS a ser removida.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-121">Specifies the name of the SAS authentication rule to be removed.</span></span>

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

### <span data-ttu-id="f4d0c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d0c-122">-DefaultProfile</span></span>
<span data-ttu-id="f4d0c-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f4d0c-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4d0c-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f4d0c-124">-Force</span></span>
<span data-ttu-id="f4d0c-125">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f4d0c-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f4d0c-126">-Namespace</span></span>
<span data-ttu-id="f4d0c-127">Especifica o namespace ao qual as regras de autorização são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-127">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="f4d0c-128">Os namespaces fornecem uma maneira de agrupar e categorizar hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="f4d0c-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f4d0c-129">-ResourceGroup</span></span>
<span data-ttu-id="f4d0c-130">Especifica o grupo de recursos ao qual o namespace é atribuído.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-130">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="f4d0c-131">Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente o gerenciamento de inventário e a administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="f4d0c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4d0c-132">-Confirm</span></span>
<span data-ttu-id="f4d0c-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4d0c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4d0c-134">-WhatIf</span></span>
<span data-ttu-id="f4d0c-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4d0c-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4d0c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d0c-137">CommonParameters</span></span>
<span data-ttu-id="f4d0c-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d0c-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4d0c-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d0c-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4d0c-140">INPUTS</span></span>

### <span data-ttu-id="f4d0c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f4d0c-141">System.String</span></span>

## <span data-ttu-id="f4d0c-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f4d0c-142">OUTPUTS</span></span>

### <span data-ttu-id="f4d0c-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f4d0c-143">System.Boolean</span></span>

## <span data-ttu-id="f4d0c-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="f4d0c-144">NOTES</span></span>

## <span data-ttu-id="f4d0c-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4d0c-145">RELATED LINKS</span></span>

[<span data-ttu-id="f4d0c-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f4d0c-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="f4d0c-147">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f4d0c-147">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="f4d0c-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f4d0c-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Set-AzNotificationHubsNamespaceAuthorizationRule.md)


