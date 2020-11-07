---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
ms.openlocfilehash: 2525792f7696c69a03a926850eaea20267d14fbf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93956071"
---
# <span data-ttu-id="58914-101">Remove-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="58914-101">Remove-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="58914-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58914-102">SYNOPSIS</span></span>
<span data-ttu-id="58914-103">Exclui um banco de dados SQL do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="58914-103">Deletes a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="58914-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58914-104">SYNTAX</span></span>

### <span data-ttu-id="58914-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="58914-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58914-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58914-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58914-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58914-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58914-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58914-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58914-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58914-109">DESCRIPTION</span></span>
<span data-ttu-id="58914-110">O cmdlet **Remove-AzSynapseSqlPool** exclui permanentemente um banco de dados SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="58914-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL database.</span></span>


## <span data-ttu-id="58914-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58914-111">EXAMPLES</span></span>

### <span data-ttu-id="58914-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="58914-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="58914-113">Esse comando exclui um banco de dados SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="58914-113">This command deletes an Azure Synapse Analytics SQL database.</span></span>

### <span data-ttu-id="58914-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="58914-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlDatabase -Name ContosoSqlDatabase
```

<span data-ttu-id="58914-115">Esse comando exclui um banco de dados SQL do Azure Synapse Analytics por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="58914-115">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="58914-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="58914-116">Example 3</span></span>
```powershell
PS C:\> $database = Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
PS C:\> $database | Remove-AzSynapseSqlDatabase
```

<span data-ttu-id="58914-117">Esse comando exclui um banco de dados SQL do Azure Synapse Analytics por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="58914-117">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="58914-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="58914-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase
```

<span data-ttu-id="58914-119">Esse comando exclui um banco de dados SQL do Azure Synapse Analytics com a ID do recurso especificada.</span><span class="sxs-lookup"><span data-stu-id="58914-119">This command deletes an Azure Synapse Analytics SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="58914-120">OS</span><span class="sxs-lookup"><span data-stu-id="58914-120">PARAMETERS</span></span>

### <span data-ttu-id="58914-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58914-121">-AsJob</span></span>
<span data-ttu-id="58914-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="58914-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58914-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58914-123">-DefaultProfile</span></span>
<span data-ttu-id="58914-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58914-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58914-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58914-125">-InputObject</span></span>
<span data-ttu-id="58914-126">Objeto de entrada de banco de dados SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="58914-126">SQL Database input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="58914-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="58914-127">-Name</span></span>
<span data-ttu-id="58914-128">Nome do banco de dados SQL do Synapse.</span><span class="sxs-lookup"><span data-stu-id="58914-128">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="58914-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58914-129">-PassThru</span></span>
<span data-ttu-id="58914-130">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="58914-130">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="58914-131">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="58914-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="58914-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58914-132">-ResourceGroupName</span></span>
<span data-ttu-id="58914-133">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="58914-133">Resource group name.</span></span>

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

### <span data-ttu-id="58914-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58914-134">-ResourceId</span></span>
<span data-ttu-id="58914-135">Identificador de recurso do banco de dados SQL do Synapse.</span><span class="sxs-lookup"><span data-stu-id="58914-135">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="58914-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="58914-136">-WorkspaceName</span></span>
<span data-ttu-id="58914-137">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="58914-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="58914-138">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="58914-138">-WorkspaceObject</span></span>
<span data-ttu-id="58914-139">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="58914-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="58914-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="58914-140">-Confirm</span></span>
<span data-ttu-id="58914-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58914-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58914-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58914-142">-WhatIf</span></span>
<span data-ttu-id="58914-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="58914-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58914-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="58914-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58914-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58914-145">CommonParameters</span></span>
<span data-ttu-id="58914-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58914-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58914-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58914-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58914-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58914-148">INPUTS</span></span>

### <span data-ttu-id="58914-149">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="58914-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="58914-150">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="58914-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

### <span data-ttu-id="58914-151">System. String</span><span class="sxs-lookup"><span data-stu-id="58914-151">System.String</span></span>

## <span data-ttu-id="58914-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58914-152">OUTPUTS</span></span>

### <span data-ttu-id="58914-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="58914-153">System.Boolean</span></span>

## <span data-ttu-id="58914-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58914-154">NOTES</span></span>

## <span data-ttu-id="58914-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58914-155">RELATED LINKS</span></span>
