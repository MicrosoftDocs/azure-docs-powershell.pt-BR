---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
ms.openlocfilehash: b4579d01ed6dd5a7d742cbb82afb424151579772
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116052"
---
# <span data-ttu-id="8e253-101">New-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8e253-101">New-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="8e253-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e253-102">SYNOPSIS</span></span>
<span data-ttu-id="8e253-103">Cria uma Regra de Firewall de Análise Synapse.</span><span class="sxs-lookup"><span data-stu-id="8e253-103">Creates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="8e253-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e253-104">SYNTAX</span></span>

### <span data-ttu-id="8e253-105">CreateByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8e253-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -StartIpAddress <String> -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e253-106">CreateByNameAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e253-106">CreateByNameAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e253-107">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e253-107">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> -StartIpAddress <String>
 -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e253-108">CreateByParentObjectAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e253-108">CreateByParentObjectAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e253-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e253-109">DESCRIPTION</span></span>
<span data-ttu-id="8e253-110">O cmdlet **New-AzSynapseFirewallRule** cria uma Regra de Firewall de Análise Synapse do Azure.</span><span class="sxs-lookup"><span data-stu-id="8e253-110">The **New-AzSynapseFirewallRule** cmdlet creates an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="8e253-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8e253-111">EXAMPLES</span></span>

### <span data-ttu-id="8e253-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8e253-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="8e253-113">Esse comando cria uma regra de firewall chamada ContosoFirewallRule sob o espaço de trabalho ContosoWorkspace com o nome ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="8e253-113">This command creates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="8e253-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8e253-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="8e253-115">Esse comando cria uma regra de firewall chamada ContosoFirewallRule sob um espaço de trabalho por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e253-115">This command creates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

### <span data-ttu-id="8e253-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="8e253-116">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -AllowAllAzureIP
```

<span data-ttu-id="8e253-117">Esse comando cria uma regra de firewall que permite todos os ips do azure sob um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8e253-117">This command creates firewall rule that allow all azure ips under a workspace.</span></span>

## <span data-ttu-id="8e253-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e253-118">PARAMETERS</span></span>

### <span data-ttu-id="8e253-119">-AllowAllAzureIP</span><span class="sxs-lookup"><span data-stu-id="8e253-119">-AllowAllAzureIP</span></span>
<span data-ttu-id="8e253-120">Cria uma regra de firewall especial que permite que todos os IPs do Azure tenham acesso.</span><span class="sxs-lookup"><span data-stu-id="8e253-120">Creates a special firewall rule that permits all Azure IPs to have access.</span></span>

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

### <span data-ttu-id="8e253-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e253-121">-AsJob</span></span>
<span data-ttu-id="8e253-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8e253-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e253-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e253-123">-DefaultProfile</span></span>
<span data-ttu-id="8e253-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e253-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e253-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="8e253-125">-EndIpAddress</span></span>
<span data-ttu-id="8e253-126">O endereço IP final da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="8e253-126">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="8e253-127">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="8e253-127">Must be IPv4 format.</span></span>
<span data-ttu-id="8e253-128">Deve ser maior ou igual a startIpAddress.</span><span class="sxs-lookup"><span data-stu-id="8e253-128">Must be greater than or equal to startIpAddress.</span></span>

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

### <span data-ttu-id="8e253-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e253-129">-Name</span></span>
<span data-ttu-id="8e253-130">O nome da regra de firerwall para o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8e253-130">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="8e253-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e253-131">-ResourceGroupName</span></span>
<span data-ttu-id="8e253-132">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8e253-132">Resource group name.</span></span>

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

### <span data-ttu-id="8e253-133">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="8e253-133">-StartIpAddress</span></span>
<span data-ttu-id="8e253-134">O endereço IP inicial da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="8e253-134">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="8e253-135">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="8e253-135">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="8e253-136">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="8e253-136">-WorkspaceName</span></span>
<span data-ttu-id="8e253-137">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="8e253-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8e253-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8e253-138">-WorkspaceObject</span></span>
<span data-ttu-id="8e253-139">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e253-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8e253-140">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8e253-140">-Confirm</span></span>
<span data-ttu-id="8e253-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e253-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e253-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e253-142">-WhatIf</span></span>
<span data-ttu-id="8e253-143">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8e253-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e253-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8e253-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e253-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e253-145">CommonParameters</span></span>
<span data-ttu-id="8e253-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e253-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e253-147">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e253-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e253-148">Entradas</span><span class="sxs-lookup"><span data-stu-id="8e253-148">INPUTS</span></span>

### <span data-ttu-id="8e253-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8e253-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8e253-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="8e253-150">OUTPUTS</span></span>

### <span data-ttu-id="8e253-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8e253-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="8e253-152">Notas</span><span class="sxs-lookup"><span data-stu-id="8e253-152">NOTES</span></span>

## <span data-ttu-id="8e253-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e253-153">RELATED LINKS</span></span>
