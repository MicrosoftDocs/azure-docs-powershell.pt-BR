---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/wait-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
ms.openlocfilehash: fa658b7727c07b7457c2a10c1ac42e3fdb5fe347
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892678"
---
# <span data-ttu-id="68993-101">Wait-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="68993-101">Wait-AzSynapseSparkJob</span></span>

## <span data-ttu-id="68993-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68993-102">SYNOPSIS</span></span>
<span data-ttu-id="68993-103">Aguarda a conclusão de um trabalho do Spark de Análise de Sinapse.</span><span class="sxs-lookup"><span data-stu-id="68993-103">Waits for a Synapse Analytics Spark job to complete.</span></span>

## <span data-ttu-id="68993-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="68993-104">SYNTAX</span></span>

### <span data-ttu-id="68993-105">WaitSparkJobByIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="68993-105">WaitSparkJobByIdParameterSet (Default)</span></span>
```
Wait-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32>
 [-WaitIntervalInSeconds <Int32>] [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="68993-106">WaitSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68993-106">WaitSparkJobByIdFromParentObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68993-107">WaitSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68993-107">WaitSparkJobByIdFromInputObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68993-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="68993-108">DESCRIPTION</span></span>
<span data-ttu-id="68993-109">O cmdlet **Wait-AzSynapseSparkJob** aguarda a conclusão de um trabalho do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="68993-109">The **Wait-AzSynapseSparkJob** cmdlet waits for an Azure Synapse Analytics job to complete.</span></span>

## <span data-ttu-id="68993-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="68993-110">EXAMPLES</span></span>

### <span data-ttu-id="68993-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="68993-111">Example 1</span></span>
```powershell
PS C:\> Wait-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="68993-112">Este comando aguarda a conclusão do trabalho com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="68993-112">This command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="68993-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="68993-113">PARAMETERS</span></span>

### <span data-ttu-id="68993-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68993-114">-DefaultProfile</span></span>
<span data-ttu-id="68993-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="68993-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68993-116">-LivyId</span><span class="sxs-lookup"><span data-stu-id="68993-116">-LivyId</span></span>
<span data-ttu-id="68993-117">Identificador do trabalho spark.</span><span class="sxs-lookup"><span data-stu-id="68993-117">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="68993-118">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="68993-118">-SparkJobObject</span></span>
<span data-ttu-id="68993-119">Objeto de entrada do trabalho de centelha, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="68993-119">Spark job input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="68993-120">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="68993-120">-SparkPoolName</span></span>
<span data-ttu-id="68993-121">Nome do pool de spark synapse.</span><span class="sxs-lookup"><span data-stu-id="68993-121">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="68993-122">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="68993-122">-SparkPoolObject</span></span>
<span data-ttu-id="68993-123">Objeto de entrada do pool de centelha, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="68993-123">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="68993-124">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="68993-124">-TimeoutInSeconds</span></span>
<span data-ttu-id="68993-125">O tempo máximo a ser aguardado antes do erro. O valor padrão é nunca passar do tempo.</span><span class="sxs-lookup"><span data-stu-id="68993-125">The maximum amount of time to wait before erroring out. Default value is to never timeout.</span></span>

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

### <span data-ttu-id="68993-126">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="68993-126">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="68993-127">O intervalo de sondagem entre verificações para o status do trabalho, em segundos.</span><span class="sxs-lookup"><span data-stu-id="68993-127">The polling interval between checks for the job status, in seconds.</span></span>

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

### <span data-ttu-id="68993-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="68993-128">-WorkspaceName</span></span>
<span data-ttu-id="68993-129">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="68993-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="68993-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68993-130">CommonParameters</span></span>
<span data-ttu-id="68993-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68993-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68993-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68993-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68993-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="68993-133">INPUTS</span></span>

### <span data-ttu-id="68993-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="68993-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="68993-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="68993-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="68993-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="68993-136">OUTPUTS</span></span>

### <span data-ttu-id="68993-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="68993-137">System.Boolean</span></span>

## <span data-ttu-id="68993-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="68993-138">NOTES</span></span>

## <span data-ttu-id="68993-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="68993-139">RELATED LINKS</span></span>
