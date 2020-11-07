---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: e795f54fbcd31a8035e892a545b4afa1c2283366
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775728"
---
# <span data-ttu-id="8d8c7-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="8d8c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d8c7-102">SYNOPSIS</span></span>
<span data-ttu-id="8d8c7-103">Cria um novo receptor de grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="8d8c7-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="8d8c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d8c7-104">SYNTAX</span></span>

### <span data-ttu-id="8d8c7-105">NewEmailReceiver (padrão)</span><span class="sxs-lookup"><span data-stu-id="8d8c7-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d8c7-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d8c7-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d8c7-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d8c7-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d8c7-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d8c7-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d8c7-112">NewLogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d8c7-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d8c7-114">NewAzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d8c7-115">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8d8c7-115">DESCRIPTION</span></span>
<span data-ttu-id="8d8c7-116">O cmdlet **New-AzActionGroupReceiver** cria um novo receptor de grupo de ação na memória.</span><span class="sxs-lookup"><span data-stu-id="8d8c7-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="8d8c7-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d8c7-117">EXAMPLES</span></span>

### <span data-ttu-id="8d8c7-118">Exemplo 1: criar um novo receptor de email na memória.</span><span class="sxs-lookup"><span data-stu-id="8d8c7-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="8d8c7-119">Esse comando cria um novo receptor de email na memória.</span><span class="sxs-lookup"><span data-stu-id="8d8c7-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="8d8c7-120">Exemplo 2: criar um novo receptor de SMS na memória.</span><span class="sxs-lookup"><span data-stu-id="8d8c7-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="8d8c7-121">Esse comando cria um novo receptor de SMS na memória.</span><span class="sxs-lookup"><span data-stu-id="8d8c7-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="8d8c7-122">Exemplo 3: criar um novo receptor de webhook na memória.</span><span class="sxs-lookup"><span data-stu-id="8d8c7-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="8d8c7-123">Esse comando cria um novo receptor de webhook na memória.</span><span class="sxs-lookup"><span data-stu-id="8d8c7-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="8d8c7-124">OS</span><span class="sxs-lookup"><span data-stu-id="8d8c7-124">PARAMETERS</span></span>

### <span data-ttu-id="8d8c7-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="8d8c7-126">Criar uma ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-126">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="8d8c7-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="8d8c7-127">-AutomationAccountId</span></span>
<span data-ttu-id="8d8c7-128">o AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="8d8c7-128">the AutomationAccountId</span></span>

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

### <span data-ttu-id="8d8c7-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="8d8c7-130">Criar uma AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-130">Create a AutomationRunbookReceiver</span></span>

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

### <span data-ttu-id="8d8c7-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="8d8c7-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="8d8c7-132">o URI onde WebHooks devem ser enviados</span><span class="sxs-lookup"><span data-stu-id="8d8c7-132">the URI where webhooks should be sent</span></span>

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

### <span data-ttu-id="8d8c7-133">-AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="8d8c7-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="8d8c7-134">o AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="8d8c7-134">the AzureAppPushEmailAddress</span></span>

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

### <span data-ttu-id="8d8c7-135">-AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="8d8c7-136">Criar uma AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-136">Create a AzureAppPushReceiver</span></span>

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

### <span data-ttu-id="8d8c7-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="8d8c7-138">Criar uma ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-138">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="8d8c7-139">-CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="8d8c7-139">-CallbackUrl</span></span>
<span data-ttu-id="8d8c7-140">o CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="8d8c7-140">the CallbackUrl</span></span>

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

### <span data-ttu-id="8d8c7-141">-ConnectionID</span><span class="sxs-lookup"><span data-stu-id="8d8c7-141">-ConnectionId</span></span>
<span data-ttu-id="8d8c7-142">a ID de conexão do ITSM deste receptor</span><span class="sxs-lookup"><span data-stu-id="8d8c7-142">the itsm connection id of this receiver</span></span>

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

### <span data-ttu-id="8d8c7-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="8d8c7-143">-CountryCode</span></span>
<span data-ttu-id="8d8c7-144">Especifica o código de país para o receptor de SMS.</span><span class="sxs-lookup"><span data-stu-id="8d8c7-144">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="8d8c7-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d8c7-145">-DefaultProfile</span></span>
<span data-ttu-id="8d8c7-146">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8d8c7-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d8c7-147">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="8d8c7-147">-EmailAddress</span></span>
<span data-ttu-id="8d8c7-148">Especifica o endereço do receptor de email.</span><span class="sxs-lookup"><span data-stu-id="8d8c7-148">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="8d8c7-149">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-149">-EmailReceiver</span></span>
<span data-ttu-id="8d8c7-150">Especifica a criação de um receptor de email</span><span class="sxs-lookup"><span data-stu-id="8d8c7-150">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="8d8c7-151">-FunctionAppResourceId</span><span class="sxs-lookup"><span data-stu-id="8d8c7-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="8d8c7-152">a função ResourceId do App</span><span class="sxs-lookup"><span data-stu-id="8d8c7-152">the function app resourceId</span></span>

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

### <span data-ttu-id="8d8c7-153">-FunctionName</span><span class="sxs-lookup"><span data-stu-id="8d8c7-153">-FunctionName</span></span>
<span data-ttu-id="8d8c7-154">o FunctionName</span><span class="sxs-lookup"><span data-stu-id="8d8c7-154">the functionName</span></span>

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

### <span data-ttu-id="8d8c7-155">-HttpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="8d8c7-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="8d8c7-156">o httpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="8d8c7-156">the httpTriggerUrl</span></span>

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

### <span data-ttu-id="8d8c7-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="8d8c7-157">-IdentifierUri</span></span>
<span data-ttu-id="8d8c7-158">o URI do identificador para o AAD auth</span><span class="sxs-lookup"><span data-stu-id="8d8c7-158">the Identifier uri for aad auth</span></span>

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

### <span data-ttu-id="8d8c7-159">-IsGlobalRunbook</span><span class="sxs-lookup"><span data-stu-id="8d8c7-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="8d8c7-160">indicando se a instância é global runbook</span><span class="sxs-lookup"><span data-stu-id="8d8c7-160">indicating whether this instance is global runbook</span></span>

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

### <span data-ttu-id="8d8c7-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-161">-ItsmReceiver</span></span>
<span data-ttu-id="8d8c7-162">Criar uma ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-162">Create a ItsmReceiver</span></span>

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

### <span data-ttu-id="8d8c7-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-163">-LogicAppReceiver</span></span>
<span data-ttu-id="8d8c7-164">Criar uma LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-164">Create a LogicAppReceiver</span></span>

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

### <span data-ttu-id="8d8c7-165">-Nome</span><span class="sxs-lookup"><span data-stu-id="8d8c7-165">-Name</span></span>
<span data-ttu-id="8d8c7-166">Especifica o nome do destinatário.</span><span class="sxs-lookup"><span data-stu-id="8d8c7-166">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="8d8c7-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8d8c7-167">-ObjectId</span></span>
<span data-ttu-id="8d8c7-168">a ID do objeto do aplicativo webhook para autenticação do AAD</span><span class="sxs-lookup"><span data-stu-id="8d8c7-168">the webhook app object Id for aad auth</span></span>

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

### <span data-ttu-id="8d8c7-169">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="8d8c7-169">-PhoneNumber</span></span>
<span data-ttu-id="8d8c7-170">Especifica o número de telefone do receptor de SMS.</span><span class="sxs-lookup"><span data-stu-id="8d8c7-170">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="8d8c7-171">-Região</span><span class="sxs-lookup"><span data-stu-id="8d8c7-171">-Region</span></span>
<span data-ttu-id="8d8c7-172">a região do ITSM deste receptor</span><span class="sxs-lookup"><span data-stu-id="8d8c7-172">the itsm Region of this receiver</span></span>

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

### <span data-ttu-id="8d8c7-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d8c7-173">-ResourceId</span></span>
<span data-ttu-id="8d8c7-174">a ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d8c7-174">the ResourceId</span></span>

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

### <span data-ttu-id="8d8c7-175">-RoleID</span><span class="sxs-lookup"><span data-stu-id="8d8c7-175">-RoleId</span></span>
<span data-ttu-id="8d8c7-176">A ID da função ARM do receptor</span><span class="sxs-lookup"><span data-stu-id="8d8c7-176">The arm role id of the receiver</span></span>

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

### <span data-ttu-id="8d8c7-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="8d8c7-177">-RunbookName</span></span>
<span data-ttu-id="8d8c7-178">o RunbookName</span><span class="sxs-lookup"><span data-stu-id="8d8c7-178">the RunbookName</span></span>

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

### <span data-ttu-id="8d8c7-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="8d8c7-179">-ServiceUri</span></span>
<span data-ttu-id="8d8c7-180">Especifica o URI para o receptor de webhook.</span><span class="sxs-lookup"><span data-stu-id="8d8c7-180">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="8d8c7-181">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-181">-SmsReceiver</span></span>
<span data-ttu-id="8d8c7-182">Especifica a criação de um receptor de SMS</span><span class="sxs-lookup"><span data-stu-id="8d8c7-182">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="8d8c7-183">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="8d8c7-183">-TenantId</span></span>
<span data-ttu-id="8d8c7-184">a ID do locatário para autenticação do AAD</span><span class="sxs-lookup"><span data-stu-id="8d8c7-184">the tenant id for aad auth</span></span>

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

### <span data-ttu-id="8d8c7-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d8c7-185">-TicketConfiguration</span></span>
<span data-ttu-id="8d8c7-186">o ITSM TicketConfiguration deste receptor</span><span class="sxs-lookup"><span data-stu-id="8d8c7-186">the itsm TicketConfiguration of this receiver</span></span>

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

### <span data-ttu-id="8d8c7-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="8d8c7-187">-UseAadAuth</span></span>
<span data-ttu-id="8d8c7-188">o sinalizador para usar adicionar autenticação</span><span class="sxs-lookup"><span data-stu-id="8d8c7-188">the flag to use add auth</span></span>

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

### <span data-ttu-id="8d8c7-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="8d8c7-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="8d8c7-190">O sinalizador se deve ser usado o esquema de alerta comum.</span><span class="sxs-lookup"><span data-stu-id="8d8c7-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="8d8c7-191">Esse valor será neglectedfor SMS, Azure app Push, ITSM e Voice recievers.</span><span class="sxs-lookup"><span data-stu-id="8d8c7-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

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

### <span data-ttu-id="8d8c7-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="8d8c7-192">-VoiceCountryCode</span></span>
<span data-ttu-id="8d8c7-193">O código de país do receptor de voz</span><span class="sxs-lookup"><span data-stu-id="8d8c7-193">The country code of the voice receiver</span></span>

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

### <span data-ttu-id="8d8c7-194">-VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="8d8c7-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="8d8c7-195">O número de telefone do receptor de voz</span><span class="sxs-lookup"><span data-stu-id="8d8c7-195">The phone number of the voice receiver</span></span>

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

### <span data-ttu-id="8d8c7-196">-VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-196">-VoiceReceiver</span></span>
<span data-ttu-id="8d8c7-197">Criar um receptor de voz</span><span class="sxs-lookup"><span data-stu-id="8d8c7-197">Create a voice receiver</span></span>

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

### <span data-ttu-id="8d8c7-198">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="8d8c7-198">-WebhookReceiver</span></span>
<span data-ttu-id="8d8c7-199">Especifica a criação de um receptor de webhook</span><span class="sxs-lookup"><span data-stu-id="8d8c7-199">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="8d8c7-200">-WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="8d8c7-200">-WebhookResourceId</span></span>
<span data-ttu-id="8d8c7-201">o WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="8d8c7-201">the WebhookResourceId</span></span>

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

### <span data-ttu-id="8d8c7-202">-Workspaceid</span><span class="sxs-lookup"><span data-stu-id="8d8c7-202">-WorkspaceId</span></span>
<span data-ttu-id="8d8c7-203">a ID do espaço de trabalho do ITSM deste receptor</span><span class="sxs-lookup"><span data-stu-id="8d8c7-203">the itsm workspace id of this receiver</span></span>

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

### <span data-ttu-id="8d8c7-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d8c7-204">CommonParameters</span></span>
<span data-ttu-id="8d8c7-205">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d8c7-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d8c7-206">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d8c7-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d8c7-207">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8d8c7-207">INPUTS</span></span>

### <span data-ttu-id="8d8c7-208">System. String</span><span class="sxs-lookup"><span data-stu-id="8d8c7-208">System.String</span></span>

### <span data-ttu-id="8d8c7-209">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8d8c7-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8d8c7-210">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8d8c7-210">OUTPUTS</span></span>

### <span data-ttu-id="8d8c7-211">Microsoft. Azure. Commands. insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="8d8c7-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="8d8c7-212">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8d8c7-212">NOTES</span></span>

## <span data-ttu-id="8d8c7-213">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d8c7-213">RELATED LINKS</span></span>

<span data-ttu-id="8d8c7-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="8d8c7-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>