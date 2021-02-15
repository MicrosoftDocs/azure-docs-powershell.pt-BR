---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: 37ece1d86c4b41dbf8a185c0d4ed5d7117db8b2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116303"
---
# <span data-ttu-id="4cfbe-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="4cfbe-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="4cfbe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4cfbe-102">SYNOPSIS</span></span>
<span data-ttu-id="4cfbe-103">Exclui um pool SQL do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="4cfbe-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4cfbe-104">SYNTAX</span></span>

### <span data-ttu-id="4cfbe-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4cfbe-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4cfbe-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cfbe-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cfbe-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cfbe-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cfbe-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cfbe-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cfbe-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4cfbe-109">DESCRIPTION</span></span>
<span data-ttu-id="4cfbe-110">O cmdlet **Remove-AzSynapseSqlPool** exclui permanentemente um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="4cfbe-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4cfbe-111">EXAMPLES</span></span>

### <span data-ttu-id="4cfbe-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4cfbe-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="4cfbe-113">Esse comando exclui um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="4cfbe-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4cfbe-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="4cfbe-115">Esse comando exclui um pool SQL do Azure Synapse Analytics por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="4cfbe-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4cfbe-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="4cfbe-117">Esse comando exclui um pool SQL do Azure Synapse Analytics por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="4cfbe-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="4cfbe-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="4cfbe-119">Esse comando exclui um pool SQL do Azure Synapse Analytics com a ID de recurso especificada.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="4cfbe-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4cfbe-120">PARAMETERS</span></span>

### <span data-ttu-id="4cfbe-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4cfbe-121">-AsJob</span></span>
<span data-ttu-id="4cfbe-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4cfbe-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4cfbe-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cfbe-123">-DefaultProfile</span></span>
<span data-ttu-id="4cfbe-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cfbe-125">-Forçar</span><span class="sxs-lookup"><span data-stu-id="4cfbe-125">-Force</span></span>
<span data-ttu-id="4cfbe-126">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4cfbe-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cfbe-127">-InputObject</span></span>
<span data-ttu-id="4cfbe-128">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-128">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4cfbe-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="4cfbe-129">-Name</span></span>
<span data-ttu-id="4cfbe-130">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-130">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="4cfbe-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4cfbe-131">-PassThru</span></span>
<span data-ttu-id="4cfbe-132">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="4cfbe-133">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4cfbe-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cfbe-134">-ResourceGroupName</span></span>
<span data-ttu-id="4cfbe-135">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-135">Resource group name.</span></span>

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

### <span data-ttu-id="4cfbe-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cfbe-136">-ResourceId</span></span>
<span data-ttu-id="4cfbe-137">Identificador de recursos do Pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-137">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="4cfbe-138">-Versão</span><span class="sxs-lookup"><span data-stu-id="4cfbe-138">-Version</span></span>
<span data-ttu-id="4cfbe-139">Versão do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-139">Version of Synapse SQL pool.</span></span> <span data-ttu-id="4cfbe-140">Por exemplo, 2 ou 3.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-140">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="4cfbe-141">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="4cfbe-141">-WorkspaceName</span></span>
<span data-ttu-id="4cfbe-142">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-142">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4cfbe-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4cfbe-143">-WorkspaceObject</span></span>
<span data-ttu-id="4cfbe-144">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-144">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4cfbe-145">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4cfbe-145">-Confirm</span></span>
<span data-ttu-id="4cfbe-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cfbe-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cfbe-147">-WhatIf</span></span>
<span data-ttu-id="4cfbe-148">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cfbe-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cfbe-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cfbe-150">CommonParameters</span></span>
<span data-ttu-id="4cfbe-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cfbe-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cfbe-152">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4cfbe-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cfbe-153">Entradas</span><span class="sxs-lookup"><span data-stu-id="4cfbe-153">INPUTS</span></span>

### <span data-ttu-id="4cfbe-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4cfbe-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4cfbe-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="4cfbe-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="4cfbe-156">System.String</span><span class="sxs-lookup"><span data-stu-id="4cfbe-156">System.String</span></span>

## <span data-ttu-id="4cfbe-157">Saídas</span><span class="sxs-lookup"><span data-stu-id="4cfbe-157">OUTPUTS</span></span>

### <span data-ttu-id="4cfbe-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4cfbe-158">System.Boolean</span></span>

## <span data-ttu-id="4cfbe-159">Notas</span><span class="sxs-lookup"><span data-stu-id="4cfbe-159">NOTES</span></span>

## <span data-ttu-id="4cfbe-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4cfbe-160">RELATED LINKS</span></span>
