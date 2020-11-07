---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
ms.openlocfilehash: 4e62a6c8820f9a9e6465c74746d589b343d99898
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785677"
---
# <span data-ttu-id="7d1c5-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="7d1c5-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="7d1c5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7d1c5-102">SYNOPSIS</span></span>
<span data-ttu-id="7d1c5-103">Cria uma nova configuração de grupo de regras desabilitada.</span><span class="sxs-lookup"><span data-stu-id="7d1c5-103">Creates a new disabled rule group configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d1c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d1c5-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String>
 [-Rules <System.Collections.Generic.List`1[System.Int32]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d1c5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7d1c5-105">DESCRIPTION</span></span>
<span data-ttu-id="7d1c5-106">O cmdlet **New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** cria uma nova configuração de grupo de regras desabilitada.</span><span class="sxs-lookup"><span data-stu-id="7d1c5-106">The **New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="7d1c5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7d1c5-107">EXAMPLES</span></span>

### <span data-ttu-id="7d1c5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7d1c5-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="7d1c5-109">O comando cria uma nova configuração de grupo de regras desabilitada para o grupo de regras chamado "REQUEST-942-APPLICATION-ATTACK-SQLI" com a regra 942130 e a regra 942140 sendo desabilitada.</span><span class="sxs-lookup"><span data-stu-id="7d1c5-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="7d1c5-110">A nova configuração do grupo de regras desabilitadas é salva no $disabledRuleGroup 1.</span><span class="sxs-lookup"><span data-stu-id="7d1c5-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="7d1c5-111">OS</span><span class="sxs-lookup"><span data-stu-id="7d1c5-111">PARAMETERS</span></span>

### <span data-ttu-id="7d1c5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d1c5-112">-DefaultProfile</span></span>
<span data-ttu-id="7d1c5-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7d1c5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1c5-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="7d1c5-114">-RuleGroupName</span></span>
<span data-ttu-id="7d1c5-115">O nome do grupo de regras que será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="7d1c5-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="7d1c5-116">-Regras</span><span class="sxs-lookup"><span data-stu-id="7d1c5-116">-Rules</span></span>
<span data-ttu-id="7d1c5-117">A lista de regras que será desabilitada.</span><span class="sxs-lookup"><span data-stu-id="7d1c5-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="7d1c5-118">Se for nulo, todas as regras do grupo de regras serão desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="7d1c5-118">If null, all rules of the rule group will be disabled.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1c5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d1c5-119">CommonParameters</span></span>
<span data-ttu-id="7d1c5-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d1c5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d1c5-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d1c5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d1c5-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7d1c5-122">INPUTS</span></span>

### <span data-ttu-id="7d1c5-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7d1c5-123">None</span></span>

## <span data-ttu-id="7d1c5-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7d1c5-124">OUTPUTS</span></span>

### <span data-ttu-id="7d1c5-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="7d1c5-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="7d1c5-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7d1c5-126">NOTES</span></span>

## <span data-ttu-id="7d1c5-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d1c5-127">RELATED LINKS</span></span>

[<span data-ttu-id="7d1c5-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d1c5-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="7d1c5-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d1c5-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

