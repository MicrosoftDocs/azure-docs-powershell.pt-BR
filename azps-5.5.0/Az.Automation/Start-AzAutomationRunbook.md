---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
ms.openlocfilehash: 70d322b46f8aa9dc90696cbd813e576cc9dd9fbd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112240"
---
# <span data-ttu-id="dfdb3-101">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dfdb3-101">Start-AzAutomationRunbook</span></span>

## <span data-ttu-id="dfdb3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dfdb3-102">SYNOPSIS</span></span>
<span data-ttu-id="dfdb3-103">Inicia um trabalho de livro de executar.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-103">Starts a runbook job.</span></span>

## <span data-ttu-id="dfdb3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dfdb3-104">SYNTAX</span></span>

### <span data-ttu-id="dfdb3-105">ByAsynchronousReturnJob (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dfdb3-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dfdb3-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="dfdb3-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfdb3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="dfdb3-107">DESCRIPTION</span></span>
<span data-ttu-id="dfdb3-108">O **cmdlet Start-AzAutomationRunbook** inicia um trabalho de manual de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-108">The **Start-AzAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="dfdb3-109">Especifique a ID ou o nome de um livro de executar.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="dfdb3-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dfdb3-110">EXAMPLES</span></span>

### <span data-ttu-id="dfdb3-111">Exemplo 1: Iniciar um trabalho de uma agenda de trabalho</span><span class="sxs-lookup"><span data-stu-id="dfdb3-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="dfdb3-112">Esse comando inicia um trabalho de runbook para o runbook chamado Runbk01 na conta de Automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="dfdb3-113">Exemplo 2: Iniciar um trabalho de uma agenda de trabalho do Python 2 com parâmetros</span><span class="sxs-lookup"><span data-stu-id="dfdb3-113">Example 2: Start a Python 2 runbook job with parameters</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "RunbkPy01" -ResourceGroupName "ResourceGroup01" -Parameters @{"Key1"="ValueForPosition1";"Key2"="ValueForPosition2"}
```

<span data-ttu-id="dfdb3-114">Este comando inicia um trabalho de runbook para o livro de runbook Python 2 chamado RunbkPy01 na conta de Automação do Azure chamada Contoso17 com "ValueForPosition1" como o primeiro parâmetro posicional e "ValueForPosition2" para o segundo.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-114">This command starts a runbook job for the Python 2 runbook named RunbkPy01 in the Azure Automation account named Contoso17 with "ValueForPosition1" as the first positional parameter and "ValueForPosition2" for the second one.</span></span>

### <span data-ttu-id="dfdb3-115">Exemplo 3: Iniciar um trabalho de uma agenda de trabalho e aguardar os resultados</span><span class="sxs-lookup"><span data-stu-id="dfdb3-115">Example 3: Start a runbook job and wait for results</span></span>
```
Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="dfdb3-116">Esse comando inicia um trabalho de runbook para o runbook chamado Runbk01 na conta de Automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-116">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="dfdb3-117">Esse comando especifica o parâmetro _Aguardar._</span><span class="sxs-lookup"><span data-stu-id="dfdb3-117">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="dfdb3-118">Portanto, ele retorna resultados depois que o trabalho é concluído.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-118">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="dfdb3-119">O cmdlet espera até 1000 segundos pelos resultados.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-119">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="dfdb3-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dfdb3-120">PARAMETERS</span></span>

### <span data-ttu-id="dfdb3-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dfdb3-121">-AutomationAccountName</span></span>
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

### <span data-ttu-id="dfdb3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfdb3-122">-DefaultProfile</span></span>
<span data-ttu-id="dfdb3-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="dfdb3-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dfdb3-124">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="dfdb3-124">-MaxWaitSeconds</span></span>
<span data-ttu-id="dfdb3-125">Especifica o número de segundos que este cmdlet espera que um trabalho termine antes que ele o desaque.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-125">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="dfdb3-126">O valor padrão é 10800 ou três horas.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-126">The default value is 10800, or three hours.</span></span>

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

### <span data-ttu-id="dfdb3-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="dfdb3-127">-Name</span></span>
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

### <span data-ttu-id="dfdb3-128">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dfdb3-128">-Parameters</span></span>
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

### <span data-ttu-id="dfdb3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfdb3-129">-ResourceGroupName</span></span>
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

### <span data-ttu-id="dfdb3-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="dfdb3-130">-RunOn</span></span>
<span data-ttu-id="dfdb3-131">Especifica qual Grupo de Trabalhadores Híbridos deve executar o runbook.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-131">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

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

### <span data-ttu-id="dfdb3-132">-Aguarde</span><span class="sxs-lookup"><span data-stu-id="dfdb3-132">-Wait</span></span>
<span data-ttu-id="dfdb3-133">Indica que esse cmdlet aguarda a conclusão do trabalho, a suspensão ou a falha e, em seguida, retorna o controle para o PowerShell do Azure.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-133">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

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

### <span data-ttu-id="dfdb3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfdb3-134">CommonParameters</span></span>
<span data-ttu-id="dfdb3-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfdb3-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfdb3-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfdb3-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="dfdb3-137">INPUTS</span></span>

### <span data-ttu-id="dfdb3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="dfdb3-138">System.String</span></span>

## <span data-ttu-id="dfdb3-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="dfdb3-139">OUTPUTS</span></span>

### <span data-ttu-id="dfdb3-140">Microsoft.Azure.Commands.Automation.Model.Job</span><span class="sxs-lookup"><span data-stu-id="dfdb3-140">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

### <span data-ttu-id="dfdb3-141">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="dfdb3-141">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="dfdb3-142">Notas</span><span class="sxs-lookup"><span data-stu-id="dfdb3-142">NOTES</span></span>

## <span data-ttu-id="dfdb3-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dfdb3-143">RELATED LINKS</span></span>

[<span data-ttu-id="dfdb3-144">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dfdb3-144">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="dfdb3-145">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dfdb3-145">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="dfdb3-146">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dfdb3-146">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="dfdb3-147">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dfdb3-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="dfdb3-148">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dfdb3-148">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="dfdb3-149">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dfdb3-149">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="dfdb3-150">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dfdb3-150">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="dfdb3-151">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dfdb3-151">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)
