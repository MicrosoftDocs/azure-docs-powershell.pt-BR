---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 997132e201864653307af3d072920d36b19d5af3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125236"
---
# <span data-ttu-id="5c76b-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5c76b-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="5c76b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5c76b-102">SYNOPSIS</span></span>
<span data-ttu-id="5c76b-103">Cria um pool do SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5c76b-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="5c76b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c76b-104">SYNTAX</span></span>

### <span data-ttu-id="5c76b-105">CreateByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5c76b-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c76b-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c76b-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c76b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5c76b-107">DESCRIPTION</span></span>
<span data-ttu-id="5c76b-108">O cmdlet **New-AzSynapseSqlPool** cria um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5c76b-108">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="5c76b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5c76b-109">EXAMPLES</span></span>

### <span data-ttu-id="5c76b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5c76b-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="5c76b-111">Esse comando cria um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5c76b-111">This command creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="5c76b-112">OS</span><span class="sxs-lookup"><span data-stu-id="5c76b-112">PARAMETERS</span></span>

### <span data-ttu-id="5c76b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c76b-113">-AsJob</span></span>
<span data-ttu-id="5c76b-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5c76b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c76b-115">-Agrupamento</span><span class="sxs-lookup"><span data-stu-id="5c76b-115">-Collation</span></span>
<span data-ttu-id="5c76b-116">O agrupamento define as regras que classificam e comparam dados, e não podem ser alterados após a criação do pool do SQL.</span><span class="sxs-lookup"><span data-stu-id="5c76b-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="5c76b-117">O agrupamento padrão é SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="5c76b-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="5c76b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c76b-118">-DefaultProfile</span></span>
<span data-ttu-id="5c76b-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5c76b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c76b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="5c76b-120">-Name</span></span>
<span data-ttu-id="5c76b-121">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="5c76b-121">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="5c76b-122">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="5c76b-122">-PerformanceLevel</span></span>
<span data-ttu-id="5c76b-123">A camada de serviço SQL e o nível de desempenho a serem atribuídos ao pool SQL.</span><span class="sxs-lookup"><span data-stu-id="5c76b-123">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="5c76b-124">Por exemplo, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="5c76b-124">For example, DW2000c.</span></span>

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

### <span data-ttu-id="5c76b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c76b-125">-ResourceGroupName</span></span>
<span data-ttu-id="5c76b-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5c76b-126">Resource group name.</span></span>

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

### <span data-ttu-id="5c76b-127">-Marca</span><span class="sxs-lookup"><span data-stu-id="5c76b-127">-Tag</span></span>
<span data-ttu-id="5c76b-128">Uma cadeia de caracteres, dicionário de cadeias de caracteres de marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="5c76b-128">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="5c76b-129">-Versão</span><span class="sxs-lookup"><span data-stu-id="5c76b-129">-Version</span></span>
<span data-ttu-id="5c76b-130">Versão do pool do SQL do Synapse.</span><span class="sxs-lookup"><span data-stu-id="5c76b-130">Version of Synapse SQL pool.</span></span> <span data-ttu-id="5c76b-131">Por exemplo, 2 ou 3.</span><span class="sxs-lookup"><span data-stu-id="5c76b-131">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="5c76b-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5c76b-132">-WorkspaceName</span></span>
<span data-ttu-id="5c76b-133">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="5c76b-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5c76b-134">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="5c76b-134">-WorkspaceObject</span></span>
<span data-ttu-id="5c76b-135">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="5c76b-135">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5c76b-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5c76b-136">-Confirm</span></span>
<span data-ttu-id="5c76b-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c76b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c76b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c76b-138">-WhatIf</span></span>
<span data-ttu-id="5c76b-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5c76b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c76b-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5c76b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c76b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c76b-141">CommonParameters</span></span>
<span data-ttu-id="5c76b-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c76b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c76b-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c76b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c76b-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5c76b-144">INPUTS</span></span>

### <span data-ttu-id="5c76b-145">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5c76b-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5c76b-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5c76b-146">OUTPUTS</span></span>

### <span data-ttu-id="5c76b-147">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5c76b-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="5c76b-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5c76b-148">NOTES</span></span>

## <span data-ttu-id="5c76b-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c76b-149">RELATED LINKS</span></span>
