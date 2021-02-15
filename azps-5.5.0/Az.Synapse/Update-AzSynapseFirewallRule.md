---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
ms.openlocfilehash: 9188a1cc8dde39db4d755fb2059f3633fc85ead8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114359"
---
# <span data-ttu-id="7a902-101">Update-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7a902-101">Update-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="7a902-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a902-102">SYNOPSIS</span></span>
<span data-ttu-id="7a902-103">Atualiza uma Regra de Firewall de Análise Synapse.</span><span class="sxs-lookup"><span data-stu-id="7a902-103">Updates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="7a902-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a902-104">SYNTAX</span></span>

### <span data-ttu-id="7a902-105">UpdateByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7a902-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-StartIpAddress <String>] [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a902-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a902-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-StartIpAddress <String>]
 [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a902-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7a902-107">DESCRIPTION</span></span>
<span data-ttu-id="7a902-108">O cmdlet **Update-AzSynapseFirewallRule** modifica uma Regra de Firewall do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="7a902-108">The **Update-AzSynapseFirewallRule** cmdlet modifys an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="7a902-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7a902-109">EXAMPLES</span></span>

### <span data-ttu-id="7a902-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7a902-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="7a902-111">Este comando atualiza a regra de firewall chamada ContosoFirewallRule no espaço de trabalho ContosoWorkspace com o nome ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="7a902-111">This command updates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="7a902-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7a902-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="7a902-113">Este comando atualiza a regra de firewall chamada ContosoFirewallRule sob um espaço de trabalho por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="7a902-113">This command updates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="7a902-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a902-114">PARAMETERS</span></span>

### <span data-ttu-id="7a902-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a902-115">-AsJob</span></span>
<span data-ttu-id="7a902-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7a902-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a902-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a902-117">-DefaultProfile</span></span>
<span data-ttu-id="7a902-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a902-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a902-119">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="7a902-119">-EndIpAddress</span></span>
<span data-ttu-id="7a902-120">O endereço IP final da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="7a902-120">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="7a902-121">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="7a902-121">Must be IPv4 format.</span></span>
<span data-ttu-id="7a902-122">Deve ser maior ou igual a startIpAddress.</span><span class="sxs-lookup"><span data-stu-id="7a902-122">Must be greater than or equal to startIpAddress.</span></span>

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

### <span data-ttu-id="7a902-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a902-123">-Name</span></span>
<span data-ttu-id="7a902-124">O nome da regra de firerwall para o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="7a902-124">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="7a902-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a902-125">-ResourceGroupName</span></span>
<span data-ttu-id="7a902-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7a902-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a902-127">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="7a902-127">-StartIpAddress</span></span>
<span data-ttu-id="7a902-128">O endereço IP inicial da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="7a902-128">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="7a902-129">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="7a902-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="7a902-130">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="7a902-130">-WorkspaceName</span></span>
<span data-ttu-id="7a902-131">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="7a902-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a902-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7a902-132">-WorkspaceObject</span></span>
<span data-ttu-id="7a902-133">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="7a902-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a902-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7a902-134">-Confirm</span></span>
<span data-ttu-id="7a902-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a902-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a902-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a902-136">-WhatIf</span></span>
<span data-ttu-id="7a902-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7a902-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a902-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7a902-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a902-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a902-139">CommonParameters</span></span>
<span data-ttu-id="7a902-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a902-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a902-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a902-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a902-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="7a902-142">INPUTS</span></span>

### <span data-ttu-id="7a902-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7a902-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7a902-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="7a902-144">OUTPUTS</span></span>

### <span data-ttu-id="7a902-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7a902-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="7a902-146">Notas</span><span class="sxs-lookup"><span data-stu-id="7a902-146">NOTES</span></span>

## <span data-ttu-id="7a902-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a902-147">RELATED LINKS</span></span>
