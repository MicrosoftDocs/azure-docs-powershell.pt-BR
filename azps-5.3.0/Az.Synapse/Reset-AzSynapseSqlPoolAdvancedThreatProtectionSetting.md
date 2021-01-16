---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: c5f1c3f2d1a23a06286cdbf7fb54915d33b1e3d3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429628"
---
# <span data-ttu-id="fa76f-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="fa76f-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="fa76f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fa76f-102">SYNOPSIS</span></span>
<span data-ttu-id="fa76f-103">Remove as configurações avançadas de proteção contra ameaças de um pool SQL.</span><span class="sxs-lookup"><span data-stu-id="fa76f-103">Removes the advanced threat protection settings from a SQL pool.</span></span>

## <span data-ttu-id="fa76f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa76f-104">SYNTAX</span></span>

### <span data-ttu-id="fa76f-105">ClearByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fa76f-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa76f-106">ClearByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa76f-106">ClearByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa76f-107">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa76f-107">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa76f-108">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa76f-108">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa76f-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fa76f-109">DESCRIPTION</span></span>
<span data-ttu-id="fa76f-110">O cmdlet **Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting** remove as configurações avançadas de proteção contra ameaças de um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="fa76f-110">The **Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="fa76f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa76f-111">EXAMPLES</span></span>

### <span data-ttu-id="fa76f-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fa76f-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="fa76f-113">Esse comando remove as configurações avançadas de proteção contra ameaças de um pool SQL chamado ContosoSqlPool sob o espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="fa76f-113">This command removes the advanced threat protection settings from a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="fa76f-114">OS</span><span class="sxs-lookup"><span data-stu-id="fa76f-114">PARAMETERS</span></span>

### <span data-ttu-id="fa76f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa76f-115">-AsJob</span></span>
<span data-ttu-id="fa76f-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fa76f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa76f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa76f-117">-DefaultProfile</span></span>
<span data-ttu-id="fa76f-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fa76f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa76f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa76f-119">-InputObject</span></span>
<span data-ttu-id="fa76f-120">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="fa76f-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="fa76f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa76f-121">-Name</span></span>
<span data-ttu-id="fa76f-122">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="fa76f-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="fa76f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa76f-123">-PassThru</span></span>
<span data-ttu-id="fa76f-124">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="fa76f-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="fa76f-125">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fa76f-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="fa76f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa76f-126">-ResourceGroupName</span></span>
<span data-ttu-id="fa76f-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fa76f-127">Resource group name.</span></span>

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

### <span data-ttu-id="fa76f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa76f-128">-ResourceId</span></span>
<span data-ttu-id="fa76f-129">Identificador de recurso do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="fa76f-129">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="fa76f-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fa76f-130">-WorkspaceName</span></span>
<span data-ttu-id="fa76f-131">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="fa76f-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="fa76f-132">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="fa76f-132">-WorkspaceObject</span></span>
<span data-ttu-id="fa76f-133">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="fa76f-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="fa76f-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fa76f-134">-Confirm</span></span>
<span data-ttu-id="fa76f-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa76f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa76f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa76f-136">-WhatIf</span></span>
<span data-ttu-id="fa76f-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fa76f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa76f-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fa76f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa76f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa76f-139">CommonParameters</span></span>
<span data-ttu-id="fa76f-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa76f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa76f-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa76f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa76f-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fa76f-142">INPUTS</span></span>

### <span data-ttu-id="fa76f-143">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fa76f-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="fa76f-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="fa76f-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="fa76f-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fa76f-145">OUTPUTS</span></span>

### <span data-ttu-id="fa76f-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fa76f-146">System.Boolean</span></span>

## <span data-ttu-id="fa76f-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fa76f-147">NOTES</span></span>

## <span data-ttu-id="fa76f-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa76f-148">RELATED LINKS</span></span>
