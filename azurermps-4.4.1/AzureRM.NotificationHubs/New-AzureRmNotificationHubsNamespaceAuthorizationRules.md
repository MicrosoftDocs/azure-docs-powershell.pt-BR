---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: baccd437f98a12376d564bee35bdb74d736ec225
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429204"
---
# <span data-ttu-id="4b6bc-101">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="4b6bc-101">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="4b6bc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b6bc-102">SYNOPSIS</span></span>
<span data-ttu-id="4b6bc-103">Cria uma regra de autorização e atribui essa regra a um namespace do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-103">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b6bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b6bc-104">SYNTAX</span></span>

### <span data-ttu-id="4b6bc-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b6bc-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b6bc-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b6bc-106">SASRuleParameterSet</span></span>
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b6bc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b6bc-107">DESCRIPTION</span></span>
<span data-ttu-id="4b6bc-108">O cmdlet **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cria uma regra de autorização de assinatura de acesso compartilhado (SAS) e a atribui a um namespace Hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-108">The **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet creates a Shared Access Signature (SAS) authorization rule and assigns it to a notification hub namespace.</span></span>
<span data-ttu-id="4b6bc-109">As regras de autorização gerenciam os direitos do usuário para o namespace e para os hubs de notificação contidos nesse namespace.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-109">Authorization rules manage user rights to the namespace and to the notification hubs contained with that namespace.</span></span>

<span data-ttu-id="4b6bc-110">Esse cmdlet fornece duas maneiras de criar uma nova regra de autorização e atribuí-la a um namespace.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-110">This cmdlet provides two ways to create a new authorization rule and assign it to a namespace.</span></span>
<span data-ttu-id="4b6bc-111">Você pode criar uma instância do objeto **SharedAccessAuthorizationRuleAttributes** e, em seguida, configurar esse objeto com os valores de propriedade que você deseja que a nova regra possua.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-111">You can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the new rule to possess.</span></span>
<span data-ttu-id="4b6bc-112">Isso pode ser feito usando o .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-112">This can be done using .NET Framework.</span></span>
<span data-ttu-id="4b6bc-113">Em seguida, você pode copiar esses valores de propriedade para sua nova regra usando o parâmetro *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="4b6bc-113">You can then copy those property values to your new rule by using *SASRule* parameter.</span></span>

<span data-ttu-id="4b6bc-114">Você também pode criar um arquivo JSON (JavaScript Object Notation) contendo os valores de configuração relevantes e, em seguida, aplicar esses valores usando o parâmetro *InputFile* .</span><span class="sxs-lookup"><span data-stu-id="4b6bc-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="4b6bc-115">Um arquivo JSON é um arquivo de texto que usa sintaxe semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="4b6bc-115">A JSON file is a text file that uses syntax similar to the following:</span></span>

<span data-ttu-id="4b6bc-116">{</span><span class="sxs-lookup"><span data-stu-id="4b6bc-116">{</span></span>  
    <span data-ttu-id="4b6bc-117">"Nome": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="4b6bc-117">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="4b6bc-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",</span><span class="sxs-lookup"><span data-stu-id="4b6bc-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="4b6bc-119">"Direitos": \[</span><span class="sxs-lookup"><span data-stu-id="4b6bc-119">"Rights": \[</span></span>  
        <span data-ttu-id="4b6bc-120">"Ouvir",</span><span class="sxs-lookup"><span data-stu-id="4b6bc-120">"Listen",</span></span>  
        <span data-ttu-id="4b6bc-121">Envio</span><span class="sxs-lookup"><span data-stu-id="4b6bc-121">"Send"</span></span>  
    \]  
<span data-ttu-id="4b6bc-122">}</span><span class="sxs-lookup"><span data-stu-id="4b6bc-122">}</span></span>

<span data-ttu-id="4b6bc-123">Quando usado em conjunto com o cmdlet **New-AzureRmNotificationHubsNamespaceAuthorizationRules** , o exemplo JSON anterior cria uma regra de autorização chamada ContosoAuthorizationRule que permite aos usuários ouvir e enviar os direitos do namespace.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-123">When used in conjunction with the **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet, the preceding JSON sample creates an authorization rule named ContosoAuthorizationRule that gives users Listen and Send rights to the namespace.</span></span>
<span data-ttu-id="4b6bc-124">A *PrimaryKey* que é usada para autenticação, pode ser gerada aleatoriamente usando o seguinte comando do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="4b6bc-124">The *PrimaryKey* that is used for authentication, can be randomly generated by using the following Windows PowerShell command:</span></span>

<span data-ttu-id="4b6bc-125">\[Converter \] :: Tobase64string ((1.. 32 |% { \[ byte/] (Get-Random-Minimum 0-Maximum 255)}))</span><span class="sxs-lookup"><span data-stu-id="4b6bc-125">\[Convert\]::ToBase64String((1..32 |% { \[byte/](Get-Random -Minimum 0 -Maximum 255) }))</span></span>

## <span data-ttu-id="4b6bc-126">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b6bc-126">EXAMPLES</span></span>

### <span data-ttu-id="4b6bc-127">Exemplo 1: criar uma regra de autorização e atribuí-la a um namespace</span><span class="sxs-lookup"><span data-stu-id="4b6bc-127">Example 1: Create an authorization rule and assign it to a namespace</span></span>
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

<span data-ttu-id="4b6bc-128">Esse comando cria uma regra de autorização e atribui essa regra ao namespace ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-128">This command creates an authorization rule and assigns that rule to the namespace ContosoNamespace.</span></span>
<span data-ttu-id="4b6bc-129">Ao criar essa regra, você deve especificar o namespace apropriado e o grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-129">When creating this rule you must specify the appropriate namespace and the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="4b6bc-130">No entanto, você não precisa especificar qualquer informação sobre a regra em si: as informações da regra serão tiradas do arquivo de entrada C:\Configuration\NamespaceAuthorizationRules.js.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-130">However, you do not need to specify any information about the rule itself: rule information will be taken from the input file C:\Configuration\NamespaceAuthorizationRules.json.</span></span>

## <span data-ttu-id="4b6bc-131">OS</span><span class="sxs-lookup"><span data-stu-id="4b6bc-131">PARAMETERS</span></span>

### <span data-ttu-id="4b6bc-132">-InputFile</span><span class="sxs-lookup"><span data-stu-id="4b6bc-132">-InputFile</span></span>
<span data-ttu-id="4b6bc-133">Especifica o caminho para um arquivo JSON contendo informações de configuração para a nova regra de autorização.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-133">Specifies the path to a JSON file containing configuration information for the new authorization rule.</span></span>

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

### <span data-ttu-id="4b6bc-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4b6bc-134">-Namespace</span></span>
<span data-ttu-id="4b6bc-135">Especifica o namespace para o qual as regras de autorização serão atribuídas.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-135">Specifies the namespace to which the authorization rules will be assigned.</span></span>

<span data-ttu-id="4b6bc-136">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-136">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="4b6bc-137">As novas regras devem ser atribuídas a um namespace existente.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-137">The new rules must be assigned to an existing namespace.</span></span>
<span data-ttu-id="4b6bc-138">O cmdlet **New-AzureRmNotificationHubsNamespaceAuthorizationRules** não pode criar um novo namespace.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-138">The **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="4b6bc-139">-Resource</span><span class="sxs-lookup"><span data-stu-id="4b6bc-139">-ResourceGroup</span></span>
<span data-ttu-id="4b6bc-140">Especifica o grupo de recursos ao qual o namespace está atribuído.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-140">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="4b6bc-141">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-141">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

<span data-ttu-id="4b6bc-142">Você deve usar um grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-142">You must use an existing resource group.</span></span>
<span data-ttu-id="4b6bc-143">Este cmdlet não pode criar um novo grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-143">This cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="4b6bc-144">-SASRule</span><span class="sxs-lookup"><span data-stu-id="4b6bc-144">-SASRule</span></span>
<span data-ttu-id="4b6bc-145">Especifica o objeto **SharedAccessAuthorizationRuleAttributes** que contém as informações de configuração para as novas regras.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-145">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="4b6bc-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4b6bc-146">-Confirm</span></span>
<span data-ttu-id="4b6bc-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b6bc-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b6bc-148">-WhatIf</span></span>
<span data-ttu-id="4b6bc-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b6bc-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b6bc-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b6bc-151">-DefaultProfile</span></span>
<span data-ttu-id="4b6bc-152">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b6bc-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b6bc-153">CommonParameters</span></span>
<span data-ttu-id="4b6bc-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b6bc-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b6bc-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b6bc-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b6bc-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b6bc-156">INPUTS</span></span>

## <span data-ttu-id="4b6bc-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b6bc-157">OUTPUTS</span></span>

### <span data-ttu-id="4b6bc-158">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="4b6bc-158">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="4b6bc-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b6bc-159">NOTES</span></span>

## <span data-ttu-id="4b6bc-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b6bc-160">RELATED LINKS</span></span>

[<span data-ttu-id="4b6bc-161">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="4b6bc-161">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="4b6bc-162">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="4b6bc-162">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="4b6bc-163">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="4b6bc-163">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


