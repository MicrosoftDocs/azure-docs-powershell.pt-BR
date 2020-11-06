---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
ms.openlocfilehash: 47d384c6ca55fb428922dc3d9e59de84aa0db166
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426449"
---
# <span data-ttu-id="90f95-101">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="90f95-101">Set-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="90f95-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="90f95-102">SYNOPSIS</span></span>
<span data-ttu-id="90f95-103">Modifica um webhook para um runbook de automação.</span><span class="sxs-lookup"><span data-stu-id="90f95-103">Modifies a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90f95-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90f95-104">SYNTAX</span></span>

```
Set-AzureRmAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90f95-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="90f95-105">DESCRIPTION</span></span>
<span data-ttu-id="90f95-106">O cmdlet **set-AzureRmAutomationWebhook** modifica um webhook para um runbook de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="90f95-106">The **Set-AzureRmAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="90f95-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="90f95-107">EXAMPLES</span></span>

### <span data-ttu-id="90f95-108">Exemplo 1: desabilitar um webhook</span><span class="sxs-lookup"><span data-stu-id="90f95-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzureAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="90f95-109">Esse comando desabilita um webhook chamado Webhook01 na conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="90f95-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="90f95-110">OS</span><span class="sxs-lookup"><span data-stu-id="90f95-110">PARAMETERS</span></span>

### <span data-ttu-id="90f95-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="90f95-111">-AutomationAccountName</span></span>
<span data-ttu-id="90f95-112">Especifica o nome de uma conta de automação na qual esse cmdlet modifica um webhook.</span><span class="sxs-lookup"><span data-stu-id="90f95-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="90f95-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90f95-113">-DefaultProfile</span></span>
<span data-ttu-id="90f95-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="90f95-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90f95-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="90f95-115">-IsEnabled</span></span>
<span data-ttu-id="90f95-116">Especifica se o webhook está habilitado.</span><span class="sxs-lookup"><span data-stu-id="90f95-116">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="90f95-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="90f95-117">-Name</span></span>
<span data-ttu-id="90f95-118">Especifica um nome do webhook que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="90f95-118">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="90f95-119">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90f95-119">-Parameters</span></span>
<span data-ttu-id="90f95-120">Especifica um dicionário de pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="90f95-120">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="90f95-121">As chaves são os nomes de parâmetro do runbook.</span><span class="sxs-lookup"><span data-stu-id="90f95-121">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="90f95-122">Os valores são os valores de parâmetro do runbook.</span><span class="sxs-lookup"><span data-stu-id="90f95-122">The values are the runbook parameter values.</span></span>
<span data-ttu-id="90f95-123">Quando o runbook é iniciado em resposta a um webhook, esses parâmetros são passados para o runbook.</span><span class="sxs-lookup"><span data-stu-id="90f95-123">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="90f95-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90f95-124">-ResourceGroupName</span></span>
<span data-ttu-id="90f95-125">Especifica o nome do grupo de recursos para o qual esse cmdlet modifica um webhook.</span><span class="sxs-lookup"><span data-stu-id="90f95-125">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="90f95-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90f95-126">CommonParameters</span></span>
<span data-ttu-id="90f95-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90f95-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90f95-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90f95-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90f95-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="90f95-129">INPUTS</span></span>

### <span data-ttu-id="90f95-130">System. String</span><span class="sxs-lookup"><span data-stu-id="90f95-130">System.String</span></span>

### <span data-ttu-id="90f95-131">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="90f95-131">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="90f95-132">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="90f95-132">System.Collections.IDictionary</span></span>

## <span data-ttu-id="90f95-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="90f95-133">OUTPUTS</span></span>

### <span data-ttu-id="90f95-134">Microsoft. Azure. Commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="90f95-134">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="90f95-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="90f95-135">NOTES</span></span>

## <span data-ttu-id="90f95-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90f95-136">RELATED LINKS</span></span>

[<span data-ttu-id="90f95-137">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="90f95-137">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="90f95-138">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="90f95-138">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="90f95-139">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="90f95-139">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)


