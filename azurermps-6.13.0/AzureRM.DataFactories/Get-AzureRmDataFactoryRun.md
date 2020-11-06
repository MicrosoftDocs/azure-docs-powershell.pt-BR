---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryRun.md
ms.openlocfilehash: 77ca77322cec186878b327bcafa9fce626a99c02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430340"
---
# <span data-ttu-id="c6aba-101">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="c6aba-101">Get-AzureRmDataFactoryRun</span></span>

## <span data-ttu-id="c6aba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6aba-102">SYNOPSIS</span></span>
<span data-ttu-id="c6aba-103">É executado para uma fatia de dados de um conjunto de dados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="c6aba-103">Gets runs for a data slice of a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6aba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6aba-104">SYNTAX</span></span>

### <span data-ttu-id="c6aba-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c6aba-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6aba-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c6aba-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6aba-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c6aba-107">DESCRIPTION</span></span>
<span data-ttu-id="c6aba-108">O cmdlet **Get-AzureRmDataFactoryRun** Obtém as execuções para uma fatia de dados de um conjunto de dados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="c6aba-108">The **Get-AzureRmDataFactoryRun** cmdlet gets the runs for a data slice of a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="c6aba-109">Um conjunto de dados em uma fábrica de dados é composto de fatias no eixo de tempo.</span><span class="sxs-lookup"><span data-stu-id="c6aba-109">A dataset in a data factory is composed of slices over the time axis.</span></span>
<span data-ttu-id="c6aba-110">A largura de uma fatia é determinada pelo cronograma, a cada hora ou diariamente.</span><span class="sxs-lookup"><span data-stu-id="c6aba-110">The width of a slice is determined by the schedule, either hourly or daily.</span></span>
<span data-ttu-id="c6aba-111">Uma execução é uma unidade de processamento para uma fatia.</span><span class="sxs-lookup"><span data-stu-id="c6aba-111">A run is a unit of processing for a slice.</span></span>
<span data-ttu-id="c6aba-112">Pode haver uma ou mais execuções para uma fatia em caso de novas tentativas ou, caso você retorne a sua fatia devido a falhas.</span><span class="sxs-lookup"><span data-stu-id="c6aba-112">There could be one or more runs for a slice in case of retries or in case you rerun your slice due to failures.</span></span>
<span data-ttu-id="c6aba-113">Uma fatia é identificada pela hora de início.</span><span class="sxs-lookup"><span data-stu-id="c6aba-113">A slice is identified by its start time.</span></span>
<span data-ttu-id="c6aba-114">Para obter a hora de início de uma fatia, use o cmdlet Get-AzureRmDataFactorySlice.</span><span class="sxs-lookup"><span data-stu-id="c6aba-114">To obtain the start time of a slice, use the Get-AzureRmDataFactorySlice cmdlet.</span></span>
<span data-ttu-id="c6aba-115">Por exemplo, para obter uma execução para a seguinte fatia, use a hora de início 2015-04-02T20:00:00.</span><span class="sxs-lookup"><span data-stu-id="c6aba-115">For example, to get a run for the following slice, use the start time 2015-04-02T20:00:00.</span></span>
<span data-ttu-id="c6aba-116">ResourceGroupName: AAD datafactoryname: SPDataFactory0924 DataSetName: MarketingCampaignEffectivenessBlobDataset Start: 5/2/2014 8:00:00 PM end: 5/3/2014 8:00:00 PM RetryCount: 0 status: Ready LatencyStatus:</span><span class="sxs-lookup"><span data-stu-id="c6aba-116">ResourceGroupName  : ADF DataFactoryName : SPDataFactory0924 DatasetName : MarketingCampaignEffectivenessBlobDataset Start : 5/2/2014 8:00:00 PM End : 5/3/2014 8:00:00 PM RetryCount : 0 Status : Ready LatencyStatus :</span></span>

## <span data-ttu-id="c6aba-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6aba-117">EXAMPLES</span></span>

### <span data-ttu-id="c6aba-118">Exemplo 1: obter um conjunto de um conjunto de um</span><span class="sxs-lookup"><span data-stu-id="c6aba-118">Example 1: Get a dataset</span></span>
```
PS C:\>Get-AzureRmDataFactoryRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z
Id                  : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ResourceGroupName   : ADF
DataFactoryName     : WikiADF
DatasetName           : DAWikiAggregatedData
PipelineName        : 249ea141-ca00-8597-fad9-a148e5e7bdba
ActivityId          : fcefe2bd-39b1-2d7a-7b35-bcc2b0432300
ResumptionToken     : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ContinuationToken   : 
ProcessingStartTime : 5/21/2014 5:02:41 PM
ProcessingEndTime   : 5/21/2014 5:04:12 PM
PercentComplete     : 100
DataSliceStart      : 5/21/2014 4:00:00 PM
DataSliceEnd        : 5/21/2014 5:00:00 PM
Status              : Succeeded
Timestamp           : 5/21/2014 5:02:41 PM
RetryAttempt        : 0
Properties          : {[errors, ]} 
ErrorMessage        :
```

<span data-ttu-id="c6aba-119">Esse comando obtém todas as execuções para fatias do conjunto de dados chamado DAWikiAggregatedData no data Factory chamado WikiADF que começam de 4 PM GMT em 05/21/2014.</span><span class="sxs-lookup"><span data-stu-id="c6aba-119">This command gets all runs for slices of the dataset named DAWikiAggregatedData in the data factory named WikiADF that start from 4 PM GMT on 05/21/2014.</span></span>

## <span data-ttu-id="c6aba-120">OS</span><span class="sxs-lookup"><span data-stu-id="c6aba-120">PARAMETERS</span></span>

### <span data-ttu-id="c6aba-121">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="c6aba-121">-DataFactory</span></span>
<span data-ttu-id="c6aba-122">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="c6aba-122">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="c6aba-123">Esse cmdlet é executado para as fatias que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c6aba-123">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6aba-124">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="c6aba-124">-DataFactoryName</span></span>
<span data-ttu-id="c6aba-125">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="c6aba-125">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c6aba-126">Esse cmdlet é executado para as fatias que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c6aba-126">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6aba-127">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="c6aba-127">-DatasetName</span></span>
<span data-ttu-id="c6aba-128">Especifica o nome do DataSet.</span><span class="sxs-lookup"><span data-stu-id="c6aba-128">Specifies the name of the dataset.</span></span>
<span data-ttu-id="c6aba-129">Esse cmdlet é executado para as fatias que pertencem ao DataSet que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c6aba-129">This cmdlet gets runs for slices that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6aba-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6aba-130">-DefaultProfile</span></span>
<span data-ttu-id="c6aba-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c6aba-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6aba-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6aba-132">-ResourceGroupName</span></span>
<span data-ttu-id="c6aba-133">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="c6aba-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c6aba-134">Esse cmdlet obtém execuções de fábrica para as fatias que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c6aba-134">This cmdlet gets factory runs for slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6aba-135">-StartDatetime</span><span class="sxs-lookup"><span data-stu-id="c6aba-135">-StartDateTime</span></span>
<span data-ttu-id="c6aba-136">Especifica o início de um período de tempo como um objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="c6aba-136">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="c6aba-137">Esse cmdlet é executado para as fatias de dados que correspondem ao período de tempo.</span><span class="sxs-lookup"><span data-stu-id="c6aba-137">This cmdlet gets runs for the data slices that match this time period.</span></span>
<span data-ttu-id="c6aba-138">*StartDateTime* deve ser especificado no formato ISO8601, como nos exemplos a seguir: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (hora padrão do Pacífico) o designador de fuso horário padrão é UTC.</span><span class="sxs-lookup"><span data-stu-id="c6aba-138">*StartDateTime* must be specified in the ISO8601 format, as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="c6aba-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6aba-139">CommonParameters</span></span>
<span data-ttu-id="c6aba-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6aba-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6aba-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6aba-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6aba-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c6aba-142">INPUTS</span></span>

### <span data-ttu-id="c6aba-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c6aba-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="c6aba-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c6aba-144">System.String</span></span>

## <span data-ttu-id="c6aba-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c6aba-145">OUTPUTS</span></span>

### <span data-ttu-id="c6aba-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span><span class="sxs-lookup"><span data-stu-id="c6aba-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span></span>

## <span data-ttu-id="c6aba-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c6aba-147">NOTES</span></span>
* <span data-ttu-id="c6aba-148">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="c6aba-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c6aba-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6aba-149">RELATED LINKS</span></span>

[<span data-ttu-id="c6aba-150">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="c6aba-150">Get-AzureRmDataFactorySlice</span></span>](./Get-AzureRmDataFactorySlice.md)

