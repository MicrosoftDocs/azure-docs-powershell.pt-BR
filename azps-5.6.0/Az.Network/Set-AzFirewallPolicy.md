---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 4e328d28ebe7faafa942d4f3448108a174f2aa71
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885848"
---
# <span data-ttu-id="e505b-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e505b-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="e505b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e505b-102">SYNOPSIS</span></span>
<span data-ttu-id="e505b-103">Salva uma política de firewall do azure modificada</span><span class="sxs-lookup"><span data-stu-id="e505b-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="e505b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e505b-104">SYNTAX</span></span>

### <span data-ttu-id="e505b-105">SetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e505b-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e505b-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e505b-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Location <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e505b-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e505b-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e505b-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e505b-108">DESCRIPTION</span></span>
<span data-ttu-id="e505b-109">O cmdlet **Set-AzFirewallPolicy** atualiza uma Política de Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="e505b-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="e505b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e505b-110">EXAMPLES</span></span>

### <span data-ttu-id="e505b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e505b-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="e505b-112">Este exemplo define a política de firewall com o novo valor de política de firewall</span><span class="sxs-lookup"><span data-stu-id="e505b-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="e505b-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e505b-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="e505b-114">Este exemplo define a política de firewall com o novo modo intel de ameaça</span><span class="sxs-lookup"><span data-stu-id="e505b-114">This example sets the firewall policy with the new threat intel mode</span></span>

### <span data-ttu-id="e505b-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e505b-115">Example 3</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="e505b-116">Este exemplo define a política de firewall com a nova lista branca de intel de ameaças</span><span class="sxs-lookup"><span data-stu-id="e505b-116">This example sets the firewall policy with the new threat intel whitelist</span></span>

## <span data-ttu-id="e505b-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e505b-117">PARAMETERS</span></span>

### <span data-ttu-id="e505b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e505b-118">-AsJob</span></span>
<span data-ttu-id="e505b-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e505b-119">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e505b-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="e505b-120">-BasePolicy</span></span>
<span data-ttu-id="e505b-121">A política base a ser herdado</span><span class="sxs-lookup"><span data-stu-id="e505b-121">The base policy to inherit from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e505b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e505b-122">-DefaultProfile</span></span>
<span data-ttu-id="e505b-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e505b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e505b-124">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="e505b-124">-DnsSetting</span></span>
<span data-ttu-id="e505b-125">A configuração DNS</span><span class="sxs-lookup"><span data-stu-id="e505b-125">The DNS Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyDnsSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e505b-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e505b-126">-InputObject</span></span>
<span data-ttu-id="e505b-127">Política do AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="e505b-127">The AzureFirewall Policy</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e505b-128">-Location</span><span class="sxs-lookup"><span data-stu-id="e505b-128">-Location</span></span>
<span data-ttu-id="e505b-129">location.</span><span class="sxs-lookup"><span data-stu-id="e505b-129">location.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e505b-130">-Name</span><span class="sxs-lookup"><span data-stu-id="e505b-130">-Name</span></span>
<span data-ttu-id="e505b-131">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="e505b-131">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e505b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e505b-132">-ResourceGroupName</span></span>
<span data-ttu-id="e505b-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e505b-133">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e505b-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e505b-134">-ResourceId</span></span>
<span data-ttu-id="e505b-135">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="e505b-135">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e505b-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="e505b-136">-Tag</span></span>
<span data-ttu-id="e505b-137">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="e505b-137">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e505b-138">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="e505b-138">-ThreatIntelMode</span></span>
<span data-ttu-id="e505b-139">O modo de operação para Inteligência de Ameaças.</span><span class="sxs-lookup"><span data-stu-id="e505b-139">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e505b-140">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="e505b-140">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="e505b-141">A lista branca para Inteligência de Ameaças</span><span class="sxs-lookup"><span data-stu-id="e505b-141">The whitelist for Threat Intelligence</span></span>

```yaml
Type: PSAzureFirewallPolicyThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e505b-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e505b-142">-Confirm</span></span>
<span data-ttu-id="e505b-143">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e505b-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e505b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e505b-144">-WhatIf</span></span>
<span data-ttu-id="e505b-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e505b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e505b-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e505b-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e505b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e505b-147">CommonParameters</span></span>
<span data-ttu-id="e505b-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e505b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e505b-149">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e505b-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e505b-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e505b-150">INPUTS</span></span>

### <span data-ttu-id="e505b-151">System.String</span><span class="sxs-lookup"><span data-stu-id="e505b-151">System.String</span></span>

### <span data-ttu-id="e505b-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e505b-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="e505b-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e505b-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e505b-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e505b-154">OUTPUTS</span></span>

### <span data-ttu-id="e505b-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="e505b-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="e505b-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="e505b-156">NOTES</span></span>

## <span data-ttu-id="e505b-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e505b-157">RELATED LINKS</span></span>
