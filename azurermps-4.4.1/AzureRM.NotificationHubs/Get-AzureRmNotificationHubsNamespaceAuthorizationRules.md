---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: aa9b4dba29c766923966571c736c7f96a608df29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429209"
---
# <span data-ttu-id="3d567-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="3d567-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="3d567-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d567-102">SYNOPSIS</span></span>
<span data-ttu-id="3d567-103">Obtém informações sobre as regras de autorização associadas a um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="3d567-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d567-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d567-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d567-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3d567-105">DESCRIPTION</span></span>
<span data-ttu-id="3d567-106">O cmdlet **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** retorna informações sobre as regras de autorização de assinatura de acesso compartilhado (SAS) associadas a um namespace de Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="3d567-106">The **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="3d567-107">Você pode retornar informações sobre todas as regras associadas ao namespace.</span><span class="sxs-lookup"><span data-stu-id="3d567-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="3d567-108">Ou, como alternativa, incluindo o parâmetro *AuthorizationRule* , você pode retornar informações para uma regra específica.</span><span class="sxs-lookup"><span data-stu-id="3d567-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>

<span data-ttu-id="3d567-109">Regras de autorização gerenciem o acesso a namespaces.</span><span class="sxs-lookup"><span data-stu-id="3d567-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="3d567-110">Isso é feito por meio da criação de links, como URIs, com base em diferentes níveis de permissão.</span><span class="sxs-lookup"><span data-stu-id="3d567-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="3d567-111">Os níveis de plataforma podem ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="3d567-111">Platform levels can be one of the following:</span></span> 

- <span data-ttu-id="3d567-112">Ouvir</span><span class="sxs-lookup"><span data-stu-id="3d567-112">Listen</span></span>
- <span data-ttu-id="3d567-113">Enviar</span><span class="sxs-lookup"><span data-stu-id="3d567-113">Send</span></span>
- <span data-ttu-id="3d567-114">Gerencia</span><span class="sxs-lookup"><span data-stu-id="3d567-114">Manage</span></span>

<span data-ttu-id="3d567-115">Os clientes são direcionados para um desses URIs com base no nível de permissão apropriado.</span><span class="sxs-lookup"><span data-stu-id="3d567-115">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="3d567-116">Por exemplo, um cliente que recebeu a permissão de escuta será direcionado para o URI dessa permissão.</span><span class="sxs-lookup"><span data-stu-id="3d567-116">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="3d567-117">Este cmdlet obtém apenas as regras de autorização associadas a um namespace.</span><span class="sxs-lookup"><span data-stu-id="3d567-117">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="3d567-118">Para obter informações sobre o próprio namespace, use Get-AzureRmNotificationHubsNamespace.</span><span class="sxs-lookup"><span data-stu-id="3d567-118">To get information about the namespace itself, use Get-AzureRmNotificationHubsNamespace.</span></span>

## <span data-ttu-id="3d567-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d567-119">EXAMPLES</span></span>

### <span data-ttu-id="3d567-120">Exemplo 1: obter informações sobre todas as regras de autorização atribuídas a namespaces</span><span class="sxs-lookup"><span data-stu-id="3d567-120">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="3d567-121">Esse comando obtém informações sobre todas as regras de autorização atribuídas ao namespace ContosoNamespace e ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="3d567-121">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="3d567-122">Exemplo 2: obter informações sobre uma regra de autorização</span><span class="sxs-lookup"><span data-stu-id="3d567-122">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="3d567-123">Esse comando obtém informações sobre uma única regra de autorização de namespace chamada ListenRule.</span><span class="sxs-lookup"><span data-stu-id="3d567-123">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="3d567-124">Você deve incluir o namespace e o grupo de recursos quando obter informações para uma regra de autorização específica.</span><span class="sxs-lookup"><span data-stu-id="3d567-124">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="3d567-125">OS</span><span class="sxs-lookup"><span data-stu-id="3d567-125">PARAMETERS</span></span>

### <span data-ttu-id="3d567-126">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3d567-126">-AuthorizationRule</span></span>
<span data-ttu-id="3d567-127">Especifica o nome de uma regra de autenticação SAS.</span><span class="sxs-lookup"><span data-stu-id="3d567-127">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="3d567-128">Essas regras determinam o tipo de acesso que os usuários têm ao namespace.</span><span class="sxs-lookup"><span data-stu-id="3d567-128">These rules determine the type of access that users have to the namespace.</span></span>

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

### <span data-ttu-id="3d567-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3d567-129">-Namespace</span></span>
<span data-ttu-id="3d567-130">Especifica o namespace para o qual as regras de autorização são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="3d567-130">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="3d567-131">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="3d567-131">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="3d567-132">-Resource</span><span class="sxs-lookup"><span data-stu-id="3d567-132">-ResourceGroup</span></span>
<span data-ttu-id="3d567-133">Especifica o grupo de recursos ao qual as regras de autorização são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="3d567-133">Specifies the resource group to which the authorization rules are assigned.</span></span>

<span data-ttu-id="3d567-134">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="3d567-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="3d567-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d567-135">-DefaultProfile</span></span>
<span data-ttu-id="3d567-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d567-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d567-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d567-137">CommonParameters</span></span>
<span data-ttu-id="3d567-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d567-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d567-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d567-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d567-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3d567-140">INPUTS</span></span>

## <span data-ttu-id="3d567-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3d567-141">OUTPUTS</span></span>

### <span data-ttu-id="3d567-142">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes]</span><span class="sxs-lookup"><span data-stu-id="3d567-142">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes]</span></span>

## <span data-ttu-id="3d567-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3d567-143">NOTES</span></span>

## <span data-ttu-id="3d567-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d567-144">RELATED LINKS</span></span>

[<span data-ttu-id="3d567-145">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="3d567-145">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="3d567-146">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="3d567-146">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="3d567-147">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="3d567-147">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="3d567-148">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="3d567-148">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


