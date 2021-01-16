---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicydnssetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
ms.openlocfilehash: 137c12a8de58c5daa8fbd3f997aa6fd8f3e04caa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262842"
---
# <span data-ttu-id="05ef5-101">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="05ef5-101">New-AzFirewallPolicyDnsSetting</span></span>

## <span data-ttu-id="05ef5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="05ef5-102">SYNOPSIS</span></span>
<span data-ttu-id="05ef5-103">Cria uma nova configuração de DNS para a política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="05ef5-103">Creates a new DNS Setting for Azure Firewall Policy</span></span>

## <span data-ttu-id="05ef5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05ef5-104">SYNTAX</span></span>

```
New-AzFirewallPolicyDnsSetting [-EnableProxy] [-Server <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05ef5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="05ef5-105">DESCRIPTION</span></span>
<span data-ttu-id="05ef5-106">O cmdlet **New-AzFirewallPolicyDnsSetting** cria um objeto de configuração de DNS para a política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="05ef5-106">The **New-AzFirewallPolicyDnsSetting** cmdlet creates a DNS Setting Object for Azure Firewall Policy</span></span>

## <span data-ttu-id="05ef5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="05ef5-107">EXAMPLES</span></span>

### <span data-ttu-id="05ef5-108">1. criar uma política vazia</span><span class="sxs-lookup"><span data-stu-id="05ef5-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy
```

<span data-ttu-id="05ef5-109">Este exemplo cria um objeto de configuração de DNS com a configuração habilitando o proxy DNS.</span><span class="sxs-lookup"><span data-stu-id="05ef5-109">This example creates a dns Setting object with setting enabling dns proxy.</span></span>

### <span data-ttu-id="05ef5-110">2. criar uma política vazia com o modo ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="05ef5-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> $dnsServers = @("10.10.10.1", "20.20.20.2")
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy -Server $dnsServers
```

<span data-ttu-id="05ef5-111">Este exemplo cria um objeto de configuração de DNS com a configuração habilitando o proxy DNS e definindo servidores DNS personalizados.</span><span class="sxs-lookup"><span data-stu-id="05ef5-111">This example creates a dns Setting object with setting enabling dns proxy and setting custom dns servers.</span></span>

## <span data-ttu-id="05ef5-112">OS</span><span class="sxs-lookup"><span data-stu-id="05ef5-112">PARAMETERS</span></span>

### <span data-ttu-id="05ef5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05ef5-113">-DefaultProfile</span></span>
<span data-ttu-id="05ef5-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="05ef5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05ef5-115">-EnableProxy</span><span class="sxs-lookup"><span data-stu-id="05ef5-115">-EnableProxy</span></span>
<span data-ttu-id="05ef5-116">Habilite o proxy de DNS.</span><span class="sxs-lookup"><span data-stu-id="05ef5-116">Enable DNS Proxy.</span></span>
<span data-ttu-id="05ef5-117">Por padrão, ele é desabilitado.</span><span class="sxs-lookup"><span data-stu-id="05ef5-117">By default it is disabled.</span></span>

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

### <span data-ttu-id="05ef5-118">-Servidor</span><span class="sxs-lookup"><span data-stu-id="05ef5-118">-Server</span></span>
<span data-ttu-id="05ef5-119">A lista de servidores DNS</span><span class="sxs-lookup"><span data-stu-id="05ef5-119">The list of DNS Servers</span></span>

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

### <span data-ttu-id="05ef5-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="05ef5-120">-Confirm</span></span>
<span data-ttu-id="05ef5-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05ef5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05ef5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05ef5-122">-WhatIf</span></span>
<span data-ttu-id="05ef5-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="05ef5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05ef5-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="05ef5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05ef5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05ef5-125">CommonParameters</span></span>
<span data-ttu-id="05ef5-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05ef5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05ef5-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05ef5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05ef5-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="05ef5-128">INPUTS</span></span>

### <span data-ttu-id="05ef5-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="05ef5-129">None</span></span>

## <span data-ttu-id="05ef5-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="05ef5-130">OUTPUTS</span></span>

### <span data-ttu-id="05ef5-131">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyDnsSettings</span><span class="sxs-lookup"><span data-stu-id="05ef5-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span></span>

## <span data-ttu-id="05ef5-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="05ef5-132">NOTES</span></span>

## <span data-ttu-id="05ef5-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05ef5-133">RELATED LINKS</span></span>
