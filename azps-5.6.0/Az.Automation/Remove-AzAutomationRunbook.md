---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: a7dc06e4ddbeac224daf9b8a80be40d343514a18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892888"
---
# <span data-ttu-id="27620-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="27620-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="27620-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27620-102">SYNOPSIS</span></span>
<span data-ttu-id="27620-103">Remove um runbook.</span><span class="sxs-lookup"><span data-stu-id="27620-103">Removes a runbook.</span></span>

## <span data-ttu-id="27620-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="27620-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27620-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="27620-105">DESCRIPTION</span></span>
<span data-ttu-id="27620-106">O cmdlet **Remove-AzAutomationRunbook** remove um runbook da Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="27620-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="27620-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="27620-107">EXAMPLES</span></span>

### <span data-ttu-id="27620-108">Exemplo 1: Remover um runbook</span><span class="sxs-lookup"><span data-stu-id="27620-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="27620-109">Este comando remove o runbook chamado Runbook03 na conta de Automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="27620-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="27620-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="27620-110">PARAMETERS</span></span>

### <span data-ttu-id="27620-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="27620-111">-AutomationAccountName</span></span>
<span data-ttu-id="27620-112">Especifica o nome da conta de automação na qual este cmdlet remove um runbook.</span><span class="sxs-lookup"><span data-stu-id="27620-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="27620-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27620-113">-DefaultProfile</span></span>
<span data-ttu-id="27620-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="27620-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27620-115">-Force</span><span class="sxs-lookup"><span data-stu-id="27620-115">-Force</span></span>
<span data-ttu-id="27620-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="27620-116">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27620-117">-Name</span><span class="sxs-lookup"><span data-stu-id="27620-117">-Name</span></span>
<span data-ttu-id="27620-118">Especifica o nome do runbook que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="27620-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="27620-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27620-119">-ResourceGroupName</span></span>
<span data-ttu-id="27620-120">Especifica o nome do grupo de recursos para o qual este cmdlet publica um runbook.</span><span class="sxs-lookup"><span data-stu-id="27620-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="27620-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27620-121">-Confirm</span></span>
<span data-ttu-id="27620-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27620-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27620-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27620-123">-WhatIf</span></span>
<span data-ttu-id="27620-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="27620-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27620-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="27620-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27620-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27620-126">CommonParameters</span></span>
<span data-ttu-id="27620-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27620-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27620-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27620-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27620-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="27620-129">INPUTS</span></span>

### <span data-ttu-id="27620-130">System.String</span><span class="sxs-lookup"><span data-stu-id="27620-130">System.String</span></span>

## <span data-ttu-id="27620-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="27620-131">OUTPUTS</span></span>

### <span data-ttu-id="27620-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="27620-132">System.Void</span></span>

## <span data-ttu-id="27620-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="27620-133">NOTES</span></span>

## <span data-ttu-id="27620-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27620-134">RELATED LINKS</span></span>

[<span data-ttu-id="27620-135">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="27620-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="27620-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="27620-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="27620-137">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="27620-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="27620-138">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="27620-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="27620-139">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="27620-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="27620-140">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="27620-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="27620-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="27620-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="27620-142">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="27620-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


