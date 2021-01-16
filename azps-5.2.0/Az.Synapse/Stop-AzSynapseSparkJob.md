---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
ms.openlocfilehash: c916b5a7a7d56c241e3cd346c5b7386c0f36ddb1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259230"
---
# <span data-ttu-id="0eeda-101">Stop-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="0eeda-101">Stop-AzSynapseSparkJob</span></span>

## <span data-ttu-id="0eeda-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0eeda-102">SYNOPSIS</span></span>
<span data-ttu-id="0eeda-103">Cancela um trabalho do Spark de análise do Synapse.</span><span class="sxs-lookup"><span data-stu-id="0eeda-103">Cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="0eeda-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0eeda-104">SYNTAX</span></span>

### <span data-ttu-id="0eeda-105">StopSparkJobByIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0eeda-105">StopSparkJobByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eeda-106">StopSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0eeda-106">StopSparkJobByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eeda-107">StopSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0eeda-107">StopSparkJobByIdFromInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eeda-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0eeda-108">DESCRIPTION</span></span>
<span data-ttu-id="0eeda-109">O cmdlet **Stop-AzSynapseSparkJob** cancela um trabalho de análise do Synapse.</span><span class="sxs-lookup"><span data-stu-id="0eeda-109">The **Stop-AzSynapseSparkJob** cmdlet cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="0eeda-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0eeda-110">EXAMPLES</span></span>

### <span data-ttu-id="0eeda-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0eeda-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
```

<span data-ttu-id="0eeda-112">Este comando cancela um trabalho de Synapse analítico da análise.</span><span class="sxs-lookup"><span data-stu-id="0eeda-112">This command cancels a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="0eeda-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0eeda-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkJob -LivyId 130
```

<span data-ttu-id="0eeda-114">Esse comando cancela um trabalho do Spark analítico do Synapse por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="0eeda-114">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

### <span data-ttu-id="0eeda-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0eeda-115">Example 3</span></span>
```powershell
PS C:\> $job = Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $job | Stop-AzSynapseSparkJob
```

<span data-ttu-id="0eeda-116">Esse comando cancela um trabalho do Spark analítico do Synapse por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="0eeda-116">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

## <span data-ttu-id="0eeda-117">OS</span><span class="sxs-lookup"><span data-stu-id="0eeda-117">PARAMETERS</span></span>

### <span data-ttu-id="0eeda-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eeda-118">-DefaultProfile</span></span>
<span data-ttu-id="0eeda-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0eeda-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0eeda-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0eeda-120">-Force</span></span>
<span data-ttu-id="0eeda-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="0eeda-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0eeda-122">-LivyId</span><span class="sxs-lookup"><span data-stu-id="0eeda-122">-LivyId</span></span>
<span data-ttu-id="0eeda-123">Identificador do trabalho Spark.</span><span class="sxs-lookup"><span data-stu-id="0eeda-123">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="0eeda-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0eeda-124">-PassThru</span></span>
<span data-ttu-id="0eeda-125">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="0eeda-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="0eeda-126">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0eeda-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="0eeda-127">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="0eeda-127">-SparkJobObject</span></span>
<span data-ttu-id="0eeda-128">Objeto de entrada de trabalho Spark, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="0eeda-128">Spark job input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0eeda-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="0eeda-129">-SparkPoolName</span></span>
<span data-ttu-id="0eeda-130">Nome do pool do Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="0eeda-130">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="0eeda-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="0eeda-131">-SparkPoolObject</span></span>
<span data-ttu-id="0eeda-132">Objeto de entrada do pool do Spark, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="0eeda-132">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0eeda-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0eeda-133">-WorkspaceName</span></span>
<span data-ttu-id="0eeda-134">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="0eeda-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0eeda-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0eeda-135">-Confirm</span></span>
<span data-ttu-id="0eeda-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eeda-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eeda-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eeda-137">-WhatIf</span></span>
<span data-ttu-id="0eeda-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0eeda-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0eeda-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0eeda-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eeda-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eeda-140">CommonParameters</span></span>
<span data-ttu-id="0eeda-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eeda-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eeda-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0eeda-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eeda-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0eeda-143">INPUTS</span></span>

### <span data-ttu-id="0eeda-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="0eeda-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="0eeda-145">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="0eeda-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="0eeda-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0eeda-146">OUTPUTS</span></span>

### <span data-ttu-id="0eeda-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0eeda-147">System.Boolean</span></span>

## <span data-ttu-id="0eeda-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0eeda-148">NOTES</span></span>

## <span data-ttu-id="0eeda-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0eeda-149">RELATED LINKS</span></span>
