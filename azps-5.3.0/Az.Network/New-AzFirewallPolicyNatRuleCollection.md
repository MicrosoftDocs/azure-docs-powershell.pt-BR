---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
ms.openlocfilehash: 010fd83d8b8e26e67e35afcc54b03ca0c1a5bd5a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428965"
---
# <span data-ttu-id="73417-101">New-AzFirewallPolicyNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="73417-101">New-AzFirewallPolicyNatRuleCollection</span></span>

## <span data-ttu-id="73417-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73417-102">SYNOPSIS</span></span>
<span data-ttu-id="73417-103">Criar uma nova coleção de regras de NAT da política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="73417-103">Create a new Azure Firewall Policy Nat Rule Collection</span></span>

## <span data-ttu-id="73417-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73417-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallPolicyNetworkRule> -ActionType <String> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73417-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="73417-105">DESCRIPTION</span></span>
<span data-ttu-id="73417-106">O cmdlet **New-AzFirewallPolicyNatRuleCollection** cria uma coleção de regras NAT para uma política de firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="73417-106">The **New-AzFirewallPolicyNatRuleCollection** cmdlet creates a Nat rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="73417-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73417-107">EXAMPLES</span></span>

### <span data-ttu-id="73417-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="73417-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRuleCollection -Name NatRule1 -Priority 200 -Rule $netRule1 -ActionType "Dnat" -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="73417-109">Este exemplo cria uma coleção de regras NAT com uma regra de rede</span><span class="sxs-lookup"><span data-stu-id="73417-109">This example creates a nat rule collection with a network rule</span></span>

## <span data-ttu-id="73417-110">OS</span><span class="sxs-lookup"><span data-stu-id="73417-110">PARAMETERS</span></span>

### <span data-ttu-id="73417-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="73417-111">-ActionType</span></span>
<span data-ttu-id="73417-112">O tipo da ação da regra</span><span class="sxs-lookup"><span data-stu-id="73417-112">The type of the rule action</span></span>

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

### <span data-ttu-id="73417-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73417-113">-DefaultProfile</span></span>
<span data-ttu-id="73417-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="73417-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73417-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="73417-115">-Name</span></span>
<span data-ttu-id="73417-116">O nome da coleção de regras de rede</span><span class="sxs-lookup"><span data-stu-id="73417-116">The name of the Network Rule Collection</span></span>

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

### <span data-ttu-id="73417-117">-Priority</span><span class="sxs-lookup"><span data-stu-id="73417-117">-Priority</span></span>
<span data-ttu-id="73417-118">A prioridade da coleção de regras</span><span class="sxs-lookup"><span data-stu-id="73417-118">The priority of the rule collection</span></span>

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

### <span data-ttu-id="73417-119">-Regra</span><span class="sxs-lookup"><span data-stu-id="73417-119">-Rule</span></span>
<span data-ttu-id="73417-120">A lista de regras de rede</span><span class="sxs-lookup"><span data-stu-id="73417-120">The list of network rules</span></span>

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

### <span data-ttu-id="73417-121">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="73417-121">-TranslatedAddress</span></span>
<span data-ttu-id="73417-122">O endereço traduzido para esta regra NAT</span><span class="sxs-lookup"><span data-stu-id="73417-122">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="73417-123">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="73417-123">-TranslatedPort</span></span>
<span data-ttu-id="73417-124">A porta traduzida para esta regra NAT</span><span class="sxs-lookup"><span data-stu-id="73417-124">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="73417-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="73417-125">-Confirm</span></span>
<span data-ttu-id="73417-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73417-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73417-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73417-127">-WhatIf</span></span>
<span data-ttu-id="73417-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="73417-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73417-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="73417-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73417-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73417-130">CommonParameters</span></span>
<span data-ttu-id="73417-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73417-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73417-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73417-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73417-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="73417-133">INPUTS</span></span>

### <span data-ttu-id="73417-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="73417-134">None</span></span>

## <span data-ttu-id="73417-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="73417-135">OUTPUTS</span></span>

### <span data-ttu-id="73417-136">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="73417-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="73417-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="73417-137">NOTES</span></span>

## <span data-ttu-id="73417-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73417-138">RELATED LINKS</span></span>
