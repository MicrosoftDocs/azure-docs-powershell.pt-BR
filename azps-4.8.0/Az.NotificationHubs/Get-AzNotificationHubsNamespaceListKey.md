---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 2217a0c8aa68e815b650cd3eb564ce7a21733e72
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114756"
---
# <span data-ttu-id="fb41b-101">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="fb41b-101">Get-AzNotificationHubsNamespaceListKey</span></span>

## <span data-ttu-id="fb41b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb41b-102">SYNOPSIS</span></span>
<span data-ttu-id="fb41b-103">Obtém as cadeias de conexão primária e secundária associadas a uma regra de autorização de namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="fb41b-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

## <span data-ttu-id="fb41b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb41b-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb41b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb41b-105">DESCRIPTION</span></span>
<span data-ttu-id="fb41b-106">O cmdlet **Get-AzNotificationHubsNamespaceListKey** retorna as cadeias de conexão primária e secundária para uma regra de autorização de assinatura de acesso compartilhado (SAS) atribuída a um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="fb41b-106">The **Get-AzNotificationHubsNamespaceListKey** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="fb41b-107">Regras de autorização gerenciar direitos de usuário em um namespace Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="fb41b-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="fb41b-108">Cada regra inclui uma cadeia de conexão principal e secundária.</span><span class="sxs-lookup"><span data-stu-id="fb41b-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="fb41b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb41b-109">EXAMPLES</span></span>

### <span data-ttu-id="fb41b-110">Exemplo 1: obter as cadeias de conexão primária e secundária para uma regra de autorização</span><span class="sxs-lookup"><span data-stu-id="fb41b-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="fb41b-111">Esse comando retorna as cadeias de conexão primária e secundária para a regra de autorização chamada ListenRule atribuída ao namespace ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="fb41b-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="fb41b-112">Ao executar esse comando, você deve incluir o nome do grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="fb41b-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="fb41b-113">OS</span><span class="sxs-lookup"><span data-stu-id="fb41b-113">PARAMETERS</span></span>

### <span data-ttu-id="fb41b-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fb41b-114">-AuthorizationRule</span></span>
<span data-ttu-id="fb41b-115">Especifica o nome de uma regra de autenticação SAS.</span><span class="sxs-lookup"><span data-stu-id="fb41b-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="fb41b-116">Essas regras determinam o tipo de acesso que os usuários têm ao Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="fb41b-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="fb41b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb41b-117">-DefaultProfile</span></span>
<span data-ttu-id="fb41b-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fb41b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb41b-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fb41b-119">-Namespace</span></span>
<span data-ttu-id="fb41b-120">Especifica o namespace que contém as cadeias de conexão que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="fb41b-120">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fb41b-121">-Resource</span><span class="sxs-lookup"><span data-stu-id="fb41b-121">-ResourceGroup</span></span>
<span data-ttu-id="fb41b-122">Especifica o grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="fb41b-122">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="fb41b-123">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="fb41b-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="fb41b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb41b-124">CommonParameters</span></span>
<span data-ttu-id="fb41b-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb41b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb41b-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb41b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb41b-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb41b-127">INPUTS</span></span>

### <span data-ttu-id="fb41b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fb41b-128">System.String</span></span>

## <span data-ttu-id="fb41b-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb41b-129">OUTPUTS</span></span>

### <span data-ttu-id="fb41b-130">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="fb41b-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="fb41b-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb41b-131">NOTES</span></span>

## <span data-ttu-id="fb41b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb41b-132">RELATED LINKS</span></span>

[<span data-ttu-id="fb41b-133">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="fb41b-133">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="fb41b-134">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fb41b-134">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)


