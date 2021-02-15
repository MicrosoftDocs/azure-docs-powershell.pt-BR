---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionbypasstraffic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
ms.openlocfilehash: c296c44c96d756dc0ca3a107d8eee265a9226b15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112837"
---
# <span data-ttu-id="08c90-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span><span class="sxs-lookup"><span data-stu-id="08c90-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span></span>

## <span data-ttu-id="08c90-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="08c90-102">SYNOPSIS</span></span>
<span data-ttu-id="08c90-103">Cria uma nova configuração de tráfego de detecção de invasão de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="08c90-103">Creates a new Azure Firewall Policy Intrusion Detection Bypass Traffic Setting</span></span>

## <span data-ttu-id="08c90-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08c90-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name <String> [-Description <String>] -Protocol <String>
 [-SourceAddress <String[]>] [-DestinationAddress <String[]>] [-SourceIpGroup <String[]>]
 [-DestinationIpGroup <String[]>] -DestinationPort <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08c90-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="08c90-105">DESCRIPTION</span></span>
<span data-ttu-id="08c90-106">O cmdlet **New-AzFirewallPolicyIntrusionDetectionBypassTraffic** cria um Objeto de Tráfego de Detecção de Invasão de Política de Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="08c90-106">The **New-AzFirewallPolicyIntrusionDetectionBypassTraffic** cmdlet creates an Azure Firewall Policy Intrusion Detection Bypass Traffic Object.</span></span>

## <span data-ttu-id="08c90-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="08c90-107">EXAMPLES</span></span>

### <span data-ttu-id="08c90-108">Exemplo 1: 1.</span><span class="sxs-lookup"><span data-stu-id="08c90-108">Example 1: 1.</span></span> <span data-ttu-id="08c90-109">Criar tráfego de bypass com porta e endereço de origem específicos</span><span class="sxs-lookup"><span data-stu-id="08c90-109">Create bypass traffic with specific port and source address</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "*"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
```

<span data-ttu-id="08c90-110">Este exemplo cria a detecção de invasão com a configuração de desvio de tráfego</span><span class="sxs-lookup"><span data-stu-id="08c90-110">This example creates intrusion detection with bypass traffic setting</span></span>

## <span data-ttu-id="08c90-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08c90-111">PARAMETERS</span></span>

### <span data-ttu-id="08c90-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08c90-112">-DefaultProfile</span></span>
<span data-ttu-id="08c90-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="08c90-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08c90-114">-Descrição</span><span class="sxs-lookup"><span data-stu-id="08c90-114">-Description</span></span>
<span data-ttu-id="08c90-115">Ignorar a descrição da configuração.</span><span class="sxs-lookup"><span data-stu-id="08c90-115">Bypass setting description.</span></span>

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

### <span data-ttu-id="08c90-116">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="08c90-116">-DestinationAddress</span></span>
<span data-ttu-id="08c90-117">Lista de intervalos ou endereços IP de destino.</span><span class="sxs-lookup"><span data-stu-id="08c90-117">List of destination IP addresses or ranges.</span></span>

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

### <span data-ttu-id="08c90-118">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="08c90-118">-DestinationIpGroup</span></span>
<span data-ttu-id="08c90-119">Lista de IpGroups de destino.</span><span class="sxs-lookup"><span data-stu-id="08c90-119">List of destination IpGroups.</span></span>

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

### <span data-ttu-id="08c90-120">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="08c90-120">-DestinationPort</span></span>
<span data-ttu-id="08c90-121">Lista de portas ou intervalos de destino.</span><span class="sxs-lookup"><span data-stu-id="08c90-121">List of destination ports or ranges.</span></span>

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

### <span data-ttu-id="08c90-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="08c90-122">-Name</span></span>
<span data-ttu-id="08c90-123">Ignorar o nome da configuração.</span><span class="sxs-lookup"><span data-stu-id="08c90-123">Bypass setting name.</span></span>

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

### <span data-ttu-id="08c90-124">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="08c90-124">-Protocol</span></span>
<span data-ttu-id="08c90-125">Ignorar o protocolo de configuração.</span><span class="sxs-lookup"><span data-stu-id="08c90-125">Bypass setting protocol.</span></span>

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

### <span data-ttu-id="08c90-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="08c90-126">-SourceAddress</span></span>
<span data-ttu-id="08c90-127">Lista de intervalos ou endereços IP de origem.</span><span class="sxs-lookup"><span data-stu-id="08c90-127">List of source IP addresses or ranges.</span></span>

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

### <span data-ttu-id="08c90-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="08c90-128">-SourceIpGroup</span></span>
<span data-ttu-id="08c90-129">Lista de IpGroups de origem.</span><span class="sxs-lookup"><span data-stu-id="08c90-129">List of source IpGroups.</span></span>

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

### <span data-ttu-id="08c90-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="08c90-130">-Confirm</span></span>
<span data-ttu-id="08c90-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08c90-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08c90-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08c90-132">-WhatIf</span></span>
<span data-ttu-id="08c90-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="08c90-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08c90-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="08c90-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08c90-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08c90-135">CommonParameters</span></span>
<span data-ttu-id="08c90-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08c90-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08c90-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08c90-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08c90-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="08c90-138">INPUTS</span></span>

### <span data-ttu-id="08c90-139">Nenhum</span><span class="sxs-lookup"><span data-stu-id="08c90-139">None</span></span>

## <span data-ttu-id="08c90-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="08c90-140">OUTPUTS</span></span>

### <span data-ttu-id="08c90-141">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span><span class="sxs-lookup"><span data-stu-id="08c90-141">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span></span>

## <span data-ttu-id="08c90-142">Notas</span><span class="sxs-lookup"><span data-stu-id="08c90-142">NOTES</span></span>

## <span data-ttu-id="08c90-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08c90-143">RELATED LINKS</span></span>
