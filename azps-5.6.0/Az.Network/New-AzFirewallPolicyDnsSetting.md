---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicydnssetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
ms.openlocfilehash: 35b56e6aafe73c09343fb17d385dd7ab4c705c5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889632"
---
# <span data-ttu-id="7cd71-101">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="7cd71-101">New-AzFirewallPolicyDnsSetting</span></span>

## <span data-ttu-id="7cd71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cd71-102">SYNOPSIS</span></span>
<span data-ttu-id="7cd71-103">Cria uma nova configuração DNS para a Política de Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="7cd71-103">Creates a new DNS Setting for Azure Firewall Policy</span></span>

## <span data-ttu-id="7cd71-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7cd71-104">SYNTAX</span></span>

```
New-AzFirewallPolicyDnsSetting [-EnableProxy] [-Server <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cd71-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7cd71-105">DESCRIPTION</span></span>
<span data-ttu-id="7cd71-106">O cmdlet **New-AzFirewallPolicyDnsSetting** cria um objeto de configuração DNS para a Política de Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="7cd71-106">The **New-AzFirewallPolicyDnsSetting** cmdlet creates a DNS Setting Object for Azure Firewall Policy</span></span>

## <span data-ttu-id="7cd71-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7cd71-107">EXAMPLES</span></span>

### <span data-ttu-id="7cd71-108">1. Criar uma política vazia</span><span class="sxs-lookup"><span data-stu-id="7cd71-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy
```

<span data-ttu-id="7cd71-109">Este exemplo cria um objeto De configuração dns com a configuração habilitando o proxy dns.</span><span class="sxs-lookup"><span data-stu-id="7cd71-109">This example creates a dns Setting object with setting enabling dns proxy.</span></span>

### <span data-ttu-id="7cd71-110">2. Criar uma política vazia com o Modo ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="7cd71-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> $dnsServers = @("10.10.10.1", "20.20.20.2")
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy -Server $dnsServers
```

<span data-ttu-id="7cd71-111">Este exemplo cria um objeto De configuração dns com a configuração habilitando o proxy dns e definindo servidores dns personalizados.</span><span class="sxs-lookup"><span data-stu-id="7cd71-111">This example creates a dns Setting object with setting enabling dns proxy and setting custom dns servers.</span></span>

## <span data-ttu-id="7cd71-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7cd71-112">PARAMETERS</span></span>

### <span data-ttu-id="7cd71-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cd71-113">-DefaultProfile</span></span>
<span data-ttu-id="7cd71-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7cd71-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cd71-115">-EnableProxy</span><span class="sxs-lookup"><span data-stu-id="7cd71-115">-EnableProxy</span></span>
<span data-ttu-id="7cd71-116">Habilitar Proxy DNS.</span><span class="sxs-lookup"><span data-stu-id="7cd71-116">Enable DNS Proxy.</span></span>
<span data-ttu-id="7cd71-117">Por padrão, ele está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="7cd71-117">By default it is disabled.</span></span>

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

### <span data-ttu-id="7cd71-118">-Server</span><span class="sxs-lookup"><span data-stu-id="7cd71-118">-Server</span></span>
<span data-ttu-id="7cd71-119">A lista de servidores DNS</span><span class="sxs-lookup"><span data-stu-id="7cd71-119">The list of DNS Servers</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd71-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cd71-120">-Confirm</span></span>
<span data-ttu-id="7cd71-121">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cd71-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cd71-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cd71-122">-WhatIf</span></span>
<span data-ttu-id="7cd71-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7cd71-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cd71-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7cd71-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cd71-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cd71-125">CommonParameters</span></span>
<span data-ttu-id="7cd71-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cd71-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cd71-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7cd71-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cd71-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7cd71-128">INPUTS</span></span>

### <span data-ttu-id="7cd71-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7cd71-129">None</span></span>

## <span data-ttu-id="7cd71-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7cd71-130">OUTPUTS</span></span>

### <span data-ttu-id="7cd71-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span><span class="sxs-lookup"><span data-stu-id="7cd71-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span></span>

## <span data-ttu-id="7cd71-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="7cd71-132">NOTES</span></span>

## <span data-ttu-id="7cd71-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7cd71-133">RELATED LINKS</span></span>
