---
Module Name: AzureRM.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/AzureRM.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/AzureRM.NotificationHubs.md
ms.openlocfilehash: e9f6fce095bd7ea4c494cf778587c3853f347c38
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93595302"
---
# <span data-ttu-id="e5635-101">Módulo AzureRM. NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="e5635-101">AzureRM.NotificationHubs Module</span></span>
## <span data-ttu-id="e5635-102">Descritivo</span><span class="sxs-lookup"><span data-stu-id="e5635-102">Description</span></span>
<span data-ttu-id="e5635-103">Este tópico exibe os tópicos da ajuda para os cmdlets do hub de notificação do Azure.</span><span class="sxs-lookup"><span data-stu-id="e5635-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="e5635-104">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma (iOS, Android, Windows Phone 8, Windows Store etc.) usadas por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="e5635-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="e5635-105">Esses hubs são aproximadamente equivalentes a aplicativos individuais: cada um dos seus aplicativos normalmente tem seu próprio Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="e5635-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="e5635-106">Os hubs de notificação são organizados em recipientes lógicos conhecidos como namespaces e as regras de autorização de assinatura de acesso compartilhado (SAS) são usadas para gerenciar o acesso a hubs e namespaces.</span><span class="sxs-lookup"><span data-stu-id="e5635-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="e5635-107">Todos esses elementos podem ser administrados usando cmdlets do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="e5635-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="e5635-108">Cmdlets AzureRM. NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="e5635-108">AzureRM.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="e5635-109">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e5635-109">Get-AzureRmNotificationHub</span></span>](Get-AzureRmNotificationHub.md)
<span data-ttu-id="e5635-110">Obtém informações sobre seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="e5635-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="e5635-111">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="e5635-111">Get-AzureRmNotificationHubAuthorizationRules</span></span>](Get-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="e5635-112">Obtém informações sobre as regras de autorização associadas a um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="e5635-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="e5635-113">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="e5635-113">Get-AzureRmNotificationHubListKeys</span></span>](Get-AzureRmNotificationHubListKeys.md)
<span data-ttu-id="e5635-114">Obtém as cadeias de conexão primária e secundária associadas a uma regra de autorização do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="e5635-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="e5635-115">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="e5635-115">Get-AzureRmNotificationHubPNSCredentials</span></span>](Get-AzureRmNotificationHubPNSCredentials.md)
<span data-ttu-id="e5635-116">Obtém as credenciais do PNS para um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="e5635-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="e5635-117">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e5635-117">Get-AzureRmNotificationHubsNamespace</span></span>](Get-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="e5635-118">Obtém informações sobre um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="e5635-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="e5635-119">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="e5635-119">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="e5635-120">Obtém informações sobre as regras de autorização associadas a um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="e5635-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="e5635-121">Get-AzureRmNotificationHubsNamespaceListKeys</span><span class="sxs-lookup"><span data-stu-id="e5635-121">Get-AzureRmNotificationHubsNamespaceListKeys</span></span>](Get-AzureRmNotificationHubsNamespaceListKeys.md)
<span data-ttu-id="e5635-122">Obtém as cadeias de conexão primária e secundária associadas a uma regra de autorização de namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="e5635-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="e5635-123">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e5635-123">New-AzureRmNotificationHub</span></span>](New-AzureRmNotificationHub.md)
<span data-ttu-id="e5635-124">Cria um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="e5635-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="e5635-125">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="e5635-125">New-AzureRmNotificationHubAuthorizationRules</span></span>](New-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="e5635-126">Cria uma regra de autorização e atribui a regra a um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="e5635-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="e5635-127">New-AzureRmNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="e5635-127">New-AzureRmNotificationHubKey</span></span>](New-AzureRmNotificationHubKey.md)
<span data-ttu-id="e5635-128">Regenerar a chave de regra de autorização para um NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="e5635-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="e5635-129">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e5635-129">New-AzureRmNotificationHubsNamespace</span></span>](New-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="e5635-130">Cria um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="e5635-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="e5635-131">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="e5635-131">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="e5635-132">Cria uma regra de autorização e atribui essa regra a um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="e5635-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="e5635-133">New-AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="e5635-133">New-AzureRmNotificationHubsNamespaceKey</span></span>](New-AzureRmNotificationHubsNamespaceKey.md)
<span data-ttu-id="e5635-134">Regenerar a chave de regra de autorização para um namespace.</span><span class="sxs-lookup"><span data-stu-id="e5635-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="e5635-135">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e5635-135">Remove-AzureRmNotificationHub</span></span>](Remove-AzureRmNotificationHub.md)
<span data-ttu-id="e5635-136">Remove um hub de notificação existente.</span><span class="sxs-lookup"><span data-stu-id="e5635-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="e5635-137">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="e5635-137">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](Remove-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="e5635-138">Remove uma regra de autorização de um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="e5635-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="e5635-139">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e5635-139">Remove-AzureRmNotificationHubsNamespace</span></span>](Remove-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="e5635-140">Remove um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="e5635-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="e5635-141">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="e5635-141">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="e5635-142">Remove uma regra de autorização de um namespace Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="e5635-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="e5635-143">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e5635-143">Set-AzureRmNotificationHub</span></span>](Set-AzureRmNotificationHub.md)
<span data-ttu-id="e5635-144">Define valores de propriedade para um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="e5635-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="e5635-145">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="e5635-145">Set-AzureRmNotificationHubAuthorizationRules</span></span>](Set-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="e5635-146">Define regras de autorização para um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="e5635-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="e5635-147">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e5635-147">Set-AzureRmNotificationHubsNamespace</span></span>](Set-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="e5635-148">Define valores de propriedade para um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="e5635-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="e5635-149">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="e5635-149">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="e5635-150">Define regras de autorização para um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="e5635-150">Sets authorization rules for a notification hub namespace.</span></span>

