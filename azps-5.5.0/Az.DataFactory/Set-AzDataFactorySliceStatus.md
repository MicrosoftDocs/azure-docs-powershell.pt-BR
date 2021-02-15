---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
ms.openlocfilehash: 8b2c55a069463120b861f1ea928ac0163a4c37df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118810"
---
# <span data-ttu-id="3e622-101">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="3e622-101">Set-AzDataFactorySliceStatus</span></span>

## <span data-ttu-id="3e622-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e622-102">SYNOPSIS</span></span>
<span data-ttu-id="3e622-103">Define o status das fatias para um conjunto de dados no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="3e622-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="3e622-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e622-104">SYNTAX</span></span>

### <span data-ttu-id="3e622-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="3e622-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e622-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3e622-106">ByFactoryObject</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e622-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e622-107">DESCRIPTION</span></span>
<span data-ttu-id="3e622-108">O cmdlet **Set-AzDataFactorySliceStatus** define o status das fatias de um conjunto de dados no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="3e622-108">The **Set-AzDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="3e622-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3e622-109">EXAMPLES</span></span>

### <span data-ttu-id="3e622-110">Exemplo 1: Definir o status de todas as fatias</span><span class="sxs-lookup"><span data-stu-id="3e622-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="3e622-111">Esse comando define o status de todas as fatias para o conjunto de dados chamado DAWikiAggregatedData como Aguardando na fábrica de dados chamada WikiADF.</span><span class="sxs-lookup"><span data-stu-id="3e622-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="3e622-112">O *parâmetro UpdateType* tem um valor de UpstreamInStreamLine e, portanto, o comando define o status de cada fatia para o conjunto de dados e todos os conjuntos de dados dependentes.</span><span class="sxs-lookup"><span data-stu-id="3e622-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="3e622-113">Os conjuntos de dados dependentes são usados como conjuntos de dados de entrada para atividades no pipeline.</span><span class="sxs-lookup"><span data-stu-id="3e622-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="3e622-114">Esse comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="3e622-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="3e622-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e622-115">PARAMETERS</span></span>

### <span data-ttu-id="3e622-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3e622-116">-DataFactory</span></span>
<span data-ttu-id="3e622-117">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="3e622-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="3e622-118">Esse cmdlet modifica o status das fatias que pertencem à fábrica de dados especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3e622-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3e622-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3e622-119">-DataFactoryName</span></span>
<span data-ttu-id="3e622-120">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="3e622-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3e622-121">Esse cmdlet modifica o status das fatias que pertencem à fábrica de dados especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3e622-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3e622-122">-NomedoConjunto de Dados</span><span class="sxs-lookup"><span data-stu-id="3e622-122">-DatasetName</span></span>
<span data-ttu-id="3e622-123">Especifica o nome do conjuntos de dados para o qual este cmdlet modifica as fatias.</span><span class="sxs-lookup"><span data-stu-id="3e622-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

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

### <span data-ttu-id="3e622-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e622-124">-DefaultProfile</span></span>
<span data-ttu-id="3e622-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3e622-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e622-126">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="3e622-126">-EndDateTime</span></span>
<span data-ttu-id="3e622-127">Especifica o fim de um período de tempo como um **objeto DateTime.**</span><span class="sxs-lookup"><span data-stu-id="3e622-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="3e622-128">Desta vez é o fim de uma fatia de dados.</span><span class="sxs-lookup"><span data-stu-id="3e622-128">This time is the end of a data slice.</span></span>
<span data-ttu-id="3e622-129">Para obter mais informações sobre **objetos DateTime,** `Get-Help Get-Date` digite.</span><span class="sxs-lookup"><span data-stu-id="3e622-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="3e622-130">*EndDateTime* deve ser especificado no formato ISO8601, como nos exemplos a seguir: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Hora Padrão do Pacífico) O designador de fuso horário padrão é UTC.</span><span class="sxs-lookup"><span data-stu-id="3e622-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="3e622-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e622-131">-ResourceGroupName</span></span>
<span data-ttu-id="3e622-132">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e622-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3e622-133">Esse cmdlet modifica o status das fatias que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3e622-133">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3e622-134">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="3e622-134">-StartDateTime</span></span>
<span data-ttu-id="3e622-135">Especifica o início de um período de tempo como um **objeto DateTime.**</span><span class="sxs-lookup"><span data-stu-id="3e622-135">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="3e622-136">Este é o início de uma fatia de dados.</span><span class="sxs-lookup"><span data-stu-id="3e622-136">This time is the beginning of a data slice.</span></span>

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

### <span data-ttu-id="3e622-137">-Status</span><span class="sxs-lookup"><span data-stu-id="3e622-137">-Status</span></span>
<span data-ttu-id="3e622-138">Especifica um status a ser atribuído à fatia de dados.</span><span class="sxs-lookup"><span data-stu-id="3e622-138">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="3e622-139">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3e622-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3e622-140">Esperando.</span><span class="sxs-lookup"><span data-stu-id="3e622-140">Waiting.</span></span>
<span data-ttu-id="3e622-141">A fatia de dados está aguardando validação em relação às políticas de validação antes de ser processada.</span><span class="sxs-lookup"><span data-stu-id="3e622-141">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="3e622-142">Pronto.</span><span class="sxs-lookup"><span data-stu-id="3e622-142">Ready.</span></span>
<span data-ttu-id="3e622-143">O processamento de dados foi concluído e a fatia de dados está pronta.</span><span class="sxs-lookup"><span data-stu-id="3e622-143">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="3e622-144">Inprogress.</span><span class="sxs-lookup"><span data-stu-id="3e622-144">InProgress.</span></span>
<span data-ttu-id="3e622-145">O processamento de dados está em andamento.</span><span class="sxs-lookup"><span data-stu-id="3e622-145">Data processing is in-progress.</span></span> 
- <span data-ttu-id="3e622-146">Falhou.</span><span class="sxs-lookup"><span data-stu-id="3e622-146">Failed.</span></span>
<span data-ttu-id="3e622-147">Falha no processamento de dados.</span><span class="sxs-lookup"><span data-stu-id="3e622-147">Data processing failed.</span></span>
- <span data-ttu-id="3e622-148">Ignorada.</span><span class="sxs-lookup"><span data-stu-id="3e622-148">Skipped.</span></span>
<span data-ttu-id="3e622-149">Ignorada a processamento da fatia de dados.</span><span class="sxs-lookup"><span data-stu-id="3e622-149">Skipped processing the data slice.</span></span>

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

### <span data-ttu-id="3e622-150">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="3e622-150">-UpdateType</span></span>
<span data-ttu-id="3e622-151">Especifica o tipo de atualização da fatia.</span><span class="sxs-lookup"><span data-stu-id="3e622-151">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="3e622-152">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3e622-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3e622-153">Individuais.</span><span class="sxs-lookup"><span data-stu-id="3e622-153">Individual.</span></span>
<span data-ttu-id="3e622-154">Define o status de cada fatia para o conjunto de dados no intervalo de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="3e622-154">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="3e622-155">UpstreamInStreamLine.</span><span class="sxs-lookup"><span data-stu-id="3e622-155">UpstreamInPipeline.</span></span>
<span data-ttu-id="3e622-156">Define o status de cada fatia para o conjunto de dados e todos os conjuntos de dados dependentes, que são usados como conjuntos de dados de entrada para atividades no pipeline.</span><span class="sxs-lookup"><span data-stu-id="3e622-156">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

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

### <span data-ttu-id="3e622-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e622-157">CommonParameters</span></span>
<span data-ttu-id="3e622-158">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e622-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e622-159">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e622-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e622-160">Entradas</span><span class="sxs-lookup"><span data-stu-id="3e622-160">INPUTS</span></span>

### <span data-ttu-id="3e622-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3e622-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="3e622-162">System.String</span><span class="sxs-lookup"><span data-stu-id="3e622-162">System.String</span></span>

## <span data-ttu-id="3e622-163">Saídas</span><span class="sxs-lookup"><span data-stu-id="3e622-163">OUTPUTS</span></span>

### <span data-ttu-id="3e622-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3e622-164">System.Boolean</span></span>

## <span data-ttu-id="3e622-165">Notas</span><span class="sxs-lookup"><span data-stu-id="3e622-165">NOTES</span></span>
* <span data-ttu-id="3e622-166">Palavras-chave: azure, azurerm, arm, resource, management, manager, data,</span><span class="sxs-lookup"><span data-stu-id="3e622-166">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3e622-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e622-167">RELATED LINKS</span></span>

[<span data-ttu-id="3e622-168">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="3e622-168">Get-AzDataFactorySlice</span></span>](./Get-AzDataFactorySlice.md)


