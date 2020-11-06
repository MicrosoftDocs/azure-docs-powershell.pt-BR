---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: a25e318aca1bca33c309a6f24b862e98c02659e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429191"
---
# <span data-ttu-id="c18f8-101">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="c18f8-101">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="c18f8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c18f8-102">SYNOPSIS</span></span>
<span data-ttu-id="c18f8-103">Define regras de autorização para um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="c18f8-103">Sets authorization rules for a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c18f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c18f8-104">SYNTAX</span></span>

### <span data-ttu-id="c18f8-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="c18f8-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c18f8-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="c18f8-106">SASRuleParameterSet</span></span>
```
Set-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c18f8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c18f8-107">DESCRIPTION</span></span>
<span data-ttu-id="c18f8-108">O cmdlet **set-AzureRmNotificationHubsNamespaceAuthorizationRules** modifica uma regra de autorização de assinatura de acesso compartilhado (SAS) atribuída a um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="c18f8-108">The **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="c18f8-109">As regras de autorização gerenciam os direitos do usuário para o namespace e para os hubs de notificação contidos nesse namespace.</span><span class="sxs-lookup"><span data-stu-id="c18f8-109">Authorization rules manage user rights to the namespace and to the notification hubs contained in that namespace.</span></span>

<span data-ttu-id="c18f8-110">Esse cmdlet fornece duas maneiras de modificar uma regra de autorização atribuída a um namespace.</span><span class="sxs-lookup"><span data-stu-id="c18f8-110">This cmdlet provides two ways to modify an authorization rule assigned to a namespace.</span></span>
<span data-ttu-id="c18f8-111">Para um, você pode criar uma instância do objeto **SharedAccessAuthorizationRuleAttributes** e, em seguida, configurar esse objeto com os valores de propriedade que você deseja que a regra possua.</span><span class="sxs-lookup"><span data-stu-id="c18f8-111">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="c18f8-112">Você pode usar o .NET Framework para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="c18f8-112">You can use the .NET Framework to accomplish this.</span></span>
<span data-ttu-id="c18f8-113">Em seguida, você pode copiar esses valores de propriedades para a regra por meio do parâmetro *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="c18f8-113">You can then copy those property values to the rule through the *SASRule* parameter.</span></span>

<span data-ttu-id="c18f8-114">Você também pode criar um arquivo JSON (JavaScript Object Notation) contendo os valores de configuração relevantes e, em seguida, aplicar esses valores por meio do parâmetro *InputFile* .</span><span class="sxs-lookup"><span data-stu-id="c18f8-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="c18f8-115">Um arquivo JSON é um arquivo de texto que usa uma sintaxe semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="c18f8-115">A JSON file is a text file that uses syntax similar to this:</span></span>

<span data-ttu-id="c18f8-116">{</span><span class="sxs-lookup"><span data-stu-id="c18f8-116">{</span></span>  
    <span data-ttu-id="c18f8-117">"Nome": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="c18f8-117">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="c18f8-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",</span><span class="sxs-lookup"><span data-stu-id="c18f8-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="c18f8-119">"Direitos": \[</span><span class="sxs-lookup"><span data-stu-id="c18f8-119">"Rights": \[</span></span>  
        <span data-ttu-id="c18f8-120">"Ouvir",</span><span class="sxs-lookup"><span data-stu-id="c18f8-120">"Listen",</span></span>  
        <span data-ttu-id="c18f8-121">Envio</span><span class="sxs-lookup"><span data-stu-id="c18f8-121">"Send"</span></span>  
    \]  
<span data-ttu-id="c18f8-122">}</span><span class="sxs-lookup"><span data-stu-id="c18f8-122">}</span></span>

<span data-ttu-id="c18f8-123">Quando usado em conjunto com o cmdlet **set-AzureRmNotificationHubsNamespaceAuthorizationRules** , o exemplo de JSON anterior modifica uma regra de autorização chamada ContosoAuthorizationRule para conceder aos usuários a permissão de escuta e envio para o namespace.</span><span class="sxs-lookup"><span data-stu-id="c18f8-123">When used in conjunction with the **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule to give users Listen and Send rights to the namespace.</span></span>

## <span data-ttu-id="c18f8-124">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c18f8-124">EXAMPLES</span></span>

### <span data-ttu-id="c18f8-125">Exemplo 1: modificar uma regra de autorização atribuída a um namespace</span><span class="sxs-lookup"><span data-stu-id="c18f8-125">Example 1: Modify an authorization rule assigned to a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="c18f8-126">Esse comando modifica uma regra de autorização atribuída ao namespace chamado ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="c18f8-126">This command modifies an authorization rule assigned to the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="c18f8-127">Você deve especificar o grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="c18f8-127">You must specify the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="c18f8-128">As informações sobre a regra de autorização não estão incluídas no próprio comando.</span><span class="sxs-lookup"><span data-stu-id="c18f8-128">Information about the authorization rule is not included in the command itself.</span></span>
<span data-ttu-id="c18f8-129">Em vez disso, essas informações são obtidas do arquivo de entrada C:\Configuration\AuthorizationRules.js.</span><span class="sxs-lookup"><span data-stu-id="c18f8-129">Instead, that information is obtained from the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="c18f8-130">OS</span><span class="sxs-lookup"><span data-stu-id="c18f8-130">PARAMETERS</span></span>

### <span data-ttu-id="c18f8-131">-Force</span><span class="sxs-lookup"><span data-stu-id="c18f8-131">-Force</span></span>
<span data-ttu-id="c18f8-132">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="c18f8-132">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c18f8-133">-InputFile</span><span class="sxs-lookup"><span data-stu-id="c18f8-133">-InputFile</span></span>
<span data-ttu-id="c18f8-134">Especifica o caminho para um arquivo JSON contendo informações de configuração para a nova regra.</span><span class="sxs-lookup"><span data-stu-id="c18f8-134">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="c18f8-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c18f8-135">-Namespace</span></span>
<span data-ttu-id="c18f8-136">Especifica o namespace que contém as regras de autorização que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="c18f8-136">Specifies the namespace that contains the authorization rules that this cmdlet modifies.</span></span>
<span data-ttu-id="c18f8-137">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="c18f8-137">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="c18f8-138">-Resource</span><span class="sxs-lookup"><span data-stu-id="c18f8-138">-ResourceGroup</span></span>
<span data-ttu-id="c18f8-139">Especifica o grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="c18f8-139">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="c18f8-140">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="c18f8-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="c18f8-141">-SASRule</span><span class="sxs-lookup"><span data-stu-id="c18f8-141">-SASRule</span></span>
<span data-ttu-id="c18f8-142">Especifica o objeto **SharedAccessAuthorizationRuleAttributes** que contém informações de configuração para as regras de autorização que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="c18f8-142">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c18f8-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c18f8-143">-Confirm</span></span>
<span data-ttu-id="c18f8-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c18f8-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c18f8-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c18f8-145">-WhatIf</span></span>
<span data-ttu-id="c18f8-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c18f8-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c18f8-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c18f8-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c18f8-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c18f8-148">-DefaultProfile</span></span>
<span data-ttu-id="c18f8-149">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c18f8-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c18f8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c18f8-150">CommonParameters</span></span>
<span data-ttu-id="c18f8-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c18f8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c18f8-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c18f8-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c18f8-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c18f8-153">INPUTS</span></span>

## <span data-ttu-id="c18f8-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c18f8-154">OUTPUTS</span></span>

### <span data-ttu-id="c18f8-155">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="c18f8-155">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="c18f8-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c18f8-156">NOTES</span></span>

## <span data-ttu-id="c18f8-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c18f8-157">RELATED LINKS</span></span>

[<span data-ttu-id="c18f8-158">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="c18f8-158">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="c18f8-159">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="c18f8-159">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="c18f8-160">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="c18f8-160">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


