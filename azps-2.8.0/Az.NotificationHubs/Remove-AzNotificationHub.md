---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
ms.openlocfilehash: c3740884d49683b7990aea1ed7543f39a4ccf80f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772924"
---
# <span data-ttu-id="80c86-101">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="80c86-101">Remove-AzNotificationHub</span></span>

## <span data-ttu-id="80c86-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="80c86-102">SYNOPSIS</span></span>
<span data-ttu-id="80c86-103">Remove um hub de notificação existente.</span><span class="sxs-lookup"><span data-stu-id="80c86-103">Removes an existing notification hub.</span></span>

## <span data-ttu-id="80c86-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80c86-104">SYNTAX</span></span>

```
Remove-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80c86-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="80c86-105">DESCRIPTION</span></span>
<span data-ttu-id="80c86-106">O cmdlet **Remove-AzNotificationHub** remove um hub de notificação existente.</span><span class="sxs-lookup"><span data-stu-id="80c86-106">The **Remove-AzNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="80c86-107">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="80c86-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="80c86-108">As plataformas incluem, mas não se limitam a: iOS, Android, Windows Phone 8 e Windows Store.</span><span class="sxs-lookup"><span data-stu-id="80c86-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="80c86-109">Os hubs de notificação são aproximadamente equivalentes a aplicativos individuais: cada um dos seus aplicativos normalmente tem seu próprio Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="80c86-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="80c86-110">Você pode remover um hub de notificação existente usando o cmdlet **Remove-AzNotificationHub** .</span><span class="sxs-lookup"><span data-stu-id="80c86-110">You can remove an existing notification hub by using the **Remove-AzNotificationHub** cmdlet.</span></span>
<span data-ttu-id="80c86-111">Depois que um hub for removido, você não poderá mais usar esse Hub para enviar notificações por push para os usuários.</span><span class="sxs-lookup"><span data-stu-id="80c86-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="80c86-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80c86-112">EXAMPLES</span></span>

### <span data-ttu-id="80c86-113">Exemplo 1: remover um hub de notificação</span><span class="sxs-lookup"><span data-stu-id="80c86-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="80c86-114">Esse comando Remove o Hub de notificação chamado ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="80c86-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="80c86-115">Para remover o Hub, você deve especificar o namespace no qual o Hub está localizado, bem como o grupo de recursos ao qual o Hub está atribuído.</span><span class="sxs-lookup"><span data-stu-id="80c86-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="80c86-116">OS</span><span class="sxs-lookup"><span data-stu-id="80c86-116">PARAMETERS</span></span>

### <span data-ttu-id="80c86-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80c86-117">-DefaultProfile</span></span>
<span data-ttu-id="80c86-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="80c86-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80c86-119">-Force</span><span class="sxs-lookup"><span data-stu-id="80c86-119">-Force</span></span>
<span data-ttu-id="80c86-120">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="80c86-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="80c86-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="80c86-121">-Namespace</span></span>
<span data-ttu-id="80c86-122">Especifica o namespace ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="80c86-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="80c86-123">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="80c86-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="80c86-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="80c86-124">-NotificationHub</span></span>
<span data-ttu-id="80c86-125">Especifica o Hub de notificação a ser removido.</span><span class="sxs-lookup"><span data-stu-id="80c86-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="80c86-126">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="80c86-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="80c86-127">-Resource</span><span class="sxs-lookup"><span data-stu-id="80c86-127">-ResourceGroup</span></span>
<span data-ttu-id="80c86-128">Especifica o grupo de recursos ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="80c86-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="80c86-129">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="80c86-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="80c86-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="80c86-130">-Confirm</span></span>
<span data-ttu-id="80c86-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80c86-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80c86-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80c86-132">-WhatIf</span></span>
<span data-ttu-id="80c86-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="80c86-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80c86-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="80c86-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80c86-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80c86-135">CommonParameters</span></span>
<span data-ttu-id="80c86-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80c86-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80c86-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80c86-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80c86-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="80c86-138">INPUTS</span></span>

### <span data-ttu-id="80c86-139">System. String</span><span class="sxs-lookup"><span data-stu-id="80c86-139">System.String</span></span>

## <span data-ttu-id="80c86-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="80c86-140">OUTPUTS</span></span>

### <span data-ttu-id="80c86-141">System. void</span><span class="sxs-lookup"><span data-stu-id="80c86-141">System.Void</span></span>

## <span data-ttu-id="80c86-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="80c86-142">NOTES</span></span>

## <span data-ttu-id="80c86-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80c86-143">RELATED LINKS</span></span>

[<span data-ttu-id="80c86-144">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="80c86-144">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="80c86-145">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="80c86-145">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="80c86-146">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="80c86-146">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)

