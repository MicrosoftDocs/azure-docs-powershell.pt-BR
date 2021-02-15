---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: a71ccc37fe1c6b6811b955c5d84353dfecd66c2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118823"
---
# <span data-ttu-id="fb500-101">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="fb500-101">Get-AzDataFactorySlice</span></span>

## <span data-ttu-id="fb500-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb500-102">SYNOPSIS</span></span>
<span data-ttu-id="fb500-103">Obtém fatias de dados para um conjuntos de dados no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="fb500-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="fb500-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb500-104">SYNTAX</span></span>

### <span data-ttu-id="fb500-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="fb500-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb500-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fb500-106">ByFactoryObject</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb500-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb500-107">DESCRIPTION</span></span>
<span data-ttu-id="fb500-108">O cmdlet **Get-AzDataFactorySlice** obtém fatias de dados para um conjuntos de dados no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="fb500-108">The **Get-AzDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="fb500-109">Especifique uma hora de início e uma hora de término para definir um intervalo de fatias de dados a exibir.</span><span class="sxs-lookup"><span data-stu-id="fb500-109">Specify a start time and an end time to define a range of data slices to view.</span></span>
<span data-ttu-id="fb500-110">O status de uma fatia de dados é um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="fb500-110">The status of a data slice is one of the following values:</span></span> 
- <span data-ttu-id="fb500-111">PendenteExecução.</span><span class="sxs-lookup"><span data-stu-id="fb500-111">PendingExecution.</span></span>
<span data-ttu-id="fb500-112">O processamento de dados não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="fb500-112">Data processing has not started.</span></span> 
- <span data-ttu-id="fb500-113">Inprogress.</span><span class="sxs-lookup"><span data-stu-id="fb500-113">InProgress.</span></span>
<span data-ttu-id="fb500-114">O processamento de dados está em andamento.</span><span class="sxs-lookup"><span data-stu-id="fb500-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="fb500-115">Pronto.</span><span class="sxs-lookup"><span data-stu-id="fb500-115">Ready.</span></span>
<span data-ttu-id="fb500-116">O processamento de dados está concluído.</span><span class="sxs-lookup"><span data-stu-id="fb500-116">Data processing is completed.</span></span>
<span data-ttu-id="fb500-117">A fatia de dados está pronta para que as fatias dependentes a consumam.</span><span class="sxs-lookup"><span data-stu-id="fb500-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="fb500-118">Falhou.</span><span class="sxs-lookup"><span data-stu-id="fb500-118">Failed.</span></span>
<span data-ttu-id="fb500-119">A correção que produz a fatia falhou.</span><span class="sxs-lookup"><span data-stu-id="fb500-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="fb500-120">Ignorar.</span><span class="sxs-lookup"><span data-stu-id="fb500-120">Skip.</span></span>
<span data-ttu-id="fb500-121">A Data Factory ignora o processamento da fatia.</span><span class="sxs-lookup"><span data-stu-id="fb500-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="fb500-122">Repetir.</span><span class="sxs-lookup"><span data-stu-id="fb500-122">Retry.</span></span>
<span data-ttu-id="fb500-123">A Data Factory recupera a executar que produz a fatia.</span><span class="sxs-lookup"><span data-stu-id="fb500-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="fb500-124">Tempo de tempo. O processamento de dados deu um tempo.</span><span class="sxs-lookup"><span data-stu-id="fb500-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="fb500-125">PendenteValidation.</span><span class="sxs-lookup"><span data-stu-id="fb500-125">PendingValidation.</span></span>
<span data-ttu-id="fb500-126">A fatia de dados está aguardando validação antes de ser processada.</span><span class="sxs-lookup"><span data-stu-id="fb500-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="fb500-127">Tentar validação novamente.</span><span class="sxs-lookup"><span data-stu-id="fb500-127">Retry Validation.</span></span>
<span data-ttu-id="fb500-128">A Data Factory recupera a validação da fatia.</span><span class="sxs-lookup"><span data-stu-id="fb500-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="fb500-129">Falha na Validação.</span><span class="sxs-lookup"><span data-stu-id="fb500-129">Failed Validation.</span></span>
<span data-ttu-id="fb500-130">Falha na validação da fatia.</span><span class="sxs-lookup"><span data-stu-id="fb500-130">Validation of the slice failed.</span></span>
<span data-ttu-id="fb500-131">Para cada uma das fatias, você pode ver mais informações sobre a operação que produz a fatia usando o cmdlet Get-AzDataFactoryRun dados.</span><span class="sxs-lookup"><span data-stu-id="fb500-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="fb500-132">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fb500-132">EXAMPLES</span></span>

### <span data-ttu-id="fb500-133">Exemplo 1: Obter fatias de dados para um conjuntos de dados</span><span class="sxs-lookup"><span data-stu-id="fb500-133">Example 1: Get data slices for a dataset</span></span>
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

<span data-ttu-id="fb500-134">Esse comando obtém todas as fatias de dados do grupo de dados chamado WikiAggregatedData na fábrica de dados chamada WikiADF.</span><span class="sxs-lookup"><span data-stu-id="fb500-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="fb500-135">O comando obtém fatias produzidas após o tempo especificado pelo parâmetro StartDateTime.</span><span class="sxs-lookup"><span data-stu-id="fb500-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="fb500-136">O código de exemplo a seguir define a disponibilidade para esse conjunto de dados a cada hora no arquivo JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="fb500-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="fb500-137">disponibilidade: { ponto: "Hora", pontoMultiplier: 1 } Alguns dos resultados estão Prontos e outros sãoPendingExecution.</span><span class="sxs-lookup"><span data-stu-id="fb500-137">availability: { period: "Hour", periodMultiplier: 1 } Some of the results are Ready and others are PendingExecution.</span></span>
<span data-ttu-id="fb500-138">As fatias prontas já foram executados.</span><span class="sxs-lookup"><span data-stu-id="fb500-138">Ready slices have already run.</span></span>
<span data-ttu-id="fb500-139">As fatias pendentes estão aguardando para ser executados no final de cada hora no intervalo especificado pelo cmdlet Set-AzDataFactoryPipelineActivePeriod dados.</span><span class="sxs-lookup"><span data-stu-id="fb500-139">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="fb500-140">Neste exemplo, os períodos de início e de término do pipeline e a fatia têm um valor de um dia (24 horas).</span><span class="sxs-lookup"><span data-stu-id="fb500-140">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

### <span data-ttu-id="fb500-141">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fb500-141">Example 2</span></span>

<span data-ttu-id="fb500-142">Obtém fatias de dados para um conjuntos de dados no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="fb500-142">Gets data slices for a dataset in Azure Data Factory.</span></span> <span data-ttu-id="fb500-143">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="fb500-143">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## <span data-ttu-id="fb500-144">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb500-144">PARAMETERS</span></span>

### <span data-ttu-id="fb500-145">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="fb500-145">-DataFactory</span></span>
<span data-ttu-id="fb500-146">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="fb500-146">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="fb500-147">Este cmdlet obtém fatias que pertencem à fábrica de dados especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fb500-147">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fb500-148">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fb500-148">-DataFactoryName</span></span>
<span data-ttu-id="fb500-149">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="fb500-149">Specifies the name of a data factory.</span></span>
<span data-ttu-id="fb500-150">Este cmdlet obtém fatias que pertencem à fábrica de dados especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fb500-150">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fb500-151">-NomedoConjunto de Dados</span><span class="sxs-lookup"><span data-stu-id="fb500-151">-DatasetName</span></span>
<span data-ttu-id="fb500-152">Especifica o nome do conjuntos de dados para o qual este cmdlet obtém fatias.</span><span class="sxs-lookup"><span data-stu-id="fb500-152">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

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

### <span data-ttu-id="fb500-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb500-153">-DefaultProfile</span></span>
<span data-ttu-id="fb500-154">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="fb500-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb500-155">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="fb500-155">-EndDateTime</span></span>
<span data-ttu-id="fb500-156">Especifica o fim de um período de tempo como um **objeto DateTime.**</span><span class="sxs-lookup"><span data-stu-id="fb500-156">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="fb500-157">Esse cmdlet obtém as fatias produzidas antes do tempo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fb500-157">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="fb500-158">Para obter mais informações sobre **objetos DateTime,** `Get-Help Get-Date` digite.</span><span class="sxs-lookup"><span data-stu-id="fb500-158">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="fb500-159">*EndDateTime* deve ser especificado no formato ISO8601, como nos exemplos a seguir: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Hora Padrão do Pacífico) O designador de fuso horário padrão é UTC.</span><span class="sxs-lookup"><span data-stu-id="fb500-159">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="fb500-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb500-160">-ResourceGroupName</span></span>
<span data-ttu-id="fb500-161">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="fb500-161">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fb500-162">Este cmdlet obtém fatias que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fb500-162">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fb500-163">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="fb500-163">-StartDateTime</span></span>
<span data-ttu-id="fb500-164">Especifica o início de um período de tempo como um **objeto DateTime.**</span><span class="sxs-lookup"><span data-stu-id="fb500-164">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="fb500-165">Esse cmdlet obtém fatias produzidas após o tempo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fb500-165">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="fb500-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb500-166">CommonParameters</span></span>
<span data-ttu-id="fb500-167">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb500-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb500-168">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb500-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb500-169">Entradas</span><span class="sxs-lookup"><span data-stu-id="fb500-169">INPUTS</span></span>

### <span data-ttu-id="fb500-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fb500-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="fb500-171">System.String</span><span class="sxs-lookup"><span data-stu-id="fb500-171">System.String</span></span>

## <span data-ttu-id="fb500-172">Saídas</span><span class="sxs-lookup"><span data-stu-id="fb500-172">OUTPUTS</span></span>

### <span data-ttu-id="fb500-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span><span class="sxs-lookup"><span data-stu-id="fb500-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span></span>

## <span data-ttu-id="fb500-174">Notas</span><span class="sxs-lookup"><span data-stu-id="fb500-174">NOTES</span></span>
* <span data-ttu-id="fb500-175">Palavras-chave: azure, azurerm, arm, resource, management, manager, data,</span><span class="sxs-lookup"><span data-stu-id="fb500-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fb500-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb500-176">RELATED LINKS</span></span>

[<span data-ttu-id="fb500-177">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="fb500-177">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)

[<span data-ttu-id="fb500-178">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="fb500-178">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="fb500-179">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="fb500-179">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


