---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
ms.openlocfilehash: 13eeb70905225b89cfc362a13425ec77e0ef9521
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430583"
---
# <span data-ttu-id="7f221-101">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="7f221-101">Remove-AzAutomationWebhook</span></span>

## <span data-ttu-id="7f221-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f221-102">SYNOPSIS</span></span>
<span data-ttu-id="7f221-103">Remove um webhook de um runbook de automação.</span><span class="sxs-lookup"><span data-stu-id="7f221-103">Removes a webhook from an Automation runbook.</span></span>

## <span data-ttu-id="7f221-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f221-104">SYNTAX</span></span>

```
Remove-AzAutomationWebhook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f221-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f221-105">DESCRIPTION</span></span>
<span data-ttu-id="7f221-106">O cmdlet **Remove-AzAutomationWebhook** remove um webhook de um runbook de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="7f221-106">The **Remove-AzAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="7f221-107">O webhook é excluído.</span><span class="sxs-lookup"><span data-stu-id="7f221-107">The webhook is deleted.</span></span>

## <span data-ttu-id="7f221-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f221-108">EXAMPLES</span></span>

### <span data-ttu-id="7f221-109">Exemplo 1: remover um webhook</span><span class="sxs-lookup"><span data-stu-id="7f221-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="7f221-110">Esse comando Remove um webhook chamado Webhook11 na conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="7f221-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="7f221-111">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="7f221-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="7f221-112">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="7f221-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7f221-113">OS</span><span class="sxs-lookup"><span data-stu-id="7f221-113">PARAMETERS</span></span>

### <span data-ttu-id="7f221-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7f221-114">-AutomationAccountName</span></span>
<span data-ttu-id="7f221-115">Especifica o nome de uma conta de automação a partir da qual esse cmdlet Remove um webhook.</span><span class="sxs-lookup"><span data-stu-id="7f221-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="7f221-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f221-116">-DefaultProfile</span></span>
<span data-ttu-id="7f221-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7f221-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f221-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f221-118">-Name</span></span>
<span data-ttu-id="7f221-119">Especifica o nome do webhook que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="7f221-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7f221-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f221-120">-ResourceGroupName</span></span>
<span data-ttu-id="7f221-121">Especifica o nome do grupo de recursos para o qual esse cmdlet Remove um webhook.</span><span class="sxs-lookup"><span data-stu-id="7f221-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="7f221-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7f221-122">-Confirm</span></span>
<span data-ttu-id="7f221-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f221-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f221-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f221-124">-WhatIf</span></span>
<span data-ttu-id="7f221-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7f221-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f221-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7f221-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f221-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f221-127">CommonParameters</span></span>
<span data-ttu-id="7f221-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f221-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f221-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f221-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f221-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f221-130">INPUTS</span></span>

### <span data-ttu-id="7f221-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7f221-131">System.String</span></span>

## <span data-ttu-id="7f221-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f221-132">OUTPUTS</span></span>

### <span data-ttu-id="7f221-133">System. void</span><span class="sxs-lookup"><span data-stu-id="7f221-133">System.Void</span></span>

## <span data-ttu-id="7f221-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f221-134">NOTES</span></span>

## <span data-ttu-id="7f221-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f221-135">RELATED LINKS</span></span>

[<span data-ttu-id="7f221-136">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="7f221-136">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="7f221-137">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="7f221-137">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="7f221-138">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="7f221-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


