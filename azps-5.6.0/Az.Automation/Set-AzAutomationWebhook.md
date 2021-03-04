---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 200cc0b6312940606bb4e75f576c60928a84b33f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892877"
---
# <span data-ttu-id="de27c-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="de27c-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="de27c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de27c-102">SYNOPSIS</span></span>
<span data-ttu-id="de27c-103">Modifica um webhook para um runbook de automação.</span><span class="sxs-lookup"><span data-stu-id="de27c-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="de27c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="de27c-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de27c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="de27c-105">DESCRIPTION</span></span>
<span data-ttu-id="de27c-106">O cmdlet **Set-AzAutomationWebhook** modifica um webhook para um runbook de Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="de27c-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="de27c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de27c-107">EXAMPLES</span></span>

### <span data-ttu-id="de27c-108">Exemplo 1: Desabilitar um webhook</span><span class="sxs-lookup"><span data-stu-id="de27c-108">Example 1: Disable a webhook</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="de27c-109">Este comando desabilita um webhook chamado Webhook01 na conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="de27c-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="de27c-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="de27c-110">Example 2</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn 'Windows'
```

<span data-ttu-id="de27c-111">Este comando define o valor de executar no webhook e força o runbook a ser executado em um grupo de Trabalhadores Híbridos chamado Windows.</span><span class="sxs-lookup"><span data-stu-id="de27c-111">This command sets the run on value for the webhook and forces the runbook to be run on a Hybrid Worker group called Windows.</span></span>

### <span data-ttu-id="de27c-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="de27c-112">Example 3</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn $null
```

<span data-ttu-id="de27c-113">Esse comando atualiza o valor de executar no webhook e força o runbook a ser executado em um trabalhador de runbook do Azure.</span><span class="sxs-lookup"><span data-stu-id="de27c-113">This command updates the run on value for the webhook and forces the runbook to be run on an Azure runbook worker.</span></span> 

## <span data-ttu-id="de27c-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="de27c-114">PARAMETERS</span></span>

### <span data-ttu-id="de27c-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="de27c-115">-AutomationAccountName</span></span>
<span data-ttu-id="de27c-116">Especifica o nome de uma conta de automação na qual esse cmdlet modifica um webhook.</span><span class="sxs-lookup"><span data-stu-id="de27c-116">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="de27c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de27c-117">-DefaultProfile</span></span>
<span data-ttu-id="de27c-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="de27c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de27c-119">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="de27c-119">-IsEnabled</span></span>
<span data-ttu-id="de27c-120">Especifica se o webhook está habilitado.</span><span class="sxs-lookup"><span data-stu-id="de27c-120">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de27c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="de27c-121">-Name</span></span>
<span data-ttu-id="de27c-122">Especifica um nome do webhook que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="de27c-122">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="de27c-123">-Parameters</span><span class="sxs-lookup"><span data-stu-id="de27c-123">-Parameters</span></span>
<span data-ttu-id="de27c-124">Especifica um dicionário de pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="de27c-124">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="de27c-125">As chaves são os nomes do parâmetro runbook.</span><span class="sxs-lookup"><span data-stu-id="de27c-125">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="de27c-126">Os valores são os valores do parâmetro runbook.</span><span class="sxs-lookup"><span data-stu-id="de27c-126">The values are the runbook parameter values.</span></span>
<span data-ttu-id="de27c-127">Quando o runbook é iniciado em resposta a um webhook, esses parâmetros são passados para o runbook.</span><span class="sxs-lookup"><span data-stu-id="de27c-127">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de27c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de27c-128">-ResourceGroupName</span></span>
<span data-ttu-id="de27c-129">Especifica o nome do grupo de recursos para o qual este cmdlet modifica um webhook.</span><span class="sxs-lookup"><span data-stu-id="de27c-129">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="de27c-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="de27c-130">-RunOn</span></span>
<span data-ttu-id="de27c-131">Nome opcional do agente híbrido que deve executar o runbook</span><span class="sxs-lookup"><span data-stu-id="de27c-131">Optional name of the hybrid agent which should execute the runbook</span></span>

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

### <span data-ttu-id="de27c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de27c-132">CommonParameters</span></span>
<span data-ttu-id="de27c-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de27c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de27c-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de27c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de27c-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="de27c-135">INPUTS</span></span>

### <span data-ttu-id="de27c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="de27c-136">System.String</span></span>

### <span data-ttu-id="de27c-137">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="de27c-137">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="de27c-138">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="de27c-138">System.Collections.IDictionary</span></span>

## <span data-ttu-id="de27c-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="de27c-139">OUTPUTS</span></span>

### <span data-ttu-id="de27c-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="de27c-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="de27c-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="de27c-141">NOTES</span></span>

## <span data-ttu-id="de27c-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de27c-142">RELATED LINKS</span></span>

[<span data-ttu-id="de27c-143">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="de27c-143">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="de27c-144">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="de27c-144">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="de27c-145">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="de27c-145">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)


