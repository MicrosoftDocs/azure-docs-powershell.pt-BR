---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
ms.openlocfilehash: a1e5a8b33ab9df4e48495d00b6a27e105088f4fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885278"
---
# <span data-ttu-id="aa718-101">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="aa718-101">Remove-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="aa718-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa718-102">SYNOPSIS</span></span>
<span data-ttu-id="aa718-103">Remove um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="aa718-103">Removes a notification hub namespace.</span></span>

## <span data-ttu-id="aa718-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="aa718-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa718-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="aa718-105">DESCRIPTION</span></span>
<span data-ttu-id="aa718-106">O cmdlet **Remove-AzNotificationHubsNamespace** remove um namespace de hub de notificação da sua implantação.</span><span class="sxs-lookup"><span data-stu-id="aa718-106">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="aa718-107">Namespaces são contêineres lógicos que ajudam você a organizar e gerenciar seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="aa718-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="aa718-108">O cmdlet **Remove-AzNotificationHubsNamespace** remove um namespace de hub de notificação da sua implantação.</span><span class="sxs-lookup"><span data-stu-id="aa718-108">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="aa718-109">Quando você executar esse cmdlet, o namespace especificado será excluído juntamente com todos os hubs de notificação associados a esse namespace.</span><span class="sxs-lookup"><span data-stu-id="aa718-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="aa718-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa718-110">EXAMPLES</span></span>

### <span data-ttu-id="aa718-111">Exemplo 1: Remover um namespace de hub de notificação</span><span class="sxs-lookup"><span data-stu-id="aa718-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="aa718-112">Este comando remove o namespace chamado ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="aa718-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="aa718-113">Você deve especificar o grupo de recursos ao qual o namespace é atribuído.</span><span class="sxs-lookup"><span data-stu-id="aa718-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="aa718-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="aa718-114">PARAMETERS</span></span>

### <span data-ttu-id="aa718-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa718-115">-DefaultProfile</span></span>
<span data-ttu-id="aa718-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="aa718-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa718-117">-Force</span><span class="sxs-lookup"><span data-stu-id="aa718-117">-Force</span></span>
<span data-ttu-id="aa718-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="aa718-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="aa718-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="aa718-119">-Namespace</span></span>
<span data-ttu-id="aa718-120">Especifica o namespace que esse cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="aa718-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="aa718-121">Os namespaces fornecem uma maneira de agrupar e categorizar hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="aa718-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="aa718-122">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="aa718-122">-ResourceGroup</span></span>
<span data-ttu-id="aa718-123">Especifica o grupo de recursos ao qual o namespace é atribuído.</span><span class="sxs-lookup"><span data-stu-id="aa718-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="aa718-124">Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente o gerenciamento de inventário e a administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="aa718-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="aa718-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa718-125">-Confirm</span></span>
<span data-ttu-id="aa718-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa718-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa718-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa718-127">-WhatIf</span></span>
<span data-ttu-id="aa718-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aa718-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa718-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aa718-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa718-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa718-130">CommonParameters</span></span>
<span data-ttu-id="aa718-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa718-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa718-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa718-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa718-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa718-133">INPUTS</span></span>

### <span data-ttu-id="aa718-134">System.String</span><span class="sxs-lookup"><span data-stu-id="aa718-134">System.String</span></span>

## <span data-ttu-id="aa718-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="aa718-135">OUTPUTS</span></span>

### <span data-ttu-id="aa718-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="aa718-136">System.Void</span></span>

## <span data-ttu-id="aa718-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="aa718-137">NOTES</span></span>

## <span data-ttu-id="aa718-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa718-138">RELATED LINKS</span></span>

[<span data-ttu-id="aa718-139">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="aa718-139">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="aa718-140">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="aa718-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="aa718-141">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="aa718-141">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


