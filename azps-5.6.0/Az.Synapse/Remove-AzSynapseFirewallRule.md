---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
ms.openlocfilehash: 6df0e33ff94be7bf5e060b929206c09180d830f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886522"
---
# <span data-ttu-id="b6e6b-101">Remove-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b6e6b-101">Remove-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="b6e6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6e6b-102">SYNOPSIS</span></span>
<span data-ttu-id="b6e6b-103">Exclui uma Regra de Firewall de Análise do Synapse.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-103">Deletes a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="b6e6b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b6e6b-104">SYNTAX</span></span>

### <span data-ttu-id="b6e6b-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b6e6b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6e6b-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6e6b-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseFirewallRule -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6e6b-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b6e6b-107">DESCRIPTION</span></span>
<span data-ttu-id="b6e6b-108">O cmdlet **Remove-AzSynapseFirewallRule** exclui permanentemente uma Regra de Firewall do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-108">The **Remove-AzSynapseFirewallRule** cmdlet permanently deletes an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="b6e6b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6e6b-109">EXAMPLES</span></span>

### <span data-ttu-id="b6e6b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b6e6b-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="b6e6b-111">Este comando exclui a regra de firewall chamada ContosoFirewallRule no espaço de trabalho ContosoWorkspace com o nome ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-111">This command deletes firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="b6e6b-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b6e6b-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseFirewallRule -Name ContosoFirewallRule
```

<span data-ttu-id="b6e6b-113">Este comando exclui a regra de firewall chamada ContosoFirewallRule em um espaço de trabalho por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-113">This command deletes firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="b6e6b-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b6e6b-114">PARAMETERS</span></span>

### <span data-ttu-id="b6e6b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6e6b-115">-AsJob</span></span>
<span data-ttu-id="b6e6b-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b6e6b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6e6b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6e6b-117">-DefaultProfile</span></span>
<span data-ttu-id="b6e6b-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6e6b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b6e6b-119">-Force</span></span>
<span data-ttu-id="b6e6b-120">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b6e6b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b6e6b-121">-Name</span></span>
<span data-ttu-id="b6e6b-122">O nome da regra firerwall para o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-122">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6e6b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6e6b-123">-PassThru</span></span>
<span data-ttu-id="b6e6b-124">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b6e6b-125">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="b6e6b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6e6b-126">-ResourceGroupName</span></span>
<span data-ttu-id="b6e6b-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6e6b-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b6e6b-128">-WorkspaceName</span></span>
<span data-ttu-id="b6e6b-129">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6e6b-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b6e6b-130">-WorkspaceObject</span></span>
<span data-ttu-id="b6e6b-131">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6e6b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6e6b-132">-Confirm</span></span>
<span data-ttu-id="b6e6b-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6e6b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6e6b-134">-WhatIf</span></span>
<span data-ttu-id="b6e6b-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6e6b-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6e6b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6e6b-137">CommonParameters</span></span>
<span data-ttu-id="b6e6b-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6e6b-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6e6b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6e6b-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6e6b-140">INPUTS</span></span>

### <span data-ttu-id="b6e6b-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b6e6b-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b6e6b-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b6e6b-142">OUTPUTS</span></span>

### <span data-ttu-id="b6e6b-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b6e6b-143">System.Boolean</span></span>

## <span data-ttu-id="b6e6b-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="b6e6b-144">NOTES</span></span>

## <span data-ttu-id="b6e6b-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6e6b-145">RELATED LINKS</span></span>
