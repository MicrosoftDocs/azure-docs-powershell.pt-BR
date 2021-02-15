---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: d6ce3a737063763d77ed408072d275c52ee5884c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118000"
---
# <span data-ttu-id="dafd9-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dafd9-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="dafd9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dafd9-102">SYNOPSIS</span></span>
<span data-ttu-id="dafd9-103">Remove um livro de executar.</span><span class="sxs-lookup"><span data-stu-id="dafd9-103">Removes a runbook.</span></span>

## <span data-ttu-id="dafd9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dafd9-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dafd9-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="dafd9-105">DESCRIPTION</span></span>
<span data-ttu-id="dafd9-106">O cmdlet **Remove-AzAutomationRunbook** remove um runbook da Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="dafd9-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="dafd9-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dafd9-107">EXAMPLES</span></span>

### <span data-ttu-id="dafd9-108">Exemplo 1: Remover um livro de executar</span><span class="sxs-lookup"><span data-stu-id="dafd9-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="dafd9-109">Esse comando remove o runbook chamado Runbook03 na conta de Automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="dafd9-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="dafd9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dafd9-110">PARAMETERS</span></span>

### <span data-ttu-id="dafd9-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dafd9-111">-AutomationAccountName</span></span>
<span data-ttu-id="dafd9-112">Especifica o nome da conta automação na qual este cmdlet remove um livro de executar.</span><span class="sxs-lookup"><span data-stu-id="dafd9-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="dafd9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dafd9-113">-DefaultProfile</span></span>
<span data-ttu-id="dafd9-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="dafd9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dafd9-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="dafd9-115">-Force</span></span>
<span data-ttu-id="dafd9-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="dafd9-116">ps_force</span></span>

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

### <span data-ttu-id="dafd9-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="dafd9-117">-Name</span></span>
<span data-ttu-id="dafd9-118">Especifica o nome do livro de executar que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="dafd9-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dafd9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dafd9-119">-ResourceGroupName</span></span>
<span data-ttu-id="dafd9-120">Especifica o nome do grupo de recursos para o qual este cmdlet publica um livro de executar.</span><span class="sxs-lookup"><span data-stu-id="dafd9-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="dafd9-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="dafd9-121">-Confirm</span></span>
<span data-ttu-id="dafd9-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dafd9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dafd9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dafd9-123">-WhatIf</span></span>
<span data-ttu-id="dafd9-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="dafd9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dafd9-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dafd9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dafd9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dafd9-126">CommonParameters</span></span>
<span data-ttu-id="dafd9-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dafd9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dafd9-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dafd9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dafd9-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="dafd9-129">INPUTS</span></span>

### <span data-ttu-id="dafd9-130">System.String</span><span class="sxs-lookup"><span data-stu-id="dafd9-130">System.String</span></span>

## <span data-ttu-id="dafd9-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="dafd9-131">OUTPUTS</span></span>

### <span data-ttu-id="dafd9-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="dafd9-132">System.Void</span></span>

## <span data-ttu-id="dafd9-133">Notas</span><span class="sxs-lookup"><span data-stu-id="dafd9-133">NOTES</span></span>

## <span data-ttu-id="dafd9-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dafd9-134">RELATED LINKS</span></span>

[<span data-ttu-id="dafd9-135">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dafd9-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="dafd9-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dafd9-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="dafd9-137">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dafd9-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="dafd9-138">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dafd9-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="dafd9-139">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dafd9-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="dafd9-140">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dafd9-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="dafd9-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dafd9-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="dafd9-142">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dafd9-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


