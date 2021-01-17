---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
ms.openlocfilehash: 5b18af8890d255dbd5514cccc0279acafe6bd611
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429924"
---
# <span data-ttu-id="1b265-101">Get-AzDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="1b265-101">Get-AzDataFactoryActivityWindow</span></span>

## <span data-ttu-id="1b265-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b265-102">SYNOPSIS</span></span>
<span data-ttu-id="1b265-103">Obtém informações sobre as janelas de atividade associadas a uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="1b265-103">Gets information about activity windows associated with a data factory.</span></span>

## <span data-ttu-id="1b265-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b265-104">SYNTAX</span></span>

### <span data-ttu-id="1b265-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="1b265-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b265-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1b265-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b265-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1b265-107">DESCRIPTION</span></span>
<span data-ttu-id="1b265-108">O cmdlet **Get-AzDataFactoryActivityWindow** Obtém informações sobre as janelas de atividade associadas a uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="1b265-108">The **Get-AzDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="1b265-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b265-109">EXAMPLES</span></span>

### <span data-ttu-id="1b265-110">Exemplo 1: obter janelas de atividade associadas a uma fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="1b265-110">Example 1: Get activity windows associated with a data factory</span></span>
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

<span data-ttu-id="1b265-111">Esse comando obtém informações sobre toda a janela de atividade associada ao data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="1b265-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="1b265-112">OS</span><span class="sxs-lookup"><span data-stu-id="1b265-112">PARAMETERS</span></span>

### <span data-ttu-id="1b265-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="1b265-113">-ActivityName</span></span>
<span data-ttu-id="1b265-114">Especifica o nome da atividade.</span><span class="sxs-lookup"><span data-stu-id="1b265-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="1b265-115">Esse cmdlet obtém as janelas de atividades para a atividade que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1b265-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b265-116">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="1b265-116">-DataFactory</span></span>
<span data-ttu-id="1b265-117">Especifica um objeto **PSDataFactory** retornado por um cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b265-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="1b265-118">Esse cmdlet obtém as janelas de atividades que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1b265-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b265-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="1b265-119">-DataFactoryName</span></span>
<span data-ttu-id="1b265-120">Especifica o nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="1b265-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="1b265-121">Esse cmdlet obtém as janelas de atividades que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1b265-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b265-122">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="1b265-122">-DatasetName</span></span>
<span data-ttu-id="1b265-123">Especifica o nome do DataSet.</span><span class="sxs-lookup"><span data-stu-id="1b265-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="1b265-124">Esse cmdlet obtém as janelas de atividades que pertencem ao conjunto de DataSet que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1b265-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b265-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b265-125">-DefaultProfile</span></span>
<span data-ttu-id="1b265-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1b265-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b265-127">-Filtro</span><span class="sxs-lookup"><span data-stu-id="1b265-127">-Filter</span></span>
<span data-ttu-id="1b265-128">Especifica a janela de atividade expressa usando a gramática do filtro de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="1b265-128">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="1b265-129">Para obter informações sobre a gramática, consulte Sintaxe de expressões OData para a pesquisa do Azure https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) no msdn.</span><span class="sxs-lookup"><span data-stu-id="1b265-129">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="1b265-130">A lista de janelas atividade é filtrada pela cadeia de caracteres de pesquisa que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1b265-130">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b265-131">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="1b265-131">-OrderBy</span></span>
<span data-ttu-id="1b265-132">Especifica para ordenar a resposta por um dos parâmetros de lista da janela atividade.</span><span class="sxs-lookup"><span data-stu-id="1b265-132">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="1b265-133">Esta é uma lista de propriedades separadas por vírgula.</span><span class="sxs-lookup"><span data-stu-id="1b265-133">This is a list of comma separated properties.</span></span>
<span data-ttu-id="1b265-134">Por exemplo: WindowStart, PorcentagemConcluída.</span><span class="sxs-lookup"><span data-stu-id="1b265-134">For example: WindowStart, PercentComplete.</span></span>
<span data-ttu-id="1b265-135">Por padrão, o pedido é de ordem crescente (ASC).</span><span class="sxs-lookup"><span data-stu-id="1b265-135">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="1b265-136">Especifique DESC se desejar ordenar a lista em ordem decrescente.</span><span class="sxs-lookup"><span data-stu-id="1b265-136">Specify DESC if you want to order the list in descending order.</span></span>

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

### <span data-ttu-id="1b265-137">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="1b265-137">-PipelineName</span></span>
<span data-ttu-id="1b265-138">Especifica o nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="1b265-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="1b265-139">Esse cmdlet obtém as janelas de atividades que pertencem ao pipeline especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1b265-139">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b265-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b265-140">-ResourceGroupName</span></span>
<span data-ttu-id="1b265-141">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1b265-141">Specifies the name of the resource group.</span></span>
<span data-ttu-id="1b265-142">Esse cmdlet obtém as janelas de atividades que pertencem ao grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1b265-142">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b265-143">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="1b265-143">-RunEnd</span></span>
<span data-ttu-id="1b265-144">Especifica a hora de término da execução da janela de atividade.</span><span class="sxs-lookup"><span data-stu-id="1b265-144">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="1b265-145">Esse cmdlet obtém janelas de atividades cujo tempo de execução cai entre *RunStart* e *RunEnd* vezes.</span><span class="sxs-lookup"><span data-stu-id="1b265-145">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="1b265-146">-RunStart</span><span class="sxs-lookup"><span data-stu-id="1b265-146">-RunStart</span></span>
<span data-ttu-id="1b265-147">Especifica a hora de início da janela atividade executada.</span><span class="sxs-lookup"><span data-stu-id="1b265-147">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="1b265-148">Esse cmdlet obtém janelas de atividades cujo tempo de execução cai entre *RunStart* e *RunEnd* vezes.</span><span class="sxs-lookup"><span data-stu-id="1b265-148">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="1b265-149">-Início</span><span class="sxs-lookup"><span data-stu-id="1b265-149">-Top</span></span>
<span data-ttu-id="1b265-150">Especifica o número máximo de janelas de atividade que o cmdlet retorna.</span><span class="sxs-lookup"><span data-stu-id="1b265-150">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

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

### <span data-ttu-id="1b265-151">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="1b265-151">-WindowEnd</span></span>
<span data-ttu-id="1b265-152">Especifica a hora de término da janela da atividade.</span><span class="sxs-lookup"><span data-stu-id="1b265-152">Specifies the end time of activity window.</span></span>
<span data-ttu-id="1b265-153">Esse cmdlet obtém as janelas de atividades cujo tempo cai entre *WindowStart* e *WindowEnd* vezes.</span><span class="sxs-lookup"><span data-stu-id="1b265-153">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="1b265-154">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="1b265-154">-WindowStart</span></span>
<span data-ttu-id="1b265-155">Especifica a janela hora de início da atividade.</span><span class="sxs-lookup"><span data-stu-id="1b265-155">Specifies the start time of activity window.</span></span>
<span data-ttu-id="1b265-156">Esse cmdlet obtém as janelas de atividades cujo tempo cai entre *WindowStart* e *WindowEnd* vezes.</span><span class="sxs-lookup"><span data-stu-id="1b265-156">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="1b265-157">-WindowState</span><span class="sxs-lookup"><span data-stu-id="1b265-157">-WindowState</span></span>
<span data-ttu-id="1b265-158">Especifica o estado da janela atividade.</span><span class="sxs-lookup"><span data-stu-id="1b265-158">Specifies the state of the activity window.</span></span>
<span data-ttu-id="1b265-159">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1b265-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1b265-160">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1b265-160">None</span></span>
- <span data-ttu-id="1b265-161">Faxes</span><span class="sxs-lookup"><span data-stu-id="1b265-161">Waiting</span></span>
- <span data-ttu-id="1b265-162">InProgress</span><span class="sxs-lookup"><span data-stu-id="1b265-162">InProgress</span></span>
- <span data-ttu-id="1b265-163">Está</span><span class="sxs-lookup"><span data-stu-id="1b265-163">Ready</span></span>
- <span data-ttu-id="1b265-164">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="1b265-164">Failed</span></span>
- <span data-ttu-id="1b265-165">Ignorado este cmdlet obtém as janelas de atividade que estão no estado especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1b265-165">Skipped This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b265-166">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="1b265-166">-WindowSubstate</span></span>
<span data-ttu-id="1b265-167">Especifica o subestado da janela atividade.</span><span class="sxs-lookup"><span data-stu-id="1b265-167">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="1b265-168">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1b265-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1b265-169">Anula</span><span class="sxs-lookup"><span data-stu-id="1b265-169">Canceled</span></span>
- <span data-ttu-id="1b265-170">timedOut</span><span class="sxs-lookup"><span data-stu-id="1b265-170">timedOut</span></span>
- <span data-ttu-id="1b265-171">Validar esse cmdlet obtém as janelas de atividade que estão no subestado que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1b265-171">Validating This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b265-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b265-172">CommonParameters</span></span>
<span data-ttu-id="1b265-173">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b265-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b265-174">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b265-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b265-175">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1b265-175">INPUTS</span></span>

### <span data-ttu-id="1b265-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1b265-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="1b265-177">System. String</span><span class="sxs-lookup"><span data-stu-id="1b265-177">System.String</span></span>

### <span data-ttu-id="1b265-178">System. Nullable ' 1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1b265-178">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1b265-179">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1b265-179">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1b265-180">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1b265-180">OUTPUTS</span></span>

### <span data-ttu-id="1b265-181">Microsoft. Azure. Commands. datafactorings. Models. PSActivityWindow</span><span class="sxs-lookup"><span data-stu-id="1b265-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span></span>

## <span data-ttu-id="1b265-182">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1b265-182">NOTES</span></span>

## <span data-ttu-id="1b265-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b265-183">RELATED LINKS</span></span>

[<span data-ttu-id="1b265-184">Cmdlets de fábricas de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="1b265-184">Azure Data Factories Cmdlets</span></span>](./Az.DataFactory.md)


