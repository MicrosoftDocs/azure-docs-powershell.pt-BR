---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
ms.openlocfilehash: b4579d01ed6dd5a7d742cbb82afb424151579772
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282321"
---
# <span data-ttu-id="eafb0-101">New-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="eafb0-101">New-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="eafb0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eafb0-102">SYNOPSIS</span></span>
<span data-ttu-id="eafb0-103">Cria uma regra de firewall de análise do Synapse.</span><span class="sxs-lookup"><span data-stu-id="eafb0-103">Creates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="eafb0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eafb0-104">SYNTAX</span></span>

### <span data-ttu-id="eafb0-105">CreateByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="eafb0-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -StartIpAddress <String> -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eafb0-106">CreateByNameAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="eafb0-106">CreateByNameAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eafb0-107">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eafb0-107">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> -StartIpAddress <String>
 -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eafb0-108">CreateByParentObjectAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="eafb0-108">CreateByParentObjectAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eafb0-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eafb0-109">DESCRIPTION</span></span>
<span data-ttu-id="eafb0-110">O cmdlet **New-AzSynapseFirewallRule** cria uma regra de firewall de análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="eafb0-110">The **New-AzSynapseFirewallRule** cmdlet creates an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="eafb0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eafb0-111">EXAMPLES</span></span>

### <span data-ttu-id="eafb0-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eafb0-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="eafb0-113">Esse comando cria uma regra de firewall chamada ContosoFirewallRule em espaço de trabalho ContosoWorkspace com o nome ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="eafb0-113">This command creates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="eafb0-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="eafb0-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="eafb0-115">Esse comando cria uma regra de firewall chamada ContosoFirewallRule em um espaço de trabalho por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="eafb0-115">This command creates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

### <span data-ttu-id="eafb0-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="eafb0-116">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -AllowAllAzureIP
```

<span data-ttu-id="eafb0-117">Esse comando cria uma regra de firewall que permite todos os IPS do Azure em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="eafb0-117">This command creates firewall rule that allow all azure ips under a workspace.</span></span>

## <span data-ttu-id="eafb0-118">OS</span><span class="sxs-lookup"><span data-stu-id="eafb0-118">PARAMETERS</span></span>

### <span data-ttu-id="eafb0-119">-AllowAllAzureIP</span><span class="sxs-lookup"><span data-stu-id="eafb0-119">-AllowAllAzureIP</span></span>
<span data-ttu-id="eafb0-120">Cria uma regra de firewall especial que permite que todos os IPs do Azure tenham acesso.</span><span class="sxs-lookup"><span data-stu-id="eafb0-120">Creates a special firewall rule that permits all Azure IPs to have access.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateByNameAllowAllIpParameterSet, CreateByParentObjectAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eafb0-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eafb0-121">-AsJob</span></span>
<span data-ttu-id="eafb0-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="eafb0-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eafb0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eafb0-123">-DefaultProfile</span></span>
<span data-ttu-id="eafb0-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eafb0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eafb0-125">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="eafb0-125">-EndIpAddress</span></span>
<span data-ttu-id="eafb0-126">O endereço IP final da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="eafb0-126">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="eafb0-127">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="eafb0-127">Must be IPv4 format.</span></span>
<span data-ttu-id="eafb0-128">Deve ser maior ou igual a startIpAddress.</span><span class="sxs-lookup"><span data-stu-id="eafb0-128">Must be greater than or equal to startIpAddress.</span></span>

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

### <span data-ttu-id="eafb0-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="eafb0-129">-Name</span></span>
<span data-ttu-id="eafb0-130">O nome da regra firerwall para o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="eafb0-130">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eafb0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eafb0-131">-ResourceGroupName</span></span>
<span data-ttu-id="eafb0-132">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eafb0-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByNameAllowAllIpParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eafb0-133">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="eafb0-133">-StartIpAddress</span></span>
<span data-ttu-id="eafb0-134">O endereço IP inicial da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="eafb0-134">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="eafb0-135">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="eafb0-135">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="eafb0-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="eafb0-136">-WorkspaceName</span></span>
<span data-ttu-id="eafb0-137">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="eafb0-137">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByNameAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eafb0-138">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="eafb0-138">-WorkspaceObject</span></span>
<span data-ttu-id="eafb0-139">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="eafb0-139">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet, CreateByParentObjectAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eafb0-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="eafb0-140">-Confirm</span></span>
<span data-ttu-id="eafb0-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eafb0-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eafb0-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eafb0-142">-WhatIf</span></span>
<span data-ttu-id="eafb0-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="eafb0-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eafb0-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eafb0-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eafb0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eafb0-145">CommonParameters</span></span>
<span data-ttu-id="eafb0-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eafb0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eafb0-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eafb0-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eafb0-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eafb0-148">INPUTS</span></span>

### <span data-ttu-id="eafb0-149">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="eafb0-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="eafb0-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eafb0-150">OUTPUTS</span></span>

### <span data-ttu-id="eafb0-151">Microsoft. Azure. Commands. Synapse. Models. PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="eafb0-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="eafb0-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eafb0-152">NOTES</span></span>

## <span data-ttu-id="eafb0-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eafb0-153">RELATED LINKS</span></span>
