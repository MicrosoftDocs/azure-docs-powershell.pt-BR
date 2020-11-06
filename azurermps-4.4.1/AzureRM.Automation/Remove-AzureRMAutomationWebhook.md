---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
ms.openlocfilehash: f191176433a5ac12507d2b29a6d52c73a1d61e88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431813"
---
# <span data-ttu-id="5b169-101">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="5b169-101">Remove-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="5b169-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5b169-102">SYNOPSIS</span></span>
<span data-ttu-id="5b169-103">Remove um webhook de um runbook de automação.</span><span class="sxs-lookup"><span data-stu-id="5b169-103">Removes a webhook from an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b169-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b169-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationWebhook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5b169-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5b169-105">DESCRIPTION</span></span>
<span data-ttu-id="5b169-106">O cmdlet **Remove-AzureRmAutomationWebhook** remove um webhook de um runbook de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="5b169-106">The **Remove-AzureRmAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="5b169-107">O webhook é excluído.</span><span class="sxs-lookup"><span data-stu-id="5b169-107">The webhook is deleted.</span></span>

## <span data-ttu-id="5b169-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5b169-108">EXAMPLES</span></span>

### <span data-ttu-id="5b169-109">Exemplo 1: remover um webhook</span><span class="sxs-lookup"><span data-stu-id="5b169-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzureRmAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="5b169-110">Esse comando Remove um webhook chamado Webhook11 na conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="5b169-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="5b169-111">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="5b169-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="5b169-112">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="5b169-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="5b169-113">OS</span><span class="sxs-lookup"><span data-stu-id="5b169-113">PARAMETERS</span></span>

### <span data-ttu-id="5b169-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5b169-114">-AutomationAccountName</span></span>
<span data-ttu-id="5b169-115">Especifica o nome de uma conta de automação a partir da qual esse cmdlet Remove um webhook.</span><span class="sxs-lookup"><span data-stu-id="5b169-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="5b169-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b169-116">-Name</span></span>
<span data-ttu-id="5b169-117">Especifica o nome do webhook que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="5b169-117">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5b169-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b169-118">-ResourceGroupName</span></span>
<span data-ttu-id="5b169-119">Especifica o nome do grupo de recursos para o qual esse cmdlet Remove um webhook.</span><span class="sxs-lookup"><span data-stu-id="5b169-119">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="5b169-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5b169-120">-Confirm</span></span>
<span data-ttu-id="5b169-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b169-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b169-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b169-122">-WhatIf</span></span>
<span data-ttu-id="5b169-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5b169-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b169-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5b169-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b169-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b169-125">-DefaultProfile</span></span>
<span data-ttu-id="5b169-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5b169-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b169-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b169-127">CommonParameters</span></span>
<span data-ttu-id="5b169-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b169-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b169-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b169-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b169-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5b169-130">INPUTS</span></span>

## <span data-ttu-id="5b169-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5b169-131">OUTPUTS</span></span>

## <span data-ttu-id="5b169-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5b169-132">NOTES</span></span>

## <span data-ttu-id="5b169-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b169-133">RELATED LINKS</span></span>

[<span data-ttu-id="5b169-134">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="5b169-134">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="5b169-135">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="5b169-135">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="5b169-136">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="5b169-136">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


