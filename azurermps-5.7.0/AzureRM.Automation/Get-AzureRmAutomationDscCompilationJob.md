---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
ms.openlocfilehash: c7e4043cb6883020b8af15d13dd46c395997e116
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441502"
---
# <span data-ttu-id="bfcc6-101">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="bfcc6-101">Get-AzureRmAutomationDscCompilationJob</span></span>

## <span data-ttu-id="bfcc6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bfcc6-102">SYNOPSIS</span></span>
<span data-ttu-id="bfcc6-103">Obtém trabalhos de compilação DSC na automação.</span><span class="sxs-lookup"><span data-stu-id="bfcc6-103">Gets DSC compilation jobs in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfcc6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bfcc6-104">SYNTAX</span></span>

### <span data-ttu-id="bfcc6-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="bfcc6-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfcc6-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="bfcc6-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfcc6-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="bfcc6-107">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>]
 [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfcc6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bfcc6-108">DESCRIPTION</span></span>
<span data-ttu-id="bfcc6-109">O cmdlet **Get-AzureRmAutomationDscCompilationJob** Obtém os trabalhos de compilação de DSC (configuração de estado desejado) do APS na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="bfcc6-109">The **Get-AzureRmAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="bfcc6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bfcc6-110">EXAMPLES</span></span>

### <span data-ttu-id="bfcc6-111">Exemplo 1: obter todos os trabalhos de compilação DSC</span><span class="sxs-lookup"><span data-stu-id="bfcc6-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="bfcc6-112">Esse comando obtém todos os trabalhos de compilação na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="bfcc6-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="bfcc6-113">Exemplo 2: obter trabalhos de compilação DSC para uma configuração</span><span class="sxs-lookup"><span data-stu-id="bfcc6-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="bfcc6-114">Esse comando obtém todos os trabalhos de compilação para a configuração DSC chamada ContosoConfiguration na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="bfcc6-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="bfcc6-115">Exemplo 3: obter um trabalho de compilação DSC específico</span><span class="sxs-lookup"><span data-stu-id="bfcc6-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="bfcc6-116">Esse comando obtém o trabalho de compilação com a ID especificada na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="bfcc6-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="bfcc6-117">OS</span><span class="sxs-lookup"><span data-stu-id="bfcc6-117">PARAMETERS</span></span>

### <span data-ttu-id="bfcc6-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bfcc6-118">-AutomationAccountName</span></span>
<span data-ttu-id="bfcc6-119">Especifica o nome da conta de automação que contém os trabalhos de compilação DSC que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="bfcc6-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfcc6-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="bfcc6-120">-ConfigurationName</span></span>
<span data-ttu-id="bfcc6-121">Especifica o nome da configuração DSC para a qual esse cmdlet obtém trabalhos de compilação.</span><span class="sxs-lookup"><span data-stu-id="bfcc6-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

```yaml
Type: String
Parameter Sets: ByConfigurationName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcc6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfcc6-122">-DefaultProfile</span></span>
<span data-ttu-id="bfcc6-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="bfcc6-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcc6-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="bfcc6-124">-EndTime</span></span>
<span data-ttu-id="bfcc6-125">Especifica uma hora de término.</span><span class="sxs-lookup"><span data-stu-id="bfcc6-125">Specifies an end time.</span></span>
<span data-ttu-id="bfcc6-126">Esse cmdlet obtém trabalhos de compilação que começaram até o momento em que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="bfcc6-126">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByConfigurationName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcc6-127">-ID</span><span class="sxs-lookup"><span data-stu-id="bfcc6-127">-Id</span></span>
<span data-ttu-id="bfcc6-128">Especifica a ID exclusiva do trabalho de compilação DSC que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="bfcc6-128">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfcc6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfcc6-129">-ResourceGroupName</span></span>
<span data-ttu-id="bfcc6-130">Especifica o nome de um grupo de recursos em que esse cmdlet obtém trabalhos de compilação DSC.</span><span class="sxs-lookup"><span data-stu-id="bfcc6-130">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfcc6-131">-StartTime</span><span class="sxs-lookup"><span data-stu-id="bfcc6-131">-StartTime</span></span>
<span data-ttu-id="bfcc6-132">Especifica uma hora de início.</span><span class="sxs-lookup"><span data-stu-id="bfcc6-132">Specifies a start time.</span></span>
<span data-ttu-id="bfcc6-133">Este cmdlet obtém trabalhos que iniciam em ou após o momento em que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="bfcc6-133">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByConfigurationName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcc6-134">-Status</span><span class="sxs-lookup"><span data-stu-id="bfcc6-134">-Status</span></span>
<span data-ttu-id="bfcc6-135">Especifica o status dos trabalhos que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="bfcc6-135">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="bfcc6-136">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="bfcc6-136">Valid values are:</span></span> 

- <span data-ttu-id="bfcc6-137">Feito</span><span class="sxs-lookup"><span data-stu-id="bfcc6-137">Completed</span></span> 
- <span data-ttu-id="bfcc6-138">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="bfcc6-138">Failed</span></span> 
- <span data-ttu-id="bfcc6-139">Na fila</span><span class="sxs-lookup"><span data-stu-id="bfcc6-139">Queued</span></span> 
- <span data-ttu-id="bfcc6-140">Iniciais</span><span class="sxs-lookup"><span data-stu-id="bfcc6-140">Starting</span></span> 
- <span data-ttu-id="bfcc6-141">Resuming</span><span class="sxs-lookup"><span data-stu-id="bfcc6-141">Resuming</span></span> 
- <span data-ttu-id="bfcc6-142">Executando</span><span class="sxs-lookup"><span data-stu-id="bfcc6-142">Running</span></span> 
- <span data-ttu-id="bfcc6-143">Terminou</span><span class="sxs-lookup"><span data-stu-id="bfcc6-143">Stopped</span></span> 
- <span data-ttu-id="bfcc6-144">Interromper</span><span class="sxs-lookup"><span data-stu-id="bfcc6-144">Stopping</span></span> 
- <span data-ttu-id="bfcc6-145">Interrompido</span><span class="sxs-lookup"><span data-stu-id="bfcc6-145">Suspended</span></span> 
- <span data-ttu-id="bfcc6-146">Suspending</span><span class="sxs-lookup"><span data-stu-id="bfcc6-146">Suspending</span></span> 
- <span data-ttu-id="bfcc6-147">Activa</span><span class="sxs-lookup"><span data-stu-id="bfcc6-147">Activating</span></span>
- <span data-ttu-id="bfcc6-148">Novo</span><span class="sxs-lookup"><span data-stu-id="bfcc6-148">New</span></span>

```yaml
Type: String
Parameter Sets: ByAll, ByConfigurationName
Aliases: 
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating, New

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcc6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfcc6-149">CommonParameters</span></span>
<span data-ttu-id="bfcc6-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfcc6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfcc6-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfcc6-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfcc6-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bfcc6-152">INPUTS</span></span>

### <span data-ttu-id="bfcc6-153">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="bfcc6-153">None</span></span>
<span data-ttu-id="bfcc6-154">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="bfcc6-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bfcc6-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bfcc6-155">OUTPUTS</span></span>

### <span data-ttu-id="bfcc6-156">Microsoft. Azure. Commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="bfcc6-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="bfcc6-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bfcc6-157">NOTES</span></span>

## <span data-ttu-id="bfcc6-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfcc6-158">RELATED LINKS</span></span>

[<span data-ttu-id="bfcc6-159">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="bfcc6-159">Get-AzureRmAutomationDscCompilationJobOutput</span></span>](./Get-AzureRmAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="bfcc6-160">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="bfcc6-160">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)


