---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
ms.openlocfilehash: efe733250c43d79aa8296db380ac453d44231c01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893066"
---
# <span data-ttu-id="3bc18-101">Get-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="3bc18-101">Get-AzSynapseSparkSession</span></span>

## <span data-ttu-id="3bc18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bc18-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc18-103">Obtém uma sessão de Spark de Análise de Synapse.</span><span class="sxs-lookup"><span data-stu-id="3bc18-103">Gets a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="3bc18-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3bc18-104">SYNTAX</span></span>

### <span data-ttu-id="3bc18-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3bc18-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bc18-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc18-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bc18-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3bc18-107">DESCRIPTION</span></span>
<span data-ttu-id="3bc18-108">O cmdlet **Get-AzSynapseSparkSession obtém** informações sobre uma sessão do Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="3bc18-108">The **Get-AzSynapseSparkSession** cmdlet gets information about an Azure Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="3bc18-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3bc18-109">EXAMPLES</span></span>

### <span data-ttu-id="3bc18-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3bc18-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="3bc18-111">Este comando obtém todas as sessões spark no pool de Spark especificado.</span><span class="sxs-lookup"><span data-stu-id="3bc18-111">This command gets all the Spark sessions under the specified Spark pool.</span></span>

### <span data-ttu-id="3bc18-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3bc18-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 1
```

<span data-ttu-id="3bc18-113">Este comando obtém a sessão Spark com a ID de viol especificada.</span><span class="sxs-lookup"><span data-stu-id="3bc18-113">This command gets the Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="3bc18-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="3bc18-114">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkSession
```

<span data-ttu-id="3bc18-115">Esse comando obtém todas as sessões spark no pool spark especificado por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="3bc18-115">This command gets all the Spark sessions under the specified Spark pool through pipeline.</span></span>

## <span data-ttu-id="3bc18-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3bc18-116">PARAMETERS</span></span>

### <span data-ttu-id="3bc18-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3bc18-117">-ApplicationId</span></span>
<span data-ttu-id="3bc18-118">O identificador de aplicativo da sessão.</span><span class="sxs-lookup"><span data-stu-id="3bc18-118">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="3bc18-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc18-119">-DefaultProfile</span></span>
<span data-ttu-id="3bc18-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc18-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bc18-121">-LivyId</span><span class="sxs-lookup"><span data-stu-id="3bc18-121">-LivyId</span></span>
<span data-ttu-id="3bc18-122">Identificador da sessão Spark.</span><span class="sxs-lookup"><span data-stu-id="3bc18-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="3bc18-123">-Name</span><span class="sxs-lookup"><span data-stu-id="3bc18-123">-Name</span></span>
<span data-ttu-id="3bc18-124">Nome do pool de spark synapse.</span><span class="sxs-lookup"><span data-stu-id="3bc18-124">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="3bc18-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="3bc18-125">-SparkPoolName</span></span>
<span data-ttu-id="3bc18-126">Nome do pool de spark synapse.</span><span class="sxs-lookup"><span data-stu-id="3bc18-126">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc18-127">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="3bc18-127">-SparkPoolObject</span></span>
<span data-ttu-id="3bc18-128">Objeto de entrada do pool de centelha, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="3bc18-128">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc18-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3bc18-129">-WorkspaceName</span></span>
<span data-ttu-id="3bc18-130">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="3bc18-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc18-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc18-131">CommonParameters</span></span>
<span data-ttu-id="3bc18-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bc18-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc18-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3bc18-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc18-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3bc18-134">INPUTS</span></span>

### <span data-ttu-id="3bc18-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="3bc18-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="3bc18-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3bc18-136">OUTPUTS</span></span>

### <span data-ttu-id="3bc18-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="3bc18-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="3bc18-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="3bc18-138">NOTES</span></span>

## <span data-ttu-id="3bc18-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3bc18-139">RELATED LINKS</span></span>
