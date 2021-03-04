---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: 5a8d38adf8016d8f0a71877aa1717df9f3389c93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885299"
---
# <span data-ttu-id="1ead9-101">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1ead9-101">Get-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="1ead9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ead9-102">SYNOPSIS</span></span>
<span data-ttu-id="1ead9-103">Obtém informações sobre um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="1ead9-103">Gets information about a notification hub namespace.</span></span>

## <span data-ttu-id="1ead9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1ead9-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ead9-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1ead9-105">DESCRIPTION</span></span>
<span data-ttu-id="1ead9-106">O cmdlet **Get-AzNotificationHubsNamespace** obtém informações sobre namespaces de hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="1ead9-106">**The Get-AzNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="1ead9-107">Este cmdlet fornece a opção de obter informações para todos os namespaces, informações sobre os namespaces atribuídos a um grupo de recursos especificado; ou para retornar informações sobre um namespace específico.</span><span class="sxs-lookup"><span data-stu-id="1ead9-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>
<span data-ttu-id="1ead9-108">Namespaces são contêineres lógicos que ajudam você a organizar e gerenciar seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="1ead9-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="1ead9-109">Você deve ter pelo menos um namespace de hub de notificação: todos os hubs de notificação devem ser atribuídos a um namespace.</span><span class="sxs-lookup"><span data-stu-id="1ead9-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="1ead9-110">Um único namespace pode abrigar vários hubs, o que significa que você pode precisar apenas de um namespace em sua organização.</span><span class="sxs-lookup"><span data-stu-id="1ead9-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="1ead9-111">No entanto, você também pode ter vários namespaces para organizar melhor seus hubs ou para dar a indivíduos específicos permissão para gerenciar um subconjunto selecionado de hubs.</span><span class="sxs-lookup"><span data-stu-id="1ead9-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>
<span data-ttu-id="1ead9-112">O cmdlet **Get-AzNotificationHubsNamespace** retorna informações básicas sobre o namespace em si.</span><span class="sxs-lookup"><span data-stu-id="1ead9-112">The **Get-AzNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="1ead9-113">Para obter informações sobre as regras de autorização associadas a um namespace, use Get-AzNotificationHubsNamespaceAuthorizationRules.</span><span class="sxs-lookup"><span data-stu-id="1ead9-113">To get information about the authorization rules associated with a namespace use Get-AzNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="1ead9-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ead9-114">EXAMPLES</span></span>

### <span data-ttu-id="1ead9-115">Exemplo 1: obter informações para todos os namespaces do hub de notificação</span><span class="sxs-lookup"><span data-stu-id="1ead9-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace
```

<span data-ttu-id="1ead9-116">Este comando retorna informações para todos os namespaces do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="1ead9-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="1ead9-117">Exemplo 2: obter informações para um único namespace de hub de notificação</span><span class="sxs-lookup"><span data-stu-id="1ead9-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="1ead9-118">Este comando obtém informações para um único namespace de hub de notificação: ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="1ead9-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="1ead9-119">Exemplo 3: obter informações para todos os hubs de notificação atribuídos a um namespace específico</span><span class="sxs-lookup"><span data-stu-id="1ead9-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="1ead9-120">Este comando obtém informações para todos os namespaces de hub de notificação atribuídos ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="1ead9-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="1ead9-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1ead9-121">PARAMETERS</span></span>

### <span data-ttu-id="1ead9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ead9-122">-DefaultProfile</span></span>
<span data-ttu-id="1ead9-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1ead9-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ead9-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1ead9-124">-Namespace</span></span>
<span data-ttu-id="1ead9-125">Especifica um nome exclusivo para o namespace.</span><span class="sxs-lookup"><span data-stu-id="1ead9-125">Specifies a unique name for the namespace.</span></span>
<span data-ttu-id="1ead9-126">Os namespaces fornecem uma maneira de agrupar e categorizar hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="1ead9-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ead9-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1ead9-127">-ResourceGroup</span></span>
<span data-ttu-id="1ead9-128">Especifica o grupo de recursos ao qual o namespace é atribuído.</span><span class="sxs-lookup"><span data-stu-id="1ead9-128">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="1ead9-129">Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente o gerenciamento de inventário e a administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="1ead9-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ead9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ead9-130">CommonParameters</span></span>
<span data-ttu-id="1ead9-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ead9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ead9-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ead9-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ead9-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ead9-133">INPUTS</span></span>

### <span data-ttu-id="1ead9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1ead9-134">System.String</span></span>

## <span data-ttu-id="1ead9-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1ead9-135">OUTPUTS</span></span>

### <span data-ttu-id="1ead9-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="1ead9-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="1ead9-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="1ead9-137">NOTES</span></span>

## <span data-ttu-id="1ead9-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ead9-138">RELATED LINKS</span></span>

[<span data-ttu-id="1ead9-139">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1ead9-139">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="1ead9-140">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1ead9-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="1ead9-141">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1ead9-141">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="1ead9-142">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1ead9-142">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


