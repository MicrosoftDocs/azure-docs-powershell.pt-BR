---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 34f63dfc89f2bb1b3b9601e8ff51b280fee9ee42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272579"
---
# <span data-ttu-id="3621c-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3621c-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="3621c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3621c-102">SYNOPSIS</span></span>
<span data-ttu-id="3621c-103">Define regras de autorização para um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="3621c-103">Sets authorization rules for a notification hub namespace.</span></span>

## <span data-ttu-id="3621c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3621c-104">SYNTAX</span></span>

### <span data-ttu-id="3621c-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="3621c-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3621c-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="3621c-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3621c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3621c-107">DESCRIPTION</span></span>
<span data-ttu-id="3621c-108">O cmdlet **set-AzNotificationHubsNamespaceAuthorizationRule** modifica uma regra de autorização de assinatura de acesso compartilhado (SAS) atribuída a um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="3621c-108">The **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="3621c-109">As regras de autorização gerenciam os direitos do usuário para o namespace e para os hubs de notificação contidos nesse namespace.</span><span class="sxs-lookup"><span data-stu-id="3621c-109">Authorization rules manage user rights to the namespace and to the notification hubs contained in that namespace.</span></span>
<span data-ttu-id="3621c-110">Esse cmdlet fornece duas maneiras de modificar uma regra de autorização atribuída a um namespace.</span><span class="sxs-lookup"><span data-stu-id="3621c-110">This cmdlet provides two ways to modify an authorization rule assigned to a namespace.</span></span>
<span data-ttu-id="3621c-111">Para um, você pode criar uma instância do objeto **SharedAccessAuthorizationRuleAttributes** e, em seguida, configurar esse objeto com os valores de propriedade que você deseja que a regra possua.</span><span class="sxs-lookup"><span data-stu-id="3621c-111">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="3621c-112">Você pode usar o .NET Framework para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="3621c-112">You can use the .NET Framework to accomplish this.</span></span>
<span data-ttu-id="3621c-113">Em seguida, você pode copiar esses valores de propriedades para a regra por meio do parâmetro *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="3621c-113">You can then copy those property values to the rule through the *SASRule* parameter.</span></span>
<span data-ttu-id="3621c-114">Você também pode criar um arquivo JSON (JavaScript Object Notation) contendo os valores de configuração relevantes e, em seguida, aplicar esses valores por meio do parâmetro *InputFile* .</span><span class="sxs-lookup"><span data-stu-id="3621c-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="3621c-115">Um arquivo JSON é um arquivo de texto que usa uma sintaxe semelhante a esta: {</span><span class="sxs-lookup"><span data-stu-id="3621c-115">A JSON file is a text file that uses syntax similar to this: {</span></span>  
    <span data-ttu-id="3621c-116">"Nome": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="3621c-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="3621c-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",</span><span class="sxs-lookup"><span data-stu-id="3621c-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="3621c-118">"Direitos": \[</span><span class="sxs-lookup"><span data-stu-id="3621c-118">"Rights": \[</span></span>  
        <span data-ttu-id="3621c-119">"Ouvir",</span><span class="sxs-lookup"><span data-stu-id="3621c-119">"Listen",</span></span>  
        <span data-ttu-id="3621c-120">Envio</span><span class="sxs-lookup"><span data-stu-id="3621c-120">"Send"</span></span>  
    \]  
<span data-ttu-id="3621c-121">} Quando usado em conjunto com o cmdlet **set-AzNotificationHubsNamespaceAuthorizationRule** , o exemplo JSON anterior modifica uma regra de autorização chamada ContosoAuthorizationRule para conceder aos usuários a permissão de escuta e envio para o namespace.</span><span class="sxs-lookup"><span data-stu-id="3621c-121">} When used in conjunction with the **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule to give users Listen and Send rights to the namespace.</span></span>

## <span data-ttu-id="3621c-122">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3621c-122">EXAMPLES</span></span>

### <span data-ttu-id="3621c-123">Exemplo 1: modificar uma regra de autorização atribuída a um namespace</span><span class="sxs-lookup"><span data-stu-id="3621c-123">Example 1: Modify an authorization rule assigned to a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="3621c-124">Esse comando modifica uma regra de autorização atribuída ao namespace chamado ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="3621c-124">This command modifies an authorization rule assigned to the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="3621c-125">Você deve especificar o grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="3621c-125">You must specify the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="3621c-126">As informações sobre a regra de autorização não estão incluídas no próprio comando.</span><span class="sxs-lookup"><span data-stu-id="3621c-126">Information about the authorization rule is not included in the command itself.</span></span>
<span data-ttu-id="3621c-127">Em vez disso, essas informações são obtidas do arquivo de entrada C:\Configuration\AuthorizationRules.js.</span><span class="sxs-lookup"><span data-stu-id="3621c-127">Instead, that information is obtained from the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="3621c-128">OS</span><span class="sxs-lookup"><span data-stu-id="3621c-128">PARAMETERS</span></span>

### <span data-ttu-id="3621c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3621c-129">-DefaultProfile</span></span>
<span data-ttu-id="3621c-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3621c-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3621c-131">-Force</span><span class="sxs-lookup"><span data-stu-id="3621c-131">-Force</span></span>
<span data-ttu-id="3621c-132">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="3621c-132">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3621c-133">-InputFile</span><span class="sxs-lookup"><span data-stu-id="3621c-133">-InputFile</span></span>
<span data-ttu-id="3621c-134">Especifica o caminho para um arquivo JSON contendo informações de configuração para a nova regra.</span><span class="sxs-lookup"><span data-stu-id="3621c-134">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="3621c-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3621c-135">-Namespace</span></span>
<span data-ttu-id="3621c-136">Especifica o namespace que contém as regras de autorização que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="3621c-136">Specifies the namespace that contains the authorization rules that this cmdlet modifies.</span></span>
<span data-ttu-id="3621c-137">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="3621c-137">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="3621c-138">-Resource</span><span class="sxs-lookup"><span data-stu-id="3621c-138">-ResourceGroup</span></span>
<span data-ttu-id="3621c-139">Especifica o grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="3621c-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="3621c-140">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="3621c-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="3621c-141">-SASRule</span><span class="sxs-lookup"><span data-stu-id="3621c-141">-SASRule</span></span>
<span data-ttu-id="3621c-142">Especifica o objeto **SharedAccessAuthorizationRuleAttributes** que contém informações de configuração para as regras de autorização que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="3621c-142">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3621c-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3621c-143">-Confirm</span></span>
<span data-ttu-id="3621c-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3621c-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3621c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3621c-145">-WhatIf</span></span>
<span data-ttu-id="3621c-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3621c-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3621c-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3621c-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3621c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3621c-148">CommonParameters</span></span>
<span data-ttu-id="3621c-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3621c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3621c-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3621c-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3621c-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3621c-151">INPUTS</span></span>

### <span data-ttu-id="3621c-152">System. String</span><span class="sxs-lookup"><span data-stu-id="3621c-152">System.String</span></span>

## <span data-ttu-id="3621c-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3621c-153">OUTPUTS</span></span>

### <span data-ttu-id="3621c-154">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="3621c-154">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="3621c-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3621c-155">NOTES</span></span>

## <span data-ttu-id="3621c-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3621c-156">RELATED LINKS</span></span>

[<span data-ttu-id="3621c-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3621c-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="3621c-158">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3621c-158">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="3621c-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3621c-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Remove-AzNotificationHubsNamespaceAuthorizationRule.md)


