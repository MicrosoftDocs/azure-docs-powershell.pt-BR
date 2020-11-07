---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
ms.openlocfilehash: 8f555b18605156aa3394ac02539b7b464feb3ab9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947456"
---
# <span data-ttu-id="e7694-101">Update-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e7694-101">Update-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="e7694-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7694-102">SYNOPSIS</span></span>
<span data-ttu-id="e7694-103">Atualiza um banco de dados do SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="e7694-103">Updates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="e7694-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7694-104">SYNTAX</span></span>

### <span data-ttu-id="e7694-105">UpdateByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e7694-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-MaxSizeInBytes <Int64>] [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7694-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7694-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -Name <String> [-MaxSizeInBytes <Int64>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7694-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7694-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7694-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7694-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -ResourceId <String> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7694-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7694-109">DESCRIPTION</span></span>
<span data-ttu-id="e7694-110">O cmdlet **Update-AzSynapseSqlDatabase** atualiza um banco de dados SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="e7694-110">The **Update-AzSynapseSqlDatabase** cmdlet updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="e7694-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7694-111">EXAMPLES</span></span>

### <span data-ttu-id="e7694-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e7694-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase -Tag @{'key'='value'}
```

<span data-ttu-id="e7694-113">Esse comando atualiza um banco de dados SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="e7694-113">This command updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="e7694-114">OS</span><span class="sxs-lookup"><span data-stu-id="e7694-114">PARAMETERS</span></span>

### <span data-ttu-id="e7694-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7694-115">-AsJob</span></span>
<span data-ttu-id="e7694-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e7694-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e7694-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7694-117">-DefaultProfile</span></span>
<span data-ttu-id="e7694-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7694-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7694-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7694-119">-InputObject</span></span>
<span data-ttu-id="e7694-120">Objeto de entrada de banco de dados SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="e7694-120">SQL Database input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e7694-121">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="e7694-121">-MaxSizeInBytes</span></span>
<span data-ttu-id="e7694-122">Especifica o tamanho máximo do banco de dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="e7694-122">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="e7694-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="e7694-123">-Name</span></span>
<span data-ttu-id="e7694-124">Nome do banco de dados SQL do Synapse.</span><span class="sxs-lookup"><span data-stu-id="e7694-124">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="e7694-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7694-125">-PassThru</span></span>
<span data-ttu-id="e7694-126">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="e7694-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e7694-127">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e7694-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e7694-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7694-128">-ResourceGroupName</span></span>
<span data-ttu-id="e7694-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e7694-129">Resource group name.</span></span>

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

### <span data-ttu-id="e7694-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7694-130">-ResourceId</span></span>
<span data-ttu-id="e7694-131">Identificador de recurso do banco de dados SQL do Synapse.</span><span class="sxs-lookup"><span data-stu-id="e7694-131">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="e7694-132">-Marca</span><span class="sxs-lookup"><span data-stu-id="e7694-132">-Tag</span></span>
<span data-ttu-id="e7694-133">Uma cadeia de caracteres, dicionário de cadeias de caracteres de marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="e7694-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="e7694-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e7694-134">-WorkspaceName</span></span>
<span data-ttu-id="e7694-135">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="e7694-135">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e7694-136">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="e7694-136">-WorkspaceObject</span></span>
<span data-ttu-id="e7694-137">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="e7694-137">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e7694-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e7694-138">-Confirm</span></span>
<span data-ttu-id="e7694-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7694-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7694-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7694-140">-WhatIf</span></span>
<span data-ttu-id="e7694-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e7694-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7694-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e7694-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7694-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7694-143">CommonParameters</span></span>
<span data-ttu-id="e7694-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7694-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7694-145">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7694-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7694-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7694-146">INPUTS</span></span>

### <span data-ttu-id="e7694-147">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e7694-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e7694-148">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e7694-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="e7694-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7694-149">OUTPUTS</span></span>

### <span data-ttu-id="e7694-150">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e7694-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="e7694-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7694-151">NOTES</span></span>

## <span data-ttu-id="e7694-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7694-152">RELATED LINKS</span></span>
