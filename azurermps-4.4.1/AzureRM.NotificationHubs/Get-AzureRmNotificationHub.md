---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
ms.openlocfilehash: 2bb7d6f6addbbbf91f7f9f93e7e30de9cb3ece81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441034"
---
# <span data-ttu-id="a9015-101">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a9015-101">Get-AzureRmNotificationHub</span></span>

## <span data-ttu-id="a9015-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9015-102">SYNOPSIS</span></span>
<span data-ttu-id="a9015-103">Obtém informações sobre seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="a9015-103">Gets information about your notification hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9015-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9015-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9015-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a9015-105">DESCRIPTION</span></span>
<span data-ttu-id="a9015-106">O cmdlet **Get-AzureRmNotificationHub** Obtém informações sobre os hubs de notificação em um namespace especificado e atribuídos a um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="a9015-106">The **Get-AzureRmNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="a9015-107">Por exemplo, você pode obter informações para todos os hubs de notificação no namespace ContosoNamespace e atribuídas ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="a9015-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>

<span data-ttu-id="a9015-108">Você também pode usar o parâmetro *NotificationHub* para limitar os dados retornados às informações sobre um hub de notificação específico.</span><span class="sxs-lookup"><span data-stu-id="a9015-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>

<span data-ttu-id="a9015-109">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma, como iOS, Android, Windows Phone 8 e Windows Store, usados por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="a9015-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="a9015-110">Esses hubs são aproximadamente equivalentes a aplicativos individuais e cada um dos seus aplicativos normalmente tem seu próprio Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="a9015-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>

<span data-ttu-id="a9015-111">Este cmdlet somente Obtém informações sobre o próprio Hub.</span><span class="sxs-lookup"><span data-stu-id="a9015-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="a9015-112">Outros cmdlets, como Get-AzureRmNotificationHubAuthorizationRules, Get-AzureRmNotificationHubListKeys e Get-AzureRmNotificationHubPNSCredentials, são necessários para obter informações sobre as regras de autorização de um Hub, cadeias de conexão e credenciais do serviço de notificação de plataforma.</span><span class="sxs-lookup"><span data-stu-id="a9015-112">Other cmdlets, such as Get-AzureRmNotificationHubAuthorizationRules, Get-AzureRmNotificationHubListKeys, and Get-AzureRmNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="a9015-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9015-113">EXAMPLES</span></span>

### <span data-ttu-id="a9015-114">Exemplo 1: obter informações para todos os hubs de notificação em um namespace específico</span><span class="sxs-lookup"><span data-stu-id="a9015-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="a9015-115">Esse comando obtém informações para todos os hubs de notificação no namespace chamado ContosoNamespace que foram atribuídos à ContosoNotificationsGroup do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a9015-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="a9015-116">OS</span><span class="sxs-lookup"><span data-stu-id="a9015-116">PARAMETERS</span></span>

### <span data-ttu-id="a9015-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a9015-117">-Namespace</span></span>
<span data-ttu-id="a9015-118">Especifica o namespace ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="a9015-118">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="a9015-119">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="a9015-119">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="a9015-120">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="a9015-120">-NotificationHub</span></span>
<span data-ttu-id="a9015-121">Especifica o nome do hub de notificação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="a9015-121">Specifies the name of the notification hub that this cmdlet gets.</span></span>

<span data-ttu-id="a9015-122">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="a9015-122">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="a9015-123">-Resource</span><span class="sxs-lookup"><span data-stu-id="a9015-123">-ResourceGroup</span></span>
<span data-ttu-id="a9015-124">Especifica o grupo de recursos ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="a9015-124">Specifies the resource group to which the notification hub is assigned.</span></span>

<span data-ttu-id="a9015-125">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="a9015-125">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="a9015-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9015-126">-DefaultProfile</span></span>
<span data-ttu-id="a9015-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a9015-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9015-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9015-128">CommonParameters</span></span>
<span data-ttu-id="a9015-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9015-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9015-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9015-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9015-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a9015-131">INPUTS</span></span>

## <span data-ttu-id="a9015-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a9015-132">OUTPUTS</span></span>

### <span data-ttu-id="a9015-133">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes]</span><span class="sxs-lookup"><span data-stu-id="a9015-133">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes]</span></span>

## <span data-ttu-id="a9015-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a9015-134">NOTES</span></span>

## <span data-ttu-id="a9015-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9015-135">RELATED LINKS</span></span>

[<span data-ttu-id="a9015-136">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a9015-136">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="a9015-137">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="a9015-137">Get-AzureRmNotificationHubListKeys</span></span>](./Get-AzureRmNotificationHubListKeys.md)

[<span data-ttu-id="a9015-138">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="a9015-138">Get-AzureRmNotificationHubPNSCredentials</span></span>](./Get-AzureRmNotificationHubPNSCredentials.md)

[<span data-ttu-id="a9015-139">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a9015-139">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="a9015-140">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a9015-140">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)

[<span data-ttu-id="a9015-141">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a9015-141">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


