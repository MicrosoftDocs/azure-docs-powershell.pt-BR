---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
ms.openlocfilehash: 59263dab3037e050229bab2a69c43559c2c1827b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432678"
---
# <span data-ttu-id="a1226-101">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="a1226-101">Get-AzureRmAutomationDscCompilationJob</span></span>

## <span data-ttu-id="a1226-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1226-102">SYNOPSIS</span></span>
<span data-ttu-id="a1226-103">Obtém trabalhos de compilação DSC na automação.</span><span class="sxs-lookup"><span data-stu-id="a1226-103">Gets DSC compilation jobs in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1226-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1226-104">SYNTAX</span></span>

### <span data-ttu-id="a1226-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="a1226-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1226-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="a1226-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1226-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a1226-107">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>]
 [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1226-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1226-108">DESCRIPTION</span></span>
<span data-ttu-id="a1226-109">O cmdlet **Get-AzureRmAutomationDscCompilationJob** Obtém os trabalhos de compilação de DSC (configuração de estado desejado) do APS na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="a1226-109">The **Get-AzureRmAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="a1226-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1226-110">EXAMPLES</span></span>

### <span data-ttu-id="a1226-111">Exemplo 1: obter todos os trabalhos de compilação DSC</span><span class="sxs-lookup"><span data-stu-id="a1226-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="a1226-112">Esse comando obtém todos os trabalhos de compilação na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a1226-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="a1226-113">Exemplo 2: obter trabalhos de compilação DSC para uma configuração</span><span class="sxs-lookup"><span data-stu-id="a1226-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="a1226-114">Esse comando obtém todos os trabalhos de compilação para a configuração DSC chamada ContosoConfiguration na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a1226-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="a1226-115">Exemplo 3: obter um trabalho de compilação DSC específico</span><span class="sxs-lookup"><span data-stu-id="a1226-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="a1226-116">Esse comando obtém o trabalho de compilação com a ID especificada na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a1226-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a1226-117">OS</span><span class="sxs-lookup"><span data-stu-id="a1226-117">PARAMETERS</span></span>

### <span data-ttu-id="a1226-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a1226-118">-AutomationAccountName</span></span>
<span data-ttu-id="a1226-119">Especifica o nome da conta de automação que contém os trabalhos de compilação DSC que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="a1226-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a1226-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a1226-120">-ConfigurationName</span></span>
<span data-ttu-id="a1226-121">Especifica o nome da configuração DSC para a qual esse cmdlet obtém trabalhos de compilação.</span><span class="sxs-lookup"><span data-stu-id="a1226-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

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

### <span data-ttu-id="a1226-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="a1226-122">-EndTime</span></span>
<span data-ttu-id="a1226-123">Especifica uma hora de término.</span><span class="sxs-lookup"><span data-stu-id="a1226-123">Specifies an end time.</span></span>
<span data-ttu-id="a1226-124">Esse cmdlet obtém trabalhos de compilação que começaram até o momento em que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="a1226-124">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="a1226-125">-ID</span><span class="sxs-lookup"><span data-stu-id="a1226-125">-Id</span></span>
<span data-ttu-id="a1226-126">Especifica a ID exclusiva do trabalho de compilação DSC que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="a1226-126">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a1226-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1226-127">-ResourceGroupName</span></span>
<span data-ttu-id="a1226-128">Especifica o nome de um grupo de recursos em que esse cmdlet obtém trabalhos de compilação DSC.</span><span class="sxs-lookup"><span data-stu-id="a1226-128">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="a1226-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a1226-129">-StartTime</span></span>
<span data-ttu-id="a1226-130">Especifica uma hora de início.</span><span class="sxs-lookup"><span data-stu-id="a1226-130">Specifies a start time.</span></span>
<span data-ttu-id="a1226-131">Este cmdlet obtém trabalhos que iniciam em ou após o momento em que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="a1226-131">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="a1226-132">-Status</span><span class="sxs-lookup"><span data-stu-id="a1226-132">-Status</span></span>
<span data-ttu-id="a1226-133">Especifica o status dos trabalhos que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="a1226-133">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="a1226-134">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="a1226-134">Valid values are:</span></span> 

- <span data-ttu-id="a1226-135">Feito</span><span class="sxs-lookup"><span data-stu-id="a1226-135">Completed</span></span> 
- <span data-ttu-id="a1226-136">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="a1226-136">Failed</span></span> 
- <span data-ttu-id="a1226-137">Na fila</span><span class="sxs-lookup"><span data-stu-id="a1226-137">Queued</span></span> 
- <span data-ttu-id="a1226-138">Iniciais</span><span class="sxs-lookup"><span data-stu-id="a1226-138">Starting</span></span> 
- <span data-ttu-id="a1226-139">Resuming</span><span class="sxs-lookup"><span data-stu-id="a1226-139">Resuming</span></span> 
- <span data-ttu-id="a1226-140">Executando</span><span class="sxs-lookup"><span data-stu-id="a1226-140">Running</span></span> 
- <span data-ttu-id="a1226-141">Terminou</span><span class="sxs-lookup"><span data-stu-id="a1226-141">Stopped</span></span> 
- <span data-ttu-id="a1226-142">Interromper</span><span class="sxs-lookup"><span data-stu-id="a1226-142">Stopping</span></span> 
- <span data-ttu-id="a1226-143">Interrompido</span><span class="sxs-lookup"><span data-stu-id="a1226-143">Suspended</span></span> 
- <span data-ttu-id="a1226-144">Suspending</span><span class="sxs-lookup"><span data-stu-id="a1226-144">Suspending</span></span> 
- <span data-ttu-id="a1226-145">Activa</span><span class="sxs-lookup"><span data-stu-id="a1226-145">Activating</span></span>
- <span data-ttu-id="a1226-146">Novo</span><span class="sxs-lookup"><span data-stu-id="a1226-146">New</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases: 
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1226-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1226-147">-DefaultProfile</span></span>
<span data-ttu-id="a1226-148">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1226-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1226-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1226-149">CommonParameters</span></span>
<span data-ttu-id="a1226-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1226-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1226-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1226-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1226-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1226-152">INPUTS</span></span>

## <span data-ttu-id="a1226-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1226-153">OUTPUTS</span></span>

### <span data-ttu-id="a1226-154">Microsoft. Azure. Commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="a1226-154">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="a1226-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1226-155">NOTES</span></span>

## <span data-ttu-id="a1226-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1226-156">RELATED LINKS</span></span>

[<span data-ttu-id="a1226-157">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="a1226-157">Get-AzureRmAutomationDscCompilationJobOutput</span></span>](./Get-AzureRmAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="a1226-158">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="a1226-158">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

