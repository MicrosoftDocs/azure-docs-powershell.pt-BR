---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 2CCDF339-9D6E-4B0C-9201-BE641C8827F6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubpnscredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubPNSCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubPNSCredentials.md
ms.openlocfilehash: 3b4bf50adafddcc70a60cba008095169b92b4fef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430384"
---
# <span data-ttu-id="a83a0-101">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="a83a0-101">Get-AzureRmNotificationHubPNSCredentials</span></span>

## <span data-ttu-id="a83a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a83a0-102">SYNOPSIS</span></span>
<span data-ttu-id="a83a0-103">Obtém as credenciais do PNS para um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="a83a0-103">Gets the PNS credentials for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a83a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a83a0-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubPNSCredentials [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a83a0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a83a0-105">DESCRIPTION</span></span>
<span data-ttu-id="a83a0-106">O cmdlet **Get-AzureRmNotificationHubPNSCredentials** Obtém as credenciais do PNS (serviço de notificação de plataforma) para um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="a83a0-106">The **Get-AzureRmNotificationHubPNSCredentials** cmdlet gets the platform notification service (PNS) credentials for a notification hub.</span></span>
<span data-ttu-id="a83a0-107">Cada Hub de notificação tem um único conjunto de credenciais PNS.</span><span class="sxs-lookup"><span data-stu-id="a83a0-107">Each notification hub has a single set of PNS credentials.</span></span>
<span data-ttu-id="a83a0-108">Essas credenciais são aplicadas a serviços de notificação por push individuais, como, mas não se limitando a; o serviço de notificação por push do iOS, o serviço de notificação por push do Android e o Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="a83a0-108">These credentials are applied to individual push notification services such as, but not limited to; the iOS push notification service, the Android push notification service, and Windows Phone 8.</span></span>

## <span data-ttu-id="a83a0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a83a0-109">EXAMPLES</span></span>

### <span data-ttu-id="a83a0-110">Exemplo 1: obter credenciais do PNS para um hub de notificação específico</span><span class="sxs-lookup"><span data-stu-id="a83a0-110">Example 1: Get PNS credentials for a specific notification hub</span></span>
```
PS C:\>Get-AzureRmNotificationHubPNSCredentials -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="a83a0-111">Este comando obtém as credenciais PNS para o Hub de notificação chamado ContosoInternalHub que pertence ao grupo de recursos chamado ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="a83a0-111">This command gets the PNS credentials for the notification hub named ContosoInternalHub that belongs to the resource group named ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="a83a0-112">OS</span><span class="sxs-lookup"><span data-stu-id="a83a0-112">PARAMETERS</span></span>

### <span data-ttu-id="a83a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a83a0-113">-DefaultProfile</span></span>
<span data-ttu-id="a83a0-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a83a0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a83a0-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a83a0-115">-Namespace</span></span>
<span data-ttu-id="a83a0-116">Especifica o namespace ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="a83a0-116">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="a83a0-117">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="a83a0-117">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a83a0-118">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="a83a0-118">-NotificationHub</span></span>
<span data-ttu-id="a83a0-119">Especifica o Hub de notificação ao qual as credenciais do PNS são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="a83a0-119">Specifies the notification hub that the PNS credentials are assigned to.</span></span>

<span data-ttu-id="a83a0-120">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="a83a0-120">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a83a0-121">-Resource</span><span class="sxs-lookup"><span data-stu-id="a83a0-121">-ResourceGroup</span></span>
<span data-ttu-id="a83a0-122">Especifica o grupo de recursos ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="a83a0-122">Specifies the resource group to which the notification hub is assigned.</span></span>

<span data-ttu-id="a83a0-123">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="a83a0-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a83a0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a83a0-124">CommonParameters</span></span>
<span data-ttu-id="a83a0-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a83a0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a83a0-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a83a0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a83a0-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a83a0-127">INPUTS</span></span>

### <span data-ttu-id="a83a0-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a83a0-128">None</span></span>
<span data-ttu-id="a83a0-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a83a0-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a83a0-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a83a0-130">OUTPUTS</span></span>

### <span data-ttu-id="a83a0-131">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="a83a0-131">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="a83a0-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a83a0-132">NOTES</span></span>

## <span data-ttu-id="a83a0-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a83a0-133">RELATED LINKS</span></span>

[<span data-ttu-id="a83a0-134">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a83a0-134">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)


