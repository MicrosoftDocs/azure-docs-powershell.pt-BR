---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
ms.openlocfilehash: d56b631f106ef4984a81a8911af26288f720cac7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601524"
---
# <span data-ttu-id="71514-101">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="71514-101">Remove-AzAutomationSchedule</span></span>

## <span data-ttu-id="71514-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71514-102">SYNOPSIS</span></span>
<span data-ttu-id="71514-103">Exclui um cronograma de automação.</span><span class="sxs-lookup"><span data-stu-id="71514-103">Deletes an Automation schedule.</span></span>

## <span data-ttu-id="71514-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71514-104">SYNTAX</span></span>

```
Remove-AzAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71514-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71514-105">DESCRIPTION</span></span>
<span data-ttu-id="71514-106">O cmdlet **Remove-AzAutomationSchedule** exclui um cronograma da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="71514-106">The **Remove-AzAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="71514-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71514-107">EXAMPLES</span></span>

### <span data-ttu-id="71514-108">Exemplo 1: remover um cronograma</span><span class="sxs-lookup"><span data-stu-id="71514-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="71514-109">Esse comando exclui o agendamento chamado Schedule01 na conta de automação Contoso17 no ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="71514-109">This command deletes the schedule named Schedule01 in automation account Contoso17 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="71514-110">OS</span><span class="sxs-lookup"><span data-stu-id="71514-110">PARAMETERS</span></span>

### <span data-ttu-id="71514-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="71514-111">-AutomationAccountName</span></span>
<span data-ttu-id="71514-112">Especifica o nome de uma conta de automação para a qual esse cmdlet Remove um cronograma.</span><span class="sxs-lookup"><span data-stu-id="71514-112">Specifies the name of an Automation account for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="71514-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71514-113">-DefaultProfile</span></span>
<span data-ttu-id="71514-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="71514-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71514-115">-Force</span><span class="sxs-lookup"><span data-stu-id="71514-115">-Force</span></span>
<span data-ttu-id="71514-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="71514-116">ps_force</span></span>

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

### <span data-ttu-id="71514-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="71514-117">-Name</span></span>
<span data-ttu-id="71514-118">Especifica o nome do agendamento que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="71514-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="71514-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71514-119">-ResourceGroupName</span></span>
<span data-ttu-id="71514-120">Especifica o nome de um grupo de recursos para o qual esse cmdlet Remove um cronograma.</span><span class="sxs-lookup"><span data-stu-id="71514-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="71514-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="71514-121">-Confirm</span></span>
<span data-ttu-id="71514-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71514-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71514-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71514-123">-WhatIf</span></span>
<span data-ttu-id="71514-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="71514-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71514-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71514-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71514-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71514-126">CommonParameters</span></span>
<span data-ttu-id="71514-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71514-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71514-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71514-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71514-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71514-129">INPUTS</span></span>

### <span data-ttu-id="71514-130">System. String</span><span class="sxs-lookup"><span data-stu-id="71514-130">System.String</span></span>

## <span data-ttu-id="71514-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71514-131">OUTPUTS</span></span>

### <span data-ttu-id="71514-132">System. void</span><span class="sxs-lookup"><span data-stu-id="71514-132">System.Void</span></span>

## <span data-ttu-id="71514-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71514-133">NOTES</span></span>

## <span data-ttu-id="71514-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71514-134">RELATED LINKS</span></span>

[<span data-ttu-id="71514-135">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="71514-135">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="71514-136">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="71514-136">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="71514-137">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="71514-137">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


