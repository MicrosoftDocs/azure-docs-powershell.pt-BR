---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 5cfdf1eb7bfbb08d0658f4245d9e45804403135f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778061"
---
# <span data-ttu-id="4c8b0-101">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4c8b0-101">New-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="4c8b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c8b0-102">SYNOPSIS</span></span>
<span data-ttu-id="4c8b0-103">Cria uma regra de autorização e atribui a regra a um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

## <span data-ttu-id="4c8b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c8b0-104">SYNTAX</span></span>

### <span data-ttu-id="4c8b0-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c8b0-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c8b0-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c8b0-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c8b0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4c8b0-107">DESCRIPTION</span></span>
<span data-ttu-id="4c8b0-108">O cmdlet **New-AzNotificationHubAuthorizationRule** cria uma regra de autorização de assinatura de acesso compartilhado (SAS) do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-108">The **New-AzNotificationHubAuthorizationRule** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="4c8b0-109">As regras de autorização são usadas para gerenciar o acesso aos seus hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="4c8b0-110">Isso é feito pela criação de links, como URIs, com base em diferentes níveis de permissão.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="4c8b0-111">Os clientes são direcionados para um desses URIs com base no nível de permissão apropriado.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="4c8b0-112">Por exemplo, um cliente que recebeu a permissão de escuta será direcionado para o URI dessa permissão.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="4c8b0-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c8b0-113">EXAMPLES</span></span>

### <span data-ttu-id="4c8b0-114">Exemplo 1: criar uma regra de autorização do hub de notificação</span><span class="sxs-lookup"><span data-stu-id="4c8b0-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="4c8b0-115">Esse comando cria uma nova regra de autorização e a atribui ao Hub de notificação chamado ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="4c8b0-116">Esse Hub está localizado no namespace ContosoNamespace e é atribuído ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="4c8b0-117">Observe que todas as informações de configuração da regra, incluindo o nome da regra, serão tiradas do arquivo de entrada C:\Configuration\ExternalAccessRule.js.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="4c8b0-118">OS</span><span class="sxs-lookup"><span data-stu-id="4c8b0-118">PARAMETERS</span></span>

### <span data-ttu-id="4c8b0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c8b0-119">-DefaultProfile</span></span>
<span data-ttu-id="4c8b0-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4c8b0-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c8b0-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="4c8b0-121">-InputFile</span></span>
<span data-ttu-id="4c8b0-122">Especifica o arquivo de entrada para a regra de autorização que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-122">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4c8b0-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4c8b0-123">-Namespace</span></span>
<span data-ttu-id="4c8b0-124">Especifica o namespace para o qual as regras de autorização são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-124">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="4c8b0-125">Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="4c8b0-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="4c8b0-126">-NotificationHub</span></span>
<span data-ttu-id="4c8b0-127">Especifica o Hub de notificação ao qual as regras de autorização serão atribuídas.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-127">Specifies the notification hub that the authorization rules will be assigned to.</span></span>
<span data-ttu-id="4c8b0-128">Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="4c8b0-129">Observe que você deve especificar o nome de um hub de notificação existente.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-129">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="4c8b0-130">O cmdlet **New-AzNotificationHubAuthorizationRule** não pode criar novos hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-130">The **New-AzNotificationHubAuthorizationRule** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="4c8b0-131">-Resource</span><span class="sxs-lookup"><span data-stu-id="4c8b0-131">-ResourceGroup</span></span>
<span data-ttu-id="4c8b0-132">Especifica o grupo de recursos ao qual o Hub de notificações está atribuído.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-132">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="4c8b0-133">-SASRule</span><span class="sxs-lookup"><span data-stu-id="4c8b0-133">-SASRule</span></span>
<span data-ttu-id="4c8b0-134">Especifica o objeto **SharedAccessAuthorizationRuleAttributes** que contém as informações de configuração para as novas regras.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-134">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="4c8b0-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4c8b0-135">-Confirm</span></span>
<span data-ttu-id="4c8b0-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c8b0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c8b0-137">-WhatIf</span></span>
<span data-ttu-id="4c8b0-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c8b0-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c8b0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c8b0-140">CommonParameters</span></span>
<span data-ttu-id="4c8b0-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c8b0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c8b0-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c8b0-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c8b0-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4c8b0-143">INPUTS</span></span>

### <span data-ttu-id="4c8b0-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4c8b0-144">System.String</span></span>

## <span data-ttu-id="4c8b0-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4c8b0-145">OUTPUTS</span></span>

### <span data-ttu-id="4c8b0-146">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="4c8b0-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="4c8b0-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4c8b0-147">NOTES</span></span>

## <span data-ttu-id="4c8b0-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c8b0-148">RELATED LINKS</span></span>

[<span data-ttu-id="4c8b0-149">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4c8b0-149">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="4c8b0-150">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4c8b0-150">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="4c8b0-151">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4c8b0-151">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


