---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
ms.openlocfilehash: f1062f1e827e27ff891f5b2797fcda95e60f3427
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431827"
---
# <span data-ttu-id="2c3ea-101">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="2c3ea-101">New-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="2c3ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c3ea-102">SYNOPSIS</span></span>
<span data-ttu-id="2c3ea-103">Cria um webhook para um runbook de automação.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-103">Creates a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c3ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c3ea-104">SYNTAX</span></span>

```
New-AzureRmAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c3ea-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2c3ea-105">DESCRIPTION</span></span>
<span data-ttu-id="2c3ea-106">O cmdlet **New-AzureRmAutomationWebhook** cria um webhook para um runbook de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-106">The **New-AzureRmAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>

<span data-ttu-id="2c3ea-107">Certifique-se de salvar a URL do webhook que esse cmdlet retorna, porque não é possível recuperá-lo novamente.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="2c3ea-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c3ea-108">EXAMPLES</span></span>

### <span data-ttu-id="2c3ea-109">Exemplo 1: criar um webhook</span><span class="sxs-lookup"><span data-stu-id="2c3ea-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzureRmAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="2c3ea-110">Esse comando cria um webhook chamado Webhook06 para o runbook chamado ContosoRunbook na conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="2c3ea-111">O comando armazena o webhook na variável $Webhook.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="2c3ea-112">O webhook está habilitado.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-112">The webhook is enabled.</span></span>
<span data-ttu-id="2c3ea-113">O webhook expira na hora especificada.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="2c3ea-114">Esse comando não fornece valores para parâmetros de webhook.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="2c3ea-115">Esse comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="2c3ea-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="2c3ea-116">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="2c3ea-117">Exemplo 2: criar um webhook com parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c3ea-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzureRmAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="2c3ea-118">O primeiro comando cria um dicionário de parâmetros e os armazena na variável $Params.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>

<span data-ttu-id="2c3ea-119">O segundo comando cria um webhook chamado Webhook11 para o runbook chamado ContosoRunbook na conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="2c3ea-120">O comando atribui os parâmetros em $Params ao webhook.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="2c3ea-121">OS</span><span class="sxs-lookup"><span data-stu-id="2c3ea-121">PARAMETERS</span></span>

### <span data-ttu-id="2c3ea-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2c3ea-122">-AutomationAccountName</span></span>
<span data-ttu-id="2c3ea-123">Especifica o nome de uma conta de automação na qual esse cmdlet cria um webhook.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="2c3ea-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2c3ea-124">-ExpiryTime</span></span>
<span data-ttu-id="2c3ea-125">Especifica o tempo de expiração do webhook como um objeto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="2c3ea-125">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="2c3ea-126">Você pode especificar uma cadeia de caracteres ou um **DateTime** que possa ser convertido em um **DateTimeOffset** válido.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-126">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="2c3ea-127">-Force</span><span class="sxs-lookup"><span data-stu-id="2c3ea-127">-Force</span></span>
<span data-ttu-id="2c3ea-128">ps_force</span><span class="sxs-lookup"><span data-stu-id="2c3ea-128">ps_force</span></span>

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

### <span data-ttu-id="2c3ea-129">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="2c3ea-129">-IsEnabled</span></span>
<span data-ttu-id="2c3ea-130">Especifica se o webhook está habilitado.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-130">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="2c3ea-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="2c3ea-131">-Name</span></span>
<span data-ttu-id="2c3ea-132">Especifica um nome para o webhook.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-132">Specifies a name for the webhook.</span></span>

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

### <span data-ttu-id="2c3ea-133">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c3ea-133">-Parameters</span></span>
<span data-ttu-id="2c3ea-134">Especifica um dicionário de pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-134">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="2c3ea-135">As chaves são os nomes de parâmetro do runbook.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-135">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="2c3ea-136">Os valores são os valores de parâmetro do runbook.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-136">The values are the runbook parameter values.</span></span>
<span data-ttu-id="2c3ea-137">Quando o runbook é iniciado em resposta a um webhook, esses parâmetros são passados para o runbook.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-137">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="2c3ea-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c3ea-138">-ResourceGroupName</span></span>
<span data-ttu-id="2c3ea-139">Especifica o nome do grupo de recursos para o qual esse cmdlet cria um webhook.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-139">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="2c3ea-140">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="2c3ea-140">-RunbookName</span></span>
<span data-ttu-id="2c3ea-141">Especifica o nome do runbook a ser associado ao webhook.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-141">Specifies the name of the runbook to associate to the webhook.</span></span>

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

### <span data-ttu-id="2c3ea-142">-RunOn</span><span class="sxs-lookup"><span data-stu-id="2c3ea-142">-RunOn</span></span>
<span data-ttu-id="2c3ea-143">Nome opcional do agente híbrido que deve executar o runbook</span><span class="sxs-lookup"><span data-stu-id="2c3ea-143">Optional name of the hybrid agent which should execute the runbook</span></span>

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

### <span data-ttu-id="2c3ea-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2c3ea-144">-Confirm</span></span>
<span data-ttu-id="2c3ea-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c3ea-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c3ea-146">-WhatIf</span></span>
<span data-ttu-id="2c3ea-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c3ea-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c3ea-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c3ea-149">-DefaultProfile</span></span>
<span data-ttu-id="2c3ea-150">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c3ea-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c3ea-151">CommonParameters</span></span>
<span data-ttu-id="2c3ea-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c3ea-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c3ea-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c3ea-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c3ea-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2c3ea-154">INPUTS</span></span>

## <span data-ttu-id="2c3ea-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2c3ea-155">OUTPUTS</span></span>

### <span data-ttu-id="2c3ea-156">Microsoft. Azure. Commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="2c3ea-156">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="2c3ea-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2c3ea-157">NOTES</span></span>

## <span data-ttu-id="2c3ea-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c3ea-158">RELATED LINKS</span></span>

[<span data-ttu-id="2c3ea-159">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="2c3ea-159">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="2c3ea-160">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="2c3ea-160">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)

[<span data-ttu-id="2c3ea-161">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="2c3ea-161">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


