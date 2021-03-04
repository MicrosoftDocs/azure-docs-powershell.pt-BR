---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyintrusiondetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetection.md
ms.openlocfilehash: 3587917e1a4216445e59b182ce6307c7a94684bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891164"
---
# <span data-ttu-id="5c065-101">New-AzFirewallPolicyIntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="5c065-101">New-AzFirewallPolicyIntrusionDetection</span></span>

## <span data-ttu-id="5c065-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c065-102">SYNOPSIS</span></span>
<span data-ttu-id="5c065-103">Cria uma nova Detecção de Invasão de Política de Firewall do Azure para associar à Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="5c065-103">Creates a new Azure Firewall Policy Intrusion Detection to associate with Firewall Policy</span></span>

## <span data-ttu-id="5c065-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5c065-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetection -Mode <String>
 [-SignatureOverride <PSAzureFirewallPolicyIntrusionDetectionSignatureOverride[]>]
 [-BypassTraffic <PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c065-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5c065-105">DESCRIPTION</span></span>
<span data-ttu-id="5c065-106">O cmdlet **New-AzFirewallPolicyIntrusionDetection** cria um Objeto de Detecção de Intrusão de Política de Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c065-106">The **New-AzFirewallPolicyIntrusionDetection** cmdlet creates an Azure Firewall Policy Intrusion Detection Object.</span></span>

## <span data-ttu-id="5c065-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5c065-107">EXAMPLES</span></span>

### <span data-ttu-id="5c065-108">Exemplo 1: 1.</span><span class="sxs-lookup"><span data-stu-id="5c065-108">Example 1: 1.</span></span> <span data-ttu-id="5c065-109">Criar detecção de intrusão com o modo</span><span class="sxs-lookup"><span data-stu-id="5c065-109">Create intrusion detection with mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert"
```

<span data-ttu-id="5c065-110">Este exemplo cria a detecção de intrusão com o modo Alerta (detecção)</span><span class="sxs-lookup"><span data-stu-id="5c065-110">This example creates intrusion detection with Alert (detection) mode</span></span>

### <span data-ttu-id="5c065-111">Exemplo 2: 2.</span><span class="sxs-lookup"><span data-stu-id="5c065-111">Example 2: 2.</span></span> <span data-ttu-id="5c065-112">Criar detecção de intrusão com substituições de assinatura</span><span class="sxs-lookup"><span data-stu-id="5c065-112">Create intrusion detection with signature overrides</span></span>
```powershell
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride
```

<span data-ttu-id="5c065-113">Este exemplo cria a detecção de intrusão com substituição de assinatura específica</span><span class="sxs-lookup"><span data-stu-id="5c065-113">This example creates intrusion detection with specific signature override</span></span>

### <span data-ttu-id="5c065-114">Exemplo 3: 3.</span><span class="sxs-lookup"><span data-stu-id="5c065-114">Example 3: 3.</span></span> <span data-ttu-id="5c065-115">Criar política de firewall com detecção de intrusão configurada com a configuração de tráfego de bypass</span><span class="sxs-lookup"><span data-stu-id="5c065-115">Create firewall policy with intrusion detection configured with bypass traffic setting</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "10.0.0.0"
PS C:\> $intrusionDetection = New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
PS C:\> New-AzFirewallPolicy -Name fp1 -Location "westus2" -ResourceGroup TestRg -SkuTier "Premium" -IntrusionDetection $intrusionDetection
```

<span data-ttu-id="5c065-116">Este exemplo cria a detecção de intrusão com a configuração de tráfego de bypass</span><span class="sxs-lookup"><span data-stu-id="5c065-116">This example creates intrusion detection with bypass traffic setting</span></span>

## <span data-ttu-id="5c065-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5c065-117">PARAMETERS</span></span>

### <span data-ttu-id="5c065-118">-BypassTraffic</span><span class="sxs-lookup"><span data-stu-id="5c065-118">-BypassTraffic</span></span>
<span data-ttu-id="5c065-119">Lista de regras para o tráfego ignorar.</span><span class="sxs-lookup"><span data-stu-id="5c065-119">List of rules for traffic to bypass.</span></span>

```yaml
Type: PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c065-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c065-120">-DefaultProfile</span></span>
<span data-ttu-id="5c065-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5c065-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c065-122">-Mode</span><span class="sxs-lookup"><span data-stu-id="5c065-122">-Mode</span></span>
<span data-ttu-id="5c065-123">Estado geral de Detecção de Intrusão.</span><span class="sxs-lookup"><span data-stu-id="5c065-123">Intrusion Detection general state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Off, Alert, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c065-124">-SignatureOverride</span><span class="sxs-lookup"><span data-stu-id="5c065-124">-SignatureOverride</span></span>
<span data-ttu-id="5c065-125">Lista de estados de assinaturas específicos.</span><span class="sxs-lookup"><span data-stu-id="5c065-125">List of specific signatures states.</span></span>

```yaml
Type: PSAzureFirewallPolicyIntrusionDetectionSignatureOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c065-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c065-126">-Confirm</span></span>
<span data-ttu-id="5c065-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c065-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c065-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c065-128">-WhatIf</span></span>
<span data-ttu-id="5c065-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5c065-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c065-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5c065-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c065-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c065-131">CommonParameters</span></span>
<span data-ttu-id="5c065-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c065-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c065-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c065-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c065-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c065-134">INPUTS</span></span>

### <span data-ttu-id="5c065-135">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5c065-135">None</span></span>

## <span data-ttu-id="5c065-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5c065-136">OUTPUTS</span></span>

### <span data-ttu-id="5c065-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="5c065-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetection</span></span>

## <span data-ttu-id="5c065-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="5c065-138">NOTES</span></span>

## <span data-ttu-id="5c065-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c065-139">RELATED LINKS</span></span>
