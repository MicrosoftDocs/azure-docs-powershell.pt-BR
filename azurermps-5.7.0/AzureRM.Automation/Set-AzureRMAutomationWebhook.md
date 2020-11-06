---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
ms.openlocfilehash: d0443d5c15dec1324a5fe306ddec7303426449b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431740"
---
# <span data-ttu-id="76ccc-101">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="76ccc-101">Set-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="76ccc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76ccc-102">SYNOPSIS</span></span>
<span data-ttu-id="76ccc-103">Modifica um webhook para um runbook de automação.</span><span class="sxs-lookup"><span data-stu-id="76ccc-103">Modifies a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76ccc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76ccc-104">SYNTAX</span></span>

```
Set-AzureRmAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76ccc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76ccc-105">DESCRIPTION</span></span>
<span data-ttu-id="76ccc-106">O cmdlet **set-AzureRmAutomationWebhook** modifica um webhook para um runbook de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="76ccc-106">The **Set-AzureRmAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="76ccc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76ccc-107">EXAMPLES</span></span>

### <span data-ttu-id="76ccc-108">Exemplo 1: desabilitar um webhook</span><span class="sxs-lookup"><span data-stu-id="76ccc-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzureAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="76ccc-109">Esse comando desabilita um webhook chamado Webhook01 na conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="76ccc-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="76ccc-110">OS</span><span class="sxs-lookup"><span data-stu-id="76ccc-110">PARAMETERS</span></span>

### <span data-ttu-id="76ccc-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="76ccc-111">-AutomationAccountName</span></span>
<span data-ttu-id="76ccc-112">Especifica o nome de uma conta de automação na qual esse cmdlet modifica um webhook.</span><span class="sxs-lookup"><span data-stu-id="76ccc-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="76ccc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76ccc-113">-DefaultProfile</span></span>
<span data-ttu-id="76ccc-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="76ccc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76ccc-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="76ccc-115">-IsEnabled</span></span>
<span data-ttu-id="76ccc-116">Especifica se o webhook está habilitado.</span><span class="sxs-lookup"><span data-stu-id="76ccc-116">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ccc-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="76ccc-117">-Name</span></span>
<span data-ttu-id="76ccc-118">Especifica um nome do webhook que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="76ccc-118">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="76ccc-119">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76ccc-119">-Parameters</span></span>
<span data-ttu-id="76ccc-120">Especifica um dicionário de pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="76ccc-120">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="76ccc-121">As chaves são os nomes de parâmetro do runbook.</span><span class="sxs-lookup"><span data-stu-id="76ccc-121">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="76ccc-122">Os valores são os valores de parâmetro do runbook.</span><span class="sxs-lookup"><span data-stu-id="76ccc-122">The values are the runbook parameter values.</span></span>
<span data-ttu-id="76ccc-123">Quando o runbook é iniciado em resposta a um webhook, esses parâmetros são passados para o runbook.</span><span class="sxs-lookup"><span data-stu-id="76ccc-123">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76ccc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76ccc-124">-ResourceGroupName</span></span>
<span data-ttu-id="76ccc-125">Especifica o nome do grupo de recursos para o qual esse cmdlet modifica um webhook.</span><span class="sxs-lookup"><span data-stu-id="76ccc-125">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="76ccc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76ccc-126">CommonParameters</span></span>
<span data-ttu-id="76ccc-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76ccc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76ccc-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76ccc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76ccc-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76ccc-129">INPUTS</span></span>

### <span data-ttu-id="76ccc-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="76ccc-130">None</span></span>
<span data-ttu-id="76ccc-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="76ccc-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="76ccc-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76ccc-132">OUTPUTS</span></span>

### <span data-ttu-id="76ccc-133">Microsoft. Azure. Commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="76ccc-133">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="76ccc-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76ccc-134">NOTES</span></span>

## <span data-ttu-id="76ccc-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76ccc-135">RELATED LINKS</span></span>

[<span data-ttu-id="76ccc-136">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="76ccc-136">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="76ccc-137">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="76ccc-137">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="76ccc-138">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="76ccc-138">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)


