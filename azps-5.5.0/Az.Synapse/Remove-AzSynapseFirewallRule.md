---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
ms.openlocfilehash: 8dd3321804afb2f7901a8acd22cfdab3dd990c41
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116307"
---
# <span data-ttu-id="411de-101">Remove-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="411de-101">Remove-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="411de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="411de-102">SYNOPSIS</span></span>
<span data-ttu-id="411de-103">Exclui uma Regra de Firewall de Análise Synapse.</span><span class="sxs-lookup"><span data-stu-id="411de-103">Deletes a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="411de-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="411de-104">SYNTAX</span></span>

### <span data-ttu-id="411de-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="411de-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="411de-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="411de-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseFirewallRule -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="411de-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="411de-107">DESCRIPTION</span></span>
<span data-ttu-id="411de-108">O cmdlet **Remove-AzSynapseFirewallRule** exclui permanentemente uma Regra de Firewall do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="411de-108">The **Remove-AzSynapseFirewallRule** cmdlet permanently deletes an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="411de-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="411de-109">EXAMPLES</span></span>

### <span data-ttu-id="411de-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="411de-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="411de-111">Esse comando exclui a regra de firewall chamada ContosoFirewallRule no espaço de trabalho ContosoWorkspace com o nome ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="411de-111">This command deletes firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="411de-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="411de-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseFirewallRule -Name ContosoFirewallRule
```

<span data-ttu-id="411de-113">Esse comando exclui a regra de firewall chamada ContosoFirewallRule sob um espaço de trabalho por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="411de-113">This command deletes firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="411de-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="411de-114">PARAMETERS</span></span>

### <span data-ttu-id="411de-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="411de-115">-AsJob</span></span>
<span data-ttu-id="411de-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="411de-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="411de-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="411de-117">-DefaultProfile</span></span>
<span data-ttu-id="411de-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="411de-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="411de-119">-Forçar</span><span class="sxs-lookup"><span data-stu-id="411de-119">-Force</span></span>
<span data-ttu-id="411de-120">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="411de-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="411de-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="411de-121">-Name</span></span>
<span data-ttu-id="411de-122">O nome da regra de firerwall para o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="411de-122">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="411de-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="411de-123">-PassThru</span></span>
<span data-ttu-id="411de-124">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="411de-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="411de-125">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="411de-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="411de-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="411de-126">-ResourceGroupName</span></span>
<span data-ttu-id="411de-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="411de-127">Resource group name.</span></span>

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

### <span data-ttu-id="411de-128">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="411de-128">-WorkspaceName</span></span>
<span data-ttu-id="411de-129">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="411de-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="411de-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="411de-130">-WorkspaceObject</span></span>
<span data-ttu-id="411de-131">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="411de-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="411de-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="411de-132">-Confirm</span></span>
<span data-ttu-id="411de-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="411de-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="411de-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="411de-134">-WhatIf</span></span>
<span data-ttu-id="411de-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="411de-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="411de-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="411de-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="411de-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="411de-137">CommonParameters</span></span>
<span data-ttu-id="411de-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="411de-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="411de-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="411de-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="411de-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="411de-140">INPUTS</span></span>

### <span data-ttu-id="411de-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="411de-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="411de-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="411de-142">OUTPUTS</span></span>

### <span data-ttu-id="411de-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="411de-143">System.Boolean</span></span>

## <span data-ttu-id="411de-144">Notas</span><span class="sxs-lookup"><span data-stu-id="411de-144">NOTES</span></span>

## <span data-ttu-id="411de-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="411de-145">RELATED LINKS</span></span>
