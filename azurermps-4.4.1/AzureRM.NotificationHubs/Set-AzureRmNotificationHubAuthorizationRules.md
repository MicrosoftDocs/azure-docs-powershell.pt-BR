---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 5396605719908d468399c126fbeca116060c25b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429198"
---
# <span data-ttu-id="7db1f-101">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="7db1f-101">Set-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="7db1f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7db1f-102">SYNOPSIS</span></span>
<span data-ttu-id="7db1f-103">Define regras de autorização para um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="7db1f-103">Sets authorization rules for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7db1f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7db1f-104">SYNTAX</span></span>

### <span data-ttu-id="7db1f-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="7db1f-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7db1f-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="7db1f-106">SASRuleParameterSet</span></span>
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7db1f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7db1f-107">DESCRIPTION</span></span>
<span data-ttu-id="7db1f-108">O cmdlet **set-AzureRmNotificationHubAuthorizationRules** modifica uma regra de autorização de assinatura de acesso compartilhado (SAS) atribuída a um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="7db1f-108">The **Set-AzureRmNotificationHubAuthorizationRules** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>

<span data-ttu-id="7db1f-109">As regras de autorização gerenciam o acesso aos seus hubs de notificação pela criação de links, como URIs, com base em diferentes níveis de permissão.</span><span class="sxs-lookup"><span data-stu-id="7db1f-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="7db1f-110">Os níveis de permissão podem ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="7db1f-110">Permission levels can be one of the following:</span></span> 

- <span data-ttu-id="7db1f-111">Ouvir</span><span class="sxs-lookup"><span data-stu-id="7db1f-111">Listen</span></span>
- <span data-ttu-id="7db1f-112">Enviar</span><span class="sxs-lookup"><span data-stu-id="7db1f-112">Send</span></span>
- <span data-ttu-id="7db1f-113">Gerencia</span><span class="sxs-lookup"><span data-stu-id="7db1f-113">Manage</span></span>

<span data-ttu-id="7db1f-114">Os clientes são direcionados para um desses URIs com base no nível de permissão apropriado.</span><span class="sxs-lookup"><span data-stu-id="7db1f-114">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="7db1f-115">Por exemplo, um cliente que recebeu a permissão de escuta será direcionado para o URI dessa permissão.</span><span class="sxs-lookup"><span data-stu-id="7db1f-115">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="7db1f-116">Esse cmdlet fornece duas maneiras de modificar uma regra de autorização atribuída a um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="7db1f-116">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="7db1f-117">Para um, você pode criar uma instância do objeto **SharedAccessAuthorizationRuleAttributes** e, em seguida, configurar esse objeto com os valores de propriedade que você deseja que a regra possua.</span><span class="sxs-lookup"><span data-stu-id="7db1f-117">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="7db1f-118">Você pode configurar o objeto por meio do .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="7db1f-118">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="7db1f-119">Em seguida, você pode copiar esses valores de propriedade para sua regra usando o parâmetro *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="7db1f-119">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>

<span data-ttu-id="7db1f-120">Você também pode criar um arquivo JSON (JavaScript Object Notation) contendo os valores de configuração relevantes e, em seguida, aplicar esses valores por meio do parâmetro *InputFile* .</span><span class="sxs-lookup"><span data-stu-id="7db1f-120">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="7db1f-121">Um arquivo JSON é um arquivo de texto que usa uma sintaxe semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="7db1f-121">A JSON file is a text file that uses syntax similar to this:</span></span>

<span data-ttu-id="7db1f-122">{"Nome": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="7db1f-122">{      "Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="7db1f-123">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",</span><span class="sxs-lookup"><span data-stu-id="7db1f-123">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="7db1f-124">"Direitos": \[</span><span class="sxs-lookup"><span data-stu-id="7db1f-124">"Rights": \[</span></span>  
        <span data-ttu-id="7db1f-125">"Ouvir",</span><span class="sxs-lookup"><span data-stu-id="7db1f-125">"Listen",</span></span>  
        <span data-ttu-id="7db1f-126">Envio</span><span class="sxs-lookup"><span data-stu-id="7db1f-126">"Send"</span></span>  
    \]  
<span data-ttu-id="7db1f-127">}</span><span class="sxs-lookup"><span data-stu-id="7db1f-127">}</span></span>

<span data-ttu-id="7db1f-128">Quando usado em conjunto com o cmdlet New-AzureRmNotificationHubAuthorizationRules, o exemplo JSON anterior modifica uma regra de autorização chamada ContosoAuthorizationRule para permitir que os usuários escutem e enviem direitos ao Hub.</span><span class="sxs-lookup"><span data-stu-id="7db1f-128">When used in conjunction with the New-AzureRmNotificationHubAuthorizationRules cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="7db1f-129">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7db1f-129">EXAMPLES</span></span>

### <span data-ttu-id="7db1f-130">Exemplo 1: modificar uma regra de autorização atribuída a um hub de notificação</span><span class="sxs-lookup"><span data-stu-id="7db1f-130">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="7db1f-131">Esse comando modifica uma regra de autorização atribuída ao Hub de notificação chamado ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="7db1f-131">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="7db1f-132">Você deve especificar o namespace no qual o Hub está localizado, bem como o grupo de recursos ao qual o Hub está atribuído.</span><span class="sxs-lookup"><span data-stu-id="7db1f-132">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="7db1f-133">As informações sobre a regra que é modificada não estão incluídas no próprio comando.</span><span class="sxs-lookup"><span data-stu-id="7db1f-133">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="7db1f-134">Em vez disso, essas informações são encontradas no arquivo de entrada C:\Configuration\AuthorizationRules.js.</span><span class="sxs-lookup"><span data-stu-id="7db1f-134">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="7db1f-135">OS</span><span class="sxs-lookup"><span data-stu-id="7db1f-135">PARAMETERS</span></span>

### <span data-ttu-id="7db1f-136">-Force</span><span class="sxs-lookup"><span data-stu-id="7db1f-136">-Force</span></span>
<span data-ttu-id="7db1f-137">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="7db1f-137">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7db1f-138">-InputFile</span><span class="sxs-lookup"><span data-stu-id="7db1f-138">-InputFile</span></span>
<span data-ttu-id="7db1f-139">Especifica o caminho para um arquivo JSON contendo informações de configuração para a nova regra.</span><span class="sxs-lookup"><span data-stu-id="7db1f-139">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7db1f-140">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7db1f-140">-Namespace</span></span>
<span data-ttu-id="7db1f-141">Especifica o namespace ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="7db1f-141">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="7db1f-142">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="7db1f-142">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="7db1f-143">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="7db1f-143">-NotificationHub</span></span>
<span data-ttu-id="7db1f-144">Especifica o Hub de notificação ao qual esse cmdlet atribui regras de autorização.</span><span class="sxs-lookup"><span data-stu-id="7db1f-144">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="7db1f-145">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente do usado por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="7db1f-145">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

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

### <span data-ttu-id="7db1f-146">-Resource</span><span class="sxs-lookup"><span data-stu-id="7db1f-146">-ResourceGroup</span></span>
<span data-ttu-id="7db1f-147">Especifica o grupo de recursos ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="7db1f-147">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="7db1f-148">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="7db1f-148">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="7db1f-149">-SASRule</span><span class="sxs-lookup"><span data-stu-id="7db1f-149">-SASRule</span></span>
<span data-ttu-id="7db1f-150">Especifica o objeto **SharedAccessAuthorizationRuleAttributes** que contém informações de configuração para as regras de autorização que são modificadas.</span><span class="sxs-lookup"><span data-stu-id="7db1f-150">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7db1f-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7db1f-151">-Confirm</span></span>
<span data-ttu-id="7db1f-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7db1f-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7db1f-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7db1f-153">-WhatIf</span></span>
<span data-ttu-id="7db1f-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7db1f-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7db1f-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7db1f-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7db1f-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7db1f-156">-DefaultProfile</span></span>
<span data-ttu-id="7db1f-157">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7db1f-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7db1f-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7db1f-158">CommonParameters</span></span>
<span data-ttu-id="7db1f-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7db1f-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7db1f-160">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7db1f-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7db1f-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7db1f-161">INPUTS</span></span>

## <span data-ttu-id="7db1f-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7db1f-162">OUTPUTS</span></span>

### <span data-ttu-id="7db1f-163">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="7db1f-163">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="7db1f-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7db1f-164">NOTES</span></span>

## <span data-ttu-id="7db1f-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7db1f-165">RELATED LINKS</span></span>

[<span data-ttu-id="7db1f-166">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="7db1f-166">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="7db1f-167">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="7db1f-167">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="7db1f-168">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="7db1f-168">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)


