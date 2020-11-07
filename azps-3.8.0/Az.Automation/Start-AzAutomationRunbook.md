---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
ms.openlocfilehash: 70d322b46f8aa9dc90696cbd813e576cc9dd9fbd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940570"
---
# <span data-ttu-id="f72fd-101">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f72fd-101">Start-AzAutomationRunbook</span></span>

## <span data-ttu-id="f72fd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f72fd-102">SYNOPSIS</span></span>
<span data-ttu-id="f72fd-103">Inicia um trabalho de runbook.</span><span class="sxs-lookup"><span data-stu-id="f72fd-103">Starts a runbook job.</span></span>

## <span data-ttu-id="f72fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f72fd-104">SYNTAX</span></span>

### <span data-ttu-id="f72fd-105">ByAsynchronousReturnJob (padrão)</span><span class="sxs-lookup"><span data-stu-id="f72fd-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f72fd-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="f72fd-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f72fd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f72fd-107">DESCRIPTION</span></span>
<span data-ttu-id="f72fd-108">O cmdlet **Start-AzAutomationRunbook** inicia um trabalho do runbook de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="f72fd-108">The **Start-AzAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="f72fd-109">Especifique a ID ou o nome de um runbook.</span><span class="sxs-lookup"><span data-stu-id="f72fd-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="f72fd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f72fd-110">EXAMPLES</span></span>

### <span data-ttu-id="f72fd-111">Exemplo 1: iniciar um trabalho de runbook</span><span class="sxs-lookup"><span data-stu-id="f72fd-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f72fd-112">Esse comando inicia um trabalho de runbook para o runbook chamado Runbk01 na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f72fd-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="f72fd-113">Exemplo 2: iniciar um trabalho de runbook do Python 2 com parâmetros</span><span class="sxs-lookup"><span data-stu-id="f72fd-113">Example 2: Start a Python 2 runbook job with parameters</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "RunbkPy01" -ResourceGroupName "ResourceGroup01" -Parameters @{"Key1"="ValueForPosition1";"Key2"="ValueForPosition2"}
```

<span data-ttu-id="f72fd-114">Esse comando inicia um trabalho de runbook para o runbook 2 do Python chamado RunbkPy01 na conta de automação do Azure chamada Contoso17 com "ValueForPosition1" como o primeiro parâmetro posicional e "ValueForPosition2" para o segundo.</span><span class="sxs-lookup"><span data-stu-id="f72fd-114">This command starts a runbook job for the Python 2 runbook named RunbkPy01 in the Azure Automation account named Contoso17 with "ValueForPosition1" as the first positional parameter and "ValueForPosition2" for the second one.</span></span>

### <span data-ttu-id="f72fd-115">Exemplo 3: iniciar um trabalho de runbook e esperar pelos resultados</span><span class="sxs-lookup"><span data-stu-id="f72fd-115">Example 3: Start a runbook job and wait for results</span></span>
```
Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="f72fd-116">Esse comando inicia um trabalho de runbook para o runbook chamado Runbk01 na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f72fd-116">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="f72fd-117">Esse comando especifica o parâmetro _Wait_ .</span><span class="sxs-lookup"><span data-stu-id="f72fd-117">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="f72fd-118">Portanto, retorna os resultados após a conclusão do trabalho.</span><span class="sxs-lookup"><span data-stu-id="f72fd-118">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="f72fd-119">O cmdlet aguarda até 1000 segundos para os resultados.</span><span class="sxs-lookup"><span data-stu-id="f72fd-119">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="f72fd-120">OS</span><span class="sxs-lookup"><span data-stu-id="f72fd-120">PARAMETERS</span></span>

### <span data-ttu-id="f72fd-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f72fd-121">-AutomationAccountName</span></span>
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

### <span data-ttu-id="f72fd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f72fd-122">-DefaultProfile</span></span>
<span data-ttu-id="f72fd-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f72fd-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f72fd-124">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="f72fd-124">-MaxWaitSeconds</span></span>
<span data-ttu-id="f72fd-125">Especifica o número de segundos que esse cmdlet aguarda para que o trabalho termine antes de abandonar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="f72fd-125">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="f72fd-126">O valor padrão é 10800 ou três horas.</span><span class="sxs-lookup"><span data-stu-id="f72fd-126">The default value is 10800, or three hours.</span></span>

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

### <span data-ttu-id="f72fd-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="f72fd-127">-Name</span></span>
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

### <span data-ttu-id="f72fd-128">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f72fd-128">-Parameters</span></span>
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

### <span data-ttu-id="f72fd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f72fd-129">-ResourceGroupName</span></span>
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

### <span data-ttu-id="f72fd-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="f72fd-130">-RunOn</span></span>
<span data-ttu-id="f72fd-131">Especifica o grupo do Hybrid Worker no qual o runbook será executado.</span><span class="sxs-lookup"><span data-stu-id="f72fd-131">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

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

### <span data-ttu-id="f72fd-132">-Wait</span><span class="sxs-lookup"><span data-stu-id="f72fd-132">-Wait</span></span>
<span data-ttu-id="f72fd-133">Indica que esse cmdlet aguarda o trabalho ser concluído, suspenso ou falha e, em seguida, retorna o controle para o Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f72fd-133">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

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

### <span data-ttu-id="f72fd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f72fd-134">CommonParameters</span></span>
<span data-ttu-id="f72fd-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f72fd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f72fd-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f72fd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f72fd-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f72fd-137">INPUTS</span></span>

### <span data-ttu-id="f72fd-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f72fd-138">System.String</span></span>

## <span data-ttu-id="f72fd-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f72fd-139">OUTPUTS</span></span>

### <span data-ttu-id="f72fd-140">Microsoft. Azure. Commands. Automation. Model. Job</span><span class="sxs-lookup"><span data-stu-id="f72fd-140">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

### <span data-ttu-id="f72fd-141">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f72fd-141">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f72fd-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f72fd-142">NOTES</span></span>

## <span data-ttu-id="f72fd-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f72fd-143">RELATED LINKS</span></span>

[<span data-ttu-id="f72fd-144">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f72fd-144">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="f72fd-145">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f72fd-145">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="f72fd-146">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f72fd-146">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="f72fd-147">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f72fd-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="f72fd-148">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f72fd-148">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="f72fd-149">Publicar-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f72fd-149">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="f72fd-150">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f72fd-150">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="f72fd-151">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f72fd-151">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)
