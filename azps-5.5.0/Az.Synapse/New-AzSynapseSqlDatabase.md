---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
ms.openlocfilehash: b89feae28cee95c63184fd5c0e172a4cb005cac2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112406"
---
# <span data-ttu-id="ae23d-101">New-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ae23d-101">New-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="ae23d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae23d-102">SYNOPSIS</span></span>
<span data-ttu-id="ae23d-103">Cria um banco de dados SQL do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ae23d-103">Creates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="ae23d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae23d-104">SYNTAX</span></span>

### <span data-ttu-id="ae23d-105">CreateByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ae23d-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae23d-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae23d-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlDatabase -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae23d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae23d-107">DESCRIPTION</span></span>
<span data-ttu-id="ae23d-108">O cmdlet **Get-AzSynapseSqlDatabase** obtém informações sobre um banco de dados SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ae23d-108">The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="ae23d-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ae23d-109">EXAMPLES</span></span>

### <span data-ttu-id="ae23d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ae23d-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="ae23d-111">Esse comando cria um banco de dados SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ae23d-111">This command creates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="ae23d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae23d-112">PARAMETERS</span></span>

### <span data-ttu-id="ae23d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae23d-113">-AsJob</span></span>
<span data-ttu-id="ae23d-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ae23d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae23d-115">-Colagem</span><span class="sxs-lookup"><span data-stu-id="ae23d-115">-Collation</span></span>
<span data-ttu-id="ae23d-116">O colamento define as regras que classificação e comparação de dados e não podem ser alteradas após a criação do pool sql.</span><span class="sxs-lookup"><span data-stu-id="ae23d-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="ae23d-117">O colamento padrão é SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="ae23d-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="ae23d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae23d-118">-DefaultProfile</span></span>
<span data-ttu-id="ae23d-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae23d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae23d-120">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="ae23d-120">-MaxSizeInBytes</span></span>
<span data-ttu-id="ae23d-121">Especifica o tamanho máximo do banco de dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="ae23d-121">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="ae23d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae23d-122">-Name</span></span>
<span data-ttu-id="ae23d-123">Nome do Banco de Dados SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="ae23d-123">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="ae23d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae23d-124">-ResourceGroupName</span></span>
<span data-ttu-id="ae23d-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ae23d-125">Resource group name.</span></span>

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

### <span data-ttu-id="ae23d-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="ae23d-126">-Tag</span></span>
<span data-ttu-id="ae23d-127">Uma cadeia de caracteres, dicionário de cadeias de caracteres de marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="ae23d-127">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="ae23d-128">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="ae23d-128">-WorkspaceName</span></span>
<span data-ttu-id="ae23d-129">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="ae23d-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ae23d-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ae23d-130">-WorkspaceObject</span></span>
<span data-ttu-id="ae23d-131">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="ae23d-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ae23d-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ae23d-132">-Confirm</span></span>
<span data-ttu-id="ae23d-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae23d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae23d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae23d-134">-WhatIf</span></span>
<span data-ttu-id="ae23d-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ae23d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae23d-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae23d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae23d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae23d-137">CommonParameters</span></span>
<span data-ttu-id="ae23d-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae23d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae23d-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae23d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae23d-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="ae23d-140">INPUTS</span></span>

### <span data-ttu-id="ae23d-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ae23d-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ae23d-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="ae23d-142">OUTPUTS</span></span>

### <span data-ttu-id="ae23d-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ae23d-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="ae23d-144">Notas</span><span class="sxs-lookup"><span data-stu-id="ae23d-144">NOTES</span></span>

## <span data-ttu-id="ae23d-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae23d-145">RELATED LINKS</span></span>
