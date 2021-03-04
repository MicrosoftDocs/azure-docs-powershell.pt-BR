---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
ms.openlocfilehash: 009f7033b7ecfe26e314a105d0bf88a7433962c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885729"
---
# <span data-ttu-id="eb2de-101">Get-AzDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="eb2de-101">Get-AzDataFactoryActivityWindow</span></span>

## <span data-ttu-id="eb2de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb2de-102">SYNOPSIS</span></span>
<span data-ttu-id="eb2de-103">Obtém informações sobre janelas de atividade associadas a um fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="eb2de-103">Gets information about activity windows associated with a data factory.</span></span>

## <span data-ttu-id="eb2de-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="eb2de-104">SYNTAX</span></span>

### <span data-ttu-id="eb2de-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="eb2de-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb2de-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="eb2de-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb2de-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="eb2de-107">DESCRIPTION</span></span>
<span data-ttu-id="eb2de-108">O cmdlet **Get-AzDataFactoryActivityWindow** obtém informações sobre as janelas de atividade associadas a um fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="eb2de-108">The **Get-AzDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="eb2de-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb2de-109">EXAMPLES</span></span>

### <span data-ttu-id="eb2de-110">Exemplo 1: Obter janelas de atividade associadas a um fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="eb2de-110">Example 1: Get activity windows associated with a data factory</span></span>
```
PS C:\>Get-AzDataFactoryActivityWindow -DataFactoryName "WikiADF" -ResourceGroupName "ADF" -Top 3
ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/17/2016 6:00:00 AM
WindowEnd         : 8/17/2016 7:00:00 AM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/16/2016 10:00:00 PM
WindowEnd         : 8/16/2016 11:00:00 PM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : WikiHiveActivity
ActivityType      : HDInsightHive
LinkedServiceName : HDILinkedService
WindowState       : Ready
WindowSubstate    : 
Duration          : 00:03:37.8020000
InputDatasets     : {DA_WikipediaClickEvents}
OutputDatasets    : {DA_CuratedWikiData}
PercentComplete   : 100
RunAttempts       : 1
RunStart          : 8/17/2016 11:09:23 PM
RunEnd            : 8/17/2016 11:13:01 PM
WindowStart       : 8/17/2016 3:00:00 AM
WindowEnd         : 8/17/2016 4:00:00 AM
```

<span data-ttu-id="eb2de-111">Este comando obtém informações sobre todas as janelas de atividade associadas ao fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="eb2de-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="eb2de-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="eb2de-112">PARAMETERS</span></span>

### <span data-ttu-id="eb2de-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="eb2de-113">-ActivityName</span></span>
<span data-ttu-id="eb2de-114">Especifica o nome da atividade.</span><span class="sxs-lookup"><span data-stu-id="eb2de-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="eb2de-115">Este cmdlet obtém janelas de atividade para a atividade especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="eb2de-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb2de-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="eb2de-116">-DataFactory</span></span>
<span data-ttu-id="eb2de-117">Especifica um **objeto PSDataFactory** retornado por um cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb2de-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="eb2de-118">Este cmdlet obtém janelas de atividade que pertencem ao fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="eb2de-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="eb2de-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="eb2de-119">-DataFactoryName</span></span>
<span data-ttu-id="eb2de-120">Especifica o nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="eb2de-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="eb2de-121">Este cmdlet obtém janelas de atividade que pertencem ao fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="eb2de-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="eb2de-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="eb2de-122">-DatasetName</span></span>
<span data-ttu-id="eb2de-123">Especifica o nome do conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="eb2de-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="eb2de-124">Este cmdlet obtém janelas de atividade que pertencem ao conjuntos de dados especificados por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="eb2de-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb2de-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb2de-125">-DefaultProfile</span></span>
<span data-ttu-id="eb2de-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="eb2de-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb2de-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="eb2de-127">-Filter</span></span>
<span data-ttu-id="eb2de-128">Especifica a janela de atividade expressa usando a gramática de filtro de Pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="eb2de-128">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="eb2de-129">Para obter informações sobre a gramática, consulte Sintaxe de Expressão OData para Pesquisa do Azure https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) no MSDN.</span><span class="sxs-lookup"><span data-stu-id="eb2de-129">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="eb2de-130">A lista de janelas de atividade é filtrada pela cadeia de caracteres de pesquisa especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="eb2de-130">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb2de-131">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="eb2de-131">-OrderBy</span></span>
<span data-ttu-id="eb2de-132">Especifica a ordem da resposta por um dos parâmetros da lista de janelas de atividade.</span><span class="sxs-lookup"><span data-stu-id="eb2de-132">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="eb2de-133">Esta é uma lista de propriedades separadas por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="eb2de-133">This is a list of comma separated properties.</span></span>
<span data-ttu-id="eb2de-134">Por exemplo: WindowStart, PercentComplete.</span><span class="sxs-lookup"><span data-stu-id="eb2de-134">For example: WindowStart, PercentComplete.</span></span>
<span data-ttu-id="eb2de-135">Por padrão, a ordem é ordem crescente (ASC).</span><span class="sxs-lookup"><span data-stu-id="eb2de-135">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="eb2de-136">Especifique DESC se você deseja ordenar a lista em ordem decrescente.</span><span class="sxs-lookup"><span data-stu-id="eb2de-136">Specify DESC if you want to order the list in descending order.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb2de-137">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="eb2de-137">-PipelineName</span></span>
<span data-ttu-id="eb2de-138">Especifica o nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="eb2de-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="eb2de-139">Este cmdlet obtém janelas de atividade que pertencem ao pipeline especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="eb2de-139">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb2de-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb2de-140">-ResourceGroupName</span></span>
<span data-ttu-id="eb2de-141">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eb2de-141">Specifies the name of the resource group.</span></span>
<span data-ttu-id="eb2de-142">Este cmdlet obtém janelas de atividade que pertencem ao grupo de recursos especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="eb2de-142">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="eb2de-143">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="eb2de-143">-RunEnd</span></span>
<span data-ttu-id="eb2de-144">Especifica a hora de término da janela de atividade em executar.</span><span class="sxs-lookup"><span data-stu-id="eb2de-144">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="eb2de-145">Este cmdlet obtém janelas de atividade cujas horas de executar se enquadram entre tempos *de RunStart* e *RunEnd.*</span><span class="sxs-lookup"><span data-stu-id="eb2de-145">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb2de-146">-RunStart</span><span class="sxs-lookup"><span data-stu-id="eb2de-146">-RunStart</span></span>
<span data-ttu-id="eb2de-147">Especifica a hora de início da janela de atividade em executar.</span><span class="sxs-lookup"><span data-stu-id="eb2de-147">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="eb2de-148">Este cmdlet obtém janelas de atividade cujas horas de executar se enquadram entre tempos *de RunStart* e *RunEnd.*</span><span class="sxs-lookup"><span data-stu-id="eb2de-148">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb2de-149">-Top</span><span class="sxs-lookup"><span data-stu-id="eb2de-149">-Top</span></span>
<span data-ttu-id="eb2de-150">Especifica o número máximo de janelas de atividade retornadas por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb2de-150">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb2de-151">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="eb2de-151">-WindowEnd</span></span>
<span data-ttu-id="eb2de-152">Especifica a janela de término da atividade.</span><span class="sxs-lookup"><span data-stu-id="eb2de-152">Specifies the end time of activity window.</span></span>
<span data-ttu-id="eb2de-153">Este cmdlet obtém janelas de atividade cujas horas se *enquadram entre* tempos windowStart e *WindowEnd.*</span><span class="sxs-lookup"><span data-stu-id="eb2de-153">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb2de-154">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="eb2de-154">-WindowStart</span></span>
<span data-ttu-id="eb2de-155">Especifica o horário de início da janela de atividade.</span><span class="sxs-lookup"><span data-stu-id="eb2de-155">Specifies the start time of activity window.</span></span>
<span data-ttu-id="eb2de-156">Este cmdlet obtém janelas de atividade cujas horas se *enquadram entre* tempos windowStart e *WindowEnd.*</span><span class="sxs-lookup"><span data-stu-id="eb2de-156">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb2de-157">-WindowState</span><span class="sxs-lookup"><span data-stu-id="eb2de-157">-WindowState</span></span>
<span data-ttu-id="eb2de-158">Especifica o estado da janela de atividade.</span><span class="sxs-lookup"><span data-stu-id="eb2de-158">Specifies the state of the activity window.</span></span>
<span data-ttu-id="eb2de-159">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="eb2de-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eb2de-160">Nenhum</span><span class="sxs-lookup"><span data-stu-id="eb2de-160">None</span></span>
- <span data-ttu-id="eb2de-161">Aguardando</span><span class="sxs-lookup"><span data-stu-id="eb2de-161">Waiting</span></span>
- <span data-ttu-id="eb2de-162">InProgress</span><span class="sxs-lookup"><span data-stu-id="eb2de-162">InProgress</span></span>
- <span data-ttu-id="eb2de-163">Pronto</span><span class="sxs-lookup"><span data-stu-id="eb2de-163">Ready</span></span>
- <span data-ttu-id="eb2de-164">Falha</span><span class="sxs-lookup"><span data-stu-id="eb2de-164">Failed</span></span>
- <span data-ttu-id="eb2de-165">Ignorado Este cmdlet obtém janelas de atividade que estão no estado especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="eb2de-165">Skipped This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb2de-166">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="eb2de-166">-WindowSubstate</span></span>
<span data-ttu-id="eb2de-167">Especifica o sub-estado da janela de atividade.</span><span class="sxs-lookup"><span data-stu-id="eb2de-167">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="eb2de-168">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="eb2de-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eb2de-169">Cancelado</span><span class="sxs-lookup"><span data-stu-id="eb2de-169">Canceled</span></span>
- <span data-ttu-id="eb2de-170">timedOut</span><span class="sxs-lookup"><span data-stu-id="eb2de-170">timedOut</span></span>
- <span data-ttu-id="eb2de-171">Validação Este cmdlet obtém janelas de atividade que estão no sub-estado especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="eb2de-171">Validating This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb2de-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb2de-172">CommonParameters</span></span>
<span data-ttu-id="eb2de-173">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb2de-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb2de-174">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb2de-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb2de-175">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb2de-175">INPUTS</span></span>

### <span data-ttu-id="eb2de-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="eb2de-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="eb2de-177">System.String</span><span class="sxs-lookup"><span data-stu-id="eb2de-177">System.String</span></span>

### <span data-ttu-id="eb2de-178">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="eb2de-178">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="eb2de-179">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="eb2de-179">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="eb2de-180">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="eb2de-180">OUTPUTS</span></span>

### <span data-ttu-id="eb2de-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span><span class="sxs-lookup"><span data-stu-id="eb2de-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span></span>

## <span data-ttu-id="eb2de-182">NOTES</span><span class="sxs-lookup"><span data-stu-id="eb2de-182">NOTES</span></span>

## <span data-ttu-id="eb2de-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb2de-183">RELATED LINKS</span></span>

[<span data-ttu-id="eb2de-184">Cmdlets de Fábricas de Dados do Azure</span><span class="sxs-lookup"><span data-stu-id="eb2de-184">Azure Data Factories Cmdlets</span></span>](./Az.DataFactory.md)


