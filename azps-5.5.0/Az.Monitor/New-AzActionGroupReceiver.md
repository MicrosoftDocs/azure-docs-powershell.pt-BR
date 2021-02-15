---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: f2862c08212f5e41de10cb600edb22c38eac68d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114769"
---
# <span data-ttu-id="72e8d-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="72e8d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="72e8d-102">SYNOPSIS</span></span>
<span data-ttu-id="72e8d-103">Cria um novo receptor de grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="72e8d-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="72e8d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72e8d-104">SYNTAX</span></span>

### <span data-ttu-id="72e8d-105">NewEmailReceiver (Padrão)</span><span class="sxs-lookup"><span data-stu-id="72e8d-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72e8d-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72e8d-107">NewWebwebwebreceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72e8d-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72e8d-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72e8d-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72e8d-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72e8d-112">New YorkAppReceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72e8d-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72e8d-114">NewAzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72e8d-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="72e8d-115">DESCRIPTION</span></span>
<span data-ttu-id="72e8d-116">O **cmdlet New-AzActionGroupReceiver** cria um novo receptor de grupo de ações na memória.</span><span class="sxs-lookup"><span data-stu-id="72e8d-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="72e8d-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="72e8d-117">EXAMPLES</span></span>

### <span data-ttu-id="72e8d-118">Exemplo 1: Criar um novo destinatário de email na memória.</span><span class="sxs-lookup"><span data-stu-id="72e8d-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="72e8d-119">Esse comando cria um novo receptor de email na memória.</span><span class="sxs-lookup"><span data-stu-id="72e8d-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="72e8d-120">Exemplo 2: Criar um novo receptor SMS na memória.</span><span class="sxs-lookup"><span data-stu-id="72e8d-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="72e8d-121">Esse comando cria um novo receptor SMS na memória.</span><span class="sxs-lookup"><span data-stu-id="72e8d-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="72e8d-122">Exemplo 3: Criar um novo receptor web receiver na memória.</span><span class="sxs-lookup"><span data-stu-id="72e8d-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="72e8d-123">Esse comando cria um novo receptor web receiver na memória.</span><span class="sxs-lookup"><span data-stu-id="72e8d-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="72e8d-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72e8d-124">PARAMETERS</span></span>

### <span data-ttu-id="72e8d-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="72e8d-126">Criar um ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-126">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="72e8d-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="72e8d-127">-AutomationAccountId</span></span>
<span data-ttu-id="72e8d-128">a AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="72e8d-128">the AutomationAccountId</span></span>

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

### <span data-ttu-id="72e8d-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="72e8d-130">Criar um AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-130">Create a AutomationRunbookReceiver</span></span>

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

### <span data-ttu-id="72e8d-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="72e8d-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="72e8d-132">o URI para o qual web browsers devem ser enviados</span><span class="sxs-lookup"><span data-stu-id="72e8d-132">the URI where webhooks should be sent</span></span>

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

### <span data-ttu-id="72e8d-133">-AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="72e8d-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="72e8d-134">o AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="72e8d-134">the AzureAppPushEmailAddress</span></span>

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

### <span data-ttu-id="72e8d-135">-AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="72e8d-136">Criar um AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-136">Create a AzureAppPushReceiver</span></span>

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

### <span data-ttu-id="72e8d-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="72e8d-138">Criar um ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-138">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="72e8d-139">-CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="72e8d-139">-CallbackUrl</span></span>
<span data-ttu-id="72e8d-140">o CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="72e8d-140">the CallbackUrl</span></span>

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

### <span data-ttu-id="72e8d-141">-ConnectionId</span><span class="sxs-lookup"><span data-stu-id="72e8d-141">-ConnectionId</span></span>
<span data-ttu-id="72e8d-142">a ID de conexão itsm deste receptor</span><span class="sxs-lookup"><span data-stu-id="72e8d-142">the itsm connection id of this receiver</span></span>

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

### <span data-ttu-id="72e8d-143">-CódigoDo País</span><span class="sxs-lookup"><span data-stu-id="72e8d-143">-CountryCode</span></span>
<span data-ttu-id="72e8d-144">Especifica o código do país para o receptor SMS.</span><span class="sxs-lookup"><span data-stu-id="72e8d-144">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="72e8d-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72e8d-145">-DefaultProfile</span></span>
<span data-ttu-id="72e8d-146">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="72e8d-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72e8d-147">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="72e8d-147">-EmailAddress</span></span>
<span data-ttu-id="72e8d-148">Especifica o endereço do destinatário de email.</span><span class="sxs-lookup"><span data-stu-id="72e8d-148">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="72e8d-149">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-149">-EmailReceiver</span></span>
<span data-ttu-id="72e8d-150">Especifica a criação de um destinatário de email</span><span class="sxs-lookup"><span data-stu-id="72e8d-150">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="72e8d-151">-FunctionAppResourceId</span><span class="sxs-lookup"><span data-stu-id="72e8d-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="72e8d-152">a função resourceId do aplicativo</span><span class="sxs-lookup"><span data-stu-id="72e8d-152">the function app resourceId</span></span>

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

### <span data-ttu-id="72e8d-153">-FunctionName</span><span class="sxs-lookup"><span data-stu-id="72e8d-153">-FunctionName</span></span>
<span data-ttu-id="72e8d-154">a funçãoName</span><span class="sxs-lookup"><span data-stu-id="72e8d-154">the functionName</span></span>

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

### <span data-ttu-id="72e8d-155">-HttpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="72e8d-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="72e8d-156">o httpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="72e8d-156">the httpTriggerUrl</span></span>

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

### <span data-ttu-id="72e8d-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="72e8d-157">-IdentifierUri</span></span>
<span data-ttu-id="72e8d-158">o uri identificador para aad auth</span><span class="sxs-lookup"><span data-stu-id="72e8d-158">the Identifier uri for aad auth</span></span>

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

### <span data-ttu-id="72e8d-159">-IsGlbalRunbook</span><span class="sxs-lookup"><span data-stu-id="72e8d-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="72e8d-160">indicando se essa instância é uma agenda de executar global</span><span class="sxs-lookup"><span data-stu-id="72e8d-160">indicating whether this instance is global runbook</span></span>

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

### <span data-ttu-id="72e8d-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-161">-ItsmReceiver</span></span>
<span data-ttu-id="72e8d-162">Criar uma ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-162">Create a ItsmReceiver</span></span>

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

### <span data-ttu-id="72e8d-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-163">-LogicAppReceiver</span></span>
<span data-ttu-id="72e8d-164">Criar um LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-164">Create a LogicAppReceiver</span></span>

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

### <span data-ttu-id="72e8d-165">-Nome</span><span class="sxs-lookup"><span data-stu-id="72e8d-165">-Name</span></span>
<span data-ttu-id="72e8d-166">Especifica o nome do receptor.</span><span class="sxs-lookup"><span data-stu-id="72e8d-166">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="72e8d-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="72e8d-167">-ObjectId</span></span>
<span data-ttu-id="72e8d-168">a ID do objeto do aplicativo Webção para aad auth</span><span class="sxs-lookup"><span data-stu-id="72e8d-168">the webhook app object Id for aad auth</span></span>

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

### <span data-ttu-id="72e8d-169">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="72e8d-169">-PhoneNumber</span></span>
<span data-ttu-id="72e8d-170">Especifica o número de telefone do receptor SMS.</span><span class="sxs-lookup"><span data-stu-id="72e8d-170">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="72e8d-171">-Região</span><span class="sxs-lookup"><span data-stu-id="72e8d-171">-Region</span></span>
<span data-ttu-id="72e8d-172">a região de itsm deste receptor</span><span class="sxs-lookup"><span data-stu-id="72e8d-172">the itsm Region of this receiver</span></span>

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

### <span data-ttu-id="72e8d-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72e8d-173">-ResourceId</span></span>
<span data-ttu-id="72e8d-174">a ResourceId</span><span class="sxs-lookup"><span data-stu-id="72e8d-174">the ResourceId</span></span>

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

### <span data-ttu-id="72e8d-175">-RoleId</span><span class="sxs-lookup"><span data-stu-id="72e8d-175">-RoleId</span></span>
<span data-ttu-id="72e8d-176">A ID de função de arm do receptor</span><span class="sxs-lookup"><span data-stu-id="72e8d-176">The arm role id of the receiver</span></span>

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

### <span data-ttu-id="72e8d-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="72e8d-177">-RunbookName</span></span>
<span data-ttu-id="72e8d-178">o RunbookName</span><span class="sxs-lookup"><span data-stu-id="72e8d-178">the RunbookName</span></span>

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

### <span data-ttu-id="72e8d-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="72e8d-179">-ServiceUri</span></span>
<span data-ttu-id="72e8d-180">Especifica o URI para o receptor web browser.</span><span class="sxs-lookup"><span data-stu-id="72e8d-180">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="72e8d-181">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-181">-SmsReceiver</span></span>
<span data-ttu-id="72e8d-182">Especifica a criação de um receptor SMS</span><span class="sxs-lookup"><span data-stu-id="72e8d-182">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="72e8d-183">-TenantId</span><span class="sxs-lookup"><span data-stu-id="72e8d-183">-TenantId</span></span>
<span data-ttu-id="72e8d-184">a ID do locatário para aad auth</span><span class="sxs-lookup"><span data-stu-id="72e8d-184">the tenant id for aad auth</span></span>

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

### <span data-ttu-id="72e8d-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="72e8d-185">-TicketConfiguration</span></span>
<span data-ttu-id="72e8d-186">a configuração itsm TicketConfiguration deste receptor</span><span class="sxs-lookup"><span data-stu-id="72e8d-186">the itsm TicketConfiguration of this receiver</span></span>

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

### <span data-ttu-id="72e8d-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="72e8d-187">-UseAadAuth</span></span>
<span data-ttu-id="72e8d-188">o sinalizador a ser usado adicionar auth</span><span class="sxs-lookup"><span data-stu-id="72e8d-188">the flag to use add auth</span></span>

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

### <span data-ttu-id="72e8d-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="72e8d-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="72e8d-190">O sinalizador se deve usar esquema de alerta comum.</span><span class="sxs-lookup"><span data-stu-id="72e8d-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="72e8d-191">Esse valor será negligenciado para SMS, push do aplicativo Azure, ITSM e Voice recievers.</span><span class="sxs-lookup"><span data-stu-id="72e8d-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

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

### <span data-ttu-id="72e8d-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="72e8d-192">-VoiceCountryCode</span></span>
<span data-ttu-id="72e8d-193">O código do país do receptor de voz</span><span class="sxs-lookup"><span data-stu-id="72e8d-193">The country code of the voice receiver</span></span>

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

### <span data-ttu-id="72e8d-194">-VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="72e8d-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="72e8d-195">O número de telefone do receptor de voz</span><span class="sxs-lookup"><span data-stu-id="72e8d-195">The phone number of the voice receiver</span></span>

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

### <span data-ttu-id="72e8d-196">-VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-196">-VoiceReceiver</span></span>
<span data-ttu-id="72e8d-197">Criar um receptor de voz</span><span class="sxs-lookup"><span data-stu-id="72e8d-197">Create a voice receiver</span></span>

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

### <span data-ttu-id="72e8d-198">-Webreceiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-198">-WebhookReceiver</span></span>
<span data-ttu-id="72e8d-199">Especifica a criação de um receptor web receiver</span><span class="sxs-lookup"><span data-stu-id="72e8d-199">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="72e8d-200">-WebourResourceId</span><span class="sxs-lookup"><span data-stu-id="72e8d-200">-WebhookResourceId</span></span>
<span data-ttu-id="72e8d-201">WebçãoResourceId</span><span class="sxs-lookup"><span data-stu-id="72e8d-201">the WebhookResourceId</span></span>

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

### <span data-ttu-id="72e8d-202">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="72e8d-202">-WorkspaceId</span></span>
<span data-ttu-id="72e8d-203">a ID do espaço de trabalho itsm deste receptor</span><span class="sxs-lookup"><span data-stu-id="72e8d-203">the itsm workspace id of this receiver</span></span>

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

### <span data-ttu-id="72e8d-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e8d-204">CommonParameters</span></span>
<span data-ttu-id="72e8d-205">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72e8d-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e8d-206">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72e8d-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e8d-207">Entradas</span><span class="sxs-lookup"><span data-stu-id="72e8d-207">INPUTS</span></span>

### <span data-ttu-id="72e8d-208">System.String</span><span class="sxs-lookup"><span data-stu-id="72e8d-208">System.String</span></span>

### <span data-ttu-id="72e8d-209">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="72e8d-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="72e8d-210">Saídas</span><span class="sxs-lookup"><span data-stu-id="72e8d-210">OUTPUTS</span></span>

### <span data-ttu-id="72e8d-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="72e8d-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="72e8d-212">Notas</span><span class="sxs-lookup"><span data-stu-id="72e8d-212">NOTES</span></span>

## <span data-ttu-id="72e8d-213">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72e8d-213">RELATED LINKS</span></span>

<span data-ttu-id="72e8d-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="72e8d-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
