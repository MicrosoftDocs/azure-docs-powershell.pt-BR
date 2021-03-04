---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 5157b4d4e1a291193f10fef22308002de210e748
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890672"
---
# <span data-ttu-id="45598-101">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="45598-101">Get-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="45598-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45598-102">SYNOPSIS</span></span>
<span data-ttu-id="45598-103">Obtém trabalhos de compilação DSC em Automação.</span><span class="sxs-lookup"><span data-stu-id="45598-103">Gets DSC compilation jobs in Automation.</span></span>

## <span data-ttu-id="45598-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="45598-104">SYNTAX</span></span>

### <span data-ttu-id="45598-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="45598-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="45598-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="45598-106">ByJobId</span></span>
```
Get-AzAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45598-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="45598-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45598-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="45598-108">DESCRIPTION</span></span>
<span data-ttu-id="45598-109">O cmdlet **Get-AzAutomationDscCompilationJob** obtém trabalhos de compilação de Configuração de Estado Desejado (DSC) do APS no Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="45598-109">The **Get-AzAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="45598-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45598-110">EXAMPLES</span></span>

### <span data-ttu-id="45598-111">Exemplo 1: Obter todos os trabalhos de compilação DSC</span><span class="sxs-lookup"><span data-stu-id="45598-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="45598-112">Este comando obtém todos os trabalhos de compilação na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="45598-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="45598-113">Exemplo 2: Obter trabalhos de compilação DSC para uma configuração</span><span class="sxs-lookup"><span data-stu-id="45598-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="45598-114">Este comando obtém todos os trabalhos de compilação para a configuração DSC chamada ContosoConfiguration na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="45598-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="45598-115">Exemplo 3: Obter um trabalho de compilação DSC específico</span><span class="sxs-lookup"><span data-stu-id="45598-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="45598-116">Este comando obtém o trabalho de compilação com a ID especificada na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="45598-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="45598-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="45598-117">PARAMETERS</span></span>

### <span data-ttu-id="45598-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="45598-118">-AutomationAccountName</span></span>
<span data-ttu-id="45598-119">Especifica o nome da conta de automação que contém trabalhos de compilação DSC que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="45598-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="45598-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="45598-120">-ConfigurationName</span></span>
<span data-ttu-id="45598-121">Especifica o nome da configuração DSC para a qual este cmdlet obtém trabalhos de compilação.</span><span class="sxs-lookup"><span data-stu-id="45598-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

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

### <span data-ttu-id="45598-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45598-122">-DefaultProfile</span></span>
<span data-ttu-id="45598-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="45598-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45598-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="45598-124">-EndTime</span></span>
<span data-ttu-id="45598-125">Especifica uma hora de término.</span><span class="sxs-lookup"><span data-stu-id="45598-125">Specifies an end time.</span></span>
<span data-ttu-id="45598-126">Este cmdlet obtém trabalhos de compilação iniciados até o momento especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="45598-126">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="45598-127">-Id</span><span class="sxs-lookup"><span data-stu-id="45598-127">-Id</span></span>
<span data-ttu-id="45598-128">Especifica a ID exclusiva do trabalho de compilação DSC que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="45598-128">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="45598-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45598-129">-ResourceGroupName</span></span>
<span data-ttu-id="45598-130">Especifica o nome de um grupo de recursos no qual este cmdlet obtém trabalhos de compilação de DSC.</span><span class="sxs-lookup"><span data-stu-id="45598-130">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="45598-131">-StartTime</span><span class="sxs-lookup"><span data-stu-id="45598-131">-StartTime</span></span>
<span data-ttu-id="45598-132">Especifica uma hora de início.</span><span class="sxs-lookup"><span data-stu-id="45598-132">Specifies a start time.</span></span>
<span data-ttu-id="45598-133">Este cmdlet obtém trabalhos que começam em ou após o tempo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="45598-133">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="45598-134">-Status</span><span class="sxs-lookup"><span data-stu-id="45598-134">-Status</span></span>
<span data-ttu-id="45598-135">Especifica o status dos trabalhos que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="45598-135">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="45598-136">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="45598-136">Valid values are:</span></span> 
- <span data-ttu-id="45598-137">Concluído</span><span class="sxs-lookup"><span data-stu-id="45598-137">Completed</span></span> 
- <span data-ttu-id="45598-138">Falha</span><span class="sxs-lookup"><span data-stu-id="45598-138">Failed</span></span> 
- <span data-ttu-id="45598-139">En fila</span><span class="sxs-lookup"><span data-stu-id="45598-139">Queued</span></span> 
- <span data-ttu-id="45598-140">Iniciando</span><span class="sxs-lookup"><span data-stu-id="45598-140">Starting</span></span> 
- <span data-ttu-id="45598-141">Resumindo</span><span class="sxs-lookup"><span data-stu-id="45598-141">Resuming</span></span> 
- <span data-ttu-id="45598-142">Executando</span><span class="sxs-lookup"><span data-stu-id="45598-142">Running</span></span> 
- <span data-ttu-id="45598-143">Parado</span><span class="sxs-lookup"><span data-stu-id="45598-143">Stopped</span></span> 
- <span data-ttu-id="45598-144">Parando</span><span class="sxs-lookup"><span data-stu-id="45598-144">Stopping</span></span> 
- <span data-ttu-id="45598-145">Suspenso</span><span class="sxs-lookup"><span data-stu-id="45598-145">Suspended</span></span> 
- <span data-ttu-id="45598-146">Suspensão</span><span class="sxs-lookup"><span data-stu-id="45598-146">Suspending</span></span> 
- <span data-ttu-id="45598-147">Ativando</span><span class="sxs-lookup"><span data-stu-id="45598-147">Activating</span></span>
- <span data-ttu-id="45598-148">Novo</span><span class="sxs-lookup"><span data-stu-id="45598-148">New</span></span>

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

### <span data-ttu-id="45598-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45598-149">CommonParameters</span></span>
<span data-ttu-id="45598-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45598-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45598-151">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45598-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45598-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45598-152">INPUTS</span></span>

### <span data-ttu-id="45598-153">System.Guid</span><span class="sxs-lookup"><span data-stu-id="45598-153">System.Guid</span></span>

### <span data-ttu-id="45598-154">System.String</span><span class="sxs-lookup"><span data-stu-id="45598-154">System.String</span></span>

## <span data-ttu-id="45598-155">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="45598-155">OUTPUTS</span></span>

### <span data-ttu-id="45598-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span><span class="sxs-lookup"><span data-stu-id="45598-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="45598-157">NOTES</span><span class="sxs-lookup"><span data-stu-id="45598-157">NOTES</span></span>

## <span data-ttu-id="45598-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45598-158">RELATED LINKS</span></span>

[<span data-ttu-id="45598-159">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="45598-159">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="45598-160">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="45598-160">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


