---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/powershell/module/az.automation/publish-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
ms.openlocfilehash: fa10c44186de06de758e4f7878bb7c8da61c4d6c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892252"
---
# <span data-ttu-id="a3999-101">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a3999-101">Publish-AzAutomationRunbook</span></span>

## <span data-ttu-id="a3999-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3999-102">SYNOPSIS</span></span>
<span data-ttu-id="a3999-103">Publica um runbook.</span><span class="sxs-lookup"><span data-stu-id="a3999-103">Publishes a runbook.</span></span>

## <span data-ttu-id="a3999-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a3999-104">SYNTAX</span></span>

```
Publish-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3999-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a3999-105">DESCRIPTION</span></span>
<span data-ttu-id="a3999-106">O cmdlet **Publish-AzAutomationRunbook** publica um runbook para uso no ambiente de produção do Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a3999-106">The **Publish-AzAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="a3999-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3999-107">EXAMPLES</span></span>

### <span data-ttu-id="a3999-108">Exemplo 1: Publicar um runbook</span><span class="sxs-lookup"><span data-stu-id="a3999-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a3999-109">Este comando publica o runbook chamado Runbk01 na conta de Automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a3999-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="a3999-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a3999-110">PARAMETERS</span></span>

### <span data-ttu-id="a3999-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a3999-111">-AutomationAccountName</span></span>
<span data-ttu-id="a3999-112">Especifica o nome da conta de automação na qual este cmdlet publica um runbook.</span><span class="sxs-lookup"><span data-stu-id="a3999-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="a3999-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3999-113">-DefaultProfile</span></span>
<span data-ttu-id="a3999-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a3999-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3999-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a3999-115">-Name</span></span>
<span data-ttu-id="a3999-116">Especifica o nome do runbook que este cmdlet publica.</span><span class="sxs-lookup"><span data-stu-id="a3999-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="a3999-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3999-117">-ResourceGroupName</span></span>
<span data-ttu-id="a3999-118">Especifica o nome do grupo de recursos para o qual este cmdlet publica um runbook.</span><span class="sxs-lookup"><span data-stu-id="a3999-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="a3999-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3999-119">CommonParameters</span></span>
<span data-ttu-id="a3999-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3999-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3999-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3999-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3999-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3999-122">INPUTS</span></span>

### <span data-ttu-id="a3999-123">System.String</span><span class="sxs-lookup"><span data-stu-id="a3999-123">System.String</span></span>

## <span data-ttu-id="a3999-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a3999-124">OUTPUTS</span></span>

### <span data-ttu-id="a3999-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="a3999-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="a3999-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="a3999-126">NOTES</span></span>

## <span data-ttu-id="a3999-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3999-127">RELATED LINKS</span></span>

[<span data-ttu-id="a3999-128">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a3999-128">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="a3999-129">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a3999-129">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="a3999-130">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a3999-130">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="a3999-131">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a3999-131">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="a3999-132">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a3999-132">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="a3999-133">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a3999-133">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="a3999-134">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a3999-134">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="a3999-135">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a3999-135">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


