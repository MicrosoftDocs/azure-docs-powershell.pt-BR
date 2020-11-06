---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
ms.openlocfilehash: 465e3ecd3f80b03eecb58309b18c91cd69c0d5a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611054"
---
# <span data-ttu-id="ff679-101">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="ff679-101">Remove-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="ff679-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff679-102">SYNOPSIS</span></span>
<span data-ttu-id="ff679-103">Remove um webhook de um runbook de automação.</span><span class="sxs-lookup"><span data-stu-id="ff679-103">Removes a webhook from an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff679-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff679-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationWebhook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff679-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff679-105">DESCRIPTION</span></span>
<span data-ttu-id="ff679-106">O cmdlet **Remove-AzureRmAutomationWebhook** remove um webhook de um runbook de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="ff679-106">The **Remove-AzureRmAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="ff679-107">O webhook é excluído.</span><span class="sxs-lookup"><span data-stu-id="ff679-107">The webhook is deleted.</span></span>

## <span data-ttu-id="ff679-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff679-108">EXAMPLES</span></span>

### <span data-ttu-id="ff679-109">Exemplo 1: remover um webhook</span><span class="sxs-lookup"><span data-stu-id="ff679-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzureRmAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="ff679-110">Esse comando Remove um webhook chamado Webhook11 na conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="ff679-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="ff679-111">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="ff679-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="ff679-112">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="ff679-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ff679-113">OS</span><span class="sxs-lookup"><span data-stu-id="ff679-113">PARAMETERS</span></span>

### <span data-ttu-id="ff679-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ff679-114">-AutomationAccountName</span></span>
<span data-ttu-id="ff679-115">Especifica o nome de uma conta de automação a partir da qual esse cmdlet Remove um webhook.</span><span class="sxs-lookup"><span data-stu-id="ff679-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff679-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff679-116">-DefaultProfile</span></span>
<span data-ttu-id="ff679-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ff679-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff679-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff679-118">-Name</span></span>
<span data-ttu-id="ff679-119">Especifica o nome do webhook que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="ff679-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff679-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff679-120">-ResourceGroupName</span></span>
<span data-ttu-id="ff679-121">Especifica o nome do grupo de recursos para o qual esse cmdlet Remove um webhook.</span><span class="sxs-lookup"><span data-stu-id="ff679-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff679-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ff679-122">-Confirm</span></span>
<span data-ttu-id="ff679-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff679-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff679-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff679-124">-WhatIf</span></span>
<span data-ttu-id="ff679-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ff679-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff679-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ff679-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff679-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff679-127">CommonParameters</span></span>
<span data-ttu-id="ff679-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff679-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff679-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff679-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff679-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff679-130">INPUTS</span></span>

### <span data-ttu-id="ff679-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ff679-131">None</span></span>
<span data-ttu-id="ff679-132">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="ff679-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ff679-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff679-133">OUTPUTS</span></span>

## <span data-ttu-id="ff679-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff679-134">NOTES</span></span>

## <span data-ttu-id="ff679-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff679-135">RELATED LINKS</span></span>

[<span data-ttu-id="ff679-136">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="ff679-136">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="ff679-137">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="ff679-137">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="ff679-138">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="ff679-138">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


