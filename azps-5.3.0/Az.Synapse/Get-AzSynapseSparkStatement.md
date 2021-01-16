---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
ms.openlocfilehash: a553f5e1e6b4929997cbd850ca199e6fd7acef08
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272431"
---
# <span data-ttu-id="c7344-101">Get-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="c7344-101">Get-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="c7344-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7344-102">SYNOPSIS</span></span>
<span data-ttu-id="c7344-103">Obtém uma instrução do Synapse Analytics Analytics.</span><span class="sxs-lookup"><span data-stu-id="c7344-103">Gets a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="c7344-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7344-104">SYNTAX</span></span>

### <span data-ttu-id="c7344-105">GetSparkStatementsByIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c7344-105">GetSparkStatementsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>]
 -SessionId <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7344-106">GetSparkStatementsByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7344-106">GetSparkStatementsByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> [-LivyId <Int32>] [-SessionId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7344-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c7344-107">DESCRIPTION</span></span>
<span data-ttu-id="c7344-108">O cmdlet **Get-AzSynapseSparkStatement** Obtém informações sobre uma declaração Spark do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="c7344-108">The **Get-AzSynapseSparkStatement** cmdlet gets information about an Azure Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="c7344-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7344-109">EXAMPLES</span></span>

### <span data-ttu-id="c7344-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c7344-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120
```

<span data-ttu-id="c7344-111">Esse comando obtém todas as instruções do Spark em uma sessão do Spark.</span><span class="sxs-lookup"><span data-stu-id="c7344-111">This command gets all the Spark statements under a Spark session.</span></span>

### <span data-ttu-id="c7344-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c7344-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120 -LivyId 0
```

<span data-ttu-id="c7344-113">Esse comando obtém a instrução Spark com a ID Livy especificada.</span><span class="sxs-lookup"><span data-stu-id="c7344-113">This command gets the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="c7344-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c7344-114">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 107
PS C:\> $session | Get-AzSynapseSparkStatement
```

<span data-ttu-id="c7344-115">Esse comando obtém todas as instruções do Spark em uma sessão do Spark por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="c7344-115">This command gets all the Spark statements under a Spark session through pipeline.</span></span>

## <span data-ttu-id="c7344-116">OS</span><span class="sxs-lookup"><span data-stu-id="c7344-116">PARAMETERS</span></span>

### <span data-ttu-id="c7344-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7344-117">-DefaultProfile</span></span>
<span data-ttu-id="c7344-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c7344-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7344-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="c7344-119">-LivyId</span></span>
<span data-ttu-id="c7344-120">Identificador da instrução Spark.</span><span class="sxs-lookup"><span data-stu-id="c7344-120">Identifier of Spark statement.</span></span>

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

### <span data-ttu-id="c7344-121">-Identificação_da_sessão</span><span class="sxs-lookup"><span data-stu-id="c7344-121">-SessionId</span></span>
<span data-ttu-id="c7344-122">Identificador da sessão do Spark.</span><span class="sxs-lookup"><span data-stu-id="c7344-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="c7344-123">-Sessionobject</span><span class="sxs-lookup"><span data-stu-id="c7344-123">-SessionObject</span></span>
<span data-ttu-id="c7344-124">Objeto de entrada do pool do Spark, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="c7344-124">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c7344-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="c7344-125">-SparkPoolName</span></span>
<span data-ttu-id="c7344-126">Nome do pool do Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="c7344-126">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="c7344-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c7344-127">-WorkspaceName</span></span>
<span data-ttu-id="c7344-128">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="c7344-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c7344-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7344-129">CommonParameters</span></span>
<span data-ttu-id="c7344-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7344-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7344-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7344-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7344-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c7344-132">INPUTS</span></span>

### <span data-ttu-id="c7344-133">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="c7344-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="c7344-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c7344-134">OUTPUTS</span></span>

### <span data-ttu-id="c7344-135">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="c7344-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span></span>

## <span data-ttu-id="c7344-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c7344-136">NOTES</span></span>

## <span data-ttu-id="c7344-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7344-137">RELATED LINKS</span></span>
