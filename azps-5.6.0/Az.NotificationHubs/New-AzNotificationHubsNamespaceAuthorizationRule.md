---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 49a856ef38d529c7d60b7c09b4d4a4fcdab5b59b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885292"
---
# <span data-ttu-id="a53f4-101">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a53f4-101">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="a53f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a53f4-102">SYNOPSIS</span></span>
<span data-ttu-id="a53f4-103">Cria uma regra de autorização e atribui essa regra a um namespace de hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="a53f4-103">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

## <span data-ttu-id="a53f4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a53f4-104">SYNTAX</span></span>

### <span data-ttu-id="a53f4-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="a53f4-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a53f4-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="a53f4-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a53f4-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a53f4-107">DESCRIPTION</span></span>
<span data-ttu-id="a53f4-108">O cmdlet **New-AzNotificationHubsNamespaceAuthorizationRule** cria uma regra de autorização SAS (Assinatura de Acesso Compartilhado) e a atribui a um namespace de hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="a53f4-108">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet creates a Shared Access Signature (SAS) authorization rule and assigns it to a notification hub namespace.</span></span>
<span data-ttu-id="a53f4-109">As regras de autorização gerenciam os direitos do usuário para o namespace e para os hubs de notificação contidos nesse namespace.</span><span class="sxs-lookup"><span data-stu-id="a53f4-109">Authorization rules manage user rights to the namespace and to the notification hubs contained with that namespace.</span></span>
<span data-ttu-id="a53f4-110">Este cmdlet fornece duas maneiras de criar uma nova regra de autorização e atribuí-la a um namespace.</span><span class="sxs-lookup"><span data-stu-id="a53f4-110">This cmdlet provides two ways to create a new authorization rule and assign it to a namespace.</span></span>
<span data-ttu-id="a53f4-111">Você pode criar uma instância do **objeto SharedAccessAuthorizationRuleAttributes** e, em seguida, configurar esse objeto com os valores de propriedade que você deseja que a nova regra possua.</span><span class="sxs-lookup"><span data-stu-id="a53f4-111">You can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the new rule to possess.</span></span>
<span data-ttu-id="a53f4-112">Isso pode ser feito usando .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="a53f4-112">This can be done using .NET Framework.</span></span>
<span data-ttu-id="a53f4-113">Em seguida, você pode copiar esses valores de propriedade para sua nova regra usando o parâmetro *SASRule.*</span><span class="sxs-lookup"><span data-stu-id="a53f4-113">You can then copy those property values to your new rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="a53f4-114">Como alternativa, você pode criar um arquivo JSON (Notação de Objeto JavaScript) contendo os valores de configuração relevantes e aplicar esses valores usando o parâmetro *InputFile.*</span><span class="sxs-lookup"><span data-stu-id="a53f4-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="a53f4-115">Um arquivo JSON é um arquivo de texto que usa uma sintaxe semelhante à seguinte: {</span><span class="sxs-lookup"><span data-stu-id="a53f4-115">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="a53f4-116">"Name": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="a53f4-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="a53f4-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span><span class="sxs-lookup"><span data-stu-id="a53f4-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="a53f4-118">"Direitos": \[</span><span class="sxs-lookup"><span data-stu-id="a53f4-118">"Rights": \[</span></span>  
        <span data-ttu-id="a53f4-119">"Escuta",</span><span class="sxs-lookup"><span data-stu-id="a53f4-119">"Listen",</span></span>  
        <span data-ttu-id="a53f4-120">"Enviar"</span><span class="sxs-lookup"><span data-stu-id="a53f4-120">"Send"</span></span>  
    \]  
<span data-ttu-id="a53f4-121">} Quando usado em conjunto com o cmdlet **New-AzNotificationHubsNamespaceAuthorizationRule,** o exemplo JSON anterior cria uma regra de autorização chamada ContosoAuthorizationRule que fornece aos usuários os direitos de Ouvir e Enviar para o namespace.</span><span class="sxs-lookup"><span data-stu-id="a53f4-121">} When used in conjunction with the **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample creates an authorization rule named ContosoAuthorizationRule that gives users Listen and Send rights to the namespace.</span></span>
<span data-ttu-id="a53f4-122">A *PrimaryKey* usada para autenticação pode ser gerada aleatoriamente usando o seguinte comando Windows PowerShell: \[ Convert \] ::ToBase64String((1..32 |% { \[ byte/](Get-Random -Minimum 0 -Maximum 255) }))</span><span class="sxs-lookup"><span data-stu-id="a53f4-122">The *PrimaryKey* that is used for authentication, can be randomly generated by using the following Windows PowerShell command: \[Convert\]::ToBase64String((1..32 |% { \[byte/](Get-Random -Minimum 0 -Maximum 255) }))</span></span>

## <span data-ttu-id="a53f4-123">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a53f4-123">EXAMPLES</span></span>

### <span data-ttu-id="a53f4-124">Exemplo 1: criar uma regra de autorização e atribuí-la a um namespace</span><span class="sxs-lookup"><span data-stu-id="a53f4-124">Example 1: Create an authorization rule and assign it to a namespace</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

<span data-ttu-id="a53f4-125">Este comando cria uma regra de autorização e atribui essa regra ao namespace ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="a53f4-125">This command creates an authorization rule and assigns that rule to the namespace ContosoNamespace.</span></span>
<span data-ttu-id="a53f4-126">Ao criar essa regra, você deve especificar o namespace apropriado e o grupo de recursos ao qual o namespace é atribuído.</span><span class="sxs-lookup"><span data-stu-id="a53f4-126">When creating this rule you must specify the appropriate namespace and the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="a53f4-127">No entanto, você não precisa especificar nenhuma informação sobre a regra em si: as informações de regra serão retiradas do arquivo de entrada C:\Configuration\NamespaceAuthorizationRules.json.</span><span class="sxs-lookup"><span data-stu-id="a53f4-127">However, you do not need to specify any information about the rule itself: rule information will be taken from the input file C:\Configuration\NamespaceAuthorizationRules.json.</span></span>

## <span data-ttu-id="a53f4-128">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a53f4-128">PARAMETERS</span></span>

### <span data-ttu-id="a53f4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a53f4-129">-DefaultProfile</span></span>
<span data-ttu-id="a53f4-130">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a53f4-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a53f4-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="a53f4-131">-InputFile</span></span>
<span data-ttu-id="a53f4-132">Especifica o caminho para um arquivo JSON contendo informações de configuração para a nova regra de autorização.</span><span class="sxs-lookup"><span data-stu-id="a53f4-132">Specifies the path to a JSON file containing configuration information for the new authorization rule.</span></span>

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

### <span data-ttu-id="a53f4-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a53f4-133">-Namespace</span></span>
<span data-ttu-id="a53f4-134">Especifica o namespace ao qual as regras de autorização serão atribuídas.</span><span class="sxs-lookup"><span data-stu-id="a53f4-134">Specifies the namespace to which the authorization rules will be assigned.</span></span>
<span data-ttu-id="a53f4-135">Os namespaces fornecem uma maneira de agrupar e categorizar hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="a53f4-135">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="a53f4-136">As novas regras devem ser atribuídas a um namespace existente.</span><span class="sxs-lookup"><span data-stu-id="a53f4-136">The new rules must be assigned to an existing namespace.</span></span>
<span data-ttu-id="a53f4-137">O cmdlet **New-AzNotificationHubsNamespaceAuthorizationRule** não pode criar um novo namespace.</span><span class="sxs-lookup"><span data-stu-id="a53f4-137">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="a53f4-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a53f4-138">-ResourceGroup</span></span>
<span data-ttu-id="a53f4-139">Especifica o grupo de recursos ao qual o namespace é atribuído.</span><span class="sxs-lookup"><span data-stu-id="a53f4-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="a53f4-140">Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente o gerenciamento de inventário e a administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="a53f4-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="a53f4-141">Você deve usar um grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="a53f4-141">You must use an existing resource group.</span></span>
<span data-ttu-id="a53f4-142">Este cmdlet não pode criar um novo grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a53f4-142">This cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="a53f4-143">-SASRule</span><span class="sxs-lookup"><span data-stu-id="a53f4-143">-SASRule</span></span>
<span data-ttu-id="a53f4-144">Especifica o **objeto SharedAccessAuthorizationRuleAttributes** que contém informações de configuração para as novas regras.</span><span class="sxs-lookup"><span data-stu-id="a53f4-144">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="a53f4-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a53f4-145">-Confirm</span></span>
<span data-ttu-id="a53f4-146">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a53f4-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a53f4-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a53f4-147">-WhatIf</span></span>
<span data-ttu-id="a53f4-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a53f4-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a53f4-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a53f4-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a53f4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a53f4-150">CommonParameters</span></span>
<span data-ttu-id="a53f4-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a53f4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a53f4-152">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a53f4-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a53f4-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a53f4-153">INPUTS</span></span>

### <span data-ttu-id="a53f4-154">System.String</span><span class="sxs-lookup"><span data-stu-id="a53f4-154">System.String</span></span>

## <span data-ttu-id="a53f4-155">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a53f4-155">OUTPUTS</span></span>

### <span data-ttu-id="a53f4-156">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="a53f4-156">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="a53f4-157">NOTES</span><span class="sxs-lookup"><span data-stu-id="a53f4-157">NOTES</span></span>

## <span data-ttu-id="a53f4-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a53f4-158">RELATED LINKS</span></span>

[<span data-ttu-id="a53f4-159">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a53f4-159">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="a53f4-160">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a53f4-160">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="a53f4-161">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a53f4-161">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


