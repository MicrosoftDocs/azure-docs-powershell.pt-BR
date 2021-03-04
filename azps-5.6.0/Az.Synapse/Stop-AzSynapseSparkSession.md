---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/stop-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
ms.openlocfilehash: 204166bc48e01ea186ca18ad5aa95b0dcf05192a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890518"
---
# <span data-ttu-id="e964c-101">Stop-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="e964c-101">Stop-AzSynapseSparkSession</span></span>

## <span data-ttu-id="e964c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e964c-102">SYNOPSIS</span></span>
<span data-ttu-id="e964c-103">Interrompe uma sessão do Spark de Análise de Sinapse.</span><span class="sxs-lookup"><span data-stu-id="e964c-103">Stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="e964c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e964c-104">SYNTAX</span></span>

### <span data-ttu-id="e964c-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e964c-105">DeleteByNameParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e964c-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e964c-106">DeleteByParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e964c-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e964c-107">DeleteByInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e964c-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e964c-108">DESCRIPTION</span></span>
<span data-ttu-id="e964c-109">O cmdlet **Stop-AzSynapseSparkSession** interrompe uma sessão synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="e964c-109">The **Stop-AzSynapseSparkSession** cmdlet stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="e964c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e964c-110">EXAMPLES</span></span>

### <span data-ttu-id="e964c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e964c-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="e964c-112">Este comando interrompe uma sessão de Spark de Análise de Synapse.</span><span class="sxs-lookup"><span data-stu-id="e964c-112">This command stops a Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="e964c-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e964c-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkSession -LivyId 324
```

<span data-ttu-id="e964c-114">Este comando interrompe uma sessão de Spark de Análise de Synapse por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="e964c-114">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

### <span data-ttu-id="e964c-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e964c-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
PS C:\> $session | Stop-AzSynapseSparkSession
```

<span data-ttu-id="e964c-116">Este comando interrompe uma sessão de Spark de Análise de Synapse por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="e964c-116">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="e964c-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e964c-117">PARAMETERS</span></span>

### <span data-ttu-id="e964c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e964c-118">-AsJob</span></span>
<span data-ttu-id="e964c-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e964c-119">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e964c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e964c-120">-DefaultProfile</span></span>
<span data-ttu-id="e964c-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e964c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e964c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e964c-122">-InputObject</span></span>
<span data-ttu-id="e964c-123">Objeto de entrada de sessão spark, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="e964c-123">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e964c-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="e964c-124">-LivyId</span></span>
<span data-ttu-id="e964c-125">Identificador da sessão Spark.</span><span class="sxs-lookup"><span data-stu-id="e964c-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e964c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e964c-126">-PassThru</span></span>
<span data-ttu-id="e964c-127">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="e964c-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="e964c-128">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="e964c-128">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e964c-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="e964c-129">-SparkPoolName</span></span>
<span data-ttu-id="e964c-130">Nome do pool de spark synapse.</span><span class="sxs-lookup"><span data-stu-id="e964c-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e964c-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="e964c-131">-SparkPoolObject</span></span>
<span data-ttu-id="e964c-132">Objeto de entrada do pool de centelha, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="e964c-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e964c-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e964c-133">-WorkspaceName</span></span>
<span data-ttu-id="e964c-134">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="e964c-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e964c-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e964c-135">-Confirm</span></span>
<span data-ttu-id="e964c-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e964c-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e964c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e964c-137">-WhatIf</span></span>
<span data-ttu-id="e964c-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e964c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e964c-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e964c-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e964c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e964c-140">CommonParameters</span></span>
<span data-ttu-id="e964c-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e964c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e964c-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e964c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e964c-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e964c-143">INPUTS</span></span>

### <span data-ttu-id="e964c-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="e964c-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="e964c-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="e964c-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="e964c-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e964c-146">OUTPUTS</span></span>

### <span data-ttu-id="e964c-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e964c-147">System.Boolean</span></span>

## <span data-ttu-id="e964c-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="e964c-148">NOTES</span></span>

## <span data-ttu-id="e964c-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e964c-149">RELATED LINKS</span></span>
