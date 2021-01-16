---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: 944805a4883edce9354cfa372bfd30db145fc4ca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258762"
---
# <span data-ttu-id="f6755-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f6755-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="f6755-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6755-102">SYNOPSIS</span></span>
<span data-ttu-id="f6755-103">Obtém informações sobre seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="f6755-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="f6755-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6755-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6755-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f6755-105">DESCRIPTION</span></span>
<span data-ttu-id="f6755-106">O cmdlet **Get-AzNotificationHub** Obtém informações sobre os hubs de notificação em um namespace especificado e atribuídos a um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="f6755-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="f6755-107">Por exemplo, você pode obter informações para todos os hubs de notificação no namespace ContosoNamespace e atribuídas ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="f6755-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="f6755-108">Você também pode usar o parâmetro *NotificationHub* para limitar os dados retornados às informações sobre um hub de notificação específico.</span><span class="sxs-lookup"><span data-stu-id="f6755-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="f6755-109">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma, como iOS, Android, Windows Phone 8 e Windows Store, usados por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="f6755-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="f6755-110">Esses hubs são aproximadamente equivalentes a aplicativos individuais e cada um dos seus aplicativos normalmente tem seu próprio Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f6755-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="f6755-111">Este cmdlet somente Obtém informações sobre o próprio Hub.</span><span class="sxs-lookup"><span data-stu-id="f6755-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="f6755-112">Outros cmdlets, como Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys e Get-AzNotificationHubPNSCredentials, são necessários para obter informações sobre as regras de autorização de um Hub, cadeias de conexão e credenciais do serviço de notificação de plataforma.</span><span class="sxs-lookup"><span data-stu-id="f6755-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="f6755-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6755-113">EXAMPLES</span></span>

### <span data-ttu-id="f6755-114">Exemplo 1: obter informações para todos os hubs de notificação em um namespace específico</span><span class="sxs-lookup"><span data-stu-id="f6755-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```powershell
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="f6755-115">Esse comando obtém informações para todos os hubs de notificação no namespace chamado ContosoNamespace que foram atribuídos à ContosoNotificationsGroup do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f6755-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

### <span data-ttu-id="f6755-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f6755-116">Example 2</span></span>

<span data-ttu-id="f6755-117">Obtém informações sobre seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="f6755-117">Gets information about your notification hubs.</span></span> <span data-ttu-id="f6755-118">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="f6755-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHub 'ContosoInternalHub' -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="f6755-119">OS</span><span class="sxs-lookup"><span data-stu-id="f6755-119">PARAMETERS</span></span>

### <span data-ttu-id="f6755-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6755-120">-DefaultProfile</span></span>
<span data-ttu-id="f6755-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f6755-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6755-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f6755-122">-Namespace</span></span>
<span data-ttu-id="f6755-123">Especifica o namespace ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="f6755-123">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="f6755-124">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="f6755-124">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="f6755-125">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="f6755-125">-NotificationHub</span></span>
<span data-ttu-id="f6755-126">Especifica o nome do hub de notificação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="f6755-126">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="f6755-127">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="f6755-127">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="f6755-128">-Resource</span><span class="sxs-lookup"><span data-stu-id="f6755-128">-ResourceGroup</span></span>
<span data-ttu-id="f6755-129">Especifica o grupo de recursos ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="f6755-129">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="f6755-130">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="f6755-130">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="f6755-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6755-131">CommonParameters</span></span>
<span data-ttu-id="f6755-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6755-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6755-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6755-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6755-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f6755-134">INPUTS</span></span>

### <span data-ttu-id="f6755-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f6755-135">System.String</span></span>

## <span data-ttu-id="f6755-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f6755-136">OUTPUTS</span></span>

### <span data-ttu-id="f6755-137">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="f6755-137">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="f6755-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f6755-138">NOTES</span></span>

## <span data-ttu-id="f6755-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6755-139">RELATED LINKS</span></span>

[<span data-ttu-id="f6755-140">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f6755-140">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="f6755-141">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="f6755-141">Get-AzNotificationHubListKey</span></span>](./Get-AzNotificationHubListKey.md)

[<span data-ttu-id="f6755-142">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="f6755-142">Get-AzNotificationHubPNSCredential</span></span>](./Get-AzNotificationHubPNSCredential.md)

[<span data-ttu-id="f6755-143">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f6755-143">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="f6755-144">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f6755-144">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="f6755-145">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f6755-145">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


