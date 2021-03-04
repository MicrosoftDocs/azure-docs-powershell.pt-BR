---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/stop-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
ms.openlocfilehash: 601ab4b0602a83b708418c626eb48695e18eb7c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890521"
---
# <span data-ttu-id="4dfd7-101">Stop-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="4dfd7-101">Stop-AzSynapseSparkJob</span></span>

## <span data-ttu-id="4dfd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dfd7-102">SYNOPSIS</span></span>
<span data-ttu-id="4dfd7-103">Cancela um trabalho de Spark de Análise de Synapse.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-103">Cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="4dfd7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4dfd7-104">SYNTAX</span></span>

### <span data-ttu-id="4dfd7-105">StopSparkJobByIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4dfd7-105">StopSparkJobByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dfd7-106">StopSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dfd7-106">StopSparkJobByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dfd7-107">StopSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dfd7-107">StopSparkJobByIdFromInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dfd7-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4dfd7-108">DESCRIPTION</span></span>
<span data-ttu-id="4dfd7-109">O cmdlet **Stop-AzSynapseSparkJob** cancela um trabalho de Spark de Análise de Synapse.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-109">The **Stop-AzSynapseSparkJob** cmdlet cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="4dfd7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4dfd7-110">EXAMPLES</span></span>

### <span data-ttu-id="4dfd7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4dfd7-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
```

<span data-ttu-id="4dfd7-112">Este comando cancela um trabalho de Spark de Análise de Synapse.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-112">This command cancels a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="4dfd7-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4dfd7-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkJob -LivyId 130
```

<span data-ttu-id="4dfd7-114">Este comando cancela um trabalho de Spark de Análise de Synapse por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-114">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

### <span data-ttu-id="4dfd7-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4dfd7-115">Example 3</span></span>
```powershell
PS C:\> $job = Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $job | Stop-AzSynapseSparkJob
```

<span data-ttu-id="4dfd7-116">Este comando cancela um trabalho de Spark de Análise de Synapse por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-116">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

## <span data-ttu-id="4dfd7-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4dfd7-117">PARAMETERS</span></span>

### <span data-ttu-id="4dfd7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dfd7-118">-DefaultProfile</span></span>
<span data-ttu-id="4dfd7-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dfd7-120">-Force</span><span class="sxs-lookup"><span data-stu-id="4dfd7-120">-Force</span></span>
<span data-ttu-id="4dfd7-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4dfd7-122">-LivyId</span><span class="sxs-lookup"><span data-stu-id="4dfd7-122">-LivyId</span></span>
<span data-ttu-id="4dfd7-123">Identificador do trabalho spark.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-123">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: StopSparkJobByIdParameterSet, StopSparkJobByIdFromParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: StopSparkJobByIdFromInputObjectParameterSet
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dfd7-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4dfd7-124">-PassThru</span></span>
<span data-ttu-id="4dfd7-125">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="4dfd7-126">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4dfd7-127">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="4dfd7-127">-SparkJobObject</span></span>
<span data-ttu-id="4dfd7-128">Objeto de entrada do trabalho de centelha, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-128">Spark job input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob
Parameter Sets: StopSparkJobByIdFromInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4dfd7-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="4dfd7-129">-SparkPoolName</span></span>
<span data-ttu-id="4dfd7-130">Nome do pool de spark synapse.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dfd7-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="4dfd7-131">-SparkPoolObject</span></span>
<span data-ttu-id="4dfd7-132">Objeto de entrada do pool de centelha, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: StopSparkJobByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4dfd7-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4dfd7-133">-WorkspaceName</span></span>
<span data-ttu-id="4dfd7-134">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dfd7-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4dfd7-135">-Confirm</span></span>
<span data-ttu-id="4dfd7-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dfd7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dfd7-137">-WhatIf</span></span>
<span data-ttu-id="4dfd7-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dfd7-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dfd7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dfd7-140">CommonParameters</span></span>
<span data-ttu-id="4dfd7-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dfd7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dfd7-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4dfd7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dfd7-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4dfd7-143">INPUTS</span></span>

### <span data-ttu-id="4dfd7-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="4dfd7-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="4dfd7-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="4dfd7-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="4dfd7-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4dfd7-146">OUTPUTS</span></span>

### <span data-ttu-id="4dfd7-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4dfd7-147">System.Boolean</span></span>

## <span data-ttu-id="4dfd7-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="4dfd7-148">NOTES</span></span>

## <span data-ttu-id="4dfd7-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4dfd7-149">RELATED LINKS</span></span>
