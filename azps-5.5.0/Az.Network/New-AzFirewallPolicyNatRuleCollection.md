---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
ms.openlocfilehash: 010fd83d8b8e26e67e35afcc54b03ca0c1a5bd5a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118314"
---
# <span data-ttu-id="f43ae-101">New-AzFirewallPolicyNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f43ae-101">New-AzFirewallPolicyNatRuleCollection</span></span>

## <span data-ttu-id="f43ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f43ae-102">SYNOPSIS</span></span>
<span data-ttu-id="f43ae-103">Criar uma nova Coleção de Regras nat da Política de Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="f43ae-103">Create a new Azure Firewall Policy Nat Rule Collection</span></span>

## <span data-ttu-id="f43ae-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f43ae-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallPolicyNetworkRule> -ActionType <String> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f43ae-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f43ae-105">DESCRIPTION</span></span>
<span data-ttu-id="f43ae-106">O cmdlet **New-AzFirewallPolicyNatRuleCollection** cria um conjunto de regras Nat para uma Política de Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="f43ae-106">The **New-AzFirewallPolicyNatRuleCollection** cmdlet creates a Nat rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="f43ae-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f43ae-107">EXAMPLES</span></span>

### <span data-ttu-id="f43ae-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f43ae-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRuleCollection -Name NatRule1 -Priority 200 -Rule $netRule1 -ActionType "Dnat" -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="f43ae-109">Este exemplo cria uma coleção de regras nat com uma regra de rede</span><span class="sxs-lookup"><span data-stu-id="f43ae-109">This example creates a nat rule collection with a network rule</span></span>

## <span data-ttu-id="f43ae-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f43ae-110">PARAMETERS</span></span>

### <span data-ttu-id="f43ae-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="f43ae-111">-ActionType</span></span>
<span data-ttu-id="f43ae-112">O tipo da ação de regra</span><span class="sxs-lookup"><span data-stu-id="f43ae-112">The type of the rule action</span></span>

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

### <span data-ttu-id="f43ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f43ae-113">-DefaultProfile</span></span>
<span data-ttu-id="f43ae-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f43ae-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f43ae-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f43ae-115">-Name</span></span>
<span data-ttu-id="f43ae-116">O nome da Coleção de Regras de Rede</span><span class="sxs-lookup"><span data-stu-id="f43ae-116">The name of the Network Rule Collection</span></span>

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

### <span data-ttu-id="f43ae-117">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="f43ae-117">-Priority</span></span>
<span data-ttu-id="f43ae-118">A prioridade da coleção de regras</span><span class="sxs-lookup"><span data-stu-id="f43ae-118">The priority of the rule collection</span></span>

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

### <span data-ttu-id="f43ae-119">-Regra</span><span class="sxs-lookup"><span data-stu-id="f43ae-119">-Rule</span></span>
<span data-ttu-id="f43ae-120">A lista de regras de rede</span><span class="sxs-lookup"><span data-stu-id="f43ae-120">The list of network rules</span></span>

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

### <span data-ttu-id="f43ae-121">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="f43ae-121">-TranslatedAddress</span></span>
<span data-ttu-id="f43ae-122">O endereço traduzido para esta regra NAT</span><span class="sxs-lookup"><span data-stu-id="f43ae-122">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="f43ae-123">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="f43ae-123">-TranslatedPort</span></span>
<span data-ttu-id="f43ae-124">A porta traduzida para esta regra NAT</span><span class="sxs-lookup"><span data-stu-id="f43ae-124">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="f43ae-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f43ae-125">-Confirm</span></span>
<span data-ttu-id="f43ae-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f43ae-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f43ae-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f43ae-127">-WhatIf</span></span>
<span data-ttu-id="f43ae-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f43ae-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f43ae-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f43ae-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f43ae-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f43ae-130">CommonParameters</span></span>
<span data-ttu-id="f43ae-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f43ae-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f43ae-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f43ae-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f43ae-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="f43ae-133">INPUTS</span></span>

### <span data-ttu-id="f43ae-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f43ae-134">None</span></span>

## <span data-ttu-id="f43ae-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="f43ae-135">OUTPUTS</span></span>

### <span data-ttu-id="f43ae-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f43ae-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="f43ae-137">Notas</span><span class="sxs-lookup"><span data-stu-id="f43ae-137">NOTES</span></span>

## <span data-ttu-id="f43ae-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f43ae-138">RELATED LINKS</span></span>
