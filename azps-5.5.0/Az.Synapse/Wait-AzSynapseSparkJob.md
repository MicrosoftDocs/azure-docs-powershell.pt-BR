---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/wait-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
ms.openlocfilehash: c7137e9fda6c947755c8bd2e0091dd33347027fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112373"
---
# <span data-ttu-id="5e36f-101">Wait-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="5e36f-101">Wait-AzSynapseSparkJob</span></span>

## <span data-ttu-id="5e36f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e36f-102">SYNOPSIS</span></span>
<span data-ttu-id="5e36f-103">Aguarda a conclusão de um trabalho do Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="5e36f-103">Waits for a Synapse Analytics Spark job to complete.</span></span>

## <span data-ttu-id="5e36f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e36f-104">SYNTAX</span></span>

### <span data-ttu-id="5e36f-105">WaitSparkJobByIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5e36f-105">WaitSparkJobByIdParameterSet (Default)</span></span>
```
Wait-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32>
 [-WaitIntervalInSeconds <Int32>] [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e36f-106">WaitSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e36f-106">WaitSparkJobByIdFromParentObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e36f-107">WaitSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e36f-107">WaitSparkJobByIdFromInputObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e36f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e36f-108">DESCRIPTION</span></span>
<span data-ttu-id="5e36f-109">O cmdlet **Wait-AzSynapseSpark Job** aguarda a conclusão de um trabalho do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5e36f-109">The **Wait-AzSynapseSparkJob** cmdlet waits for an Azure Synapse Analytics job to complete.</span></span>

## <span data-ttu-id="5e36f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5e36f-110">EXAMPLES</span></span>

### <span data-ttu-id="5e36f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5e36f-111">Example 1</span></span>
```powershell
PS C:\> Wait-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="5e36f-112">Esse comando aguarda a conclusão do trabalho com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="5e36f-112">This command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="5e36f-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e36f-113">PARAMETERS</span></span>

### <span data-ttu-id="5e36f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e36f-114">-DefaultProfile</span></span>
<span data-ttu-id="5e36f-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5e36f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e36f-116">-Ela</span><span class="sxs-lookup"><span data-stu-id="5e36f-116">-LivyId</span></span>
<span data-ttu-id="5e36f-117">Identificador do trabalho do Spark.</span><span class="sxs-lookup"><span data-stu-id="5e36f-117">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: WaitSparkJobByIdParameterSet, WaitSparkJobByIdFromParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: WaitSparkJobByIdFromInputObjectParameterSet
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e36f-118">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="5e36f-118">-SparkJobObject</span></span>
<span data-ttu-id="5e36f-119">Spark job input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="5e36f-119">Spark job input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob
Parameter Sets: WaitSparkJobByIdFromInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e36f-120">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="5e36f-120">-SparkPoolName</span></span>
<span data-ttu-id="5e36f-121">Nome do pool de miniapse.</span><span class="sxs-lookup"><span data-stu-id="5e36f-121">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: WaitSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e36f-122">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="5e36f-122">-SparkPoolObject</span></span>
<span data-ttu-id="5e36f-123">Objeto de entrada de pool de spark, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="5e36f-123">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: WaitSparkJobByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e36f-124">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="5e36f-124">-TimeoutInSeconds</span></span>
<span data-ttu-id="5e36f-125">A quantidade máxima de tempo para aguardar antes do erro. O valor padrão é nunca ter tempo de tempo.</span><span class="sxs-lookup"><span data-stu-id="5e36f-125">The maximum amount of time to wait before erroring out. Default value is to never timeout.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e36f-126">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="5e36f-126">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="5e36f-127">O intervalo de votação entre verifica o status do trabalho em segundos.</span><span class="sxs-lookup"><span data-stu-id="5e36f-127">The polling interval between checks for the job status, in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e36f-128">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="5e36f-128">-WorkspaceName</span></span>
<span data-ttu-id="5e36f-129">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="5e36f-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: WaitSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e36f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e36f-130">CommonParameters</span></span>
<span data-ttu-id="5e36f-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e36f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e36f-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e36f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e36f-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="5e36f-133">INPUTS</span></span>

### <span data-ttu-id="5e36f-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="5e36f-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="5e36f-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="5e36f-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="5e36f-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="5e36f-136">OUTPUTS</span></span>

### <span data-ttu-id="5e36f-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5e36f-137">System.Boolean</span></span>

## <span data-ttu-id="5e36f-138">Notas</span><span class="sxs-lookup"><span data-stu-id="5e36f-138">NOTES</span></span>

## <span data-ttu-id="5e36f-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e36f-139">RELATED LINKS</span></span>
