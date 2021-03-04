---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/powershell/module/az.automation/start-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
ms.openlocfilehash: 00eb652bc9779554f1c860edd503fc752c7ccaa0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886096"
---
# <span data-ttu-id="91491-101">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="91491-101">Start-AzAutomationRunbook</span></span>

## <span data-ttu-id="91491-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91491-102">SYNOPSIS</span></span>
<span data-ttu-id="91491-103">Inicia um trabalho de runbook.</span><span class="sxs-lookup"><span data-stu-id="91491-103">Starts a runbook job.</span></span>

## <span data-ttu-id="91491-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="91491-104">SYNTAX</span></span>

### <span data-ttu-id="91491-105">ByAsynchronousReturnJob (Padrão)</span><span class="sxs-lookup"><span data-stu-id="91491-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91491-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="91491-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91491-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="91491-107">DESCRIPTION</span></span>
<span data-ttu-id="91491-108">O cmdlet **Start-AzAutomationRunbook** inicia um trabalho de runbook de Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="91491-108">The **Start-AzAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="91491-109">Especifique a ID ou o nome de um runbook.</span><span class="sxs-lookup"><span data-stu-id="91491-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="91491-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91491-110">EXAMPLES</span></span>

### <span data-ttu-id="91491-111">Exemplo 1: Iniciar um trabalho de runbook</span><span class="sxs-lookup"><span data-stu-id="91491-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="91491-112">Este comando inicia um trabalho de runbook para o runbook chamado Runbk01 na conta de Automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="91491-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="91491-113">Exemplo 2: Iniciar um trabalho de runbook do Python 2 com parâmetros</span><span class="sxs-lookup"><span data-stu-id="91491-113">Example 2: Start a Python 2 runbook job with parameters</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "RunbkPy01" -ResourceGroupName "ResourceGroup01" -Parameters @{"Key1"="ValueForPosition1";"Key2"="ValueForPosition2"}
```

<span data-ttu-id="91491-114">Este comando inicia um trabalho de runbook para o runbook Python 2 chamado RunbkPy01 na conta de Automação do Azure chamada Contoso17 com "ValueForPosition1" como o primeiro parâmetro posicional e "ValueForPosition2" para o segundo.</span><span class="sxs-lookup"><span data-stu-id="91491-114">This command starts a runbook job for the Python 2 runbook named RunbkPy01 in the Azure Automation account named Contoso17 with "ValueForPosition1" as the first positional parameter and "ValueForPosition2" for the second one.</span></span>

### <span data-ttu-id="91491-115">Exemplo 3: Iniciar um trabalho de runbook e aguardar resultados</span><span class="sxs-lookup"><span data-stu-id="91491-115">Example 3: Start a runbook job and wait for results</span></span>
```
Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="91491-116">Este comando inicia um trabalho de runbook para o runbook chamado Runbk01 na conta de Automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="91491-116">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="91491-117">Este comando especifica o parâmetro _Wait._</span><span class="sxs-lookup"><span data-stu-id="91491-117">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="91491-118">Portanto, ele retorna resultados após a conclusão do trabalho.</span><span class="sxs-lookup"><span data-stu-id="91491-118">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="91491-119">O cmdlet aguarda até 1000 segundos pelos resultados.</span><span class="sxs-lookup"><span data-stu-id="91491-119">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="91491-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="91491-120">PARAMETERS</span></span>

### <span data-ttu-id="91491-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="91491-121">-AutomationAccountName</span></span>
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

### <span data-ttu-id="91491-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91491-122">-DefaultProfile</span></span>
<span data-ttu-id="91491-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="91491-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91491-124">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="91491-124">-MaxWaitSeconds</span></span>
<span data-ttu-id="91491-125">Especifica o número de segundos que esse cmdlet aguarda a finalização de um trabalho antes de abandonar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="91491-125">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="91491-126">O valor padrão é 10800 ou três horas.</span><span class="sxs-lookup"><span data-stu-id="91491-126">The default value is 10800, or three hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: BySynchronousReturnJobOutput
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91491-127">-Name</span><span class="sxs-lookup"><span data-stu-id="91491-127">-Name</span></span>
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

### <span data-ttu-id="91491-128">-Parameters</span><span class="sxs-lookup"><span data-stu-id="91491-128">-Parameters</span></span>
```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: JobParameters

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91491-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91491-129">-ResourceGroupName</span></span>
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

### <span data-ttu-id="91491-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="91491-130">-RunOn</span></span>
<span data-ttu-id="91491-131">Especifica o grupo de trabalho híbrido no qual executar o runbook.</span><span class="sxs-lookup"><span data-stu-id="91491-131">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91491-132">-Wait</span><span class="sxs-lookup"><span data-stu-id="91491-132">-Wait</span></span>
<span data-ttu-id="91491-133">Indica que esse cmdlet aguarda a conclusão, suspensão ou falha do trabalho e retorna o controle ao Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="91491-133">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySynchronousReturnJobOutput
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91491-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91491-134">CommonParameters</span></span>
<span data-ttu-id="91491-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91491-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91491-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91491-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91491-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91491-137">INPUTS</span></span>

### <span data-ttu-id="91491-138">System.String</span><span class="sxs-lookup"><span data-stu-id="91491-138">System.String</span></span>

## <span data-ttu-id="91491-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="91491-139">OUTPUTS</span></span>

### <span data-ttu-id="91491-140">Microsoft.Azure.Commands.Automation.Model.Job</span><span class="sxs-lookup"><span data-stu-id="91491-140">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

### <span data-ttu-id="91491-141">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="91491-141">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="91491-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="91491-142">NOTES</span></span>

## <span data-ttu-id="91491-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91491-143">RELATED LINKS</span></span>

[<span data-ttu-id="91491-144">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="91491-144">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="91491-145">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="91491-145">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="91491-146">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="91491-146">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="91491-147">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="91491-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="91491-148">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="91491-148">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="91491-149">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="91491-149">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="91491-150">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="91491-150">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="91491-151">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="91491-151">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)
