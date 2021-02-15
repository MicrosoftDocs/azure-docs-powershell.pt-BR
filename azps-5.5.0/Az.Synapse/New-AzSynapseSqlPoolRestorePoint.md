---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 574c41fe8b0f3266a6fff80c020b60c9832cb431
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112401"
---
# <span data-ttu-id="91ffd-101">New-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="91ffd-101">New-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="91ffd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91ffd-102">SYNOPSIS</span></span>
<span data-ttu-id="91ffd-103">Cria um novo ponto de restauração em um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="91ffd-103">Creates a new restore point in an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="91ffd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91ffd-104">SYNTAX</span></span>

### <span data-ttu-id="91ffd-105">CreateByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="91ffd-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91ffd-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91ffd-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91ffd-107">CreateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91ffd-107">CreateByInputObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91ffd-108">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="91ffd-108">CreateByResourceIdParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -ResourceId <String> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91ffd-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="91ffd-109">DESCRIPTION</span></span>
<span data-ttu-id="91ffd-110">O cmdlet **New-AzSynapseSqlPoolRestorePoint** cria um novo ponto de restauração de onde um pool SQL do Azure Synapse Analytics pode ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="91ffd-110">The **New-AzSynapseSqlPoolRestorePoint** cmdlet creates a new restore point that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="91ffd-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="91ffd-111">EXAMPLES</span></span>

### <span data-ttu-id="91ffd-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="91ffd-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -RestorePointLabel ContosoRestorePoint
```

<span data-ttu-id="91ffd-113">Esse comando cria um ponto de restauração para o pool SQL chamado ContosoSqlPool no espaço de trabalho ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="91ffd-113">This command creates a restore point for SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="91ffd-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91ffd-114">PARAMETERS</span></span>

### <span data-ttu-id="91ffd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91ffd-115">-AsJob</span></span>
<span data-ttu-id="91ffd-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="91ffd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91ffd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91ffd-117">-DefaultProfile</span></span>
<span data-ttu-id="91ffd-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="91ffd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91ffd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91ffd-119">-InputObject</span></span>
<span data-ttu-id="91ffd-120">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="91ffd-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="91ffd-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="91ffd-121">-Name</span></span>
<span data-ttu-id="91ffd-122">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="91ffd-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="91ffd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91ffd-123">-ResourceGroupName</span></span>
<span data-ttu-id="91ffd-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="91ffd-124">Resource group name.</span></span>

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

### <span data-ttu-id="91ffd-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91ffd-125">-ResourceId</span></span>
<span data-ttu-id="91ffd-126">Identificador de recursos do Pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="91ffd-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="91ffd-127">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="91ffd-127">-RestorePointLabel</span></span>
<span data-ttu-id="91ffd-128">O rótulo ao que associamos um ponto de restauração pode não ser exclusivo.</span><span class="sxs-lookup"><span data-stu-id="91ffd-128">The label we associate a restore point with, may not be unique.</span></span>

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

### <span data-ttu-id="91ffd-129">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="91ffd-129">-WorkspaceName</span></span>
<span data-ttu-id="91ffd-130">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="91ffd-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="91ffd-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="91ffd-131">-WorkspaceObject</span></span>
<span data-ttu-id="91ffd-132">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="91ffd-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="91ffd-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="91ffd-133">-Confirm</span></span>
<span data-ttu-id="91ffd-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91ffd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91ffd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91ffd-135">-WhatIf</span></span>
<span data-ttu-id="91ffd-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="91ffd-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91ffd-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="91ffd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91ffd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91ffd-138">CommonParameters</span></span>
<span data-ttu-id="91ffd-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91ffd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91ffd-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91ffd-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91ffd-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="91ffd-141">INPUTS</span></span>

### <span data-ttu-id="91ffd-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="91ffd-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="91ffd-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="91ffd-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="91ffd-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="91ffd-144">OUTPUTS</span></span>

### <span data-ttu-id="91ffd-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="91ffd-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

## <span data-ttu-id="91ffd-146">Notas</span><span class="sxs-lookup"><span data-stu-id="91ffd-146">NOTES</span></span>

## <span data-ttu-id="91ffd-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91ffd-147">RELATED LINKS</span></span>
