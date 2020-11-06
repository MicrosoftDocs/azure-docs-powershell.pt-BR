---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/publish-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
ms.openlocfilehash: 1d3ea7321efaae0f9d1107e3d1e87fd3c432656f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597781"
---
# <span data-ttu-id="8882e-101">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8882e-101">Publish-AzAutomationRunbook</span></span>

## <span data-ttu-id="8882e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8882e-102">SYNOPSIS</span></span>
<span data-ttu-id="8882e-103">Publica um runbook.</span><span class="sxs-lookup"><span data-stu-id="8882e-103">Publishes a runbook.</span></span>

## <span data-ttu-id="8882e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8882e-104">SYNTAX</span></span>

```
Publish-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8882e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8882e-105">DESCRIPTION</span></span>
<span data-ttu-id="8882e-106">O cmdlet **Publish-AzAutomationRunbook** publica um runbook para uso no ambiente de produção da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="8882e-106">The **Publish-AzAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="8882e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8882e-107">EXAMPLES</span></span>

### <span data-ttu-id="8882e-108">Exemplo 1: publicar um runbook</span><span class="sxs-lookup"><span data-stu-id="8882e-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8882e-109">Esse comando publica o runbook chamado Runbk01 na conta de automação do Azure chamado Contoso17.</span><span class="sxs-lookup"><span data-stu-id="8882e-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="8882e-110">OS</span><span class="sxs-lookup"><span data-stu-id="8882e-110">PARAMETERS</span></span>

### <span data-ttu-id="8882e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8882e-111">-AutomationAccountName</span></span>
<span data-ttu-id="8882e-112">Especifica o nome da conta de automação na qual esse cmdlet publica um runbook.</span><span class="sxs-lookup"><span data-stu-id="8882e-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="8882e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8882e-113">-DefaultProfile</span></span>
<span data-ttu-id="8882e-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8882e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8882e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8882e-115">-Name</span></span>
<span data-ttu-id="8882e-116">Especifica o nome do runbook que esse cmdlet publica.</span><span class="sxs-lookup"><span data-stu-id="8882e-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8882e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8882e-117">-ResourceGroupName</span></span>
<span data-ttu-id="8882e-118">Especifica o nome do grupo de recursos para o qual esse cmdlet publica um runbook.</span><span class="sxs-lookup"><span data-stu-id="8882e-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="8882e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8882e-119">CommonParameters</span></span>
<span data-ttu-id="8882e-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8882e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8882e-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8882e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8882e-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8882e-122">INPUTS</span></span>

### <span data-ttu-id="8882e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="8882e-123">System.String</span></span>

## <span data-ttu-id="8882e-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8882e-124">OUTPUTS</span></span>

### <span data-ttu-id="8882e-125">Microsoft. Azure. Commands. Automation. Model. runbook</span><span class="sxs-lookup"><span data-stu-id="8882e-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="8882e-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8882e-126">NOTES</span></span>

## <span data-ttu-id="8882e-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8882e-127">RELATED LINKS</span></span>

[<span data-ttu-id="8882e-128">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8882e-128">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="8882e-129">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8882e-129">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="8882e-130">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8882e-130">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="8882e-131">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8882e-131">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="8882e-132">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8882e-132">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="8882e-133">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8882e-133">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="8882e-134">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8882e-134">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="8882e-135">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8882e-135">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


