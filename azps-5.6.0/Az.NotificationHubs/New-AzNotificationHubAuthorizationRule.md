---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 74ad4f80a25250129d050ed3a2769dca6f776376
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885295"
---
# <span data-ttu-id="91d26-101">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="91d26-101">New-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="91d26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91d26-102">SYNOPSIS</span></span>
<span data-ttu-id="91d26-103">Cria uma regra de autorização e atribui a regra a um hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="91d26-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

## <span data-ttu-id="91d26-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="91d26-104">SYNTAX</span></span>

### <span data-ttu-id="91d26-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="91d26-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91d26-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="91d26-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91d26-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="91d26-107">DESCRIPTION</span></span>
<span data-ttu-id="91d26-108">O cmdlet **New-AzNotificationHubAuthorizationRule** cria uma regra de autorização SAS (Assinatura de Acesso Compartilhado) do hub de notificação.</span><span class="sxs-lookup"><span data-stu-id="91d26-108">The **New-AzNotificationHubAuthorizationRule** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="91d26-109">As regras de autorização são usadas para gerenciar o acesso aos hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="91d26-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="91d26-110">Isso é feito pela criação de links, como URIs, com base em diferentes níveis de permissão.</span><span class="sxs-lookup"><span data-stu-id="91d26-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="91d26-111">Os clientes são direcionados para uma dessas URIs com base no nível de permissão apropriado.</span><span class="sxs-lookup"><span data-stu-id="91d26-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="91d26-112">Por exemplo, um cliente com a permissão Ouvir será direcionado para o URI para essa permissão.</span><span class="sxs-lookup"><span data-stu-id="91d26-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="91d26-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91d26-113">EXAMPLES</span></span>

### <span data-ttu-id="91d26-114">Exemplo 1: Criar uma regra de autorização de hub de notificação</span><span class="sxs-lookup"><span data-stu-id="91d26-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="91d26-115">Este comando cria uma nova regra de autorização e a atribui ao hub de notificação chamado ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="91d26-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="91d26-116">Esse hub está localizado no namespace ContosoNamespace e é atribuído ao grupo de recursos ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="91d26-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="91d26-117">Observe que todas as informações de configuração da regra, incluindo o nome da regra, serão retiradas do arquivo de entrada C:\Configuration\ExternalAccessRule.json.</span><span class="sxs-lookup"><span data-stu-id="91d26-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="91d26-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="91d26-118">PARAMETERS</span></span>

### <span data-ttu-id="91d26-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91d26-119">-DefaultProfile</span></span>
<span data-ttu-id="91d26-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="91d26-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91d26-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="91d26-121">-InputFile</span></span>
<span data-ttu-id="91d26-122">Especifica o arquivo de entrada para a regra de autorização que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="91d26-122">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="91d26-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="91d26-123">-Namespace</span></span>
<span data-ttu-id="91d26-124">Especifica o namespace ao qual as regras de autorização são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="91d26-124">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="91d26-125">Os namespaces fornecem uma maneira de agrupar e categorizar hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="91d26-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="91d26-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="91d26-126">-NotificationHub</span></span>
<span data-ttu-id="91d26-127">Especifica o hub de notificação ao que as regras de autorização serão atribuídas.</span><span class="sxs-lookup"><span data-stu-id="91d26-127">Specifies the notification hub that the authorization rules will be assigned to.</span></span>
<span data-ttu-id="91d26-128">Os hubs de notificação são usados para enviar notificações por push a vários clientes, independentemente da plataforma usada por esses clientes.</span><span class="sxs-lookup"><span data-stu-id="91d26-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="91d26-129">Observe que você deve especificar o nome de um hub de notificação existente.</span><span class="sxs-lookup"><span data-stu-id="91d26-129">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="91d26-130">O cmdlet **New-AzNotificationHubAuthorizationRule** não pode criar novos hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="91d26-130">The **New-AzNotificationHubAuthorizationRule** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="91d26-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="91d26-131">-ResourceGroup</span></span>
<span data-ttu-id="91d26-132">Especifica o grupo de recursos ao que o hub de notificação é atribuído.</span><span class="sxs-lookup"><span data-stu-id="91d26-132">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="91d26-133">-SASRule</span><span class="sxs-lookup"><span data-stu-id="91d26-133">-SASRule</span></span>
<span data-ttu-id="91d26-134">Especifica o **objeto SharedAccessAuthorizationRuleAttributes** que contém informações de configuração para as novas regras.</span><span class="sxs-lookup"><span data-stu-id="91d26-134">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="91d26-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91d26-135">-Confirm</span></span>
<span data-ttu-id="91d26-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91d26-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91d26-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91d26-137">-WhatIf</span></span>
<span data-ttu-id="91d26-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="91d26-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91d26-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="91d26-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91d26-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91d26-140">CommonParameters</span></span>
<span data-ttu-id="91d26-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91d26-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91d26-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91d26-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91d26-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91d26-143">INPUTS</span></span>

### <span data-ttu-id="91d26-144">System.String</span><span class="sxs-lookup"><span data-stu-id="91d26-144">System.String</span></span>

## <span data-ttu-id="91d26-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="91d26-145">OUTPUTS</span></span>

### <span data-ttu-id="91d26-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="91d26-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="91d26-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="91d26-147">NOTES</span></span>

## <span data-ttu-id="91d26-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91d26-148">RELATED LINKS</span></span>

[<span data-ttu-id="91d26-149">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="91d26-149">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="91d26-150">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="91d26-150">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="91d26-151">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="91d26-151">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


