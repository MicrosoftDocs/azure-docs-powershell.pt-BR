---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/start-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
ms.openlocfilehash: b066807d812fc9a74b36b2826cc978589d39ea49
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112381"
---
# <span data-ttu-id="a0514-101">Start-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="a0514-101">Start-AzSynapseSparkSession</span></span>

## <span data-ttu-id="a0514-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0514-102">SYNOPSIS</span></span>
<span data-ttu-id="a0514-103">Inicia uma sessão synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="a0514-103">Starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="a0514-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0514-104">SYNTAX</span></span>

### <span data-ttu-id="a0514-105">CreateByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a0514-105">CreateByNameParameterSet (Default)</span></span>
```
Start-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0514-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0514-106">CreateByParentObjectParameterSet</span></span>
```
Start-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0514-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a0514-107">DESCRIPTION</span></span>
<span data-ttu-id="a0514-108">O cmdlet **Start-AzSynapseSparkSession** inicia uma sessão synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="a0514-108">The **Start-AzSynapseSparkSession** cmdlet starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="a0514-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a0514-109">EXAMPLES</span></span>

### <span data-ttu-id="a0514-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a0514-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="a0514-111">Esse comando inicia uma sessão do Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="a0514-111">This command starts an Azure Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="a0514-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a0514-112">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Start-AzSynapseSparkSession -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="a0514-113">Esse comando inicia uma sessão do Azure Synapse Analytics Spark por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="a0514-113">This command starts an Azure Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="a0514-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0514-114">PARAMETERS</span></span>

### <span data-ttu-id="a0514-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0514-115">-AsJob</span></span>
<span data-ttu-id="a0514-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a0514-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0514-117">-Configuração</span><span class="sxs-lookup"><span data-stu-id="a0514-117">-Configuration</span></span>
<span data-ttu-id="a0514-118">Propriedades de configuração de spark.</span><span class="sxs-lookup"><span data-stu-id="a0514-118">Spark configuration properties.</span></span>

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

### <span data-ttu-id="a0514-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0514-119">-DefaultProfile</span></span>
<span data-ttu-id="a0514-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a0514-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0514-121">-IndemenCount</span><span class="sxs-lookup"><span data-stu-id="a0514-121">-ExecutorCount</span></span>
<span data-ttu-id="a0514-122">Número de casais a serem alocadas no pool de Spark especificado para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="a0514-122">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="a0514-123">-WidgetSize</span><span class="sxs-lookup"><span data-stu-id="a0514-123">-ExecutorSize</span></span>
<span data-ttu-id="a0514-124">Número de núcleo e memória a serem usados para os que foram alocados no Pool de Spark especificado para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="a0514-124">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="a0514-125">-Idioma</span><span class="sxs-lookup"><span data-stu-id="a0514-125">-Language</span></span>
<span data-ttu-id="a0514-126">Idioma do código de execução.</span><span class="sxs-lookup"><span data-stu-id="a0514-126">Language of the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0514-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0514-127">-Name</span></span>
<span data-ttu-id="a0514-128">Nome da sessão do Spark.</span><span class="sxs-lookup"><span data-stu-id="a0514-128">Name of Spark session.</span></span>

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

### <span data-ttu-id="a0514-129">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="a0514-129">-ReferenceFile</span></span>
<span data-ttu-id="a0514-130">Arquivos adicionais usados para referência no arquivo de definição principal.</span><span class="sxs-lookup"><span data-stu-id="a0514-130">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="a0514-131">Lista de URI de armazenamento separado por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="a0514-131">Comma-separated storage URI list.</span></span> <span data-ttu-id="a0514-132">por exemplo, " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="a0514-132">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

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

### <span data-ttu-id="a0514-133">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="a0514-133">-SparkPoolName</span></span>
<span data-ttu-id="a0514-134">Nome do pool de miniapse.</span><span class="sxs-lookup"><span data-stu-id="a0514-134">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0514-135">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="a0514-135">-SparkPoolObject</span></span>
<span data-ttu-id="a0514-136">Objeto de entrada de pool de spark, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="a0514-136">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0514-137">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="a0514-137">-WorkspaceName</span></span>
<span data-ttu-id="a0514-138">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="a0514-138">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0514-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a0514-139">-Confirm</span></span>
<span data-ttu-id="a0514-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0514-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0514-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0514-141">-WhatIf</span></span>
<span data-ttu-id="a0514-142">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a0514-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0514-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a0514-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0514-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0514-144">CommonParameters</span></span>
<span data-ttu-id="a0514-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0514-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0514-146">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0514-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0514-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="a0514-147">INPUTS</span></span>

### <span data-ttu-id="a0514-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="a0514-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="a0514-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="a0514-149">OUTPUTS</span></span>

### <span data-ttu-id="a0514-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="a0514-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="a0514-151">Notas</span><span class="sxs-lookup"><span data-stu-id="a0514-151">NOTES</span></span>

## <span data-ttu-id="a0514-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0514-152">RELATED LINKS</span></span>
