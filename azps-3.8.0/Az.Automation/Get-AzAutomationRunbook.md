---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
ms.openlocfilehash: edae476893de5a64e950902d2de7b31fe53b51ea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942753"
---
# <span data-ttu-id="6a622-101">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6a622-101">Get-AzAutomationRunbook</span></span>

## <span data-ttu-id="6a622-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6a622-102">SYNOPSIS</span></span>
<span data-ttu-id="6a622-103">Obtém um runbook.</span><span class="sxs-lookup"><span data-stu-id="6a622-103">Gets a runbook.</span></span>

## <span data-ttu-id="6a622-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a622-104">SYNTAX</span></span>

### <span data-ttu-id="6a622-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="6a622-105">ByAll (Default)</span></span>
```
Get-AzAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a622-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="6a622-106">ByRunbookName</span></span>
```
Get-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a622-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6a622-107">DESCRIPTION</span></span>
<span data-ttu-id="6a622-108">O cmdlet **Get-AzAutomationRunbook** Obtém os Runbooks de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="6a622-108">The **Get-AzAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="6a622-109">Para obter um runbook específico, especifique seu nome.</span><span class="sxs-lookup"><span data-stu-id="6a622-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="6a622-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6a622-110">EXAMPLES</span></span>

### <span data-ttu-id="6a622-111">Exemplo 1: obter todos os runbooks</span><span class="sxs-lookup"><span data-stu-id="6a622-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6a622-112">Esse comando obtém todos os runbooks na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="6a622-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="6a622-113">OS</span><span class="sxs-lookup"><span data-stu-id="6a622-113">PARAMETERS</span></span>

### <span data-ttu-id="6a622-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6a622-114">-AutomationAccountName</span></span>
<span data-ttu-id="6a622-115">Especifica o nome de uma conta de automação na qual esse cmdlet recebe runbooks.</span><span class="sxs-lookup"><span data-stu-id="6a622-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="6a622-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a622-116">-DefaultProfile</span></span>
<span data-ttu-id="6a622-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6a622-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a622-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a622-118">-Name</span></span>
<span data-ttu-id="6a622-119">Especifica o nome de um runbook que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="6a622-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6a622-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a622-120">-ResourceGroupName</span></span>
<span data-ttu-id="6a622-121">Especifica o nome do grupo de recursos para o qual esse cmdlet recebe runbooks.</span><span class="sxs-lookup"><span data-stu-id="6a622-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="6a622-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a622-122">CommonParameters</span></span>
<span data-ttu-id="6a622-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a622-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a622-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a622-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a622-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6a622-125">INPUTS</span></span>

### <span data-ttu-id="6a622-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6a622-126">System.String</span></span>

## <span data-ttu-id="6a622-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6a622-127">OUTPUTS</span></span>

### <span data-ttu-id="6a622-128">Microsoft. Azure. Commands. Automation. Model. runbook</span><span class="sxs-lookup"><span data-stu-id="6a622-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="6a622-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6a622-129">NOTES</span></span>

## <span data-ttu-id="6a622-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6a622-130">RELATED LINKS</span></span>

[<span data-ttu-id="6a622-131">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6a622-131">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="6a622-132">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6a622-132">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="6a622-133">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6a622-133">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="6a622-134">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6a622-134">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="6a622-135">Publicar-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6a622-135">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="6a622-136">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6a622-136">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="6a622-137">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6a622-137">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="6a622-138">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6a622-138">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


