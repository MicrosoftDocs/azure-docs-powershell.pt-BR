---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
ms.openlocfilehash: 73664b619670f17a92bd915f6e4d8501a8ac9f6d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888393"
---
# <span data-ttu-id="67d06-101">New-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="67d06-101">New-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="67d06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67d06-102">SYNOPSIS</span></span>
<span data-ttu-id="67d06-103">Cria um banco de dados do Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="67d06-103">Creates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="67d06-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="67d06-104">SYNTAX</span></span>

### <span data-ttu-id="67d06-105">CreateByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="67d06-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67d06-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67d06-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlDatabase -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67d06-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="67d06-107">DESCRIPTION</span></span>
<span data-ttu-id="67d06-108">O cmdlet **Get-AzSynapseSqlDatabase** obtém informações sobre um banco de dados do Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="67d06-108">The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="67d06-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67d06-109">EXAMPLES</span></span>

### <span data-ttu-id="67d06-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="67d06-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="67d06-111">Este comando cria um banco de dados do Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="67d06-111">This command creates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="67d06-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="67d06-112">PARAMETERS</span></span>

### <span data-ttu-id="67d06-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67d06-113">-AsJob</span></span>
<span data-ttu-id="67d06-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="67d06-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67d06-115">-Collation</span><span class="sxs-lookup"><span data-stu-id="67d06-115">-Collation</span></span>
<span data-ttu-id="67d06-116">O collation define as regras que classificar e comparar dados e não pode ser alterado após a criação SQL pool.</span><span class="sxs-lookup"><span data-stu-id="67d06-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="67d06-117">O collation padrão é SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="67d06-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="67d06-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67d06-118">-DefaultProfile</span></span>
<span data-ttu-id="67d06-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="67d06-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67d06-120">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="67d06-120">-MaxSizeInBytes</span></span>
<span data-ttu-id="67d06-121">Especifica o tamanho máximo do banco de dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="67d06-121">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d06-122">-Name</span><span class="sxs-lookup"><span data-stu-id="67d06-122">-Name</span></span>
<span data-ttu-id="67d06-123">Nome do banco de dados SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="67d06-123">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d06-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67d06-124">-ResourceGroupName</span></span>
<span data-ttu-id="67d06-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="67d06-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d06-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="67d06-126">-Tag</span></span>
<span data-ttu-id="67d06-127">Uma cadeia de caracteres, um dicionário de cadeias de caracteres de marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="67d06-127">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="67d06-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="67d06-128">-WorkspaceName</span></span>
<span data-ttu-id="67d06-129">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="67d06-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d06-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="67d06-130">-WorkspaceObject</span></span>
<span data-ttu-id="67d06-131">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="67d06-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67d06-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67d06-132">-Confirm</span></span>
<span data-ttu-id="67d06-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67d06-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67d06-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67d06-134">-WhatIf</span></span>
<span data-ttu-id="67d06-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="67d06-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67d06-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="67d06-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67d06-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67d06-137">CommonParameters</span></span>
<span data-ttu-id="67d06-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67d06-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67d06-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67d06-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67d06-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67d06-140">INPUTS</span></span>

### <span data-ttu-id="67d06-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="67d06-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="67d06-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="67d06-142">OUTPUTS</span></span>

### <span data-ttu-id="67d06-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="67d06-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="67d06-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="67d06-144">NOTES</span></span>

## <span data-ttu-id="67d06-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67d06-145">RELATED LINKS</span></span>
