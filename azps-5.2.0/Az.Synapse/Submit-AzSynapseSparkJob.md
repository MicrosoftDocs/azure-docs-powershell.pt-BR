---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/submit-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
ms.openlocfilehash: c8e710db383aae6698278ac4fb5ad7eb4344641b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260914"
---
# <span data-ttu-id="e387f-101">Submit-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="e387f-101">Submit-AzSynapseSparkJob</span></span>

## <span data-ttu-id="e387f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e387f-102">SYNOPSIS</span></span>
<span data-ttu-id="e387f-103">Envia um trabalho Spark de análise Synapse.</span><span class="sxs-lookup"><span data-stu-id="e387f-103">Submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="e387f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e387f-104">SYNTAX</span></span>

### <span data-ttu-id="e387f-105">RunSparkJobParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e387f-105">RunSparkJobParameterSetName (Default)</span></span>
```
Submit-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e387f-106">RunSparkJobByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e387f-106">RunSparkJobByParentObjectParameterSet</span></span>
```
Submit-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e387f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e387f-107">DESCRIPTION</span></span>
<span data-ttu-id="e387f-108">O cmdlet **Submit-AzSynapseSparkJob** envia um trabalho do analítico do Synapse.</span><span class="sxs-lookup"><span data-stu-id="e387f-108">The **Submit-AzSynapseSparkJob** cmdlet submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="e387f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e387f-109">EXAMPLES</span></span>

### <span data-ttu-id="e387f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e387f-110">Example 1</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language Spark -Name WordCount_Java -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/wordcount.jar -MainClassName WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="e387f-111">Esse comando envia um trabalho do Spark de análise Synapse.</span><span class="sxs-lookup"><span data-stu-id="e387f-111">This command submits a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="e387f-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e387f-112">Example 2</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language SparkDotNet -Name WordCount_Dotnet -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/wordcount.zip -MainExecutableFile WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/result -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="e387f-113">Esse comando envia um trabalho do Synapse analítico Spark .NET.</span><span class="sxs-lookup"><span data-stu-id="e387f-113">This command submits a Synapse Analytics Spark .NET job.</span></span>

### <span data-ttu-id="e387f-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e387f-114">Example 3</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language PySpark -Name WordCount_Python -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/wordcount.py -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="e387f-115">Esse comando envia um trabalho de Synapse analítico PySpark.</span><span class="sxs-lookup"><span data-stu-id="e387f-115">This command submits a Synapse Analytics PySpark job.</span></span>

## <span data-ttu-id="e387f-116">OS</span><span class="sxs-lookup"><span data-stu-id="e387f-116">PARAMETERS</span></span>

### <span data-ttu-id="e387f-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="e387f-117">-CommandLineArgument</span></span>
<span data-ttu-id="e387f-118">Argumentos opcionais para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="e387f-118">Optional arguments to the job.</span></span> <span data-ttu-id="e387f-119">por exemplo, "--iteração 10000--tempo limite 20s"</span><span class="sxs-lookup"><span data-stu-id="e387f-119">e.g. "--iteration 10000 --timeout 20s"</span></span>

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

### <span data-ttu-id="e387f-120">-Configuração</span><span class="sxs-lookup"><span data-stu-id="e387f-120">-Configuration</span></span>
<span data-ttu-id="e387f-121">Propriedades de configuração do Spark.</span><span class="sxs-lookup"><span data-stu-id="e387f-121">Spark configuration properties.</span></span>

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

### <span data-ttu-id="e387f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e387f-122">-DefaultProfile</span></span>
<span data-ttu-id="e387f-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e387f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e387f-124">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="e387f-124">-ExecutorCount</span></span>
<span data-ttu-id="e387f-125">Número de execuções a serem alocadas no pool do Spark especificado para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="e387f-125">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="e387f-126">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="e387f-126">-ExecutorSize</span></span>
<span data-ttu-id="e387f-127">Número de núcleo e memória a serem usados para execuções alocadas no pool do Spark especificado para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="e387f-127">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="e387f-128">-Idioma</span><span class="sxs-lookup"><span data-stu-id="e387f-128">-Language</span></span>
<span data-ttu-id="e387f-129">Idioma do trabalho para enviar.</span><span class="sxs-lookup"><span data-stu-id="e387f-129">Language of the job to submit.</span></span>

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

### <span data-ttu-id="e387f-130">-MainClassName</span><span class="sxs-lookup"><span data-stu-id="e387f-130">-MainClassName</span></span>
<span data-ttu-id="e387f-131">O identificador totalmente qualificado ou a classe principal que está no arquivo de definição principal.</span><span class="sxs-lookup"><span data-stu-id="e387f-131">The fully-qualified identifier or the main class that is in the main definition file.</span></span>
<span data-ttu-id="e387f-132">Obrigatório para o serviço Spark e .NET Spark.</span><span class="sxs-lookup"><span data-stu-id="e387f-132">Required for Spark and .NET Spark job.</span></span>
<span data-ttu-id="e387f-133">por exemplo, "org. Apache. Spark. examples. SparkPi"</span><span class="sxs-lookup"><span data-stu-id="e387f-133">e.g. "org.apache.spark.examples.SparkPi"</span></span>

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

### <span data-ttu-id="e387f-134">-MainDefinitionFile</span><span class="sxs-lookup"><span data-stu-id="e387f-134">-MainDefinitionFile</span></span>
<span data-ttu-id="e387f-135">O arquivo principal usado para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="e387f-135">The main file used for the job.</span></span>
<span data-ttu-id="e387f-136">por exemplo: " abfss://filesystem@account.dfs.core.windows.net/mySpark.jar "</span><span class="sxs-lookup"><span data-stu-id="e387f-136">e.g. "abfss://filesystem@account.dfs.core.windows.net/mySpark.jar"</span></span>

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

### <span data-ttu-id="e387f-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="e387f-137">-Name</span></span>
<span data-ttu-id="e387f-138">Nome do trabalho do Spark.</span><span class="sxs-lookup"><span data-stu-id="e387f-138">Name of Spark job.</span></span>

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

### <span data-ttu-id="e387f-139">-Referencefile</span><span class="sxs-lookup"><span data-stu-id="e387f-139">-ReferenceFile</span></span>
<span data-ttu-id="e387f-140">Arquivos adicionais usados para referência no arquivo de definição principal.</span><span class="sxs-lookup"><span data-stu-id="e387f-140">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="e387f-141">Lista de URI de armazenamento separada por vírgula.</span><span class="sxs-lookup"><span data-stu-id="e387f-141">Comma-separated storage URI list.</span></span> <span data-ttu-id="e387f-142">por exemplo abfss://filesystem@account.dfs.core.windows.net/file1.txt , ", abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="e387f-142">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

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

### <span data-ttu-id="e387f-143">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="e387f-143">-SparkPoolName</span></span>
<span data-ttu-id="e387f-144">Nome do pool do Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="e387f-144">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="e387f-145">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="e387f-145">-SparkPoolObject</span></span>
<span data-ttu-id="e387f-146">Objeto de entrada do pool do Spark, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="e387f-146">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e387f-147">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e387f-147">-WorkspaceName</span></span>
<span data-ttu-id="e387f-148">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="e387f-148">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e387f-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e387f-149">-Confirm</span></span>
<span data-ttu-id="e387f-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e387f-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e387f-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e387f-151">-WhatIf</span></span>
<span data-ttu-id="e387f-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e387f-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e387f-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e387f-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e387f-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e387f-154">CommonParameters</span></span>
<span data-ttu-id="e387f-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e387f-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e387f-156">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e387f-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e387f-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e387f-157">INPUTS</span></span>

### <span data-ttu-id="e387f-158">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="e387f-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="e387f-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e387f-159">OUTPUTS</span></span>

### <span data-ttu-id="e387f-160">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="e387f-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="e387f-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e387f-161">NOTES</span></span>

## <span data-ttu-id="e387f-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e387f-162">RELATED LINKS</span></span>
