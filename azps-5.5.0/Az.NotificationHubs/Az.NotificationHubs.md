---
Module Name: Az.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs
Help Version: 4.1.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
ms.openlocfilehash: dd39a8f87120ea7aaddb4570276e1e3060873e2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111543"
---
# <span data-ttu-id="bab89-101">Módulo Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="bab89-101">Az.NotificationHubs Module</span></span>
## <span data-ttu-id="bab89-102">Descrição</span><span class="sxs-lookup"><span data-stu-id="bab89-102">Description</span></span>
<span data-ttu-id="bab89-103">Este tópico exibe tópicos de ajuda para os cmdlets do Hub de Notificação do Azure.</span><span class="sxs-lookup"><span data-stu-id="bab89-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="bab89-104">Os hubs de notificação são usados para enviar notificações por push para vários clientes independentemente da plataforma (iOS, Android, Windows Phone 8, Windows Store, etc.) usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="bab89-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="bab89-105">Esses hubs são aproximadamente equivalentes a aplicativos individuais: cada um dos seus aplicativos normalmente terá seu próprio hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="bab89-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="bab89-106">Os hubs de notificação são organizados dentro de contêineres lógicos conhecidos como namespaces, e as regras de autorização de Assinatura de Acesso Compartilhado (SAS) são usadas para gerenciar o acesso a hubs e namespaces.</span><span class="sxs-lookup"><span data-stu-id="bab89-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="bab89-107">Todos esses elementos podem ser administrados usando os cmdlets do Hub de Notificação.</span><span class="sxs-lookup"><span data-stu-id="bab89-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="bab89-108">Az.NotificationHubs Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bab89-108">Az.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="bab89-109">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="bab89-109">Get-AzNotificationHub</span></span>](Get-AzNotificationHub.md)
<span data-ttu-id="bab89-110">Obtém informações sobre seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="bab89-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="bab89-111">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bab89-111">Get-AzNotificationHubAuthorizationRule</span></span>](Get-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="bab89-112">Obtém informações sobre as regras de autorização associadas a um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="bab89-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="bab89-113">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="bab89-113">Get-AzNotificationHubListKey</span></span>](Get-AzNotificationHubListKey.md)
<span data-ttu-id="bab89-114">Obtém as cadeias de conexão primária e secundária associadas a uma regra de autorização do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="bab89-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="bab89-115">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="bab89-115">Get-AzNotificationHubPNSCredential</span></span>](Get-AzNotificationHubPNSCredential.md)
<span data-ttu-id="bab89-116">Obtém as credenciais PNS para um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="bab89-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="bab89-117">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="bab89-117">Get-AzNotificationHubsNamespace</span></span>](Get-AzNotificationHubsNamespace.md)
<span data-ttu-id="bab89-118">Obtém informações sobre um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="bab89-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="bab89-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bab89-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Get-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="bab89-120">Obtém informações sobre as regras de autorização associadas a um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="bab89-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="bab89-121">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="bab89-121">Get-AzNotificationHubsNamespaceListKey</span></span>](Get-AzNotificationHubsNamespaceListKey.md)
<span data-ttu-id="bab89-122">Obtém as cadeias de conexão primária e secundária associadas a uma regra de autorização do namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="bab89-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="bab89-123">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="bab89-123">New-AzNotificationHub</span></span>](New-AzNotificationHub.md)
<span data-ttu-id="bab89-124">Cria um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="bab89-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="bab89-125">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bab89-125">New-AzNotificationHubAuthorizationRule</span></span>](New-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="bab89-126">Cria uma regra de autorização e atribui a regra a um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="bab89-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="bab89-127">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="bab89-127">New-AzNotificationHubKey</span></span>](New-AzNotificationHubKey.md)
<span data-ttu-id="bab89-128">Regenerar a Chave de Regra de Autorização para um NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="bab89-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="bab89-129">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="bab89-129">New-AzNotificationHubsNamespace</span></span>](New-AzNotificationHubsNamespace.md)
<span data-ttu-id="bab89-130">Cria um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="bab89-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="bab89-131">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bab89-131">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](New-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="bab89-132">Cria uma regra de autorização e atribui essa regra a um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="bab89-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="bab89-133">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="bab89-133">New-AzNotificationHubsNamespaceKey</span></span>](New-AzNotificationHubsNamespaceKey.md)
<span data-ttu-id="bab89-134">Regenerar a Chave de Regra de Autorização para um Namespace.</span><span class="sxs-lookup"><span data-stu-id="bab89-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="bab89-135">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="bab89-135">Remove-AzNotificationHub</span></span>](Remove-AzNotificationHub.md)
<span data-ttu-id="bab89-136">Remove um hub de notificação existente.</span><span class="sxs-lookup"><span data-stu-id="bab89-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="bab89-137">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bab89-137">Remove-AzNotificationHubAuthorizationRule</span></span>](Remove-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="bab89-138">Remove uma regra de autorização de um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="bab89-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="bab89-139">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="bab89-139">Remove-AzNotificationHubsNamespace</span></span>](Remove-AzNotificationHubsNamespace.md)
<span data-ttu-id="bab89-140">Remove um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="bab89-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="bab89-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bab89-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Remove-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="bab89-142">Remove uma regra de autorização de um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="bab89-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="bab89-143">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="bab89-143">Set-AzNotificationHub</span></span>](Set-AzNotificationHub.md)
<span data-ttu-id="bab89-144">Define valores de propriedade para um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="bab89-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="bab89-145">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bab89-145">Set-AzNotificationHubAuthorizationRule</span></span>](Set-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="bab89-146">Define regras de autorização para um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="bab89-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="bab89-147">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="bab89-147">Set-AzNotificationHubsNamespace</span></span>](Set-AzNotificationHubsNamespace.md)
<span data-ttu-id="bab89-148">Define valores de propriedade para um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="bab89-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="bab89-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bab89-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Set-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="bab89-150">Define regras de autorização para um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="bab89-150">Sets authorization rules for a notification hub namespace.</span></span>

