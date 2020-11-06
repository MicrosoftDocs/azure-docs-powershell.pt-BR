---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
ms.openlocfilehash: a7418dd1e0570d4e92310371e658dd130b36bc44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596978"
---
# <span data-ttu-id="ef96a-101">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="ef96a-101">Set-AzDataFactorySliceStatus</span></span>

## <span data-ttu-id="ef96a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ef96a-102">SYNOPSIS</span></span>
<span data-ttu-id="ef96a-103">Define o status das fatias de um conjunto de dados na fábrica de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="ef96a-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="ef96a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef96a-104">SYNTAX</span></span>

### <span data-ttu-id="ef96a-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ef96a-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef96a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ef96a-106">ByFactoryObject</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef96a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ef96a-107">DESCRIPTION</span></span>
<span data-ttu-id="ef96a-108">O cmdlet **set-AzDataFactorySliceStatus** define o status das fatias de um conjunto de dados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="ef96a-108">The **Set-AzDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="ef96a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef96a-109">EXAMPLES</span></span>

### <span data-ttu-id="ef96a-110">Exemplo 1: definir o status de todas as fatias</span><span class="sxs-lookup"><span data-stu-id="ef96a-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="ef96a-111">Esse comando define o status de todas as fatias do conjunto de dados chamado DAWikiAggregatedData para aguardar no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ef96a-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="ef96a-112">O parâmetro *UpdateType* tem um valor de UpstreamInPipeline e, portanto, o comando define o status de cada fatia para o conjunto de dados e todos os conjuntos de dados dependentes.</span><span class="sxs-lookup"><span data-stu-id="ef96a-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="ef96a-113">Conjuntos de dados dependentes são usados como conjuntos de dados de entrada para atividades no pipeline.</span><span class="sxs-lookup"><span data-stu-id="ef96a-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="ef96a-114">Esse comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="ef96a-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="ef96a-115">OS</span><span class="sxs-lookup"><span data-stu-id="ef96a-115">PARAMETERS</span></span>

### <span data-ttu-id="ef96a-116">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="ef96a-116">-DataFactory</span></span>
<span data-ttu-id="ef96a-117">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="ef96a-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ef96a-118">Esse cmdlet modifica o status de fatias que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ef96a-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ef96a-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="ef96a-119">-DataFactoryName</span></span>
<span data-ttu-id="ef96a-120">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="ef96a-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ef96a-121">Esse cmdlet modifica o status de fatias que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ef96a-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ef96a-122">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="ef96a-122">-DatasetName</span></span>
<span data-ttu-id="ef96a-123">Especifica o nome do DataSet para o qual esse cmdlet modifica fatias.</span><span class="sxs-lookup"><span data-stu-id="ef96a-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

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

### <span data-ttu-id="ef96a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef96a-124">-DefaultProfile</span></span>
<span data-ttu-id="ef96a-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ef96a-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef96a-126">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="ef96a-126">-EndDateTime</span></span>
<span data-ttu-id="ef96a-127">Especifica o fim de um período de tempo como um objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="ef96a-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="ef96a-128">Esta hora é o final de uma fatia de dados.</span><span class="sxs-lookup"><span data-stu-id="ef96a-128">This time is the end of a data slice.</span></span>
<span data-ttu-id="ef96a-129">Para obter mais informações sobre objetos **DateTime** , digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="ef96a-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="ef96a-130">*EndDateTime* deve ser especificado no formato ISO8601 como nos exemplos a seguir: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (hora padrão do Pacífico) o designador de fuso horário padrão é UTC.</span><span class="sxs-lookup"><span data-stu-id="ef96a-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="ef96a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef96a-131">-ResourceGroupName</span></span>
<span data-ttu-id="ef96a-132">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="ef96a-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ef96a-133">Esse cmdlet modifica o status de fatias que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ef96a-133">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ef96a-134">-StartDatetime</span><span class="sxs-lookup"><span data-stu-id="ef96a-134">-StartDateTime</span></span>
<span data-ttu-id="ef96a-135">Especifica o início de um período de tempo como um objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="ef96a-135">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="ef96a-136">Esta hora é o início de uma fatia de dados.</span><span class="sxs-lookup"><span data-stu-id="ef96a-136">This time is the beginning of a data slice.</span></span>

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

### <span data-ttu-id="ef96a-137">-Status</span><span class="sxs-lookup"><span data-stu-id="ef96a-137">-Status</span></span>
<span data-ttu-id="ef96a-138">Especifica um status a ser atribuído à fatia de dados.</span><span class="sxs-lookup"><span data-stu-id="ef96a-138">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="ef96a-139">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ef96a-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ef96a-140">Faxes.</span><span class="sxs-lookup"><span data-stu-id="ef96a-140">Waiting.</span></span>
<span data-ttu-id="ef96a-141">A fatia de dados está aguardando a validação em políticas de validação antes de ser processada.</span><span class="sxs-lookup"><span data-stu-id="ef96a-141">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="ef96a-142">Está.</span><span class="sxs-lookup"><span data-stu-id="ef96a-142">Ready.</span></span>
<span data-ttu-id="ef96a-143">O processamento de dados foi concluído e a fatia de dados está pronta.</span><span class="sxs-lookup"><span data-stu-id="ef96a-143">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="ef96a-144">InProgress.</span><span class="sxs-lookup"><span data-stu-id="ef96a-144">InProgress.</span></span>
<span data-ttu-id="ef96a-145">O processamento de dados está em andamento.</span><span class="sxs-lookup"><span data-stu-id="ef96a-145">Data processing is in-progress.</span></span> 
- <span data-ttu-id="ef96a-146">Conseguiu.</span><span class="sxs-lookup"><span data-stu-id="ef96a-146">Failed.</span></span>
<span data-ttu-id="ef96a-147">Falha no processamento de dados.</span><span class="sxs-lookup"><span data-stu-id="ef96a-147">Data processing failed.</span></span>
- <span data-ttu-id="ef96a-148">Ignorada.</span><span class="sxs-lookup"><span data-stu-id="ef96a-148">Skipped.</span></span>
<span data-ttu-id="ef96a-149">O processamento da fatia de dados foi ignorado.</span><span class="sxs-lookup"><span data-stu-id="ef96a-149">Skipped processing the data slice.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef96a-150">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="ef96a-150">-UpdateType</span></span>
<span data-ttu-id="ef96a-151">Especifica o tipo de atualização para a fatia.</span><span class="sxs-lookup"><span data-stu-id="ef96a-151">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="ef96a-152">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ef96a-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ef96a-153">Cada.</span><span class="sxs-lookup"><span data-stu-id="ef96a-153">Individual.</span></span>
<span data-ttu-id="ef96a-154">Define o status de cada fatia para o conjunto de valores no intervalo de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="ef96a-154">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="ef96a-155">UpstreamInPipeline.</span><span class="sxs-lookup"><span data-stu-id="ef96a-155">UpstreamInPipeline.</span></span>
<span data-ttu-id="ef96a-156">Define o status de cada fatia para o conjunto de dados e todos os conjuntos de dados dependentes, que são usados como conjuntos de dados de entrada para atividades no pipeline.</span><span class="sxs-lookup"><span data-stu-id="ef96a-156">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef96a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef96a-157">CommonParameters</span></span>
<span data-ttu-id="ef96a-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef96a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef96a-159">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef96a-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef96a-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ef96a-160">INPUTS</span></span>

### <span data-ttu-id="ef96a-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ef96a-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="ef96a-162">System. String</span><span class="sxs-lookup"><span data-stu-id="ef96a-162">System.String</span></span>

## <span data-ttu-id="ef96a-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ef96a-163">OUTPUTS</span></span>

### <span data-ttu-id="ef96a-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ef96a-164">System.Boolean</span></span>

## <span data-ttu-id="ef96a-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ef96a-165">NOTES</span></span>
* <span data-ttu-id="ef96a-166">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="ef96a-166">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ef96a-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef96a-167">RELATED LINKS</span></span>

[<span data-ttu-id="ef96a-168">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="ef96a-168">Get-AzDataFactorySlice</span></span>](./Get-AzDataFactorySlice.md)


