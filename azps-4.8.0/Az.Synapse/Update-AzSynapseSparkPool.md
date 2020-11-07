---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
ms.openlocfilehash: 1ed539f6064d6f99aff632a43cee5f200d735b6d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947457"
---
# <span data-ttu-id="78403-101">Update-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="78403-101">Update-AzSynapseSparkPool</span></span>

## <span data-ttu-id="78403-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78403-102">SYNOPSIS</span></span>
<span data-ttu-id="78403-103">Atualiza um pool Spark do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="78403-103">Updates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="78403-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78403-104">SYNTAX</span></span>

### <span data-ttu-id="78403-105">SetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="78403-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>]
 [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>]
 [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78403-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78403-106">SetByParentObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>]
 [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>]
 [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78403-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78403-107">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78403-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78403-108">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseSparkPool -ResourceId <String> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78403-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="78403-109">DESCRIPTION</span></span>
<span data-ttu-id="78403-110">O cmdlet **Update-AzSynapseSparkPool** atualiza um pool Spark do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="78403-110">The **Update-AzSynapseSparkPool** cmdlet updates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="78403-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78403-111">EXAMPLES</span></span>

### <span data-ttu-id="78403-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="78403-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -Tag @{"key" = "value"} -NodeCount 5 -NodeSize Medium
```

<span data-ttu-id="78403-113">Esse comando atualiza um pool do Spark da análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="78403-113">This command updates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="78403-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="78403-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
$pool | Update-AzSynapseSparkPool -Tag @{"key" = "value1"}
```

<span data-ttu-id="78403-115">Esse comando atualiza um pool do Spark do Azure Synapse Analytics pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="78403-115">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="78403-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="78403-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSparkPool -Name ContosoSparkPool -Tag @{"key" = "value2"}
```

<span data-ttu-id="78403-117">Esse comando atualiza um pool do Spark do Azure Synapse Analytics pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="78403-117">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="78403-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="78403-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool -Tag @{"key" = "value3"}
```

<span data-ttu-id="78403-119">Esse comando atualiza um pool Spark do Azure Synapse Analytics com ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="78403-119">This command updates an Azure Synapse Analytics Spark pool with resource ID.</span></span>

### <span data-ttu-id="78403-120">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="78403-120">Example 5</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $true -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 7
```

<span data-ttu-id="78403-121">Esse comando habilita a escala automática para um pool Spark do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="78403-121">This command enables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="78403-122">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="78403-122">Example 6</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $false
```

<span data-ttu-id="78403-123">Esse comando desabilita a escala automática de um pool Spark do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="78403-123">This command disables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="78403-124">Exemplo 7</span><span class="sxs-lookup"><span data-stu-id="78403-124">Example 7</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $true -AutoPauseDelayInMinute 15
```

<span data-ttu-id="78403-125">Esse comando habilita a pausa automática para um pool Spark do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="78403-125">This command enables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="78403-126">Exemplo 8</span><span class="sxs-lookup"><span data-stu-id="78403-126">Example 8</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $false
```

<span data-ttu-id="78403-127">Esse comando desabilita a pausa automática para um pool Spark do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="78403-127">This command disables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="78403-128">OS</span><span class="sxs-lookup"><span data-stu-id="78403-128">PARAMETERS</span></span>

### <span data-ttu-id="78403-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78403-129">-AsJob</span></span>
<span data-ttu-id="78403-130">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="78403-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78403-131">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="78403-131">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="78403-132">Número de minutos ociosos.</span><span class="sxs-lookup"><span data-stu-id="78403-132">Number of minutes idle.</span></span> <span data-ttu-id="78403-133">Esse parâmetro deve ser especificado quando a pausa automática está habilitada.</span><span class="sxs-lookup"><span data-stu-id="78403-133">This parameter must be specified when Auto-pause is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78403-134">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="78403-134">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="78403-135">Número máximo de nós a serem alocados no pool do Spark especificado.</span><span class="sxs-lookup"><span data-stu-id="78403-135">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="78403-136">Esse parâmetro deve ser especificado quando a dimensionamento automático está habilitada.</span><span class="sxs-lookup"><span data-stu-id="78403-136">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78403-137">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="78403-137">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="78403-138">Número mínimo de nós a serem alocados no pool do Spark especificado.</span><span class="sxs-lookup"><span data-stu-id="78403-138">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="78403-139">Esse parâmetro deve ser especificado quando a dimensionamento automático está habilitada.</span><span class="sxs-lookup"><span data-stu-id="78403-139">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78403-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78403-140">-DefaultProfile</span></span>
<span data-ttu-id="78403-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="78403-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78403-142">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="78403-142">-EnableAutoPause</span></span>
<span data-ttu-id="78403-143">Indica se a pausa automática deve ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="78403-143">Indicates whether Auto-pause should be enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78403-144">-EnableAutoScale</span><span class="sxs-lookup"><span data-stu-id="78403-144">-EnableAutoScale</span></span>
<span data-ttu-id="78403-145">Indica se a dimensionamento automático deve ser habilitada</span><span class="sxs-lookup"><span data-stu-id="78403-145">Indicates whether Auto-scale should be enabled</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78403-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78403-146">-InputObject</span></span>
<span data-ttu-id="78403-147">Objeto de entrada do pool do Spark, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="78403-147">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78403-148">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="78403-148">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="78403-149">Arquivo de configuração de ambiente (saída de "PIP Freeze").</span><span class="sxs-lookup"><span data-stu-id="78403-149">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="78403-150">-Nome</span><span class="sxs-lookup"><span data-stu-id="78403-150">-Name</span></span>
<span data-ttu-id="78403-151">Nome do pool do Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="78403-151">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78403-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="78403-152">-NodeCount</span></span>
<span data-ttu-id="78403-153">Número de nós a serem alocados no pool do Spark especificado.</span><span class="sxs-lookup"><span data-stu-id="78403-153">Number of nodes to be allocated in the specified Spark pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78403-154">-Nós</span><span class="sxs-lookup"><span data-stu-id="78403-154">-NodeSize</span></span>
<span data-ttu-id="78403-155">Número de núcleo e memória a serem usados para nós atribuídos no pool do Spark especificado.</span><span class="sxs-lookup"><span data-stu-id="78403-155">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="78403-156">Esse parâmetro deve ser especificado quando a dimensionamento automático está desabilitada</span><span class="sxs-lookup"><span data-stu-id="78403-156">This parameter must be specified when Auto-scale is disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78403-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78403-157">-ResourceGroupName</span></span>
<span data-ttu-id="78403-158">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="78403-158">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78403-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78403-159">-ResourceId</span></span>
<span data-ttu-id="78403-160">Identificador de recurso do pool do Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="78403-160">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78403-161">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="78403-161">-SparkVersion</span></span>
<span data-ttu-id="78403-162">Versão do Apache Spark.</span><span class="sxs-lookup"><span data-stu-id="78403-162">Apache Spark version.</span></span>
<span data-ttu-id="78403-163">Valores permitidos: 2,4</span><span class="sxs-lookup"><span data-stu-id="78403-163">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="78403-164">-Marca</span><span class="sxs-lookup"><span data-stu-id="78403-164">-Tag</span></span>
<span data-ttu-id="78403-165">Uma cadeia de caracteres, dicionário de cadeias de caracteres de marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="78403-165">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78403-166">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="78403-166">-WorkspaceName</span></span>
<span data-ttu-id="78403-167">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="78403-167">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78403-168">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="78403-168">-WorkspaceObject</span></span>
<span data-ttu-id="78403-169">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="78403-169">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78403-170">-Confirme</span><span class="sxs-lookup"><span data-stu-id="78403-170">-Confirm</span></span>
<span data-ttu-id="78403-171">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78403-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78403-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78403-172">-WhatIf</span></span>
<span data-ttu-id="78403-173">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="78403-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78403-174">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="78403-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78403-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78403-175">CommonParameters</span></span>
<span data-ttu-id="78403-176">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78403-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78403-177">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78403-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78403-178">SENSORES</span><span class="sxs-lookup"><span data-stu-id="78403-178">INPUTS</span></span>

### <span data-ttu-id="78403-179">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="78403-179">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="78403-180">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="78403-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="78403-181">EXIBE</span><span class="sxs-lookup"><span data-stu-id="78403-181">OUTPUTS</span></span>

### <span data-ttu-id="78403-182">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="78403-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="78403-183">INFORMA</span><span class="sxs-lookup"><span data-stu-id="78403-183">NOTES</span></span>

## <span data-ttu-id="78403-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78403-184">RELATED LINKS</span></span>
