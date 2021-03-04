---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: 00125a7ad3d74d3e710b782d0be7fdb20004ef4a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893416"
---
# <span data-ttu-id="9a3ce-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="9a3ce-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="9a3ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a3ce-102">SYNOPSIS</span></span>
<span data-ttu-id="9a3ce-103">Obtém webhooks de Automação.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="9a3ce-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9a3ce-104">SYNTAX</span></span>

### <span data-ttu-id="9a3ce-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9a3ce-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a3ce-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9a3ce-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a3ce-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="9a3ce-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a3ce-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9a3ce-108">DESCRIPTION</span></span>
<span data-ttu-id="9a3ce-109">O cmdlet **Get-AzAutomationWebhook** obtém webhooks.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="9a3ce-110">Para obter webhooks específicos, especifique um nome de webhook ou especifique o nome de um runbook de Automação do Azure para conectar os webhooks a ele.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span><br>
<span data-ttu-id="9a3ce-111">**Observação:** O WebhookUri é retornado como cadeia de caracteres vazia devido a questões de segurança.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-111">**Note:** The WebhookUri is returned as empty string due to security concerns.</span></span> <span data-ttu-id="9a3ce-112">Certifique-se de salvar a URL de webhook que o cmdlet **New-AzAutomationWebhook** retorna, pois ela não pode ser recuperada usando **Get-AzAutomationWebhook**.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-112">Please make sure to save the webhook URL that **New-AzAutomationWebhook** cmdlet returns, because it cannot be retrieved by using **Get-AzAutomationWebhook**.</span></span>

## <span data-ttu-id="9a3ce-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9a3ce-113">EXAMPLES</span></span>

### <span data-ttu-id="9a3ce-114">Exemplo 1: Obter todos os webhooks para um runbook</span><span class="sxs-lookup"><span data-stu-id="9a3ce-114">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="9a3ce-115">Esse comando obtém todos os webhooks de um runbook chamado Runbook03 na conta de automação chamada AutomationAccount01 no grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-115">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="9a3ce-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9a3ce-116">PARAMETERS</span></span>

### <span data-ttu-id="9a3ce-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9a3ce-117">-AutomationAccountName</span></span>
<span data-ttu-id="9a3ce-118">Especifica o nome de uma conta de automação na qual esse cmdlet obtém um webhook.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-118">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="9a3ce-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a3ce-119">-DefaultProfile</span></span>
<span data-ttu-id="9a3ce-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="9a3ce-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a3ce-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9a3ce-121">-Name</span></span>
<span data-ttu-id="9a3ce-122">Especifica o nome do webhook que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-122">Specifies the name of the webhook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: WebhookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a3ce-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a3ce-123">-ResourceGroupName</span></span>
<span data-ttu-id="9a3ce-124">Especifica o nome do grupo de recursos para o qual este cmdlet obtém webhooks.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-124">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="9a3ce-125">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="9a3ce-125">-RunbookName</span></span>
<span data-ttu-id="9a3ce-126">Especifica o nome de um runbook para o qual este cmdlet obtém webhooks.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-126">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a3ce-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a3ce-127">CommonParameters</span></span>
<span data-ttu-id="9a3ce-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a3ce-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a3ce-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a3ce-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a3ce-130">INPUTS</span></span>

### <span data-ttu-id="9a3ce-131">System.String</span><span class="sxs-lookup"><span data-stu-id="9a3ce-131">System.String</span></span>

## <span data-ttu-id="9a3ce-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9a3ce-132">OUTPUTS</span></span>

### <span data-ttu-id="9a3ce-133">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="9a3ce-133">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="9a3ce-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="9a3ce-134">NOTES</span></span>

## <span data-ttu-id="9a3ce-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a3ce-135">RELATED LINKS</span></span>

[<span data-ttu-id="9a3ce-136">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="9a3ce-136">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="9a3ce-137">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="9a3ce-137">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="9a3ce-138">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="9a3ce-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


