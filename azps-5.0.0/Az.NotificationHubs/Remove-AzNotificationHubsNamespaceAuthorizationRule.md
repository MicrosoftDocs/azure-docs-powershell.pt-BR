---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: a25535e3aef21894091197d816c61f2aa5131df9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281994"
---
# <span data-ttu-id="006f5-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="006f5-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="006f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="006f5-102">SYNOPSIS</span></span>
<span data-ttu-id="006f5-103">Remove uma regra de autorização de um namespace Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="006f5-103">Removes an authorization rule from a notification hub namespace.</span></span>

## <span data-ttu-id="006f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="006f5-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="006f5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="006f5-105">DESCRIPTION</span></span>
<span data-ttu-id="006f5-106">O cmdlet **Remove-AzNotificationHubsNamespaceAuthorizationRule** remove uma regra de autorização de assinatura de acesso compartilhado (SAS) de um namespace de Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="006f5-106">The **Remove-AzNotificationHubsNamespaceAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>
<span data-ttu-id="006f5-107">Regras de autorização gerenciem o acesso a um namespace.</span><span class="sxs-lookup"><span data-stu-id="006f5-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="006f5-108">Isso é feito por meio da criação de links, como URIs, com base em diferentes níveis de permissão.</span><span class="sxs-lookup"><span data-stu-id="006f5-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="006f5-109">Os níveis de permissão podem ser dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="006f5-109">Permission levels can be of the following:</span></span> 
- <span data-ttu-id="006f5-110">Ouvir</span><span class="sxs-lookup"><span data-stu-id="006f5-110">Listen</span></span>
- <span data-ttu-id="006f5-111">Enviar</span><span class="sxs-lookup"><span data-stu-id="006f5-111">Send</span></span>
- <span data-ttu-id="006f5-112">Gerenciar clientes são direcionados para um desses URIs com base no nível de permissão apropriado.</span><span class="sxs-lookup"><span data-stu-id="006f5-112">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="006f5-113">Por exemplo, um cliente que recebeu a permissão de escuta é direcionado para o URI dessa permissão.</span><span class="sxs-lookup"><span data-stu-id="006f5-113">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>
<span data-ttu-id="006f5-114">A remoção de uma regra de autorização também remove a permissão do usuário correspondente.</span><span class="sxs-lookup"><span data-stu-id="006f5-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="006f5-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="006f5-115">EXAMPLES</span></span>

### <span data-ttu-id="006f5-116">Exemplo 1: remover uma regra de autorização de um namespace</span><span class="sxs-lookup"><span data-stu-id="006f5-116">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzNotificationHubNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="006f5-117">Esse comando Remove a regra de autorização chamada ListenRule do namespace chamado ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="006f5-117">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="006f5-118">Ao executar esse comando, você deve especificar o grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="006f5-118">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="006f5-119">OS</span><span class="sxs-lookup"><span data-stu-id="006f5-119">PARAMETERS</span></span>

### <span data-ttu-id="006f5-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="006f5-120">-AuthorizationRule</span></span>
<span data-ttu-id="006f5-121">Especifica o nome da regra de autenticação SAS a ser removida.</span><span class="sxs-lookup"><span data-stu-id="006f5-121">Specifies the name of the SAS authentication rule to be removed.</span></span>

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

### <span data-ttu-id="006f5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="006f5-122">-DefaultProfile</span></span>
<span data-ttu-id="006f5-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="006f5-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="006f5-124">-Force</span><span class="sxs-lookup"><span data-stu-id="006f5-124">-Force</span></span>
<span data-ttu-id="006f5-125">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="006f5-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="006f5-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="006f5-126">-Namespace</span></span>
<span data-ttu-id="006f5-127">Especifica o namespace para o qual as regras de autorização são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="006f5-127">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="006f5-128">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="006f5-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="006f5-129">-Resource</span><span class="sxs-lookup"><span data-stu-id="006f5-129">-ResourceGroup</span></span>
<span data-ttu-id="006f5-130">Especifica o grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="006f5-130">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="006f5-131">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="006f5-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="006f5-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="006f5-132">-Confirm</span></span>
<span data-ttu-id="006f5-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="006f5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="006f5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="006f5-134">-WhatIf</span></span>
<span data-ttu-id="006f5-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="006f5-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="006f5-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="006f5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="006f5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="006f5-137">CommonParameters</span></span>
<span data-ttu-id="006f5-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="006f5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="006f5-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="006f5-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="006f5-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="006f5-140">INPUTS</span></span>

### <span data-ttu-id="006f5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="006f5-141">System.String</span></span>

## <span data-ttu-id="006f5-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="006f5-142">OUTPUTS</span></span>

### <span data-ttu-id="006f5-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="006f5-143">System.Boolean</span></span>

## <span data-ttu-id="006f5-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="006f5-144">NOTES</span></span>

## <span data-ttu-id="006f5-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="006f5-145">RELATED LINKS</span></span>

[<span data-ttu-id="006f5-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="006f5-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="006f5-147">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="006f5-147">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="006f5-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="006f5-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Set-AzNotificationHubsNamespaceAuthorizationRule.md)


