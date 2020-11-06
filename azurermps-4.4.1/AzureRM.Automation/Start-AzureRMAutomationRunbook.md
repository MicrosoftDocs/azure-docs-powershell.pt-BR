---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
ms.openlocfilehash: c84410a38cb803eab9dbe4866c7a9426c9c3a21d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428292"
---
# <span data-ttu-id="9fff0-101">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9fff0-101">Start-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="9fff0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9fff0-102">SYNOPSIS</span></span>
<span data-ttu-id="9fff0-103">Inicia um trabalho de runbook.</span><span class="sxs-lookup"><span data-stu-id="9fff0-103">Starts a runbook job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fff0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9fff0-104">SYNTAX</span></span>

### <span data-ttu-id="9fff0-105">ByAsynchronousReturnJob (padrão)</span><span class="sxs-lookup"><span data-stu-id="9fff0-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9fff0-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="9fff0-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fff0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9fff0-107">DESCRIPTION</span></span>
<span data-ttu-id="9fff0-108">O cmdlet **Start-AzureRmAutomationRunbook** inicia um trabalho do runbook de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="9fff0-108">The **Start-AzureRmAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="9fff0-109">Especifique a ID ou o nome de um runbook.</span><span class="sxs-lookup"><span data-stu-id="9fff0-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="9fff0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9fff0-110">EXAMPLES</span></span>

### <span data-ttu-id="9fff0-111">Exemplo 1: iniciar um trabalho de runbook</span><span class="sxs-lookup"><span data-stu-id="9fff0-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9fff0-112">Esse comando inicia um trabalho de runbook para o runbook chamado Runbk01 na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9fff0-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="9fff0-113">Exemplo 2: iniciar um trabalho do runbook e esperar pelos resultados</span><span class="sxs-lookup"><span data-stu-id="9fff0-113">Example 2: Start a runbook job and wait for results</span></span>
```
Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="9fff0-114">Esse comando inicia um trabalho de runbook para o runbook chamado Runbk01 na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9fff0-114">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="9fff0-115">Esse comando especifica o parâmetro _Wait_ .</span><span class="sxs-lookup"><span data-stu-id="9fff0-115">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="9fff0-116">Portanto, retorna os resultados após a conclusão do trabalho.</span><span class="sxs-lookup"><span data-stu-id="9fff0-116">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="9fff0-117">O cmdlet aguarda até 1000 segundos para os resultados.</span><span class="sxs-lookup"><span data-stu-id="9fff0-117">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="9fff0-118">OS</span><span class="sxs-lookup"><span data-stu-id="9fff0-118">PARAMETERS</span></span>

### <span data-ttu-id="9fff0-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9fff0-119">-AutomationAccountName</span></span>
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

### <span data-ttu-id="9fff0-120">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="9fff0-120">-MaxWaitSeconds</span></span>
<span data-ttu-id="9fff0-121">Especifica o número de segundos que esse cmdlet aguarda para que o trabalho termine antes de abandonar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="9fff0-121">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="9fff0-122">O valor padrão é 10800 ou três horas.</span><span class="sxs-lookup"><span data-stu-id="9fff0-122">The default value is 10800, or three hours.</span></span>

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

### <span data-ttu-id="9fff0-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="9fff0-123">-Name</span></span>
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

### <span data-ttu-id="9fff0-124">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9fff0-124">-Parameters</span></span>
```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fff0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fff0-125">-ResourceGroupName</span></span>
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

### <span data-ttu-id="9fff0-126">-RunOn</span><span class="sxs-lookup"><span data-stu-id="9fff0-126">-RunOn</span></span>
<span data-ttu-id="9fff0-127">Especifica o grupo do Hybrid Worker no qual o runbook será executado.</span><span class="sxs-lookup"><span data-stu-id="9fff0-127">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

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

### <span data-ttu-id="9fff0-128">-Wait</span><span class="sxs-lookup"><span data-stu-id="9fff0-128">-Wait</span></span>
<span data-ttu-id="9fff0-129">Indica que esse cmdlet aguarda o trabalho ser concluído, suspenso ou falha e, em seguida, retorna o controle para o Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9fff0-129">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

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

### <span data-ttu-id="9fff0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fff0-130">-DefaultProfile</span></span>
<span data-ttu-id="9fff0-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9fff0-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fff0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fff0-132">CommonParameters</span></span>
<span data-ttu-id="9fff0-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fff0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fff0-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fff0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fff0-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9fff0-135">INPUTS</span></span>

## <span data-ttu-id="9fff0-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9fff0-136">OUTPUTS</span></span>

### <span data-ttu-id="9fff0-137">Microsoft. Azure. Commands. Automation. Model. Job</span><span class="sxs-lookup"><span data-stu-id="9fff0-137">Microsoft.Azure.Commands.Automation.Model.Job</span></span>
<span data-ttu-id="9fff0-138">Esse cmdlet retorna um objeto de **trabalho** , a menos que você especifique o parâmetro _Wait_ .</span><span class="sxs-lookup"><span data-stu-id="9fff0-138">This cmdlet returns a **Job** object, unless you specify the _Wait_ parameter.</span></span>

<span data-ttu-id="9fff0-139">Se você não especificar _Wait_ , o PowerShell do Azure retorna um objeto de **trabalho** imediatamente.</span><span class="sxs-lookup"><span data-stu-id="9fff0-139">If you do not specify _Wait_ , Azure PowerShell returns a **Job** object immediately.</span></span>
<span data-ttu-id="9fff0-140">Se você especificar _Wait_ , o PowerShell do Azure concluirá o trabalho e, em seguida, retornará o resultado.</span><span class="sxs-lookup"><span data-stu-id="9fff0-140">If you specify _Wait_ , Azure PowerShell completes the job, and then returns the result.</span></span>
<span data-ttu-id="9fff0-141">O resultado não é um objeto de **trabalho** .</span><span class="sxs-lookup"><span data-stu-id="9fff0-141">The result is not a **Job** object.</span></span>

## <span data-ttu-id="9fff0-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9fff0-142">NOTES</span></span>

## <span data-ttu-id="9fff0-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9fff0-143">RELATED LINKS</span></span>

[<span data-ttu-id="9fff0-144">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9fff0-144">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9fff0-145">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9fff0-145">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9fff0-146">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9fff0-146">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9fff0-147">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9fff0-147">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9fff0-148">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9fff0-148">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9fff0-149">Publicar-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9fff0-149">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9fff0-150">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9fff0-150">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9fff0-151">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9fff0-151">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)
