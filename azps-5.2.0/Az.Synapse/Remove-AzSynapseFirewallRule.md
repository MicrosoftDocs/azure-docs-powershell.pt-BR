---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
ms.openlocfilehash: 8dd3321804afb2f7901a8acd22cfdab3dd990c41
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263940"
---
# <span data-ttu-id="f89e6-101">Remove-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f89e6-101">Remove-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="f89e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f89e6-102">SYNOPSIS</span></span>
<span data-ttu-id="f89e6-103">Exclui uma regra de firewall de análise do Synapse.</span><span class="sxs-lookup"><span data-stu-id="f89e6-103">Deletes a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="f89e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f89e6-104">SYNTAX</span></span>

### <span data-ttu-id="f89e6-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f89e6-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f89e6-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f89e6-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseFirewallRule -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f89e6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f89e6-107">DESCRIPTION</span></span>
<span data-ttu-id="f89e6-108">O cmdlet **Remove-AzSynapseFirewallRule** exclui permanentemente uma regra de firewall de análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="f89e6-108">The **Remove-AzSynapseFirewallRule** cmdlet permanently deletes an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="f89e6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f89e6-109">EXAMPLES</span></span>

### <span data-ttu-id="f89e6-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f89e6-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="f89e6-111">Esse comando exclui a regra de firewall chamada ContosoFirewallRule em espaço de trabalho ContosoWorkspace com o nome ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="f89e6-111">This command deletes firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="f89e6-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f89e6-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseFirewallRule -Name ContosoFirewallRule
```

<span data-ttu-id="f89e6-113">Esse comando exclui a regra de firewall chamada ContosoFirewallRule em um espaço de trabalho por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="f89e6-113">This command deletes firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="f89e6-114">OS</span><span class="sxs-lookup"><span data-stu-id="f89e6-114">PARAMETERS</span></span>

### <span data-ttu-id="f89e6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f89e6-115">-AsJob</span></span>
<span data-ttu-id="f89e6-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f89e6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f89e6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f89e6-117">-DefaultProfile</span></span>
<span data-ttu-id="f89e6-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f89e6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f89e6-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f89e6-119">-Force</span></span>
<span data-ttu-id="f89e6-120">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="f89e6-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f89e6-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f89e6-121">-Name</span></span>
<span data-ttu-id="f89e6-122">O nome da regra firerwall para o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f89e6-122">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="f89e6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f89e6-123">-PassThru</span></span>
<span data-ttu-id="f89e6-124">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="f89e6-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f89e6-125">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f89e6-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f89e6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f89e6-126">-ResourceGroupName</span></span>
<span data-ttu-id="f89e6-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f89e6-127">Resource group name.</span></span>

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

### <span data-ttu-id="f89e6-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f89e6-128">-WorkspaceName</span></span>
<span data-ttu-id="f89e6-129">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="f89e6-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f89e6-130">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="f89e6-130">-WorkspaceObject</span></span>
<span data-ttu-id="f89e6-131">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="f89e6-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f89e6-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f89e6-132">-Confirm</span></span>
<span data-ttu-id="f89e6-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f89e6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f89e6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f89e6-134">-WhatIf</span></span>
<span data-ttu-id="f89e6-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f89e6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f89e6-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f89e6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f89e6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f89e6-137">CommonParameters</span></span>
<span data-ttu-id="f89e6-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f89e6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f89e6-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f89e6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f89e6-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f89e6-140">INPUTS</span></span>

### <span data-ttu-id="f89e6-141">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f89e6-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f89e6-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f89e6-142">OUTPUTS</span></span>

### <span data-ttu-id="f89e6-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f89e6-143">System.Boolean</span></span>

## <span data-ttu-id="f89e6-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f89e6-144">NOTES</span></span>

## <span data-ttu-id="f89e6-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f89e6-145">RELATED LINKS</span></span>
