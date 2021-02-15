---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 34f63dfc89f2bb1b3b9601e8ff51b280fee9ee42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118228"
---
# <span data-ttu-id="a3b66-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a3b66-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="a3b66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3b66-102">SYNOPSIS</span></span>
<span data-ttu-id="a3b66-103">Define regras de autorização para um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="a3b66-103">Sets authorization rules for a notification hub namespace.</span></span>

## <span data-ttu-id="a3b66-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3b66-104">SYNTAX</span></span>

### <span data-ttu-id="a3b66-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3b66-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3b66-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3b66-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3b66-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3b66-107">DESCRIPTION</span></span>
<span data-ttu-id="a3b66-108">O cmdlet **Set-AzNotificationHubsNamespaceAuthorizationRule** modifica uma regra de autorização de Assinatura de Acesso Compartilhado (SAS) atribuída a um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="a3b66-108">The **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="a3b66-109">As regras de autorização gerenciam direitos de usuário para o namespace e para os hubs de notificação contidos nesse namespace.</span><span class="sxs-lookup"><span data-stu-id="a3b66-109">Authorization rules manage user rights to the namespace and to the notification hubs contained in that namespace.</span></span>
<span data-ttu-id="a3b66-110">Este cmdlet fornece duas maneiras de modificar uma regra de autorização atribuída a um namespace.</span><span class="sxs-lookup"><span data-stu-id="a3b66-110">This cmdlet provides two ways to modify an authorization rule assigned to a namespace.</span></span>
<span data-ttu-id="a3b66-111">Por exemplo, você pode criar uma instância do objeto **SharedAccessAuthorizationRuleAttributes** e configurar esse objeto com os valores de propriedade que você deseja que a regra possua.</span><span class="sxs-lookup"><span data-stu-id="a3b66-111">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="a3b66-112">Você pode usar o .NET Framework para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="a3b66-112">You can use the .NET Framework to accomplish this.</span></span>
<span data-ttu-id="a3b66-113">Em seguida, você pode copiar esses valores de propriedade para a regra por meio do parâmetro *SASRule.*</span><span class="sxs-lookup"><span data-stu-id="a3b66-113">You can then copy those property values to the rule through the *SASRule* parameter.</span></span>
<span data-ttu-id="a3b66-114">Como alternativa, você pode criar um arquivo JSON (Notação de Objeto JavaScript) contendo os valores de configuração relevantes e aplicar esses valores por meio do parâmetro *InputFile.*</span><span class="sxs-lookup"><span data-stu-id="a3b66-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="a3b66-115">Um arquivo JSON é um arquivo de texto que usa sintaxe semelhante a esta: {</span><span class="sxs-lookup"><span data-stu-id="a3b66-115">A JSON file is a text file that uses syntax similar to this: {</span></span>  
    <span data-ttu-id="a3b66-116">"Nome": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="a3b66-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="a3b66-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span><span class="sxs-lookup"><span data-stu-id="a3b66-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="a3b66-118">"Direitos": \[</span><span class="sxs-lookup"><span data-stu-id="a3b66-118">"Rights": \[</span></span>  
        <span data-ttu-id="a3b66-119">"Ouça",</span><span class="sxs-lookup"><span data-stu-id="a3b66-119">"Listen",</span></span>  
        <span data-ttu-id="a3b66-120">"Enviar"</span><span class="sxs-lookup"><span data-stu-id="a3b66-120">"Send"</span></span>  
    \]  
<span data-ttu-id="a3b66-121">} Quando usado em conjunto com o cmdlet **Set-AzNotificationHubsNamespaceAuthorizationRule,** a amostra JSON anterior modifica uma regra de autorização chamada ContosoAuthorizationRule para dar aos usuários direitos de Ouvir e Enviar para o namespace.</span><span class="sxs-lookup"><span data-stu-id="a3b66-121">} When used in conjunction with the **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule to give users Listen and Send rights to the namespace.</span></span>

## <span data-ttu-id="a3b66-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a3b66-122">EXAMPLES</span></span>

### <span data-ttu-id="a3b66-123">Exemplo 1: Modificar uma regra de autorização atribuída a um namespace</span><span class="sxs-lookup"><span data-stu-id="a3b66-123">Example 1: Modify an authorization rule assigned to a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="a3b66-124">Esse comando modifica uma regra de autorização atribuída ao namespace chamado ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="a3b66-124">This command modifies an authorization rule assigned to the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="a3b66-125">Você deve especificar o grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="a3b66-125">You must specify the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="a3b66-126">As informações sobre a regra de autorização não estão incluídas no próprio comando.</span><span class="sxs-lookup"><span data-stu-id="a3b66-126">Information about the authorization rule is not included in the command itself.</span></span>
<span data-ttu-id="a3b66-127">Em vez disso, essas informações são obtidas do arquivo de entrada C:\Configuration\AuthorizationRules.jsem.</span><span class="sxs-lookup"><span data-stu-id="a3b66-127">Instead, that information is obtained from the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="a3b66-128">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3b66-128">PARAMETERS</span></span>

### <span data-ttu-id="a3b66-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3b66-129">-DefaultProfile</span></span>
<span data-ttu-id="a3b66-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a3b66-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3b66-131">-Forçar</span><span class="sxs-lookup"><span data-stu-id="a3b66-131">-Force</span></span>
<span data-ttu-id="a3b66-132">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="a3b66-132">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a3b66-133">-InputFile</span><span class="sxs-lookup"><span data-stu-id="a3b66-133">-InputFile</span></span>
<span data-ttu-id="a3b66-134">Especifica o caminho para um arquivo JSON que contém informações de configuração para a nova regra.</span><span class="sxs-lookup"><span data-stu-id="a3b66-134">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="a3b66-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a3b66-135">-Namespace</span></span>
<span data-ttu-id="a3b66-136">Especifica o namespace que contém as regras de autorização que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="a3b66-136">Specifies the namespace that contains the authorization rules that this cmdlet modifies.</span></span>
<span data-ttu-id="a3b66-137">Os namespaces oferecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="a3b66-137">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="a3b66-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a3b66-138">-ResourceGroup</span></span>
<span data-ttu-id="a3b66-139">Especifica o grupo de recursos ao qual o namespace é atribuído.</span><span class="sxs-lookup"><span data-stu-id="a3b66-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="a3b66-140">Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente o gerenciamento de estoque e a administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="a3b66-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="a3b66-141">-SASRule</span><span class="sxs-lookup"><span data-stu-id="a3b66-141">-SASRule</span></span>
<span data-ttu-id="a3b66-142">Especifica o **objeto SharedAccessAuthorizationRuleAttributes** que contém informações de configuração para as regras de autorização que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="a3b66-142">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a3b66-143">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a3b66-143">-Confirm</span></span>
<span data-ttu-id="a3b66-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3b66-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3b66-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3b66-145">-WhatIf</span></span>
<span data-ttu-id="a3b66-146">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a3b66-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3b66-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a3b66-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3b66-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3b66-148">CommonParameters</span></span>
<span data-ttu-id="a3b66-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3b66-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3b66-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3b66-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3b66-151">Entradas</span><span class="sxs-lookup"><span data-stu-id="a3b66-151">INPUTS</span></span>

### <span data-ttu-id="a3b66-152">System.String</span><span class="sxs-lookup"><span data-stu-id="a3b66-152">System.String</span></span>

## <span data-ttu-id="a3b66-153">Saídas</span><span class="sxs-lookup"><span data-stu-id="a3b66-153">OUTPUTS</span></span>

### <span data-ttu-id="a3b66-154">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="a3b66-154">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="a3b66-155">Notas</span><span class="sxs-lookup"><span data-stu-id="a3b66-155">NOTES</span></span>

## <span data-ttu-id="a3b66-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3b66-156">RELATED LINKS</span></span>

[<span data-ttu-id="a3b66-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a3b66-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="a3b66-158">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a3b66-158">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="a3b66-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a3b66-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Remove-AzNotificationHubsNamespaceAuthorizationRule.md)


