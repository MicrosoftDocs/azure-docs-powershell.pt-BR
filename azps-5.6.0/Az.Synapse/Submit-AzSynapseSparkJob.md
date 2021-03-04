---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/submit-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
ms.openlocfilehash: 0555d9ba860d9a8c4c036fa9171d1fadc7a167eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893063"
---
# <span data-ttu-id="3574f-101">Submit-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="3574f-101">Submit-AzSynapseSparkJob</span></span>

## <span data-ttu-id="3574f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3574f-102">SYNOPSIS</span></span>
<span data-ttu-id="3574f-103">Envia um trabalho de Spark de Análise de Synapse.</span><span class="sxs-lookup"><span data-stu-id="3574f-103">Submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="3574f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3574f-104">SYNTAX</span></span>

### <span data-ttu-id="3574f-105">RunSparkJobParameterSetName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3574f-105">RunSparkJobParameterSetName (Default)</span></span>
```
Submit-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3574f-106">RunSparkJobByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3574f-106">RunSparkJobByParentObjectParameterSet</span></span>
```
Submit-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3574f-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3574f-107">DESCRIPTION</span></span>
<span data-ttu-id="3574f-108">O cmdlet **Submit-AzSynapseSparkJob** envia um trabalho de Spark de Análise de Synapse.</span><span class="sxs-lookup"><span data-stu-id="3574f-108">The **Submit-AzSynapseSparkJob** cmdlet submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="3574f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3574f-109">EXAMPLES</span></span>

### <span data-ttu-id="3574f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3574f-110">Example 1</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language Spark -Name WordCount_Java -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/wordcount.jar -MainClassName WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="3574f-111">Este comando envia um trabalho de Spark de Análise de Synapse.</span><span class="sxs-lookup"><span data-stu-id="3574f-111">This command submits a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="3574f-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3574f-112">Example 2</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language SparkDotNet -Name WordCount_Dotnet -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/wordcount.zip -MainExecutableFile WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/result -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="3574f-113">Este comando envia um trabalho do Synapse Analytics Spark .NET.</span><span class="sxs-lookup"><span data-stu-id="3574f-113">This command submits a Synapse Analytics Spark .NET job.</span></span>

### <span data-ttu-id="3574f-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="3574f-114">Example 3</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language PySpark -Name WordCount_Python -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/wordcount.py -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="3574f-115">Este comando envia um trabalho do Synapse Analytics PySpark.</span><span class="sxs-lookup"><span data-stu-id="3574f-115">This command submits a Synapse Analytics PySpark job.</span></span>

## <span data-ttu-id="3574f-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3574f-116">PARAMETERS</span></span>

### <span data-ttu-id="3574f-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="3574f-117">-CommandLineArgument</span></span>
<span data-ttu-id="3574f-118">Argumentos opcionais para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="3574f-118">Optional arguments to the job.</span></span> <span data-ttu-id="3574f-119">por exemplo, "--iteração 10000 --timeout 20s"</span><span class="sxs-lookup"><span data-stu-id="3574f-119">e.g. "--iteration 10000 --timeout 20s"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3574f-120">-Configuration</span><span class="sxs-lookup"><span data-stu-id="3574f-120">-Configuration</span></span>
<span data-ttu-id="3574f-121">Propriedades de configuração spark.</span><span class="sxs-lookup"><span data-stu-id="3574f-121">Spark configuration properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3574f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3574f-122">-DefaultProfile</span></span>
<span data-ttu-id="3574f-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3574f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3574f-124">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="3574f-124">-ExecutorCount</span></span>
<span data-ttu-id="3574f-125">Número de executores a serem alocados no pool de Spark especificado para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="3574f-125">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3574f-126">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="3574f-126">-ExecutorSize</span></span>
<span data-ttu-id="3574f-127">Número de núcleo e memória a serem usados para executores alocados no pool de Spark especificado para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="3574f-127">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3574f-128">-Language</span><span class="sxs-lookup"><span data-stu-id="3574f-128">-Language</span></span>
<span data-ttu-id="3574f-129">Idioma do trabalho a ser envio.</span><span class="sxs-lookup"><span data-stu-id="3574f-129">Language of the job to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3574f-130">-MainClassName</span><span class="sxs-lookup"><span data-stu-id="3574f-130">-MainClassName</span></span>
<span data-ttu-id="3574f-131">O identificador totalmente qualificado ou a classe principal que está no arquivo de definição principal.</span><span class="sxs-lookup"><span data-stu-id="3574f-131">The fully-qualified identifier or the main class that is in the main definition file.</span></span>
<span data-ttu-id="3574f-132">Obrigatório para o trabalho spark e .NET Spark.</span><span class="sxs-lookup"><span data-stu-id="3574f-132">Required for Spark and .NET Spark job.</span></span>
<span data-ttu-id="3574f-133">por exemplo, "org.apache.spark.examples.SparkPi"</span><span class="sxs-lookup"><span data-stu-id="3574f-133">e.g. "org.apache.spark.examples.SparkPi"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MainExecutableFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3574f-134">-MainDefinitionFile</span><span class="sxs-lookup"><span data-stu-id="3574f-134">-MainDefinitionFile</span></span>
<span data-ttu-id="3574f-135">O arquivo principal usado para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="3574f-135">The main file used for the job.</span></span>
<span data-ttu-id="3574f-136">por exemplo, abfss://filesystem@account.dfs.core.windows.net/mySpark.jar " "</span><span class="sxs-lookup"><span data-stu-id="3574f-136">e.g. "abfss://filesystem@account.dfs.core.windows.net/mySpark.jar"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3574f-137">-Name</span><span class="sxs-lookup"><span data-stu-id="3574f-137">-Name</span></span>
<span data-ttu-id="3574f-138">Nome do trabalho do Spark.</span><span class="sxs-lookup"><span data-stu-id="3574f-138">Name of Spark job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3574f-139">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="3574f-139">-ReferenceFile</span></span>
<span data-ttu-id="3574f-140">Arquivos adicionais usados para referência no arquivo de definição principal.</span><span class="sxs-lookup"><span data-stu-id="3574f-140">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="3574f-141">Lista de URI de armazenamento separado por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="3574f-141">Comma-separated storage URI list.</span></span> <span data-ttu-id="3574f-142">por exemplo, " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="3574f-142">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3574f-143">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="3574f-143">-SparkPoolName</span></span>
<span data-ttu-id="3574f-144">Nome do pool de spark synapse.</span><span class="sxs-lookup"><span data-stu-id="3574f-144">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkJobParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3574f-145">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="3574f-145">-SparkPoolObject</span></span>
<span data-ttu-id="3574f-146">Objeto de entrada do pool de centelha, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="3574f-146">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: RunSparkJobByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3574f-147">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3574f-147">-WorkspaceName</span></span>
<span data-ttu-id="3574f-148">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="3574f-148">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkJobParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3574f-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3574f-149">-Confirm</span></span>
<span data-ttu-id="3574f-150">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3574f-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3574f-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3574f-151">-WhatIf</span></span>
<span data-ttu-id="3574f-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3574f-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3574f-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3574f-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3574f-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3574f-154">CommonParameters</span></span>
<span data-ttu-id="3574f-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3574f-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3574f-156">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3574f-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3574f-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3574f-157">INPUTS</span></span>

### <span data-ttu-id="3574f-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="3574f-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="3574f-159">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3574f-159">OUTPUTS</span></span>

### <span data-ttu-id="3574f-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="3574f-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="3574f-161">NOTES</span><span class="sxs-lookup"><span data-stu-id="3574f-161">NOTES</span></span>

## <span data-ttu-id="3574f-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3574f-162">RELATED LINKS</span></span>
