---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
ms.openlocfilehash: 4951fbe707dbae8c1fdff34e828e468a2d3168bf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258906"
---
# <span data-ttu-id="000dd-101">Remove-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="000dd-101">Remove-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="000dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="000dd-102">SYNOPSIS</span></span>
<span data-ttu-id="000dd-103">Exclui um banco de dados SQL do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="000dd-103">Deletes a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="000dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="000dd-104">SYNTAX</span></span>

### <span data-ttu-id="000dd-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="000dd-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="000dd-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="000dd-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="000dd-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="000dd-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="000dd-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="000dd-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="000dd-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="000dd-109">DESCRIPTION</span></span>
<span data-ttu-id="000dd-110">O cmdlet **Remove-AzSynapseSqlPool** exclui permanentemente um banco de dados SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="000dd-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="000dd-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="000dd-111">EXAMPLES</span></span>

### <span data-ttu-id="000dd-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="000dd-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="000dd-113">Esse comando exclui um banco de dados SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="000dd-113">This command deletes an Azure Synapse Analytics SQL database.</span></span>

### <span data-ttu-id="000dd-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="000dd-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlDatabase -Name ContosoSqlDatabase
```

<span data-ttu-id="000dd-115">Esse comando exclui um banco de dados SQL do Azure Synapse Analytics por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="000dd-115">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="000dd-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="000dd-116">Example 3</span></span>
```powershell
PS C:\> $database = Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
PS C:\> $database | Remove-AzSynapseSqlDatabase
```

<span data-ttu-id="000dd-117">Esse comando exclui um banco de dados SQL do Azure Synapse Analytics por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="000dd-117">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="000dd-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="000dd-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase
```

<span data-ttu-id="000dd-119">Esse comando exclui um banco de dados SQL do Azure Synapse Analytics com a ID do recurso especificada.</span><span class="sxs-lookup"><span data-stu-id="000dd-119">This command deletes an Azure Synapse Analytics SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="000dd-120">OS</span><span class="sxs-lookup"><span data-stu-id="000dd-120">PARAMETERS</span></span>

### <span data-ttu-id="000dd-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="000dd-121">-AsJob</span></span>
<span data-ttu-id="000dd-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="000dd-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="000dd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="000dd-123">-DefaultProfile</span></span>
<span data-ttu-id="000dd-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="000dd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="000dd-125">-Force</span><span class="sxs-lookup"><span data-stu-id="000dd-125">-Force</span></span>
<span data-ttu-id="000dd-126">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="000dd-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="000dd-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="000dd-127">-InputObject</span></span>
<span data-ttu-id="000dd-128">Objeto de entrada de banco de dados SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="000dd-128">SQL Database input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="000dd-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="000dd-129">-Name</span></span>
<span data-ttu-id="000dd-130">Nome do banco de dados SQL do Synapse.</span><span class="sxs-lookup"><span data-stu-id="000dd-130">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="000dd-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="000dd-131">-PassThru</span></span>
<span data-ttu-id="000dd-132">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="000dd-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="000dd-133">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="000dd-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="000dd-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="000dd-134">-ResourceGroupName</span></span>
<span data-ttu-id="000dd-135">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="000dd-135">Resource group name.</span></span>

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

### <span data-ttu-id="000dd-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="000dd-136">-ResourceId</span></span>
<span data-ttu-id="000dd-137">Identificador de recurso do banco de dados SQL do Synapse.</span><span class="sxs-lookup"><span data-stu-id="000dd-137">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="000dd-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="000dd-138">-WorkspaceName</span></span>
<span data-ttu-id="000dd-139">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="000dd-139">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="000dd-140">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="000dd-140">-WorkspaceObject</span></span>
<span data-ttu-id="000dd-141">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="000dd-141">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="000dd-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="000dd-142">-Confirm</span></span>
<span data-ttu-id="000dd-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="000dd-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="000dd-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="000dd-144">-WhatIf</span></span>
<span data-ttu-id="000dd-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="000dd-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="000dd-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="000dd-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="000dd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="000dd-147">CommonParameters</span></span>
<span data-ttu-id="000dd-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="000dd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="000dd-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="000dd-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="000dd-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="000dd-150">INPUTS</span></span>

### <span data-ttu-id="000dd-151">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="000dd-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="000dd-152">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="000dd-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

### <span data-ttu-id="000dd-153">System. String</span><span class="sxs-lookup"><span data-stu-id="000dd-153">System.String</span></span>

## <span data-ttu-id="000dd-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="000dd-154">OUTPUTS</span></span>

### <span data-ttu-id="000dd-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="000dd-155">System.Boolean</span></span>

## <span data-ttu-id="000dd-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="000dd-156">NOTES</span></span>

## <span data-ttu-id="000dd-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="000dd-157">RELATED LINKS</span></span>
