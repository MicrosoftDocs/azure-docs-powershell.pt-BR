---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: eaf34373cb17fea94c498e16f623cef4bf65e937
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118238"
---
# <span data-ttu-id="7913a-101">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7913a-101">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="7913a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7913a-102">SYNOPSIS</span></span>
<span data-ttu-id="7913a-103">Cria uma regra de autorização e atribui essa regra a um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="7913a-103">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

## <span data-ttu-id="7913a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7913a-104">SYNTAX</span></span>

### <span data-ttu-id="7913a-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="7913a-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7913a-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="7913a-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7913a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7913a-107">DESCRIPTION</span></span>
<span data-ttu-id="7913a-108">O cmdlet **New-AzNotificationHubsNamespaceAuthorizationRule** cria uma regra de autorização de Assinatura de Acesso Compartilhado (SAS) e a atribui a um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="7913a-108">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet creates a Shared Access Signature (SAS) authorization rule and assigns it to a notification hub namespace.</span></span>
<span data-ttu-id="7913a-109">As regras de autorização gerenciam direitos de usuário para o namespace e para os hubs de notificação contidos com esse namespace.</span><span class="sxs-lookup"><span data-stu-id="7913a-109">Authorization rules manage user rights to the namespace and to the notification hubs contained with that namespace.</span></span>
<span data-ttu-id="7913a-110">Este cmdlet fornece duas maneiras de criar uma nova regra de autorização e atribuí-la a um namespace.</span><span class="sxs-lookup"><span data-stu-id="7913a-110">This cmdlet provides two ways to create a new authorization rule and assign it to a namespace.</span></span>
<span data-ttu-id="7913a-111">Você pode criar uma instância do objeto **SharedAccessAuthorizationRuleAttributes** e configurar esse objeto com os valores de propriedade que você deseja que a nova regra possua.</span><span class="sxs-lookup"><span data-stu-id="7913a-111">You can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the new rule to possess.</span></span>
<span data-ttu-id="7913a-112">Isso pode ser feito usando o .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="7913a-112">This can be done using .NET Framework.</span></span>
<span data-ttu-id="7913a-113">Em seguida, você pode copiar esses valores de propriedade para a nova regra usando o parâmetro *SASRule.*</span><span class="sxs-lookup"><span data-stu-id="7913a-113">You can then copy those property values to your new rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="7913a-114">Como alternativa, você pode criar um arquivo JSON (Notação de Objeto JavaScript) contendo os valores de configuração relevantes e aplicar esses valores usando o parâmetro *InputFile.*</span><span class="sxs-lookup"><span data-stu-id="7913a-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="7913a-115">Um arquivo JSON é um arquivo de texto que usa sintaxe semelhante à seguinte: {</span><span class="sxs-lookup"><span data-stu-id="7913a-115">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="7913a-116">"Nome": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="7913a-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="7913a-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span><span class="sxs-lookup"><span data-stu-id="7913a-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="7913a-118">"Direitos": \[</span><span class="sxs-lookup"><span data-stu-id="7913a-118">"Rights": \[</span></span>  
        <span data-ttu-id="7913a-119">"Ouça",</span><span class="sxs-lookup"><span data-stu-id="7913a-119">"Listen",</span></span>  
        <span data-ttu-id="7913a-120">"Enviar"</span><span class="sxs-lookup"><span data-stu-id="7913a-120">"Send"</span></span>  
    \]  
<span data-ttu-id="7913a-121">} Quando usado em conjunto com o cmdlet **New-AzNotificationHubsNamespaceAuthorizationRule,** a amostra JSON anterior cria uma regra de autorização chamada ContosoAuthorizationRule que dá aos usuários direitos de Ouvir e Enviar para o namespace.</span><span class="sxs-lookup"><span data-stu-id="7913a-121">} When used in conjunction with the **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample creates an authorization rule named ContosoAuthorizationRule that gives users Listen and Send rights to the namespace.</span></span>
<span data-ttu-id="7913a-122">A *PrimaryKey* usada para autenticação pode ser gerada aleatoriamente usando o seguinte comando do Windows PowerShell: \[ Converter \] ::ToBase64String((1,32 |% { \[ byte/](Get-Random -Minimum 0 -Maximum 255) }))</span><span class="sxs-lookup"><span data-stu-id="7913a-122">The *PrimaryKey* that is used for authentication, can be randomly generated by using the following Windows PowerShell command: \[Convert\]::ToBase64String((1..32 |% { \[byte/](Get-Random -Minimum 0 -Maximum 255) }))</span></span>

## <span data-ttu-id="7913a-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7913a-123">EXAMPLES</span></span>

### <span data-ttu-id="7913a-124">Exemplo 1: Criar uma regra de autorização e atribuí-la a um namespace</span><span class="sxs-lookup"><span data-stu-id="7913a-124">Example 1: Create an authorization rule and assign it to a namespace</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

<span data-ttu-id="7913a-125">Esse comando cria uma regra de autorização e atribui essa regra ao namespace ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="7913a-125">This command creates an authorization rule and assigns that rule to the namespace ContosoNamespace.</span></span>
<span data-ttu-id="7913a-126">Ao criar essa regra, você deve especificar o namespace apropriado e o grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="7913a-126">When creating this rule you must specify the appropriate namespace and the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="7913a-127">No entanto, você não precisa especificar nenhuma informação sobre a regra em si: as informações da regra serão retiradas do arquivo de entrada C:\Configuration\NamespaceAuthorizationRules.jsem.</span><span class="sxs-lookup"><span data-stu-id="7913a-127">However, you do not need to specify any information about the rule itself: rule information will be taken from the input file C:\Configuration\NamespaceAuthorizationRules.json.</span></span>

## <span data-ttu-id="7913a-128">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7913a-128">PARAMETERS</span></span>

### <span data-ttu-id="7913a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7913a-129">-DefaultProfile</span></span>
<span data-ttu-id="7913a-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7913a-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7913a-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="7913a-131">-InputFile</span></span>
<span data-ttu-id="7913a-132">Especifica o caminho para um arquivo JSON que contém informações de configuração para a nova regra de autorização.</span><span class="sxs-lookup"><span data-stu-id="7913a-132">Specifies the path to a JSON file containing configuration information for the new authorization rule.</span></span>

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

### <span data-ttu-id="7913a-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7913a-133">-Namespace</span></span>
<span data-ttu-id="7913a-134">Especifica o namespace ao qual as regras de autorização serão atribuídas.</span><span class="sxs-lookup"><span data-stu-id="7913a-134">Specifies the namespace to which the authorization rules will be assigned.</span></span>
<span data-ttu-id="7913a-135">Os namespaces oferecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="7913a-135">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="7913a-136">As novas regras devem ser atribuídas a um espaço de nome existente.</span><span class="sxs-lookup"><span data-stu-id="7913a-136">The new rules must be assigned to an existing namespace.</span></span>
<span data-ttu-id="7913a-137">O **cmdlet New-AzNotificationHubsNamespaceAuthorizationRule** não pode criar um novo namespace.</span><span class="sxs-lookup"><span data-stu-id="7913a-137">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="7913a-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7913a-138">-ResourceGroup</span></span>
<span data-ttu-id="7913a-139">Especifica o grupo de recursos ao qual o namespace é atribuído.</span><span class="sxs-lookup"><span data-stu-id="7913a-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="7913a-140">Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente o gerenciamento de estoque e a administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="7913a-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="7913a-141">Você deve usar um grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="7913a-141">You must use an existing resource group.</span></span>
<span data-ttu-id="7913a-142">Este cmdlet não pode criar um novo grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7913a-142">This cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="7913a-143">-SASRule</span><span class="sxs-lookup"><span data-stu-id="7913a-143">-SASRule</span></span>
<span data-ttu-id="7913a-144">Especifica o **objeto SharedAccessAuthorizationRuleAttributes** contendo informações de configuração para as novas regras.</span><span class="sxs-lookup"><span data-stu-id="7913a-144">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="7913a-145">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7913a-145">-Confirm</span></span>
<span data-ttu-id="7913a-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7913a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7913a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7913a-147">-WhatIf</span></span>
<span data-ttu-id="7913a-148">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7913a-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7913a-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7913a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7913a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7913a-150">CommonParameters</span></span>
<span data-ttu-id="7913a-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7913a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7913a-152">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7913a-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7913a-153">Entradas</span><span class="sxs-lookup"><span data-stu-id="7913a-153">INPUTS</span></span>

### <span data-ttu-id="7913a-154">System.String</span><span class="sxs-lookup"><span data-stu-id="7913a-154">System.String</span></span>

## <span data-ttu-id="7913a-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="7913a-155">OUTPUTS</span></span>

### <span data-ttu-id="7913a-156">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="7913a-156">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="7913a-157">Notas</span><span class="sxs-lookup"><span data-stu-id="7913a-157">NOTES</span></span>

## <span data-ttu-id="7913a-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7913a-158">RELATED LINKS</span></span>

[<span data-ttu-id="7913a-159">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7913a-159">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="7913a-160">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7913a-160">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="7913a-161">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7913a-161">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


