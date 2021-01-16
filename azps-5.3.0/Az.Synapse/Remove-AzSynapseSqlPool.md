---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: 37ece1d86c4b41dbf8a185c0d4ed5d7117db8b2d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272345"
---
# <span data-ttu-id="456c1-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="456c1-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="456c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="456c1-102">SYNOPSIS</span></span>
<span data-ttu-id="456c1-103">Exclui um pool SQL do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="456c1-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="456c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="456c1-104">SYNTAX</span></span>

### <span data-ttu-id="456c1-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="456c1-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="456c1-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="456c1-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="456c1-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="456c1-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="456c1-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="456c1-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="456c1-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="456c1-109">DESCRIPTION</span></span>
<span data-ttu-id="456c1-110">O cmdlet **Remove-AzSynapseSqlPool** exclui permanentemente um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="456c1-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="456c1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="456c1-111">EXAMPLES</span></span>

### <span data-ttu-id="456c1-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="456c1-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="456c1-113">Esse comando exclui um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="456c1-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="456c1-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="456c1-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="456c1-115">Esse comando exclui um pool do SQL do Azure Synapse Analytics por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="456c1-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="456c1-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="456c1-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="456c1-117">Esse comando exclui um pool do SQL do Azure Synapse Analytics por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="456c1-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="456c1-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="456c1-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="456c1-119">Esse comando exclui um pool SQL do Azure Synapse Analytics com a ID do recurso especificada.</span><span class="sxs-lookup"><span data-stu-id="456c1-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="456c1-120">OS</span><span class="sxs-lookup"><span data-stu-id="456c1-120">PARAMETERS</span></span>

### <span data-ttu-id="456c1-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="456c1-121">-AsJob</span></span>
<span data-ttu-id="456c1-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="456c1-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="456c1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="456c1-123">-DefaultProfile</span></span>
<span data-ttu-id="456c1-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="456c1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="456c1-125">-Force</span><span class="sxs-lookup"><span data-stu-id="456c1-125">-Force</span></span>
<span data-ttu-id="456c1-126">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="456c1-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="456c1-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="456c1-127">-InputObject</span></span>
<span data-ttu-id="456c1-128">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="456c1-128">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="456c1-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="456c1-129">-Name</span></span>
<span data-ttu-id="456c1-130">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="456c1-130">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="456c1-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="456c1-131">-PassThru</span></span>
<span data-ttu-id="456c1-132">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="456c1-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="456c1-133">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="456c1-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="456c1-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="456c1-134">-ResourceGroupName</span></span>
<span data-ttu-id="456c1-135">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="456c1-135">Resource group name.</span></span>

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

### <span data-ttu-id="456c1-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="456c1-136">-ResourceId</span></span>
<span data-ttu-id="456c1-137">Identificador de recurso do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="456c1-137">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="456c1-138">-Versão</span><span class="sxs-lookup"><span data-stu-id="456c1-138">-Version</span></span>
<span data-ttu-id="456c1-139">Versão do pool do SQL do Synapse.</span><span class="sxs-lookup"><span data-stu-id="456c1-139">Version of Synapse SQL pool.</span></span> <span data-ttu-id="456c1-140">Por exemplo, 2 ou 3.</span><span class="sxs-lookup"><span data-stu-id="456c1-140">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="456c1-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="456c1-141">-WorkspaceName</span></span>
<span data-ttu-id="456c1-142">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="456c1-142">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="456c1-143">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="456c1-143">-WorkspaceObject</span></span>
<span data-ttu-id="456c1-144">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="456c1-144">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="456c1-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="456c1-145">-Confirm</span></span>
<span data-ttu-id="456c1-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="456c1-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="456c1-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="456c1-147">-WhatIf</span></span>
<span data-ttu-id="456c1-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="456c1-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="456c1-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="456c1-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="456c1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="456c1-150">CommonParameters</span></span>
<span data-ttu-id="456c1-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="456c1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="456c1-152">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="456c1-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="456c1-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="456c1-153">INPUTS</span></span>

### <span data-ttu-id="456c1-154">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="456c1-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="456c1-155">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="456c1-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="456c1-156">System. String</span><span class="sxs-lookup"><span data-stu-id="456c1-156">System.String</span></span>

## <span data-ttu-id="456c1-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="456c1-157">OUTPUTS</span></span>

### <span data-ttu-id="456c1-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="456c1-158">System.Boolean</span></span>

## <span data-ttu-id="456c1-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="456c1-159">NOTES</span></span>

## <span data-ttu-id="456c1-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="456c1-160">RELATED LINKS</span></span>
