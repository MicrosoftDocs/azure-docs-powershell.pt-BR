---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 24a42fba23427f437cb064e1915c19e36e7a71bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114595"
---
# <span data-ttu-id="086a4-101">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="086a4-101">New-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="086a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="086a4-102">SYNOPSIS</span></span>
<span data-ttu-id="086a4-103">Cria um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="086a4-103">Creates a notification hub namespace.</span></span>

## <span data-ttu-id="086a4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="086a4-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="086a4-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="086a4-105">DESCRIPTION</span></span>
<span data-ttu-id="086a4-106">O **cmdlet New-AzNotificationHubsNamespace** cria um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="086a4-106">The **New-AzNotificationHubsNamespace** cmdlet creates a notification hub namespace.</span></span>
<span data-ttu-id="086a4-107">Os namespaces são contêineres lógicos que ajudam você a organizar e gerenciar seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="086a4-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="086a4-108">Você deve ter pelo menos um espaço de nome do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="086a4-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="086a4-109">Um único namespace pode ter vários hubs.</span><span class="sxs-lookup"><span data-stu-id="086a4-109">A single namespace can house multiple hubs.</span></span>
<span data-ttu-id="086a4-110">Você pode ter vários namespaces para organizar seus hubs ou para dar permissão a indivíduos específicos para gerenciar um subconjunto selecionado de seus hubs.</span><span class="sxs-lookup"><span data-stu-id="086a4-110">You can have multiple namespaces to organize your hubs, or to give specific individuals permission to manage a selected subset of your hubs.</span></span>
<span data-ttu-id="086a4-111">Para criar um namespace, especifique um nome exclusivo para o namespace; especifique o datacenter onde o namespace estará localizado; e especifique o grupo de recursos ao qual o namespace será atribuído.</span><span class="sxs-lookup"><span data-stu-id="086a4-111">To create a namespace, make sure that you specify a unique name for the namespace; specify the datacenter where the namespace will be located; and, specify the resource group that the namespace will be assigned to.</span></span>
<span data-ttu-id="086a4-112">Depois que o namespace tiver sido criado, você poderá usar o cmdlet New-AzNotificationHubsNamespaceAuthorizationRules para atribuir regras de autorização a esse namespace.</span><span class="sxs-lookup"><span data-stu-id="086a4-112">After the namespace has been created you can use the New-AzNotificationHubsNamespaceAuthorizationRules cmdlet to assign authorization rules to that namespace.</span></span>
<span data-ttu-id="086a4-113">As regras de autorização são usadas para gerenciar permissões para o namespace.</span><span class="sxs-lookup"><span data-stu-id="086a4-113">Authorization rules are used to manage permissions to the namespace.</span></span>

## <span data-ttu-id="086a4-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="086a4-114">EXAMPLES</span></span>

### <span data-ttu-id="086a4-115">Exemplo 1: Criar um hub de notificação</span><span class="sxs-lookup"><span data-stu-id="086a4-115">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

<span data-ttu-id="086a4-116">Esse comando cria um hub de notificação chamado ContosoPartners.</span><span class="sxs-lookup"><span data-stu-id="086a4-116">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="086a4-117">O namespace será localizado no datacenter do Oeste dos EUA e será atribuído ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="086a4-117">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="086a4-118">Exemplo 2: Criar um hub de notificação com marcas</span><span class="sxs-lookup"><span data-stu-id="086a4-118">Example 2: Create a notification hub with tags</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

<span data-ttu-id="086a4-119">Esse comando cria um hub de notificação chamado ContosoPartners.</span><span class="sxs-lookup"><span data-stu-id="086a4-119">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="086a4-120">O namespace será localizado no datacenter do Oeste dos EUA e será atribuído ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="086a4-120">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="086a4-121">Além disso, esse comando cria uma marca com o nome Audiência e o valor PartnerOrganizations e é atribuído ao namespace.</span><span class="sxs-lookup"><span data-stu-id="086a4-121">In addition, this command creates a tag with the name Audience and the value PartnerOrganizations and is assigned to the namespace.</span></span>
<span data-ttu-id="086a4-122">Isso garante que o namespace seja exibido sempre que você filtrar itens em que a marca Audiência está definida como PartnerOrganizações.</span><span class="sxs-lookup"><span data-stu-id="086a4-122">This ensures that the namespace will be displayed any time you filter for items where the Audience tag is set to PartnerOrganizations.</span></span>

## <span data-ttu-id="086a4-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="086a4-123">PARAMETERS</span></span>

### <span data-ttu-id="086a4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="086a4-124">-DefaultProfile</span></span>
<span data-ttu-id="086a4-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="086a4-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="086a4-126">-Local</span><span class="sxs-lookup"><span data-stu-id="086a4-126">-Location</span></span>
<span data-ttu-id="086a4-127">Especifica o nome de exibição do datacenter que hospedará o Namespace.</span><span class="sxs-lookup"><span data-stu-id="086a4-127">Specifies the display name of the datacenter that will host the Namespace.</span></span>
<span data-ttu-id="086a4-128">Embora você possa definir esse parâmetro para qualquer local válido, para obter um desempenho ideal, talvez você queira usar um datacenter localizado próximo à maioria dos seus usuários.</span><span class="sxs-lookup"><span data-stu-id="086a4-128">Although you can set this parameter to any valid location, for optimal performance you might want to use a datacenter located near the majority of your users.</span></span>

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

### <span data-ttu-id="086a4-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="086a4-129">-Namespace</span></span>
<span data-ttu-id="086a4-130">Especifica o nome do novo namespace.</span><span class="sxs-lookup"><span data-stu-id="086a4-130">Specifies the name of the new namespace.</span></span>
<span data-ttu-id="086a4-131">Os namespaces oferecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="086a4-131">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="086a4-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="086a4-132">-ResourceGroup</span></span>
<span data-ttu-id="086a4-133">Especifica o grupo de recursos ao qual o namespace será atribuído.</span><span class="sxs-lookup"><span data-stu-id="086a4-133">Specifies the resource group to which the namespace will be assigned.</span></span>
<span data-ttu-id="086a4-134">Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento e administração de estoques.</span><span class="sxs-lookup"><span data-stu-id="086a4-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and administration.</span></span>

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

### <span data-ttu-id="086a4-135">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="086a4-135">-SkuTier</span></span>
<span data-ttu-id="086a4-136">Camada SKU do namespace</span><span class="sxs-lookup"><span data-stu-id="086a4-136">Sku tier of the namespace</span></span>

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

### <span data-ttu-id="086a4-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="086a4-137">-Tag</span></span>
<span data-ttu-id="086a4-138">Especifica pares de nome e valor que podem ser usados para categorizar e organizar itens do Azure.</span><span class="sxs-lookup"><span data-stu-id="086a4-138">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="086a4-139">As marcas são semelhantes às palavras-chave e operam em uma implantação.</span><span class="sxs-lookup"><span data-stu-id="086a4-139">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="086a4-140">Por exemplo, se você pesquisar todos os itens com a marca Departamento:TI, a pesquisa retornará todos os itens do Azure que têm essa marca, independentemente de itens como tipo de item, local ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="086a4-140">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="086a4-141">Uma marca individual consiste em duas partes: o *Nome* e, opcionalmente, o *Valor.*</span><span class="sxs-lookup"><span data-stu-id="086a4-141">An individual tag consists of two parts: the *Name* and, optionally, the *Value*.</span></span>
<span data-ttu-id="086a4-142">Por exemplo, em Departamento:IT, o nome da marca é Departamento e o valor da marca é IT.</span><span class="sxs-lookup"><span data-stu-id="086a4-142">For instance, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="086a4-143">Para adicionar uma marca, use a sintaxe da tabela hash semelhante a esta, que cria a marca CalendarYear:2016:</span><span class="sxs-lookup"><span data-stu-id="086a4-143">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016:</span></span>

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

### <span data-ttu-id="086a4-144">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="086a4-144">-Confirm</span></span>
<span data-ttu-id="086a4-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="086a4-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="086a4-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="086a4-146">-WhatIf</span></span>
<span data-ttu-id="086a4-147">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="086a4-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="086a4-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="086a4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="086a4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="086a4-149">CommonParameters</span></span>
<span data-ttu-id="086a4-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="086a4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="086a4-151">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="086a4-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="086a4-152">Entradas</span><span class="sxs-lookup"><span data-stu-id="086a4-152">INPUTS</span></span>

### <span data-ttu-id="086a4-153">System.String</span><span class="sxs-lookup"><span data-stu-id="086a4-153">System.String</span></span>

### <span data-ttu-id="086a4-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="086a4-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="086a4-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="086a4-155">OUTPUTS</span></span>

### <span data-ttu-id="086a4-156">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="086a4-156">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="086a4-157">Notas</span><span class="sxs-lookup"><span data-stu-id="086a4-157">NOTES</span></span>

## <span data-ttu-id="086a4-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="086a4-158">RELATED LINKS</span></span>

[<span data-ttu-id="086a4-159">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="086a4-159">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="086a4-160">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="086a4-160">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="086a4-161">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="086a4-161">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


