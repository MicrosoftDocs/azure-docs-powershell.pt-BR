---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
ms.openlocfilehash: ea330bad812c7718d464a2ee237aa8c20c1f653f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890544"
---
# <span data-ttu-id="db9b4-101">Get-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="db9b4-101">Get-AzSynapseSparkJob</span></span>

## <span data-ttu-id="db9b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db9b4-102">SYNOPSIS</span></span>
<span data-ttu-id="db9b4-103">Obtém um trabalho de Spark de Análise de Synapse.</span><span class="sxs-lookup"><span data-stu-id="db9b4-103">Gets a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="db9b4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="db9b4-104">SYNTAX</span></span>

### <span data-ttu-id="db9b4-105">GetSparkJobsByIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="db9b4-105">GetSparkJobsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db9b4-106">GetSparkJobsByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db9b4-106">GetSparkJobsByIdFromParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db9b4-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="db9b4-107">DESCRIPTION</span></span>
<span data-ttu-id="db9b4-108">O cmdlet **Get-AzSynapseSparkJob** obtém um trabalho de Spark de Análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="db9b4-108">The **Get-AzSynapseSparkJob** cmdlet gets an Azure Synapse Analytics Spark job.</span></span>
<span data-ttu-id="db9b4-109">Se você não especificar um trabalho, este cmdlet obtém todos os trabalhos.</span><span class="sxs-lookup"><span data-stu-id="db9b4-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="db9b4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db9b4-110">EXAMPLES</span></span>

### <span data-ttu-id="db9b4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="db9b4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="db9b4-112">Este comando obtém todos os trabalhos em um pool de Spark.</span><span class="sxs-lookup"><span data-stu-id="db9b4-112">This command gets all jobs under a Spark pool.</span></span>

### <span data-ttu-id="db9b4-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="db9b4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 119
```

<span data-ttu-id="db9b4-114">Este comando obtém o trabalho com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="db9b4-114">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="db9b4-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="db9b4-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -ApplicationId application_1585023543211_0004
```

<span data-ttu-id="db9b4-116">Esse comando obtém o trabalho com a ID de aplicativo especificada.</span><span class="sxs-lookup"><span data-stu-id="db9b4-116">This command gets the job with the specified application ID.</span></span>

### <span data-ttu-id="db9b4-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="db9b4-117">Example 4</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkJob
```

<span data-ttu-id="db9b4-118">Este comando obtém todos os trabalhos em um pool de Spark por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="db9b4-118">This command gets all jobs under a Spark pool through pipeline.</span></span>

## <span data-ttu-id="db9b4-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="db9b4-119">PARAMETERS</span></span>

### <span data-ttu-id="db9b4-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="db9b4-120">-ApplicationId</span></span>
<span data-ttu-id="db9b4-121">O identificador de aplicativo da sessão.</span><span class="sxs-lookup"><span data-stu-id="db9b4-121">The Application identifier of the session.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9b4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db9b4-122">-DefaultProfile</span></span>
<span data-ttu-id="db9b4-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db9b4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db9b4-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="db9b4-124">-LivyId</span></span>
<span data-ttu-id="db9b4-125">Identificador do trabalho spark.</span><span class="sxs-lookup"><span data-stu-id="db9b4-125">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9b4-126">-Name</span><span class="sxs-lookup"><span data-stu-id="db9b4-126">-Name</span></span>
<span data-ttu-id="db9b4-127">Nome do trabalho do Spark.</span><span class="sxs-lookup"><span data-stu-id="db9b4-127">Name of Spark job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9b4-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="db9b4-128">-SparkPoolName</span></span>
<span data-ttu-id="db9b4-129">Nome do pool de spark synapse.</span><span class="sxs-lookup"><span data-stu-id="db9b4-129">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkJobsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9b4-130">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="db9b4-130">-SparkPoolObject</span></span>
<span data-ttu-id="db9b4-131">Objeto de entrada do pool de centelha, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="db9b4-131">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: GetSparkJobsByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db9b4-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="db9b4-132">-WorkspaceName</span></span>
<span data-ttu-id="db9b4-133">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="db9b4-133">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkJobsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9b4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db9b4-134">CommonParameters</span></span>
<span data-ttu-id="db9b4-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db9b4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db9b4-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db9b4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db9b4-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db9b4-137">INPUTS</span></span>

### <span data-ttu-id="db9b4-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="db9b4-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="db9b4-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="db9b4-139">OUTPUTS</span></span>

### <span data-ttu-id="db9b4-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="db9b4-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="db9b4-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="db9b4-141">NOTES</span></span>

## <span data-ttu-id="db9b4-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db9b4-142">RELATED LINKS</span></span>
