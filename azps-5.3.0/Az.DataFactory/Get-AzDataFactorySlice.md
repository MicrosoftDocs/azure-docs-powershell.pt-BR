---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: a71ccc37fe1c6b6811b955c5d84353dfecd66c2f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429915"
---
# <span data-ttu-id="9f163-101">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="9f163-101">Get-AzDataFactorySlice</span></span>

## <span data-ttu-id="9f163-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f163-102">SYNOPSIS</span></span>
<span data-ttu-id="9f163-103">Obtém fatias de dados para um conjunto de dados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="9f163-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="9f163-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f163-104">SYNTAX</span></span>

### <span data-ttu-id="9f163-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="9f163-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f163-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9f163-106">ByFactoryObject</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f163-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9f163-107">DESCRIPTION</span></span>
<span data-ttu-id="9f163-108">O cmdlet **Get-AzDataFactorySlice** Obtém fatias de dados de um conjunto de dados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="9f163-108">The **Get-AzDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="9f163-109">Especifique uma hora de início e uma hora de término para definir um intervalo de fatias de dados a serem exibidas.</span><span class="sxs-lookup"><span data-stu-id="9f163-109">Specify a start time and an end time to define a range of data slices to view.</span></span>
<span data-ttu-id="9f163-110">O status de uma fatia de dados é um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="9f163-110">The status of a data slice is one of the following values:</span></span> 
- <span data-ttu-id="9f163-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="9f163-111">PendingExecution.</span></span>
<span data-ttu-id="9f163-112">O processamento de dados não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="9f163-112">Data processing has not started.</span></span> 
- <span data-ttu-id="9f163-113">InProgress.</span><span class="sxs-lookup"><span data-stu-id="9f163-113">InProgress.</span></span>
<span data-ttu-id="9f163-114">O processamento de dados está em andamento.</span><span class="sxs-lookup"><span data-stu-id="9f163-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="9f163-115">Está.</span><span class="sxs-lookup"><span data-stu-id="9f163-115">Ready.</span></span>
<span data-ttu-id="9f163-116">O processamento de dados foi concluído.</span><span class="sxs-lookup"><span data-stu-id="9f163-116">Data processing is completed.</span></span>
<span data-ttu-id="9f163-117">A fatia de dados está pronta para fatias dependentes para consumi-la.</span><span class="sxs-lookup"><span data-stu-id="9f163-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="9f163-118">Conseguiu.</span><span class="sxs-lookup"><span data-stu-id="9f163-118">Failed.</span></span>
<span data-ttu-id="9f163-119">Falha na execução que produz a fatia.</span><span class="sxs-lookup"><span data-stu-id="9f163-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="9f163-120">Siga.</span><span class="sxs-lookup"><span data-stu-id="9f163-120">Skip.</span></span>
<span data-ttu-id="9f163-121">O data Factory ignora o processamento da fatia.</span><span class="sxs-lookup"><span data-stu-id="9f163-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="9f163-122">Executar.</span><span class="sxs-lookup"><span data-stu-id="9f163-122">Retry.</span></span>
<span data-ttu-id="9f163-123">O realocador de dados repete a execução que produz a fatia.</span><span class="sxs-lookup"><span data-stu-id="9f163-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="9f163-124">Tempo limite esgotado. O processamento de dados expirou.</span><span class="sxs-lookup"><span data-stu-id="9f163-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="9f163-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="9f163-125">PendingValidation.</span></span>
<span data-ttu-id="9f163-126">A fatia de dados está aguardando a validação antes de ser processada.</span><span class="sxs-lookup"><span data-stu-id="9f163-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="9f163-127">Tente validar novamente.</span><span class="sxs-lookup"><span data-stu-id="9f163-127">Retry Validation.</span></span>
<span data-ttu-id="9f163-128">O realocador de dados repete a validação da fatia.</span><span class="sxs-lookup"><span data-stu-id="9f163-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="9f163-129">Falha na validação.</span><span class="sxs-lookup"><span data-stu-id="9f163-129">Failed Validation.</span></span>
<span data-ttu-id="9f163-130">Falha na validação da fatia.</span><span class="sxs-lookup"><span data-stu-id="9f163-130">Validation of the slice failed.</span></span>
<span data-ttu-id="9f163-131">Para cada uma das fatias, você pode ver mais informações sobre a execução que produz a fatia usando o cmdlet Get-AzDataFactoryRun.</span><span class="sxs-lookup"><span data-stu-id="9f163-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="9f163-132">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f163-132">EXAMPLES</span></span>

### <span data-ttu-id="9f163-133">Exemplo 1: obter fatias de dados de um conjunto de dados</span><span class="sxs-lookup"><span data-stu-id="9f163-133">Example 1: Get data slices for a dataset</span></span>
```powershell
PS C:\>Get-AzDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 1:00:00 AM
End               : 5/21/2014 2:00:00 AM
RetryCount        : 0
Status            : Ready

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 2:00:00 AM
End               : 5/21/2014 3:00:00 AM
RetryCount        : 0
Status            : Ready

. . . 

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 8:00:00 PM
End               : 5/21/2014 9:00:00 PM
RetryCount        : 0
Status            : PendingExecution

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 9:00:00 PM
End               : 5/21/2014 10:00:00 PM
RetryCount        : 0
Status            : PendingExecution

. . .
```

<span data-ttu-id="9f163-134">Esse comando obtém todas as fatias de dados para o conjunto de dados chamado WikiAggregatedData no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="9f163-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="9f163-135">O comando obtém as fatias produzidas após a hora em que o parâmetro StartDatetime especifica.</span><span class="sxs-lookup"><span data-stu-id="9f163-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="9f163-136">O código de exemplo a seguir define a disponibilidade desse conjunto de código a cada hora no arquivo JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="9f163-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="9f163-137">disponibilidade: {período: "hora", periodMultiplier: 1} alguns dos resultados estão prontos e outros são PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="9f163-137">availability: { period: "Hour", periodMultiplier: 1 } Some of the results are Ready and others are PendingExecution.</span></span>
<span data-ttu-id="9f163-138">As fatias prontas já foram executadas.</span><span class="sxs-lookup"><span data-stu-id="9f163-138">Ready slices have already run.</span></span>
<span data-ttu-id="9f163-139">As faixas pendentes estão aguardando para serem executadas no final de cada hora no intervalo especificado pelo cmdlet de Set-AzDataFactoryPipelineActivePeriod.</span><span class="sxs-lookup"><span data-stu-id="9f163-139">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="9f163-140">Neste exemplo, os períodos de início e término do pipeline e a fatia têm um valor de um dia (24 horas).</span><span class="sxs-lookup"><span data-stu-id="9f163-140">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

### <span data-ttu-id="9f163-141">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9f163-141">Example 2</span></span>

<span data-ttu-id="9f163-142">Obtém fatias de dados para um conjunto de dados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="9f163-142">Gets data slices for a dataset in Azure Data Factory.</span></span> <span data-ttu-id="9f163-143">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="9f163-143">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## <span data-ttu-id="9f163-144">OS</span><span class="sxs-lookup"><span data-stu-id="9f163-144">PARAMETERS</span></span>

### <span data-ttu-id="9f163-145">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="9f163-145">-DataFactory</span></span>
<span data-ttu-id="9f163-146">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="9f163-146">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="9f163-147">Esse cmdlet obtém as fatias que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="9f163-147">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f163-148">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="9f163-148">-DataFactoryName</span></span>
<span data-ttu-id="9f163-149">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="9f163-149">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9f163-150">Esse cmdlet obtém as fatias que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="9f163-150">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f163-151">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="9f163-151">-DatasetName</span></span>
<span data-ttu-id="9f163-152">Especifica o nome do DataSet para o qual esse cmdlet obtém fatias.</span><span class="sxs-lookup"><span data-stu-id="9f163-152">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

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

### <span data-ttu-id="9f163-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f163-153">-DefaultProfile</span></span>
<span data-ttu-id="9f163-154">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9f163-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f163-155">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="9f163-155">-EndDateTime</span></span>
<span data-ttu-id="9f163-156">Especifica o fim de um período de tempo como um objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="9f163-156">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="9f163-157">Esse cmdlet obtém as fatias geradas antes do tempo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="9f163-157">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="9f163-158">Para obter mais informações sobre objetos **DateTime** , digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="9f163-158">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="9f163-159">*EndDateTime* deve ser especificado no formato ISO8601 como nos exemplos a seguir: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (hora padrão do Pacífico) o designador de fuso horário padrão é UTC.</span><span class="sxs-lookup"><span data-stu-id="9f163-159">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f163-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f163-160">-ResourceGroupName</span></span>
<span data-ttu-id="9f163-161">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="9f163-161">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9f163-162">Esse cmdlet obtém as fatias que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9f163-162">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f163-163">-StartDatetime</span><span class="sxs-lookup"><span data-stu-id="9f163-163">-StartDateTime</span></span>
<span data-ttu-id="9f163-164">Especifica o início de um período de tempo como um objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="9f163-164">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="9f163-165">Esse cmdlet obtém as fatias produzidas após o momento em que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="9f163-165">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f163-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f163-166">CommonParameters</span></span>
<span data-ttu-id="9f163-167">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f163-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f163-168">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f163-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f163-169">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9f163-169">INPUTS</span></span>

### <span data-ttu-id="9f163-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9f163-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="9f163-171">System. String</span><span class="sxs-lookup"><span data-stu-id="9f163-171">System.String</span></span>

## <span data-ttu-id="9f163-172">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9f163-172">OUTPUTS</span></span>

### <span data-ttu-id="9f163-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span><span class="sxs-lookup"><span data-stu-id="9f163-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span></span>

## <span data-ttu-id="9f163-174">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9f163-174">NOTES</span></span>
* <span data-ttu-id="9f163-175">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="9f163-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9f163-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f163-176">RELATED LINKS</span></span>

[<span data-ttu-id="9f163-177">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="9f163-177">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)

[<span data-ttu-id="9f163-178">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="9f163-178">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="9f163-179">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="9f163-179">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


