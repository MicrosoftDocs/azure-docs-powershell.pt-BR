---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: 5c5517faa5dbd65cc6a76a02209cb2b8c429300a
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399865"
---
# <span data-ttu-id="91712-101">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="91712-101">Get-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="91712-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91712-102">SYNOPSIS</span></span>
<span data-ttu-id="91712-103">Obtém informações sobre um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="91712-103">Gets information about a notification hub namespace.</span></span>

## <span data-ttu-id="91712-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91712-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91712-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="91712-105">DESCRIPTION</span></span>
<span data-ttu-id="91712-106">**O cmdlet Get-AzNotificationHubsNamespace** obtém informações sobre namespaces do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="91712-106">**The Get-AzNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="91712-107">Este cmdlet fornece a opção de obter informações para todos os seus namespaces, informações sobre os namespaces atribuídos a um grupo de recursos especificado; ou para retornar informações sobre um espaço de nome específico.</span><span class="sxs-lookup"><span data-stu-id="91712-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>
<span data-ttu-id="91712-108">Os namespaces são contêineres lógicos que ajudam você a organizar e gerenciar seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="91712-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="91712-109">Você deve ter pelo menos um namespace do hub de notificação: todos os hubs de notificação devem ser atribuídos a um namespace.</span><span class="sxs-lookup"><span data-stu-id="91712-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="91712-110">Um único namespace pode ter vários hubs, o que significa que talvez você só precise de um namespace em sua organização.</span><span class="sxs-lookup"><span data-stu-id="91712-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="91712-111">No entanto, você também pode ter vários namespaces para organizar melhor seus hubs ou para dar permissão a indivíduos específicos para gerenciar um subconjunto de hubs selecionado.</span><span class="sxs-lookup"><span data-stu-id="91712-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>
<span data-ttu-id="91712-112">O **cmdlet Get-AzNotificationHubsNamespace retorna** informações básicas sobre o próprio namespace.</span><span class="sxs-lookup"><span data-stu-id="91712-112">The **Get-AzNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="91712-113">Para obter informações sobre as regras de autorização associadas a um namespace, use Get-AzNotificationHubsNamespaceAuthorizationRules.</span><span class="sxs-lookup"><span data-stu-id="91712-113">To get information about the authorization rules associated with a namespace use Get-AzNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="91712-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="91712-114">EXAMPLES</span></span>

### <span data-ttu-id="91712-115">Exemplo 1: Obter informações para todos os namespaces do hub de notificação</span><span class="sxs-lookup"><span data-stu-id="91712-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace
```

<span data-ttu-id="91712-116">Esse comando retorna informações para todos os namespaces do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="91712-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="91712-117">Exemplo 2: Obter informações para um único espaço de nome do hub de notificação</span><span class="sxs-lookup"><span data-stu-id="91712-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="91712-118">Este comando obtém informações para um único namespace de hub de notificação: ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="91712-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="91712-119">Exemplo 3: Obter informações para todos os hubs de notificação atribuídos a um espaço de nome específico</span><span class="sxs-lookup"><span data-stu-id="91712-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="91712-120">Esse comando obtém informações para todos os namespaces do hub de notificação atribuídos ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="91712-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="91712-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91712-121">PARAMETERS</span></span>

### <span data-ttu-id="91712-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91712-122">-DefaultProfile</span></span>
<span data-ttu-id="91712-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="91712-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91712-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="91712-124">-Namespace</span></span>
<span data-ttu-id="91712-125">Especifica um nome exclusivo para o namespace.</span><span class="sxs-lookup"><span data-stu-id="91712-125">Specifies a unique name for the namespace.</span></span>
<span data-ttu-id="91712-126">Os namespaces oferecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="91712-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="91712-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="91712-127">-ResourceGroup</span></span>
<span data-ttu-id="91712-128">Especifica o grupo de recursos ao qual o namespace é atribuído.</span><span class="sxs-lookup"><span data-stu-id="91712-128">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="91712-129">Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente o gerenciamento de estoque e a administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="91712-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="91712-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91712-130">CommonParameters</span></span>
<span data-ttu-id="91712-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91712-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91712-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91712-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91712-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="91712-133">INPUTS</span></span>

### <span data-ttu-id="91712-134">System.String</span><span class="sxs-lookup"><span data-stu-id="91712-134">System.String</span></span>

## <span data-ttu-id="91712-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="91712-135">OUTPUTS</span></span>

### <span data-ttu-id="91712-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="91712-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="91712-137">Notas</span><span class="sxs-lookup"><span data-stu-id="91712-137">NOTES</span></span>

## <span data-ttu-id="91712-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91712-138">RELATED LINKS</span></span>


[<span data-ttu-id="91712-139">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="91712-139">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="91712-140">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="91712-140">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="91712-141">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="91712-141">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


