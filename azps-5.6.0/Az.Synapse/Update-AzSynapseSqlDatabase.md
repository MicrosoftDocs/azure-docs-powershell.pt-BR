---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
ms.openlocfilehash: a939ef485976a746e705de10a4706b03c63f910e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890506"
---
# <span data-ttu-id="de444-101">Update-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="de444-101">Update-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="de444-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de444-102">SYNOPSIS</span></span>
<span data-ttu-id="de444-103">Atualiza um banco de dados do Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="de444-103">Updates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="de444-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="de444-104">SYNTAX</span></span>

### <span data-ttu-id="de444-105">UpdateByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="de444-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-MaxSizeInBytes <Int64>] [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de444-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de444-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -Name <String> [-MaxSizeInBytes <Int64>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de444-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de444-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de444-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de444-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -ResourceId <String> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de444-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="de444-109">DESCRIPTION</span></span>
<span data-ttu-id="de444-110">O cmdlet **Update-AzSynapseSqlDatabase** atualiza um banco de dados do Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="de444-110">The **Update-AzSynapseSqlDatabase** cmdlet updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="de444-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de444-111">EXAMPLES</span></span>

### <span data-ttu-id="de444-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="de444-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase -Tag @{'key'='value'}
```

<span data-ttu-id="de444-113">Este comando atualiza um banco de dados do Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="de444-113">This command updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="de444-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="de444-114">PARAMETERS</span></span>

### <span data-ttu-id="de444-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de444-115">-AsJob</span></span>
<span data-ttu-id="de444-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="de444-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="de444-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de444-117">-DefaultProfile</span></span>
<span data-ttu-id="de444-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de444-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de444-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de444-119">-InputObject</span></span>
<span data-ttu-id="de444-120">SQL objeto de entrada Banco de Dados, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="de444-120">SQL Database input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de444-121">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="de444-121">-MaxSizeInBytes</span></span>
<span data-ttu-id="de444-122">Especifica o tamanho máximo do banco de dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="de444-122">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de444-123">-Name</span><span class="sxs-lookup"><span data-stu-id="de444-123">-Name</span></span>
<span data-ttu-id="de444-124">Nome do banco de dados SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="de444-124">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de444-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de444-125">-PassThru</span></span>
<span data-ttu-id="de444-126">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="de444-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="de444-127">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="de444-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="de444-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de444-128">-ResourceGroupName</span></span>
<span data-ttu-id="de444-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="de444-129">Resource group name.</span></span>

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

### <span data-ttu-id="de444-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de444-130">-ResourceId</span></span>
<span data-ttu-id="de444-131">Identificador de recursos do Banco de Dados SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="de444-131">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="de444-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="de444-132">-Tag</span></span>
<span data-ttu-id="de444-133">Uma cadeia de caracteres, um dicionário de cadeias de caracteres de marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="de444-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="de444-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="de444-134">-WorkspaceName</span></span>
<span data-ttu-id="de444-135">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="de444-135">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="de444-136">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="de444-136">-WorkspaceObject</span></span>
<span data-ttu-id="de444-137">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="de444-137">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="de444-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de444-138">-Confirm</span></span>
<span data-ttu-id="de444-139">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de444-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de444-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de444-140">-WhatIf</span></span>
<span data-ttu-id="de444-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="de444-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de444-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="de444-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de444-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de444-143">CommonParameters</span></span>
<span data-ttu-id="de444-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de444-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de444-145">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de444-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de444-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="de444-146">INPUTS</span></span>

### <span data-ttu-id="de444-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="de444-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="de444-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="de444-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="de444-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="de444-149">OUTPUTS</span></span>

### <span data-ttu-id="de444-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="de444-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="de444-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="de444-151">NOTES</span></span>

## <span data-ttu-id="de444-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de444-152">RELATED LINKS</span></span>
