---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
ms.openlocfilehash: 587183d72c6fdeec965f1ec1aa6aa88f5d6f36f9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118897"
---
# <span data-ttu-id="ed9bf-101">Get-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="ed9bf-101">Get-AzSynapseSparkSession</span></span>

## <span data-ttu-id="ed9bf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed9bf-102">SYNOPSIS</span></span>
<span data-ttu-id="ed9bf-103">Obtém uma sessão synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="ed9bf-103">Gets a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="ed9bf-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed9bf-104">SYNTAX</span></span>

### <span data-ttu-id="ed9bf-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ed9bf-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed9bf-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed9bf-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed9bf-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed9bf-107">DESCRIPTION</span></span>
<span data-ttu-id="ed9bf-108">O cmdlet **Get-AzSynapseSparkSession obtém** informações sobre uma sessão do Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="ed9bf-108">The **Get-AzSynapseSparkSession** cmdlet gets information about an Azure Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="ed9bf-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ed9bf-109">EXAMPLES</span></span>

### <span data-ttu-id="ed9bf-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ed9bf-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="ed9bf-111">Esse comando obtém todas as sessões do Spark sob o pool de Spark especificado.</span><span class="sxs-lookup"><span data-stu-id="ed9bf-111">This command gets all the Spark sessions under the specified Spark pool.</span></span>

### <span data-ttu-id="ed9bf-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ed9bf-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 1
```

<span data-ttu-id="ed9bf-113">Esse comando obtém a sessão do Spark com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="ed9bf-113">This command gets the Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="ed9bf-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ed9bf-114">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkSession
```

<span data-ttu-id="ed9bf-115">Esse comando obtém todas as sessões do Spark sob o pool de Spark especificado por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="ed9bf-115">This command gets all the Spark sessions under the specified Spark pool through pipeline.</span></span>

## <span data-ttu-id="ed9bf-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed9bf-116">PARAMETERS</span></span>

### <span data-ttu-id="ed9bf-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ed9bf-117">-ApplicationId</span></span>
<span data-ttu-id="ed9bf-118">O identificador de aplicativo da sessão.</span><span class="sxs-lookup"><span data-stu-id="ed9bf-118">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="ed9bf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed9bf-119">-DefaultProfile</span></span>
<span data-ttu-id="ed9bf-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed9bf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed9bf-121">-Ela</span><span class="sxs-lookup"><span data-stu-id="ed9bf-121">-LivyId</span></span>
<span data-ttu-id="ed9bf-122">Identificador da sessão do Spark.</span><span class="sxs-lookup"><span data-stu-id="ed9bf-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="ed9bf-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed9bf-123">-Name</span></span>
<span data-ttu-id="ed9bf-124">Nome do pool de miniapse.</span><span class="sxs-lookup"><span data-stu-id="ed9bf-124">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="ed9bf-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="ed9bf-125">-SparkPoolName</span></span>
<span data-ttu-id="ed9bf-126">Nome do pool de miniapse.</span><span class="sxs-lookup"><span data-stu-id="ed9bf-126">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="ed9bf-127">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="ed9bf-127">-SparkPoolObject</span></span>
<span data-ttu-id="ed9bf-128">Objeto de entrada de pool de spark, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="ed9bf-128">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ed9bf-129">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="ed9bf-129">-WorkspaceName</span></span>
<span data-ttu-id="ed9bf-130">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="ed9bf-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ed9bf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed9bf-131">CommonParameters</span></span>
<span data-ttu-id="ed9bf-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed9bf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed9bf-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed9bf-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed9bf-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="ed9bf-134">INPUTS</span></span>

### <span data-ttu-id="ed9bf-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="ed9bf-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="ed9bf-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="ed9bf-136">OUTPUTS</span></span>

### <span data-ttu-id="ed9bf-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="ed9bf-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="ed9bf-138">Notas</span><span class="sxs-lookup"><span data-stu-id="ed9bf-138">NOTES</span></span>

## <span data-ttu-id="ed9bf-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed9bf-139">RELATED LINKS</span></span>
