---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubListKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubListKeys.md
ms.openlocfilehash: 924b729ca8ba324a6f44cade48ed803b2867b6b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440986"
---
# <span data-ttu-id="3430c-101">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="3430c-101">Get-AzureRmNotificationHubListKeys</span></span>

## <span data-ttu-id="3430c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3430c-102">SYNOPSIS</span></span>
<span data-ttu-id="3430c-103">Obtém as cadeias de conexão primária e secundária associadas a uma regra de autorização do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="3430c-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3430c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3430c-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubListKeys [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3430c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3430c-105">DESCRIPTION</span></span>
<span data-ttu-id="3430c-106">O cmdlet **Get-AzureRmNotificationHubListKeys** retorna as cadeias de conexão primária e secundária de uma regra de autorização de assinatura de acesso compartilhado (SAS) do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="3430c-106">The **Get-AzureRmNotificationHubListKeys** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>

<span data-ttu-id="3430c-107">Regras de autorização gerenciem os direitos de usuário ao Hub.</span><span class="sxs-lookup"><span data-stu-id="3430c-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="3430c-108">Cada regra inclui uma cadeia de conexão principal e secundária.</span><span class="sxs-lookup"><span data-stu-id="3430c-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="3430c-109">Essas cadeias de conexão (URIs) executam o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3430c-109">These connection strings (URIs) perform the following:</span></span>

- <span data-ttu-id="3430c-110">Aponte os usuários para um recurso.</span><span class="sxs-lookup"><span data-stu-id="3430c-110">Point users to a resource.</span></span>
- <span data-ttu-id="3430c-111">Inclua um token contendo parâmetros de consulta.</span><span class="sxs-lookup"><span data-stu-id="3430c-111">Include a token containing query parameters.</span></span>

<span data-ttu-id="3430c-112">Um desses parâmetros, a assinatura, é usado para autenticar o usuário e fornecer o nível de acesso especificado.</span><span class="sxs-lookup"><span data-stu-id="3430c-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="3430c-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3430c-113">EXAMPLES</span></span>

### <span data-ttu-id="3430c-114">Exemplo 1: obter as cadeias de conexão primária e secundária para uma regra de autorização</span><span class="sxs-lookup"><span data-stu-id="3430c-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubListKeys -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="3430c-115">Esse comando obtém as cadeias de conexão primária e secundária para a regra de autorização ListenRule, uma regra atribuída ao Hub de notificação ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="3430c-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="3430c-116">O comando deve incluir o namespace Hub e o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3430c-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="3430c-117">OS</span><span class="sxs-lookup"><span data-stu-id="3430c-117">PARAMETERS</span></span>

### <span data-ttu-id="3430c-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3430c-118">-AuthorizationRule</span></span>
<span data-ttu-id="3430c-119">Especifica o nome de uma regra de autenticação de assinatura de acesso compartilhado (SAS).</span><span class="sxs-lookup"><span data-stu-id="3430c-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="3430c-120">Essas regras determinam o tipo de acesso que os usuários têm ao Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="3430c-120">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="3430c-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3430c-121">-Namespace</span></span>
<span data-ttu-id="3430c-122">Especifica o namespace ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="3430c-122">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="3430c-123">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="3430c-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="3430c-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="3430c-124">-NotificationHub</span></span>
<span data-ttu-id="3430c-125">Especifica o Hub de notificação para o qual esse cmdlet atribui uma regra de autorização.</span><span class="sxs-lookup"><span data-stu-id="3430c-125">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="3430c-126">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="3430c-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="3430c-127">-Resource</span><span class="sxs-lookup"><span data-stu-id="3430c-127">-ResourceGroup</span></span>
<span data-ttu-id="3430c-128">Especifica o grupo de recursos ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="3430c-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="3430c-129">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="3430c-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="3430c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3430c-130">-DefaultProfile</span></span>
<span data-ttu-id="3430c-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3430c-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3430c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3430c-132">CommonParameters</span></span>
<span data-ttu-id="3430c-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3430c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3430c-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3430c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3430c-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3430c-135">INPUTS</span></span>

## <span data-ttu-id="3430c-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3430c-136">OUTPUTS</span></span>

### <span data-ttu-id="3430c-137">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="3430c-137">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="3430c-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3430c-138">NOTES</span></span>

## <span data-ttu-id="3430c-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3430c-139">RELATED LINKS</span></span>

[<span data-ttu-id="3430c-140">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="3430c-140">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)


