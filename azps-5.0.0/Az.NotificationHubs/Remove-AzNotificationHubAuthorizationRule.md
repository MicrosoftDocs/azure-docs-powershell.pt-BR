---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: d908d9d12e917efca6901c08bc69d4888072b6ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116041"
---
# <span data-ttu-id="36121-101">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="36121-101">Remove-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="36121-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36121-102">SYNOPSIS</span></span>
<span data-ttu-id="36121-103">Remove uma regra de autorização de um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="36121-103">Removes an authorization rule from a notification hub.</span></span>

## <span data-ttu-id="36121-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36121-104">SYNTAX</span></span>

```
Remove-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36121-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="36121-105">DESCRIPTION</span></span>
<span data-ttu-id="36121-106">O cmdlet **Remove-AzNotificationHubAuthorizationRule** remove uma regra de autorização de assinatura de acesso compartilhado (SAS) de um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="36121-106">The **Remove-AzNotificationHubAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>
<span data-ttu-id="36121-107">As regras de autorização gerenciam o acesso aos seus hubs de notificação por meio da criação de links, como URIs, com base em diferentes níveis de permissão.</span><span class="sxs-lookup"><span data-stu-id="36121-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="36121-108">Os níveis de permissão podem ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="36121-108">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="36121-109">Ouvir</span><span class="sxs-lookup"><span data-stu-id="36121-109">Listen</span></span>
- <span data-ttu-id="36121-110">Enviar</span><span class="sxs-lookup"><span data-stu-id="36121-110">Send</span></span>
- <span data-ttu-id="36121-111">Gerenciar clientes são direcionados para um desses URIs com base no nível de permissão apropriado.</span><span class="sxs-lookup"><span data-stu-id="36121-111">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="36121-112">Por exemplo, um cliente que recebeu a permissão de escuta será direcionado para o URI dessa permissão.</span><span class="sxs-lookup"><span data-stu-id="36121-112">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="36121-113">A remoção de uma regra de autorização também remove a permissão do usuário correspondente.</span><span class="sxs-lookup"><span data-stu-id="36121-113">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="36121-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36121-114">EXAMPLES</span></span>

### <span data-ttu-id="36121-115">Exemplo 1: remover uma regra de autorização de um hub de notificação</span><span class="sxs-lookup"><span data-stu-id="36121-115">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="36121-116">Esse comando Remove a regra de autorização chamada ListenRule do hub de notificação chamado ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="36121-116">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="36121-117">Ao executar esse comando, você deve especificar o namespace e o grupo de recursos aos quais o Hub está atribuído.</span><span class="sxs-lookup"><span data-stu-id="36121-117">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="36121-118">OS</span><span class="sxs-lookup"><span data-stu-id="36121-118">PARAMETERS</span></span>

### <span data-ttu-id="36121-119">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="36121-119">-AuthorizationRule</span></span>
<span data-ttu-id="36121-120">Especifica o nome da regra de autenticação SAS que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="36121-120">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36121-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36121-121">-DefaultProfile</span></span>
<span data-ttu-id="36121-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="36121-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36121-123">-Force</span><span class="sxs-lookup"><span data-stu-id="36121-123">-Force</span></span>
<span data-ttu-id="36121-124">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="36121-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="36121-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="36121-125">-Namespace</span></span>
<span data-ttu-id="36121-126">Especifica o namespace ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="36121-126">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="36121-127">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="36121-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="36121-128">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="36121-128">-NotificationHub</span></span>
<span data-ttu-id="36121-129">Especifica o Hub de notificação ao qual as regras de autorização são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="36121-129">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="36121-130">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma.</span><span class="sxs-lookup"><span data-stu-id="36121-130">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

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

### <span data-ttu-id="36121-131">-Resource</span><span class="sxs-lookup"><span data-stu-id="36121-131">-ResourceGroup</span></span>
<span data-ttu-id="36121-132">Especifica o grupo de recursos ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="36121-132">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="36121-133">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="36121-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="36121-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="36121-134">-Confirm</span></span>
<span data-ttu-id="36121-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36121-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36121-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36121-136">-WhatIf</span></span>
<span data-ttu-id="36121-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="36121-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36121-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="36121-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36121-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36121-139">CommonParameters</span></span>
<span data-ttu-id="36121-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36121-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36121-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36121-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36121-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="36121-142">INPUTS</span></span>

### <span data-ttu-id="36121-143">System. String</span><span class="sxs-lookup"><span data-stu-id="36121-143">System.String</span></span>

## <span data-ttu-id="36121-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="36121-144">OUTPUTS</span></span>

### <span data-ttu-id="36121-145">System. void</span><span class="sxs-lookup"><span data-stu-id="36121-145">System.Void</span></span>

## <span data-ttu-id="36121-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="36121-146">NOTES</span></span>

## <span data-ttu-id="36121-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36121-147">RELATED LINKS</span></span>

[<span data-ttu-id="36121-148">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="36121-148">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="36121-149">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="36121-149">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="36121-150">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="36121-150">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


