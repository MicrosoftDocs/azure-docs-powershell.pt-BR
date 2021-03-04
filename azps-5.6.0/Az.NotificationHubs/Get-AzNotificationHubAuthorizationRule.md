---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 260cf95d04d6a923acbdeaa91a412aa0046d9ea0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885312"
---
# <span data-ttu-id="e2e00-101">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e2e00-101">Get-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="e2e00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2e00-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e00-103">Obtém informações sobre as regras de autorização associadas a um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="e2e00-103">Gets information about the authorization rules associated with a notification hub.</span></span>

## <span data-ttu-id="e2e00-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e2e00-104">SYNTAX</span></span>

```
Get-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2e00-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e2e00-105">DESCRIPTION</span></span>
<span data-ttu-id="e2e00-106">O cmdlet **Get-AzNotificationHubAuthorizationRule** obtém informações sobre as regras de autorização da Assinatura de Acesso Compartilhado (SAS) associadas a um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="e2e00-106">The **Get-AzNotificationHubAuthorizationRule** cmdlet gets information about the Shared Access Signature (SAS) authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="e2e00-107">O cmdlet retorna informações sobre todas as regras associadas a um hub ou, incluindo o parâmetro *AuthorizationRule,* obtém informações sobre uma regra específica.</span><span class="sxs-lookup"><span data-stu-id="e2e00-107">The cmdlet returns information about all the rules associated with a hub or, by including the *AuthorizationRule* parameter, gets information about a specific rule.</span></span>
<span data-ttu-id="e2e00-108">As regras de autorização gerenciam o acesso aos hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="e2e00-108">Authorization rules manage access to your notification hubs.</span></span>
<span data-ttu-id="e2e00-109">Uma regra de autorização criará links, como URI, com base em diferentes níveis de permissão.</span><span class="sxs-lookup"><span data-stu-id="e2e00-109">An authorization rule will create links, as a URI, based on different permission levels.</span></span>
<span data-ttu-id="e2e00-110">Os clientes são direcionados para uma dessas URIs com base no nível de permissão apropriado.</span><span class="sxs-lookup"><span data-stu-id="e2e00-110">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="e2e00-111">Por exemplo, um cliente com a permissão Ouvir será direcionado para o URI para essa permissão.</span><span class="sxs-lookup"><span data-stu-id="e2e00-111">For instance, a client with the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="e2e00-112">O cmdlet **Get-AzNotificationHubAuthorizationRule** só obtém informações sobre as regras de autorização associadas a um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="e2e00-112">The **Get-AzNotificationHubAuthorizationRule** cmdlet only gets information about the authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="e2e00-113">Para obter informações sobre o hub em si, use Get-AzNotificationHub.</span><span class="sxs-lookup"><span data-stu-id="e2e00-113">To get information about the hub itself, use Get-AzNotificationHub.</span></span>

## <span data-ttu-id="e2e00-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2e00-114">EXAMPLES</span></span>

### <span data-ttu-id="e2e00-115">Exemplo 1: obter informações para todas as regras de autorização atribuídas a um hub de notificação</span><span class="sxs-lookup"><span data-stu-id="e2e00-115">Example 1: Get information for all authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="e2e00-116">Este comando obtém informações de todas as regras de autorização atribuídas ao hub de notificação chamado ContosoInternalHub no namespace ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="e2e00-116">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="e2e00-117">Você deve especificar o namespace no qual o hub está localizado, bem como o grupo de recursos ao qual o hub foi atribuído.</span><span class="sxs-lookup"><span data-stu-id="e2e00-117">You must specify the namespace where the hub is located as well as the resource group that the hub has been assigned to.</span></span>

### <span data-ttu-id="e2e00-118">Exemplo 2: obter informações sobre regras de autorização atribuídas a um hub de notificação</span><span class="sxs-lookup"><span data-stu-id="e2e00-118">Example 2: Get information for an authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="e2e00-119">Este comando obtém informações de todas as regras de autorização atribuídas ao hub de notificação chamado ContosoInternalHub no namespace ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="e2e00-119">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="e2e00-120">O comando usa o *parâmetro AuthorizationRule* para limitar os dados retornados a uma única regra de autorização chamada ListenRule.</span><span class="sxs-lookup"><span data-stu-id="e2e00-120">The command uses the *AuthorizationRule* parameter to limit the returned data to a single authorization rule named ListenRule.</span></span>

## <span data-ttu-id="e2e00-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e2e00-121">PARAMETERS</span></span>

### <span data-ttu-id="e2e00-122">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e2e00-122">-AuthorizationRule</span></span>
<span data-ttu-id="e2e00-123">Especifica o nome de uma regra de autenticação SAS.</span><span class="sxs-lookup"><span data-stu-id="e2e00-123">Specifies the name of an SAS authentication rule.</span></span>
<span data-ttu-id="e2e00-124">Essas regras determinam o tipo de acesso que os usuários têm ao hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="e2e00-124">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e00-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2e00-125">-DefaultProfile</span></span>
<span data-ttu-id="e2e00-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e2e00-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2e00-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e2e00-127">-Namespace</span></span>
<span data-ttu-id="e2e00-128">Especifica o namespace ao qual o hub de notificação é atribuído.</span><span class="sxs-lookup"><span data-stu-id="e2e00-128">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="e2e00-129">Os namespaces fornecem uma maneira de agrupar e categorizar hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="e2e00-129">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="e2e00-130">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="e2e00-130">-NotificationHub</span></span>
<span data-ttu-id="e2e00-131">Especifica o hub de notificação que este cmdlet atribui regras de autorização.</span><span class="sxs-lookup"><span data-stu-id="e2e00-131">Specifies the notification hub that this cmdlet assigns authorization rules.</span></span>
<span data-ttu-id="e2e00-132">Os hubs de notificação são usados para enviar notificações por push a vários clientes, independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="e2e00-132">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="e2e00-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e2e00-133">-ResourceGroup</span></span>
<span data-ttu-id="e2e00-134">Especifica o grupo de recursos ao qual o hub de notificação é atribuído.</span><span class="sxs-lookup"><span data-stu-id="e2e00-134">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="e2e00-135">Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplificar o gerenciamento de inventário e a administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="e2e00-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simplify inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="e2e00-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e00-136">CommonParameters</span></span>
<span data-ttu-id="e2e00-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2e00-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e00-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2e00-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e00-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2e00-139">INPUTS</span></span>

### <span data-ttu-id="e2e00-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e2e00-140">System.String</span></span>

## <span data-ttu-id="e2e00-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e2e00-141">OUTPUTS</span></span>

### <span data-ttu-id="e2e00-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e2e00-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="e2e00-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="e2e00-143">NOTES</span></span>

## <span data-ttu-id="e2e00-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2e00-144">RELATED LINKS</span></span>

[<span data-ttu-id="e2e00-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e2e00-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="e2e00-146">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e2e00-146">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="e2e00-147">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e2e00-147">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="e2e00-148">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e2e00-148">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


