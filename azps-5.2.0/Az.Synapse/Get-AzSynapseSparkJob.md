---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
ms.openlocfilehash: 6af36401c8b1ebd4a059493ae7afd70c5e9b4dab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259229"
---
# <span data-ttu-id="8cc59-101">Get-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="8cc59-101">Get-AzSynapseSparkJob</span></span>

## <span data-ttu-id="8cc59-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8cc59-102">SYNOPSIS</span></span>
<span data-ttu-id="8cc59-103">Obtém um trabalho do Spark de análise Synapse.</span><span class="sxs-lookup"><span data-stu-id="8cc59-103">Gets a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="8cc59-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8cc59-104">SYNTAX</span></span>

### <span data-ttu-id="8cc59-105">GetSparkJobsByIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8cc59-105">GetSparkJobsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cc59-106">GetSparkJobsByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cc59-106">GetSparkJobsByIdFromParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cc59-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8cc59-107">DESCRIPTION</span></span>
<span data-ttu-id="8cc59-108">O cmdlet **Get-AzSynapseSparkJob** Obtém um trabalho Spark de análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="8cc59-108">The **Get-AzSynapseSparkJob** cmdlet gets an Azure Synapse Analytics Spark job.</span></span>
<span data-ttu-id="8cc59-109">Se você não especificar um trabalho, esse cmdlet receberá todos os trabalhos.</span><span class="sxs-lookup"><span data-stu-id="8cc59-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="8cc59-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8cc59-110">EXAMPLES</span></span>

### <span data-ttu-id="8cc59-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8cc59-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="8cc59-112">Esse comando obtém todos os trabalhos em um pool do Spark.</span><span class="sxs-lookup"><span data-stu-id="8cc59-112">This command gets all jobs under a Spark pool.</span></span>

### <span data-ttu-id="8cc59-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8cc59-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 119
```

<span data-ttu-id="8cc59-114">Este comando obtém o trabalho com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="8cc59-114">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="8cc59-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="8cc59-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -ApplicationId application_1585023543211_0004
```

<span data-ttu-id="8cc59-116">Este comando obtém o trabalho com a ID de aplicativo especificada.</span><span class="sxs-lookup"><span data-stu-id="8cc59-116">This command gets the job with the specified application ID.</span></span>

### <span data-ttu-id="8cc59-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="8cc59-117">Example 4</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkJob
```

<span data-ttu-id="8cc59-118">Esse comando obtém todos os trabalhos em um pool do Spark por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="8cc59-118">This command gets all jobs under a Spark pool through pipeline.</span></span>

## <span data-ttu-id="8cc59-119">OS</span><span class="sxs-lookup"><span data-stu-id="8cc59-119">PARAMETERS</span></span>

### <span data-ttu-id="8cc59-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8cc59-120">-ApplicationId</span></span>
<span data-ttu-id="8cc59-121">O identificador de aplicativo da sessão.</span><span class="sxs-lookup"><span data-stu-id="8cc59-121">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="8cc59-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cc59-122">-DefaultProfile</span></span>
<span data-ttu-id="8cc59-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc59-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cc59-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="8cc59-124">-LivyId</span></span>
<span data-ttu-id="8cc59-125">Identificador do trabalho Spark.</span><span class="sxs-lookup"><span data-stu-id="8cc59-125">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="8cc59-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="8cc59-126">-Name</span></span>
<span data-ttu-id="8cc59-127">Nome do trabalho do Spark.</span><span class="sxs-lookup"><span data-stu-id="8cc59-127">Name of Spark job.</span></span>

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

### <span data-ttu-id="8cc59-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="8cc59-128">-SparkPoolName</span></span>
<span data-ttu-id="8cc59-129">Nome do pool do Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="8cc59-129">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="8cc59-130">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="8cc59-130">-SparkPoolObject</span></span>
<span data-ttu-id="8cc59-131">Objeto de entrada do pool do Spark, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="8cc59-131">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8cc59-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8cc59-132">-WorkspaceName</span></span>
<span data-ttu-id="8cc59-133">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="8cc59-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8cc59-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cc59-134">CommonParameters</span></span>
<span data-ttu-id="8cc59-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cc59-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cc59-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8cc59-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cc59-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8cc59-137">INPUTS</span></span>

### <span data-ttu-id="8cc59-138">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="8cc59-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="8cc59-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8cc59-139">OUTPUTS</span></span>

### <span data-ttu-id="8cc59-140">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="8cc59-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="8cc59-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8cc59-141">NOTES</span></span>

## <span data-ttu-id="8cc59-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8cc59-142">RELATED LINKS</span></span>
