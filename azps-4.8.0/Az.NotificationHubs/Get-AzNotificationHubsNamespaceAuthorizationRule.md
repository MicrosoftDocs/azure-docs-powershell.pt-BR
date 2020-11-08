---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: f3ba8428a6f6a9e618872e1292234751979b3c4b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114757"
---
# <span data-ttu-id="b94c1-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b94c1-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="b94c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b94c1-102">SYNOPSIS</span></span>
<span data-ttu-id="b94c1-103">Obtém informações sobre as regras de autorização associadas a um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="b94c1-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

## <span data-ttu-id="b94c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b94c1-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b94c1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b94c1-105">DESCRIPTION</span></span>
<span data-ttu-id="b94c1-106">O cmdlet **Get-AzNotificationHubsNamespaceAuthorizationRule** retorna informações sobre as regras de autorização de assinatura de acesso compartilhado (SAS) associadas a um namespace de Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="b94c1-106">The **Get-AzNotificationHubsNamespaceAuthorizationRule** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="b94c1-107">Você pode retornar informações sobre todas as regras associadas ao namespace.</span><span class="sxs-lookup"><span data-stu-id="b94c1-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="b94c1-108">Ou, como alternativa, incluindo o parâmetro *AuthorizationRule* , você pode retornar informações para uma regra específica.</span><span class="sxs-lookup"><span data-stu-id="b94c1-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>
<span data-ttu-id="b94c1-109">Regras de autorização gerenciem o acesso a namespaces.</span><span class="sxs-lookup"><span data-stu-id="b94c1-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="b94c1-110">Isso é feito por meio da criação de links, como URIs, com base em diferentes níveis de permissão.</span><span class="sxs-lookup"><span data-stu-id="b94c1-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="b94c1-111">Os níveis de plataforma podem ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="b94c1-111">Platform levels can be one of the following:</span></span> 
- <span data-ttu-id="b94c1-112">Ouvir</span><span class="sxs-lookup"><span data-stu-id="b94c1-112">Listen</span></span>
- <span data-ttu-id="b94c1-113">Enviar</span><span class="sxs-lookup"><span data-stu-id="b94c1-113">Send</span></span>
- <span data-ttu-id="b94c1-114">Gerenciar clientes são direcionados para um desses URIs com base no nível de permissão apropriado.</span><span class="sxs-lookup"><span data-stu-id="b94c1-114">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="b94c1-115">Por exemplo, um cliente que recebeu a permissão de escuta será direcionado para o URI dessa permissão.</span><span class="sxs-lookup"><span data-stu-id="b94c1-115">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="b94c1-116">Este cmdlet obtém apenas as regras de autorização associadas a um namespace.</span><span class="sxs-lookup"><span data-stu-id="b94c1-116">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="b94c1-117">Para obter informações sobre o próprio namespace, use Get-AzNotificationHubsNamespace.</span><span class="sxs-lookup"><span data-stu-id="b94c1-117">To get information about the namespace itself, use Get-AzNotificationHubsNamespace.</span></span>

## <span data-ttu-id="b94c1-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b94c1-118">EXAMPLES</span></span>

### <span data-ttu-id="b94c1-119">Exemplo 1: obter informações sobre todas as regras de autorização atribuídas a namespaces</span><span class="sxs-lookup"><span data-stu-id="b94c1-119">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="b94c1-120">Esse comando obtém informações sobre todas as regras de autorização atribuídas ao namespace ContosoNamespace e ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="b94c1-120">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="b94c1-121">Exemplo 2: obter informações sobre uma regra de autorização</span><span class="sxs-lookup"><span data-stu-id="b94c1-121">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="b94c1-122">Esse comando obtém informações sobre uma única regra de autorização de namespace chamada ListenRule.</span><span class="sxs-lookup"><span data-stu-id="b94c1-122">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="b94c1-123">Você deve incluir o namespace e o grupo de recursos quando obter informações para uma regra de autorização específica.</span><span class="sxs-lookup"><span data-stu-id="b94c1-123">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="b94c1-124">OS</span><span class="sxs-lookup"><span data-stu-id="b94c1-124">PARAMETERS</span></span>

### <span data-ttu-id="b94c1-125">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b94c1-125">-AuthorizationRule</span></span>
<span data-ttu-id="b94c1-126">Especifica o nome de uma regra de autenticação SAS.</span><span class="sxs-lookup"><span data-stu-id="b94c1-126">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="b94c1-127">Essas regras determinam o tipo de acesso que os usuários têm ao namespace.</span><span class="sxs-lookup"><span data-stu-id="b94c1-127">These rules determine the type of access that users have to the namespace.</span></span>

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

### <span data-ttu-id="b94c1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b94c1-128">-DefaultProfile</span></span>
<span data-ttu-id="b94c1-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b94c1-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b94c1-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b94c1-130">-Namespace</span></span>
<span data-ttu-id="b94c1-131">Especifica o namespace para o qual as regras de autorização são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="b94c1-131">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="b94c1-132">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="b94c1-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="b94c1-133">-Resource</span><span class="sxs-lookup"><span data-stu-id="b94c1-133">-ResourceGroup</span></span>
<span data-ttu-id="b94c1-134">Especifica o grupo de recursos ao qual as regras de autorização são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="b94c1-134">Specifies the resource group to which the authorization rules are assigned.</span></span>
<span data-ttu-id="b94c1-135">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="b94c1-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="b94c1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b94c1-136">CommonParameters</span></span>
<span data-ttu-id="b94c1-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b94c1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b94c1-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b94c1-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b94c1-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b94c1-139">INPUTS</span></span>

### <span data-ttu-id="b94c1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b94c1-140">System.String</span></span>

## <span data-ttu-id="b94c1-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b94c1-141">OUTPUTS</span></span>

### <span data-ttu-id="b94c1-142">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="b94c1-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="b94c1-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b94c1-143">NOTES</span></span>

## <span data-ttu-id="b94c1-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b94c1-144">RELATED LINKS</span></span>

[<span data-ttu-id="b94c1-145">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b94c1-145">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="b94c1-146">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b94c1-146">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="b94c1-147">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b94c1-147">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="b94c1-148">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b94c1-148">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


