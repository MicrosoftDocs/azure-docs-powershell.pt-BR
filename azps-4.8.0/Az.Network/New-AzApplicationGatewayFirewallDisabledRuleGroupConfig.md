---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5eafcfc825b710e31954e247e4114d0f90e97c41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113029"
---
# <span data-ttu-id="6810f-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="6810f-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="6810f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6810f-102">SYNOPSIS</span></span>
<span data-ttu-id="6810f-103">Cria uma nova configuração de grupo de regras desabilitada.</span><span class="sxs-lookup"><span data-stu-id="6810f-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="6810f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6810f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String> [-Rules <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6810f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6810f-105">DESCRIPTION</span></span>
<span data-ttu-id="6810f-106">O cmdlet **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cria uma nova configuração de grupo de regras desabilitada.</span><span class="sxs-lookup"><span data-stu-id="6810f-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="6810f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6810f-107">EXAMPLES</span></span>

### <span data-ttu-id="6810f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6810f-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="6810f-109">O comando cria uma nova configuração de grupo de regras desabilitada para o grupo de regras chamado "REQUEST-942-APPLICATION-ATTACK-SQLI" com a regra 942130 e a regra 942140 sendo desabilitada.</span><span class="sxs-lookup"><span data-stu-id="6810f-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="6810f-110">A nova configuração do grupo de regras desabilitadas é salva no $disabledRuleGroup 1.</span><span class="sxs-lookup"><span data-stu-id="6810f-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="6810f-111">OS</span><span class="sxs-lookup"><span data-stu-id="6810f-111">PARAMETERS</span></span>

### <span data-ttu-id="6810f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6810f-112">-DefaultProfile</span></span>
<span data-ttu-id="6810f-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6810f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6810f-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="6810f-114">-RuleGroupName</span></span>
<span data-ttu-id="6810f-115">O nome do grupo de regras que será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="6810f-115">The name of the rule group that will be disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6810f-116">-Regras</span><span class="sxs-lookup"><span data-stu-id="6810f-116">-Rules</span></span>
<span data-ttu-id="6810f-117">A lista de regras que será desabilitada.</span><span class="sxs-lookup"><span data-stu-id="6810f-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="6810f-118">Se for nulo, todas as regras do grupo de regras serão desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="6810f-118">If null, all rules of the rule group will be disabled.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6810f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6810f-119">CommonParameters</span></span>
<span data-ttu-id="6810f-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6810f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6810f-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6810f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6810f-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6810f-122">INPUTS</span></span>

### <span data-ttu-id="6810f-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6810f-123">None</span></span>

## <span data-ttu-id="6810f-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6810f-124">OUTPUTS</span></span>

### <span data-ttu-id="6810f-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="6810f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="6810f-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6810f-126">NOTES</span></span>

## <span data-ttu-id="6810f-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6810f-127">RELATED LINKS</span></span>

[<span data-ttu-id="6810f-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="6810f-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="6810f-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="6810f-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

