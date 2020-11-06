---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
ms.openlocfilehash: df6fc949fe1aa105a84ede2329c71feb4b27a449
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601546"
---
# <span data-ttu-id="6c229-101">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="6c229-101">Register-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="6c229-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6c229-102">SYNOPSIS</span></span>
<span data-ttu-id="6c229-103">Associa um runbook a um cronograma.</span><span class="sxs-lookup"><span data-stu-id="6c229-103">Associates a runbook to a schedule.</span></span>

## <span data-ttu-id="6c229-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6c229-104">SYNTAX</span></span>

### <span data-ttu-id="6c229-105">ByRunbookName (padrão)</span><span class="sxs-lookup"><span data-stu-id="6c229-105">ByRunbookName (Default)</span></span>
```
Register-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c229-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="6c229-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Parameters <IDictionary>]
 [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c229-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6c229-107">DESCRIPTION</span></span>
<span data-ttu-id="6c229-108">O cmdlet **Register-AzAutomationScheduledRunbook** associa um runbook de automação do Azure a um cronograma.</span><span class="sxs-lookup"><span data-stu-id="6c229-108">The **Register-AzAutomationScheduledRunbook** cmdlet associates an Azure Automation runbook to a schedule.</span></span>
<span data-ttu-id="6c229-109">O runbook começará com base no agendamento especificado usando o parâmetro *Scheduler* .</span><span class="sxs-lookup"><span data-stu-id="6c229-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="6c229-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6c229-110">EXAMPLES</span></span>

### <span data-ttu-id="6c229-111">Exemplo 1: associar um runbook a um cronograma</span><span class="sxs-lookup"><span data-stu-id="6c229-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\>Register-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6c229-112">Esse comando associa o runbook chamado Runbk01 com o cronograma chamado Sched01 na conta de automação do Azure chamado Contoso17.</span><span class="sxs-lookup"><span data-stu-id="6c229-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="6c229-113">OS</span><span class="sxs-lookup"><span data-stu-id="6c229-113">PARAMETERS</span></span>

### <span data-ttu-id="6c229-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6c229-114">-AutomationAccountName</span></span>
<span data-ttu-id="6c229-115">Especifica uma conta de automação para o runbook no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="6c229-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="6c229-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c229-116">-DefaultProfile</span></span>
<span data-ttu-id="6c229-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6c229-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c229-118">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c229-118">-Parameters</span></span>
<span data-ttu-id="6c229-119">Especifica uma tabela de hash de pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="6c229-119">Specifies a hash table of key/value pairs.</span></span>
<span data-ttu-id="6c229-120">As chaves são nomes de parâmetro de runbook.</span><span class="sxs-lookup"><span data-stu-id="6c229-120">The keys are runbook parameter names.</span></span>
<span data-ttu-id="6c229-121">Os valores são valores de parâmetro de runbook.</span><span class="sxs-lookup"><span data-stu-id="6c229-121">The values are runbook parameter values.</span></span>
<span data-ttu-id="6c229-122">Quando o runbook é iniciado em resposta ao cronograma associado, esses parâmetros são passados para o runbook.</span><span class="sxs-lookup"><span data-stu-id="6c229-122">When the runbook starts in response to the associated schedule, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c229-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c229-123">-ResourceGroupName</span></span>
<span data-ttu-id="6c229-124">Especifica o nome de um grupo de recursos para o runbook agendado.</span><span class="sxs-lookup"><span data-stu-id="6c229-124">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="6c229-125">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="6c229-125">-RunbookName</span></span>
<span data-ttu-id="6c229-126">Especifica o nome do runbook que este cmdlet associa a um cronograma.</span><span class="sxs-lookup"><span data-stu-id="6c229-126">Specifies the name of the runbook that this cmdlet associates to a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c229-127">-RunOn</span><span class="sxs-lookup"><span data-stu-id="6c229-127">-RunOn</span></span>
<span data-ttu-id="6c229-128">O nome do grupo de trabalho híbrido do runbook.</span><span class="sxs-lookup"><span data-stu-id="6c229-128">The name of the hybrid runbook worker group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c229-129">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="6c229-129">-ScheduleName</span></span>
<span data-ttu-id="6c229-130">Especifica o nome do cronograma para o qual esse cmdlet associa um runbook.</span><span class="sxs-lookup"><span data-stu-id="6c229-130">Specifies the name of the schedule to which this cmdlet associates a runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c229-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c229-131">CommonParameters</span></span>
<span data-ttu-id="6c229-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c229-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c229-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c229-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c229-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6c229-134">INPUTS</span></span>

### <span data-ttu-id="6c229-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6c229-135">System.String</span></span>

## <span data-ttu-id="6c229-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6c229-136">OUTPUTS</span></span>

### <span data-ttu-id="6c229-137">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="6c229-137">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="6c229-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6c229-138">NOTES</span></span>

## <span data-ttu-id="6c229-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6c229-139">RELATED LINKS</span></span>

[<span data-ttu-id="6c229-140">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="6c229-140">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="6c229-141">Cancelar registro-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="6c229-141">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)


