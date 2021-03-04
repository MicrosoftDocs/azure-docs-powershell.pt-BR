---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicynatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
ms.openlocfilehash: 4dd93dec5aad6fe0e77e92e44884c687d5841e49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886437"
---
# <span data-ttu-id="e14fe-101">New-AzFirewallPolicyNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="e14fe-101">New-AzFirewallPolicyNatRuleCollection</span></span>

## <span data-ttu-id="e14fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e14fe-102">SYNOPSIS</span></span>
<span data-ttu-id="e14fe-103">Criar uma nova coleção de regras nat da política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="e14fe-103">Create a new Azure Firewall Policy Nat Rule Collection</span></span>

## <span data-ttu-id="e14fe-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e14fe-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallPolicyNetworkRule> -ActionType <String> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e14fe-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e14fe-105">DESCRIPTION</span></span>
<span data-ttu-id="e14fe-106">O cmdlet **New-AzFirewallPolicyNatRuleCollection** cria uma coleção de regras Nat para uma Política de Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="e14fe-106">The **New-AzFirewallPolicyNatRuleCollection** cmdlet creates a Nat rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="e14fe-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e14fe-107">EXAMPLES</span></span>

### <span data-ttu-id="e14fe-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e14fe-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRuleCollection -Name NatRule1 -Priority 200 -Rule $netRule1 -ActionType "Dnat" -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="e14fe-109">Este exemplo cria uma coleção de regras nat com uma regra de rede</span><span class="sxs-lookup"><span data-stu-id="e14fe-109">This example creates a nat rule collection with a network rule</span></span>

## <span data-ttu-id="e14fe-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e14fe-110">PARAMETERS</span></span>

### <span data-ttu-id="e14fe-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="e14fe-111">-ActionType</span></span>
<span data-ttu-id="e14fe-112">O tipo da ação de regra</span><span class="sxs-lookup"><span data-stu-id="e14fe-112">The type of the rule action</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Dnat

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e14fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e14fe-113">-DefaultProfile</span></span>
<span data-ttu-id="e14fe-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e14fe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e14fe-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e14fe-115">-Name</span></span>
<span data-ttu-id="e14fe-116">O nome da coleção de regras de rede</span><span class="sxs-lookup"><span data-stu-id="e14fe-116">The name of the Network Rule Collection</span></span>

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

### <span data-ttu-id="e14fe-117">-Priority</span><span class="sxs-lookup"><span data-stu-id="e14fe-117">-Priority</span></span>
<span data-ttu-id="e14fe-118">A prioridade da coleção de regras</span><span class="sxs-lookup"><span data-stu-id="e14fe-118">The priority of the rule collection</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e14fe-119">-Rule</span><span class="sxs-lookup"><span data-stu-id="e14fe-119">-Rule</span></span>
<span data-ttu-id="e14fe-120">A lista de regras de rede</span><span class="sxs-lookup"><span data-stu-id="e14fe-120">The list of network rules</span></span>

```yaml
Type: PSAzureFirewallPolicyNetworkRule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e14fe-121">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="e14fe-121">-TranslatedAddress</span></span>
<span data-ttu-id="e14fe-122">O endereço convertido para esta regra NAT</span><span class="sxs-lookup"><span data-stu-id="e14fe-122">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="e14fe-123">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="e14fe-123">-TranslatedPort</span></span>
<span data-ttu-id="e14fe-124">A porta traduzida para esta regra NAT</span><span class="sxs-lookup"><span data-stu-id="e14fe-124">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="e14fe-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e14fe-125">-Confirm</span></span>
<span data-ttu-id="e14fe-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e14fe-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e14fe-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e14fe-127">-WhatIf</span></span>
<span data-ttu-id="e14fe-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e14fe-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e14fe-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e14fe-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e14fe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e14fe-130">CommonParameters</span></span>
<span data-ttu-id="e14fe-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e14fe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e14fe-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e14fe-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e14fe-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e14fe-133">INPUTS</span></span>

### <span data-ttu-id="e14fe-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e14fe-134">None</span></span>

## <span data-ttu-id="e14fe-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e14fe-135">OUTPUTS</span></span>

### <span data-ttu-id="e14fe-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="e14fe-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="e14fe-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="e14fe-137">NOTES</span></span>

## <span data-ttu-id="e14fe-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e14fe-138">RELATED LINKS</span></span>
