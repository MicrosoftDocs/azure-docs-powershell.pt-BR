---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
ms.openlocfilehash: 88881e9ca5869bc2f63f4cec7c3993facc2cb3f6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944951"
---
# <span data-ttu-id="761f0-101">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="761f0-101">New-AzAutomationWebhook</span></span>

## <span data-ttu-id="761f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="761f0-102">SYNOPSIS</span></span>
<span data-ttu-id="761f0-103">Cria um webhook para um runbook de automação.</span><span class="sxs-lookup"><span data-stu-id="761f0-103">Creates a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="761f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="761f0-104">SYNTAX</span></span>

```
New-AzAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="761f0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="761f0-105">DESCRIPTION</span></span>
<span data-ttu-id="761f0-106">O cmdlet **New-AzAutomationWebhook** cria um webhook para um runbook de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="761f0-106">The **New-AzAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>
<span data-ttu-id="761f0-107">Certifique-se de salvar a URL do webhook que esse cmdlet retorna, porque não é possível recuperá-lo novamente.</span><span class="sxs-lookup"><span data-stu-id="761f0-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="761f0-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="761f0-108">EXAMPLES</span></span>

### <span data-ttu-id="761f0-109">Exemplo 1: criar um webhook</span><span class="sxs-lookup"><span data-stu-id="761f0-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="761f0-110">Esse comando cria um webhook chamado Webhook06 para o runbook chamado ContosoRunbook na conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="761f0-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="761f0-111">O comando armazena o webhook na variável $Webhook.</span><span class="sxs-lookup"><span data-stu-id="761f0-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="761f0-112">O webhook está habilitado.</span><span class="sxs-lookup"><span data-stu-id="761f0-112">The webhook is enabled.</span></span>
<span data-ttu-id="761f0-113">O webhook expira na hora especificada.</span><span class="sxs-lookup"><span data-stu-id="761f0-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="761f0-114">Esse comando não fornece valores para parâmetros de webhook.</span><span class="sxs-lookup"><span data-stu-id="761f0-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="761f0-115">Esse comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="761f0-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="761f0-116">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="761f0-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="761f0-117">Exemplo 2: criar um webhook com parâmetros</span><span class="sxs-lookup"><span data-stu-id="761f0-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="761f0-118">O primeiro comando cria um dicionário de parâmetros e os armazena na variável $Params.</span><span class="sxs-lookup"><span data-stu-id="761f0-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="761f0-119">O segundo comando cria um webhook chamado Webhook11 para o runbook chamado ContosoRunbook na conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="761f0-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="761f0-120">O comando atribui os parâmetros em $Params ao webhook.</span><span class="sxs-lookup"><span data-stu-id="761f0-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="761f0-121">OS</span><span class="sxs-lookup"><span data-stu-id="761f0-121">PARAMETERS</span></span>

### <span data-ttu-id="761f0-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="761f0-122">-AutomationAccountName</span></span>
<span data-ttu-id="761f0-123">Especifica o nome de uma conta de automação na qual esse cmdlet cria um webhook.</span><span class="sxs-lookup"><span data-stu-id="761f0-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="761f0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="761f0-124">-DefaultProfile</span></span>
<span data-ttu-id="761f0-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="761f0-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="761f0-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="761f0-126">-ExpiryTime</span></span>
<span data-ttu-id="761f0-127">Especifica o tempo de expiração do webhook como um objeto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="761f0-127">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="761f0-128">Você pode especificar uma cadeia de caracteres ou um **DateTime** que possa ser convertido em um **DateTimeOffset** válido.</span><span class="sxs-lookup"><span data-stu-id="761f0-128">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="761f0-129">-Force</span><span class="sxs-lookup"><span data-stu-id="761f0-129">-Force</span></span>
<span data-ttu-id="761f0-130">ps_force</span><span class="sxs-lookup"><span data-stu-id="761f0-130">ps_force</span></span>

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

### <span data-ttu-id="761f0-131">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="761f0-131">-IsEnabled</span></span>
<span data-ttu-id="761f0-132">Especifica se o webhook está habilitado.</span><span class="sxs-lookup"><span data-stu-id="761f0-132">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="761f0-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="761f0-133">-Name</span></span>
<span data-ttu-id="761f0-134">Especifica um nome para o webhook.</span><span class="sxs-lookup"><span data-stu-id="761f0-134">Specifies a name for the webhook.</span></span>

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

### <span data-ttu-id="761f0-135">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="761f0-135">-Parameters</span></span>
<span data-ttu-id="761f0-136">Especifica um dicionário de pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="761f0-136">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="761f0-137">As chaves são os nomes de parâmetro do runbook.</span><span class="sxs-lookup"><span data-stu-id="761f0-137">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="761f0-138">Os valores são os valores de parâmetro do runbook.</span><span class="sxs-lookup"><span data-stu-id="761f0-138">The values are the runbook parameter values.</span></span>
<span data-ttu-id="761f0-139">Quando o runbook é iniciado em resposta a um webhook, esses parâmetros são passados para o runbook.</span><span class="sxs-lookup"><span data-stu-id="761f0-139">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="761f0-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="761f0-140">-ResourceGroupName</span></span>
<span data-ttu-id="761f0-141">Especifica o nome do grupo de recursos para o qual esse cmdlet cria um webhook.</span><span class="sxs-lookup"><span data-stu-id="761f0-141">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="761f0-142">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="761f0-142">-RunbookName</span></span>
<span data-ttu-id="761f0-143">Especifica o nome do runbook a ser associado ao webhook.</span><span class="sxs-lookup"><span data-stu-id="761f0-143">Specifies the name of the runbook to associate to the webhook.</span></span>

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

### <span data-ttu-id="761f0-144">-RunOn</span><span class="sxs-lookup"><span data-stu-id="761f0-144">-RunOn</span></span>
<span data-ttu-id="761f0-145">Nome opcional do grupo do Hybrid Worker que deve executar o runbook</span><span class="sxs-lookup"><span data-stu-id="761f0-145">Optional name of the hybrid worker group which should execute the runbook</span></span>

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

### <span data-ttu-id="761f0-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="761f0-146">-Confirm</span></span>
<span data-ttu-id="761f0-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="761f0-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="761f0-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="761f0-148">-WhatIf</span></span>
<span data-ttu-id="761f0-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="761f0-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="761f0-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="761f0-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="761f0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="761f0-151">CommonParameters</span></span>
<span data-ttu-id="761f0-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="761f0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="761f0-153">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="761f0-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="761f0-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="761f0-154">INPUTS</span></span>

### <span data-ttu-id="761f0-155">System. String</span><span class="sxs-lookup"><span data-stu-id="761f0-155">System.String</span></span>

### <span data-ttu-id="761f0-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="761f0-156">System.Boolean</span></span>

### <span data-ttu-id="761f0-157">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="761f0-157">System.DateTimeOffset</span></span>

## <span data-ttu-id="761f0-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="761f0-158">OUTPUTS</span></span>

### <span data-ttu-id="761f0-159">Microsoft. Azure. Commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="761f0-159">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="761f0-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="761f0-160">NOTES</span></span>

## <span data-ttu-id="761f0-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="761f0-161">RELATED LINKS</span></span>

[<span data-ttu-id="761f0-162">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="761f0-162">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="761f0-163">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="761f0-163">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="761f0-164">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="761f0-164">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


