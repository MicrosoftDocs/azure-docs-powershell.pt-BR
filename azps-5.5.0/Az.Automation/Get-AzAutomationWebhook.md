---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: ceca8c13b2cac0cc8685b1fa9fa3b26ab6017856
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117001"
---
# <span data-ttu-id="43db9-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="43db9-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="43db9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43db9-102">SYNOPSIS</span></span>
<span data-ttu-id="43db9-103">Obtém webções de Automação.</span><span class="sxs-lookup"><span data-stu-id="43db9-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="43db9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43db9-104">SYNTAX</span></span>

### <span data-ttu-id="43db9-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="43db9-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43db9-106">ByName</span><span class="sxs-lookup"><span data-stu-id="43db9-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43db9-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="43db9-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43db9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="43db9-108">DESCRIPTION</span></span>
<span data-ttu-id="43db9-109">O **cmdlet Get-AzAutomationWebweblet** obtém webções.</span><span class="sxs-lookup"><span data-stu-id="43db9-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="43db9-110">Para obter webções específicas, especifique um nome webtareia ou especifique o nome de um livro de aplicação de Automação do Azure para conectar os Webconectados a ele.</span><span class="sxs-lookup"><span data-stu-id="43db9-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="43db9-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="43db9-111">EXAMPLES</span></span>

### <span data-ttu-id="43db9-112">Exemplo 1: Obter todas as webções para um livro de runbook</span><span class="sxs-lookup"><span data-stu-id="43db9-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="43db9-113">Esse comando obtém todas as webções de um livro de executar chamado Runbook03 na conta automação chamada AutomationAccount01 no grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="43db9-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="43db9-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43db9-114">PARAMETERS</span></span>

### <span data-ttu-id="43db9-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="43db9-115">-AutomationAccountName</span></span>
<span data-ttu-id="43db9-116">Especifica o nome de uma conta de Automação na qual este cmdlet obtém um web browser.</span><span class="sxs-lookup"><span data-stu-id="43db9-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="43db9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43db9-117">-DefaultProfile</span></span>
<span data-ttu-id="43db9-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="43db9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43db9-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="43db9-119">-Name</span></span>
<span data-ttu-id="43db9-120">Especifica o nome da web que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="43db9-120">Specifies the name of the webhook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="43db9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43db9-121">-ResourceGroupName</span></span>
<span data-ttu-id="43db9-122">Especifica o nome do grupo de recursos para o qual este cmdlet obtém webções.</span><span class="sxs-lookup"><span data-stu-id="43db9-122">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="43db9-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="43db9-123">-RunbookName</span></span>
<span data-ttu-id="43db9-124">Especifica o nome de um runbook para o qual este cmdlet obtém webções.</span><span class="sxs-lookup"><span data-stu-id="43db9-124">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="43db9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43db9-125">CommonParameters</span></span>
<span data-ttu-id="43db9-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43db9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43db9-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43db9-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43db9-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="43db9-128">INPUTS</span></span>

### <span data-ttu-id="43db9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="43db9-129">System.String</span></span>

## <span data-ttu-id="43db9-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="43db9-130">OUTPUTS</span></span>

### <span data-ttu-id="43db9-131">Microsoft.Azure.Commands.Automation.Model.Web browser</span><span class="sxs-lookup"><span data-stu-id="43db9-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="43db9-132">Notas</span><span class="sxs-lookup"><span data-stu-id="43db9-132">NOTES</span></span>

## <span data-ttu-id="43db9-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43db9-133">RELATED LINKS</span></span>

[<span data-ttu-id="43db9-134">New-AzAutomationWebweb</span><span class="sxs-lookup"><span data-stu-id="43db9-134">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="43db9-135">Remove-AzAutomationWebweb</span><span class="sxs-lookup"><span data-stu-id="43db9-135">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="43db9-136">Set-AzAutomationWebweb</span><span class="sxs-lookup"><span data-stu-id="43db9-136">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


