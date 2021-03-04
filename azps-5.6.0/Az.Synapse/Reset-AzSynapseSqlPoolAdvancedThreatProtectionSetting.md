---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 425b9c74fac1cd17b8e2c86045fbb4fcd8875b67
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888772"
---
# <span data-ttu-id="cbe2b-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="cbe2b-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="cbe2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbe2b-102">SYNOPSIS</span></span>
<span data-ttu-id="cbe2b-103">Remove as configurações avançadas de proteção contra ameaças de um SQL pool.</span><span class="sxs-lookup"><span data-stu-id="cbe2b-103">Removes the advanced threat protection settings from a SQL pool.</span></span>

## <span data-ttu-id="cbe2b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cbe2b-104">SYNTAX</span></span>

### <span data-ttu-id="cbe2b-105">ClearByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cbe2b-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cbe2b-106">ClearByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbe2b-106">ClearByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbe2b-107">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbe2b-107">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbe2b-108">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbe2b-108">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbe2b-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cbe2b-109">DESCRIPTION</span></span>
<span data-ttu-id="cbe2b-110">O cmdlet **Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting** remove as configurações avançadas de proteção contra ameaças de um pool do Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="cbe2b-110">The **Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="cbe2b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cbe2b-111">EXAMPLES</span></span>

### <span data-ttu-id="cbe2b-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cbe2b-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="cbe2b-113">Este comando remove as configurações avançadas de proteção contra ameaças de um pool SQL chamado ContosoSqlPool no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cbe2b-113">This command removes the advanced threat protection settings from a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="cbe2b-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cbe2b-114">PARAMETERS</span></span>

### <span data-ttu-id="cbe2b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbe2b-115">-AsJob</span></span>
<span data-ttu-id="cbe2b-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cbe2b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cbe2b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbe2b-117">-DefaultProfile</span></span>
<span data-ttu-id="cbe2b-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cbe2b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbe2b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbe2b-119">-InputObject</span></span>
<span data-ttu-id="cbe2b-120">SQL objeto de entrada do pool, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="cbe2b-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: ClearByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbe2b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cbe2b-121">-Name</span></span>
<span data-ttu-id="cbe2b-122">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="cbe2b-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet, ClearByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbe2b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbe2b-123">-PassThru</span></span>
<span data-ttu-id="cbe2b-124">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="cbe2b-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="cbe2b-125">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="cbe2b-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="cbe2b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbe2b-126">-ResourceGroupName</span></span>
<span data-ttu-id="cbe2b-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cbe2b-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbe2b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbe2b-128">-ResourceId</span></span>
<span data-ttu-id="cbe2b-129">Identificador de recursos do Pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="cbe2b-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbe2b-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cbe2b-130">-WorkspaceName</span></span>
<span data-ttu-id="cbe2b-131">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="cbe2b-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbe2b-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cbe2b-132">-WorkspaceObject</span></span>
<span data-ttu-id="cbe2b-133">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="cbe2b-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ClearByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbe2b-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cbe2b-134">-Confirm</span></span>
<span data-ttu-id="cbe2b-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbe2b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbe2b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbe2b-136">-WhatIf</span></span>
<span data-ttu-id="cbe2b-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cbe2b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbe2b-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cbe2b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbe2b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbe2b-139">CommonParameters</span></span>
<span data-ttu-id="cbe2b-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbe2b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbe2b-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbe2b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbe2b-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cbe2b-142">INPUTS</span></span>

### <span data-ttu-id="cbe2b-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cbe2b-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="cbe2b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="cbe2b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="cbe2b-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cbe2b-145">OUTPUTS</span></span>

### <span data-ttu-id="cbe2b-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cbe2b-146">System.Boolean</span></span>

## <span data-ttu-id="cbe2b-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="cbe2b-147">NOTES</span></span>

## <span data-ttu-id="cbe2b-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbe2b-148">RELATED LINKS</span></span>
