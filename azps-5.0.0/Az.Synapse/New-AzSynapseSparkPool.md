---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
ms.openlocfilehash: c931bff1ba95ee1be185b5fe4dfdc2256d2cafec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116316"
---
# <span data-ttu-id="9d9c6-101">New-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="9d9c6-101">New-AzSynapseSparkPool</span></span>

## <span data-ttu-id="9d9c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d9c6-102">SYNOPSIS</span></span>
<span data-ttu-id="9d9c6-103">Cria um pool Spark do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-103">Creates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="9d9c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d9c6-104">SYNTAX</span></span>

### <span data-ttu-id="9d9c6-105">CreateByNameAndEnableAutoScaleParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9d9c6-105">CreateByNameAndEnableAutoScaleParameterSet (Default)</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d9c6-106">CreateByNameAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d9c6-106">CreateByNameAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d9c6-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d9c6-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d9c6-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d9c6-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d9c6-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9d9c6-109">DESCRIPTION</span></span>
<span data-ttu-id="9d9c6-110">O cmdlet **New-AzSynapseSparkPool** cria um pool Spark do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-110">The **New-AzSynapseSparkPool** cmdlet creates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="9d9c6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d9c6-111">EXAMPLES</span></span>

### <span data-ttu-id="9d9c6-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9d9c6-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="9d9c6-113">Esse comando cria um pool Spark do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-113">This command creates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="9d9c6-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9d9c6-114">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="9d9c6-115">Esse comando cria um pool do Spark do Azure Synapse Analytics com escala automática habilitada.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-115">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled.</span></span>

### <span data-ttu-id="9d9c6-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="9d9c6-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="9d9c6-117">Esse comando cria um pool do Spark do Azure Synapse Analytics por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-117">This command creates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="9d9c6-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="9d9c6-118">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="9d9c6-119">Esse comando cria um pool Spark do Azure Synapse Analytics com escala automática habilitada por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-119">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled through pipeline.</span></span>

## <span data-ttu-id="9d9c6-120">OS</span><span class="sxs-lookup"><span data-stu-id="9d9c6-120">PARAMETERS</span></span>

### <span data-ttu-id="9d9c6-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d9c6-121">-AsJob</span></span>
<span data-ttu-id="9d9c6-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9d9c6-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9d9c6-123">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="9d9c6-123">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="9d9c6-124">Número de minutos ociosos.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-124">Number of minutes idle.</span></span> <span data-ttu-id="9d9c6-125">Esse parâmetro deve ser especificado quando a pausa automática está habilitada.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-125">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="9d9c6-126">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="9d9c6-126">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="9d9c6-127">Número máximo de nós a serem alocados no pool do Spark especificado.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-127">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="9d9c6-128">Esse parâmetro deve ser especificado quando a dimensionamento automático está habilitada.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-128">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByParentObjectAndEnableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9c6-129">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="9d9c6-129">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="9d9c6-130">Número mínimo de nós a serem alocados no pool do Spark especificado.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-130">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="9d9c6-131">Esse parâmetro deve ser especificado quando a dimensionamento automático está habilitada.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-131">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByParentObjectAndEnableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9c6-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d9c6-132">-DefaultProfile</span></span>
<span data-ttu-id="9d9c6-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d9c6-134">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="9d9c6-134">-EnableAutoPause</span></span>
<span data-ttu-id="9d9c6-135">Indica se a pausa automática deve ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-135">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="9d9c6-136">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="9d9c6-136">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="9d9c6-137">Arquivo de configuração de ambiente (saída de "PIP Freeze").</span><span class="sxs-lookup"><span data-stu-id="9d9c6-137">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="9d9c6-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d9c6-138">-Name</span></span>
<span data-ttu-id="9d9c6-139">Nome do pool do Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-139">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9c6-140">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="9d9c6-140">-NodeCount</span></span>
<span data-ttu-id="9d9c6-141">Número de nós a serem alocados no pool do Spark especificado.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-141">Number of nodes to be allocated in the specified Spark pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndDisableAutoScaleParameterSet, CreateByParentObjectAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9c6-142">-Nós</span><span class="sxs-lookup"><span data-stu-id="9d9c6-142">-NodeSize</span></span>
<span data-ttu-id="9d9c6-143">Número de núcleo e memória a serem usados para nós atribuídos no pool do Spark especificado.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-143">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="9d9c6-144">Esse parâmetro deve ser especificado quando a dimensionamento automático está desabilitada</span><span class="sxs-lookup"><span data-stu-id="9d9c6-144">This parameter must be specified when Auto-scale is disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9c6-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d9c6-145">-ResourceGroupName</span></span>
<span data-ttu-id="9d9c6-146">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-146">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByNameAndDisableAutoScaleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9c6-147">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="9d9c6-147">-SparkVersion</span></span>
<span data-ttu-id="9d9c6-148">Versão do Apache Spark.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-148">Apache Spark version.</span></span>
<span data-ttu-id="9d9c6-149">Valores permitidos: 2,4</span><span class="sxs-lookup"><span data-stu-id="9d9c6-149">Allowed values: 2.4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9c6-150">-Marca</span><span class="sxs-lookup"><span data-stu-id="9d9c6-150">-Tag</span></span>
<span data-ttu-id="9d9c6-151">Uma cadeia de caracteres, dicionário de cadeias de caracteres de marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-151">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="9d9c6-152">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9d9c6-152">-WorkspaceName</span></span>
<span data-ttu-id="9d9c6-153">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-153">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByNameAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9c6-154">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="9d9c6-154">-WorkspaceObject</span></span>
<span data-ttu-id="9d9c6-155">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-155">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectAndEnableAutoScaleParameterSet, CreateByParentObjectAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d9c6-156">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9d9c6-156">-Confirm</span></span>
<span data-ttu-id="9d9c6-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d9c6-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d9c6-158">-WhatIf</span></span>
<span data-ttu-id="9d9c6-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d9c6-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d9c6-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d9c6-161">CommonParameters</span></span>
<span data-ttu-id="9d9c6-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d9c6-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d9c6-163">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d9c6-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d9c6-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9d9c6-164">INPUTS</span></span>

### <span data-ttu-id="9d9c6-165">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9d9c6-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="9d9c6-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9d9c6-166">OUTPUTS</span></span>

### <span data-ttu-id="9d9c6-167">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="9d9c6-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="9d9c6-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9d9c6-168">NOTES</span></span>

## <span data-ttu-id="9d9c6-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d9c6-169">RELATED LINKS</span></span>
