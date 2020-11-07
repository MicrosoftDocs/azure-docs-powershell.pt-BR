---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 5b2c8685596771cd7986d8cfa071808daa63435c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942707"
---
# <span data-ttu-id="19d5a-101">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="19d5a-101">Get-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="19d5a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19d5a-102">SYNOPSIS</span></span>
<span data-ttu-id="19d5a-103">Obtém trabalhos de compilação DSC na automação.</span><span class="sxs-lookup"><span data-stu-id="19d5a-103">Gets DSC compilation jobs in Automation.</span></span>

## <span data-ttu-id="19d5a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19d5a-104">SYNTAX</span></span>

### <span data-ttu-id="19d5a-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="19d5a-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19d5a-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="19d5a-106">ByJobId</span></span>
```
Get-AzAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19d5a-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="19d5a-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19d5a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="19d5a-108">DESCRIPTION</span></span>
<span data-ttu-id="19d5a-109">O cmdlet **Get-AzAutomationDscCompilationJob** Obtém os trabalhos de compilação de DSC (configuração de estado desejado) do APS na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="19d5a-109">The **Get-AzAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="19d5a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19d5a-110">EXAMPLES</span></span>

### <span data-ttu-id="19d5a-111">Exemplo 1: obter todos os trabalhos de compilação DSC</span><span class="sxs-lookup"><span data-stu-id="19d5a-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="19d5a-112">Esse comando obtém todos os trabalhos de compilação na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="19d5a-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="19d5a-113">Exemplo 2: obter trabalhos de compilação DSC para uma configuração</span><span class="sxs-lookup"><span data-stu-id="19d5a-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="19d5a-114">Esse comando obtém todos os trabalhos de compilação para a configuração DSC chamada ContosoConfiguration na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="19d5a-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="19d5a-115">Exemplo 3: obter um trabalho de compilação DSC específico</span><span class="sxs-lookup"><span data-stu-id="19d5a-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="19d5a-116">Esse comando obtém o trabalho de compilação com a ID especificada na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="19d5a-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="19d5a-117">OS</span><span class="sxs-lookup"><span data-stu-id="19d5a-117">PARAMETERS</span></span>

### <span data-ttu-id="19d5a-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="19d5a-118">-AutomationAccountName</span></span>
<span data-ttu-id="19d5a-119">Especifica o nome da conta de automação que contém os trabalhos de compilação DSC que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="19d5a-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="19d5a-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="19d5a-120">-ConfigurationName</span></span>
<span data-ttu-id="19d5a-121">Especifica o nome da configuração DSC para a qual esse cmdlet obtém trabalhos de compilação.</span><span class="sxs-lookup"><span data-stu-id="19d5a-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19d5a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19d5a-122">-DefaultProfile</span></span>
<span data-ttu-id="19d5a-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="19d5a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19d5a-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="19d5a-124">-EndTime</span></span>
<span data-ttu-id="19d5a-125">Especifica uma hora de término.</span><span class="sxs-lookup"><span data-stu-id="19d5a-125">Specifies an end time.</span></span>
<span data-ttu-id="19d5a-126">Esse cmdlet obtém trabalhos de compilação que começaram até o momento em que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="19d5a-126">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19d5a-127">-ID</span><span class="sxs-lookup"><span data-stu-id="19d5a-127">-Id</span></span>
<span data-ttu-id="19d5a-128">Especifica a ID exclusiva do trabalho de compilação DSC que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="19d5a-128">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19d5a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19d5a-129">-ResourceGroupName</span></span>
<span data-ttu-id="19d5a-130">Especifica o nome de um grupo de recursos em que esse cmdlet obtém trabalhos de compilação DSC.</span><span class="sxs-lookup"><span data-stu-id="19d5a-130">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="19d5a-131">-StartTime</span><span class="sxs-lookup"><span data-stu-id="19d5a-131">-StartTime</span></span>
<span data-ttu-id="19d5a-132">Especifica uma hora de início.</span><span class="sxs-lookup"><span data-stu-id="19d5a-132">Specifies a start time.</span></span>
<span data-ttu-id="19d5a-133">Este cmdlet obtém trabalhos que iniciam em ou após o momento em que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="19d5a-133">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19d5a-134">-Status</span><span class="sxs-lookup"><span data-stu-id="19d5a-134">-Status</span></span>
<span data-ttu-id="19d5a-135">Especifica o status dos trabalhos que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="19d5a-135">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="19d5a-136">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="19d5a-136">Valid values are:</span></span> 
- <span data-ttu-id="19d5a-137">Feito</span><span class="sxs-lookup"><span data-stu-id="19d5a-137">Completed</span></span> 
- <span data-ttu-id="19d5a-138">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="19d5a-138">Failed</span></span> 
- <span data-ttu-id="19d5a-139">Na fila</span><span class="sxs-lookup"><span data-stu-id="19d5a-139">Queued</span></span> 
- <span data-ttu-id="19d5a-140">Iniciais</span><span class="sxs-lookup"><span data-stu-id="19d5a-140">Starting</span></span> 
- <span data-ttu-id="19d5a-141">Resuming</span><span class="sxs-lookup"><span data-stu-id="19d5a-141">Resuming</span></span> 
- <span data-ttu-id="19d5a-142">Executando</span><span class="sxs-lookup"><span data-stu-id="19d5a-142">Running</span></span> 
- <span data-ttu-id="19d5a-143">Terminou</span><span class="sxs-lookup"><span data-stu-id="19d5a-143">Stopped</span></span> 
- <span data-ttu-id="19d5a-144">Interromper</span><span class="sxs-lookup"><span data-stu-id="19d5a-144">Stopping</span></span> 
- <span data-ttu-id="19d5a-145">Interrompido</span><span class="sxs-lookup"><span data-stu-id="19d5a-145">Suspended</span></span> 
- <span data-ttu-id="19d5a-146">Suspending</span><span class="sxs-lookup"><span data-stu-id="19d5a-146">Suspending</span></span> 
- <span data-ttu-id="19d5a-147">Activa</span><span class="sxs-lookup"><span data-stu-id="19d5a-147">Activating</span></span>
- <span data-ttu-id="19d5a-148">Novo</span><span class="sxs-lookup"><span data-stu-id="19d5a-148">New</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating, New

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19d5a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19d5a-149">CommonParameters</span></span>
<span data-ttu-id="19d5a-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19d5a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19d5a-151">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19d5a-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19d5a-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="19d5a-152">INPUTS</span></span>

### <span data-ttu-id="19d5a-153">System. GUID</span><span class="sxs-lookup"><span data-stu-id="19d5a-153">System.Guid</span></span>

### <span data-ttu-id="19d5a-154">System. String</span><span class="sxs-lookup"><span data-stu-id="19d5a-154">System.String</span></span>

## <span data-ttu-id="19d5a-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="19d5a-155">OUTPUTS</span></span>

### <span data-ttu-id="19d5a-156">Microsoft. Azure. Commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="19d5a-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="19d5a-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="19d5a-157">NOTES</span></span>

## <span data-ttu-id="19d5a-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19d5a-158">RELATED LINKS</span></span>

[<span data-ttu-id="19d5a-159">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="19d5a-159">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="19d5a-160">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="19d5a-160">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


