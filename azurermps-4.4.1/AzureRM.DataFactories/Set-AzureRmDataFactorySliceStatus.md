---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
ms.openlocfilehash: 30e6a3ec6d3cd9cba978ed51d6545b3f68375779
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426904"
---
# <span data-ttu-id="52877-101">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="52877-101">Set-AzureRmDataFactorySliceStatus</span></span>

## <span data-ttu-id="52877-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52877-102">SYNOPSIS</span></span>
<span data-ttu-id="52877-103">Define o status das fatias de um conjunto de dados na fábrica de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="52877-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52877-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52877-104">SYNTAX</span></span>

### <span data-ttu-id="52877-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="52877-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52877-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="52877-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52877-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52877-107">DESCRIPTION</span></span>
<span data-ttu-id="52877-108">O cmdlet **set-AzureRmDataFactorySliceStatus** define o status das fatias de um conjunto de dados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="52877-108">The **Set-AzureRmDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="52877-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52877-109">EXAMPLES</span></span>

### <span data-ttu-id="52877-110">Exemplo 1: definir o status de todas as fatias</span><span class="sxs-lookup"><span data-stu-id="52877-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzureRmDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="52877-111">Esse comando define o status de todas as fatias do conjunto de dados chamado DAWikiAggregatedData para aguardar no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="52877-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="52877-112">O parâmetro *UpdateType* tem um valor de UpstreamInPipeline e, portanto, o comando define o status de cada fatia para o conjunto de dados e todos os conjuntos de dados dependentes.</span><span class="sxs-lookup"><span data-stu-id="52877-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="52877-113">Conjuntos de dados dependentes são usados como conjuntos de dados de entrada para atividades no pipeline.</span><span class="sxs-lookup"><span data-stu-id="52877-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="52877-114">Esse comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="52877-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="52877-115">OS</span><span class="sxs-lookup"><span data-stu-id="52877-115">PARAMETERS</span></span>

### <span data-ttu-id="52877-116">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="52877-116">-DataFactory</span></span>
<span data-ttu-id="52877-117">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="52877-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="52877-118">Esse cmdlet modifica o status de fatias que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="52877-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="52877-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="52877-119">-DataFactoryName</span></span>
<span data-ttu-id="52877-120">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="52877-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="52877-121">Esse cmdlet modifica o status de fatias que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="52877-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="52877-122">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="52877-122">-DatasetName</span></span>
<span data-ttu-id="52877-123">Especifica o nome do DataSet para o qual esse cmdlet modifica fatias.</span><span class="sxs-lookup"><span data-stu-id="52877-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

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

### <span data-ttu-id="52877-124">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="52877-124">-EndDateTime</span></span>
<span data-ttu-id="52877-125">Especifica o fim de um período de tempo como um objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="52877-125">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="52877-126">Esta hora é o final de uma fatia de dados.</span><span class="sxs-lookup"><span data-stu-id="52877-126">This time is the end of a data slice.</span></span>
<span data-ttu-id="52877-127">Para obter mais informações sobre objetos **DateTime** , digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="52877-127">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="52877-128">*EndDateTime* deve ser especificado no formato ISO8601 como nos exemplos a seguir:</span><span class="sxs-lookup"><span data-stu-id="52877-128">*EndDateTime* must be specified in the ISO8601 format as in the following examples:</span></span> 

<span data-ttu-id="52877-129">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (hora padrão do Pacífico)</span><span class="sxs-lookup"><span data-stu-id="52877-129">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="52877-130">O designador de fuso horário padrão é UTC.</span><span class="sxs-lookup"><span data-stu-id="52877-130">The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="52877-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52877-131">-ResourceGroupName</span></span>
<span data-ttu-id="52877-132">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="52877-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="52877-133">Esse cmdlet modifica o status de fatias que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="52877-133">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="52877-134">-StartDatetime</span><span class="sxs-lookup"><span data-stu-id="52877-134">-StartDateTime</span></span>
<span data-ttu-id="52877-135">Especifica o início de um período de tempo como um objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="52877-135">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="52877-136">Esta hora é o início de uma fatia de dados.</span><span class="sxs-lookup"><span data-stu-id="52877-136">This time is the beginning of a data slice.</span></span>

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

### <span data-ttu-id="52877-137">-Status</span><span class="sxs-lookup"><span data-stu-id="52877-137">-Status</span></span>
<span data-ttu-id="52877-138">Especifica um status a ser atribuído à fatia de dados.</span><span class="sxs-lookup"><span data-stu-id="52877-138">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="52877-139">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="52877-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="52877-140">Faxes.</span><span class="sxs-lookup"><span data-stu-id="52877-140">Waiting.</span></span>
<span data-ttu-id="52877-141">A fatia de dados está aguardando a validação em políticas de validação antes de ser processada.</span><span class="sxs-lookup"><span data-stu-id="52877-141">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="52877-142">Está.</span><span class="sxs-lookup"><span data-stu-id="52877-142">Ready.</span></span>
<span data-ttu-id="52877-143">O processamento de dados foi concluído e a fatia de dados está pronta.</span><span class="sxs-lookup"><span data-stu-id="52877-143">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="52877-144">InProgress.</span><span class="sxs-lookup"><span data-stu-id="52877-144">InProgress.</span></span>
<span data-ttu-id="52877-145">O processamento de dados está em andamento.</span><span class="sxs-lookup"><span data-stu-id="52877-145">Data processing is in-progress.</span></span> 
- <span data-ttu-id="52877-146">Conseguiu.</span><span class="sxs-lookup"><span data-stu-id="52877-146">Failed.</span></span>
<span data-ttu-id="52877-147">Falha no processamento de dados.</span><span class="sxs-lookup"><span data-stu-id="52877-147">Data processing failed.</span></span>
- <span data-ttu-id="52877-148">Ignorada.</span><span class="sxs-lookup"><span data-stu-id="52877-148">Skipped.</span></span>
<span data-ttu-id="52877-149">O processamento da fatia de dados foi ignorado.</span><span class="sxs-lookup"><span data-stu-id="52877-149">Skipped processing the data slice.</span></span>

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

### <span data-ttu-id="52877-150">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="52877-150">-UpdateType</span></span>
<span data-ttu-id="52877-151">Especifica o tipo de atualização para a fatia.</span><span class="sxs-lookup"><span data-stu-id="52877-151">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="52877-152">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="52877-152">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="52877-153">Cada.</span><span class="sxs-lookup"><span data-stu-id="52877-153">Individual.</span></span>
<span data-ttu-id="52877-154">Define o status de cada fatia para o conjunto de valores no intervalo de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="52877-154">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="52877-155">UpstreamInPipeline.</span><span class="sxs-lookup"><span data-stu-id="52877-155">UpstreamInPipeline.</span></span>
<span data-ttu-id="52877-156">Define o status de cada fatia para o conjunto de dados e todos os conjuntos de dados dependentes, que são usados como conjuntos de dados de entrada para atividades no pipeline.</span><span class="sxs-lookup"><span data-stu-id="52877-156">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

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

### <span data-ttu-id="52877-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52877-157">-DefaultProfile</span></span>
<span data-ttu-id="52877-158">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52877-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52877-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52877-159">CommonParameters</span></span>
<span data-ttu-id="52877-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52877-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52877-161">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52877-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52877-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52877-162">INPUTS</span></span>

## <span data-ttu-id="52877-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52877-163">OUTPUTS</span></span>

### <span data-ttu-id="52877-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52877-164">System.Boolean</span></span>

## <span data-ttu-id="52877-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52877-165">NOTES</span></span>
* <span data-ttu-id="52877-166">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="52877-166">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="52877-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52877-167">RELATED LINKS</span></span>

[<span data-ttu-id="52877-168">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="52877-168">Get-AzureRmDataFactorySlice</span></span>](./Get-AzureRmDataFactorySlice.md)


