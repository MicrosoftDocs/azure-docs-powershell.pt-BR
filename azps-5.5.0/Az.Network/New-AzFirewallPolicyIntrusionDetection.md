---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyintrusiondetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetection.md
ms.openlocfilehash: bc3c71c8900be049dce7b00b698068e96ccc8519
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112838"
---
# <span data-ttu-id="9bc99-101">New-AzFirewallPolicyIntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="9bc99-101">New-AzFirewallPolicyIntrusionDetection</span></span>

## <span data-ttu-id="9bc99-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9bc99-102">SYNOPSIS</span></span>
<span data-ttu-id="9bc99-103">Cria uma nova Detecção de Invasão de Política de Firewall do Azure para associar à Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="9bc99-103">Creates a new Azure Firewall Policy Intrusion Detection to associate with Firewall Policy</span></span>

## <span data-ttu-id="9bc99-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9bc99-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetection -Mode <String>
 [-SignatureOverride <PSAzureFirewallPolicyIntrusionDetectionSignatureOverride[]>]
 [-BypassTraffic <PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bc99-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="9bc99-105">DESCRIPTION</span></span>
<span data-ttu-id="9bc99-106">O **cmdlet New-AzFirewallPolicyIntrusionDetection** cria um Objeto de Detecção de Invasão de Política de Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="9bc99-106">The **New-AzFirewallPolicyIntrusionDetection** cmdlet creates an Azure Firewall Policy Intrusion Detection Object.</span></span>

## <span data-ttu-id="9bc99-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9bc99-107">EXAMPLES</span></span>

### <span data-ttu-id="9bc99-108">Exemplo 1: 1.</span><span class="sxs-lookup"><span data-stu-id="9bc99-108">Example 1: 1.</span></span> <span data-ttu-id="9bc99-109">Criar detecção de invasão com o modo</span><span class="sxs-lookup"><span data-stu-id="9bc99-109">Create intrusion detection with mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert"
```

<span data-ttu-id="9bc99-110">Este exemplo cria a detecção de invasão com o modo alerta (detecção)</span><span class="sxs-lookup"><span data-stu-id="9bc99-110">This example creates intrusion detection with Alert (detection) mode</span></span>

### <span data-ttu-id="9bc99-111">Exemplo 2: 2.</span><span class="sxs-lookup"><span data-stu-id="9bc99-111">Example 2: 2.</span></span> <span data-ttu-id="9bc99-112">Criar detecção de invasão com substituições de assinatura</span><span class="sxs-lookup"><span data-stu-id="9bc99-112">Create intrusion detection with signature overrides</span></span>
```powershell
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride
```

<span data-ttu-id="9bc99-113">Este exemplo cria a detecção de invasão com substituição de assinatura específica</span><span class="sxs-lookup"><span data-stu-id="9bc99-113">This example creates intrusion detection with specific signature override</span></span>

### <span data-ttu-id="9bc99-114">Exemplo 3: 3.</span><span class="sxs-lookup"><span data-stu-id="9bc99-114">Example 3: 3.</span></span> <span data-ttu-id="9bc99-115">Criar política de firewall com detecção de invasão configurada com a configuração de ignorar tráfego</span><span class="sxs-lookup"><span data-stu-id="9bc99-115">Create firewall policy with intrusion detection configured with bypass traffic setting</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "10.0.0.0"
PS C:\> $intrusionDetection = New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
PS C:\> New-AzFirewallPolicy -Name fp1 -Location "westus2" -ResourceGroup TestRg -SkuTier "Premium" -IntrusionDetection $intrusionDetection
```

<span data-ttu-id="9bc99-116">Este exemplo cria a detecção de invasão com a configuração de desvio de tráfego</span><span class="sxs-lookup"><span data-stu-id="9bc99-116">This example creates intrusion detection with bypass traffic setting</span></span>

## <span data-ttu-id="9bc99-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9bc99-117">PARAMETERS</span></span>

### <span data-ttu-id="9bc99-118">-BypassTraffic</span><span class="sxs-lookup"><span data-stu-id="9bc99-118">-BypassTraffic</span></span>
<span data-ttu-id="9bc99-119">Lista de regras para o tráfego ignorar.</span><span class="sxs-lookup"><span data-stu-id="9bc99-119">List of rules for traffic to bypass.</span></span>

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

### <span data-ttu-id="9bc99-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bc99-120">-DefaultProfile</span></span>
<span data-ttu-id="9bc99-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9bc99-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bc99-122">-Modo</span><span class="sxs-lookup"><span data-stu-id="9bc99-122">-Mode</span></span>
<span data-ttu-id="9bc99-123">Estado geral de Detecção de Invasão.</span><span class="sxs-lookup"><span data-stu-id="9bc99-123">Intrusion Detection general state.</span></span>

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

### <span data-ttu-id="9bc99-124">-SignatureOverride</span><span class="sxs-lookup"><span data-stu-id="9bc99-124">-SignatureOverride</span></span>
<span data-ttu-id="9bc99-125">Lista de estados de assinaturas específicas.</span><span class="sxs-lookup"><span data-stu-id="9bc99-125">List of specific signatures states.</span></span>

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

### <span data-ttu-id="9bc99-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9bc99-126">-Confirm</span></span>
<span data-ttu-id="9bc99-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bc99-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bc99-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bc99-128">-WhatIf</span></span>
<span data-ttu-id="9bc99-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9bc99-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bc99-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9bc99-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bc99-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bc99-131">CommonParameters</span></span>
<span data-ttu-id="9bc99-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bc99-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bc99-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9bc99-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bc99-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="9bc99-134">INPUTS</span></span>

### <span data-ttu-id="9bc99-135">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9bc99-135">None</span></span>

## <span data-ttu-id="9bc99-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="9bc99-136">OUTPUTS</span></span>

### <span data-ttu-id="9bc99-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="9bc99-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetection</span></span>

## <span data-ttu-id="9bc99-138">Notas</span><span class="sxs-lookup"><span data-stu-id="9bc99-138">NOTES</span></span>

## <span data-ttu-id="9bc99-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9bc99-139">RELATED LINKS</span></span>
