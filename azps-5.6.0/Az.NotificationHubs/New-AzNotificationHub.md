---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
ms.openlocfilehash: 88ed662dc9938e6d4c9c3caa07ce733530dff6b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885297"
---
# <span data-ttu-id="45d7f-101">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="45d7f-101">New-AzNotificationHub</span></span>

## <span data-ttu-id="45d7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45d7f-102">SYNOPSIS</span></span>
<span data-ttu-id="45d7f-103">Cria um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="45d7f-103">Creates a notification hub.</span></span>

## <span data-ttu-id="45d7f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="45d7f-104">SYNTAX</span></span>

### <span data-ttu-id="45d7f-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="45d7f-105">InputFileParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45d7f-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="45d7f-106">NotificationHubParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45d7f-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="45d7f-107">DESCRIPTION</span></span>
<span data-ttu-id="45d7f-108">O cmdlet **New-AzNotificationHub** cria um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="45d7f-108">The **New-AzNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="45d7f-109">Os hubs de notificação são usados para enviar notificações por push a vários clientes, independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="45d7f-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="45d7f-110">Os hubs de notificação são aproximadamente equivalentes a aplicativos individuais: cada um dos seus aplicativos normalmente terá seu próprio hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="45d7f-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="45d7f-111">O cmdlet **New-AzNotificationHub** fornece duas maneiras de criar um novo hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="45d7f-111">The **New-AzNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="45d7f-112">Você pode criar uma instância do **objeto NotificationHubAttributes** e configurar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="45d7f-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="45d7f-113">Em seguida, você pode copiar esses valores de propriedade para seu novo hub por meio do *parâmetro NotificationHubObj.*</span><span class="sxs-lookup"><span data-stu-id="45d7f-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="45d7f-114">Como alternativa, você pode criar um arquivo JSON (Notação de Objeto JavaScript) contendo os valores de configuração relevantes e aplicar esses valores usando o parâmetro *InputFile.*</span><span class="sxs-lookup"><span data-stu-id="45d7f-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="45d7f-115">Quando usado em conjunto com o cmdlet **New-AzNotificationHub,** o exemplo JSON anterior cria um hub de notificação chamado ContosoNotificationHub localizado no datacenter do Oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="45d7f-115">When used in conjunction with the **New-AzNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="45d7f-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45d7f-116">EXAMPLES</span></span>

### <span data-ttu-id="45d7f-117">Exemplo 1: Criar um hub de notificação</span><span class="sxs-lookup"><span data-stu-id="45d7f-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="45d7f-118">Este comando cria um hub de notificação no namespace ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="45d7f-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="45d7f-119">O novo hub será atribuído ao ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="45d7f-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="45d7f-120">Você não precisa especificar um nome ou qualquer outra informação de configuração para o hub; essas informações serão retiradas do arquivo de entrada C:\Configurations\InternalHub.json.</span><span class="sxs-lookup"><span data-stu-id="45d7f-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="45d7f-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="45d7f-121">PARAMETERS</span></span>

### <span data-ttu-id="45d7f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45d7f-122">-DefaultProfile</span></span>
<span data-ttu-id="45d7f-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="45d7f-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45d7f-124">-InputFile</span><span class="sxs-lookup"><span data-stu-id="45d7f-124">-InputFile</span></span>
<span data-ttu-id="45d7f-125">Especifica o caminho para um arquivo JSON que contém valores de configuração para o novo hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="45d7f-125">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d7f-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="45d7f-126">-Namespace</span></span>
<span data-ttu-id="45d7f-127">Especifica o namespace ao qual o hub de notificação será atribuído.</span><span class="sxs-lookup"><span data-stu-id="45d7f-127">Specifies the namespace to which the notification hub will be assigned.</span></span>
<span data-ttu-id="45d7f-128">Os namespaces fornecem uma maneira de agrupar e categorizar hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="45d7f-128">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="45d7f-129">Os hubs de notificação devem ser atribuídos a um namespace existente.</span><span class="sxs-lookup"><span data-stu-id="45d7f-129">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="45d7f-130">O cmdlet **New-AzNotificationHub** não pode criar um novo namespace.</span><span class="sxs-lookup"><span data-stu-id="45d7f-130">The **New-AzNotificationHub** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="45d7f-131">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="45d7f-131">-NotificationHubObj</span></span>
<span data-ttu-id="45d7f-132">Especifica o **objeto NotificationHubAttributes** que contém informações de configuração para o novo hub.</span><span class="sxs-lookup"><span data-stu-id="45d7f-132">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d7f-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="45d7f-133">-ResourceGroup</span></span>
<span data-ttu-id="45d7f-134">Especifica o grupo de recursos ao qual o hub de notificação será atribuído.</span><span class="sxs-lookup"><span data-stu-id="45d7f-134">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="45d7f-135">Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente o gerenciamento de inventário e a administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="45d7f-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="45d7f-136">Você deve usar um grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="45d7f-136">You must use an existing resource group.</span></span>
<span data-ttu-id="45d7f-137">O cmdlet **New-AzNotificationHub** não pode criar um novo grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="45d7f-137">The **New-AzNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="45d7f-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45d7f-138">-Confirm</span></span>
<span data-ttu-id="45d7f-139">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45d7f-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d7f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45d7f-140">-WhatIf</span></span>
<span data-ttu-id="45d7f-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="45d7f-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45d7f-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="45d7f-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d7f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d7f-143">CommonParameters</span></span>
<span data-ttu-id="45d7f-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45d7f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d7f-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45d7f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d7f-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45d7f-146">INPUTS</span></span>

### <span data-ttu-id="45d7f-147">System.String</span><span class="sxs-lookup"><span data-stu-id="45d7f-147">System.String</span></span>

## <span data-ttu-id="45d7f-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="45d7f-148">OUTPUTS</span></span>

### <span data-ttu-id="45d7f-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="45d7f-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="45d7f-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="45d7f-150">NOTES</span></span>

## <span data-ttu-id="45d7f-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45d7f-151">RELATED LINKS</span></span>

[<span data-ttu-id="45d7f-152">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="45d7f-152">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="45d7f-153">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="45d7f-153">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="45d7f-154">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="45d7f-154">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


