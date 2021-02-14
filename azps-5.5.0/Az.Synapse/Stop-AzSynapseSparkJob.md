---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
ms.openlocfilehash: c916b5a7a7d56c241e3cd346c5b7386c0f36ddb1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115602"
---
# <span data-ttu-id="2fc57-101">Stop-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="2fc57-101">Stop-AzSynapseSparkJob</span></span>

## <span data-ttu-id="2fc57-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2fc57-102">SYNOPSIS</span></span>
<span data-ttu-id="2fc57-103">Cancela um trabalho do Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="2fc57-103">Cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="2fc57-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2fc57-104">SYNTAX</span></span>

### <span data-ttu-id="2fc57-105">StopSparkJobByIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2fc57-105">StopSparkJobByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fc57-106">StopSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fc57-106">StopSparkJobByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fc57-107">StopSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fc57-107">StopSparkJobByIdFromInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fc57-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="2fc57-108">DESCRIPTION</span></span>
<span data-ttu-id="2fc57-109">O cmdlet **Stop-AzSynapseSparkJob** cancela um trabalho do Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="2fc57-109">The **Stop-AzSynapseSparkJob** cmdlet cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="2fc57-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2fc57-110">EXAMPLES</span></span>

### <span data-ttu-id="2fc57-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2fc57-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
```

<span data-ttu-id="2fc57-112">Este comando cancela um trabalho do Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="2fc57-112">This command cancels a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="2fc57-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2fc57-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkJob -LivyId 130
```

<span data-ttu-id="2fc57-114">Esse comando cancela um trabalho do Synapse Analytics Spark por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="2fc57-114">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

### <span data-ttu-id="2fc57-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="2fc57-115">Example 3</span></span>
```powershell
PS C:\> $job = Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $job | Stop-AzSynapseSparkJob
```

<span data-ttu-id="2fc57-116">Esse comando cancela um trabalho do Synapse Analytics Spark por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="2fc57-116">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

## <span data-ttu-id="2fc57-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2fc57-117">PARAMETERS</span></span>

### <span data-ttu-id="2fc57-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fc57-118">-DefaultProfile</span></span>
<span data-ttu-id="2fc57-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2fc57-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fc57-120">-Forçar</span><span class="sxs-lookup"><span data-stu-id="2fc57-120">-Force</span></span>
<span data-ttu-id="2fc57-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="2fc57-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2fc57-122">-Ela</span><span class="sxs-lookup"><span data-stu-id="2fc57-122">-LivyId</span></span>
<span data-ttu-id="2fc57-123">Identificador do trabalho do Spark.</span><span class="sxs-lookup"><span data-stu-id="2fc57-123">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="2fc57-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2fc57-124">-PassThru</span></span>
<span data-ttu-id="2fc57-125">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="2fc57-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="2fc57-126">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2fc57-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="2fc57-127">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="2fc57-127">-SparkJobObject</span></span>
<span data-ttu-id="2fc57-128">Spark job input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="2fc57-128">Spark job input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2fc57-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="2fc57-129">-SparkPoolName</span></span>
<span data-ttu-id="2fc57-130">Nome do pool de miniapse.</span><span class="sxs-lookup"><span data-stu-id="2fc57-130">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="2fc57-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="2fc57-131">-SparkPoolObject</span></span>
<span data-ttu-id="2fc57-132">Objeto de entrada de pool de spark, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="2fc57-132">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2fc57-133">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="2fc57-133">-WorkspaceName</span></span>
<span data-ttu-id="2fc57-134">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="2fc57-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2fc57-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2fc57-135">-Confirm</span></span>
<span data-ttu-id="2fc57-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fc57-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fc57-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fc57-137">-WhatIf</span></span>
<span data-ttu-id="2fc57-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2fc57-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fc57-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2fc57-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fc57-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fc57-140">CommonParameters</span></span>
<span data-ttu-id="2fc57-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fc57-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fc57-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2fc57-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fc57-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="2fc57-143">INPUTS</span></span>

### <span data-ttu-id="2fc57-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="2fc57-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="2fc57-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="2fc57-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="2fc57-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="2fc57-146">OUTPUTS</span></span>

### <span data-ttu-id="2fc57-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2fc57-147">System.Boolean</span></span>

## <span data-ttu-id="2fc57-148">Notas</span><span class="sxs-lookup"><span data-stu-id="2fc57-148">NOTES</span></span>

## <span data-ttu-id="2fc57-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2fc57-149">RELATED LINKS</span></span>
