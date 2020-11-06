---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
ms.openlocfilehash: b0911045313b26b19fd1de70af926e8c8e066ca8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429205"
---
# <span data-ttu-id="7ae73-101">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7ae73-101">Remove-AzureRmNotificationHub</span></span>

## <span data-ttu-id="7ae73-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ae73-102">SYNOPSIS</span></span>
<span data-ttu-id="7ae73-103">Remove um hub de notificação existente.</span><span class="sxs-lookup"><span data-stu-id="7ae73-103">Removes an existing notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ae73-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ae73-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ae73-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ae73-105">DESCRIPTION</span></span>
<span data-ttu-id="7ae73-106">O cmdlet **Remove-AzureRmNotificationHub** remove um hub de notificação existente.</span><span class="sxs-lookup"><span data-stu-id="7ae73-106">The **Remove-AzureRmNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="7ae73-107">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="7ae73-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="7ae73-108">As plataformas incluem, mas não se limitam a: iOS, Android, Windows Phone 8 e Windows Store.</span><span class="sxs-lookup"><span data-stu-id="7ae73-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="7ae73-109">Os hubs de notificação são aproximadamente equivalentes a aplicativos individuais: cada um dos seus aplicativos normalmente tem seu próprio Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="7ae73-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>

<span data-ttu-id="7ae73-110">Você pode remover um hub de notificação existente usando o cmdlet **Remove-AzureRmNotificationHub** .</span><span class="sxs-lookup"><span data-stu-id="7ae73-110">You can remove an existing notification hub by using the **Remove-AzureRmNotificationHub** cmdlet.</span></span>
<span data-ttu-id="7ae73-111">Depois que um hub for removido, você não poderá mais usar esse Hub para enviar notificações por push para os usuários.</span><span class="sxs-lookup"><span data-stu-id="7ae73-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="7ae73-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ae73-112">EXAMPLES</span></span>

### <span data-ttu-id="7ae73-113">Exemplo 1: remover um hub de notificação</span><span class="sxs-lookup"><span data-stu-id="7ae73-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="7ae73-114">Esse comando Remove o Hub de notificação chamado ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="7ae73-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="7ae73-115">Para remover o Hub, você deve especificar o namespace no qual o Hub está localizado, bem como o grupo de recursos ao qual o Hub está atribuído.</span><span class="sxs-lookup"><span data-stu-id="7ae73-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="7ae73-116">OS</span><span class="sxs-lookup"><span data-stu-id="7ae73-116">PARAMETERS</span></span>

### <span data-ttu-id="7ae73-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7ae73-117">-Force</span></span>
<span data-ttu-id="7ae73-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="7ae73-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7ae73-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7ae73-119">-Namespace</span></span>
<span data-ttu-id="7ae73-120">Especifica o namespace ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="7ae73-120">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="7ae73-121">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="7ae73-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="7ae73-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="7ae73-122">-NotificationHub</span></span>
<span data-ttu-id="7ae73-123">Especifica o Hub de notificação a ser removido.</span><span class="sxs-lookup"><span data-stu-id="7ae73-123">Specifies the notification hub to be removed.</span></span>

<span data-ttu-id="7ae73-124">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="7ae73-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="7ae73-125">-Resource</span><span class="sxs-lookup"><span data-stu-id="7ae73-125">-ResourceGroup</span></span>
<span data-ttu-id="7ae73-126">Especifica o grupo de recursos ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="7ae73-126">Specifies the resource group to which the notification hub is assigned.</span></span>

<span data-ttu-id="7ae73-127">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="7ae73-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="7ae73-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7ae73-128">-Confirm</span></span>
<span data-ttu-id="7ae73-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ae73-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ae73-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ae73-130">-WhatIf</span></span>
<span data-ttu-id="7ae73-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7ae73-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ae73-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7ae73-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ae73-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ae73-133">-DefaultProfile</span></span>
<span data-ttu-id="7ae73-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ae73-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ae73-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ae73-135">CommonParameters</span></span>
<span data-ttu-id="7ae73-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ae73-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ae73-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ae73-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ae73-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ae73-138">INPUTS</span></span>

## <span data-ttu-id="7ae73-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ae73-139">OUTPUTS</span></span>

## <span data-ttu-id="7ae73-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ae73-140">NOTES</span></span>

## <span data-ttu-id="7ae73-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ae73-141">RELATED LINKS</span></span>

[<span data-ttu-id="7ae73-142">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7ae73-142">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="7ae73-143">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7ae73-143">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="7ae73-144">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7ae73-144">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


