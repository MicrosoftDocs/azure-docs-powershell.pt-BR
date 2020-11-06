---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: 9546039459792d5ef72807d8466f728f2060a346
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602466"
---
# <span data-ttu-id="f85bd-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f85bd-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="f85bd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f85bd-102">SYNOPSIS</span></span>
<span data-ttu-id="f85bd-103">Obtém informações sobre as regras de autorização associadas a um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f85bd-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f85bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f85bd-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f85bd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f85bd-105">DESCRIPTION</span></span>
<span data-ttu-id="f85bd-106">O cmdlet **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** retorna informações sobre as regras de autorização de assinatura de acesso compartilhado (SAS) associadas a um namespace de Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f85bd-106">The **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="f85bd-107">Você pode retornar informações sobre todas as regras associadas ao namespace.</span><span class="sxs-lookup"><span data-stu-id="f85bd-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="f85bd-108">Ou, como alternativa, incluindo o parâmetro *AuthorizationRule* , você pode retornar informações para uma regra específica.</span><span class="sxs-lookup"><span data-stu-id="f85bd-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>
<span data-ttu-id="f85bd-109">Regras de autorização gerenciem o acesso a namespaces.</span><span class="sxs-lookup"><span data-stu-id="f85bd-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="f85bd-110">Isso é feito por meio da criação de links, como URIs, com base em diferentes níveis de permissão.</span><span class="sxs-lookup"><span data-stu-id="f85bd-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="f85bd-111">Os níveis de plataforma podem ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="f85bd-111">Platform levels can be one of the following:</span></span> 
- <span data-ttu-id="f85bd-112">Ouvir</span><span class="sxs-lookup"><span data-stu-id="f85bd-112">Listen</span></span>
- <span data-ttu-id="f85bd-113">Enviar</span><span class="sxs-lookup"><span data-stu-id="f85bd-113">Send</span></span>
- <span data-ttu-id="f85bd-114">Gerenciar clientes são direcionados para um desses URIs com base no nível de permissão apropriado.</span><span class="sxs-lookup"><span data-stu-id="f85bd-114">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="f85bd-115">Por exemplo, um cliente que recebeu a permissão de escuta será direcionado para o URI dessa permissão.</span><span class="sxs-lookup"><span data-stu-id="f85bd-115">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="f85bd-116">Este cmdlet obtém apenas as regras de autorização associadas a um namespace.</span><span class="sxs-lookup"><span data-stu-id="f85bd-116">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="f85bd-117">Para obter informações sobre o próprio namespace, use Get-AzureRmNotificationHubsNamespace.</span><span class="sxs-lookup"><span data-stu-id="f85bd-117">To get information about the namespace itself, use Get-AzureRmNotificationHubsNamespace.</span></span>

## <span data-ttu-id="f85bd-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f85bd-118">EXAMPLES</span></span>

### <span data-ttu-id="f85bd-119">Exemplo 1: obter informações sobre todas as regras de autorização atribuídas a namespaces</span><span class="sxs-lookup"><span data-stu-id="f85bd-119">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="f85bd-120">Esse comando obtém informações sobre todas as regras de autorização atribuídas ao namespace ContosoNamespace e ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="f85bd-120">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="f85bd-121">Exemplo 2: obter informações sobre uma regra de autorização</span><span class="sxs-lookup"><span data-stu-id="f85bd-121">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="f85bd-122">Esse comando obtém informações sobre uma única regra de autorização de namespace chamada ListenRule.</span><span class="sxs-lookup"><span data-stu-id="f85bd-122">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="f85bd-123">Você deve incluir o namespace e o grupo de recursos quando obter informações para uma regra de autorização específica.</span><span class="sxs-lookup"><span data-stu-id="f85bd-123">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="f85bd-124">OS</span><span class="sxs-lookup"><span data-stu-id="f85bd-124">PARAMETERS</span></span>

### <span data-ttu-id="f85bd-125">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f85bd-125">-AuthorizationRule</span></span>
<span data-ttu-id="f85bd-126">Especifica o nome de uma regra de autenticação SAS.</span><span class="sxs-lookup"><span data-stu-id="f85bd-126">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="f85bd-127">Essas regras determinam o tipo de acesso que os usuários têm ao namespace.</span><span class="sxs-lookup"><span data-stu-id="f85bd-127">These rules determine the type of access that users have to the namespace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f85bd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f85bd-128">-DefaultProfile</span></span>
<span data-ttu-id="f85bd-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f85bd-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85bd-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f85bd-130">-Namespace</span></span>
<span data-ttu-id="f85bd-131">Especifica o namespace para o qual as regras de autorização são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="f85bd-131">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="f85bd-132">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="f85bd-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="f85bd-133">-Resource</span><span class="sxs-lookup"><span data-stu-id="f85bd-133">-ResourceGroup</span></span>
<span data-ttu-id="f85bd-134">Especifica o grupo de recursos ao qual as regras de autorização são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="f85bd-134">Specifies the resource group to which the authorization rules are assigned.</span></span>
<span data-ttu-id="f85bd-135">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="f85bd-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="f85bd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f85bd-136">CommonParameters</span></span>
<span data-ttu-id="f85bd-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f85bd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f85bd-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f85bd-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f85bd-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f85bd-139">INPUTS</span></span>

### <span data-ttu-id="f85bd-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f85bd-140">System.String</span></span>

## <span data-ttu-id="f85bd-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f85bd-141">OUTPUTS</span></span>

### <span data-ttu-id="f85bd-142">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f85bd-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f85bd-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f85bd-143">NOTES</span></span>

## <span data-ttu-id="f85bd-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f85bd-144">RELATED LINKS</span></span>

[<span data-ttu-id="f85bd-145">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f85bd-145">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="f85bd-146">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f85bd-146">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="f85bd-147">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f85bd-147">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="f85bd-148">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f85bd-148">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


