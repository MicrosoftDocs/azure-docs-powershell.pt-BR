---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: dce2736329fe4cfac6406a6646de7388869d20e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885301"
---
# <span data-ttu-id="c0f71-101">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="c0f71-101">Get-AzNotificationHubListKey</span></span>

## <span data-ttu-id="c0f71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0f71-102">SYNOPSIS</span></span>
<span data-ttu-id="c0f71-103">Obtém as cadeias de conexão primárias e secundárias associadas a uma regra de autorização do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="c0f71-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

## <span data-ttu-id="c0f71-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c0f71-104">SYNTAX</span></span>

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0f71-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c0f71-105">DESCRIPTION</span></span>
<span data-ttu-id="c0f71-106">O cmdlet **Get-AzNotificationHubListKey** retorna as cadeias de conexão primárias e secundárias de uma regra de autorização SAS (Assinatura de Acesso Compartilhado) do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="c0f71-106">The **Get-AzNotificationHubListKey** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="c0f71-107">As regras de autorização gerenciam os direitos do usuário para o hub.</span><span class="sxs-lookup"><span data-stu-id="c0f71-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="c0f71-108">Cada regra inclui uma cadeia de caracteres de conexão primária e secundária.</span><span class="sxs-lookup"><span data-stu-id="c0f71-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="c0f71-109">Essas cadeias de caracteres de conexão (URIs) executam o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c0f71-109">These connection strings (URIs) perform the following:</span></span>
- <span data-ttu-id="c0f71-110">Aponte os usuários para um recurso.</span><span class="sxs-lookup"><span data-stu-id="c0f71-110">Point users to a resource.</span></span>
- <span data-ttu-id="c0f71-111">Inclua um token contendo parâmetros de consulta.</span><span class="sxs-lookup"><span data-stu-id="c0f71-111">Include a token containing query parameters.</span></span>
<span data-ttu-id="c0f71-112">Um desses parâmetros, a assinatura, é usado para autenticar o usuário e fornecer o nível de acesso especificado.</span><span class="sxs-lookup"><span data-stu-id="c0f71-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="c0f71-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0f71-113">EXAMPLES</span></span>

### <span data-ttu-id="c0f71-114">Exemplo 1: Obter as cadeias de caracteres de conexão primárias e secundárias para uma regra de autorização</span><span class="sxs-lookup"><span data-stu-id="c0f71-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="c0f71-115">Este comando obtém as cadeias de conexão primárias e secundárias para a regra de autorização ListenRule, uma regra atribuída ao hub de notificação ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="c0f71-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="c0f71-116">O comando deve incluir o namespace do hub e o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c0f71-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="c0f71-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c0f71-117">PARAMETERS</span></span>

### <span data-ttu-id="c0f71-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c0f71-118">-AuthorizationRule</span></span>
<span data-ttu-id="c0f71-119">Especifica o nome de uma regra de autenticação SAS (Assinatura de Acesso Compartilhado).</span><span class="sxs-lookup"><span data-stu-id="c0f71-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="c0f71-120">Essas regras determinam o tipo de acesso que os usuários têm ao hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="c0f71-120">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0f71-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0f71-121">-DefaultProfile</span></span>
<span data-ttu-id="c0f71-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c0f71-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0f71-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c0f71-123">-Namespace</span></span>
<span data-ttu-id="c0f71-124">Especifica o namespace ao qual o hub de notificação é atribuído.</span><span class="sxs-lookup"><span data-stu-id="c0f71-124">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="c0f71-125">Os namespaces fornecem uma maneira de agrupar e categorizar hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="c0f71-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="c0f71-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="c0f71-126">-NotificationHub</span></span>
<span data-ttu-id="c0f71-127">Especifica o hub de notificação ao que este cmdlet atribui uma regra de autorização.</span><span class="sxs-lookup"><span data-stu-id="c0f71-127">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="c0f71-128">Os hubs de notificação são usados para enviar notificações por push a vários clientes, independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="c0f71-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="c0f71-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c0f71-129">-ResourceGroup</span></span>
<span data-ttu-id="c0f71-130">Especifica o grupo de recursos ao qual o hub de notificação é atribuído.</span><span class="sxs-lookup"><span data-stu-id="c0f71-130">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="c0f71-131">Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente o gerenciamento de inventário e a administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="c0f71-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="c0f71-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0f71-132">CommonParameters</span></span>
<span data-ttu-id="c0f71-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0f71-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0f71-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0f71-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0f71-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0f71-135">INPUTS</span></span>

### <span data-ttu-id="c0f71-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c0f71-136">System.String</span></span>

## <span data-ttu-id="c0f71-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c0f71-137">OUTPUTS</span></span>

### <span data-ttu-id="c0f71-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="c0f71-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="c0f71-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="c0f71-139">NOTES</span></span>

## <span data-ttu-id="c0f71-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0f71-140">RELATED LINKS</span></span>

[<span data-ttu-id="c0f71-141">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c0f71-141">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)


