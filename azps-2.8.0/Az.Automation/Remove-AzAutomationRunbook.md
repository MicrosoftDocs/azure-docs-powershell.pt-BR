---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: c77413f27bcde145334221465cbe792a5e1eaa5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597759"
---
# <span data-ttu-id="a6add-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a6add-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="a6add-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6add-102">SYNOPSIS</span></span>
<span data-ttu-id="a6add-103">Remove um runbook.</span><span class="sxs-lookup"><span data-stu-id="a6add-103">Removes a runbook.</span></span>

## <span data-ttu-id="a6add-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6add-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6add-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6add-105">DESCRIPTION</span></span>
<span data-ttu-id="a6add-106">O cmdlet **Remove-AzAutomationRunbook** remove um runbook da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="a6add-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="a6add-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6add-107">EXAMPLES</span></span>

### <span data-ttu-id="a6add-108">Exemplo 1: remover um runbook</span><span class="sxs-lookup"><span data-stu-id="a6add-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a6add-109">Esse comando Remove o runbook chamado Runbook03 na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a6add-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="a6add-110">OS</span><span class="sxs-lookup"><span data-stu-id="a6add-110">PARAMETERS</span></span>

### <span data-ttu-id="a6add-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a6add-111">-AutomationAccountName</span></span>
<span data-ttu-id="a6add-112">Especifica o nome da conta de automação na qual esse cmdlet Remove um runbook.</span><span class="sxs-lookup"><span data-stu-id="a6add-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="a6add-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6add-113">-DefaultProfile</span></span>
<span data-ttu-id="a6add-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a6add-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6add-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a6add-115">-Force</span></span>
<span data-ttu-id="a6add-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="a6add-116">ps_force</span></span>

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

### <span data-ttu-id="a6add-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6add-117">-Name</span></span>
<span data-ttu-id="a6add-118">Especifica o nome do runbook que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="a6add-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a6add-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6add-119">-ResourceGroupName</span></span>
<span data-ttu-id="a6add-120">Especifica o nome do grupo de recursos para o qual esse cmdlet publica um runbook.</span><span class="sxs-lookup"><span data-stu-id="a6add-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="a6add-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a6add-121">-Confirm</span></span>
<span data-ttu-id="a6add-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6add-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6add-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6add-123">-WhatIf</span></span>
<span data-ttu-id="a6add-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a6add-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6add-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a6add-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6add-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6add-126">CommonParameters</span></span>
<span data-ttu-id="a6add-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6add-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6add-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6add-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6add-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6add-129">INPUTS</span></span>

### <span data-ttu-id="a6add-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a6add-130">System.String</span></span>

## <span data-ttu-id="a6add-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6add-131">OUTPUTS</span></span>

### <span data-ttu-id="a6add-132">System. void</span><span class="sxs-lookup"><span data-stu-id="a6add-132">System.Void</span></span>

## <span data-ttu-id="a6add-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6add-133">NOTES</span></span>

## <span data-ttu-id="a6add-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6add-134">RELATED LINKS</span></span>

[<span data-ttu-id="a6add-135">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a6add-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="a6add-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a6add-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="a6add-137">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a6add-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="a6add-138">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a6add-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="a6add-139">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a6add-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="a6add-140">Publicar-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a6add-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="a6add-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a6add-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="a6add-142">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a6add-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


