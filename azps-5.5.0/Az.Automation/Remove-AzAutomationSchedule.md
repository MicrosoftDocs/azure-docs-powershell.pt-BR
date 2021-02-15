---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
ms.openlocfilehash: 0c37c33b60d430bc1782254401033934552f5663
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117999"
---
# <span data-ttu-id="6c7de-101">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6c7de-101">Remove-AzAutomationSchedule</span></span>

## <span data-ttu-id="6c7de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6c7de-102">SYNOPSIS</span></span>
<span data-ttu-id="6c7de-103">Exclui um cronograma de Automação.</span><span class="sxs-lookup"><span data-stu-id="6c7de-103">Deletes an Automation schedule.</span></span>

## <span data-ttu-id="6c7de-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c7de-104">SYNTAX</span></span>

```
Remove-AzAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c7de-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c7de-105">DESCRIPTION</span></span>
<span data-ttu-id="6c7de-106">O cmdlet **Remove-AzAutomationSchedule** exclui um cronograma da Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="6c7de-106">The **Remove-AzAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="6c7de-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6c7de-107">EXAMPLES</span></span>

### <span data-ttu-id="6c7de-108">Exemplo 1: Remover um cronograma</span><span class="sxs-lookup"><span data-stu-id="6c7de-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6c7de-109">Esse comando exclui o cronograma chamado Agenda01 na conta de automação Contoso17 no grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="6c7de-109">This command deletes the schedule named Schedule01 in automation account Contoso17 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="6c7de-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c7de-110">PARAMETERS</span></span>

### <span data-ttu-id="6c7de-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6c7de-111">-AutomationAccountName</span></span>
<span data-ttu-id="6c7de-112">Especifica o nome de uma conta de Automação para a qual este cmdlet remove um cronograma.</span><span class="sxs-lookup"><span data-stu-id="6c7de-112">Specifies the name of an Automation account for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="6c7de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c7de-113">-DefaultProfile</span></span>
<span data-ttu-id="6c7de-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="6c7de-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c7de-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="6c7de-115">-Force</span></span>
<span data-ttu-id="6c7de-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="6c7de-116">ps_force</span></span>

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

### <span data-ttu-id="6c7de-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c7de-117">-Name</span></span>
<span data-ttu-id="6c7de-118">Especifica o nome do cronograma que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="6c7de-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6c7de-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c7de-119">-ResourceGroupName</span></span>
<span data-ttu-id="6c7de-120">Especifica o nome de um grupo de recursos para o qual este cmdlet remove um cronograma.</span><span class="sxs-lookup"><span data-stu-id="6c7de-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="6c7de-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6c7de-121">-Confirm</span></span>
<span data-ttu-id="6c7de-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c7de-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c7de-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c7de-123">-WhatIf</span></span>
<span data-ttu-id="6c7de-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6c7de-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c7de-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6c7de-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c7de-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c7de-126">CommonParameters</span></span>
<span data-ttu-id="6c7de-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c7de-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c7de-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c7de-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c7de-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="6c7de-129">INPUTS</span></span>

### <span data-ttu-id="6c7de-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6c7de-130">System.String</span></span>

## <span data-ttu-id="6c7de-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="6c7de-131">OUTPUTS</span></span>

### <span data-ttu-id="6c7de-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="6c7de-132">System.Void</span></span>

## <span data-ttu-id="6c7de-133">Notas</span><span class="sxs-lookup"><span data-stu-id="6c7de-133">NOTES</span></span>

## <span data-ttu-id="6c7de-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6c7de-134">RELATED LINKS</span></span>

[<span data-ttu-id="6c7de-135">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6c7de-135">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="6c7de-136">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6c7de-136">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="6c7de-137">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6c7de-137">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


