---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 3cffe65b1b8e4ba811ee00b7537dc95d9d6dfb72
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114778"
---
# <span data-ttu-id="7966f-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="7966f-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="7966f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7966f-102">SYNOPSIS</span></span>
<span data-ttu-id="7966f-103">Salva uma política de firewall do Azure modificada</span><span class="sxs-lookup"><span data-stu-id="7966f-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="7966f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7966f-104">SYNTAX</span></span>

### <span data-ttu-id="7966f-105">SetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7966f-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7966f-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7966f-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Location <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7966f-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7966f-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7966f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7966f-108">DESCRIPTION</span></span>
<span data-ttu-id="7966f-109">O cmdlet **set-AzFirewallPolicy** atualiza uma política de firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="7966f-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="7966f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7966f-110">EXAMPLES</span></span>

### <span data-ttu-id="7966f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7966f-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="7966f-112">Este exemplo define a política de firewall com o novo valor de política de firewall</span><span class="sxs-lookup"><span data-stu-id="7966f-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="7966f-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7966f-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="7966f-114">Este exemplo define a política de firewall com o novo modo de ameaça Intel</span><span class="sxs-lookup"><span data-stu-id="7966f-114">This example sets the firewall policy with the new threat intel mode</span></span>

### <span data-ttu-id="7966f-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="7966f-115">Example 3</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="7966f-116">Este exemplo define a política de firewall com a nova lista branca da Intel Threat</span><span class="sxs-lookup"><span data-stu-id="7966f-116">This example sets the firewall policy with the new threat intel whitelist</span></span>

## <span data-ttu-id="7966f-117">OS</span><span class="sxs-lookup"><span data-stu-id="7966f-117">PARAMETERS</span></span>

### <span data-ttu-id="7966f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7966f-118">-AsJob</span></span>
<span data-ttu-id="7966f-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7966f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7966f-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="7966f-120">-BasePolicy</span></span>
<span data-ttu-id="7966f-121">A política base a ser herdada</span><span class="sxs-lookup"><span data-stu-id="7966f-121">The base policy to inherit from</span></span>

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

### <span data-ttu-id="7966f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7966f-122">-DefaultProfile</span></span>
<span data-ttu-id="7966f-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7966f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7966f-124">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="7966f-124">-DnsSetting</span></span>
<span data-ttu-id="7966f-125">A configuração de DNS</span><span class="sxs-lookup"><span data-stu-id="7966f-125">The DNS Setting</span></span>

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

### <span data-ttu-id="7966f-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7966f-126">-InputObject</span></span>
<span data-ttu-id="7966f-127">A política AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="7966f-127">The AzureFirewall Policy</span></span>

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

### <span data-ttu-id="7966f-128">-Local</span><span class="sxs-lookup"><span data-stu-id="7966f-128">-Location</span></span>
<span data-ttu-id="7966f-129">ponto.</span><span class="sxs-lookup"><span data-stu-id="7966f-129">location.</span></span>

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

### <span data-ttu-id="7966f-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="7966f-130">-Name</span></span>
<span data-ttu-id="7966f-131">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="7966f-131">The resource name.</span></span>

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

### <span data-ttu-id="7966f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7966f-132">-ResourceGroupName</span></span>
<span data-ttu-id="7966f-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7966f-133">The resource group name.</span></span>

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

### <span data-ttu-id="7966f-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7966f-134">-ResourceId</span></span>
<span data-ttu-id="7966f-135">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="7966f-135">The resource Id.</span></span>

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

### <span data-ttu-id="7966f-136">-Marca</span><span class="sxs-lookup"><span data-stu-id="7966f-136">-Tag</span></span>
<span data-ttu-id="7966f-137">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="7966f-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="7966f-138">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="7966f-138">-ThreatIntelMode</span></span>
<span data-ttu-id="7966f-139">O modo de operação para inteligência de ameaças.</span><span class="sxs-lookup"><span data-stu-id="7966f-139">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="7966f-140">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="7966f-140">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="7966f-141">A lista branca para inteligência de ameaças</span><span class="sxs-lookup"><span data-stu-id="7966f-141">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="7966f-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7966f-142">-Confirm</span></span>
<span data-ttu-id="7966f-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7966f-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7966f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7966f-144">-WhatIf</span></span>
<span data-ttu-id="7966f-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7966f-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7966f-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7966f-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7966f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7966f-147">CommonParameters</span></span>
<span data-ttu-id="7966f-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7966f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7966f-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7966f-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7966f-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7966f-150">INPUTS</span></span>

### <span data-ttu-id="7966f-151">System. String</span><span class="sxs-lookup"><span data-stu-id="7966f-151">System.String</span></span>

### <span data-ttu-id="7966f-152">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="7966f-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="7966f-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7966f-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7966f-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7966f-154">OUTPUTS</span></span>

### <span data-ttu-id="7966f-155">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="7966f-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="7966f-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7966f-156">NOTES</span></span>

## <span data-ttu-id="7966f-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7966f-157">RELATED LINKS</span></span>
