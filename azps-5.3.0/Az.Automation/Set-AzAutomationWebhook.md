---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 0c1f2e5135596dd0911b02414d35b15c824b7936
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430558"
---
# <span data-ttu-id="05321-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="05321-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="05321-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="05321-102">SYNOPSIS</span></span>
<span data-ttu-id="05321-103">Modifica um webhook para um runbook de automação.</span><span class="sxs-lookup"><span data-stu-id="05321-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="05321-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05321-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05321-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="05321-105">DESCRIPTION</span></span>
<span data-ttu-id="05321-106">O cmdlet **set-AzAutomationWebhook** modifica um webhook para um runbook de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="05321-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="05321-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="05321-107">EXAMPLES</span></span>

### <span data-ttu-id="05321-108">Exemplo 1: desabilitar um webhook</span><span class="sxs-lookup"><span data-stu-id="05321-108">Example 1: Disable a webhook</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="05321-109">Esse comando desabilita um webhook chamado Webhook01 na conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="05321-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="05321-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="05321-110">Example 2</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn 'Windows'
```

<span data-ttu-id="05321-111">Esse comando define o valor Run on para o webhook e força o runbook a ser executado em um grupo de trabalho híbrido chamado Windows.</span><span class="sxs-lookup"><span data-stu-id="05321-111">This command sets the run on value for the webhook and forces the runbook to be run on a Hybrid Worker group called Windows.</span></span>

### <span data-ttu-id="05321-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="05321-112">Example 3</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn $null
```

<span data-ttu-id="05321-113">Esse comando atualiza o valor Run on para o webhook e força o runbook a ser executado em um trabalhador do runbook do Azure.</span><span class="sxs-lookup"><span data-stu-id="05321-113">This command updates the run on value for the webhook and forces the runbook to be run on an Azure runbook worker.</span></span> 

## <span data-ttu-id="05321-114">OS</span><span class="sxs-lookup"><span data-stu-id="05321-114">PARAMETERS</span></span>

### <span data-ttu-id="05321-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="05321-115">-AutomationAccountName</span></span>
<span data-ttu-id="05321-116">Especifica o nome de uma conta de automação na qual esse cmdlet modifica um webhook.</span><span class="sxs-lookup"><span data-stu-id="05321-116">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="05321-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05321-117">-DefaultProfile</span></span>
<span data-ttu-id="05321-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="05321-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05321-119">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="05321-119">-IsEnabled</span></span>
<span data-ttu-id="05321-120">Especifica se o webhook está habilitado.</span><span class="sxs-lookup"><span data-stu-id="05321-120">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="05321-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="05321-121">-Name</span></span>
<span data-ttu-id="05321-122">Especifica um nome do webhook que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="05321-122">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="05321-123">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05321-123">-Parameters</span></span>
<span data-ttu-id="05321-124">Especifica um dicionário de pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="05321-124">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="05321-125">As chaves são os nomes de parâmetro do runbook.</span><span class="sxs-lookup"><span data-stu-id="05321-125">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="05321-126">Os valores são os valores de parâmetro do runbook.</span><span class="sxs-lookup"><span data-stu-id="05321-126">The values are the runbook parameter values.</span></span>
<span data-ttu-id="05321-127">Quando o runbook é iniciado em resposta a um webhook, esses parâmetros são passados para o runbook.</span><span class="sxs-lookup"><span data-stu-id="05321-127">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="05321-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05321-128">-ResourceGroupName</span></span>
<span data-ttu-id="05321-129">Especifica o nome do grupo de recursos para o qual esse cmdlet modifica um webhook.</span><span class="sxs-lookup"><span data-stu-id="05321-129">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="05321-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="05321-130">-RunOn</span></span>
<span data-ttu-id="05321-131">Nome opcional do agente híbrido que deve executar o runbook</span><span class="sxs-lookup"><span data-stu-id="05321-131">Optional name of the hybrid agent which should execute the runbook</span></span>

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

### <span data-ttu-id="05321-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05321-132">CommonParameters</span></span>
<span data-ttu-id="05321-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05321-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05321-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05321-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05321-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="05321-135">INPUTS</span></span>

### <span data-ttu-id="05321-136">System. String</span><span class="sxs-lookup"><span data-stu-id="05321-136">System.String</span></span>

### <span data-ttu-id="05321-137">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="05321-137">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="05321-138">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="05321-138">System.Collections.IDictionary</span></span>

## <span data-ttu-id="05321-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="05321-139">OUTPUTS</span></span>

### <span data-ttu-id="05321-140">Microsoft. Azure. Commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="05321-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="05321-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="05321-141">NOTES</span></span>

## <span data-ttu-id="05321-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05321-142">RELATED LINKS</span></span>

[<span data-ttu-id="05321-143">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="05321-143">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="05321-144">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="05321-144">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="05321-145">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="05321-145">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)


