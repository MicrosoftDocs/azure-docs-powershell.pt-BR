---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: 7535ff45b8350cb107b7593dc78ab0709d747f8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885275"
---
# <span data-ttu-id="b44b9-101">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b44b9-101">Set-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="b44b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b44b9-102">SYNOPSIS</span></span>
<span data-ttu-id="b44b9-103">Define valores de propriedade para um namespace de hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="b44b9-103">Sets property values for a notification hub namespace.</span></span>

## <span data-ttu-id="b44b9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b44b9-104">SYNTAX</span></span>

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b44b9-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b44b9-105">DESCRIPTION</span></span>
<span data-ttu-id="b44b9-106">O cmdlet **Set-AzNotificationHubsNamespace** define os valores de propriedade de um namespace de hub de notificação existente.</span><span class="sxs-lookup"><span data-stu-id="b44b9-106">The **Set-AzNotificationHubsNamespace** cmdlet sets the property values of an existing notification hub namespace.</span></span>
<span data-ttu-id="b44b9-107">Namespaces são contêineres lógicos que ajudam você a organizar e gerenciar seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="b44b9-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="b44b9-108">Você deve ter pelo menos um namespace de hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="b44b9-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="b44b9-109">Além disso, todos os hubs de notificação devem ter um namespace atribuído.</span><span class="sxs-lookup"><span data-stu-id="b44b9-109">Additionally, all notification hubs must have an assigned namespace.</span></span>
<span data-ttu-id="b44b9-110">Esse cmdlet é usado principalmente para habilitar e desabilitar um namespace.</span><span class="sxs-lookup"><span data-stu-id="b44b9-110">This cmdlet is primarily used to enable and disable a namespace.</span></span>
<span data-ttu-id="b44b9-111">Quando um namespace é desabilitado, os usuários não podem se conectar a nenhum dos hubs de notificação no namespace, nem os administradores podem usar esses hubs para enviar notificações por push.</span><span class="sxs-lookup"><span data-stu-id="b44b9-111">When a namespace is disabled, users cannot connect to any of the notification hubs in the namespace, nor can administrators use those hubs to send push notifications.</span></span>
<span data-ttu-id="b44b9-112">Para habilitar um namespace desabilitado, use este cmdlet para definir a propriedade **State** do namespace como Active.</span><span class="sxs-lookup"><span data-stu-id="b44b9-112">To re-enable a disabled namespace, use this cmdlet to set the **State** property of the namespace to Active.</span></span>
<span data-ttu-id="b44b9-113">Você também pode usar esse cmdlet para marcar um namespace como crítico.</span><span class="sxs-lookup"><span data-stu-id="b44b9-113">You can also use this cmdlet to tag a namespace as critical.</span></span>
<span data-ttu-id="b44b9-114">Isso impede que o namespace seja excluído.</span><span class="sxs-lookup"><span data-stu-id="b44b9-114">This prevents the namespace from being deleted.</span></span>
<span data-ttu-id="b44b9-115">Para remover um namespace crítico, primeiro remova a marca Critical.</span><span class="sxs-lookup"><span data-stu-id="b44b9-115">To remove a critical namespace you must first remove the Critical tag.</span></span>

## <span data-ttu-id="b44b9-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b44b9-116">EXAMPLES</span></span>

### <span data-ttu-id="b44b9-117">Exemplo 1: Desabilitar um namespace</span><span class="sxs-lookup"><span data-stu-id="b44b9-117">Example 1: Disable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

<span data-ttu-id="b44b9-118">Este comando desabilita o namespace chamado ContosoPartners localizado no datacenter dos EUA Ocidental e atribuído ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="b44b9-118">This command disables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="b44b9-119">Exemplo 2: Habilitar um namespace</span><span class="sxs-lookup"><span data-stu-id="b44b9-119">Example 2: Enable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

<span data-ttu-id="b44b9-120">Esse comando habilita o namespace chamado ContosoPartners localizado no datacenter dos EUA Ocidental e atribuído ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="b44b9-120">This command enables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

## <span data-ttu-id="b44b9-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b44b9-121">PARAMETERS</span></span>

### <span data-ttu-id="b44b9-122">-Critical</span><span class="sxs-lookup"><span data-stu-id="b44b9-122">-Critical</span></span>
<span data-ttu-id="b44b9-123">Indica se o namespace é um namespace crítico.</span><span class="sxs-lookup"><span data-stu-id="b44b9-123">Indicates whether the namespace is a critical namespace.</span></span>
<span data-ttu-id="b44b9-124">Namespaces críticos não podem ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="b44b9-124">Critical namespaces cannot be deleted.</span></span>
<span data-ttu-id="b44b9-125">Para excluir um namespace crítico, você deve definir o valor dessa propriedade como False para marcar o namespace como não crítico.</span><span class="sxs-lookup"><span data-stu-id="b44b9-125">To delete a critical namespace, you must set the value of this property to False in order to mark the namespace as non-critical.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b44b9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b44b9-126">-DefaultProfile</span></span>
<span data-ttu-id="b44b9-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b44b9-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b44b9-128">-Force</span><span class="sxs-lookup"><span data-stu-id="b44b9-128">-Force</span></span>
<span data-ttu-id="b44b9-129">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="b44b9-129">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b44b9-130">-Location</span><span class="sxs-lookup"><span data-stu-id="b44b9-130">-Location</span></span>
<span data-ttu-id="b44b9-131">Especifica o nome de exibição do datacenter que hospeda o namespace.</span><span class="sxs-lookup"><span data-stu-id="b44b9-131">Specifies the display name of the datacenter that hosts the namespace.</span></span>
<span data-ttu-id="b44b9-132">Embora você possa definir esse parâmetro para qualquer local válido do Azure, para um desempenho ideal, você deve usar um datacenter localizado perto da maioria dos usuários.</span><span class="sxs-lookup"><span data-stu-id="b44b9-132">Although you can set this parameter to any valid Azure location, for optimal performance you should use a datacenter located near the majority of your users.</span></span>
<span data-ttu-id="b44b9-133">Para obter uma lista atualizada de locais do Azure, execute o seguinte comando: `Get-AzLocation | Select-Object DisplayName`</span><span class="sxs-lookup"><span data-stu-id="b44b9-133">To get an up-to-date list of Azure locations run the following command: `Get-AzLocation | Select-Object DisplayName`</span></span>

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

### <span data-ttu-id="b44b9-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b44b9-134">-Namespace</span></span>
<span data-ttu-id="b44b9-135">Especifica o namespace que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="b44b9-135">Specifies the namespace that this cmdlet modifies.</span></span>
<span data-ttu-id="b44b9-136">Os namespaces fornecem uma maneira de agrupar e categorizar hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="b44b9-136">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="b44b9-137">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b44b9-137">-ResourceGroup</span></span>
<span data-ttu-id="b44b9-138">Especifica o grupo de recursos ao qual o namespace é atribuído.</span><span class="sxs-lookup"><span data-stu-id="b44b9-138">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="b44b9-139">Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente o gerenciamento de inventário e a administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="b44b9-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="b44b9-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="b44b9-140">-SkuTier</span></span>
<span data-ttu-id="b44b9-141">Camada Sku do namespace</span><span class="sxs-lookup"><span data-stu-id="b44b9-141">Sku tier of the namespace</span></span>

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

### <span data-ttu-id="b44b9-142">-State</span><span class="sxs-lookup"><span data-stu-id="b44b9-142">-State</span></span>
<span data-ttu-id="b44b9-143">Especifica o estado atual do namespace.</span><span class="sxs-lookup"><span data-stu-id="b44b9-143">Specifies the current state of the namespace.</span></span>
<span data-ttu-id="b44b9-144">Os valores aceitáveis para este parâmetro são: Ativo e Desabilitado.</span><span class="sxs-lookup"><span data-stu-id="b44b9-144">The acceptable values for this parameter are: Active and Disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b44b9-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="b44b9-145">-Tag</span></span>
<span data-ttu-id="b44b9-146">Especifica pares de valores de nome que podem ser usados para categorizar e organizar itens do Azure.</span><span class="sxs-lookup"><span data-stu-id="b44b9-146">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="b44b9-147">Marcas funcionam como palavras-chave e operam em uma implantação.</span><span class="sxs-lookup"><span data-stu-id="b44b9-147">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="b44b9-148">Por exemplo, se você pesquisar todos os itens com a marca Department:IT, a pesquisa retornará todos os itens do Azure que têm essa marca, independentemente de coisas como tipo de item, local ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b44b9-148">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="b44b9-149">Uma marca individual consiste em duas partes: *o Nome* e (opcionalmente) o *Valor*.</span><span class="sxs-lookup"><span data-stu-id="b44b9-149">An individual tag consists of two parts: the *Name* and (optionally) the *Value*.</span></span>
<span data-ttu-id="b44b9-150">Por exemplo, em Department:IT, o nome da marca é Department e o valor da marca é IT.</span><span class="sxs-lookup"><span data-stu-id="b44b9-150">For example, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="b44b9-151">Para adicionar uma marca, use uma sintaxe de tabela de hash semelhante a esta, que cria a marca CalendarYear:2016: -Tags @{Name="CalendarYear"; Value="2016"} Para adicionar várias marcas no mesmo comando, separe as marcas individuais usando vírgulas: -Tag @{Name="CalendarYear"; Value="2016"}, @{Name="FiscalYear"; Value="2017"}</span><span class="sxs-lookup"><span data-stu-id="b44b9-151">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016: -Tags @{Name="CalendarYear";Value="2016"} To add multiple tags in the same command, separate the individual tags by using commas: -Tag @{Name="CalendarYear";Value="2016"}, @{Name="FiscalYear";Value="2017"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b44b9-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b44b9-152">-Confirm</span></span>
<span data-ttu-id="b44b9-153">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b44b9-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b44b9-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b44b9-154">-WhatIf</span></span>
<span data-ttu-id="b44b9-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b44b9-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b44b9-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b44b9-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b44b9-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b44b9-157">CommonParameters</span></span>
<span data-ttu-id="b44b9-158">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b44b9-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b44b9-159">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b44b9-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b44b9-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b44b9-160">INPUTS</span></span>

### <span data-ttu-id="b44b9-161">System.String</span><span class="sxs-lookup"><span data-stu-id="b44b9-161">System.String</span></span>

### <span data-ttu-id="b44b9-162">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState</span><span class="sxs-lookup"><span data-stu-id="b44b9-162">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState</span></span>

### <span data-ttu-id="b44b9-163">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b44b9-163">System.Boolean</span></span>

### <span data-ttu-id="b44b9-164">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b44b9-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b44b9-165">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b44b9-165">OUTPUTS</span></span>

### <span data-ttu-id="b44b9-166">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="b44b9-166">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="b44b9-167">NOTES</span><span class="sxs-lookup"><span data-stu-id="b44b9-167">NOTES</span></span>

## <span data-ttu-id="b44b9-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b44b9-168">RELATED LINKS</span></span>

[<span data-ttu-id="b44b9-169">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b44b9-169">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="b44b9-170">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b44b9-170">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="b44b9-171">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b44b9-171">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)


