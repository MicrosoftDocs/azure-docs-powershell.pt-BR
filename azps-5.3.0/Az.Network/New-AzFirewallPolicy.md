---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 17aea8ab38582373420107df87e2b6837a83a1a4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428971"
---
# <span data-ttu-id="bafa4-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="bafa4-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="bafa4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bafa4-102">SYNOPSIS</span></span>
<span data-ttu-id="bafa4-103">Cria uma nova política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="bafa4-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="bafa4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bafa4-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bafa4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bafa4-105">DESCRIPTION</span></span>
<span data-ttu-id="bafa4-106">O cmdlet **New-AzFirewallPolicy** cria uma política de firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="bafa4-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="bafa4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bafa4-107">EXAMPLES</span></span>

### <span data-ttu-id="bafa4-108">Exemplo 1:1.</span><span class="sxs-lookup"><span data-stu-id="bafa4-108">Example 1: 1.</span></span> <span data-ttu-id="bafa4-109">Criar uma política vazia</span><span class="sxs-lookup"><span data-stu-id="bafa4-109">Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="bafa4-110">Este exemplo cria uma política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="bafa4-110">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="bafa4-111">Exemplo 2:2.</span><span class="sxs-lookup"><span data-stu-id="bafa4-111">Example 2: 2.</span></span> <span data-ttu-id="bafa4-112">Criar uma política vazia com o modo ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="bafa4-112">Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="bafa4-113">Este exemplo cria uma política de firewall do Azure com um modo de ameaça Intel</span><span class="sxs-lookup"><span data-stu-id="bafa4-113">This example creates an azure firewall policy with a threat intel mode</span></span>

### <span data-ttu-id="bafa4-114">Exemplo 3:3.</span><span class="sxs-lookup"><span data-stu-id="bafa4-114">Example 3: 3.</span></span> <span data-ttu-id="bafa4-115">Criar uma política vazia com a lista branca do ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="bafa4-115">Create an empty policy with ThreatIntel Whitelist</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="bafa4-116">Este exemplo cria uma política de firewall do Azure com uma lista branca da Intel com ameaças</span><span class="sxs-lookup"><span data-stu-id="bafa4-116">This example creates an azure firewall policy with a threat intel whitelist</span></span>

## <span data-ttu-id="bafa4-117">OS</span><span class="sxs-lookup"><span data-stu-id="bafa4-117">PARAMETERS</span></span>

### <span data-ttu-id="bafa4-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bafa4-118">-AsJob</span></span>
<span data-ttu-id="bafa4-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bafa4-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bafa4-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="bafa4-120">-BasePolicy</span></span>
<span data-ttu-id="bafa4-121">A política base a ser herdada</span><span class="sxs-lookup"><span data-stu-id="bafa4-121">The base policy to inherit from</span></span>

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

### <span data-ttu-id="bafa4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bafa4-122">-DefaultProfile</span></span>
<span data-ttu-id="bafa4-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bafa4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bafa4-124">-Force</span><span class="sxs-lookup"><span data-stu-id="bafa4-124">-Force</span></span>
<span data-ttu-id="bafa4-125">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="bafa4-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="bafa4-126">-Local</span><span class="sxs-lookup"><span data-stu-id="bafa4-126">-Location</span></span>
<span data-ttu-id="bafa4-127">ponto.</span><span class="sxs-lookup"><span data-stu-id="bafa4-127">location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bafa4-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="bafa4-128">-Name</span></span>
<span data-ttu-id="bafa4-129">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="bafa4-129">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bafa4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bafa4-130">-ResourceGroupName</span></span>
<span data-ttu-id="bafa4-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bafa4-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bafa4-132">-Marca</span><span class="sxs-lookup"><span data-stu-id="bafa4-132">-Tag</span></span>
<span data-ttu-id="bafa4-133">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="bafa4-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="bafa4-134">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="bafa4-134">-ThreatIntelMode</span></span>
<span data-ttu-id="bafa4-135">O modo de operação para inteligência de ameaças.</span><span class="sxs-lookup"><span data-stu-id="bafa4-135">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="bafa4-136">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="bafa4-136">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="bafa4-137">A lista branca para inteligência de ameaças</span><span class="sxs-lookup"><span data-stu-id="bafa4-137">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="bafa4-138">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="bafa4-138">-DnsSetting</span></span>
<span data-ttu-id="bafa4-139">A configuração de DNS</span><span class="sxs-lookup"><span data-stu-id="bafa4-139">The DNS Setting</span></span>

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

### <span data-ttu-id="bafa4-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bafa4-140">-Confirm</span></span>
<span data-ttu-id="bafa4-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bafa4-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bafa4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bafa4-142">-WhatIf</span></span>
<span data-ttu-id="bafa4-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bafa4-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bafa4-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bafa4-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bafa4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bafa4-145">CommonParameters</span></span>
<span data-ttu-id="bafa4-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bafa4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bafa4-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bafa4-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bafa4-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bafa4-148">INPUTS</span></span>

### <span data-ttu-id="bafa4-149">System. String</span><span class="sxs-lookup"><span data-stu-id="bafa4-149">System.String</span></span>

### <span data-ttu-id="bafa4-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bafa4-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bafa4-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bafa4-151">OUTPUTS</span></span>

### <span data-ttu-id="bafa4-152">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="bafa4-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="bafa4-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bafa4-153">NOTES</span></span>

## <span data-ttu-id="bafa4-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bafa4-154">RELATED LINKS</span></span>
