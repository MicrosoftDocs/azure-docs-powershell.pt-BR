---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 63c0dbc30557230f67e419bcde482e445f3df758
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118889"
---
# <span data-ttu-id="7f735-101">Remove-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="7f735-101">Remove-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="7f735-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f735-102">SYNOPSIS</span></span>
<span data-ttu-id="7f735-103">Exclui um ponto de restauração de pool SQL do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="7f735-103">Deletes a Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="7f735-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f735-104">SYNTAX</span></span>

### <span data-ttu-id="7f735-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7f735-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointCreationDate <DateTime> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f735-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f735-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -RestorePointCreationDate <DateTime> -SqlPoolObject <PSSynapseSqlPool>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f735-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f735-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -InputObject <PSRestorePoint> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f735-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f735-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f735-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f735-109">DESCRIPTION</span></span>
<span data-ttu-id="7f735-110">O cmdlet **Remove-AzSynapseSqlPoolRestorePoint** exclui permanentemente um ponto de restauração do pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="7f735-110">The **Remove-AzSynapseSqlPoolRestorePoint** cmdlet permanently deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="7f735-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7f735-111">EXAMPLES</span></span>

### <span data-ttu-id="7f735-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7f735-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="7f735-113">Esse comando exclui um ponto de restauração de pool sql do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="7f735-113">This command deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

### <span data-ttu-id="7f735-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7f735-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPoolRestorePoint -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="7f735-115">Esse comando exclui um ponto de restauração de pool SQL do Azure Synapse Analytics através do pipeline.</span><span class="sxs-lookup"><span data-stu-id="7f735-115">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="7f735-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="7f735-116">Example 3</span></span>
```powershell
PS C:\> $points = Get-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $points[index] | Remove-AzSynapseSqlPoolRestorePoint
```

<span data-ttu-id="7f735-117">Esse comando exclui um ponto de restauração de pool SQL do Azure Synapse Analytics através do pipeline.</span><span class="sxs-lookup"><span data-stu-id="7f735-117">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="7f735-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="7f735-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool/SqlPoolRestorePoints/RestorePointCreationDate
```

<span data-ttu-id="7f735-119">Esse comando exclui um ponto de restauração de pool sql do Azure Synapse Analytics com a ID de recurso especificada.</span><span class="sxs-lookup"><span data-stu-id="7f735-119">This command deletes an Azure Synapse Analytics SQL pool restore point with the specified resource ID.</span></span>

## <span data-ttu-id="7f735-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f735-120">PARAMETERS</span></span>

### <span data-ttu-id="7f735-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f735-121">-AsJob</span></span>
<span data-ttu-id="7f735-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7f735-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7f735-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f735-123">-DefaultProfile</span></span>
<span data-ttu-id="7f735-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7f735-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f735-125">-Forçar</span><span class="sxs-lookup"><span data-stu-id="7f735-125">-Force</span></span>
<span data-ttu-id="7f735-126">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="7f735-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7f735-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f735-127">-InputObject</span></span>
<span data-ttu-id="7f735-128">Objeto de entrada de tempo de criação de ponto de restauração do pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="7f735-128">SQL pool restore point creation time input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f735-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f735-129">-Name</span></span>
<span data-ttu-id="7f735-130">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="7f735-130">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f735-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f735-131">-PassThru</span></span>
<span data-ttu-id="7f735-132">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="7f735-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="7f735-133">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7f735-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7f735-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f735-134">-ResourceGroupName</span></span>
<span data-ttu-id="7f735-135">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7f735-135">Resource group name.</span></span>

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

### <span data-ttu-id="7f735-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f735-136">-ResourceId</span></span>
<span data-ttu-id="7f735-137">Identificador de recursos do Pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="7f735-137">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="7f735-138">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="7f735-138">-RestorePointCreationDate</span></span>
<span data-ttu-id="7f735-139">Nome da Data de Criação do Ponto de Restauração SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="7f735-139">Name of Synapse SQL Restore Point Creation Date .</span></span>

```yaml
Type: System.DateTime
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f735-140">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="7f735-140">-SqlPoolObject</span></span>
<span data-ttu-id="7f735-141">Objeto de entrada do Sql Pool, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="7f735-141">Sql Pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f735-142">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="7f735-142">-WorkspaceName</span></span>
<span data-ttu-id="7f735-143">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="7f735-143">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7f735-144">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7f735-144">-Confirm</span></span>
<span data-ttu-id="7f735-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f735-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f735-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f735-146">-WhatIf</span></span>
<span data-ttu-id="7f735-147">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7f735-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f735-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7f735-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f735-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f735-149">CommonParameters</span></span>
<span data-ttu-id="7f735-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f735-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f735-151">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f735-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f735-152">Entradas</span><span class="sxs-lookup"><span data-stu-id="7f735-152">INPUTS</span></span>

### <span data-ttu-id="7f735-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7f735-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7f735-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7f735-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="7f735-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="7f735-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

### <span data-ttu-id="7f735-156">System.String</span><span class="sxs-lookup"><span data-stu-id="7f735-156">System.String</span></span>

## <span data-ttu-id="7f735-157">Saídas</span><span class="sxs-lookup"><span data-stu-id="7f735-157">OUTPUTS</span></span>

### <span data-ttu-id="7f735-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7f735-158">System.Boolean</span></span>

## <span data-ttu-id="7f735-159">Notas</span><span class="sxs-lookup"><span data-stu-id="7f735-159">NOTES</span></span>

## <span data-ttu-id="7f735-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f735-160">RELATED LINKS</span></span>
