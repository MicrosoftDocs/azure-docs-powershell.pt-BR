---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: bb653669ff15dad78ce3cec10f406aa099808e55
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112405"
---
# <span data-ttu-id="1270e-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1270e-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="1270e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1270e-102">SYNOPSIS</span></span>
<span data-ttu-id="1270e-103">Cria um pool SQL do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1270e-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="1270e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1270e-104">SYNTAX</span></span>

### <span data-ttu-id="1270e-105">CreateByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1270e-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1270e-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1270e-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1270e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1270e-107">DESCRIPTION</span></span>
<span data-ttu-id="1270e-108">O cmdlet **New-AzSynapseSqlPool** cria um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1270e-108">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="1270e-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1270e-109">EXAMPLES</span></span>

### <span data-ttu-id="1270e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1270e-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="1270e-111">Esse comando cria um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1270e-111">This command creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="1270e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1270e-112">PARAMETERS</span></span>

### <span data-ttu-id="1270e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1270e-113">-AsJob</span></span>
<span data-ttu-id="1270e-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1270e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1270e-115">-Colagem</span><span class="sxs-lookup"><span data-stu-id="1270e-115">-Collation</span></span>
<span data-ttu-id="1270e-116">O colamento define as regras que classificação e comparação de dados e não podem ser alteradas após a criação do pool sql.</span><span class="sxs-lookup"><span data-stu-id="1270e-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="1270e-117">O colamento padrão é SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="1270e-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="1270e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1270e-118">-DefaultProfile</span></span>
<span data-ttu-id="1270e-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1270e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1270e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="1270e-120">-Name</span></span>
<span data-ttu-id="1270e-121">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="1270e-121">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1270e-122">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="1270e-122">-PerformanceLevel</span></span>
<span data-ttu-id="1270e-123">O nível de desempenho e o nível de desempenho do SQL Service a ser atribuído ao pool SQL.</span><span class="sxs-lookup"><span data-stu-id="1270e-123">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="1270e-124">Por exemplo, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="1270e-124">For example, DW2000c.</span></span>

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

### <span data-ttu-id="1270e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1270e-125">-ResourceGroupName</span></span>
<span data-ttu-id="1270e-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1270e-126">Resource group name.</span></span>

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

### <span data-ttu-id="1270e-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="1270e-127">-Tag</span></span>
<span data-ttu-id="1270e-128">Uma cadeia de caracteres, dicionário de cadeias de caracteres de marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="1270e-128">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="1270e-129">-Versão</span><span class="sxs-lookup"><span data-stu-id="1270e-129">-Version</span></span>
<span data-ttu-id="1270e-130">Versão do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="1270e-130">Version of Synapse SQL pool.</span></span> <span data-ttu-id="1270e-131">Por exemplo, 2 ou 3.</span><span class="sxs-lookup"><span data-stu-id="1270e-131">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="1270e-132">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="1270e-132">-WorkspaceName</span></span>
<span data-ttu-id="1270e-133">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="1270e-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1270e-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1270e-134">-WorkspaceObject</span></span>
<span data-ttu-id="1270e-135">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="1270e-135">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1270e-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1270e-136">-Confirm</span></span>
<span data-ttu-id="1270e-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1270e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1270e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1270e-138">-WhatIf</span></span>
<span data-ttu-id="1270e-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1270e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1270e-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1270e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1270e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1270e-141">CommonParameters</span></span>
<span data-ttu-id="1270e-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1270e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1270e-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1270e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1270e-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="1270e-144">INPUTS</span></span>

### <span data-ttu-id="1270e-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1270e-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="1270e-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="1270e-146">OUTPUTS</span></span>

### <span data-ttu-id="1270e-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1270e-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="1270e-148">Notas</span><span class="sxs-lookup"><span data-stu-id="1270e-148">NOTES</span></span>

## <span data-ttu-id="1270e-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1270e-149">RELATED LINKS</span></span>
