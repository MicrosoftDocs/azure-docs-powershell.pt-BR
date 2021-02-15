---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/resume-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
ms.openlocfilehash: ff2a68d7e0ae0ad94f685bbe1cfb795f7cd6a706
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112386"
---
# <span data-ttu-id="92b7e-101">Resume-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="92b7e-101">Resume-AzSynapseSqlPool</span></span>

## <span data-ttu-id="92b7e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="92b7e-102">SYNOPSIS</span></span>
<span data-ttu-id="92b7e-103">Retoma um pool SQL do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="92b7e-103">Resumes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="92b7e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92b7e-104">SYNTAX</span></span>

### <span data-ttu-id="92b7e-105">ResumeByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="92b7e-105">ResumeByNameParameterSet (Default)</span></span>
```
Resume-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92b7e-106">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92b7e-106">ResumeByParentObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92b7e-107">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92b7e-107">ResumeByInputObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92b7e-108">ResumeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92b7e-108">ResumeByResourceIdParameterSet</span></span>
```
Resume-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92b7e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="92b7e-109">DESCRIPTION</span></span>
<span data-ttu-id="92b7e-110">O cmdlet **Resume-AzSynapseSqlPool** retomará um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="92b7e-110">The **Resume-AzSynapseSqlPool** cmdlet resumes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="92b7e-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="92b7e-111">EXAMPLES</span></span>

### <span data-ttu-id="92b7e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="92b7e-112">Example 1</span></span>
```powershell
PS C:\> Resume-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="92b7e-113">Esse comando retoma um pool SQL suspenso do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="92b7e-113">This command resumes a suspended Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="92b7e-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92b7e-114">PARAMETERS</span></span>

### <span data-ttu-id="92b7e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92b7e-115">-AsJob</span></span>
<span data-ttu-id="92b7e-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="92b7e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="92b7e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92b7e-117">-DefaultProfile</span></span>
<span data-ttu-id="92b7e-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="92b7e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92b7e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92b7e-119">-InputObject</span></span>
<span data-ttu-id="92b7e-120">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="92b7e-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: ResumeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92b7e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="92b7e-121">-Name</span></span>
<span data-ttu-id="92b7e-122">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="92b7e-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b7e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92b7e-123">-PassThru</span></span>
<span data-ttu-id="92b7e-124">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="92b7e-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="92b7e-125">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="92b7e-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="92b7e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92b7e-126">-ResourceGroupName</span></span>
<span data-ttu-id="92b7e-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="92b7e-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b7e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92b7e-128">-ResourceId</span></span>
<span data-ttu-id="92b7e-129">Identificador de recursos do Pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="92b7e-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b7e-130">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="92b7e-130">-WorkspaceName</span></span>
<span data-ttu-id="92b7e-131">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="92b7e-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b7e-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="92b7e-132">-WorkspaceObject</span></span>
<span data-ttu-id="92b7e-133">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="92b7e-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92b7e-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="92b7e-134">-Confirm</span></span>
<span data-ttu-id="92b7e-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92b7e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92b7e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92b7e-136">-WhatIf</span></span>
<span data-ttu-id="92b7e-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="92b7e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92b7e-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="92b7e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92b7e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92b7e-139">CommonParameters</span></span>
<span data-ttu-id="92b7e-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92b7e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92b7e-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92b7e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92b7e-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="92b7e-142">INPUTS</span></span>

### <span data-ttu-id="92b7e-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="92b7e-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="92b7e-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="92b7e-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="92b7e-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="92b7e-145">OUTPUTS</span></span>

### <span data-ttu-id="92b7e-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="92b7e-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="92b7e-147">Notas</span><span class="sxs-lookup"><span data-stu-id="92b7e-147">NOTES</span></span>

## <span data-ttu-id="92b7e-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92b7e-148">RELATED LINKS</span></span>
