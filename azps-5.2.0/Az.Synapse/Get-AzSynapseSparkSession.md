---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
ms.openlocfilehash: 587183d72c6fdeec965f1ec1aa6aa88f5d6f36f9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262546"
---
# <span data-ttu-id="9dd75-101">Get-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="9dd75-101">Get-AzSynapseSparkSession</span></span>

## <span data-ttu-id="9dd75-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9dd75-102">SYNOPSIS</span></span>
<span data-ttu-id="9dd75-103">Obtém uma sessão do Spark Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="9dd75-103">Gets a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="9dd75-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9dd75-104">SYNTAX</span></span>

### <span data-ttu-id="9dd75-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9dd75-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dd75-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9dd75-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dd75-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9dd75-107">DESCRIPTION</span></span>
<span data-ttu-id="9dd75-108">O cmdlet **Get-AzSynapseSparkSession** Obtém informações sobre uma sessão do Spark do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="9dd75-108">The **Get-AzSynapseSparkSession** cmdlet gets information about an Azure Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="9dd75-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9dd75-109">EXAMPLES</span></span>

### <span data-ttu-id="9dd75-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9dd75-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="9dd75-111">Esse comando obtém todas as sessões do Spark no pool do Spark especificado.</span><span class="sxs-lookup"><span data-stu-id="9dd75-111">This command gets all the Spark sessions under the specified Spark pool.</span></span>

### <span data-ttu-id="9dd75-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9dd75-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 1
```

<span data-ttu-id="9dd75-113">Este comando obtém a sessão do Spark com a ID Livy especificada.</span><span class="sxs-lookup"><span data-stu-id="9dd75-113">This command gets the Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="9dd75-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="9dd75-114">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkSession
```

<span data-ttu-id="9dd75-115">Esse comando obtém todas as sessões do Spark no pool do Spark especificado por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="9dd75-115">This command gets all the Spark sessions under the specified Spark pool through pipeline.</span></span>

## <span data-ttu-id="9dd75-116">OS</span><span class="sxs-lookup"><span data-stu-id="9dd75-116">PARAMETERS</span></span>

### <span data-ttu-id="9dd75-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="9dd75-117">-ApplicationId</span></span>
<span data-ttu-id="9dd75-118">O identificador de aplicativo da sessão.</span><span class="sxs-lookup"><span data-stu-id="9dd75-118">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="9dd75-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dd75-119">-DefaultProfile</span></span>
<span data-ttu-id="9dd75-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9dd75-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dd75-121">-LivyId</span><span class="sxs-lookup"><span data-stu-id="9dd75-121">-LivyId</span></span>
<span data-ttu-id="9dd75-122">Identificador da sessão do Spark.</span><span class="sxs-lookup"><span data-stu-id="9dd75-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="9dd75-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="9dd75-123">-Name</span></span>
<span data-ttu-id="9dd75-124">Nome do pool do Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="9dd75-124">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="9dd75-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="9dd75-125">-SparkPoolName</span></span>
<span data-ttu-id="9dd75-126">Nome do pool do Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="9dd75-126">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="9dd75-127">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="9dd75-127">-SparkPoolObject</span></span>
<span data-ttu-id="9dd75-128">Objeto de entrada do pool do Spark, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="9dd75-128">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9dd75-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9dd75-129">-WorkspaceName</span></span>
<span data-ttu-id="9dd75-130">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="9dd75-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9dd75-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dd75-131">CommonParameters</span></span>
<span data-ttu-id="9dd75-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dd75-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dd75-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9dd75-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dd75-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9dd75-134">INPUTS</span></span>

### <span data-ttu-id="9dd75-135">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="9dd75-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="9dd75-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9dd75-136">OUTPUTS</span></span>

### <span data-ttu-id="9dd75-137">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="9dd75-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="9dd75-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9dd75-138">NOTES</span></span>

## <span data-ttu-id="9dd75-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9dd75-139">RELATED LINKS</span></span>
