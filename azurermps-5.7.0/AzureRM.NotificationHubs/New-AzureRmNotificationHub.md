---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
ms.openlocfilehash: 57b810c448c739b6346a410284272e26b44d3aa8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428857"
---
# <span data-ttu-id="f5702-101">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f5702-101">New-AzureRmNotificationHub</span></span>

## <span data-ttu-id="f5702-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5702-102">SYNOPSIS</span></span>
<span data-ttu-id="f5702-103">Cria um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f5702-103">Creates a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5702-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5702-104">SYNTAX</span></span>

### <span data-ttu-id="f5702-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5702-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5702-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5702-106">NotificationHubParameterSet</span></span>
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5702-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f5702-107">DESCRIPTION</span></span>
<span data-ttu-id="f5702-108">O cmdlet **New-AzureRmNotificationHub** cria um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f5702-108">The **New-AzureRmNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="f5702-109">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="f5702-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="f5702-110">Os hubs de notificação são aproximadamente equivalentes a aplicativos individuais: cada um dos seus aplicativos normalmente tem seu próprio Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f5702-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>

<span data-ttu-id="f5702-111">O cmdlet **New-AzureRmNotificationHub** fornece duas maneiras de criar um novo hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f5702-111">The **New-AzureRmNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="f5702-112">Você pode criar uma instância do objeto **NotificationHubAttributes** e, em seguida, configurar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="f5702-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="f5702-113">Em seguida, você pode copiar esses valores de propriedade para o novo hub por meio do parâmetro *NotificationHubObj* .</span><span class="sxs-lookup"><span data-stu-id="f5702-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>

<span data-ttu-id="f5702-114">Você também pode criar um arquivo JSON (JavaScript Object Notation) contendo os valores de configuração relevantes e, em seguida, aplicar esses valores usando o parâmetro *InputFile* .</span><span class="sxs-lookup"><span data-stu-id="f5702-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>

<span data-ttu-id="f5702-115">Quando usado em conjunto com o cmdlet **New-AzureRmNotificationHub** , o exemplo JSON anterior cria um hub de notificação chamado ContosoNotificationHub localizado no datacenter dos EUA.</span><span class="sxs-lookup"><span data-stu-id="f5702-115">When used in conjunction with the **New-AzureRmNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="f5702-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5702-116">EXAMPLES</span></span>

### <span data-ttu-id="f5702-117">Exemplo 1: criar um hub de notificação</span><span class="sxs-lookup"><span data-stu-id="f5702-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="f5702-118">Esse comando cria um hub de notificação no namespace ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="f5702-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="f5702-119">O novo hub será atribuído ao ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="f5702-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="f5702-120">Você não precisa especificar um nome ou outras informações de configuração para o Hub; essas informações serão tiradas do arquivo de entrada C:\Configurations\InternalHub.js.</span><span class="sxs-lookup"><span data-stu-id="f5702-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="f5702-121">OS</span><span class="sxs-lookup"><span data-stu-id="f5702-121">PARAMETERS</span></span>

### <span data-ttu-id="f5702-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5702-122">-DefaultProfile</span></span>
<span data-ttu-id="f5702-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f5702-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5702-124">-InputFile</span><span class="sxs-lookup"><span data-stu-id="f5702-124">-InputFile</span></span>
<span data-ttu-id="f5702-125">Especifica o caminho para um arquivo JSON contendo valores de configuração para o novo hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="f5702-125">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5702-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f5702-126">-Namespace</span></span>
<span data-ttu-id="f5702-127">Especifica o namespace ao qual o Hub de notificações será atribuído.</span><span class="sxs-lookup"><span data-stu-id="f5702-127">Specifies the namespace to which the notification hub will be assigned.</span></span>

<span data-ttu-id="f5702-128">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="f5702-128">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="f5702-129">Os hubs de notificação devem ser atribuídos a um namespace existente.</span><span class="sxs-lookup"><span data-stu-id="f5702-129">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="f5702-130">O cmdlet **New-AzureRmNotificationHub** não pode criar um novo namespace.</span><span class="sxs-lookup"><span data-stu-id="f5702-130">The **New-AzureRmNotificationHub** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="f5702-131">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="f5702-131">-NotificationHubObj</span></span>
<span data-ttu-id="f5702-132">Especifica o objeto **NotificationHubAttributes** que contém informações de configuração para o novo hub.</span><span class="sxs-lookup"><span data-stu-id="f5702-132">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

```yaml
Type: NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5702-133">-Resource</span><span class="sxs-lookup"><span data-stu-id="f5702-133">-ResourceGroup</span></span>
<span data-ttu-id="f5702-134">Especifica o grupo de recursos ao qual o Hub de notificações será atribuído.</span><span class="sxs-lookup"><span data-stu-id="f5702-134">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="f5702-135">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="f5702-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

<span data-ttu-id="f5702-136">Você deve usar um grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="f5702-136">You must use an existing resource group.</span></span>
<span data-ttu-id="f5702-137">O cmdlet **New-AzureRmNotificationHub** não pode criar um novo grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f5702-137">The **New-AzureRmNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="f5702-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f5702-138">-Confirm</span></span>
<span data-ttu-id="f5702-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5702-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5702-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5702-140">-WhatIf</span></span>
<span data-ttu-id="f5702-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f5702-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5702-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f5702-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5702-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5702-143">CommonParameters</span></span>
<span data-ttu-id="f5702-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5702-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5702-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5702-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5702-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f5702-146">INPUTS</span></span>

### <span data-ttu-id="f5702-147">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f5702-147">None</span></span>
<span data-ttu-id="f5702-148">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="f5702-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f5702-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f5702-149">OUTPUTS</span></span>

### <span data-ttu-id="f5702-150">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="f5702-150">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="f5702-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f5702-151">NOTES</span></span>

## <span data-ttu-id="f5702-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5702-152">RELATED LINKS</span></span>

[<span data-ttu-id="f5702-153">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f5702-153">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="f5702-154">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f5702-154">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)

[<span data-ttu-id="f5702-155">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f5702-155">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


