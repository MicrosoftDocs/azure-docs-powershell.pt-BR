---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: c3a30457e6fd25aa633a0faa0510ed4ce61efbd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430714"
---
# <span data-ttu-id="a5e1c-101">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a5e1c-101">New-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="a5e1c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e1c-103">Cria uma regra de autorização e atribui a regra a um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="a5e1c-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5e1c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5e1c-104">SYNTAX</span></span>

### <span data-ttu-id="a5e1c-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5e1c-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5e1c-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5e1c-106">SASRuleParameterSet</span></span>
```
New-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5e1c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5e1c-107">DESCRIPTION</span></span>
<span data-ttu-id="a5e1c-108">O cmdlet **New-AzureRmNotificationHubAuthorizationRules** cria uma regra de autorização de assinatura de acesso compartilhado (SAS) do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="a5e1c-108">The **New-AzureRmNotificationHubAuthorizationRules** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>

<span data-ttu-id="a5e1c-109">As regras de autorização são usadas para gerenciar o acesso aos seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="a5e1c-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="a5e1c-110">Isso é feito pela criação de links, como URIs, com base em diferentes níveis de permissão.</span><span class="sxs-lookup"><span data-stu-id="a5e1c-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="a5e1c-111">Os clientes são direcionados para um desses URIs com base no nível de permissão apropriado.</span><span class="sxs-lookup"><span data-stu-id="a5e1c-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="a5e1c-112">Por exemplo, um cliente que recebeu a permissão de escuta será direcionado para o URI dessa permissão.</span><span class="sxs-lookup"><span data-stu-id="a5e1c-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="a5e1c-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5e1c-113">EXAMPLES</span></span>

### <span data-ttu-id="a5e1c-114">Exemplo 1: criar uma regra de autorização do hub de notificação</span><span class="sxs-lookup"><span data-stu-id="a5e1c-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="a5e1c-115">Esse comando cria uma nova regra de autorização e a atribui ao Hub de notificação chamado ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="a5e1c-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="a5e1c-116">Esse Hub está localizado no namespace ContosoNamespace e é atribuído ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="a5e1c-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="a5e1c-117">Observe que todas as informações de configuração da regra, incluindo o nome da regra, serão tiradas do arquivo de entrada C:\Configuration\ExternalAccessRule.js.</span><span class="sxs-lookup"><span data-stu-id="a5e1c-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="a5e1c-118">OS</span><span class="sxs-lookup"><span data-stu-id="a5e1c-118">PARAMETERS</span></span>

### <span data-ttu-id="a5e1c-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="a5e1c-119">-InputFile</span></span>
<span data-ttu-id="a5e1c-120">Especifica o arquivo de entrada para a regra de autorização que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="a5e1c-120">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a5e1c-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a5e1c-121">-Namespace</span></span>
<span data-ttu-id="a5e1c-122">Especifica o namespace para o qual as regras de autorização são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="a5e1c-122">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="a5e1c-123">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="a5e1c-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="a5e1c-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="a5e1c-124">-NotificationHub</span></span>
<span data-ttu-id="a5e1c-125">Especifica o Hub de notificação ao qual as regras de autorização serão atribuídas.</span><span class="sxs-lookup"><span data-stu-id="a5e1c-125">Specifies the notification hub that the authorization rules will be assigned to.</span></span>

<span data-ttu-id="a5e1c-126">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="a5e1c-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="a5e1c-127">Observe que você deve especificar o nome de um hub de notificação existente.</span><span class="sxs-lookup"><span data-stu-id="a5e1c-127">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="a5e1c-128">O cmdlet **New-AzureRmNotificationHubAuthorizationRules** não pode criar novos hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="a5e1c-128">The **New-AzureRmNotificationHubAuthorizationRules** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="a5e1c-129">-Resource</span><span class="sxs-lookup"><span data-stu-id="a5e1c-129">-ResourceGroup</span></span>
<span data-ttu-id="a5e1c-130">Especifica o grupo de recursos ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="a5e1c-130">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="a5e1c-131">-SASRule</span><span class="sxs-lookup"><span data-stu-id="a5e1c-131">-SASRule</span></span>
<span data-ttu-id="a5e1c-132">Especifica o objeto **SharedAccessAuthorizationRuleAttributes** que contém as informações de configuração para as novas regras.</span><span class="sxs-lookup"><span data-stu-id="a5e1c-132">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="a5e1c-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a5e1c-133">-Confirm</span></span>
<span data-ttu-id="a5e1c-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5e1c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5e1c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5e1c-135">-WhatIf</span></span>
<span data-ttu-id="a5e1c-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a5e1c-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5e1c-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a5e1c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5e1c-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e1c-138">-DefaultProfile</span></span>
<span data-ttu-id="a5e1c-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5e1c-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5e1c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e1c-140">CommonParameters</span></span>
<span data-ttu-id="a5e1c-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5e1c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e1c-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5e1c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e1c-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5e1c-143">INPUTS</span></span>

## <span data-ttu-id="a5e1c-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5e1c-144">OUTPUTS</span></span>

### <span data-ttu-id="a5e1c-145">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="a5e1c-145">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="a5e1c-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5e1c-146">NOTES</span></span>

## <span data-ttu-id="a5e1c-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5e1c-147">RELATED LINKS</span></span>

[<span data-ttu-id="a5e1c-148">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a5e1c-148">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="a5e1c-149">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a5e1c-149">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="a5e1c-150">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a5e1c-150">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)

