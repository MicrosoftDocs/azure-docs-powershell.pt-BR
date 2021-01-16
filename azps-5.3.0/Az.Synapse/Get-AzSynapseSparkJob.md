---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
ms.openlocfilehash: 6af36401c8b1ebd4a059493ae7afd70c5e9b4dab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272434"
---
# <span data-ttu-id="575aa-101">Get-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="575aa-101">Get-AzSynapseSparkJob</span></span>

## <span data-ttu-id="575aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="575aa-102">SYNOPSIS</span></span>
<span data-ttu-id="575aa-103">Obtém um trabalho do Spark de análise Synapse.</span><span class="sxs-lookup"><span data-stu-id="575aa-103">Gets a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="575aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="575aa-104">SYNTAX</span></span>

### <span data-ttu-id="575aa-105">GetSparkJobsByIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="575aa-105">GetSparkJobsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="575aa-106">GetSparkJobsByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="575aa-106">GetSparkJobsByIdFromParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="575aa-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="575aa-107">DESCRIPTION</span></span>
<span data-ttu-id="575aa-108">O cmdlet **Get-AzSynapseSparkJob** Obtém um trabalho Spark de análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="575aa-108">The **Get-AzSynapseSparkJob** cmdlet gets an Azure Synapse Analytics Spark job.</span></span>
<span data-ttu-id="575aa-109">Se você não especificar um trabalho, esse cmdlet receberá todos os trabalhos.</span><span class="sxs-lookup"><span data-stu-id="575aa-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="575aa-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="575aa-110">EXAMPLES</span></span>

### <span data-ttu-id="575aa-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="575aa-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="575aa-112">Esse comando obtém todos os trabalhos em um pool do Spark.</span><span class="sxs-lookup"><span data-stu-id="575aa-112">This command gets all jobs under a Spark pool.</span></span>

### <span data-ttu-id="575aa-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="575aa-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 119
```

<span data-ttu-id="575aa-114">Este comando obtém o trabalho com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="575aa-114">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="575aa-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="575aa-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -ApplicationId application_1585023543211_0004
```

<span data-ttu-id="575aa-116">Este comando obtém o trabalho com a ID de aplicativo especificada.</span><span class="sxs-lookup"><span data-stu-id="575aa-116">This command gets the job with the specified application ID.</span></span>

### <span data-ttu-id="575aa-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="575aa-117">Example 4</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkJob
```

<span data-ttu-id="575aa-118">Esse comando obtém todos os trabalhos em um pool do Spark por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="575aa-118">This command gets all jobs under a Spark pool through pipeline.</span></span>

## <span data-ttu-id="575aa-119">OS</span><span class="sxs-lookup"><span data-stu-id="575aa-119">PARAMETERS</span></span>

### <span data-ttu-id="575aa-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="575aa-120">-ApplicationId</span></span>
<span data-ttu-id="575aa-121">O identificador de aplicativo da sessão.</span><span class="sxs-lookup"><span data-stu-id="575aa-121">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="575aa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="575aa-122">-DefaultProfile</span></span>
<span data-ttu-id="575aa-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="575aa-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="575aa-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="575aa-124">-LivyId</span></span>
<span data-ttu-id="575aa-125">Identificador do trabalho Spark.</span><span class="sxs-lookup"><span data-stu-id="575aa-125">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="575aa-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="575aa-126">-Name</span></span>
<span data-ttu-id="575aa-127">Nome do trabalho do Spark.</span><span class="sxs-lookup"><span data-stu-id="575aa-127">Name of Spark job.</span></span>

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

### <span data-ttu-id="575aa-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="575aa-128">-SparkPoolName</span></span>
<span data-ttu-id="575aa-129">Nome do pool do Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="575aa-129">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="575aa-130">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="575aa-130">-SparkPoolObject</span></span>
<span data-ttu-id="575aa-131">Objeto de entrada do pool do Spark, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="575aa-131">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="575aa-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="575aa-132">-WorkspaceName</span></span>
<span data-ttu-id="575aa-133">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="575aa-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="575aa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="575aa-134">CommonParameters</span></span>
<span data-ttu-id="575aa-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="575aa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="575aa-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="575aa-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="575aa-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="575aa-137">INPUTS</span></span>

### <span data-ttu-id="575aa-138">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="575aa-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="575aa-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="575aa-139">OUTPUTS</span></span>

### <span data-ttu-id="575aa-140">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="575aa-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="575aa-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="575aa-141">NOTES</span></span>

## <span data-ttu-id="575aa-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="575aa-142">RELATED LINKS</span></span>
