---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: bb92344616c79db26b37bd9b18bdff7973946c24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429206"
---
# <span data-ttu-id="47e6c-101">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="47e6c-101">Remove-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="47e6c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47e6c-102">SYNOPSIS</span></span>
<span data-ttu-id="47e6c-103">Remove uma regra de autorização de um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="47e6c-103">Removes an authorization rule from a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47e6c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47e6c-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47e6c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="47e6c-105">DESCRIPTION</span></span>
<span data-ttu-id="47e6c-106">O cmdlet **Remove-AzureRmNotificationHubAuthorizationRules** remove uma regra de autorização de assinatura de acesso compartilhado (SAS) de um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="47e6c-106">The **Remove-AzureRmNotificationHubAuthorizationRules** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>

<span data-ttu-id="47e6c-107">As regras de autorização gerenciam o acesso aos seus hubs de notificação por meio da criação de links, como URIs, com base em diferentes níveis de permissão.</span><span class="sxs-lookup"><span data-stu-id="47e6c-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="47e6c-108">Os níveis de permissão podem ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="47e6c-108">Permission levels can be one of the following:</span></span> 

- <span data-ttu-id="47e6c-109">Ouvir</span><span class="sxs-lookup"><span data-stu-id="47e6c-109">Listen</span></span>
- <span data-ttu-id="47e6c-110">Enviar</span><span class="sxs-lookup"><span data-stu-id="47e6c-110">Send</span></span>
- <span data-ttu-id="47e6c-111">Gerencia</span><span class="sxs-lookup"><span data-stu-id="47e6c-111">Manage</span></span>

<span data-ttu-id="47e6c-112">Os clientes são direcionados para um desses URIs com base no nível de permissão apropriado.</span><span class="sxs-lookup"><span data-stu-id="47e6c-112">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="47e6c-113">Por exemplo, um cliente que recebeu a permissão de escuta será direcionado para o URI dessa permissão.</span><span class="sxs-lookup"><span data-stu-id="47e6c-113">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="47e6c-114">A remoção de uma regra de autorização também remove a permissão do usuário correspondente.</span><span class="sxs-lookup"><span data-stu-id="47e6c-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="47e6c-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47e6c-115">EXAMPLES</span></span>

### <span data-ttu-id="47e6c-116">Exemplo 1: remover uma regra de autorização de um hub de notificação</span><span class="sxs-lookup"><span data-stu-id="47e6c-116">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="47e6c-117">Esse comando Remove a regra de autorização chamada ListenRule do hub de notificação chamado ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="47e6c-117">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="47e6c-118">Ao executar esse comando, você deve especificar o namespace e o grupo de recursos aos quais o Hub está atribuído.</span><span class="sxs-lookup"><span data-stu-id="47e6c-118">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="47e6c-119">OS</span><span class="sxs-lookup"><span data-stu-id="47e6c-119">PARAMETERS</span></span>

### <span data-ttu-id="47e6c-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="47e6c-120">-AuthorizationRule</span></span>
<span data-ttu-id="47e6c-121">Especifica o nome da regra de autenticação SAS que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="47e6c-121">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="47e6c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="47e6c-122">-Force</span></span>
<span data-ttu-id="47e6c-123">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="47e6c-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="47e6c-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="47e6c-124">-Namespace</span></span>
<span data-ttu-id="47e6c-125">Especifica o namespace ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="47e6c-125">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="47e6c-126">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="47e6c-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="47e6c-127">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="47e6c-127">-NotificationHub</span></span>
<span data-ttu-id="47e6c-128">Especifica o Hub de notificação ao qual as regras de autorização são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="47e6c-128">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="47e6c-129">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma.</span><span class="sxs-lookup"><span data-stu-id="47e6c-129">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

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

### <span data-ttu-id="47e6c-130">-Resource</span><span class="sxs-lookup"><span data-stu-id="47e6c-130">-ResourceGroup</span></span>
<span data-ttu-id="47e6c-131">Especifica o grupo de recursos ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="47e6c-131">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="47e6c-132">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="47e6c-132">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="47e6c-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="47e6c-133">-Confirm</span></span>
<span data-ttu-id="47e6c-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47e6c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47e6c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47e6c-135">-WhatIf</span></span>
<span data-ttu-id="47e6c-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="47e6c-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47e6c-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="47e6c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47e6c-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47e6c-138">-DefaultProfile</span></span>
<span data-ttu-id="47e6c-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47e6c-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47e6c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47e6c-140">CommonParameters</span></span>
<span data-ttu-id="47e6c-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47e6c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47e6c-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47e6c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47e6c-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="47e6c-143">INPUTS</span></span>

## <span data-ttu-id="47e6c-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="47e6c-144">OUTPUTS</span></span>

## <span data-ttu-id="47e6c-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="47e6c-145">NOTES</span></span>

## <span data-ttu-id="47e6c-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47e6c-146">RELATED LINKS</span></span>

[<span data-ttu-id="47e6c-147">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="47e6c-147">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="47e6c-148">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="47e6c-148">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="47e6c-149">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="47e6c-149">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


