---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
ms.openlocfilehash: f4dc14fd922852fa67085588c78847623eb5eb64
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430114"
---
# <span data-ttu-id="b2c08-101">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="b2c08-101">Remove-AzureRmNotificationHub</span></span>

## <span data-ttu-id="b2c08-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2c08-102">SYNOPSIS</span></span>
<span data-ttu-id="b2c08-103">Remove um hub de notificação existente.</span><span class="sxs-lookup"><span data-stu-id="b2c08-103">Removes an existing notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2c08-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2c08-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2c08-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b2c08-105">DESCRIPTION</span></span>
<span data-ttu-id="b2c08-106">O cmdlet **Remove-AzureRmNotificationHub** remove um hub de notificação existente.</span><span class="sxs-lookup"><span data-stu-id="b2c08-106">The **Remove-AzureRmNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="b2c08-107">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="b2c08-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="b2c08-108">As plataformas incluem, mas não se limitam a: iOS, Android, Windows Phone 8 e Windows Store.</span><span class="sxs-lookup"><span data-stu-id="b2c08-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="b2c08-109">Os hubs de notificação são aproximadamente equivalentes a aplicativos individuais: cada um dos seus aplicativos normalmente tem seu próprio Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="b2c08-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="b2c08-110">Você pode remover um hub de notificação existente usando o cmdlet **Remove-AzureRmNotificationHub** .</span><span class="sxs-lookup"><span data-stu-id="b2c08-110">You can remove an existing notification hub by using the **Remove-AzureRmNotificationHub** cmdlet.</span></span>
<span data-ttu-id="b2c08-111">Depois que um hub for removido, você não poderá mais usar esse Hub para enviar notificações por push para os usuários.</span><span class="sxs-lookup"><span data-stu-id="b2c08-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="b2c08-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2c08-112">EXAMPLES</span></span>

### <span data-ttu-id="b2c08-113">Exemplo 1: remover um hub de notificação</span><span class="sxs-lookup"><span data-stu-id="b2c08-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="b2c08-114">Esse comando Remove o Hub de notificação chamado ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="b2c08-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="b2c08-115">Para remover o Hub, você deve especificar o namespace no qual o Hub está localizado, bem como o grupo de recursos ao qual o Hub está atribuído.</span><span class="sxs-lookup"><span data-stu-id="b2c08-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="b2c08-116">OS</span><span class="sxs-lookup"><span data-stu-id="b2c08-116">PARAMETERS</span></span>

### <span data-ttu-id="b2c08-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2c08-117">-DefaultProfile</span></span>
<span data-ttu-id="b2c08-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b2c08-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2c08-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b2c08-119">-Force</span></span>
<span data-ttu-id="b2c08-120">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="b2c08-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b2c08-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b2c08-121">-Namespace</span></span>
<span data-ttu-id="b2c08-122">Especifica o namespace ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="b2c08-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="b2c08-123">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="b2c08-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="b2c08-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="b2c08-124">-NotificationHub</span></span>
<span data-ttu-id="b2c08-125">Especifica o Hub de notificação a ser removido.</span><span class="sxs-lookup"><span data-stu-id="b2c08-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="b2c08-126">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="b2c08-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="b2c08-127">-Resource</span><span class="sxs-lookup"><span data-stu-id="b2c08-127">-ResourceGroup</span></span>
<span data-ttu-id="b2c08-128">Especifica o grupo de recursos ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="b2c08-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="b2c08-129">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="b2c08-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="b2c08-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b2c08-130">-Confirm</span></span>
<span data-ttu-id="b2c08-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2c08-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2c08-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2c08-132">-WhatIf</span></span>
<span data-ttu-id="b2c08-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b2c08-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2c08-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b2c08-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2c08-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2c08-135">CommonParameters</span></span>
<span data-ttu-id="b2c08-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2c08-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2c08-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2c08-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2c08-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b2c08-138">INPUTS</span></span>

### <span data-ttu-id="b2c08-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b2c08-139">System.String</span></span>

## <span data-ttu-id="b2c08-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b2c08-140">OUTPUTS</span></span>

### <span data-ttu-id="b2c08-141">System. void</span><span class="sxs-lookup"><span data-stu-id="b2c08-141">System.Void</span></span>

## <span data-ttu-id="b2c08-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b2c08-142">NOTES</span></span>

## <span data-ttu-id="b2c08-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2c08-143">RELATED LINKS</span></span>

[<span data-ttu-id="b2c08-144">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="b2c08-144">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="b2c08-145">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="b2c08-145">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="b2c08-146">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="b2c08-146">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


