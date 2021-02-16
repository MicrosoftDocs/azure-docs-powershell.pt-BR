---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: 25f9c829bd0f2557f4419bcc0c3b95c71a2e4b9b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118526"
---
# <span data-ttu-id="4c81d-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="4c81d-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="4c81d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c81d-102">SYNOPSIS</span></span>
<span data-ttu-id="4c81d-103">Atualiza um pool SQL do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="4c81d-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="4c81d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c81d-104">SYNTAX</span></span>

### <span data-ttu-id="4c81d-105">UpdateByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4c81d-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c81d-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c81d-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c81d-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c81d-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c81d-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c81d-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c81d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c81d-109">DESCRIPTION</span></span>
<span data-ttu-id="4c81d-110">O cmdlet **Update-AzSynapseSqlPool** atualiza um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="4c81d-110">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="4c81d-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4c81d-111">EXAMPLES</span></span>

### <span data-ttu-id="4c81d-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4c81d-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="4c81d-113">Este comando atualiza um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="4c81d-113">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="4c81d-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4c81d-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="4c81d-115">Este comando atualiza um pool SQL do Azure Synapse Analytics por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="4c81d-115">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="4c81d-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4c81d-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="4c81d-117">Este comando atualiza um pool SQL do Azure Synapse Analytics por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="4c81d-117">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="4c81d-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="4c81d-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="4c81d-119">Este comando atualiza um pool SQL do Azure Synapse Analytics com ID de recurso.</span><span class="sxs-lookup"><span data-stu-id="4c81d-119">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="4c81d-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c81d-120">PARAMETERS</span></span>

### <span data-ttu-id="4c81d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c81d-121">-AsJob</span></span>
<span data-ttu-id="4c81d-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4c81d-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c81d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c81d-123">-DefaultProfile</span></span>
<span data-ttu-id="4c81d-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4c81d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c81d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c81d-125">-InputObject</span></span>
<span data-ttu-id="4c81d-126">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="4c81d-126">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4c81d-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c81d-127">-Name</span></span>
<span data-ttu-id="4c81d-128">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="4c81d-128">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="4c81d-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c81d-129">-PassThru</span></span>
<span data-ttu-id="4c81d-130">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="4c81d-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="4c81d-131">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4c81d-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4c81d-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="4c81d-132">-PerformanceLevel</span></span>
<span data-ttu-id="4c81d-133">O nível de desempenho e o nível de desempenho do SQL Service a ser atribuído ao pool SQL.</span><span class="sxs-lookup"><span data-stu-id="4c81d-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="4c81d-134">Por exemplo, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="4c81d-134">For example, DW2000c.</span></span>

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

### <span data-ttu-id="4c81d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c81d-135">-ResourceGroupName</span></span>
<span data-ttu-id="4c81d-136">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4c81d-136">Resource group name.</span></span>

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

### <span data-ttu-id="4c81d-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c81d-137">-ResourceId</span></span>
<span data-ttu-id="4c81d-138">Identificador de recursos do Pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="4c81d-138">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="4c81d-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="4c81d-139">-Tag</span></span>
<span data-ttu-id="4c81d-140">Uma cadeia de caracteres, dicionário de cadeias de caracteres de marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="4c81d-140">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="4c81d-141">-Versão</span><span class="sxs-lookup"><span data-stu-id="4c81d-141">-Version</span></span>
<span data-ttu-id="4c81d-142">Versão do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="4c81d-142">Version of Synapse SQL pool.</span></span> <span data-ttu-id="4c81d-143">Por exemplo, 2 ou 3.</span><span class="sxs-lookup"><span data-stu-id="4c81d-143">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="4c81d-144">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="4c81d-144">-WorkspaceName</span></span>
<span data-ttu-id="4c81d-145">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="4c81d-145">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4c81d-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4c81d-146">-WorkspaceObject</span></span>
<span data-ttu-id="4c81d-147">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="4c81d-147">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4c81d-148">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4c81d-148">-Confirm</span></span>
<span data-ttu-id="4c81d-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c81d-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c81d-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c81d-150">-WhatIf</span></span>
<span data-ttu-id="4c81d-151">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4c81d-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c81d-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4c81d-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c81d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c81d-153">CommonParameters</span></span>
<span data-ttu-id="4c81d-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c81d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c81d-155">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c81d-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c81d-156">Entradas</span><span class="sxs-lookup"><span data-stu-id="4c81d-156">INPUTS</span></span>

### <span data-ttu-id="4c81d-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4c81d-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4c81d-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="4c81d-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="4c81d-159">Saídas</span><span class="sxs-lookup"><span data-stu-id="4c81d-159">OUTPUTS</span></span>

### <span data-ttu-id="4c81d-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="4c81d-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="4c81d-161">Notas</span><span class="sxs-lookup"><span data-stu-id="4c81d-161">NOTES</span></span>

## <span data-ttu-id="4c81d-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c81d-162">RELATED LINKS</span></span>
