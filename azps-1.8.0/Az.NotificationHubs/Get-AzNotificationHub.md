---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: ea16c01e5c528742702dd08f1f2bd4c14e0cebcd
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399933"
---
# <span data-ttu-id="565dd-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="565dd-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="565dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="565dd-102">SYNOPSIS</span></span>
<span data-ttu-id="565dd-103">Obtém informações sobre seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="565dd-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="565dd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="565dd-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="565dd-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="565dd-105">DESCRIPTION</span></span>
<span data-ttu-id="565dd-106">O **cmdlet Get-AzNotificationHub** obtém informações sobre os hubs de notificação em um espaço de nome especificado e atribuído a um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="565dd-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="565dd-107">Por exemplo, você pode obter informações para todos os hubs de notificação no namespace ContosoNamespace e atribuídas ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="565dd-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="565dd-108">Como alternativa, você pode usar o parâmetro *NotificationHub* para limitar os dados retornados a informações sobre um hub de notificação específico.</span><span class="sxs-lookup"><span data-stu-id="565dd-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="565dd-109">Os hubs de notificação são usados para enviar notificações por push para vários clientes independentemente da plataforma, como iOS, Android, Windows Phone 8 e Windows Store, usados por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="565dd-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="565dd-110">Esses hubs são aproximadamente equivalentes a aplicativos individuais e cada um dos seus aplicativos normalmente terá seu próprio hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="565dd-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="565dd-111">Este cmdlet só obtém informações sobre o hub em si.</span><span class="sxs-lookup"><span data-stu-id="565dd-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="565dd-112">Outros cmdlets, como Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys e Get-AzNotificationHubPNSCredentials, são necessários para obter informações sobre regras de autorização do hub, cadeias de conexão e credenciais de serviço de notificação de plataforma.</span><span class="sxs-lookup"><span data-stu-id="565dd-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="565dd-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="565dd-113">EXAMPLES</span></span>

### <span data-ttu-id="565dd-114">Exemplo 1: Obter informações para todos os hubs de notificação em um namespace específico</span><span class="sxs-lookup"><span data-stu-id="565dd-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="565dd-115">Esse comando obtém informações para todos os hubs de notificação no namespace chamado ContosoNamespace que foram atribuídos ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="565dd-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="565dd-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="565dd-116">PARAMETERS</span></span>

### <span data-ttu-id="565dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="565dd-117">-DefaultProfile</span></span>
<span data-ttu-id="565dd-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="565dd-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="565dd-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="565dd-119">-Namespace</span></span>
<span data-ttu-id="565dd-120">Especifica o namespace ao qual o hub de notificação está atribuído.</span><span class="sxs-lookup"><span data-stu-id="565dd-120">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="565dd-121">Os namespaces oferecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="565dd-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="565dd-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="565dd-122">-NotificationHub</span></span>
<span data-ttu-id="565dd-123">Especifica o nome do hub de notificação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="565dd-123">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="565dd-124">Os hubs de notificação são usados para enviar notificações por push para vários clientes independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="565dd-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="565dd-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="565dd-125">-ResourceGroup</span></span>
<span data-ttu-id="565dd-126">Especifica o grupo de recursos ao qual o hub de notificação está atribuído.</span><span class="sxs-lookup"><span data-stu-id="565dd-126">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="565dd-127">Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente o gerenciamento de estoque e a administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="565dd-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="565dd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="565dd-128">CommonParameters</span></span>
<span data-ttu-id="565dd-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="565dd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="565dd-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="565dd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="565dd-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="565dd-131">INPUTS</span></span>

### <span data-ttu-id="565dd-132">System.String</span><span class="sxs-lookup"><span data-stu-id="565dd-132">System.String</span></span>

## <span data-ttu-id="565dd-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="565dd-133">OUTPUTS</span></span>

### <span data-ttu-id="565dd-134">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="565dd-134">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="565dd-135">Notas</span><span class="sxs-lookup"><span data-stu-id="565dd-135">NOTES</span></span>

## <span data-ttu-id="565dd-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="565dd-136">RELATED LINKS</span></span>




[<span data-ttu-id="565dd-137">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="565dd-137">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="565dd-138">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="565dd-138">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="565dd-139">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="565dd-139">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


