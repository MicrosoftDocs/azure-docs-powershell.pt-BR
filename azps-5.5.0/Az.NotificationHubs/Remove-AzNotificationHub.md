---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
ms.openlocfilehash: 66f3dae7d92b9db18db418bf9de62671f084b7c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111541"
---
# <span data-ttu-id="fc5aa-101">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="fc5aa-101">Remove-AzNotificationHub</span></span>

## <span data-ttu-id="fc5aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc5aa-102">SYNOPSIS</span></span>
<span data-ttu-id="fc5aa-103">Remove um hub de notificação existente.</span><span class="sxs-lookup"><span data-stu-id="fc5aa-103">Removes an existing notification hub.</span></span>

## <span data-ttu-id="fc5aa-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc5aa-104">SYNTAX</span></span>

```
Remove-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc5aa-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc5aa-105">DESCRIPTION</span></span>
<span data-ttu-id="fc5aa-106">O cmdlet **Remove-AzNotificationHub** remove um hub de notificação existente.</span><span class="sxs-lookup"><span data-stu-id="fc5aa-106">The **Remove-AzNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="fc5aa-107">Os hubs de notificação são usados para enviar notificações por push para vários clientes independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="fc5aa-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="fc5aa-108">As plataformas incluem, mas não estão limitadas a: iOS, Android, Windows Phone 8 e Windows Store.</span><span class="sxs-lookup"><span data-stu-id="fc5aa-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="fc5aa-109">Os hubs de notificação são aproximadamente equivalentes a aplicativos individuais: cada um dos seus aplicativos normalmente terá seu próprio hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="fc5aa-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="fc5aa-110">Você pode remover um hub de notificação existente usando o cmdlet **Remove-AzNotificationHub.**</span><span class="sxs-lookup"><span data-stu-id="fc5aa-110">You can remove an existing notification hub by using the **Remove-AzNotificationHub** cmdlet.</span></span>
<span data-ttu-id="fc5aa-111">Depois que um hub for removido, você não poderá mais usar esse hub para enviar notificações por push para os usuários.</span><span class="sxs-lookup"><span data-stu-id="fc5aa-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="fc5aa-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fc5aa-112">EXAMPLES</span></span>

### <span data-ttu-id="fc5aa-113">Exemplo 1: Remover um hub de notificação</span><span class="sxs-lookup"><span data-stu-id="fc5aa-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="fc5aa-114">Esse comando remove o hub de notificação chamado ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="fc5aa-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="fc5aa-115">Para remover o hub, você deve especificar o namespace onde o hub está localizado, bem como o grupo de recursos ao qual o hub está atribuído.</span><span class="sxs-lookup"><span data-stu-id="fc5aa-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="fc5aa-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc5aa-116">PARAMETERS</span></span>

### <span data-ttu-id="fc5aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc5aa-117">-DefaultProfile</span></span>
<span data-ttu-id="fc5aa-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="fc5aa-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc5aa-119">-Forçar</span><span class="sxs-lookup"><span data-stu-id="fc5aa-119">-Force</span></span>
<span data-ttu-id="fc5aa-120">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="fc5aa-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fc5aa-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fc5aa-121">-Namespace</span></span>
<span data-ttu-id="fc5aa-122">Especifica o namespace ao qual o hub de notificação está atribuído.</span><span class="sxs-lookup"><span data-stu-id="fc5aa-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="fc5aa-123">Os namespaces oferecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="fc5aa-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="fc5aa-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="fc5aa-124">-NotificationHub</span></span>
<span data-ttu-id="fc5aa-125">Especifica o hub de notificação a ser removido.</span><span class="sxs-lookup"><span data-stu-id="fc5aa-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="fc5aa-126">Os hubs de notificação são usados para enviar notificações por push para vários clientes independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="fc5aa-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="fc5aa-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fc5aa-127">-ResourceGroup</span></span>
<span data-ttu-id="fc5aa-128">Especifica o grupo de recursos ao qual o hub de notificação está atribuído.</span><span class="sxs-lookup"><span data-stu-id="fc5aa-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="fc5aa-129">Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente o gerenciamento de estoque e a administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc5aa-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="fc5aa-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fc5aa-130">-Confirm</span></span>
<span data-ttu-id="fc5aa-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc5aa-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc5aa-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc5aa-132">-WhatIf</span></span>
<span data-ttu-id="fc5aa-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fc5aa-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc5aa-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fc5aa-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc5aa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc5aa-135">CommonParameters</span></span>
<span data-ttu-id="fc5aa-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc5aa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc5aa-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc5aa-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc5aa-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="fc5aa-138">INPUTS</span></span>

### <span data-ttu-id="fc5aa-139">System.String</span><span class="sxs-lookup"><span data-stu-id="fc5aa-139">System.String</span></span>

## <span data-ttu-id="fc5aa-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="fc5aa-140">OUTPUTS</span></span>

### <span data-ttu-id="fc5aa-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="fc5aa-141">System.Void</span></span>

## <span data-ttu-id="fc5aa-142">Notas</span><span class="sxs-lookup"><span data-stu-id="fc5aa-142">NOTES</span></span>

## <span data-ttu-id="fc5aa-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc5aa-143">RELATED LINKS</span></span>

[<span data-ttu-id="fc5aa-144">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="fc5aa-144">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="fc5aa-145">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="fc5aa-145">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="fc5aa-146">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="fc5aa-146">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


