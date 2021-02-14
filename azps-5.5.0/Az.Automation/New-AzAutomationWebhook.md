---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
ms.openlocfilehash: 88881e9ca5869bc2f63f4cec7c3993facc2cb3f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116966"
---
# <span data-ttu-id="6f27f-101">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="6f27f-101">New-AzAutomationWebhook</span></span>

## <span data-ttu-id="6f27f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6f27f-102">SYNOPSIS</span></span>
<span data-ttu-id="6f27f-103">Cria um web browser para um manual de automação.</span><span class="sxs-lookup"><span data-stu-id="6f27f-103">Creates a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="6f27f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f27f-104">SYNTAX</span></span>

```
New-AzAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f27f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f27f-105">DESCRIPTION</span></span>
<span data-ttu-id="6f27f-106">O **cmdlet New-AzAutomationWebweb cria uma Webwebwebwebbook** para um livro de executar do Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="6f27f-106">The **New-AzAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>
<span data-ttu-id="6f27f-107">Salve a URL web url que este cmdlet retorna, pois não pode ser recuperada novamente.</span><span class="sxs-lookup"><span data-stu-id="6f27f-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="6f27f-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6f27f-108">EXAMPLES</span></span>

### <span data-ttu-id="6f27f-109">Exemplo 1: Criar um web browser</span><span class="sxs-lookup"><span data-stu-id="6f27f-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="6f27f-110">Esse comando cria uma webrecisão chamada Web browser06 para o livro de runbook chamado ContosoRunbook na conta automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="6f27f-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="6f27f-111">O comando armazena a web$Webhook variável.</span><span class="sxs-lookup"><span data-stu-id="6f27f-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="6f27f-112">A Webção está habilitada.</span><span class="sxs-lookup"><span data-stu-id="6f27f-112">The webhook is enabled.</span></span>
<span data-ttu-id="6f27f-113">O web browser expira no momento especificado.</span><span class="sxs-lookup"><span data-stu-id="6f27f-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="6f27f-114">Esse comando não fornece valores para parâmetros Web parameters.</span><span class="sxs-lookup"><span data-stu-id="6f27f-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="6f27f-115">Esse comando especifica o parâmetro *Forçar.*</span><span class="sxs-lookup"><span data-stu-id="6f27f-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="6f27f-116">Portanto, ele não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="6f27f-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="6f27f-117">Exemplo 2: Criar um web parameters com parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f27f-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="6f27f-118">O primeiro comando cria um dicionário de parâmetros e os armazena na variável $Params dados.</span><span class="sxs-lookup"><span data-stu-id="6f27f-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="6f27f-119">O segundo comando cria uma Webcounter chamada Web browser11 para o livro de runbook chamado ContosoRunbook na conta automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="6f27f-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="6f27f-120">O comando atribui os parâmetros em $Params à Web.</span><span class="sxs-lookup"><span data-stu-id="6f27f-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="6f27f-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f27f-121">PARAMETERS</span></span>

### <span data-ttu-id="6f27f-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6f27f-122">-AutomationAccountName</span></span>
<span data-ttu-id="6f27f-123">Especifica o nome de uma conta de Automação na qual este cmdlet cria um web browser.</span><span class="sxs-lookup"><span data-stu-id="6f27f-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="6f27f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f27f-124">-DefaultProfile</span></span>
<span data-ttu-id="6f27f-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="6f27f-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f27f-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6f27f-126">-ExpiryTime</span></span>
<span data-ttu-id="6f27f-127">Especifica o tempo de expiração para o webfique como um **objeto DateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="6f27f-127">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="6f27f-128">Você pode especificar uma cadeia de caracteres ou **um DateTime** que pode ser convertido em um **DateTimeOffset válido.**</span><span class="sxs-lookup"><span data-stu-id="6f27f-128">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f27f-129">-Forçar</span><span class="sxs-lookup"><span data-stu-id="6f27f-129">-Force</span></span>
<span data-ttu-id="6f27f-130">ps_force</span><span class="sxs-lookup"><span data-stu-id="6f27f-130">ps_force</span></span>

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

### <span data-ttu-id="6f27f-131">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="6f27f-131">-IsEnabled</span></span>
<span data-ttu-id="6f27f-132">Especifica se a Web browser está habilitada.</span><span class="sxs-lookup"><span data-stu-id="6f27f-132">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f27f-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="6f27f-133">-Name</span></span>
<span data-ttu-id="6f27f-134">Especifica um nome para o web browser.</span><span class="sxs-lookup"><span data-stu-id="6f27f-134">Specifies a name for the webhook.</span></span>

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

### <span data-ttu-id="6f27f-135">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f27f-135">-Parameters</span></span>
<span data-ttu-id="6f27f-136">Especifica um dicionário de pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="6f27f-136">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="6f27f-137">As chaves são os nomes dos parâmetros do livro de executar.</span><span class="sxs-lookup"><span data-stu-id="6f27f-137">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="6f27f-138">Os valores são os valores de parâmetros do runbook.</span><span class="sxs-lookup"><span data-stu-id="6f27f-138">The values are the runbook parameter values.</span></span>
<span data-ttu-id="6f27f-139">Quando o runbook é iniciado em resposta a um web browser, esses parâmetros são passados para o runbook.</span><span class="sxs-lookup"><span data-stu-id="6f27f-139">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f27f-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f27f-140">-ResourceGroupName</span></span>
<span data-ttu-id="6f27f-141">Especifica o nome do grupo de recursos para o qual este cmdlet cria uma webção.</span><span class="sxs-lookup"><span data-stu-id="6f27f-141">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="6f27f-142">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="6f27f-142">-RunbookName</span></span>
<span data-ttu-id="6f27f-143">Especifica o nome do livro de runbook a ser associado à webtareia.</span><span class="sxs-lookup"><span data-stu-id="6f27f-143">Specifies the name of the runbook to associate to the webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f27f-144">-RunOn</span><span class="sxs-lookup"><span data-stu-id="6f27f-144">-RunOn</span></span>
<span data-ttu-id="6f27f-145">Nome opcional do grupo de trabalhadores híbridos que deve executar o livro de execução</span><span class="sxs-lookup"><span data-stu-id="6f27f-145">Optional name of the hybrid worker group which should execute the runbook</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f27f-146">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6f27f-146">-Confirm</span></span>
<span data-ttu-id="6f27f-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f27f-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f27f-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f27f-148">-WhatIf</span></span>
<span data-ttu-id="6f27f-149">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6f27f-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f27f-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6f27f-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f27f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f27f-151">CommonParameters</span></span>
<span data-ttu-id="6f27f-152">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f27f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f27f-153">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f27f-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f27f-154">Entradas</span><span class="sxs-lookup"><span data-stu-id="6f27f-154">INPUTS</span></span>

### <span data-ttu-id="6f27f-155">System.String</span><span class="sxs-lookup"><span data-stu-id="6f27f-155">System.String</span></span>

### <span data-ttu-id="6f27f-156">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6f27f-156">System.Boolean</span></span>

### <span data-ttu-id="6f27f-157">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6f27f-157">System.DateTimeOffset</span></span>

## <span data-ttu-id="6f27f-158">Saídas</span><span class="sxs-lookup"><span data-stu-id="6f27f-158">OUTPUTS</span></span>

### <span data-ttu-id="6f27f-159">Microsoft.Azure.Commands.Automation.Model.Web browser</span><span class="sxs-lookup"><span data-stu-id="6f27f-159">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="6f27f-160">Notas</span><span class="sxs-lookup"><span data-stu-id="6f27f-160">NOTES</span></span>

## <span data-ttu-id="6f27f-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f27f-161">RELATED LINKS</span></span>

[<span data-ttu-id="6f27f-162">Get-AzAutomationWebweb</span><span class="sxs-lookup"><span data-stu-id="6f27f-162">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="6f27f-163">Remove-AzAutomationWebweb</span><span class="sxs-lookup"><span data-stu-id="6f27f-163">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="6f27f-164">Set-AzAutomationWebweb</span><span class="sxs-lookup"><span data-stu-id="6f27f-164">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


