---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceListKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceListKeys.md
ms.openlocfilehash: 0c834f8ee24090fa0da11f6c01fb0ddad3251756
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432597"
---
# <span data-ttu-id="68859-101">Get-AzureRmNotificationHubsNamespaceListKeys</span><span class="sxs-lookup"><span data-stu-id="68859-101">Get-AzureRmNotificationHubsNamespaceListKeys</span></span>

## <span data-ttu-id="68859-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="68859-102">SYNOPSIS</span></span>
<span data-ttu-id="68859-103">Obtém as cadeias de conexão primária e secundária associadas a uma regra de autorização de namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="68859-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68859-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="68859-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespaceListKeys [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68859-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="68859-105">DESCRIPTION</span></span>
<span data-ttu-id="68859-106">O cmdlet **Get-AzureRmNotificationHubsNamespaceListKeys** retorna as cadeias de conexão primária e secundária para uma regra de autorização de assinatura de acesso compartilhado (SAS) atribuída a um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="68859-106">The **Get-AzureRmNotificationHubsNamespaceListKeys** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>

<span data-ttu-id="68859-107">Regras de autorização gerenciar direitos de usuário em um namespace Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="68859-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="68859-108">Cada regra inclui uma cadeia de conexão principal e secundária.</span><span class="sxs-lookup"><span data-stu-id="68859-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="68859-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="68859-109">EXAMPLES</span></span>

### <span data-ttu-id="68859-110">Exemplo 1: obter as cadeias de conexão primária e secundária para uma regra de autorização</span><span class="sxs-lookup"><span data-stu-id="68859-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceListKeys -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="68859-111">Esse comando retorna as cadeias de conexão primária e secundária para a regra de autorização chamada ListenRule atribuída ao namespace ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="68859-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="68859-112">Ao executar esse comando, você deve incluir o nome do grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="68859-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="68859-113">OS</span><span class="sxs-lookup"><span data-stu-id="68859-113">PARAMETERS</span></span>

### <span data-ttu-id="68859-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="68859-114">-AuthorizationRule</span></span>
<span data-ttu-id="68859-115">Especifica o nome de uma regra de autenticação SAS.</span><span class="sxs-lookup"><span data-stu-id="68859-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="68859-116">Essas regras determinam o tipo de acesso que os usuários têm ao Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="68859-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="68859-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="68859-117">-Namespace</span></span>
<span data-ttu-id="68859-118">Especifica o namespace que contém as cadeias de conexão que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="68859-118">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="68859-119">-Resource</span><span class="sxs-lookup"><span data-stu-id="68859-119">-ResourceGroup</span></span>
<span data-ttu-id="68859-120">Especifica o grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="68859-120">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="68859-121">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="68859-121">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="68859-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68859-122">-DefaultProfile</span></span>
<span data-ttu-id="68859-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="68859-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68859-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68859-124">CommonParameters</span></span>
<span data-ttu-id="68859-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68859-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68859-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68859-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68859-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="68859-127">INPUTS</span></span>

## <span data-ttu-id="68859-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="68859-128">OUTPUTS</span></span>

### <span data-ttu-id="68859-129">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="68859-129">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="68859-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="68859-130">NOTES</span></span>

## <span data-ttu-id="68859-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="68859-131">RELATED LINKS</span></span>

[<span data-ttu-id="68859-132">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="68859-132">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="68859-133">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="68859-133">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


