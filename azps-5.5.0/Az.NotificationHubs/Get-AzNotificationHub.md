---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: 944805a4883edce9354cfa372bfd30db145fc4ca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115033"
---
# <span data-ttu-id="22782-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="22782-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="22782-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22782-102">SYNOPSIS</span></span>
<span data-ttu-id="22782-103">Obtém informações sobre seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="22782-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="22782-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22782-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22782-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="22782-105">DESCRIPTION</span></span>
<span data-ttu-id="22782-106">O **cmdlet Get-AzNotificationHub** obtém informações sobre os hubs de notificação em um espaço de nome especificado e atribuído a um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="22782-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="22782-107">Por exemplo, você pode obter informações para todos os hubs de notificação no namespace ContosoNamespace e atribuídas ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="22782-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="22782-108">Como alternativa, você pode usar o parâmetro *NotificationHub* para limitar os dados retornados a informações sobre um hub de notificação específico.</span><span class="sxs-lookup"><span data-stu-id="22782-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="22782-109">Os hubs de notificação são usados para enviar notificações por push para vários clientes independentemente da plataforma, como iOS, Android, Windows Phone 8 e Windows Store, usados por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="22782-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="22782-110">Esses hubs são aproximadamente equivalentes a aplicativos individuais e cada um dos seus aplicativos normalmente terá seu próprio hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="22782-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="22782-111">Este cmdlet só obtém informações sobre o hub em si.</span><span class="sxs-lookup"><span data-stu-id="22782-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="22782-112">Outros cmdlets, como Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys e Get-AzNotificationHubPNSCredentials, são necessários para obter informações sobre regras de autorização do hub, cadeias de conexão e credenciais de serviço de notificação de plataforma.</span><span class="sxs-lookup"><span data-stu-id="22782-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="22782-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="22782-113">EXAMPLES</span></span>

### <span data-ttu-id="22782-114">Exemplo 1: Obter informações para todos os hubs de notificação em um namespace específico</span><span class="sxs-lookup"><span data-stu-id="22782-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```powershell
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="22782-115">Esse comando obtém informações para todos os hubs de notificação no namespace chamado ContosoNamespace que foram atribuídos ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="22782-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

### <span data-ttu-id="22782-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="22782-116">Example 2</span></span>

<span data-ttu-id="22782-117">Obtém informações sobre seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="22782-117">Gets information about your notification hubs.</span></span> <span data-ttu-id="22782-118">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="22782-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHub 'ContosoInternalHub' -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="22782-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22782-119">PARAMETERS</span></span>

### <span data-ttu-id="22782-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22782-120">-DefaultProfile</span></span>
<span data-ttu-id="22782-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="22782-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22782-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="22782-122">-Namespace</span></span>
<span data-ttu-id="22782-123">Especifica o namespace ao qual o hub de notificação está atribuído.</span><span class="sxs-lookup"><span data-stu-id="22782-123">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="22782-124">Os namespaces oferecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="22782-124">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="22782-125">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="22782-125">-NotificationHub</span></span>
<span data-ttu-id="22782-126">Especifica o nome do hub de notificação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="22782-126">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="22782-127">Os hubs de notificação são usados para enviar notificações por push para vários clientes independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="22782-127">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="22782-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="22782-128">-ResourceGroup</span></span>
<span data-ttu-id="22782-129">Especifica o grupo de recursos ao qual o hub de notificação está atribuído.</span><span class="sxs-lookup"><span data-stu-id="22782-129">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="22782-130">Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente o gerenciamento de estoque e a administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="22782-130">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="22782-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22782-131">CommonParameters</span></span>
<span data-ttu-id="22782-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22782-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22782-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22782-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22782-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="22782-134">INPUTS</span></span>

### <span data-ttu-id="22782-135">System.String</span><span class="sxs-lookup"><span data-stu-id="22782-135">System.String</span></span>

## <span data-ttu-id="22782-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="22782-136">OUTPUTS</span></span>

### <span data-ttu-id="22782-137">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="22782-137">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="22782-138">Notas</span><span class="sxs-lookup"><span data-stu-id="22782-138">NOTES</span></span>

## <span data-ttu-id="22782-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22782-139">RELATED LINKS</span></span>

[<span data-ttu-id="22782-140">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="22782-140">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="22782-141">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="22782-141">Get-AzNotificationHubListKey</span></span>](./Get-AzNotificationHubListKey.md)

[<span data-ttu-id="22782-142">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="22782-142">Get-AzNotificationHubPNSCredential</span></span>](./Get-AzNotificationHubPNSCredential.md)

[<span data-ttu-id="22782-143">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="22782-143">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="22782-144">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="22782-144">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="22782-145">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="22782-145">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


