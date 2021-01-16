---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: 25f9c829bd0f2557f4419bcc0c3b95c71a2e4b9b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271269"
---
# <span data-ttu-id="dfdce-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="dfdce-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="dfdce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dfdce-102">SYNOPSIS</span></span>
<span data-ttu-id="dfdce-103">Atualiza um pool do SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="dfdce-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="dfdce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dfdce-104">SYNTAX</span></span>

### <span data-ttu-id="dfdce-105">UpdateByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="dfdce-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfdce-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfdce-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfdce-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfdce-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfdce-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfdce-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfdce-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dfdce-109">DESCRIPTION</span></span>
<span data-ttu-id="dfdce-110">O cmdlet **Update-AzSynapseSqlPool** atualiza um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="dfdce-110">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="dfdce-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dfdce-111">EXAMPLES</span></span>

### <span data-ttu-id="dfdce-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dfdce-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="dfdce-113">Esse comando atualiza um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="dfdce-113">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="dfdce-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="dfdce-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="dfdce-115">Esse comando atualiza um pool do SQL do Azure Synapse Analytics por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="dfdce-115">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="dfdce-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="dfdce-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="dfdce-117">Esse comando atualiza um pool do SQL do Azure Synapse Analytics por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="dfdce-117">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="dfdce-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="dfdce-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="dfdce-119">Esse comando atualiza um pool SQL do Azure Synapse Analytics com ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="dfdce-119">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="dfdce-120">OS</span><span class="sxs-lookup"><span data-stu-id="dfdce-120">PARAMETERS</span></span>

### <span data-ttu-id="dfdce-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dfdce-121">-AsJob</span></span>
<span data-ttu-id="dfdce-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="dfdce-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dfdce-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfdce-123">-DefaultProfile</span></span>
<span data-ttu-id="dfdce-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dfdce-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfdce-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfdce-125">-InputObject</span></span>
<span data-ttu-id="dfdce-126">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="dfdce-126">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfdce-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="dfdce-127">-Name</span></span>
<span data-ttu-id="dfdce-128">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="dfdce-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfdce-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dfdce-129">-PassThru</span></span>
<span data-ttu-id="dfdce-130">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="dfdce-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="dfdce-131">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="dfdce-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="dfdce-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="dfdce-132">-PerformanceLevel</span></span>
<span data-ttu-id="dfdce-133">A camada de serviço SQL e o nível de desempenho a serem atribuídos ao pool SQL.</span><span class="sxs-lookup"><span data-stu-id="dfdce-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="dfdce-134">Por exemplo, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="dfdce-134">For example, DW2000c.</span></span>

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

### <span data-ttu-id="dfdce-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfdce-135">-ResourceGroupName</span></span>
<span data-ttu-id="dfdce-136">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dfdce-136">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfdce-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dfdce-137">-ResourceId</span></span>
<span data-ttu-id="dfdce-138">Identificador de recurso do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="dfdce-138">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfdce-139">-Marca</span><span class="sxs-lookup"><span data-stu-id="dfdce-139">-Tag</span></span>
<span data-ttu-id="dfdce-140">Uma cadeia de caracteres, dicionário de cadeias de caracteres de marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="dfdce-140">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="dfdce-141">-Versão</span><span class="sxs-lookup"><span data-stu-id="dfdce-141">-Version</span></span>
<span data-ttu-id="dfdce-142">Versão do pool do SQL do Synapse.</span><span class="sxs-lookup"><span data-stu-id="dfdce-142">Version of Synapse SQL pool.</span></span> <span data-ttu-id="dfdce-143">Por exemplo, 2 ou 3.</span><span class="sxs-lookup"><span data-stu-id="dfdce-143">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="dfdce-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dfdce-144">-WorkspaceName</span></span>
<span data-ttu-id="dfdce-145">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="dfdce-145">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfdce-146">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="dfdce-146">-WorkspaceObject</span></span>
<span data-ttu-id="dfdce-147">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="dfdce-147">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfdce-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dfdce-148">-Confirm</span></span>
<span data-ttu-id="dfdce-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfdce-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfdce-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfdce-150">-WhatIf</span></span>
<span data-ttu-id="dfdce-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dfdce-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfdce-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dfdce-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfdce-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfdce-153">CommonParameters</span></span>
<span data-ttu-id="dfdce-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfdce-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfdce-155">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfdce-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfdce-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dfdce-156">INPUTS</span></span>

### <span data-ttu-id="dfdce-157">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="dfdce-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="dfdce-158">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="dfdce-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="dfdce-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dfdce-159">OUTPUTS</span></span>

### <span data-ttu-id="dfdce-160">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="dfdce-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="dfdce-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dfdce-161">NOTES</span></span>

## <span data-ttu-id="dfdce-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dfdce-162">RELATED LINKS</span></span>
