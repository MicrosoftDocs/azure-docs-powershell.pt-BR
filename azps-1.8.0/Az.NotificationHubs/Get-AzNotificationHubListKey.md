---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: 6b9aa676e00d137612908955e88558b4cefb0eb8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599909"
---
# <span data-ttu-id="413a1-101">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="413a1-101">Get-AzNotificationHubListKey</span></span>

## <span data-ttu-id="413a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="413a1-102">SYNOPSIS</span></span>
<span data-ttu-id="413a1-103">Obtém as cadeias de conexão primária e secundária associadas a uma regra de autorização do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="413a1-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

## <span data-ttu-id="413a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="413a1-104">SYNTAX</span></span>

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="413a1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="413a1-105">DESCRIPTION</span></span>
<span data-ttu-id="413a1-106">O cmdlet **Get-AzNotificationHubListKey** retorna as cadeias de conexão primária e secundária de uma regra de autorização de assinatura de acesso compartilhado (SAS) do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="413a1-106">The **Get-AzNotificationHubListKey** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="413a1-107">Regras de autorização gerenciem os direitos de usuário ao Hub.</span><span class="sxs-lookup"><span data-stu-id="413a1-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="413a1-108">Cada regra inclui uma cadeia de conexão principal e secundária.</span><span class="sxs-lookup"><span data-stu-id="413a1-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="413a1-109">Essas cadeias de conexão (URIs) executam o seguinte:</span><span class="sxs-lookup"><span data-stu-id="413a1-109">These connection strings (URIs) perform the following:</span></span>
- <span data-ttu-id="413a1-110">Aponte os usuários para um recurso.</span><span class="sxs-lookup"><span data-stu-id="413a1-110">Point users to a resource.</span></span>
- <span data-ttu-id="413a1-111">Inclua um token contendo parâmetros de consulta.</span><span class="sxs-lookup"><span data-stu-id="413a1-111">Include a token containing query parameters.</span></span>
<span data-ttu-id="413a1-112">Um desses parâmetros, a assinatura, é usado para autenticar o usuário e fornecer o nível de acesso especificado.</span><span class="sxs-lookup"><span data-stu-id="413a1-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="413a1-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="413a1-113">EXAMPLES</span></span>

### <span data-ttu-id="413a1-114">Exemplo 1: obter as cadeias de conexão primária e secundária para uma regra de autorização</span><span class="sxs-lookup"><span data-stu-id="413a1-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="413a1-115">Esse comando obtém as cadeias de conexão primária e secundária para a regra de autorização ListenRule, uma regra atribuída ao Hub de notificação ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="413a1-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="413a1-116">O comando deve incluir o namespace Hub e o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="413a1-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="413a1-117">OS</span><span class="sxs-lookup"><span data-stu-id="413a1-117">PARAMETERS</span></span>

### <span data-ttu-id="413a1-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="413a1-118">-AuthorizationRule</span></span>
<span data-ttu-id="413a1-119">Especifica o nome de uma regra de autenticação de assinatura de acesso compartilhado (SAS).</span><span class="sxs-lookup"><span data-stu-id="413a1-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="413a1-120">Essas regras determinam o tipo de acesso que os usuários têm ao Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="413a1-120">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="413a1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="413a1-121">-DefaultProfile</span></span>
<span data-ttu-id="413a1-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="413a1-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="413a1-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="413a1-123">-Namespace</span></span>
<span data-ttu-id="413a1-124">Especifica o namespace ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="413a1-124">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="413a1-125">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="413a1-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="413a1-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="413a1-126">-NotificationHub</span></span>
<span data-ttu-id="413a1-127">Especifica o Hub de notificação para o qual esse cmdlet atribui uma regra de autorização.</span><span class="sxs-lookup"><span data-stu-id="413a1-127">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="413a1-128">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="413a1-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="413a1-129">-Resource</span><span class="sxs-lookup"><span data-stu-id="413a1-129">-ResourceGroup</span></span>
<span data-ttu-id="413a1-130">Especifica o grupo de recursos ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="413a1-130">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="413a1-131">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="413a1-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="413a1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="413a1-132">CommonParameters</span></span>
<span data-ttu-id="413a1-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="413a1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="413a1-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="413a1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="413a1-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="413a1-135">INPUTS</span></span>

### <span data-ttu-id="413a1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="413a1-136">System.String</span></span>

## <span data-ttu-id="413a1-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="413a1-137">OUTPUTS</span></span>

### <span data-ttu-id="413a1-138">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="413a1-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="413a1-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="413a1-139">NOTES</span></span>

## <span data-ttu-id="413a1-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="413a1-140">RELATED LINKS</span></span>

[<span data-ttu-id="413a1-141">Get-AzNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="413a1-141">Get-AzNotificationHubAuthorizationRules</span></span>](./Get-AzNotificationHubAuthorizationRules.md)


