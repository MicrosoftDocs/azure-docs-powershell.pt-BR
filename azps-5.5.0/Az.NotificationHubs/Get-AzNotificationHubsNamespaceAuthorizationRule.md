---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: f3ba8428a6f6a9e618872e1292234751979b3c4b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118240"
---
# <span data-ttu-id="d0bc7-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d0bc7-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="d0bc7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d0bc7-102">SYNOPSIS</span></span>
<span data-ttu-id="d0bc7-103">Obtém informações sobre as regras de autorização associadas a um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="d0bc7-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

## <span data-ttu-id="d0bc7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0bc7-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0bc7-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0bc7-105">DESCRIPTION</span></span>
<span data-ttu-id="d0bc7-106">O cmdlet **Get-AzNotificationHubsNamespaceAuthorizationRule** retorna informações sobre as regras de autorização de Assinatura de Acesso Compartilhado (SAS) associadas a um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="d0bc7-106">The **Get-AzNotificationHubsNamespaceAuthorizationRule** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="d0bc7-107">Você pode retornar informações sobre todas as regras associadas ao namespace.</span><span class="sxs-lookup"><span data-stu-id="d0bc7-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="d0bc7-108">Como alternativa, e ao incluir o parâmetro *AuthorizationRule,* você pode retornar informações para uma regra específica.</span><span class="sxs-lookup"><span data-stu-id="d0bc7-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>
<span data-ttu-id="d0bc7-109">As regras de autorização gerenciam o acesso a namespaces.</span><span class="sxs-lookup"><span data-stu-id="d0bc7-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="d0bc7-110">Isso é feito por meio da criação de links, como URIs, com base em diferentes níveis de permissão.</span><span class="sxs-lookup"><span data-stu-id="d0bc7-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="d0bc7-111">Os níveis de plataforma podem ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="d0bc7-111">Platform levels can be one of the following:</span></span> 
- <span data-ttu-id="d0bc7-112">Escute</span><span class="sxs-lookup"><span data-stu-id="d0bc7-112">Listen</span></span>
- <span data-ttu-id="d0bc7-113">Enviar</span><span class="sxs-lookup"><span data-stu-id="d0bc7-113">Send</span></span>
- <span data-ttu-id="d0bc7-114">Gerenciar Clientes são direcionados para uma dessas URIs com base no nível de permissão apropriado.</span><span class="sxs-lookup"><span data-stu-id="d0bc7-114">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="d0bc7-115">Por exemplo, um cliente com a permissão Ouvir será direcionado para o URI para essa permissão.</span><span class="sxs-lookup"><span data-stu-id="d0bc7-115">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="d0bc7-116">Este cmdlet só obtém as regras de autorização associadas a um namespace.</span><span class="sxs-lookup"><span data-stu-id="d0bc7-116">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="d0bc7-117">Para obter informações sobre o namespace em si, use Get-AzNotificationHubsNamespace.</span><span class="sxs-lookup"><span data-stu-id="d0bc7-117">To get information about the namespace itself, use Get-AzNotificationHubsNamespace.</span></span>

## <span data-ttu-id="d0bc7-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d0bc7-118">EXAMPLES</span></span>

### <span data-ttu-id="d0bc7-119">Exemplo 1: Obter informações sobre todas as regras de autorização atribuídas a namespaces</span><span class="sxs-lookup"><span data-stu-id="d0bc7-119">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="d0bc7-120">Esse comando obtém informações sobre todas as regras de autorização atribuídas ao namespace ContosoNamespace e ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="d0bc7-120">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="d0bc7-121">Exemplo 2: obter informações sobre uma regra de autorização</span><span class="sxs-lookup"><span data-stu-id="d0bc7-121">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="d0bc7-122">Este comando obtém informações sobre uma única regra de autorização de namespace chamada ListenRule.</span><span class="sxs-lookup"><span data-stu-id="d0bc7-122">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="d0bc7-123">Você deve incluir o namespace e o grupo de recursos quando obter informações para uma regra de autorização específica.</span><span class="sxs-lookup"><span data-stu-id="d0bc7-123">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="d0bc7-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0bc7-124">PARAMETERS</span></span>

### <span data-ttu-id="d0bc7-125">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d0bc7-125">-AuthorizationRule</span></span>
<span data-ttu-id="d0bc7-126">Especifica o nome de uma regra de autenticação SAS.</span><span class="sxs-lookup"><span data-stu-id="d0bc7-126">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="d0bc7-127">Essas regras determinam o tipo de acesso que os usuários têm ao namespace.</span><span class="sxs-lookup"><span data-stu-id="d0bc7-127">These rules determine the type of access that users have to the namespace.</span></span>

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

### <span data-ttu-id="d0bc7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0bc7-128">-DefaultProfile</span></span>
<span data-ttu-id="d0bc7-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="d0bc7-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0bc7-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d0bc7-130">-Namespace</span></span>
<span data-ttu-id="d0bc7-131">Especifica o namespace ao qual as regras de autorização são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="d0bc7-131">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="d0bc7-132">Os namespaces oferecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="d0bc7-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="d0bc7-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d0bc7-133">-ResourceGroup</span></span>
<span data-ttu-id="d0bc7-134">Especifica o grupo de recursos ao qual as regras de autorização são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="d0bc7-134">Specifies the resource group to which the authorization rules are assigned.</span></span>
<span data-ttu-id="d0bc7-135">Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente o gerenciamento de estoque e a administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="d0bc7-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="d0bc7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0bc7-136">CommonParameters</span></span>
<span data-ttu-id="d0bc7-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0bc7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0bc7-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0bc7-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0bc7-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="d0bc7-139">INPUTS</span></span>

### <span data-ttu-id="d0bc7-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d0bc7-140">System.String</span></span>

## <span data-ttu-id="d0bc7-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="d0bc7-141">OUTPUTS</span></span>

### <span data-ttu-id="d0bc7-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="d0bc7-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="d0bc7-143">Notas</span><span class="sxs-lookup"><span data-stu-id="d0bc7-143">NOTES</span></span>

## <span data-ttu-id="d0bc7-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0bc7-144">RELATED LINKS</span></span>

[<span data-ttu-id="d0bc7-145">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d0bc7-145">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="d0bc7-146">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d0bc7-146">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="d0bc7-147">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d0bc7-147">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="d0bc7-148">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d0bc7-148">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


