---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionbypasstraffic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
ms.openlocfilehash: dd15a93fc2df022a0b016f9dae4845da13240534
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889098"
---
# <span data-ttu-id="02044-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span><span class="sxs-lookup"><span data-stu-id="02044-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span></span>

## <span data-ttu-id="02044-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02044-102">SYNOPSIS</span></span>
<span data-ttu-id="02044-103">Cria uma nova configuração de desvio de tráfego de detecção de intrusão de política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="02044-103">Creates a new Azure Firewall Policy Intrusion Detection Bypass Traffic Setting</span></span>

## <span data-ttu-id="02044-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="02044-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name <String> [-Description <String>] -Protocol <String>
 [-SourceAddress <String[]>] [-DestinationAddress <String[]>] [-SourceIpGroup <String[]>]
 [-DestinationIpGroup <String[]>] -DestinationPort <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02044-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="02044-105">DESCRIPTION</span></span>
<span data-ttu-id="02044-106">O cmdlet **New-AzFirewallPolicyIntrusionDetectionBypassTraffic** cria um objeto de tráfego de bypass de detecção de intrusão de política de firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="02044-106">The **New-AzFirewallPolicyIntrusionDetectionBypassTraffic** cmdlet creates an Azure Firewall Policy Intrusion Detection Bypass Traffic Object.</span></span>

## <span data-ttu-id="02044-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02044-107">EXAMPLES</span></span>

### <span data-ttu-id="02044-108">Exemplo 1: 1.</span><span class="sxs-lookup"><span data-stu-id="02044-108">Example 1: 1.</span></span> <span data-ttu-id="02044-109">Criar tráfego de bypass com endereço de origem e porta específicos</span><span class="sxs-lookup"><span data-stu-id="02044-109">Create bypass traffic with specific port and source address</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "*"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
```

<span data-ttu-id="02044-110">Este exemplo cria a detecção de intrusão com a configuração de tráfego de bypass</span><span class="sxs-lookup"><span data-stu-id="02044-110">This example creates intrusion detection with bypass traffic setting</span></span>

## <span data-ttu-id="02044-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="02044-111">PARAMETERS</span></span>

### <span data-ttu-id="02044-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02044-112">-DefaultProfile</span></span>
<span data-ttu-id="02044-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02044-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02044-114">-Description</span><span class="sxs-lookup"><span data-stu-id="02044-114">-Description</span></span>
<span data-ttu-id="02044-115">Ignorar a descrição da configuração.</span><span class="sxs-lookup"><span data-stu-id="02044-115">Bypass setting description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02044-116">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="02044-116">-DestinationAddress</span></span>
<span data-ttu-id="02044-117">Lista de endereços IP de destino ou intervalos.</span><span class="sxs-lookup"><span data-stu-id="02044-117">List of destination IP addresses or ranges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02044-118">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="02044-118">-DestinationIpGroup</span></span>
<span data-ttu-id="02044-119">Lista de IpGroups de destino.</span><span class="sxs-lookup"><span data-stu-id="02044-119">List of destination IpGroups.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02044-120">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="02044-120">-DestinationPort</span></span>
<span data-ttu-id="02044-121">Lista de portas de destino ou intervalos.</span><span class="sxs-lookup"><span data-stu-id="02044-121">List of destination ports or ranges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02044-122">-Name</span><span class="sxs-lookup"><span data-stu-id="02044-122">-Name</span></span>
<span data-ttu-id="02044-123">Nome da configuração bypass.</span><span class="sxs-lookup"><span data-stu-id="02044-123">Bypass setting name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02044-124">-Protocol</span><span class="sxs-lookup"><span data-stu-id="02044-124">-Protocol</span></span>
<span data-ttu-id="02044-125">Ignorar o protocolo de configuração.</span><span class="sxs-lookup"><span data-stu-id="02044-125">Bypass setting protocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: TCP, UDP, ICMP, ANY

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02044-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="02044-126">-SourceAddress</span></span>
<span data-ttu-id="02044-127">Lista de endereços IP de origem ou intervalos.</span><span class="sxs-lookup"><span data-stu-id="02044-127">List of source IP addresses or ranges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02044-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="02044-128">-SourceIpGroup</span></span>
<span data-ttu-id="02044-129">Lista de IpGroups de origem.</span><span class="sxs-lookup"><span data-stu-id="02044-129">List of source IpGroups.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02044-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02044-130">-Confirm</span></span>
<span data-ttu-id="02044-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02044-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02044-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02044-132">-WhatIf</span></span>
<span data-ttu-id="02044-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="02044-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02044-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="02044-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02044-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02044-135">CommonParameters</span></span>
<span data-ttu-id="02044-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02044-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02044-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02044-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02044-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02044-138">INPUTS</span></span>

### <span data-ttu-id="02044-139">Nenhum</span><span class="sxs-lookup"><span data-stu-id="02044-139">None</span></span>

## <span data-ttu-id="02044-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="02044-140">OUTPUTS</span></span>

### <span data-ttu-id="02044-141">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span><span class="sxs-lookup"><span data-stu-id="02044-141">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span></span>

## <span data-ttu-id="02044-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="02044-142">NOTES</span></span>

## <span data-ttu-id="02044-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02044-143">RELATED LINKS</span></span>
