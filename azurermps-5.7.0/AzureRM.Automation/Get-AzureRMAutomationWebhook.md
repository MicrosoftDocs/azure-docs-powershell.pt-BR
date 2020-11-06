---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationWebhook.md
ms.openlocfilehash: e695495b13cbad32cbf1d945a7de4080a88cc49c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441503"
---
# <span data-ttu-id="c68c2-101">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="c68c2-101">Get-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="c68c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c68c2-102">SYNOPSIS</span></span>
<span data-ttu-id="c68c2-103">Obtém WebHooks da automação.</span><span class="sxs-lookup"><span data-stu-id="c68c2-103">Gets webhooks from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c68c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c68c2-104">SYNTAX</span></span>

### <span data-ttu-id="c68c2-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="c68c2-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c68c2-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c68c2-106">ByName</span></span>
```
Get-AzureRmAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c68c2-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="c68c2-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c68c2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c68c2-108">DESCRIPTION</span></span>
<span data-ttu-id="c68c2-109">O cmdlet **Get-AzureRmAutomationWebhook** Obtém WebHooks.</span><span class="sxs-lookup"><span data-stu-id="c68c2-109">The **Get-AzureRmAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="c68c2-110">Para obter WebHooks específicos, especifique um nome de webhook ou especifique o nome de um runbook de automação do Azure para obter os WebHooks conectados a ele.</span><span class="sxs-lookup"><span data-stu-id="c68c2-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="c68c2-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c68c2-111">EXAMPLES</span></span>

### <span data-ttu-id="c68c2-112">Exemplo 1: obter todos os WebHooks para um runbook</span><span class="sxs-lookup"><span data-stu-id="c68c2-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="c68c2-113">Esse comando obtém todos os WebHooks para um runbook chamado Runbook03 na conta de automação chamada AutomationAccount01 no grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="c68c2-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="c68c2-114">OS</span><span class="sxs-lookup"><span data-stu-id="c68c2-114">PARAMETERS</span></span>

### <span data-ttu-id="c68c2-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c68c2-115">-AutomationAccountName</span></span>
<span data-ttu-id="c68c2-116">Especifica o nome de uma conta de automação na qual esse cmdlet recebe um webhook.</span><span class="sxs-lookup"><span data-stu-id="c68c2-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="c68c2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c68c2-117">-DefaultProfile</span></span>
<span data-ttu-id="c68c2-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c68c2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c68c2-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c68c2-119">-Name</span></span>
<span data-ttu-id="c68c2-120">Especifica o nome do webhook que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="c68c2-120">Specifies the name of the webhook that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: WebhookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c68c2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c68c2-121">-ResourceGroupName</span></span>
<span data-ttu-id="c68c2-122">Especifica o nome do grupo de recursos para o qual esse cmdlet obtém WebHooks.</span><span class="sxs-lookup"><span data-stu-id="c68c2-122">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="c68c2-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="c68c2-123">-RunbookName</span></span>
<span data-ttu-id="c68c2-124">Especifica o nome de um runbook para o qual esse cmdlet obtém WebHooks.</span><span class="sxs-lookup"><span data-stu-id="c68c2-124">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c68c2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c68c2-125">CommonParameters</span></span>
<span data-ttu-id="c68c2-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c68c2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c68c2-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c68c2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c68c2-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c68c2-128">INPUTS</span></span>

### <span data-ttu-id="c68c2-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c68c2-129">None</span></span>
<span data-ttu-id="c68c2-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="c68c2-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c68c2-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c68c2-131">OUTPUTS</span></span>

### <span data-ttu-id="c68c2-132">Microsoft. Azure. Commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="c68c2-132">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="c68c2-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c68c2-133">NOTES</span></span>

## <span data-ttu-id="c68c2-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c68c2-134">RELATED LINKS</span></span>

[<span data-ttu-id="c68c2-135">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="c68c2-135">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="c68c2-136">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="c68c2-136">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)

[<span data-ttu-id="c68c2-137">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="c68c2-137">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


