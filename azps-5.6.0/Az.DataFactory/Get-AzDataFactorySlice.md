---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: 497899400c05697fb9b273a89743172b672e4892
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888300"
---
# <span data-ttu-id="dcdc1-101">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="dcdc1-101">Get-AzDataFactorySlice</span></span>

## <span data-ttu-id="dcdc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcdc1-102">SYNOPSIS</span></span>
<span data-ttu-id="dcdc1-103">Obtém fatias de dados para um conjuntos de dados no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="dcdc1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dcdc1-104">SYNTAX</span></span>

### <span data-ttu-id="dcdc1-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dcdc1-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dcdc1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="dcdc1-106">ByFactoryObject</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcdc1-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dcdc1-107">DESCRIPTION</span></span>
<span data-ttu-id="dcdc1-108">O cmdlet **Get-AzDataFactorySlice** obtém fatias de dados para um conjuntos de dados no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-108">The **Get-AzDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="dcdc1-109">Especifique uma hora de início e uma hora de término para definir um intervalo de fatias de dados a ser visualizada.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-109">Specify a start time and an end time to define a range of data slices to view.</span></span>
<span data-ttu-id="dcdc1-110">O status de uma fatia de dados é um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="dcdc1-110">The status of a data slice is one of the following values:</span></span> 
- <span data-ttu-id="dcdc1-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-111">PendingExecution.</span></span>
<span data-ttu-id="dcdc1-112">O processamento de dados não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-112">Data processing has not started.</span></span> 
- <span data-ttu-id="dcdc1-113">InProgress.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-113">InProgress.</span></span>
<span data-ttu-id="dcdc1-114">O processamento de dados está em andamento.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="dcdc1-115">Pronto.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-115">Ready.</span></span>
<span data-ttu-id="dcdc1-116">O processamento de dados é concluído.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-116">Data processing is completed.</span></span>
<span data-ttu-id="dcdc1-117">A fatia de dados está pronta para que as fatias dependentes a consumam.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="dcdc1-118">Falha.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-118">Failed.</span></span>
<span data-ttu-id="dcdc1-119">A executar que produz a fatia falhou.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="dcdc1-120">Pule.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-120">Skip.</span></span>
<span data-ttu-id="dcdc1-121">A Fábrica de Dados ignora o processamento da fatia.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="dcdc1-122">Repetir.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-122">Retry.</span></span>
<span data-ttu-id="dcdc1-123">A Fábrica de Dados recupera a executar que produz a fatia.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="dcdc1-124">Tempo de saída. O processamento de dados passou do tempo.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="dcdc1-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-125">PendingValidation.</span></span>
<span data-ttu-id="dcdc1-126">A fatia de dados aguarda a validação antes de ser processada.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="dcdc1-127">Validação de repetir.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-127">Retry Validation.</span></span>
<span data-ttu-id="dcdc1-128">A Fábrica de Dados recupera a validação da fatia.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="dcdc1-129">Validação com falha.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-129">Failed Validation.</span></span>
<span data-ttu-id="dcdc1-130">Falha na validação da fatia.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-130">Validation of the slice failed.</span></span>
<span data-ttu-id="dcdc1-131">Para cada uma das fatias, você pode ver mais informações sobre a executar que produz a fatia usando o cmdlet Get-AzDataFactoryRun.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="dcdc1-132">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dcdc1-132">EXAMPLES</span></span>

### <span data-ttu-id="dcdc1-133">Exemplo 1: Obter fatias de dados para um conjuntos de dados</span><span class="sxs-lookup"><span data-stu-id="dcdc1-133">Example 1: Get data slices for a dataset</span></span>
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

<span data-ttu-id="dcdc1-134">Este comando obtém todas as fatias de dados do grupo de dados chamado WikiAggregatedData no fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="dcdc1-135">O comando obtém fatias produzidas após o tempo especificado pelo parâmetro StartDateTime.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="dcdc1-136">O código de exemplo a seguir define a disponibilidade desse conjunto de dados a cada hora no arquivo JSON (Notação de Objeto JavaScript).</span><span class="sxs-lookup"><span data-stu-id="dcdc1-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="dcdc1-137">availability: { period: "Hour", periodMultiplier: 1 } Alguns dos resultados são Ready e outros são PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-137">availability: { period: "Hour", periodMultiplier: 1 } Some of the results are Ready and others are PendingExecution.</span></span>
<span data-ttu-id="dcdc1-138">As fatias prontas já foram executados.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-138">Ready slices have already run.</span></span>
<span data-ttu-id="dcdc1-139">As fatias pendentes aguardam para ser executados no final de cada hora no intervalo especificado pelo cmdlet Set-AzDataFactoryPipelineActivePeriod.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-139">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="dcdc1-140">Neste exemplo, os períodos inicial e final para o pipeline e a fatia têm um valor de um dia (24 horas).</span><span class="sxs-lookup"><span data-stu-id="dcdc1-140">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

### <span data-ttu-id="dcdc1-141">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="dcdc1-141">Example 2</span></span>

<span data-ttu-id="dcdc1-142">Obtém fatias de dados para um conjuntos de dados no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-142">Gets data slices for a dataset in Azure Data Factory.</span></span> <span data-ttu-id="dcdc1-143">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="dcdc1-143">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## <span data-ttu-id="dcdc1-144">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dcdc1-144">PARAMETERS</span></span>

### <span data-ttu-id="dcdc1-145">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="dcdc1-145">-DataFactory</span></span>
<span data-ttu-id="dcdc1-146">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="dcdc1-146">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="dcdc1-147">Este cmdlet obtém fatias que pertencem ao fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-147">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="dcdc1-148">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="dcdc1-148">-DataFactoryName</span></span>
<span data-ttu-id="dcdc1-149">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-149">Specifies the name of a data factory.</span></span>
<span data-ttu-id="dcdc1-150">Este cmdlet obtém fatias que pertencem ao fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-150">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="dcdc1-151">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="dcdc1-151">-DatasetName</span></span>
<span data-ttu-id="dcdc1-152">Especifica o nome do conjuntos de dados para o qual este cmdlet obtém fatias.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-152">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

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

### <span data-ttu-id="dcdc1-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcdc1-153">-DefaultProfile</span></span>
<span data-ttu-id="dcdc1-154">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="dcdc1-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dcdc1-155">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="dcdc1-155">-EndDateTime</span></span>
<span data-ttu-id="dcdc1-156">Especifica o fim de um período de tempo como um **objeto DateTime.**</span><span class="sxs-lookup"><span data-stu-id="dcdc1-156">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="dcdc1-157">Este cmdlet obtém fatias produzidas antes do tempo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-157">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="dcdc1-158">Para obter mais informações sobre **objetos DateTime,** digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="dcdc1-158">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="dcdc1-159">*EndDateTime* deve ser especificado no formato ISO8601, como nos seguintes exemplos: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Hora Padrão do Pacífico) O designador de fuso horário padrão é UTC.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-159">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="dcdc1-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcdc1-160">-ResourceGroupName</span></span>
<span data-ttu-id="dcdc1-161">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-161">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="dcdc1-162">Este cmdlet obtém fatias que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-162">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="dcdc1-163">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="dcdc1-163">-StartDateTime</span></span>
<span data-ttu-id="dcdc1-164">Especifica o início de um período de tempo como um **objeto DateTime.**</span><span class="sxs-lookup"><span data-stu-id="dcdc1-164">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="dcdc1-165">Este cmdlet obtém fatias produzidas após o tempo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-165">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="dcdc1-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcdc1-166">CommonParameters</span></span>
<span data-ttu-id="dcdc1-167">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcdc1-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcdc1-168">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcdc1-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcdc1-169">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dcdc1-169">INPUTS</span></span>

### <span data-ttu-id="dcdc1-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="dcdc1-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="dcdc1-171">System.String</span><span class="sxs-lookup"><span data-stu-id="dcdc1-171">System.String</span></span>

## <span data-ttu-id="dcdc1-172">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dcdc1-172">OUTPUTS</span></span>

### <span data-ttu-id="dcdc1-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span><span class="sxs-lookup"><span data-stu-id="dcdc1-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span></span>

## <span data-ttu-id="dcdc1-174">NOTES</span><span class="sxs-lookup"><span data-stu-id="dcdc1-174">NOTES</span></span>
* <span data-ttu-id="dcdc1-175">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="dcdc1-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="dcdc1-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dcdc1-176">RELATED LINKS</span></span>

[<span data-ttu-id="dcdc1-177">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="dcdc1-177">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)

[<span data-ttu-id="dcdc1-178">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="dcdc1-178">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="dcdc1-179">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="dcdc1-179">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


