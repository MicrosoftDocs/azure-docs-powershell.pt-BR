---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicydnssetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
ms.openlocfilehash: 137c12a8de58c5daa8fbd3f997aa6fd8f3e04caa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113483"
---
# <span data-ttu-id="287c3-101">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="287c3-101">New-AzFirewallPolicyDnsSetting</span></span>

## <span data-ttu-id="287c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="287c3-102">SYNOPSIS</span></span>
<span data-ttu-id="287c3-103">Cria uma nova Configuração DNS para a Política de Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="287c3-103">Creates a new DNS Setting for Azure Firewall Policy</span></span>

## <span data-ttu-id="287c3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="287c3-104">SYNTAX</span></span>

```
New-AzFirewallPolicyDnsSetting [-EnableProxy] [-Server <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="287c3-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="287c3-105">DESCRIPTION</span></span>
<span data-ttu-id="287c3-106">O cmdlet **New-AzFirewallPolicyDnsSetting** cria um Objeto de Configuração de DNS para a Política de Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="287c3-106">The **New-AzFirewallPolicyDnsSetting** cmdlet creates a DNS Setting Object for Azure Firewall Policy</span></span>

## <span data-ttu-id="287c3-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="287c3-107">EXAMPLES</span></span>

### <span data-ttu-id="287c3-108">1. Criar uma política vazia</span><span class="sxs-lookup"><span data-stu-id="287c3-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy
```

<span data-ttu-id="287c3-109">Este exemplo cria um objeto de Configuração dns com a configuração habilitando o proxy dns.</span><span class="sxs-lookup"><span data-stu-id="287c3-109">This example creates a dns Setting object with setting enabling dns proxy.</span></span>

### <span data-ttu-id="287c3-110">2. Criar uma política vazia com o Modo ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="287c3-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> $dnsServers = @("10.10.10.1", "20.20.20.2")
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy -Server $dnsServers
```

<span data-ttu-id="287c3-111">Este exemplo cria um objeto de Configuração dns com a configuração de proxy dns e configuração de servidores dns personalizados.</span><span class="sxs-lookup"><span data-stu-id="287c3-111">This example creates a dns Setting object with setting enabling dns proxy and setting custom dns servers.</span></span>

## <span data-ttu-id="287c3-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="287c3-112">PARAMETERS</span></span>

### <span data-ttu-id="287c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="287c3-113">-DefaultProfile</span></span>
<span data-ttu-id="287c3-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="287c3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="287c3-115">-EnableProxy</span><span class="sxs-lookup"><span data-stu-id="287c3-115">-EnableProxy</span></span>
<span data-ttu-id="287c3-116">Habilitar Proxy DNS.</span><span class="sxs-lookup"><span data-stu-id="287c3-116">Enable DNS Proxy.</span></span>
<span data-ttu-id="287c3-117">Por padrão, ela está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="287c3-117">By default it is disabled.</span></span>

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

### <span data-ttu-id="287c3-118">-Server</span><span class="sxs-lookup"><span data-stu-id="287c3-118">-Server</span></span>
<span data-ttu-id="287c3-119">A lista de servidores DNS</span><span class="sxs-lookup"><span data-stu-id="287c3-119">The list of DNS Servers</span></span>

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

### <span data-ttu-id="287c3-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="287c3-120">-Confirm</span></span>
<span data-ttu-id="287c3-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="287c3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="287c3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="287c3-122">-WhatIf</span></span>
<span data-ttu-id="287c3-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="287c3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="287c3-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="287c3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="287c3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="287c3-125">CommonParameters</span></span>
<span data-ttu-id="287c3-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="287c3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="287c3-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="287c3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="287c3-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="287c3-128">INPUTS</span></span>

### <span data-ttu-id="287c3-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="287c3-129">None</span></span>

## <span data-ttu-id="287c3-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="287c3-130">OUTPUTS</span></span>

### <span data-ttu-id="287c3-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span><span class="sxs-lookup"><span data-stu-id="287c3-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span></span>

## <span data-ttu-id="287c3-132">Notas</span><span class="sxs-lookup"><span data-stu-id="287c3-132">NOTES</span></span>

## <span data-ttu-id="287c3-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="287c3-133">RELATED LINKS</span></span>
