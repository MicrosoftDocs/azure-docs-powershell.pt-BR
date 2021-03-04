---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: 917f6287c40d4c26123217cccbf1dfc11866a488
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888874"
---
# <span data-ttu-id="b3b97-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="b3b97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3b97-102">SYNOPSIS</span></span>
<span data-ttu-id="b3b97-103">Cria um novo receptor de grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="b3b97-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="b3b97-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b3b97-104">SYNTAX</span></span>

### <span data-ttu-id="b3b97-105">NewEmailReceiver (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b3b97-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b97-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b97-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b97-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b97-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b97-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b97-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b97-112">NewLogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b97-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b97-114">NewAzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3b97-115">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b3b97-115">DESCRIPTION</span></span>
<span data-ttu-id="b3b97-116">O cmdlet **New-AzActionGroupReceiver** cria um novo receptor de grupo de ações na memória.</span><span class="sxs-lookup"><span data-stu-id="b3b97-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="b3b97-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b3b97-117">EXAMPLES</span></span>

### <span data-ttu-id="b3b97-118">Exemplo 1: Criar um novo receptor de email na memória.</span><span class="sxs-lookup"><span data-stu-id="b3b97-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="b3b97-119">Este comando cria um novo receptor de email na memória.</span><span class="sxs-lookup"><span data-stu-id="b3b97-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="b3b97-120">Exemplo 2: Criar um novo receptor SMS na memória.</span><span class="sxs-lookup"><span data-stu-id="b3b97-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="b3b97-121">Este comando cria um novo receptor SMS na memória.</span><span class="sxs-lookup"><span data-stu-id="b3b97-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="b3b97-122">Exemplo 3: Criar um novo receptor de webhook na memória.</span><span class="sxs-lookup"><span data-stu-id="b3b97-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="b3b97-123">Este comando cria um novo receptor de webhook na memória.</span><span class="sxs-lookup"><span data-stu-id="b3b97-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="b3b97-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b3b97-124">PARAMETERS</span></span>

### <span data-ttu-id="b3b97-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="b3b97-126">Criar um ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-126">Create a ArmRoleReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewArmRoleReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="b3b97-127">-AutomationAccountId</span></span>
<span data-ttu-id="b3b97-128">automationAccountId</span><span class="sxs-lookup"><span data-stu-id="b3b97-128">the AutomationAccountId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="b3b97-130">Criar um AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-130">Create a AutomationRunbookReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="b3b97-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="b3b97-132">o URI onde webhooks devem ser enviados</span><span class="sxs-lookup"><span data-stu-id="b3b97-132">the URI where webhooks should be sent</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-133">-AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="b3b97-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="b3b97-134">the AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="b3b97-134">the AzureAppPushEmailAddress</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureAppPushReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-135">-AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="b3b97-136">Criar um AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-136">Create a AzureAppPushReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAzureAppPushReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="b3b97-138">Criar um ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-138">Create a ArmRoleReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-139">-CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="b3b97-139">-CallbackUrl</span></span>
<span data-ttu-id="b3b97-140">o CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="b3b97-140">the CallbackUrl</span></span>

```yaml
Type: System.String
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-141">-ConnectionId</span><span class="sxs-lookup"><span data-stu-id="b3b97-141">-ConnectionId</span></span>
<span data-ttu-id="b3b97-142">a id de conexão de itsm deste receptor</span><span class="sxs-lookup"><span data-stu-id="b3b97-142">the itsm connection id of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="b3b97-143">-CountryCode</span></span>
<span data-ttu-id="b3b97-144">Especifica o código do país para o receptor SMS.</span><span class="sxs-lookup"><span data-stu-id="b3b97-144">Specifies the country code for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3b97-145">-DefaultProfile</span></span>
<span data-ttu-id="b3b97-146">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b3b97-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3b97-147">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="b3b97-147">-EmailAddress</span></span>
<span data-ttu-id="b3b97-148">Especifica o endereço do receptor de email.</span><span class="sxs-lookup"><span data-stu-id="b3b97-148">Specifies the address for the Email receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewEmailReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-149">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-149">-EmailReceiver</span></span>
<span data-ttu-id="b3b97-150">Especifica a criação de um receptor de email</span><span class="sxs-lookup"><span data-stu-id="b3b97-150">Specifies to create an Email receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewEmailReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-151">-FunctionAppResourceId</span><span class="sxs-lookup"><span data-stu-id="b3b97-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="b3b97-152">resourceId do aplicativo de função</span><span class="sxs-lookup"><span data-stu-id="b3b97-152">the function app resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-153">-FunctionName</span><span class="sxs-lookup"><span data-stu-id="b3b97-153">-FunctionName</span></span>
<span data-ttu-id="b3b97-154">functionName</span><span class="sxs-lookup"><span data-stu-id="b3b97-154">the functionName</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-155">-HttpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="b3b97-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="b3b97-156">httpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="b3b97-156">the httpTriggerUrl</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="b3b97-157">-IdentifierUri</span></span>
<span data-ttu-id="b3b97-158">o uri identificador para aad auth</span><span class="sxs-lookup"><span data-stu-id="b3b97-158">the Identifier uri for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-159">-IsGlobalRunbook</span><span class="sxs-lookup"><span data-stu-id="b3b97-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="b3b97-160">indicando se essa instância é um runbook global</span><span class="sxs-lookup"><span data-stu-id="b3b97-160">indicating whether this instance is global runbook</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-161">-ItsmReceiver</span></span>
<span data-ttu-id="b3b97-162">Criar um ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-162">Create a ItsmReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewItsmReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-163">-LogicAppReceiver</span></span>
<span data-ttu-id="b3b97-164">Criar um LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-164">Create a LogicAppReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-165">-Name</span><span class="sxs-lookup"><span data-stu-id="b3b97-165">-Name</span></span>
<span data-ttu-id="b3b97-166">Especifica o nome do receptor.</span><span class="sxs-lookup"><span data-stu-id="b3b97-166">Specifies the name for the receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b3b97-167">-ObjectId</span></span>
<span data-ttu-id="b3b97-168">a ID do objeto do aplicativo webhook para aad auth</span><span class="sxs-lookup"><span data-stu-id="b3b97-168">the webhook app object Id for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-169">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="b3b97-169">-PhoneNumber</span></span>
<span data-ttu-id="b3b97-170">Especifica o número de telefone do receptor SMS.</span><span class="sxs-lookup"><span data-stu-id="b3b97-170">Specifies the phone number for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-171">-Region</span><span class="sxs-lookup"><span data-stu-id="b3b97-171">-Region</span></span>
<span data-ttu-id="b3b97-172">a região itsm deste receptor</span><span class="sxs-lookup"><span data-stu-id="b3b97-172">the itsm Region of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3b97-173">-ResourceId</span></span>
<span data-ttu-id="b3b97-174">resourceId</span><span class="sxs-lookup"><span data-stu-id="b3b97-174">the ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-175">-RoleId</span><span class="sxs-lookup"><span data-stu-id="b3b97-175">-RoleId</span></span>
<span data-ttu-id="b3b97-176">A id da função de braço do receptor</span><span class="sxs-lookup"><span data-stu-id="b3b97-176">The arm role id of the receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewArmRoleReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="b3b97-177">-RunbookName</span></span>
<span data-ttu-id="b3b97-178">o RunbookName</span><span class="sxs-lookup"><span data-stu-id="b3b97-178">the RunbookName</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="b3b97-179">-ServiceUri</span></span>
<span data-ttu-id="b3b97-180">Especifica o URI do receptor de webhook.</span><span class="sxs-lookup"><span data-stu-id="b3b97-180">Specifies the URI for the webhook receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-181">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-181">-SmsReceiver</span></span>
<span data-ttu-id="b3b97-182">Especifica a criação de um receptor SMS</span><span class="sxs-lookup"><span data-stu-id="b3b97-182">Specifies to create a SMS receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-183">-TenantId</span><span class="sxs-lookup"><span data-stu-id="b3b97-183">-TenantId</span></span>
<span data-ttu-id="b3b97-184">a id de locatário para aad auth</span><span class="sxs-lookup"><span data-stu-id="b3b97-184">the tenant id for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3b97-185">-TicketConfiguration</span></span>
<span data-ttu-id="b3b97-186">o itsm TicketConfiguration deste receptor</span><span class="sxs-lookup"><span data-stu-id="b3b97-186">the itsm TicketConfiguration of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="b3b97-187">-UseAadAuth</span></span>
<span data-ttu-id="b3b97-188">o sinalizador a ser usado add auth</span><span class="sxs-lookup"><span data-stu-id="b3b97-188">the flag to use add auth</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="b3b97-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="b3b97-190">O sinalizador se deve usar o esquema de alerta comum .</span><span class="sxs-lookup"><span data-stu-id="b3b97-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="b3b97-191">Esse valor será negligenciadopara SMS, push do Aplicativo do Azure, ITSM e Recievers do Voice.</span><span class="sxs-lookup"><span data-stu-id="b3b97-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="b3b97-192">-VoiceCountryCode</span></span>
<span data-ttu-id="b3b97-193">O código de país do receptor de voz</span><span class="sxs-lookup"><span data-stu-id="b3b97-193">The country code of the voice receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewVoiceReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-194">-VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="b3b97-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="b3b97-195">O número de telefone do receptor de voz</span><span class="sxs-lookup"><span data-stu-id="b3b97-195">The phone number of the voice receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewVoiceReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-196">-VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-196">-VoiceReceiver</span></span>
<span data-ttu-id="b3b97-197">Criar um receptor de voz</span><span class="sxs-lookup"><span data-stu-id="b3b97-197">Create a voice receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewVoiceReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-198">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="b3b97-198">-WebhookReceiver</span></span>
<span data-ttu-id="b3b97-199">Especifica a criação de um receptor de webhook</span><span class="sxs-lookup"><span data-stu-id="b3b97-199">Specifies to create a webhook receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-200">-WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="b3b97-200">-WebhookResourceId</span></span>
<span data-ttu-id="b3b97-201">webhookResourceId</span><span class="sxs-lookup"><span data-stu-id="b3b97-201">the WebhookResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-202">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="b3b97-202">-WorkspaceId</span></span>
<span data-ttu-id="b3b97-203">a id do espaço de trabalho itsm deste receptor</span><span class="sxs-lookup"><span data-stu-id="b3b97-203">the itsm workspace id of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b97-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3b97-204">CommonParameters</span></span>
<span data-ttu-id="b3b97-205">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3b97-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3b97-206">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3b97-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3b97-207">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3b97-207">INPUTS</span></span>

### <span data-ttu-id="b3b97-208">System.String</span><span class="sxs-lookup"><span data-stu-id="b3b97-208">System.String</span></span>

### <span data-ttu-id="b3b97-209">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b3b97-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b3b97-210">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b3b97-210">OUTPUTS</span></span>

### <span data-ttu-id="b3b97-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="b3b97-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="b3b97-212">NOTES</span><span class="sxs-lookup"><span data-stu-id="b3b97-212">NOTES</span></span>

## <span data-ttu-id="b3b97-213">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3b97-213">RELATED LINKS</span></span>

<span data-ttu-id="b3b97-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="b3b97-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
