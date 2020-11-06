---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: ff315c7f3634c0a8a4afd5c4b54926c0a260ed75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429200"
---
# <span data-ttu-id="5ded6-101">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="5ded6-101">Remove-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="5ded6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5ded6-102">SYNOPSIS</span></span>
<span data-ttu-id="5ded6-103">Remove um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="5ded6-103">Removes a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ded6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ded6-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ded6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5ded6-105">DESCRIPTION</span></span>
<span data-ttu-id="5ded6-106">O cmdlet **Remove-AzureRmNotificationHubsNamespace** remove um namespace de Hub de notificação da sua implantação.</span><span class="sxs-lookup"><span data-stu-id="5ded6-106">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>

<span data-ttu-id="5ded6-107">Namespaces são recipientes lógicos que ajudam você a organizar e gerenciar seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="5ded6-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="5ded6-108">O cmdlet **Remove-AzureRmNotificationHubsNamespace** remove um namespace de Hub de notificação da sua implantação.</span><span class="sxs-lookup"><span data-stu-id="5ded6-108">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="5ded6-109">Quando você executar esse cmdlet, o namespace especificado será excluído juntamente com todos os hubs de notificação associados a esse namespace.</span><span class="sxs-lookup"><span data-stu-id="5ded6-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="5ded6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5ded6-110">EXAMPLES</span></span>

### <span data-ttu-id="5ded6-111">Exemplo 1: remover um namespace do hub de notificação</span><span class="sxs-lookup"><span data-stu-id="5ded6-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="5ded6-112">Esse comando Remove o namespace chamado ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="5ded6-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="5ded6-113">Você deve especificar o grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="5ded6-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="5ded6-114">OS</span><span class="sxs-lookup"><span data-stu-id="5ded6-114">PARAMETERS</span></span>

### <span data-ttu-id="5ded6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5ded6-115">-Force</span></span>
<span data-ttu-id="5ded6-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="5ded6-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5ded6-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5ded6-117">-Namespace</span></span>
<span data-ttu-id="5ded6-118">Especifica o namespace que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="5ded6-118">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="5ded6-119">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="5ded6-119">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="5ded6-120">-Resource</span><span class="sxs-lookup"><span data-stu-id="5ded6-120">-ResourceGroup</span></span>
<span data-ttu-id="5ded6-121">Especifica o grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="5ded6-121">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="5ded6-122">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="5ded6-122">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="5ded6-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5ded6-123">-Confirm</span></span>
<span data-ttu-id="5ded6-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ded6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ded6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ded6-125">-WhatIf</span></span>
<span data-ttu-id="5ded6-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5ded6-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ded6-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5ded6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ded6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ded6-128">-DefaultProfile</span></span>
<span data-ttu-id="5ded6-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5ded6-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ded6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ded6-130">CommonParameters</span></span>
<span data-ttu-id="5ded6-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ded6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ded6-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ded6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ded6-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5ded6-133">INPUTS</span></span>

## <span data-ttu-id="5ded6-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5ded6-134">OUTPUTS</span></span>

## <span data-ttu-id="5ded6-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5ded6-135">NOTES</span></span>

## <span data-ttu-id="5ded6-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ded6-136">RELATED LINKS</span></span>

[<span data-ttu-id="5ded6-137">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="5ded6-137">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="5ded6-138">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="5ded6-138">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="5ded6-139">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="5ded6-139">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


