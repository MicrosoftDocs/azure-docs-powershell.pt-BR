---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: d4bba9d54dac21a8eb19a4b161bb2fdef29d4bb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440735"
---
# <span data-ttu-id="6ce44-101">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="6ce44-101">New-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="6ce44-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ce44-102">SYNOPSIS</span></span>
<span data-ttu-id="6ce44-103">Cria um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="6ce44-103">Creates a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ce44-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ce44-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ce44-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6ce44-105">DESCRIPTION</span></span>
<span data-ttu-id="6ce44-106">O cmdlet **New-AzureRmNotificationHubsNamespace** cria um namespace Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="6ce44-106">The **New-AzureRmNotificationHubsNamespace** cmdlet creates a notification hub namespace.</span></span>
<span data-ttu-id="6ce44-107">Namespaces são recipientes lógicos que ajudam você a organizar e gerenciar seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="6ce44-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="6ce44-108">Você deve ter pelo menos um namespace de Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="6ce44-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="6ce44-109">Um único namespace pode alojar vários hubs.</span><span class="sxs-lookup"><span data-stu-id="6ce44-109">A single namespace can house multiple hubs.</span></span>
<span data-ttu-id="6ce44-110">Você pode ter vários namespaces para organizar seus hubs ou para dar a pessoas específicas permissão para gerenciar um subconjunto selecionado de seus hubs.</span><span class="sxs-lookup"><span data-stu-id="6ce44-110">You can have multiple namespaces to organize your hubs, or to give specific individuals permission to manage a selected subset of your hubs.</span></span>
<span data-ttu-id="6ce44-111">Para criar um namespace, certifique-se de especificar um nome exclusivo para o namespace; Especifique o datacenter onde o namespace será localizado; e especifique o grupo de recursos ao qual o namespace será atribuído.</span><span class="sxs-lookup"><span data-stu-id="6ce44-111">To create a namespace, make sure that you specify a unique name for the namespace; specify the datacenter where the namespace will be located; and, specify the resource group that the namespace will be assigned to.</span></span>
<span data-ttu-id="6ce44-112">Após a criação do namespace, você pode usar o cmdlet New-AzureRmNotificationHubsNamespaceAuthorizationRules para atribuir regras de autorização a esse namespace.</span><span class="sxs-lookup"><span data-stu-id="6ce44-112">After the namespace has been created you can use the New-AzureRmNotificationHubsNamespaceAuthorizationRules cmdlet to assign authorization rules to that namespace.</span></span>
<span data-ttu-id="6ce44-113">Regras de autorização são usadas para gerenciar permissões para o namespace.</span><span class="sxs-lookup"><span data-stu-id="6ce44-113">Authorization rules are used to manage permissions to the namespace.</span></span>

## <span data-ttu-id="6ce44-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ce44-114">EXAMPLES</span></span>

### <span data-ttu-id="6ce44-115">Exemplo 1: criar um hub de notificação</span><span class="sxs-lookup"><span data-stu-id="6ce44-115">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

<span data-ttu-id="6ce44-116">Esse comando cria um hub de notificação chamado ContosoPartners.</span><span class="sxs-lookup"><span data-stu-id="6ce44-116">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="6ce44-117">O namespace estará localizado no centro de data do oeste dos EUA e será atribuído ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="6ce44-117">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="6ce44-118">Exemplo 2: criar um hub de notificação com marcas</span><span class="sxs-lookup"><span data-stu-id="6ce44-118">Example 2: Create a notification hub with tags</span></span>
```
PS C:\>New-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

<span data-ttu-id="6ce44-119">Esse comando cria um hub de notificação chamado ContosoPartners.</span><span class="sxs-lookup"><span data-stu-id="6ce44-119">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="6ce44-120">O namespace estará localizado no centro de data do oeste dos EUA e será atribuído ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="6ce44-120">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="6ce44-121">Além disso, esse comando cria uma marca com o nome Audience e o valor PartnerOrganizations e é atribuído ao namespace.</span><span class="sxs-lookup"><span data-stu-id="6ce44-121">In addition, this command creates a tag with the name Audience and the value PartnerOrganizations and is assigned to the namespace.</span></span>
<span data-ttu-id="6ce44-122">Isso garante que o namespace será exibido sempre que você filtrar itens em que a marca de audiência estiver definida como PartnerOrganizations.</span><span class="sxs-lookup"><span data-stu-id="6ce44-122">This ensures that the namespace will be displayed any time you filter for items where the Audience tag is set to PartnerOrganizations.</span></span>

## <span data-ttu-id="6ce44-123">OS</span><span class="sxs-lookup"><span data-stu-id="6ce44-123">PARAMETERS</span></span>

### <span data-ttu-id="6ce44-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ce44-124">-DefaultProfile</span></span>
<span data-ttu-id="6ce44-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6ce44-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ce44-126">-Local</span><span class="sxs-lookup"><span data-stu-id="6ce44-126">-Location</span></span>
<span data-ttu-id="6ce44-127">Especifica o nome de exibição do datacenter que irá hospedar o namespace.</span><span class="sxs-lookup"><span data-stu-id="6ce44-127">Specifies the display name of the datacenter that will host the Namespace.</span></span>
<span data-ttu-id="6ce44-128">Embora você possa definir esse parâmetro como qualquer local válido para obter um desempenho ideal, talvez queira usar um Datacenter localizado próximo à maioria dos usuários.</span><span class="sxs-lookup"><span data-stu-id="6ce44-128">Although you can set this parameter to any valid location, for optimal performance you might want to use a datacenter located near the majority of your users.</span></span>

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

### <span data-ttu-id="6ce44-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6ce44-129">-Namespace</span></span>
<span data-ttu-id="6ce44-130">Especifica o nome do novo namespace.</span><span class="sxs-lookup"><span data-stu-id="6ce44-130">Specifies the name of the new namespace.</span></span>
<span data-ttu-id="6ce44-131">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="6ce44-131">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="6ce44-132">-Resource</span><span class="sxs-lookup"><span data-stu-id="6ce44-132">-ResourceGroup</span></span>
<span data-ttu-id="6ce44-133">Especifica o grupo de recursos ao qual o namespace será atribuído.</span><span class="sxs-lookup"><span data-stu-id="6ce44-133">Specifies the resource group to which the namespace will be assigned.</span></span>
<span data-ttu-id="6ce44-134">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento e administração de inventário.</span><span class="sxs-lookup"><span data-stu-id="6ce44-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and administration.</span></span>

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

### <span data-ttu-id="6ce44-135">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="6ce44-135">-SkuTier</span></span>
<span data-ttu-id="6ce44-136">Nível de SKU do namespace</span><span class="sxs-lookup"><span data-stu-id="6ce44-136">Sku tier of the namespace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce44-137">-Marca</span><span class="sxs-lookup"><span data-stu-id="6ce44-137">-Tag</span></span>
<span data-ttu-id="6ce44-138">Especifica pares de nomes e valores que podem ser usados para categorizar e organizar os itens do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ce44-138">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="6ce44-139">A função marcas é semelhante a palavras-chave e operam em uma implantação.</span><span class="sxs-lookup"><span data-stu-id="6ce44-139">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="6ce44-140">Por exemplo, se você Pesquisar todos os itens com o departamento de marcas: ele a pesquisa retornará todos os itens do Azure que têm essa marca, independentemente de itens como tipo de item, local ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6ce44-140">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="6ce44-141">Uma marca individual consiste em duas partes: o *nome* e, opcionalmente, o *valor*.</span><span class="sxs-lookup"><span data-stu-id="6ce44-141">An individual tag consists of two parts: the *Name* and, optionally, the *Value*.</span></span>
<span data-ttu-id="6ce44-142">Por exemplo, no departamento: ele, o nome da marca é departamento e o valor da marca é.</span><span class="sxs-lookup"><span data-stu-id="6ce44-142">For instance, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="6ce44-143">Para adicionar uma marca, use a sintaxe de tabela de hash semelhante a essa, que cria a marca CalendarYear: 2016:</span><span class="sxs-lookup"><span data-stu-id="6ce44-143">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016:</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce44-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6ce44-144">-Confirm</span></span>
<span data-ttu-id="6ce44-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ce44-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ce44-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ce44-146">-WhatIf</span></span>
<span data-ttu-id="6ce44-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6ce44-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ce44-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6ce44-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ce44-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ce44-149">CommonParameters</span></span>
<span data-ttu-id="6ce44-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ce44-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ce44-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ce44-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ce44-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6ce44-152">INPUTS</span></span>

### <span data-ttu-id="6ce44-153">System. String</span><span class="sxs-lookup"><span data-stu-id="6ce44-153">System.String</span></span>

### <span data-ttu-id="6ce44-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6ce44-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6ce44-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6ce44-155">OUTPUTS</span></span>

### <span data-ttu-id="6ce44-156">Microsoft. Azure. Commands. NotificationHubs. Models. Namespaceattributes</span><span class="sxs-lookup"><span data-stu-id="6ce44-156">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="6ce44-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6ce44-157">NOTES</span></span>

## <span data-ttu-id="6ce44-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ce44-158">RELATED LINKS</span></span>

[<span data-ttu-id="6ce44-159">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="6ce44-159">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="6ce44-160">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="6ce44-160">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="6ce44-161">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="6ce44-161">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)

