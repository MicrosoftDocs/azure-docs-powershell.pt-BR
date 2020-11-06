---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: 30ecb11822e622457600eb2a126171d431372f07
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601585"
---
# <span data-ttu-id="2e3a7-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="2e3a7-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="2e3a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e3a7-102">SYNOPSIS</span></span>
<span data-ttu-id="2e3a7-103">Obtém WebHooks da automação.</span><span class="sxs-lookup"><span data-stu-id="2e3a7-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="2e3a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e3a7-104">SYNTAX</span></span>

### <span data-ttu-id="2e3a7-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="2e3a7-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e3a7-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2e3a7-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e3a7-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="2e3a7-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e3a7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e3a7-108">DESCRIPTION</span></span>
<span data-ttu-id="2e3a7-109">O cmdlet **Get-AzAutomationWebhook** Obtém WebHooks.</span><span class="sxs-lookup"><span data-stu-id="2e3a7-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="2e3a7-110">Para obter WebHooks específicos, especifique um nome de webhook ou especifique o nome de um runbook de automação do Azure para obter os WebHooks conectados a ele.</span><span class="sxs-lookup"><span data-stu-id="2e3a7-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="2e3a7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e3a7-111">EXAMPLES</span></span>

### <span data-ttu-id="2e3a7-112">Exemplo 1: obter todos os WebHooks para um runbook</span><span class="sxs-lookup"><span data-stu-id="2e3a7-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="2e3a7-113">Esse comando obtém todos os WebHooks para um runbook chamado Runbook03 na conta de automação chamada AutomationAccount01 no grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="2e3a7-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="2e3a7-114">OS</span><span class="sxs-lookup"><span data-stu-id="2e3a7-114">PARAMETERS</span></span>

### <span data-ttu-id="2e3a7-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2e3a7-115">-AutomationAccountName</span></span>
<span data-ttu-id="2e3a7-116">Especifica o nome de uma conta de automação na qual esse cmdlet recebe um webhook.</span><span class="sxs-lookup"><span data-stu-id="2e3a7-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="2e3a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e3a7-117">-DefaultProfile</span></span>
<span data-ttu-id="2e3a7-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2e3a7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e3a7-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e3a7-119">-Name</span></span>
<span data-ttu-id="2e3a7-120">Especifica o nome do webhook que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="2e3a7-120">Specifies the name of the webhook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2e3a7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e3a7-121">-ResourceGroupName</span></span>
<span data-ttu-id="2e3a7-122">Especifica o nome do grupo de recursos para o qual esse cmdlet obtém WebHooks.</span><span class="sxs-lookup"><span data-stu-id="2e3a7-122">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="2e3a7-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="2e3a7-123">-RunbookName</span></span>
<span data-ttu-id="2e3a7-124">Especifica o nome de um runbook para o qual esse cmdlet obtém WebHooks.</span><span class="sxs-lookup"><span data-stu-id="2e3a7-124">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="2e3a7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e3a7-125">CommonParameters</span></span>
<span data-ttu-id="2e3a7-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e3a7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e3a7-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e3a7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e3a7-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e3a7-128">INPUTS</span></span>

### <span data-ttu-id="2e3a7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2e3a7-129">System.String</span></span>

## <span data-ttu-id="2e3a7-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e3a7-130">OUTPUTS</span></span>

### <span data-ttu-id="2e3a7-131">Microsoft. Azure. Commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="2e3a7-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="2e3a7-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e3a7-132">NOTES</span></span>

## <span data-ttu-id="2e3a7-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e3a7-133">RELATED LINKS</span></span>

[<span data-ttu-id="2e3a7-134">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="2e3a7-134">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="2e3a7-135">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="2e3a7-135">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="2e3a7-136">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="2e3a7-136">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


