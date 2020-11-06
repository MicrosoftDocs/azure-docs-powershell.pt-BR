---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
ms.openlocfilehash: 50942dfc9b31b96a796b0a77df8b1ffc1a4cbd36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610607"
---
# <span data-ttu-id="512b8-101">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="512b8-101">Get-AzureRmDataFactorySlice</span></span>

## <span data-ttu-id="512b8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="512b8-102">SYNOPSIS</span></span>
<span data-ttu-id="512b8-103">Obtém fatias de dados para um conjunto de dados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="512b8-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="512b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="512b8-104">SYNTAX</span></span>

### <span data-ttu-id="512b8-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="512b8-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="512b8-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="512b8-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="512b8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="512b8-107">DESCRIPTION</span></span>
<span data-ttu-id="512b8-108">O cmdlet **Get-AzureRmDataFactorySlice** Obtém fatias de dados de um conjunto de dados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="512b8-108">The **Get-AzureRmDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="512b8-109">Especifique uma hora de início e uma hora de término para definir um intervalo de fatias de dados a serem exibidas.</span><span class="sxs-lookup"><span data-stu-id="512b8-109">Specify a start time and an end time to define a range of data slices to view.</span></span>
<span data-ttu-id="512b8-110">O status de uma fatia de dados é um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="512b8-110">The status of a data slice is one of the following values:</span></span> 
- <span data-ttu-id="512b8-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="512b8-111">PendingExecution.</span></span>
<span data-ttu-id="512b8-112">O processamento de dados não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="512b8-112">Data processing has not started.</span></span> 
- <span data-ttu-id="512b8-113">InProgress.</span><span class="sxs-lookup"><span data-stu-id="512b8-113">InProgress.</span></span>
<span data-ttu-id="512b8-114">O processamento de dados está em andamento.</span><span class="sxs-lookup"><span data-stu-id="512b8-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="512b8-115">Está.</span><span class="sxs-lookup"><span data-stu-id="512b8-115">Ready.</span></span>
<span data-ttu-id="512b8-116">O processamento de dados foi concluído.</span><span class="sxs-lookup"><span data-stu-id="512b8-116">Data processing is completed.</span></span>
<span data-ttu-id="512b8-117">A fatia de dados está pronta para fatias dependentes para consumi-la.</span><span class="sxs-lookup"><span data-stu-id="512b8-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="512b8-118">Conseguiu.</span><span class="sxs-lookup"><span data-stu-id="512b8-118">Failed.</span></span>
<span data-ttu-id="512b8-119">Falha na execução que produz a fatia.</span><span class="sxs-lookup"><span data-stu-id="512b8-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="512b8-120">Siga.</span><span class="sxs-lookup"><span data-stu-id="512b8-120">Skip.</span></span>
<span data-ttu-id="512b8-121">O data Factory ignora o processamento da fatia.</span><span class="sxs-lookup"><span data-stu-id="512b8-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="512b8-122">Executar.</span><span class="sxs-lookup"><span data-stu-id="512b8-122">Retry.</span></span>
<span data-ttu-id="512b8-123">O realocador de dados repete a execução que produz a fatia.</span><span class="sxs-lookup"><span data-stu-id="512b8-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="512b8-124">Tempo limite esgotado. O processamento de dados expirou.</span><span class="sxs-lookup"><span data-stu-id="512b8-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="512b8-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="512b8-125">PendingValidation.</span></span>
<span data-ttu-id="512b8-126">A fatia de dados está aguardando a validação antes de ser processada.</span><span class="sxs-lookup"><span data-stu-id="512b8-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="512b8-127">Tente validar novamente.</span><span class="sxs-lookup"><span data-stu-id="512b8-127">Retry Validation.</span></span>
<span data-ttu-id="512b8-128">O realocador de dados repete a validação da fatia.</span><span class="sxs-lookup"><span data-stu-id="512b8-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="512b8-129">Falha na validação.</span><span class="sxs-lookup"><span data-stu-id="512b8-129">Failed Validation.</span></span>
<span data-ttu-id="512b8-130">Falha na validação da fatia.</span><span class="sxs-lookup"><span data-stu-id="512b8-130">Validation of the slice failed.</span></span>
<span data-ttu-id="512b8-131">Para cada uma das fatias, você pode ver mais informações sobre a execução que produz a fatia usando o cmdlet Get-AzureRmDataFactoryRun.</span><span class="sxs-lookup"><span data-stu-id="512b8-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzureRmDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="512b8-132">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="512b8-132">EXAMPLES</span></span>

### <span data-ttu-id="512b8-133">Exemplo 1: obter fatias de dados de um conjunto de dados</span><span class="sxs-lookup"><span data-stu-id="512b8-133">Example 1: Get data slices for a dataset</span></span>
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

<span data-ttu-id="512b8-134">Esse comando obtém todas as fatias de dados para o conjunto de dados chamado WikiAggregatedData no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="512b8-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="512b8-135">O comando obtém as fatias produzidas após a hora em que o parâmetro StartDatetime especifica.</span><span class="sxs-lookup"><span data-stu-id="512b8-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="512b8-136">O código de exemplo a seguir define a disponibilidade desse conjunto de código a cada hora no arquivo JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="512b8-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="512b8-137">disponibilidade: {período: "hora", periodMultiplier: 1} alguns dos resultados estão prontos e outros são PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="512b8-137">availability: { period: "Hour", periodMultiplier: 1 } Some of the results are Ready and others are PendingExecution.</span></span>
<span data-ttu-id="512b8-138">As fatias prontas já foram executadas.</span><span class="sxs-lookup"><span data-stu-id="512b8-138">Ready slices have already run.</span></span>
<span data-ttu-id="512b8-139">As faixas pendentes estão aguardando para serem executadas no final de cada hora no intervalo especificado pelo cmdlet de Set-AzureRmDataFactoryPipelineActivePeriod.</span><span class="sxs-lookup"><span data-stu-id="512b8-139">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzureRmDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="512b8-140">Neste exemplo, os períodos de início e término do pipeline e a fatia têm um valor de um dia (24 horas).</span><span class="sxs-lookup"><span data-stu-id="512b8-140">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

## <span data-ttu-id="512b8-141">OS</span><span class="sxs-lookup"><span data-stu-id="512b8-141">PARAMETERS</span></span>

### <span data-ttu-id="512b8-142">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="512b8-142">-DataFactory</span></span>
<span data-ttu-id="512b8-143">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="512b8-143">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="512b8-144">Esse cmdlet obtém as fatias que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="512b8-144">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="512b8-145">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="512b8-145">-DataFactoryName</span></span>
<span data-ttu-id="512b8-146">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="512b8-146">Specifies the name of a data factory.</span></span>
<span data-ttu-id="512b8-147">Esse cmdlet obtém as fatias que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="512b8-147">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="512b8-148">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="512b8-148">-DatasetName</span></span>
<span data-ttu-id="512b8-149">Especifica o nome do DataSet para o qual esse cmdlet obtém fatias.</span><span class="sxs-lookup"><span data-stu-id="512b8-149">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

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

### <span data-ttu-id="512b8-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="512b8-150">-DefaultProfile</span></span>
<span data-ttu-id="512b8-151">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="512b8-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="512b8-152">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="512b8-152">-EndDateTime</span></span>
<span data-ttu-id="512b8-153">Especifica o fim de um período de tempo como um objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="512b8-153">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="512b8-154">Esse cmdlet obtém as fatias geradas antes do tempo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="512b8-154">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="512b8-155">Para obter mais informações sobre objetos **DateTime** , digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="512b8-155">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="512b8-156">*EndDateTime* deve ser especificado no formato ISO8601 como nos exemplos a seguir: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (hora padrão do Pacífico) o designador de fuso horário padrão é UTC.</span><span class="sxs-lookup"><span data-stu-id="512b8-156">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="512b8-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="512b8-157">-ResourceGroupName</span></span>
<span data-ttu-id="512b8-158">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="512b8-158">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="512b8-159">Esse cmdlet obtém as fatias que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="512b8-159">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="512b8-160">-StartDatetime</span><span class="sxs-lookup"><span data-stu-id="512b8-160">-StartDateTime</span></span>
<span data-ttu-id="512b8-161">Especifica o início de um período de tempo como um objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="512b8-161">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="512b8-162">Esse cmdlet obtém as fatias produzidas após o momento em que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="512b8-162">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="512b8-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="512b8-163">CommonParameters</span></span>
<span data-ttu-id="512b8-164">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="512b8-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="512b8-165">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="512b8-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="512b8-166">SENSORES</span><span class="sxs-lookup"><span data-stu-id="512b8-166">INPUTS</span></span>

### <span data-ttu-id="512b8-167">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="512b8-167">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="512b8-168">System. String</span><span class="sxs-lookup"><span data-stu-id="512b8-168">System.String</span></span>

## <span data-ttu-id="512b8-169">EXIBE</span><span class="sxs-lookup"><span data-stu-id="512b8-169">OUTPUTS</span></span>

### <span data-ttu-id="512b8-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span><span class="sxs-lookup"><span data-stu-id="512b8-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span></span>

## <span data-ttu-id="512b8-171">INFORMA</span><span class="sxs-lookup"><span data-stu-id="512b8-171">NOTES</span></span>
* <span data-ttu-id="512b8-172">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="512b8-172">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="512b8-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="512b8-173">RELATED LINKS</span></span>

[<span data-ttu-id="512b8-174">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="512b8-174">Set-AzureRmDataFactorySliceStatus</span></span>](./Set-AzureRmDataFactorySliceStatus.md)

[<span data-ttu-id="512b8-175">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="512b8-175">Get-AzureRmDataFactoryRun</span></span>](./Get-AzureRmDataFactoryRun.md)

[<span data-ttu-id="512b8-176">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="512b8-176">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)


