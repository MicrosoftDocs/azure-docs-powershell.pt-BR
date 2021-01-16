---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
ms.openlocfilehash: e03be5a1daae753e1538b171586d9a8e46ad8021
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272591"
---
# <span data-ttu-id="87693-101">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="87693-101">Remove-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="87693-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87693-102">SYNOPSIS</span></span>
<span data-ttu-id="87693-103">Remove um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="87693-103">Removes a notification hub namespace.</span></span>

## <span data-ttu-id="87693-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87693-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87693-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="87693-105">DESCRIPTION</span></span>
<span data-ttu-id="87693-106">O cmdlet **Remove-AzNotificationHubsNamespace** remove um namespace de Hub de notificação da sua implantação.</span><span class="sxs-lookup"><span data-stu-id="87693-106">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="87693-107">Namespaces são recipientes lógicos que ajudam você a organizar e gerenciar seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="87693-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="87693-108">O cmdlet **Remove-AzNotificationHubsNamespace** remove um namespace de Hub de notificação da sua implantação.</span><span class="sxs-lookup"><span data-stu-id="87693-108">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="87693-109">Quando você executar esse cmdlet, o namespace especificado será excluído juntamente com todos os hubs de notificação associados a esse namespace.</span><span class="sxs-lookup"><span data-stu-id="87693-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="87693-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87693-110">EXAMPLES</span></span>

### <span data-ttu-id="87693-111">Exemplo 1: remover um namespace do hub de notificação</span><span class="sxs-lookup"><span data-stu-id="87693-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="87693-112">Esse comando Remove o namespace chamado ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="87693-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="87693-113">Você deve especificar o grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="87693-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="87693-114">OS</span><span class="sxs-lookup"><span data-stu-id="87693-114">PARAMETERS</span></span>

### <span data-ttu-id="87693-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87693-115">-DefaultProfile</span></span>
<span data-ttu-id="87693-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="87693-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87693-117">-Force</span><span class="sxs-lookup"><span data-stu-id="87693-117">-Force</span></span>
<span data-ttu-id="87693-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="87693-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="87693-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="87693-119">-Namespace</span></span>
<span data-ttu-id="87693-120">Especifica o namespace que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="87693-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="87693-121">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="87693-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="87693-122">-Resource</span><span class="sxs-lookup"><span data-stu-id="87693-122">-ResourceGroup</span></span>
<span data-ttu-id="87693-123">Especifica o grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="87693-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="87693-124">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="87693-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="87693-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="87693-125">-Confirm</span></span>
<span data-ttu-id="87693-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87693-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87693-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87693-127">-WhatIf</span></span>
<span data-ttu-id="87693-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="87693-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87693-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="87693-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87693-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87693-130">CommonParameters</span></span>
<span data-ttu-id="87693-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87693-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87693-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87693-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87693-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="87693-133">INPUTS</span></span>

### <span data-ttu-id="87693-134">System. String</span><span class="sxs-lookup"><span data-stu-id="87693-134">System.String</span></span>

## <span data-ttu-id="87693-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="87693-135">OUTPUTS</span></span>

### <span data-ttu-id="87693-136">System. void</span><span class="sxs-lookup"><span data-stu-id="87693-136">System.Void</span></span>

## <span data-ttu-id="87693-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="87693-137">NOTES</span></span>

## <span data-ttu-id="87693-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87693-138">RELATED LINKS</span></span>

[<span data-ttu-id="87693-139">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="87693-139">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="87693-140">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="87693-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="87693-141">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="87693-141">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


