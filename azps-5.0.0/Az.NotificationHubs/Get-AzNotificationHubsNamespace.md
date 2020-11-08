---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: 3d0e604d3984a40acde02fb1f977e2922ae2d1d7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116054"
---
# <span data-ttu-id="403d4-101">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="403d4-101">Get-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="403d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="403d4-102">SYNOPSIS</span></span>
<span data-ttu-id="403d4-103">Obtém informações sobre um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="403d4-103">Gets information about a notification hub namespace.</span></span>

## <span data-ttu-id="403d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="403d4-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="403d4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="403d4-105">DESCRIPTION</span></span>
<span data-ttu-id="403d4-106">**O cmdlet Get-AzNotificationHubsNamespace** Obtém informações sobre namespaces do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="403d4-106">**The Get-AzNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="403d4-107">Esse cmdlet oferece a opção de obter informações para todos os namespaces, informações sobre os namespaces atribuídos a um grupo de recursos especificado; ou para retornar informações sobre um namespace específico.</span><span class="sxs-lookup"><span data-stu-id="403d4-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>
<span data-ttu-id="403d4-108">Namespaces são recipientes lógicos que ajudam você a organizar e gerenciar seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="403d4-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="403d4-109">Você deve ter pelo menos um namespace de Hub de notificação: todos os hubs de notificação devem ser atribuídos a um namespace.</span><span class="sxs-lookup"><span data-stu-id="403d4-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="403d4-110">Um único namespace pode alojar vários hubs, o que significa que você pode só precisar de um namespace em sua organização.</span><span class="sxs-lookup"><span data-stu-id="403d4-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="403d4-111">No entanto, você também pode ter vários namespaces para organizar melhor seus hubs, ou para dar a pessoas específicas permissão para gerenciar um subconjunto de hubs selecionado.</span><span class="sxs-lookup"><span data-stu-id="403d4-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>
<span data-ttu-id="403d4-112">O cmdlet **Get-AzNotificationHubsNamespace** retorna informações básicas sobre o próprio namespace.</span><span class="sxs-lookup"><span data-stu-id="403d4-112">The **Get-AzNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="403d4-113">Para obter informações sobre as regras de autorização associadas a um namespace, use Get-AzNotificationHubsNamespaceAuthorizationRules.</span><span class="sxs-lookup"><span data-stu-id="403d4-113">To get information about the authorization rules associated with a namespace use Get-AzNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="403d4-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="403d4-114">EXAMPLES</span></span>

### <span data-ttu-id="403d4-115">Exemplo 1: obter informações para todos os namespaces do hub de notificação</span><span class="sxs-lookup"><span data-stu-id="403d4-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace
```

<span data-ttu-id="403d4-116">Esse comando retorna informações para todos os namespaces do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="403d4-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="403d4-117">Exemplo 2: obter informações para um único namespace Hub de notificação</span><span class="sxs-lookup"><span data-stu-id="403d4-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="403d4-118">Esse comando obtém informações para um único namespace Hub de notificação: ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="403d4-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="403d4-119">Exemplo 3: obter informações para todos os hubs de notificação atribuídos a um namespace específico</span><span class="sxs-lookup"><span data-stu-id="403d4-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="403d4-120">Esse comando obtém informações para todos os namespaces do hub de notificação atribuídos à ContosoNotificationsGroup do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="403d4-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="403d4-121">OS</span><span class="sxs-lookup"><span data-stu-id="403d4-121">PARAMETERS</span></span>

### <span data-ttu-id="403d4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="403d4-122">-DefaultProfile</span></span>
<span data-ttu-id="403d4-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="403d4-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="403d4-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="403d4-124">-Namespace</span></span>
<span data-ttu-id="403d4-125">Especifica um nome exclusivo para o namespace.</span><span class="sxs-lookup"><span data-stu-id="403d4-125">Specifies a unique name for the namespace.</span></span>
<span data-ttu-id="403d4-126">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="403d4-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="403d4-127">-Resource</span><span class="sxs-lookup"><span data-stu-id="403d4-127">-ResourceGroup</span></span>
<span data-ttu-id="403d4-128">Especifica o grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="403d4-128">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="403d4-129">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="403d4-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="403d4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="403d4-130">CommonParameters</span></span>
<span data-ttu-id="403d4-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="403d4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="403d4-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="403d4-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="403d4-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="403d4-133">INPUTS</span></span>

### <span data-ttu-id="403d4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="403d4-134">System.String</span></span>

## <span data-ttu-id="403d4-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="403d4-135">OUTPUTS</span></span>

### <span data-ttu-id="403d4-136">Microsoft. Azure. Commands. NotificationHubs. Models. Namespaceattributes</span><span class="sxs-lookup"><span data-stu-id="403d4-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="403d4-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="403d4-137">NOTES</span></span>

## <span data-ttu-id="403d4-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="403d4-138">RELATED LINKS</span></span>

[<span data-ttu-id="403d4-139">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="403d4-139">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="403d4-140">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="403d4-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="403d4-141">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="403d4-141">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="403d4-142">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="403d4-142">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


