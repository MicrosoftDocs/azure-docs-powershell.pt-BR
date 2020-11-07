---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 74aa4d00d387e832c1abf02a5c65ca5e34e42123
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772916"
---
# <span data-ttu-id="a096b-101">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a096b-101">Set-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="a096b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a096b-102">SYNOPSIS</span></span>
<span data-ttu-id="a096b-103">Define regras de autorização para um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="a096b-103">Sets authorization rules for a notification hub.</span></span>

## <span data-ttu-id="a096b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a096b-104">SYNTAX</span></span>

### <span data-ttu-id="a096b-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="a096b-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a096b-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="a096b-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a096b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a096b-107">DESCRIPTION</span></span>
<span data-ttu-id="a096b-108">O cmdlet **set-AzNotificationHubAuthorizationRule** modifica uma regra de autorização de assinatura de acesso compartilhado (SAS) atribuída a um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="a096b-108">The **Set-AzNotificationHubAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="a096b-109">As regras de autorização gerenciam o acesso aos seus hubs de notificação pela criação de links, como URIs, com base em diferentes níveis de permissão.</span><span class="sxs-lookup"><span data-stu-id="a096b-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="a096b-110">Os níveis de permissão podem ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="a096b-110">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="a096b-111">Ouvir</span><span class="sxs-lookup"><span data-stu-id="a096b-111">Listen</span></span>
- <span data-ttu-id="a096b-112">Enviar</span><span class="sxs-lookup"><span data-stu-id="a096b-112">Send</span></span>
- <span data-ttu-id="a096b-113">Gerenciar clientes são direcionados para um desses URIs com base no nível de permissão apropriado.</span><span class="sxs-lookup"><span data-stu-id="a096b-113">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="a096b-114">Por exemplo, um cliente que recebeu a permissão de escuta será direcionado para o URI dessa permissão.</span><span class="sxs-lookup"><span data-stu-id="a096b-114">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="a096b-115">Esse cmdlet fornece duas maneiras de modificar uma regra de autorização atribuída a um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="a096b-115">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="a096b-116">Para um, você pode criar uma instância do objeto **SharedAccessAuthorizationRuleAttributes** e, em seguida, configurar esse objeto com os valores de propriedade que você deseja que a regra possua.</span><span class="sxs-lookup"><span data-stu-id="a096b-116">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="a096b-117">Você pode configurar o objeto por meio do .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="a096b-117">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="a096b-118">Em seguida, você pode copiar esses valores de propriedade para sua regra usando o parâmetro *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="a096b-118">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="a096b-119">Você também pode criar um arquivo JSON (JavaScript Object Notation) contendo os valores de configuração relevantes e, em seguida, aplicar esses valores por meio do parâmetro *InputFile* .</span><span class="sxs-lookup"><span data-stu-id="a096b-119">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="a096b-120">Um arquivo JSON é um arquivo de texto que usa uma sintaxe semelhante a esta: {"Name": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="a096b-120">A JSON file is a text file that uses syntax similar to this: {      "Name": "ContosoAuthorizationRule",</span></span>  
  <span data-ttu-id="a096b-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",</span><span class="sxs-lookup"><span data-stu-id="a096b-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
  <span data-ttu-id="a096b-122">"Direitos": \[</span><span class="sxs-lookup"><span data-stu-id="a096b-122">"Rights": \[</span></span>  
        <span data-ttu-id="a096b-123">"Ouvir",</span><span class="sxs-lookup"><span data-stu-id="a096b-123">"Listen",</span></span>  
        <span data-ttu-id="a096b-124">Envio</span><span class="sxs-lookup"><span data-stu-id="a096b-124">"Send"</span></span>  
    \]  
  <span data-ttu-id="a096b-125">} Quando usado em conjunto com o cmdlet New-AzNotificationHubAuthorizationRule, o exemplo JSON anterior modifica uma regra de autorização chamada ContosoAuthorizationRule para permitir que os usuários escutem e enviem direitos ao Hub.</span><span class="sxs-lookup"><span data-stu-id="a096b-125">} When used in conjunction with the New-AzNotificationHubAuthorizationRule cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="a096b-126">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a096b-126">EXAMPLES</span></span>

### <span data-ttu-id="a096b-127">Exemplo 1: modificar uma regra de autorização atribuída a um hub de notificação</span><span class="sxs-lookup"><span data-stu-id="a096b-127">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="a096b-128">Esse comando modifica uma regra de autorização atribuída ao Hub de notificação chamado ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="a096b-128">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="a096b-129">Você deve especificar o namespace no qual o Hub está localizado, bem como o grupo de recursos ao qual o Hub está atribuído.</span><span class="sxs-lookup"><span data-stu-id="a096b-129">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="a096b-130">As informações sobre a regra que é modificada não estão incluídas no próprio comando.</span><span class="sxs-lookup"><span data-stu-id="a096b-130">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="a096b-131">Em vez disso, essas informações são encontradas no arquivo de entrada C:\Configuration\AuthorizationRules.js.</span><span class="sxs-lookup"><span data-stu-id="a096b-131">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="a096b-132">OS</span><span class="sxs-lookup"><span data-stu-id="a096b-132">PARAMETERS</span></span>

### <span data-ttu-id="a096b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a096b-133">-DefaultProfile</span></span>
<span data-ttu-id="a096b-134">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a096b-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a096b-135">-Force</span><span class="sxs-lookup"><span data-stu-id="a096b-135">-Force</span></span>
<span data-ttu-id="a096b-136">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="a096b-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a096b-137">-InputFile</span><span class="sxs-lookup"><span data-stu-id="a096b-137">-InputFile</span></span>
<span data-ttu-id="a096b-138">Especifica o caminho para um arquivo JSON contendo informações de configuração para a nova regra.</span><span class="sxs-lookup"><span data-stu-id="a096b-138">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="a096b-139">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a096b-139">-Namespace</span></span>
<span data-ttu-id="a096b-140">Especifica o namespace ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="a096b-140">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="a096b-141">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="a096b-141">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="a096b-142">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="a096b-142">-NotificationHub</span></span>
<span data-ttu-id="a096b-143">Especifica o Hub de notificação ao qual esse cmdlet atribui regras de autorização.</span><span class="sxs-lookup"><span data-stu-id="a096b-143">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="a096b-144">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente do usado por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="a096b-144">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

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

### <span data-ttu-id="a096b-145">-Resource</span><span class="sxs-lookup"><span data-stu-id="a096b-145">-ResourceGroup</span></span>
<span data-ttu-id="a096b-146">Especifica o grupo de recursos ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="a096b-146">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="a096b-147">Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.</span><span class="sxs-lookup"><span data-stu-id="a096b-147">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="a096b-148">-SASRule</span><span class="sxs-lookup"><span data-stu-id="a096b-148">-SASRule</span></span>
<span data-ttu-id="a096b-149">Especifica o objeto **SharedAccessAuthorizationRuleAttributes** que contém informações de configuração para as regras de autorização que são modificadas.</span><span class="sxs-lookup"><span data-stu-id="a096b-149">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

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

### <span data-ttu-id="a096b-150">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a096b-150">-Confirm</span></span>
<span data-ttu-id="a096b-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a096b-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a096b-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a096b-152">-WhatIf</span></span>
<span data-ttu-id="a096b-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a096b-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a096b-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a096b-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a096b-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a096b-155">CommonParameters</span></span>
<span data-ttu-id="a096b-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a096b-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a096b-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a096b-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a096b-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a096b-158">INPUTS</span></span>

### <span data-ttu-id="a096b-159">System. String</span><span class="sxs-lookup"><span data-stu-id="a096b-159">System.String</span></span>

## <span data-ttu-id="a096b-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a096b-160">OUTPUTS</span></span>

### <span data-ttu-id="a096b-161">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="a096b-161">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="a096b-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a096b-162">NOTES</span></span>

## <span data-ttu-id="a096b-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a096b-163">RELATED LINKS</span></span>

[<span data-ttu-id="a096b-164">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a096b-164">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="a096b-165">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a096b-165">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="a096b-166">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a096b-166">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

