---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
ms.openlocfilehash: 77b12c17f46c9a04d1166b3066fa5ea9c2df1d74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426744"
---
# <span data-ttu-id="ca577-101">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="ca577-101">Get-AzureRmDataFactorySlice</span></span>

## <span data-ttu-id="ca577-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca577-102">SYNOPSIS</span></span>
<span data-ttu-id="ca577-103">Obtém fatias de dados para um conjunto de dados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="ca577-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca577-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca577-104">SYNTAX</span></span>

### <span data-ttu-id="ca577-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ca577-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ca577-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ca577-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca577-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca577-107">DESCRIPTION</span></span>
<span data-ttu-id="ca577-108">O cmdlet **Get-AzureRmDataFactorySlice** Obtém fatias de dados de um conjunto de dados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="ca577-108">The **Get-AzureRmDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="ca577-109">Especifique uma hora de início e uma hora de término para definir um intervalo de fatias de dados a serem exibidas.</span><span class="sxs-lookup"><span data-stu-id="ca577-109">Specify a start time and an end time to define a range of data slices to view.</span></span>

<span data-ttu-id="ca577-110">O status de uma fatia de dados é um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="ca577-110">The status of a data slice is one of the following values:</span></span> 

- <span data-ttu-id="ca577-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="ca577-111">PendingExecution.</span></span>
<span data-ttu-id="ca577-112">O processamento de dados não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="ca577-112">Data processing has not started.</span></span> 
- <span data-ttu-id="ca577-113">InProgress.</span><span class="sxs-lookup"><span data-stu-id="ca577-113">InProgress.</span></span>
<span data-ttu-id="ca577-114">O processamento de dados está em andamento.</span><span class="sxs-lookup"><span data-stu-id="ca577-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="ca577-115">Está.</span><span class="sxs-lookup"><span data-stu-id="ca577-115">Ready.</span></span>
<span data-ttu-id="ca577-116">O processamento de dados foi concluído.</span><span class="sxs-lookup"><span data-stu-id="ca577-116">Data processing is completed.</span></span>
<span data-ttu-id="ca577-117">A fatia de dados está pronta para fatias dependentes para consumi-la.</span><span class="sxs-lookup"><span data-stu-id="ca577-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="ca577-118">Conseguiu.</span><span class="sxs-lookup"><span data-stu-id="ca577-118">Failed.</span></span>
<span data-ttu-id="ca577-119">Falha na execução que produz a fatia.</span><span class="sxs-lookup"><span data-stu-id="ca577-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="ca577-120">Siga.</span><span class="sxs-lookup"><span data-stu-id="ca577-120">Skip.</span></span>
<span data-ttu-id="ca577-121">O data Factory ignora o processamento da fatia.</span><span class="sxs-lookup"><span data-stu-id="ca577-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="ca577-122">Executar.</span><span class="sxs-lookup"><span data-stu-id="ca577-122">Retry.</span></span>
<span data-ttu-id="ca577-123">O realocador de dados repete a execução que produz a fatia.</span><span class="sxs-lookup"><span data-stu-id="ca577-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="ca577-124">Tempo limite esgotado. O processamento de dados expirou.</span><span class="sxs-lookup"><span data-stu-id="ca577-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="ca577-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="ca577-125">PendingValidation.</span></span>
<span data-ttu-id="ca577-126">A fatia de dados está aguardando a validação antes de ser processada.</span><span class="sxs-lookup"><span data-stu-id="ca577-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="ca577-127">Tente validar novamente.</span><span class="sxs-lookup"><span data-stu-id="ca577-127">Retry Validation.</span></span>
<span data-ttu-id="ca577-128">O realocador de dados repete a validação da fatia.</span><span class="sxs-lookup"><span data-stu-id="ca577-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="ca577-129">Falha na validação.</span><span class="sxs-lookup"><span data-stu-id="ca577-129">Failed Validation.</span></span>
<span data-ttu-id="ca577-130">Falha na validação da fatia.</span><span class="sxs-lookup"><span data-stu-id="ca577-130">Validation of the slice failed.</span></span>

<span data-ttu-id="ca577-131">Para cada uma das fatias, você pode ver mais informações sobre a execução que produz a fatia usando o cmdlet Get-AzureRmDataFactoryRun.</span><span class="sxs-lookup"><span data-stu-id="ca577-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzureRmDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="ca577-132">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca577-132">EXAMPLES</span></span>

### <span data-ttu-id="ca577-133">Exemplo 1: obter fatias de dados de um conjunto de dados</span><span class="sxs-lookup"><span data-stu-id="ca577-133">Example 1: Get data slices for a dataset</span></span>
```
PS C:\>Get-AzureRmDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
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

<span data-ttu-id="ca577-134">Esse comando obtém todas as fatias de dados para o conjunto de dados chamado WikiAggregatedData no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ca577-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="ca577-135">O comando obtém as fatias produzidas após a hora em que o parâmetro StartDatetime especifica.</span><span class="sxs-lookup"><span data-stu-id="ca577-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="ca577-136">O código de exemplo a seguir define a disponibilidade desse conjunto de código a cada hora no arquivo JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="ca577-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>

                        availability: 
                        {
                        period: "Hour",
                        periodMultiplier: 1
                        }

                    Some of the results are Ready and others are PendingExecution.
<span data-ttu-id="ca577-137">As fatias prontas já foram executadas.</span><span class="sxs-lookup"><span data-stu-id="ca577-137">Ready slices have already run.</span></span>
<span data-ttu-id="ca577-138">As faixas pendentes estão aguardando para serem executadas no final de cada hora no intervalo especificado pelo cmdlet de Set-AzureRmDataFactoryPipelineActivePeriod.</span><span class="sxs-lookup"><span data-stu-id="ca577-138">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzureRmDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="ca577-139">Neste exemplo, os períodos de início e término do pipeline e a fatia têm um valor de um dia (24 horas).</span><span class="sxs-lookup"><span data-stu-id="ca577-139">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

## <span data-ttu-id="ca577-140">OS</span><span class="sxs-lookup"><span data-stu-id="ca577-140">PARAMETERS</span></span>

### <span data-ttu-id="ca577-141">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="ca577-141">-DataFactory</span></span>
<span data-ttu-id="ca577-142">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="ca577-142">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ca577-143">Esse cmdlet obtém as fatias que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ca577-143">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca577-144">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="ca577-144">-DataFactoryName</span></span>
<span data-ttu-id="ca577-145">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="ca577-145">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ca577-146">Esse cmdlet obtém as fatias que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ca577-146">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca577-147">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="ca577-147">-DatasetName</span></span>
<span data-ttu-id="ca577-148">Especifica o nome do DataSet para o qual esse cmdlet obtém fatias.</span><span class="sxs-lookup"><span data-stu-id="ca577-148">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca577-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca577-149">-DefaultProfile</span></span>
<span data-ttu-id="ca577-150">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ca577-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca577-151">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="ca577-151">-EndDateTime</span></span>
<span data-ttu-id="ca577-152">Especifica o fim de um período de tempo como um objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="ca577-152">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="ca577-153">Esse cmdlet obtém as fatias geradas antes do tempo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ca577-153">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="ca577-154">Para obter mais informações sobre objetos **DateTime** , digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="ca577-154">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="ca577-155">*EndDateTime* deve ser especificado no formato ISO8601 como nos exemplos a seguir:</span><span class="sxs-lookup"><span data-stu-id="ca577-155">*EndDateTime* must be specified in the ISO8601 format as in the following examples:</span></span> 

<span data-ttu-id="ca577-156">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (hora padrão do Pacífico)</span><span class="sxs-lookup"><span data-stu-id="ca577-156">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="ca577-157">O designador de fuso horário padrão é UTC.</span><span class="sxs-lookup"><span data-stu-id="ca577-157">The default time zone designator is UTC.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca577-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca577-158">-ResourceGroupName</span></span>
<span data-ttu-id="ca577-159">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca577-159">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ca577-160">Esse cmdlet obtém as fatias que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ca577-160">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca577-161">-StartDatetime</span><span class="sxs-lookup"><span data-stu-id="ca577-161">-StartDateTime</span></span>
<span data-ttu-id="ca577-162">Especifica o início de um período de tempo como um objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="ca577-162">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="ca577-163">Esse cmdlet obtém as fatias produzidas após o momento em que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ca577-163">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca577-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca577-164">CommonParameters</span></span>
<span data-ttu-id="ca577-165">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca577-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca577-166">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca577-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca577-167">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca577-167">INPUTS</span></span>

### <span data-ttu-id="ca577-168">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ca577-168">None</span></span>
<span data-ttu-id="ca577-169">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="ca577-169">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ca577-170">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca577-170">OUTPUTS</span></span>

### <span data-ttu-id="ca577-171">System. Collections. Generic. List ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataSlice, Microsoft. WindowsAzure. Commands. Utilities, Version = 0.8.2.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ca577-171">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataSlice, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="ca577-172">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca577-172">NOTES</span></span>
* <span data-ttu-id="ca577-173">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="ca577-173">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ca577-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca577-174">RELATED LINKS</span></span>

[<span data-ttu-id="ca577-175">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="ca577-175">Set-AzureRmDataFactorySliceStatus</span></span>](./Set-AzureRmDataFactorySliceStatus.md)

[<span data-ttu-id="ca577-176">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="ca577-176">Get-AzureRmDataFactoryRun</span></span>](./Get-AzureRmDataFactoryRun.md)

[<span data-ttu-id="ca577-177">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="ca577-177">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)


