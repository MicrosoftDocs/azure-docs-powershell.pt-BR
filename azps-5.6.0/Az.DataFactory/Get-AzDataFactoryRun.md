---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
ms.openlocfilehash: 2dbab7978716d6bb960c1804abf9e86246571e29
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888302"
---
# <span data-ttu-id="34202-101">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="34202-101">Get-AzDataFactoryRun</span></span>

## <span data-ttu-id="34202-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34202-102">SYNOPSIS</span></span>
<span data-ttu-id="34202-103">Obtém executa para uma fatia de dados de um conjuntos de dados no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="34202-103">Gets runs for a data slice of a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="34202-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="34202-104">SYNTAX</span></span>

### <span data-ttu-id="34202-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="34202-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34202-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="34202-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34202-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="34202-107">DESCRIPTION</span></span>
<span data-ttu-id="34202-108">O cmdlet **Get-AzDataFactoryRun** obtém as executas para uma fatia de dados de um conjuntos de dados no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="34202-108">The **Get-AzDataFactoryRun** cmdlet gets the runs for a data slice of a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="34202-109">Um conjuntos de dados em uma fábrica de dados é composto de fatias ao longo do eixo do tempo.</span><span class="sxs-lookup"><span data-stu-id="34202-109">A dataset in a data factory is composed of slices over the time axis.</span></span>
<span data-ttu-id="34202-110">A largura de uma fatia é determinada pelo cronograma, por hora ou diariamente.</span><span class="sxs-lookup"><span data-stu-id="34202-110">The width of a slice is determined by the schedule, either hourly or daily.</span></span>
<span data-ttu-id="34202-111">Uma run é uma unidade de processamento de uma fatia.</span><span class="sxs-lookup"><span data-stu-id="34202-111">A run is a unit of processing for a slice.</span></span>
<span data-ttu-id="34202-112">Pode haver uma ou mais correções para uma fatia em caso de recuperação ou caso você reprise sua fatia devido a falhas.</span><span class="sxs-lookup"><span data-stu-id="34202-112">There could be one or more runs for a slice in case of retries or in case you rerun your slice due to failures.</span></span>
<span data-ttu-id="34202-113">Uma fatia é identificada pela hora de início.</span><span class="sxs-lookup"><span data-stu-id="34202-113">A slice is identified by its start time.</span></span>
<span data-ttu-id="34202-114">Para obter a hora de início de uma fatia, use o cmdlet Get-AzDataFactorySlice de entrada.</span><span class="sxs-lookup"><span data-stu-id="34202-114">To obtain the start time of a slice, use the Get-AzDataFactorySlice cmdlet.</span></span>
<span data-ttu-id="34202-115">Por exemplo, para obter uma corrida para a seguinte fatia, use a hora de início 2015-04-02T20:00:00.</span><span class="sxs-lookup"><span data-stu-id="34202-115">For example, to get a run for the following slice, use the start time 2015-04-02T20:00:00.</span></span>
<span data-ttu-id="34202-116">ResourceGroupName : ADF DataFactoryName : SPDataFactory0924 DatasetName : MarketingCampaignEffectivenessBlobDataset Start : 5/2/2014 8:00:00 PM Fim : 03/05/2014 8:00:00 PM RetryCount : 0 Status : Ready LatencyStatus :</span><span class="sxs-lookup"><span data-stu-id="34202-116">ResourceGroupName  : ADF DataFactoryName : SPDataFactory0924 DatasetName : MarketingCampaignEffectivenessBlobDataset Start : 5/2/2014 8:00:00 PM End : 5/3/2014 8:00:00 PM RetryCount : 0 Status : Ready LatencyStatus :</span></span>

## <span data-ttu-id="34202-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34202-117">EXAMPLES</span></span>

### <span data-ttu-id="34202-118">Exemplo 1: Obter um conjuntos de dados</span><span class="sxs-lookup"><span data-stu-id="34202-118">Example 1: Get a dataset</span></span>
```
PS C:\>Get-AzDataFactoryRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z
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

<span data-ttu-id="34202-119">Este comando obtém todas as executados para fatias do conjuntos de dados chamado DAWikiAggregatedData no fábrica de dados chamado WikiADF que começa a partir das 16:00 GMT de 21/05/2014.</span><span class="sxs-lookup"><span data-stu-id="34202-119">This command gets all runs for slices of the dataset named DAWikiAggregatedData in the data factory named WikiADF that start from 4 PM GMT on 05/21/2014.</span></span>

## <span data-ttu-id="34202-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="34202-120">PARAMETERS</span></span>

### <span data-ttu-id="34202-121">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="34202-121">-DataFactory</span></span>
<span data-ttu-id="34202-122">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="34202-122">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="34202-123">Este cmdlet é executado para fatias que pertencem ao fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="34202-123">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="34202-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="34202-124">-DataFactoryName</span></span>
<span data-ttu-id="34202-125">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="34202-125">Specifies the name of a data factory.</span></span>
<span data-ttu-id="34202-126">Este cmdlet é executado para fatias que pertencem ao fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="34202-126">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="34202-127">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="34202-127">-DatasetName</span></span>
<span data-ttu-id="34202-128">Especifica o nome do conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="34202-128">Specifies the name of the dataset.</span></span>
<span data-ttu-id="34202-129">Este cmdlet é executado para fatias que pertencem ao conjuntos de dados especificados por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="34202-129">This cmdlet gets runs for slices that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="34202-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34202-130">-DefaultProfile</span></span>
<span data-ttu-id="34202-131">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="34202-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34202-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34202-132">-ResourceGroupName</span></span>
<span data-ttu-id="34202-133">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="34202-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="34202-134">Este cmdlet obtém as executações de fábrica para fatias que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="34202-134">This cmdlet gets factory runs for slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="34202-135">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="34202-135">-StartDateTime</span></span>
<span data-ttu-id="34202-136">Especifica o início de um período de tempo como um **objeto DateTime.**</span><span class="sxs-lookup"><span data-stu-id="34202-136">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="34202-137">Este cmdlet obtém as runs para as fatias de dados que corresponderem a esse período de tempo.</span><span class="sxs-lookup"><span data-stu-id="34202-137">This cmdlet gets runs for the data slices that match this time period.</span></span>
<span data-ttu-id="34202-138">*StartDateTime* deve ser especificado no formato ISO8601, como nos seguintes exemplos: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Hora Padrão do Pacífico) O designador de fuso horário padrão é UTC.</span><span class="sxs-lookup"><span data-stu-id="34202-138">*StartDateTime* must be specified in the ISO8601 format, as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="34202-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34202-139">CommonParameters</span></span>
<span data-ttu-id="34202-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34202-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34202-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34202-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34202-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="34202-142">INPUTS</span></span>

### <span data-ttu-id="34202-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="34202-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="34202-144">System.String</span><span class="sxs-lookup"><span data-stu-id="34202-144">System.String</span></span>

## <span data-ttu-id="34202-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="34202-145">OUTPUTS</span></span>

### <span data-ttu-id="34202-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span><span class="sxs-lookup"><span data-stu-id="34202-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span></span>

## <span data-ttu-id="34202-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="34202-147">NOTES</span></span>
* <span data-ttu-id="34202-148">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="34202-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="34202-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34202-149">RELATED LINKS</span></span>

[<span data-ttu-id="34202-150">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="34202-150">Get-AzDataFactorySlice</span></span>](./Get-AzDataFactorySlice.md)


