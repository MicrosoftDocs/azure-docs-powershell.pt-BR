---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
ms.openlocfilehash: 13eeb70905225b89cfc362a13425ec77e0ef9521
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117992"
---
# <span data-ttu-id="da0de-101">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="da0de-101">Remove-AzAutomationWebhook</span></span>

## <span data-ttu-id="da0de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da0de-102">SYNOPSIS</span></span>
<span data-ttu-id="da0de-103">Remove um web browser de um manual de automação.</span><span class="sxs-lookup"><span data-stu-id="da0de-103">Removes a webhook from an Automation runbook.</span></span>

## <span data-ttu-id="da0de-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da0de-104">SYNTAX</span></span>

```
Remove-AzAutomationWebhook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da0de-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="da0de-105">DESCRIPTION</span></span>
<span data-ttu-id="da0de-106">O cmdlet **Remove-AzAutomationWebweb remove um webwebwebaut** de um livro de aplicação de Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="da0de-106">The **Remove-AzAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="da0de-107">O web browser é excluído.</span><span class="sxs-lookup"><span data-stu-id="da0de-107">The webhook is deleted.</span></span>

## <span data-ttu-id="da0de-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="da0de-108">EXAMPLES</span></span>

### <span data-ttu-id="da0de-109">Exemplo 1: Remover um web browser</span><span class="sxs-lookup"><span data-stu-id="da0de-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="da0de-110">Esse comando remove um webrecisão chamado Web browser11 na conta automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="da0de-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="da0de-111">O comando especifica o parâmetro *Forçar.*</span><span class="sxs-lookup"><span data-stu-id="da0de-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="da0de-112">Portanto, ele não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="da0de-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="da0de-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da0de-113">PARAMETERS</span></span>

### <span data-ttu-id="da0de-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="da0de-114">-AutomationAccountName</span></span>
<span data-ttu-id="da0de-115">Especifica o nome de uma conta de Automação da qual este cmdlet remove um web browser.</span><span class="sxs-lookup"><span data-stu-id="da0de-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="da0de-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da0de-116">-DefaultProfile</span></span>
<span data-ttu-id="da0de-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="da0de-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da0de-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="da0de-118">-Name</span></span>
<span data-ttu-id="da0de-119">Especifica o nome da webtareia que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="da0de-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="da0de-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da0de-120">-ResourceGroupName</span></span>
<span data-ttu-id="da0de-121">Especifica o nome do grupo de recursos para o qual este cmdlet remove um web browser.</span><span class="sxs-lookup"><span data-stu-id="da0de-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="da0de-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="da0de-122">-Confirm</span></span>
<span data-ttu-id="da0de-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da0de-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da0de-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da0de-124">-WhatIf</span></span>
<span data-ttu-id="da0de-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="da0de-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da0de-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="da0de-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da0de-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da0de-127">CommonParameters</span></span>
<span data-ttu-id="da0de-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da0de-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da0de-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da0de-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da0de-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="da0de-130">INPUTS</span></span>

### <span data-ttu-id="da0de-131">System.String</span><span class="sxs-lookup"><span data-stu-id="da0de-131">System.String</span></span>

## <span data-ttu-id="da0de-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="da0de-132">OUTPUTS</span></span>

### <span data-ttu-id="da0de-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="da0de-133">System.Void</span></span>

## <span data-ttu-id="da0de-134">Notas</span><span class="sxs-lookup"><span data-stu-id="da0de-134">NOTES</span></span>

## <span data-ttu-id="da0de-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da0de-135">RELATED LINKS</span></span>

[<span data-ttu-id="da0de-136">Get-AzAutomationWebweb</span><span class="sxs-lookup"><span data-stu-id="da0de-136">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="da0de-137">New-AzAutomationWebweb</span><span class="sxs-lookup"><span data-stu-id="da0de-137">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="da0de-138">Set-AzAutomationWebweb</span><span class="sxs-lookup"><span data-stu-id="da0de-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


