---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: f58a34c5fb5a7ca108f2f4f55c9322f1f439fbf9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772681"
---
# <span data-ttu-id="b6c60-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="b6c60-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="b6c60-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6c60-102">SYNOPSIS</span></span>
<span data-ttu-id="b6c60-103">Obtém informações sobre seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="b6c60-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="b6c60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6c60-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6c60-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b6c60-105">DESCRIPTION</span></span>
<span data-ttu-id="b6c60-106">O cmdlet **Get-AzNotificationHub** Obtém informações sobre os hubs de notificação em um namespace especificado e atribuídos a um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="b6c60-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="b6c60-107">Por exemplo, você pode obter informações para todos os hubs de notificação no namespace ContosoNamespace e atribuídas ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="b6c60-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="b6c60-108">Você também pode usar o parâmetro *NotificationHub* para limitar os dados retornados às informações sobre um hub de notificação específico.</span><span class="sxs-lookup"><span data-stu-id="b6c60-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="b6c60-109">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma, como iOS, Android, Windows Phone 8 e Windows Store, usados por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="b6c60-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="b6c60-110">Esses hubs são aproximadamente equivalentes a aplicativos individuais e cada um dos seus aplicativos normalmente tem seu próprio Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="b6c60-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="b6c60-111">Este cmdlet somente Obtém informações sobre o próprio Hub.</span><span class="sxs-lookup"><span data-stu-id="b6c60-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="b6c60-112">Outros cmdlets, como Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys e Get-AzNotificationHubPNSCredentials, são necessários para obter informações sobre as regras de autorização de um Hub, cadeias de conexão e credenciais do serviço de notificação de plataforma.</span><span class="sxs-lookup"><span data-stu-id="b6c60-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="b6c60-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6c60-113">EXAMPLES</span></span>

### <span data-ttu-id="b6c60-114">Exemplo 1: obter informações para todos os hubs de notificação em um namespace específico</span><span class="sxs-lookup"><span data-stu-id="b6c60-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="b6c60-115">Esse comando obtém informações para todos os hubs de notificação no namespace chamado ContosoNamespace que foram atribuídos à ContosoNotificationsGroup do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b6c60-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="b6c60-116">OS</span><span class="sxs-lookup"><span data-stu-id="b6c60-116">PARAMETERS</span></span>

### <span data-ttu-id="b6c60-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6c60-117">-DefaultProfile</span></span>
<span data-ttu-id="b6c60-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b6c60-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6c60-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b6c60-119">-Namespace</span></span>
<span data-ttu-id="b6c60-120">Especifica o namespace ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="b6c60-120">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="b6c60-121">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="b6c60-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="b6c60-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="b6c60-122">-NotificationHub</span></span>
<span data-ttu-id="b6c60-123">Especifica o nome do hub de notificação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="b6c60-123">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="b6c60-124">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="b6c60-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="b6c60-125">-Resource</span><span class="sxs-lookup"><span data-stu-id="b6c60-125">-ResourceGroup</span></span>
<span data-ttu-id="b6c60-126">Especifica o grupo de recursos ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="b6c60-126">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="b6c60-127">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="b6c60-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="b6c60-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6c60-128">CommonParameters</span></span>
<span data-ttu-id="b6c60-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6c60-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6c60-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6c60-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6c60-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b6c60-131">INPUTS</span></span>

### <span data-ttu-id="b6c60-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b6c60-132">System.String</span></span>

## <span data-ttu-id="b6c60-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b6c60-133">OUTPUTS</span></span>

### <span data-ttu-id="b6c60-134">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="b6c60-134">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="b6c60-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b6c60-135">NOTES</span></span>

## <span data-ttu-id="b6c60-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6c60-136">RELATED LINKS</span></span>

[<span data-ttu-id="b6c60-137">Get-AzNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="b6c60-137">Get-AzNotificationHubAuthorizationRules</span></span>](./Get-AzNotificationHubAuthorizationRules.md)

[<span data-ttu-id="b6c60-138">Get-AzNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="b6c60-138">Get-AzNotificationHubListKeys</span></span>](./Get-AzNotificationHubListKeys.md)

[<span data-ttu-id="b6c60-139">Get-AzNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="b6c60-139">Get-AzNotificationHubPNSCredentials</span></span>](./Get-AzNotificationHubPNSCredentials.md)

[<span data-ttu-id="b6c60-140">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="b6c60-140">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="b6c60-141">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="b6c60-141">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="b6c60-142">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="b6c60-142">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


