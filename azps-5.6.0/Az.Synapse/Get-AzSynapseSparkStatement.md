---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
ms.openlocfilehash: 612ca41bf96a1372cda2b2abe984a56c1ec5411c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901542"
---
# <span data-ttu-id="b609a-101">Get-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="b609a-101">Get-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="b609a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b609a-102">SYNOPSIS</span></span>
<span data-ttu-id="b609a-103">Obtém uma instrução Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="b609a-103">Gets a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="b609a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b609a-104">SYNTAX</span></span>

### <span data-ttu-id="b609a-105">GetSparkStatementsByIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b609a-105">GetSparkStatementsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>]
 -SessionId <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b609a-106">GetSparkStatementsByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b609a-106">GetSparkStatementsByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> [-LivyId <Int32>] [-SessionId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b609a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b609a-107">DESCRIPTION</span></span>
<span data-ttu-id="b609a-108">O cmdlet **Get-AzSynapseSparkStatement** obtém informações sobre uma instrução Spark do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="b609a-108">The **Get-AzSynapseSparkStatement** cmdlet gets information about an Azure Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="b609a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b609a-109">EXAMPLES</span></span>

### <span data-ttu-id="b609a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b609a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120
```

<span data-ttu-id="b609a-111">Este comando obtém todas as instruções Spark em uma sessão Spark.</span><span class="sxs-lookup"><span data-stu-id="b609a-111">This command gets all the Spark statements under a Spark session.</span></span>

### <span data-ttu-id="b609a-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b609a-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120 -LivyId 0
```

<span data-ttu-id="b609a-113">Este comando obtém a instrução Spark com a ID de viol especificada.</span><span class="sxs-lookup"><span data-stu-id="b609a-113">This command gets the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="b609a-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b609a-114">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 107
PS C:\> $session | Get-AzSynapseSparkStatement
```

<span data-ttu-id="b609a-115">Este comando obtém todas as instruções Spark em uma sessão Spark por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="b609a-115">This command gets all the Spark statements under a Spark session through pipeline.</span></span>

## <span data-ttu-id="b609a-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b609a-116">PARAMETERS</span></span>

### <span data-ttu-id="b609a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b609a-117">-DefaultProfile</span></span>
<span data-ttu-id="b609a-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b609a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b609a-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="b609a-119">-LivyId</span></span>
<span data-ttu-id="b609a-120">Identificador da instrução Spark.</span><span class="sxs-lookup"><span data-stu-id="b609a-120">Identifier of Spark statement.</span></span>

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

### <span data-ttu-id="b609a-121">-SessionId</span><span class="sxs-lookup"><span data-stu-id="b609a-121">-SessionId</span></span>
<span data-ttu-id="b609a-122">Identificador da sessão Spark.</span><span class="sxs-lookup"><span data-stu-id="b609a-122">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: GetSparkStatementsByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b609a-123">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="b609a-123">-SessionObject</span></span>
<span data-ttu-id="b609a-124">Objeto de entrada do pool de centelha, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="b609a-124">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: GetSparkStatementsByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b609a-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="b609a-125">-SparkPoolName</span></span>
<span data-ttu-id="b609a-126">Nome do pool de spark synapse.</span><span class="sxs-lookup"><span data-stu-id="b609a-126">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b609a-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b609a-127">-WorkspaceName</span></span>
<span data-ttu-id="b609a-128">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="b609a-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b609a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b609a-129">CommonParameters</span></span>
<span data-ttu-id="b609a-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b609a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b609a-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b609a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b609a-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b609a-132">INPUTS</span></span>

### <span data-ttu-id="b609a-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="b609a-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="b609a-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b609a-134">OUTPUTS</span></span>

### <span data-ttu-id="b609a-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="b609a-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span></span>

## <span data-ttu-id="b609a-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="b609a-136">NOTES</span></span>

## <span data-ttu-id="b609a-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b609a-137">RELATED LINKS</span></span>
