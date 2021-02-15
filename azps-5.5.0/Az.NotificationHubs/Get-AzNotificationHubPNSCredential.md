---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 2CCDF339-9D6E-4B0C-9201-BE641C8827F6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubpnscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
ms.openlocfilehash: 282e8092050b5859809c8dad71c4da1ee86c779d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112746"
---
# <span data-ttu-id="8eed6-101">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="8eed6-101">Get-AzNotificationHubPNSCredential</span></span>

## <span data-ttu-id="8eed6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8eed6-102">SYNOPSIS</span></span>
<span data-ttu-id="8eed6-103">Obtém as credenciais PNS para um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="8eed6-103">Gets the PNS credentials for a notification hub.</span></span>

## <span data-ttu-id="8eed6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8eed6-104">SYNTAX</span></span>

```
Get-AzNotificationHubPNSCredential [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8eed6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8eed6-105">DESCRIPTION</span></span>
<span data-ttu-id="8eed6-106">O cmdlet **Get-AzNotificationHubPNSCredential** obtém as credenciais de serviço de notificação da plataforma (PNS) para um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="8eed6-106">The **Get-AzNotificationHubPNSCredential** cmdlet gets the platform notification service (PNS) credentials for a notification hub.</span></span>
<span data-ttu-id="8eed6-107">Cada hub de notificação tem um único conjunto de credenciais PNS.</span><span class="sxs-lookup"><span data-stu-id="8eed6-107">Each notification hub has a single set of PNS credentials.</span></span>
<span data-ttu-id="8eed6-108">Essas credenciais são aplicadas a serviços de notificação por push individuais, como, mas não se limitam a; o serviço de notificação por push do iOS, o serviço de notificação por push do Android e o Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="8eed6-108">These credentials are applied to individual push notification services such as, but not limited to; the iOS push notification service, the Android push notification service, and Windows Phone 8.</span></span>

## <span data-ttu-id="8eed6-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8eed6-109">EXAMPLES</span></span>

### <span data-ttu-id="8eed6-110">Exemplo 1: Obter credenciais PNS para um hub de notificação específico</span><span class="sxs-lookup"><span data-stu-id="8eed6-110">Example 1: Get PNS credentials for a specific notification hub</span></span>
```
PS C:\>Get-AzNotificationHubPNSCredential -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="8eed6-111">Esse comando obtém as credenciais PNS do hub de notificação chamado ContosoInternalHub que pertence ao grupo de recursos chamado ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="8eed6-111">This command gets the PNS credentials for the notification hub named ContosoInternalHub that belongs to the resource group named ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="8eed6-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8eed6-112">PARAMETERS</span></span>

### <span data-ttu-id="8eed6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eed6-113">-DefaultProfile</span></span>
<span data-ttu-id="8eed6-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="8eed6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8eed6-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8eed6-115">-Namespace</span></span>
<span data-ttu-id="8eed6-116">Especifica o namespace ao qual o hub de notificação está atribuído.</span><span class="sxs-lookup"><span data-stu-id="8eed6-116">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="8eed6-117">Os namespaces oferecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="8eed6-117">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="8eed6-118">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="8eed6-118">-NotificationHub</span></span>
<span data-ttu-id="8eed6-119">Especifica o hub de notificação ao que as credenciais PNS estão atribuídas.</span><span class="sxs-lookup"><span data-stu-id="8eed6-119">Specifies the notification hub that the PNS credentials are assigned to.</span></span>
<span data-ttu-id="8eed6-120">Os hubs de notificação são usados para enviar notificações por push para vários clientes independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="8eed6-120">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="8eed6-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8eed6-121">-ResourceGroup</span></span>
<span data-ttu-id="8eed6-122">Especifica o grupo de recursos ao qual o hub de notificação está atribuído.</span><span class="sxs-lookup"><span data-stu-id="8eed6-122">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="8eed6-123">Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente o gerenciamento de estoque e a administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="8eed6-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="8eed6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eed6-124">CommonParameters</span></span>
<span data-ttu-id="8eed6-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eed6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eed6-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eed6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eed6-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="8eed6-127">INPUTS</span></span>

### <span data-ttu-id="8eed6-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8eed6-128">System.String</span></span>

## <span data-ttu-id="8eed6-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="8eed6-129">OUTPUTS</span></span>

### <span data-ttu-id="8eed6-130">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="8eed6-130">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="8eed6-131">Notas</span><span class="sxs-lookup"><span data-stu-id="8eed6-131">NOTES</span></span>

## <span data-ttu-id="8eed6-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8eed6-132">RELATED LINKS</span></span>

[<span data-ttu-id="8eed6-133">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="8eed6-133">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)


