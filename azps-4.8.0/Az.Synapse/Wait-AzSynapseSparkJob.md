---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/wait-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
ms.openlocfilehash: c7137e9fda6c947755c8bd2e0091dd33347027fc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113454"
---
# <span data-ttu-id="233e1-101">Wait-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="233e1-101">Wait-AzSynapseSparkJob</span></span>

## <span data-ttu-id="233e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="233e1-102">SYNOPSIS</span></span>
<span data-ttu-id="233e1-103">Aguarda a conclusão de um trabalho do Spark do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="233e1-103">Waits for a Synapse Analytics Spark job to complete.</span></span>

## <span data-ttu-id="233e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="233e1-104">SYNTAX</span></span>

### <span data-ttu-id="233e1-105">WaitSparkJobByIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="233e1-105">WaitSparkJobByIdParameterSet (Default)</span></span>
```
Wait-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32>
 [-WaitIntervalInSeconds <Int32>] [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="233e1-106">WaitSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="233e1-106">WaitSparkJobByIdFromParentObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="233e1-107">WaitSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="233e1-107">WaitSparkJobByIdFromInputObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="233e1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="233e1-108">DESCRIPTION</span></span>
<span data-ttu-id="233e1-109">O cmdlet **Wait-AzSynapseSparkJob** aguarda a conclusão de um trabalho de análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="233e1-109">The **Wait-AzSynapseSparkJob** cmdlet waits for an Azure Synapse Analytics job to complete.</span></span>

## <span data-ttu-id="233e1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="233e1-110">EXAMPLES</span></span>

### <span data-ttu-id="233e1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="233e1-111">Example 1</span></span>
```powershell
PS C:\> Wait-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="233e1-112">Este comando aguarda o trabalho com a ID especificada ser concluída.</span><span class="sxs-lookup"><span data-stu-id="233e1-112">This command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="233e1-113">OS</span><span class="sxs-lookup"><span data-stu-id="233e1-113">PARAMETERS</span></span>

### <span data-ttu-id="233e1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="233e1-114">-DefaultProfile</span></span>
<span data-ttu-id="233e1-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="233e1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="233e1-116">-LivyId</span><span class="sxs-lookup"><span data-stu-id="233e1-116">-LivyId</span></span>
<span data-ttu-id="233e1-117">Identificador do trabalho Spark.</span><span class="sxs-lookup"><span data-stu-id="233e1-117">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="233e1-118">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="233e1-118">-SparkJobObject</span></span>
<span data-ttu-id="233e1-119">Objeto de entrada de trabalho Spark, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="233e1-119">Spark job input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="233e1-120">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="233e1-120">-SparkPoolName</span></span>
<span data-ttu-id="233e1-121">Nome do pool do Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="233e1-121">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="233e1-122">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="233e1-122">-SparkPoolObject</span></span>
<span data-ttu-id="233e1-123">Objeto de entrada do pool do Spark, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="233e1-123">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="233e1-124">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="233e1-124">-TimeoutInSeconds</span></span>
<span data-ttu-id="233e1-125">O período máximo de tempo de espera antes do erro. O valor padrão é para nunca tempo limite.</span><span class="sxs-lookup"><span data-stu-id="233e1-125">The maximum amount of time to wait before erroring out. Default value is to never timeout.</span></span>

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

### <span data-ttu-id="233e1-126">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="233e1-126">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="233e1-127">O intervalo de sondagem entre as verificações do status do trabalho, em segundos.</span><span class="sxs-lookup"><span data-stu-id="233e1-127">The polling interval between checks for the job status, in seconds.</span></span>

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

### <span data-ttu-id="233e1-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="233e1-128">-WorkspaceName</span></span>
<span data-ttu-id="233e1-129">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="233e1-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="233e1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="233e1-130">CommonParameters</span></span>
<span data-ttu-id="233e1-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="233e1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="233e1-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="233e1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="233e1-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="233e1-133">INPUTS</span></span>

### <span data-ttu-id="233e1-134">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="233e1-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="233e1-135">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="233e1-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="233e1-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="233e1-136">OUTPUTS</span></span>

### <span data-ttu-id="233e1-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="233e1-137">System.Boolean</span></span>

## <span data-ttu-id="233e1-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="233e1-138">NOTES</span></span>

## <span data-ttu-id="233e1-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="233e1-139">RELATED LINKS</span></span>
