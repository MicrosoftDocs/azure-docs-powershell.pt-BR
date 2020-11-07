---
Module Name: Az.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs
Help Version: 4.1.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
ms.openlocfilehash: dd39a8f87120ea7aaddb4570276e1e3060873e2f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942339"
---
# <span data-ttu-id="f282d-101">Módulo AZ. NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="f282d-101">Az.NotificationHubs Module</span></span>
## <span data-ttu-id="f282d-102">Descritivo</span><span class="sxs-lookup"><span data-stu-id="f282d-102">Description</span></span>
<span data-ttu-id="f282d-103">Este tópico exibe os tópicos da ajuda para os cmdlets do hub de notificação do Azure.</span><span class="sxs-lookup"><span data-stu-id="f282d-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="f282d-104">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma (iOS, Android, Windows Phone 8, Windows Store etc.) usadas por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="f282d-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="f282d-105">Esses hubs são aproximadamente equivalentes a aplicativos individuais: cada um dos seus aplicativos normalmente tem seu próprio Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f282d-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="f282d-106">Os hubs de notificação são organizados em recipientes lógicos conhecidos como namespaces e as regras de autorização de assinatura de acesso compartilhado (SAS) são usadas para gerenciar o acesso a hubs e namespaces.</span><span class="sxs-lookup"><span data-stu-id="f282d-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="f282d-107">Todos esses elementos podem ser administrados usando cmdlets do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f282d-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="f282d-108">Cmdlets AZ. NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="f282d-108">Az.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="f282d-109">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f282d-109">Get-AzNotificationHub</span></span>](Get-AzNotificationHub.md)
<span data-ttu-id="f282d-110">Obtém informações sobre seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="f282d-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="f282d-111">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f282d-111">Get-AzNotificationHubAuthorizationRule</span></span>](Get-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="f282d-112">Obtém informações sobre as regras de autorização associadas a um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f282d-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="f282d-113">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="f282d-113">Get-AzNotificationHubListKey</span></span>](Get-AzNotificationHubListKey.md)
<span data-ttu-id="f282d-114">Obtém as cadeias de conexão primária e secundária associadas a uma regra de autorização do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f282d-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="f282d-115">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="f282d-115">Get-AzNotificationHubPNSCredential</span></span>](Get-AzNotificationHubPNSCredential.md)
<span data-ttu-id="f282d-116">Obtém as credenciais do PNS para um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f282d-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="f282d-117">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f282d-117">Get-AzNotificationHubsNamespace</span></span>](Get-AzNotificationHubsNamespace.md)
<span data-ttu-id="f282d-118">Obtém informações sobre um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f282d-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="f282d-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f282d-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Get-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="f282d-120">Obtém informações sobre as regras de autorização associadas a um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f282d-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="f282d-121">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="f282d-121">Get-AzNotificationHubsNamespaceListKey</span></span>](Get-AzNotificationHubsNamespaceListKey.md)
<span data-ttu-id="f282d-122">Obtém as cadeias de conexão primária e secundária associadas a uma regra de autorização de namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f282d-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="f282d-123">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f282d-123">New-AzNotificationHub</span></span>](New-AzNotificationHub.md)
<span data-ttu-id="f282d-124">Cria um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f282d-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="f282d-125">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f282d-125">New-AzNotificationHubAuthorizationRule</span></span>](New-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="f282d-126">Cria uma regra de autorização e atribui a regra a um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f282d-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="f282d-127">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="f282d-127">New-AzNotificationHubKey</span></span>](New-AzNotificationHubKey.md)
<span data-ttu-id="f282d-128">Regenerar a chave de regra de autorização para um NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="f282d-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="f282d-129">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f282d-129">New-AzNotificationHubsNamespace</span></span>](New-AzNotificationHubsNamespace.md)
<span data-ttu-id="f282d-130">Cria um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f282d-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="f282d-131">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f282d-131">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](New-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="f282d-132">Cria uma regra de autorização e atribui essa regra a um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f282d-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="f282d-133">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="f282d-133">New-AzNotificationHubsNamespaceKey</span></span>](New-AzNotificationHubsNamespaceKey.md)
<span data-ttu-id="f282d-134">Regenerar a chave de regra de autorização para um namespace.</span><span class="sxs-lookup"><span data-stu-id="f282d-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="f282d-135">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f282d-135">Remove-AzNotificationHub</span></span>](Remove-AzNotificationHub.md)
<span data-ttu-id="f282d-136">Remove um hub de notificação existente.</span><span class="sxs-lookup"><span data-stu-id="f282d-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="f282d-137">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f282d-137">Remove-AzNotificationHubAuthorizationRule</span></span>](Remove-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="f282d-138">Remove uma regra de autorização de um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f282d-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="f282d-139">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f282d-139">Remove-AzNotificationHubsNamespace</span></span>](Remove-AzNotificationHubsNamespace.md)
<span data-ttu-id="f282d-140">Remove um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f282d-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="f282d-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f282d-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Remove-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="f282d-142">Remove uma regra de autorização de um namespace Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f282d-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="f282d-143">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f282d-143">Set-AzNotificationHub</span></span>](Set-AzNotificationHub.md)
<span data-ttu-id="f282d-144">Define valores de propriedade para um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f282d-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="f282d-145">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f282d-145">Set-AzNotificationHubAuthorizationRule</span></span>](Set-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="f282d-146">Define regras de autorização para um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f282d-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="f282d-147">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f282d-147">Set-AzNotificationHubsNamespace</span></span>](Set-AzNotificationHubsNamespace.md)
<span data-ttu-id="f282d-148">Define valores de propriedade para um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f282d-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="f282d-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f282d-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Set-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="f282d-150">Define regras de autorização para um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f282d-150">Sets authorization rules for a notification hub namespace.</span></span>

