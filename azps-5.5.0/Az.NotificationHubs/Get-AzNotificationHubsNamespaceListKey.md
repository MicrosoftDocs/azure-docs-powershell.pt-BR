---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 2217a0c8aa68e815b650cd3eb564ce7a21733e72
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115030"
---
# <span data-ttu-id="7675c-101">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="7675c-101">Get-AzNotificationHubsNamespaceListKey</span></span>

## <span data-ttu-id="7675c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7675c-102">SYNOPSIS</span></span>
<span data-ttu-id="7675c-103">Obtém as cadeias de conexão primária e secundária associadas a uma regra de autorização do namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="7675c-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

## <span data-ttu-id="7675c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7675c-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7675c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7675c-105">DESCRIPTION</span></span>
<span data-ttu-id="7675c-106">O cmdlet **Get-AzNotificationHubsNamespaceListKey** retorna as cadeias de conexão primária e secundária para uma regra de autorização de Assinatura de Acesso Compartilhado (SAS) atribuída a um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="7675c-106">The **Get-AzNotificationHubsNamespaceListKey** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="7675c-107">As regras de autorização gerenciam direitos de usuário para um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="7675c-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="7675c-108">Cada regra inclui uma cadeia de conexão primária e secundária.</span><span class="sxs-lookup"><span data-stu-id="7675c-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="7675c-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7675c-109">EXAMPLES</span></span>

### <span data-ttu-id="7675c-110">Exemplo 1: Obter as cadeias de conexão primária e secundária para uma regra de autorização</span><span class="sxs-lookup"><span data-stu-id="7675c-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="7675c-111">Esse comando retorna as cadeias de conexão primária e secundária para a regra de autorização chamada ListenRule atribuída ao namespace ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="7675c-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="7675c-112">Ao executar esse comando, você deve incluir o nome do grupo de recursos ao que o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="7675c-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="7675c-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7675c-113">PARAMETERS</span></span>

### <span data-ttu-id="7675c-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7675c-114">-AuthorizationRule</span></span>
<span data-ttu-id="7675c-115">Especifica o nome de uma regra de autenticação SAS.</span><span class="sxs-lookup"><span data-stu-id="7675c-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="7675c-116">Essas regras determinam o tipo de acesso que os usuários têm ao hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="7675c-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="7675c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7675c-117">-DefaultProfile</span></span>
<span data-ttu-id="7675c-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7675c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7675c-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7675c-119">-Namespace</span></span>
<span data-ttu-id="7675c-120">Especifica o namespace que contém as cadeias de conexão que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="7675c-120">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7675c-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7675c-121">-ResourceGroup</span></span>
<span data-ttu-id="7675c-122">Especifica o grupo de recursos ao qual o namespace é atribuído.</span><span class="sxs-lookup"><span data-stu-id="7675c-122">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="7675c-123">Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente o gerenciamento de estoque e a administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="7675c-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="7675c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7675c-124">CommonParameters</span></span>
<span data-ttu-id="7675c-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7675c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7675c-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7675c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7675c-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="7675c-127">INPUTS</span></span>

### <span data-ttu-id="7675c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="7675c-128">System.String</span></span>

## <span data-ttu-id="7675c-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="7675c-129">OUTPUTS</span></span>

### <span data-ttu-id="7675c-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="7675c-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="7675c-131">Notas</span><span class="sxs-lookup"><span data-stu-id="7675c-131">NOTES</span></span>

## <span data-ttu-id="7675c-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7675c-132">RELATED LINKS</span></span>

[<span data-ttu-id="7675c-133">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="7675c-133">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="7675c-134">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7675c-134">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)


