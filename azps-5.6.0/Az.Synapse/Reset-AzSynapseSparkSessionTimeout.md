---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesparksessiontimeout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
ms.openlocfilehash: 485558c47fa8b879999777b79341fc855085b81a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888100"
---
# <span data-ttu-id="95e00-101">Reset-AzSynapseSparkSessionTimeout</span><span class="sxs-lookup"><span data-stu-id="95e00-101">Reset-AzSynapseSparkSessionTimeout</span></span>

## <span data-ttu-id="95e00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95e00-102">SYNOPSIS</span></span>
<span data-ttu-id="95e00-103">Redefine o tempo-de-tempo de uma sessão de Spark de Análise de Synapse.</span><span class="sxs-lookup"><span data-stu-id="95e00-103">Resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="95e00-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="95e00-104">SYNTAX</span></span>

### <span data-ttu-id="95e00-105">ResetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="95e00-105">ResetByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSparkSessionTimeout -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95e00-106">ResetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95e00-106">ResetByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95e00-107">ResetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95e00-107">ResetByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95e00-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="95e00-108">DESCRIPTION</span></span>
<span data-ttu-id="95e00-109">O cmdlet **Remove-AzSynapseSparkSessionTimeout** redefine o tempo de uma sessão de Spark de Análise de Synapse.</span><span class="sxs-lookup"><span data-stu-id="95e00-109">The **Remove-AzSynapseSparkSessionTimeout** cmdlet resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="95e00-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95e00-110">EXAMPLES</span></span>

### <span data-ttu-id="95e00-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="95e00-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSparkSessionTimeout -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
```

<span data-ttu-id="95e00-112">Este comando redefine o tempo de tempo da sessão Synapse Analytics Spark com a ID de violência especificada.</span><span class="sxs-lookup"><span data-stu-id="95e00-112">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="95e00-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="95e00-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Reset-AzSynapseSparkSessionTimeout -LivyId 125
```

<span data-ttu-id="95e00-114">Este comando redefine o tempo de tempo da sessão Synapse Analytics Spark com a ID de violência especificada através do pipeline.</span><span class="sxs-lookup"><span data-stu-id="95e00-114">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

### <span data-ttu-id="95e00-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="95e00-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
PS C:\> $session | Reset-AzSynapseSparkSessionTimeout
```

<span data-ttu-id="95e00-116">Este comando redefine o tempo de tempo da sessão Synapse Analytics Spark com a ID de violência especificada através do pipeline.</span><span class="sxs-lookup"><span data-stu-id="95e00-116">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="95e00-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="95e00-117">PARAMETERS</span></span>

### <span data-ttu-id="95e00-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95e00-118">-AsJob</span></span>
<span data-ttu-id="95e00-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="95e00-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="95e00-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95e00-120">-DefaultProfile</span></span>
<span data-ttu-id="95e00-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="95e00-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95e00-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95e00-122">-InputObject</span></span>
<span data-ttu-id="95e00-123">Objeto de entrada de sessão spark, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="95e00-123">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: ResetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95e00-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="95e00-124">-LivyId</span></span>
<span data-ttu-id="95e00-125">Identificador da sessão Spark.</span><span class="sxs-lookup"><span data-stu-id="95e00-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResetByNameParameterSet, ResetByParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95e00-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95e00-126">-PassThru</span></span>
<span data-ttu-id="95e00-127">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="95e00-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="95e00-128">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="95e00-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="95e00-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="95e00-129">-SparkPoolName</span></span>
<span data-ttu-id="95e00-130">Nome do pool de spark synapse.</span><span class="sxs-lookup"><span data-stu-id="95e00-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95e00-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="95e00-131">-SparkPoolObject</span></span>
<span data-ttu-id="95e00-132">Objeto de entrada do pool de centelha, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="95e00-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: ResetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95e00-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="95e00-133">-WorkspaceName</span></span>
<span data-ttu-id="95e00-134">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="95e00-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ResetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95e00-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95e00-135">-Confirm</span></span>
<span data-ttu-id="95e00-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95e00-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95e00-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95e00-137">-WhatIf</span></span>
<span data-ttu-id="95e00-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="95e00-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95e00-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="95e00-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95e00-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95e00-140">CommonParameters</span></span>
<span data-ttu-id="95e00-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95e00-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95e00-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95e00-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95e00-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95e00-143">INPUTS</span></span>

### <span data-ttu-id="95e00-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="95e00-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="95e00-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="95e00-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="95e00-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="95e00-146">OUTPUTS</span></span>

### <span data-ttu-id="95e00-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="95e00-147">System.Boolean</span></span>

## <span data-ttu-id="95e00-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="95e00-148">NOTES</span></span>

## <span data-ttu-id="95e00-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95e00-149">RELATED LINKS</span></span>
