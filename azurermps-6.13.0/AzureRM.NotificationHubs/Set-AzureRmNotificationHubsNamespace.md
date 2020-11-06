---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 2fb349628a686bb96df5685bff8a4329c0173212
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430108"
---
# <span data-ttu-id="b7dc6-101">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b7dc6-101">Set-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="b7dc6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b7dc6-102">SYNOPSIS</span></span>
<span data-ttu-id="b7dc6-103">Define valores de propriedade para um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-103">Sets property values for a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7dc6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7dc6-104">SYNTAX</span></span>

```
Set-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7dc6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b7dc6-105">DESCRIPTION</span></span>
<span data-ttu-id="b7dc6-106">O cmdlet **set-AzureRmNotificationHubsNamespace** define os valores de propriedade de um namespace de Hub de notificação existente.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-106">The **Set-AzureRmNotificationHubsNamespace** cmdlet sets the property values of an existing notification hub namespace.</span></span>
<span data-ttu-id="b7dc6-107">Namespaces são recipientes lógicos que ajudam você a organizar e gerenciar seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="b7dc6-108">Você deve ter pelo menos um namespace de Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="b7dc6-109">Além disso, todos os hubs de notificação devem ter um namespace atribuído.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-109">Additionally, all notification hubs must have an assigned namespace.</span></span>
<span data-ttu-id="b7dc6-110">Esse cmdlet é usado principalmente para habilitar e desabilitar um namespace.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-110">This cmdlet is primarily used to enable and disable a namespace.</span></span>
<span data-ttu-id="b7dc6-111">Quando um namespace está desabilitado, os usuários não podem se conectar a nenhum dos hubs de notificação no namespace, nem os administradores podem usar esses hubs para enviar notificações por push.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-111">When a namespace is disabled, users cannot connect to any of the notification hubs in the namespace, nor can administrators use those hubs to send push notifications.</span></span>
<span data-ttu-id="b7dc6-112">Para habilitar novamente um namespace desabilitado, use esse cmdlet para definir a propriedade **State** do namespace como active.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-112">To re-enable a disabled namespace, use this cmdlet to set the **State** property of the namespace to Active.</span></span>
<span data-ttu-id="b7dc6-113">Você também pode usar esse cmdlet para marcar um namespace como crítico.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-113">You can also use this cmdlet to tag a namespace as critical.</span></span>
<span data-ttu-id="b7dc6-114">Isso impede que o namespace seja excluído.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-114">This prevents the namespace from being deleted.</span></span>
<span data-ttu-id="b7dc6-115">Para remover um namespace crítico, primeiro você deve remover a marca crítica.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-115">To remove a critical namespace you must first remove the Critical tag.</span></span>

## <span data-ttu-id="b7dc6-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7dc6-116">EXAMPLES</span></span>

### <span data-ttu-id="b7dc6-117">Exemplo 1: desabilitar um namespace</span><span class="sxs-lookup"><span data-stu-id="b7dc6-117">Example 1: Disable a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

<span data-ttu-id="b7dc6-118">Esse comando desabilita o namespace chamado ContosoPartners localizado no datacenter dos EUA e atribuído ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-118">This command disables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="b7dc6-119">Exemplo 2: habilitar um namespace</span><span class="sxs-lookup"><span data-stu-id="b7dc6-119">Example 2: Enable a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

<span data-ttu-id="b7dc6-120">Esse comando habilita o namespace chamado ContosoPartners localizado no datacenter dos EUA e atribuído ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-120">This command enables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

## <span data-ttu-id="b7dc6-121">OS</span><span class="sxs-lookup"><span data-stu-id="b7dc6-121">PARAMETERS</span></span>

### <span data-ttu-id="b7dc6-122">-Crítica</span><span class="sxs-lookup"><span data-stu-id="b7dc6-122">-Critical</span></span>
<span data-ttu-id="b7dc6-123">Indica se o namespace é um namespace crítico.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-123">Indicates whether the namespace is a critical namespace.</span></span>
<span data-ttu-id="b7dc6-124">Namespaces críticos não podem ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-124">Critical namespaces cannot be deleted.</span></span>
<span data-ttu-id="b7dc6-125">Para excluir um namespace crítico, você deve definir o valor dessa propriedade como false para marcar o namespace como não crítico.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-125">To delete a critical namespace, you must set the value of this property to False in order to mark the namespace as non-critical.</span></span>

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

### <span data-ttu-id="b7dc6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7dc6-126">-DefaultProfile</span></span>
<span data-ttu-id="b7dc6-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b7dc6-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7dc6-128">-Force</span><span class="sxs-lookup"><span data-stu-id="b7dc6-128">-Force</span></span>
<span data-ttu-id="b7dc6-129">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-129">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b7dc6-130">-Local</span><span class="sxs-lookup"><span data-stu-id="b7dc6-130">-Location</span></span>
<span data-ttu-id="b7dc6-131">Especifica o nome de exibição do datacenter que hospeda o namespace.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-131">Specifies the display name of the datacenter that hosts the namespace.</span></span>
<span data-ttu-id="b7dc6-132">Embora você possa definir esse parâmetro para qualquer local válido do Azure, para desempenho ideal, você deve usar um Datacenter localizado próximo à maioria dos seus usuários.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-132">Although you can set this parameter to any valid Azure location, for optimal performance you should use a datacenter located near the majority of your users.</span></span>
<span data-ttu-id="b7dc6-133">Para obter uma lista atualizada dos locais do Azure, execute o seguinte comando: `Get-AzureLocation | Select-Object DisplayName`</span><span class="sxs-lookup"><span data-stu-id="b7dc6-133">To get an up-to-date list of Azure locations run the following command: `Get-AzureLocation | Select-Object DisplayName`</span></span>

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

### <span data-ttu-id="b7dc6-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b7dc6-134">-Namespace</span></span>
<span data-ttu-id="b7dc6-135">Especifica o namespace que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-135">Specifies the namespace that this cmdlet modifies.</span></span>
<span data-ttu-id="b7dc6-136">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-136">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="b7dc6-137">-Resource</span><span class="sxs-lookup"><span data-stu-id="b7dc6-137">-ResourceGroup</span></span>
<span data-ttu-id="b7dc6-138">Especifica o grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-138">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="b7dc6-139">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="b7dc6-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="b7dc6-140">-SkuTier</span></span>
<span data-ttu-id="b7dc6-141">Nível de SKU do namespace</span><span class="sxs-lookup"><span data-stu-id="b7dc6-141">Sku tier of the namespace</span></span>

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

### <span data-ttu-id="b7dc6-142">-Estado</span><span class="sxs-lookup"><span data-stu-id="b7dc6-142">-State</span></span>
<span data-ttu-id="b7dc6-143">Especifica o estado atual do namespace.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-143">Specifies the current state of the namespace.</span></span>
<span data-ttu-id="b7dc6-144">Os valores aceitáveis para esse parâmetro são: active e Disabled.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-144">The acceptable values for this parameter are: Active and Disabled.</span></span>

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

### <span data-ttu-id="b7dc6-145">-Marca</span><span class="sxs-lookup"><span data-stu-id="b7dc6-145">-Tag</span></span>
<span data-ttu-id="b7dc6-146">Especifica pares de nomes e valores que podem ser usados para categorizar e organizar os itens do Azure.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-146">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="b7dc6-147">A função marcas é semelhante a palavras-chave e operam em uma implantação.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-147">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="b7dc6-148">Por exemplo, se você Pesquisar todos os itens com o departamento de marcas: ele a pesquisa retornará todos os itens do Azure que têm essa marca, independentemente de itens como tipo de item, local ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-148">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="b7dc6-149">Uma marca individual consiste em duas partes: o *nome* e (opcionalmente) o *valor*.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-149">An individual tag consists of two parts: the *Name* and (optionally) the *Value*.</span></span>
<span data-ttu-id="b7dc6-150">Por exemplo, no departamento: ele, o nome da marca é departamento e o valor da marca é.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-150">For example, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="b7dc6-151">Para adicionar uma marca, use a sintaxe de tabela de hash semelhante a isso, que cria a marca CalendarYear: 2016:-Tags @ {Name = "CalendarYear"; Valor = "2016"} para adicionar várias marcas no mesmo comando, separe as marcas individuais usando vírgulas:-marca @ {Name = "CalendarYear"; Valor = "2016"}, @ {Name = "FiscalYear"; Valor = "2017"}</span><span class="sxs-lookup"><span data-stu-id="b7dc6-151">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016: -Tags @{Name="CalendarYear";Value="2016"} To add multiple tags in the same command, separate the individual tags by using commas: -Tag @{Name="CalendarYear";Value="2016"}, @{Name="FiscalYear";Value="2017"}</span></span>

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

### <span data-ttu-id="b7dc6-152">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b7dc6-152">-Confirm</span></span>
<span data-ttu-id="b7dc6-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7dc6-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7dc6-154">-WhatIf</span></span>
<span data-ttu-id="b7dc6-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7dc6-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7dc6-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7dc6-157">CommonParameters</span></span>
<span data-ttu-id="b7dc6-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7dc6-159">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7dc6-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7dc6-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b7dc6-160">INPUTS</span></span>

### <span data-ttu-id="b7dc6-161">System. String</span><span class="sxs-lookup"><span data-stu-id="b7dc6-161">System.String</span></span>

### <span data-ttu-id="b7dc6-162">Microsoft. Azure. Commands. NotificationHubs. Models. Namespacestate</span><span class="sxs-lookup"><span data-stu-id="b7dc6-162">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState</span></span>

### <span data-ttu-id="b7dc6-163">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b7dc6-163">System.Boolean</span></span>

### <span data-ttu-id="b7dc6-164">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b7dc6-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b7dc6-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b7dc6-165">OUTPUTS</span></span>

### <span data-ttu-id="b7dc6-166">Microsoft. Azure. Commands. NotificationHubs. Models. Namespaceattributes</span><span class="sxs-lookup"><span data-stu-id="b7dc6-166">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="b7dc6-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b7dc6-167">NOTES</span></span>

## <span data-ttu-id="b7dc6-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7dc6-168">RELATED LINKS</span></span>

[<span data-ttu-id="b7dc6-169">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b7dc6-169">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="b7dc6-170">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b7dc6-170">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="b7dc6-171">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="b7dc6-171">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

