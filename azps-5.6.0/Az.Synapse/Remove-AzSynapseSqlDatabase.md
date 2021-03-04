---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
ms.openlocfilehash: a60bcb20610449b9f76ff3e62684da43a2a792c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886383"
---
# <span data-ttu-id="4ac00-101">Remove-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4ac00-101">Remove-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="4ac00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ac00-102">SYNOPSIS</span></span>
<span data-ttu-id="4ac00-103">Exclui um banco de dados do Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="4ac00-103">Deletes a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="4ac00-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4ac00-104">SYNTAX</span></span>

### <span data-ttu-id="4ac00-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4ac00-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ac00-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ac00-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ac00-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ac00-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ac00-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ac00-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ac00-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4ac00-109">DESCRIPTION</span></span>
<span data-ttu-id="4ac00-110">O cmdlet **Remove-AzSynapseSqlPool** exclui permanentemente um banco de dados do Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="4ac00-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="4ac00-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ac00-111">EXAMPLES</span></span>

### <span data-ttu-id="4ac00-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4ac00-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="4ac00-113">Este comando exclui um banco de dados do Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="4ac00-113">This command deletes an Azure Synapse Analytics SQL database.</span></span>

### <span data-ttu-id="4ac00-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4ac00-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlDatabase -Name ContosoSqlDatabase
```

<span data-ttu-id="4ac00-115">Este comando exclui um banco de dados do Azure Synapse Analytics SQL pipeline.</span><span class="sxs-lookup"><span data-stu-id="4ac00-115">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="4ac00-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4ac00-116">Example 3</span></span>
```powershell
PS C:\> $database = Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
PS C:\> $database | Remove-AzSynapseSqlDatabase
```

<span data-ttu-id="4ac00-117">Este comando exclui um banco de dados do Azure Synapse Analytics SQL pipeline.</span><span class="sxs-lookup"><span data-stu-id="4ac00-117">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="4ac00-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="4ac00-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase
```

<span data-ttu-id="4ac00-119">Este comando exclui um banco de dados do Azure Synapse Analytics SQL com a ID de recurso especificada.</span><span class="sxs-lookup"><span data-stu-id="4ac00-119">This command deletes an Azure Synapse Analytics SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="4ac00-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4ac00-120">PARAMETERS</span></span>

### <span data-ttu-id="4ac00-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ac00-121">-AsJob</span></span>
<span data-ttu-id="4ac00-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4ac00-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ac00-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ac00-123">-DefaultProfile</span></span>
<span data-ttu-id="4ac00-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4ac00-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ac00-125">-Force</span><span class="sxs-lookup"><span data-stu-id="4ac00-125">-Force</span></span>
<span data-ttu-id="4ac00-126">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="4ac00-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4ac00-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ac00-127">-InputObject</span></span>
<span data-ttu-id="4ac00-128">SQL objeto de entrada Banco de Dados, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="4ac00-128">SQL Database input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ac00-129">-Name</span><span class="sxs-lookup"><span data-stu-id="4ac00-129">-Name</span></span>
<span data-ttu-id="4ac00-130">Nome do banco de dados SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="4ac00-130">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ac00-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ac00-131">-PassThru</span></span>
<span data-ttu-id="4ac00-132">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="4ac00-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4ac00-133">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="4ac00-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4ac00-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ac00-134">-ResourceGroupName</span></span>
<span data-ttu-id="4ac00-135">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4ac00-135">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ac00-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ac00-136">-ResourceId</span></span>
<span data-ttu-id="4ac00-137">Identificador de recursos do Banco de Dados SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="4ac00-137">Resource identifier of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ac00-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4ac00-138">-WorkspaceName</span></span>
<span data-ttu-id="4ac00-139">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="4ac00-139">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4ac00-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4ac00-140">-WorkspaceObject</span></span>
<span data-ttu-id="4ac00-141">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="4ac00-141">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ac00-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ac00-142">-Confirm</span></span>
<span data-ttu-id="4ac00-143">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ac00-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ac00-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ac00-144">-WhatIf</span></span>
<span data-ttu-id="4ac00-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4ac00-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ac00-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4ac00-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ac00-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ac00-147">CommonParameters</span></span>
<span data-ttu-id="4ac00-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ac00-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ac00-149">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ac00-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ac00-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ac00-150">INPUTS</span></span>

### <span data-ttu-id="4ac00-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4ac00-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4ac00-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4ac00-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

### <span data-ttu-id="4ac00-153">System.String</span><span class="sxs-lookup"><span data-stu-id="4ac00-153">System.String</span></span>

## <span data-ttu-id="4ac00-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4ac00-154">OUTPUTS</span></span>

### <span data-ttu-id="4ac00-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4ac00-155">System.Boolean</span></span>

## <span data-ttu-id="4ac00-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="4ac00-156">NOTES</span></span>

## <span data-ttu-id="4ac00-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ac00-157">RELATED LINKS</span></span>
