---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
ms.openlocfilehash: edae476893de5a64e950902d2de7b31fe53b51ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116630"
---
# <span data-ttu-id="1f995-101">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1f995-101">Get-AzAutomationRunbook</span></span>

## <span data-ttu-id="1f995-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f995-102">SYNOPSIS</span></span>
<span data-ttu-id="1f995-103">Obtém um livro de executar.</span><span class="sxs-lookup"><span data-stu-id="1f995-103">Gets a runbook.</span></span>

## <span data-ttu-id="1f995-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f995-104">SYNTAX</span></span>

### <span data-ttu-id="1f995-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1f995-105">ByAll (Default)</span></span>
```
Get-AzAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f995-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="1f995-106">ByRunbookName</span></span>
```
Get-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f995-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f995-107">DESCRIPTION</span></span>
<span data-ttu-id="1f995-108">O **cmdlet Get-AzAutomationRunbook** obtém os runbooks de Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="1f995-108">The **Get-AzAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="1f995-109">Para obter um runbook específico, especifique seu nome.</span><span class="sxs-lookup"><span data-stu-id="1f995-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="1f995-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1f995-110">EXAMPLES</span></span>

### <span data-ttu-id="1f995-111">Exemplo 1: Obter todos os runbooks</span><span class="sxs-lookup"><span data-stu-id="1f995-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1f995-112">Esse comando obtém todos os runbooks na conta automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="1f995-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="1f995-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f995-113">PARAMETERS</span></span>

### <span data-ttu-id="1f995-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1f995-114">-AutomationAccountName</span></span>
<span data-ttu-id="1f995-115">Especifica o nome de uma conta de Automação na qual este cmdlet obtém runbooks.</span><span class="sxs-lookup"><span data-stu-id="1f995-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="1f995-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f995-116">-DefaultProfile</span></span>
<span data-ttu-id="1f995-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1f995-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f995-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f995-118">-Name</span></span>
<span data-ttu-id="1f995-119">Especifica o nome de uma runbook que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="1f995-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f995-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f995-120">-ResourceGroupName</span></span>
<span data-ttu-id="1f995-121">Especifica o nome do grupo de recursos para o qual este cmdlet obtém os runbooks.</span><span class="sxs-lookup"><span data-stu-id="1f995-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="1f995-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f995-122">CommonParameters</span></span>
<span data-ttu-id="1f995-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f995-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f995-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f995-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f995-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="1f995-125">INPUTS</span></span>

### <span data-ttu-id="1f995-126">System.String</span><span class="sxs-lookup"><span data-stu-id="1f995-126">System.String</span></span>

## <span data-ttu-id="1f995-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="1f995-127">OUTPUTS</span></span>

### <span data-ttu-id="1f995-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="1f995-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="1f995-129">Notas</span><span class="sxs-lookup"><span data-stu-id="1f995-129">NOTES</span></span>

## <span data-ttu-id="1f995-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f995-130">RELATED LINKS</span></span>

[<span data-ttu-id="1f995-131">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1f995-131">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="1f995-132">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1f995-132">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="1f995-133">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1f995-133">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="1f995-134">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1f995-134">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="1f995-135">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1f995-135">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="1f995-136">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1f995-136">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="1f995-137">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1f995-137">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="1f995-138">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1f995-138">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


