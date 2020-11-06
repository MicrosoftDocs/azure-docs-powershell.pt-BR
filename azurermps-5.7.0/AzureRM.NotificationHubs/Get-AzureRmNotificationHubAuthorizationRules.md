---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: b6ece0370642d5ef0b913c96d3b817834b204e52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440835"
---
# <span data-ttu-id="41d60-101">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="41d60-101">Get-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="41d60-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41d60-102">SYNOPSIS</span></span>
<span data-ttu-id="41d60-103">Obtém informações sobre as regras de autorização associadas a um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="41d60-103">Gets information about the authorization rules associated with a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41d60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41d60-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41d60-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41d60-105">DESCRIPTION</span></span>
<span data-ttu-id="41d60-106">O cmdlet **Get-AzureRmNotificationHubAuthorizationRules** Obtém informações sobre as regras de autorização de assinatura de acesso compartilhado (SAS) associadas a um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="41d60-106">The **Get-AzureRmNotificationHubAuthorizationRules** cmdlet gets information about the Shared Access Signature (SAS) authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="41d60-107">O cmdlet retorna informações sobre todas as regras associadas a um Hub ou, incluindo o parâmetro *AuthorizationRule* , obtém informações sobre uma regra específica.</span><span class="sxs-lookup"><span data-stu-id="41d60-107">The cmdlet returns information about all the rules associated with a hub or, by including the *AuthorizationRule* parameter, gets information about a specific rule.</span></span>

<span data-ttu-id="41d60-108">Regras de autorização gerenciem o acesso aos seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="41d60-108">Authorization rules manage access to your notification hubs.</span></span>
<span data-ttu-id="41d60-109">Uma regra de autorização criará links, como um URI, com base em diferentes níveis de permissão.</span><span class="sxs-lookup"><span data-stu-id="41d60-109">An authorization rule will create links, as a URI, based on different permission levels.</span></span>
<span data-ttu-id="41d60-110">Os clientes são direcionados para um desses URIs com base no nível de permissão apropriado.</span><span class="sxs-lookup"><span data-stu-id="41d60-110">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="41d60-111">Por exemplo, um cliente com a permissão Listen será direcionado para o URI dessa permissão.</span><span class="sxs-lookup"><span data-stu-id="41d60-111">For instance, a client with the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="41d60-112">O cmdlet **Get-AzureRmNotificationHubAuthorizationRules** só obtém informações sobre as regras de autorização associadas a um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="41d60-112">The **Get-AzureRmNotificationHubAuthorizationRules** cmdlet only gets information about the authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="41d60-113">Para obter informações sobre o próprio Hub, use Get-AzureRmNotificationHub.</span><span class="sxs-lookup"><span data-stu-id="41d60-113">To get information about the hub itself, use Get-AzureRmNotificationHub.</span></span>

## <span data-ttu-id="41d60-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41d60-114">EXAMPLES</span></span>

### <span data-ttu-id="41d60-115">Exemplo 1: obter informações de todas as regras de autorização atribuídas a um hub de notificação</span><span class="sxs-lookup"><span data-stu-id="41d60-115">Example 1: Get information for all authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="41d60-116">Esse comando obtém informações para todas as regras de autorização atribuídas ao Hub de notificação chamado ContosoInternalHub no namespace ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="41d60-116">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="41d60-117">Você deve especificar o namespace no qual o Hub está localizado, bem como o grupo de recursos ao qual o Hub foi atribuído.</span><span class="sxs-lookup"><span data-stu-id="41d60-117">You must specify the namespace where the hub is located as well as the resource group that the hub has been assigned to.</span></span>

### <span data-ttu-id="41d60-118">Exemplo 2: obter informações para uma regra de autorização atribuída a um hub de notificação</span><span class="sxs-lookup"><span data-stu-id="41d60-118">Example 2: Get information for an authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="41d60-119">Esse comando obtém informações para todas as regras de autorização atribuídas ao Hub de notificação chamado ContosoInternalHub no namespace ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="41d60-119">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="41d60-120">O comando usa o parâmetro *AuthorizationRule* para limitar os dados retornados a uma única regra de autorização chamada ListenRule.</span><span class="sxs-lookup"><span data-stu-id="41d60-120">The command uses the *AuthorizationRule* parameter to limit the returned data to a single authorization rule named ListenRule.</span></span>

## <span data-ttu-id="41d60-121">OS</span><span class="sxs-lookup"><span data-stu-id="41d60-121">PARAMETERS</span></span>

### <span data-ttu-id="41d60-122">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="41d60-122">-AuthorizationRule</span></span>
<span data-ttu-id="41d60-123">Especifica o nome de uma regra de autenticação SAS.</span><span class="sxs-lookup"><span data-stu-id="41d60-123">Specifies the name of an SAS authentication rule.</span></span>
<span data-ttu-id="41d60-124">Essas regras determinam o tipo de acesso que os usuários têm ao Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="41d60-124">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41d60-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41d60-125">-DefaultProfile</span></span>
<span data-ttu-id="41d60-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="41d60-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41d60-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="41d60-127">-Namespace</span></span>
<span data-ttu-id="41d60-128">Especifica o namespace ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="41d60-128">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="41d60-129">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="41d60-129">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="41d60-130">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="41d60-130">-NotificationHub</span></span>
<span data-ttu-id="41d60-131">Especifica o Hub de notificação que esse cmdlet atribui regras de autorização.</span><span class="sxs-lookup"><span data-stu-id="41d60-131">Specifies the notification hub that this cmdlet assigns authorization rules.</span></span>
<span data-ttu-id="41d60-132">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="41d60-132">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="41d60-133">-Resource</span><span class="sxs-lookup"><span data-stu-id="41d60-133">-ResourceGroup</span></span>
<span data-ttu-id="41d60-134">Especifica o grupo de recursos ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="41d60-134">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="41d60-135">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplificar o gerenciamento de inventário e a administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="41d60-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simplify inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="41d60-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41d60-136">CommonParameters</span></span>
<span data-ttu-id="41d60-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41d60-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41d60-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41d60-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41d60-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41d60-139">INPUTS</span></span>

### <span data-ttu-id="41d60-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="41d60-140">None</span></span>
<span data-ttu-id="41d60-141">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="41d60-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="41d60-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41d60-142">OUTPUTS</span></span>

### <span data-ttu-id="41d60-143">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes]</span><span class="sxs-lookup"><span data-stu-id="41d60-143">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes]</span></span>

## <span data-ttu-id="41d60-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41d60-144">NOTES</span></span>

## <span data-ttu-id="41d60-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41d60-145">RELATED LINKS</span></span>

[<span data-ttu-id="41d60-146">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="41d60-146">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="41d60-147">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="41d60-147">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="41d60-148">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="41d60-148">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="41d60-149">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="41d60-149">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


