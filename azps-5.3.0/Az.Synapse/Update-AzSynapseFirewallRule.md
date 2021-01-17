---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
ms.openlocfilehash: 9188a1cc8dde39db4d755fb2059f3633fc85ead8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432898"
---
# <span data-ttu-id="3cae3-101">Update-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3cae3-101">Update-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="3cae3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3cae3-102">SYNOPSIS</span></span>
<span data-ttu-id="3cae3-103">Atualiza uma regra de firewall de análise do Synapse.</span><span class="sxs-lookup"><span data-stu-id="3cae3-103">Updates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="3cae3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3cae3-104">SYNTAX</span></span>

### <span data-ttu-id="3cae3-105">UpdateByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3cae3-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-StartIpAddress <String>] [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cae3-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cae3-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-StartIpAddress <String>]
 [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3cae3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3cae3-107">DESCRIPTION</span></span>
<span data-ttu-id="3cae3-108">O cmdlet **Update-AzSynapseFirewallRule** modifica uma regra de firewall de análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="3cae3-108">The **Update-AzSynapseFirewallRule** cmdlet modifys an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="3cae3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3cae3-109">EXAMPLES</span></span>

### <span data-ttu-id="3cae3-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3cae3-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="3cae3-111">Este comando atualiza a regra de firewall chamada ContosoFirewallRule em espaço de trabalho ContosoWorkspace com o nome ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="3cae3-111">This command updates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="3cae3-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3cae3-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="3cae3-113">Este comando atualiza a regra de firewall chamada ContosoFirewallRule em um espaço de trabalho por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="3cae3-113">This command updates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="3cae3-114">OS</span><span class="sxs-lookup"><span data-stu-id="3cae3-114">PARAMETERS</span></span>

### <span data-ttu-id="3cae3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3cae3-115">-AsJob</span></span>
<span data-ttu-id="3cae3-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3cae3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3cae3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cae3-117">-DefaultProfile</span></span>
<span data-ttu-id="3cae3-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3cae3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cae3-119">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="3cae3-119">-EndIpAddress</span></span>
<span data-ttu-id="3cae3-120">O endereço IP final da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="3cae3-120">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="3cae3-121">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="3cae3-121">Must be IPv4 format.</span></span>
<span data-ttu-id="3cae3-122">Deve ser maior ou igual a startIpAddress.</span><span class="sxs-lookup"><span data-stu-id="3cae3-122">Must be greater than or equal to startIpAddress.</span></span>

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

### <span data-ttu-id="3cae3-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="3cae3-123">-Name</span></span>
<span data-ttu-id="3cae3-124">O nome da regra firerwall para o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3cae3-124">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="3cae3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cae3-125">-ResourceGroupName</span></span>
<span data-ttu-id="3cae3-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3cae3-126">Resource group name.</span></span>

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

### <span data-ttu-id="3cae3-127">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="3cae3-127">-StartIpAddress</span></span>
<span data-ttu-id="3cae3-128">O endereço IP inicial da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="3cae3-128">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="3cae3-129">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="3cae3-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="3cae3-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3cae3-130">-WorkspaceName</span></span>
<span data-ttu-id="3cae3-131">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="3cae3-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3cae3-132">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="3cae3-132">-WorkspaceObject</span></span>
<span data-ttu-id="3cae3-133">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="3cae3-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3cae3-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3cae3-134">-Confirm</span></span>
<span data-ttu-id="3cae3-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cae3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cae3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cae3-136">-WhatIf</span></span>
<span data-ttu-id="3cae3-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3cae3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cae3-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3cae3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cae3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cae3-139">CommonParameters</span></span>
<span data-ttu-id="3cae3-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cae3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cae3-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3cae3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cae3-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3cae3-142">INPUTS</span></span>

### <span data-ttu-id="3cae3-143">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3cae3-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3cae3-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3cae3-144">OUTPUTS</span></span>

### <span data-ttu-id="3cae3-145">Microsoft. Azure. Commands. Synapse. Models. PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3cae3-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="3cae3-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3cae3-146">NOTES</span></span>

## <span data-ttu-id="3cae3-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3cae3-147">RELATED LINKS</span></span>
