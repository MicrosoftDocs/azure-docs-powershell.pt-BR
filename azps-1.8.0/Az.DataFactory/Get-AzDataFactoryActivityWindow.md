---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
ms.openlocfilehash: 3e79f4c11a5df5da8c01c323405f78c36aa5245b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771060"
---
# <span data-ttu-id="ec00e-101">Get-AzDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="ec00e-101">Get-AzDataFactoryActivityWindow</span></span>

## <span data-ttu-id="ec00e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ec00e-102">SYNOPSIS</span></span>
<span data-ttu-id="ec00e-103">Obtém informações sobre as janelas de atividade associadas a uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="ec00e-103">Gets information about activity windows associated with a data factory.</span></span>

## <span data-ttu-id="ec00e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec00e-104">SYNTAX</span></span>

### <span data-ttu-id="ec00e-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ec00e-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec00e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ec00e-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec00e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ec00e-107">DESCRIPTION</span></span>
<span data-ttu-id="ec00e-108">O cmdlet **Get-AzDataFactoryActivityWindow** Obtém informações sobre as janelas de atividade associadas a uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="ec00e-108">The **Get-AzDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="ec00e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ec00e-109">EXAMPLES</span></span>

### <span data-ttu-id="ec00e-110">Exemplo 1: obter janelas de atividade associadas a uma fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="ec00e-110">Example 1: Get activity windows associated with a data factory</span></span>
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

<span data-ttu-id="ec00e-111">Esse comando obtém informações sobre toda a janela de atividade associada ao data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ec00e-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="ec00e-112">OS</span><span class="sxs-lookup"><span data-stu-id="ec00e-112">PARAMETERS</span></span>

### <span data-ttu-id="ec00e-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="ec00e-113">-ActivityName</span></span>
<span data-ttu-id="ec00e-114">Especifica o nome da atividade.</span><span class="sxs-lookup"><span data-stu-id="ec00e-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="ec00e-115">Esse cmdlet obtém as janelas de atividades para a atividade que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ec00e-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

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

### <span data-ttu-id="ec00e-116">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="ec00e-116">-DataFactory</span></span>
<span data-ttu-id="ec00e-117">Especifica um objeto **PSDataFactory** retornado por um cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec00e-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="ec00e-118">Esse cmdlet obtém as janelas de atividades que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ec00e-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ec00e-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="ec00e-119">-DataFactoryName</span></span>
<span data-ttu-id="ec00e-120">Especifica o nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="ec00e-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="ec00e-121">Esse cmdlet obtém as janelas de atividades que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ec00e-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ec00e-122">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="ec00e-122">-DatasetName</span></span>
<span data-ttu-id="ec00e-123">Especifica o nome do DataSet.</span><span class="sxs-lookup"><span data-stu-id="ec00e-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="ec00e-124">Esse cmdlet obtém as janelas de atividades que pertencem ao conjunto de DataSet que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ec00e-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="ec00e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec00e-125">-DefaultProfile</span></span>
<span data-ttu-id="ec00e-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ec00e-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec00e-127">-Filtro</span><span class="sxs-lookup"><span data-stu-id="ec00e-127">-Filter</span></span>
<span data-ttu-id="ec00e-128">Especifica a janela de atividade expressa usando a gramática do filtro de pesquisa do Azure.</span><span class="sxs-lookup"><span data-stu-id="ec00e-128">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="ec00e-129">Para obter informações sobre a gramática, consulte Sintaxe de expressões OData para a pesquisa do Azure https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) no msdn.</span><span class="sxs-lookup"><span data-stu-id="ec00e-129">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="ec00e-130">A lista de janelas atividade é filtrada pela cadeia de caracteres de pesquisa que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ec00e-130">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

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

### <span data-ttu-id="ec00e-131">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="ec00e-131">-OrderBy</span></span>
<span data-ttu-id="ec00e-132">Especifica para ordenar a resposta por um dos parâmetros de lista da janela atividade.</span><span class="sxs-lookup"><span data-stu-id="ec00e-132">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="ec00e-133">Esta é uma lista de propriedades separadas por vírgula.</span><span class="sxs-lookup"><span data-stu-id="ec00e-133">This is a list of comma separated properties.</span></span>
<span data-ttu-id="ec00e-134">Por exemplo: WindowStart, PorcentagemConcluída.</span><span class="sxs-lookup"><span data-stu-id="ec00e-134">For example: WindowStart, PercentComplete.</span></span>
<span data-ttu-id="ec00e-135">Por padrão, o pedido é de ordem crescente (ASC).</span><span class="sxs-lookup"><span data-stu-id="ec00e-135">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="ec00e-136">Especifique DESC se desejar ordenar a lista em ordem decrescente.</span><span class="sxs-lookup"><span data-stu-id="ec00e-136">Specify DESC if you want to order the list in descending order.</span></span>

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

### <span data-ttu-id="ec00e-137">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="ec00e-137">-PipelineName</span></span>
<span data-ttu-id="ec00e-138">Especifica o nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="ec00e-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="ec00e-139">Esse cmdlet obtém as janelas de atividades que pertencem ao pipeline especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ec00e-139">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="ec00e-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec00e-140">-ResourceGroupName</span></span>
<span data-ttu-id="ec00e-141">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ec00e-141">Specifies the name of the resource group.</span></span>
<span data-ttu-id="ec00e-142">Esse cmdlet obtém as janelas de atividades que pertencem ao grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ec00e-142">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ec00e-143">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="ec00e-143">-RunEnd</span></span>
<span data-ttu-id="ec00e-144">Especifica a hora de término da execução da janela de atividade.</span><span class="sxs-lookup"><span data-stu-id="ec00e-144">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="ec00e-145">Esse cmdlet obtém janelas de atividades cujo tempo de execução cai entre *RunStart* e *RunEnd* vezes.</span><span class="sxs-lookup"><span data-stu-id="ec00e-145">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="ec00e-146">-RunStart</span><span class="sxs-lookup"><span data-stu-id="ec00e-146">-RunStart</span></span>
<span data-ttu-id="ec00e-147">Especifica a hora de início da janela atividade executada.</span><span class="sxs-lookup"><span data-stu-id="ec00e-147">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="ec00e-148">Esse cmdlet obtém janelas de atividades cujo tempo de execução cai entre *RunStart* e *RunEnd* vezes.</span><span class="sxs-lookup"><span data-stu-id="ec00e-148">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="ec00e-149">-Início</span><span class="sxs-lookup"><span data-stu-id="ec00e-149">-Top</span></span>
<span data-ttu-id="ec00e-150">Especifica o número máximo de janelas de atividade que o cmdlet retorna.</span><span class="sxs-lookup"><span data-stu-id="ec00e-150">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

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

### <span data-ttu-id="ec00e-151">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="ec00e-151">-WindowEnd</span></span>
<span data-ttu-id="ec00e-152">Especifica a hora de término da janela da atividade.</span><span class="sxs-lookup"><span data-stu-id="ec00e-152">Specifies the end time of activity window.</span></span>
<span data-ttu-id="ec00e-153">Esse cmdlet obtém as janelas de atividades cujo tempo cai entre *WindowStart* e *WindowEnd* vezes.</span><span class="sxs-lookup"><span data-stu-id="ec00e-153">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="ec00e-154">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="ec00e-154">-WindowStart</span></span>
<span data-ttu-id="ec00e-155">Especifica a janela hora de início da atividade.</span><span class="sxs-lookup"><span data-stu-id="ec00e-155">Specifies the start time of activity window.</span></span>
<span data-ttu-id="ec00e-156">Esse cmdlet obtém as janelas de atividades cujo tempo cai entre *WindowStart* e *WindowEnd* vezes.</span><span class="sxs-lookup"><span data-stu-id="ec00e-156">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="ec00e-157">-WindowState</span><span class="sxs-lookup"><span data-stu-id="ec00e-157">-WindowState</span></span>
<span data-ttu-id="ec00e-158">Especifica o estado da janela atividade.</span><span class="sxs-lookup"><span data-stu-id="ec00e-158">Specifies the state of the activity window.</span></span>
<span data-ttu-id="ec00e-159">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ec00e-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ec00e-160">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ec00e-160">None</span></span>
- <span data-ttu-id="ec00e-161">Faxes</span><span class="sxs-lookup"><span data-stu-id="ec00e-161">Waiting</span></span>
- <span data-ttu-id="ec00e-162">InProgress</span><span class="sxs-lookup"><span data-stu-id="ec00e-162">InProgress</span></span>
- <span data-ttu-id="ec00e-163">Está</span><span class="sxs-lookup"><span data-stu-id="ec00e-163">Ready</span></span>
- <span data-ttu-id="ec00e-164">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="ec00e-164">Failed</span></span>
- <span data-ttu-id="ec00e-165">Ignorado este cmdlet obtém as janelas de atividade que estão no estado especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ec00e-165">Skipped This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

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

### <span data-ttu-id="ec00e-166">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="ec00e-166">-WindowSubstate</span></span>
<span data-ttu-id="ec00e-167">Especifica o subestado da janela atividade.</span><span class="sxs-lookup"><span data-stu-id="ec00e-167">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="ec00e-168">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ec00e-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ec00e-169">Anula</span><span class="sxs-lookup"><span data-stu-id="ec00e-169">Canceled</span></span>
- <span data-ttu-id="ec00e-170">timedOut</span><span class="sxs-lookup"><span data-stu-id="ec00e-170">timedOut</span></span>
- <span data-ttu-id="ec00e-171">Validar esse cmdlet obtém as janelas de atividade que estão no subestado que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ec00e-171">Validating This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

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

### <span data-ttu-id="ec00e-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec00e-172">CommonParameters</span></span>
<span data-ttu-id="ec00e-173">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec00e-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec00e-174">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec00e-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec00e-175">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ec00e-175">INPUTS</span></span>

### <span data-ttu-id="ec00e-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ec00e-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="ec00e-177">System. String</span><span class="sxs-lookup"><span data-stu-id="ec00e-177">System.String</span></span>

### <span data-ttu-id="ec00e-178">System. Nullable ' 1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ec00e-178">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ec00e-179">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ec00e-179">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ec00e-180">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ec00e-180">OUTPUTS</span></span>

### <span data-ttu-id="ec00e-181">Microsoft. Azure. Commands. datafactorings. Models. PSActivityWindow</span><span class="sxs-lookup"><span data-stu-id="ec00e-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span></span>

## <span data-ttu-id="ec00e-182">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ec00e-182">NOTES</span></span>

## <span data-ttu-id="ec00e-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec00e-183">RELATED LINKS</span></span>

[<span data-ttu-id="ec00e-184">Cmdlets de fábricas de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="ec00e-184">Azure Data Factories Cmdlets</span></span>](./Az.DataFactory.md)


