---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 574c41fe8b0f3266a6fff80c020b60c9832cb431
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262127"
---
# <span data-ttu-id="8125a-101">New-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="8125a-101">New-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="8125a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8125a-102">SYNOPSIS</span></span>
<span data-ttu-id="8125a-103">Cria um novo ponto de restauração em um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="8125a-103">Creates a new restore point in an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="8125a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8125a-104">SYNTAX</span></span>

### <span data-ttu-id="8125a-105">CreateByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8125a-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8125a-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8125a-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8125a-107">CreateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8125a-107">CreateByInputObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8125a-108">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8125a-108">CreateByResourceIdParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -ResourceId <String> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8125a-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8125a-109">DESCRIPTION</span></span>
<span data-ttu-id="8125a-110">O cmdlet **New-AzSynapseSqlPoolRestorePoint** cria um novo ponto de restauração no qual um pool SQL do Azure Synapse Analytics pode ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="8125a-110">The **New-AzSynapseSqlPoolRestorePoint** cmdlet creates a new restore point that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="8125a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8125a-111">EXAMPLES</span></span>

### <span data-ttu-id="8125a-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8125a-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -RestorePointLabel ContosoRestorePoint
```

<span data-ttu-id="8125a-113">Esse comando cria um ponto de restauração do pool do SQL chamado ContosoSqlPool na ContosoWorkspace do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8125a-113">This command creates a restore point for SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="8125a-114">OS</span><span class="sxs-lookup"><span data-stu-id="8125a-114">PARAMETERS</span></span>

### <span data-ttu-id="8125a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8125a-115">-AsJob</span></span>
<span data-ttu-id="8125a-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8125a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8125a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8125a-117">-DefaultProfile</span></span>
<span data-ttu-id="8125a-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8125a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8125a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8125a-119">-InputObject</span></span>
<span data-ttu-id="8125a-120">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="8125a-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8125a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8125a-121">-Name</span></span>
<span data-ttu-id="8125a-122">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="8125a-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8125a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8125a-123">-ResourceGroupName</span></span>
<span data-ttu-id="8125a-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8125a-124">Resource group name.</span></span>

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

### <span data-ttu-id="8125a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8125a-125">-ResourceId</span></span>
<span data-ttu-id="8125a-126">Identificador de recurso do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="8125a-126">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8125a-127">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="8125a-127">-RestorePointLabel</span></span>
<span data-ttu-id="8125a-128">O rótulo ao qual associamos um ponto de restauração pode não ser exclusivo.</span><span class="sxs-lookup"><span data-stu-id="8125a-128">The label we associate a restore point with, may not be unique.</span></span>

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

### <span data-ttu-id="8125a-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8125a-129">-WorkspaceName</span></span>
<span data-ttu-id="8125a-130">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="8125a-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8125a-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="8125a-131">-WorkspaceObject</span></span>
<span data-ttu-id="8125a-132">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="8125a-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8125a-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8125a-133">-Confirm</span></span>
<span data-ttu-id="8125a-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8125a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8125a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8125a-135">-WhatIf</span></span>
<span data-ttu-id="8125a-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8125a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8125a-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8125a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8125a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8125a-138">CommonParameters</span></span>
<span data-ttu-id="8125a-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8125a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8125a-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8125a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8125a-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8125a-141">INPUTS</span></span>

### <span data-ttu-id="8125a-142">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8125a-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="8125a-143">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="8125a-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="8125a-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8125a-144">OUTPUTS</span></span>

### <span data-ttu-id="8125a-145">Microsoft. Azure. Commands. Synapse. Models. PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="8125a-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

## <span data-ttu-id="8125a-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8125a-146">NOTES</span></span>

## <span data-ttu-id="8125a-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8125a-147">RELATED LINKS</span></span>
