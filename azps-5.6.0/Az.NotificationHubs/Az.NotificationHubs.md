---
Module Name: Az.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link: https://docs.microsoft.com/powershell/module/az.notificationhubs
Help Version: 4.1.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
ms.openlocfilehash: f82f5ec814159bd71a83594a501df3561b747aee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885314"
---
# <span data-ttu-id="df2b4-101">Módulo Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="df2b4-101">Az.NotificationHubs Module</span></span>
## <span data-ttu-id="df2b4-102">Descrição</span><span class="sxs-lookup"><span data-stu-id="df2b4-102">Description</span></span>
<span data-ttu-id="df2b4-103">Este tópico exibe tópicos de ajuda para os cmdlets do Hub de Notificação do Azure.</span><span class="sxs-lookup"><span data-stu-id="df2b4-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="df2b4-104">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma (iOS, Android, Windows Phone 8, Windows Store, etc.) usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="df2b4-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="df2b4-105">Esses hubs são aproximadamente equivalentes a aplicativos individuais: cada um dos seus aplicativos normalmente terá seu próprio hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="df2b4-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="df2b4-106">Os hubs de notificação são organizados em contêineres lógicos conhecidos como namespaces e as regras de autorização de SAS (Assinatura de Acesso Compartilhado) são usadas para gerenciar o acesso a hubs e namespaces.</span><span class="sxs-lookup"><span data-stu-id="df2b4-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="df2b4-107">Todos esses elementos podem ser administrados usando os cmdlets do Hub de Notificação.</span><span class="sxs-lookup"><span data-stu-id="df2b4-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="df2b4-108">Az.NotificationHubs Cmdlets</span><span class="sxs-lookup"><span data-stu-id="df2b4-108">Az.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="df2b4-109">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="df2b4-109">Get-AzNotificationHub</span></span>](Get-AzNotificationHub.md)
<span data-ttu-id="df2b4-110">Obtém informações sobre seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="df2b4-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="df2b4-111">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="df2b4-111">Get-AzNotificationHubAuthorizationRule</span></span>](Get-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="df2b4-112">Obtém informações sobre as regras de autorização associadas a um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="df2b4-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="df2b4-113">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="df2b4-113">Get-AzNotificationHubListKey</span></span>](Get-AzNotificationHubListKey.md)
<span data-ttu-id="df2b4-114">Obtém as cadeias de conexão primárias e secundárias associadas a uma regra de autorização do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="df2b4-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="df2b4-115">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="df2b4-115">Get-AzNotificationHubPNSCredential</span></span>](Get-AzNotificationHubPNSCredential.md)
<span data-ttu-id="df2b4-116">Obtém as credenciais PNS para um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="df2b4-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="df2b4-117">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="df2b4-117">Get-AzNotificationHubsNamespace</span></span>](Get-AzNotificationHubsNamespace.md)
<span data-ttu-id="df2b4-118">Obtém informações sobre um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="df2b4-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="df2b4-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="df2b4-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Get-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="df2b4-120">Obtém informações sobre as regras de autorização associadas a um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="df2b4-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="df2b4-121">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="df2b4-121">Get-AzNotificationHubsNamespaceListKey</span></span>](Get-AzNotificationHubsNamespaceListKey.md)
<span data-ttu-id="df2b4-122">Obtém as cadeias de caracteres de conexão primárias e secundárias associadas a uma regra de autorização de namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="df2b4-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="df2b4-123">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="df2b4-123">New-AzNotificationHub</span></span>](New-AzNotificationHub.md)
<span data-ttu-id="df2b4-124">Cria um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="df2b4-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="df2b4-125">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="df2b4-125">New-AzNotificationHubAuthorizationRule</span></span>](New-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="df2b4-126">Cria uma regra de autorização e atribui a regra a um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="df2b4-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="df2b4-127">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="df2b4-127">New-AzNotificationHubKey</span></span>](New-AzNotificationHubKey.md)
<span data-ttu-id="df2b4-128">Regenerar a Chave de Regra de Autorização para um NotificationHub .</span><span class="sxs-lookup"><span data-stu-id="df2b4-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="df2b4-129">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="df2b4-129">New-AzNotificationHubsNamespace</span></span>](New-AzNotificationHubsNamespace.md)
<span data-ttu-id="df2b4-130">Cria um namespace de hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="df2b4-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="df2b4-131">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="df2b4-131">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](New-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="df2b4-132">Cria uma regra de autorização e atribui essa regra a um namespace de hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="df2b4-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="df2b4-133">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="df2b4-133">New-AzNotificationHubsNamespaceKey</span></span>](New-AzNotificationHubsNamespaceKey.md)
<span data-ttu-id="df2b4-134">Regenerar a Chave de Regra de Autorização para um Namespace.</span><span class="sxs-lookup"><span data-stu-id="df2b4-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="df2b4-135">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="df2b4-135">Remove-AzNotificationHub</span></span>](Remove-AzNotificationHub.md)
<span data-ttu-id="df2b4-136">Remove um hub de notificação existente.</span><span class="sxs-lookup"><span data-stu-id="df2b4-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="df2b4-137">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="df2b4-137">Remove-AzNotificationHubAuthorizationRule</span></span>](Remove-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="df2b4-138">Remove uma regra de autorização de um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="df2b4-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="df2b4-139">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="df2b4-139">Remove-AzNotificationHubsNamespace</span></span>](Remove-AzNotificationHubsNamespace.md)
<span data-ttu-id="df2b4-140">Remove um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="df2b4-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="df2b4-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="df2b4-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Remove-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="df2b4-142">Remove uma regra de autorização de um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="df2b4-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="df2b4-143">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="df2b4-143">Set-AzNotificationHub</span></span>](Set-AzNotificationHub.md)
<span data-ttu-id="df2b4-144">Define valores de propriedade para um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="df2b4-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="df2b4-145">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="df2b4-145">Set-AzNotificationHubAuthorizationRule</span></span>](Set-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="df2b4-146">Define regras de autorização para um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="df2b4-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="df2b4-147">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="df2b4-147">Set-AzNotificationHubsNamespace</span></span>](Set-AzNotificationHubsNamespace.md)
<span data-ttu-id="df2b4-148">Define valores de propriedade para um namespace de hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="df2b4-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="df2b4-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="df2b4-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Set-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="df2b4-150">Define regras de autorização para um namespace de hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="df2b4-150">Sets authorization rules for a notification hub namespace.</span></span>

