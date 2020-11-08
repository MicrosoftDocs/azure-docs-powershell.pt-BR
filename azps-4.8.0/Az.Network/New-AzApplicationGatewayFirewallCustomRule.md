---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcustomrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
ms.openlocfilehash: b25c25b642f8c912f62f75788e69e96c3ebdc73c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110533"
---
# <span data-ttu-id="4a6a6-101">New-AzApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="4a6a6-101">New-AzApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="4a6a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4a6a6-102">SYNOPSIS</span></span>
<span data-ttu-id="4a6a6-103">Cria uma nova regra personalizada para a política de firewall do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4a6a6-103">Creates a new custom rule for the application gateway firewall policy.</span></span>

## <span data-ttu-id="4a6a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a6a6-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCustomRule -Name <String> -Priority <Int32> -RuleType <String>
 -MatchCondition <PSApplicationGatewayFirewallCondition[]> -Action <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a6a6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4a6a6-105">DESCRIPTION</span></span>
<span data-ttu-id="4a6a6-106">O **New-AzApplicationGatewayFirewallCustomRule** cria uma regra personalizada para a política de firewall.</span><span class="sxs-lookup"><span data-stu-id="4a6a6-106">The **New-AzApplicationGatewayFirewallCustomRule** creates a custom rule for firewall policy.</span></span>

## <span data-ttu-id="4a6a6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a6a6-107">EXAMPLES</span></span>

### <span data-ttu-id="4a6a6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4a6a6-108">Example 1</span></span>
```powershell
PS C:\> $customRule = New-AzApplicationGatewayFirewallCustomRule -Name example-rule -Priority 1 -RuleType MatchRule -MatchCondition $condtion -Action Allow
```

<span data-ttu-id="4a6a6-109">O comando cria uma nova regra personalizada com nome do exemplo-regra, prioridade 1 e o tipo de regra será MatchRule com a condição definida na variável de condição, a ação será permitida.</span><span class="sxs-lookup"><span data-stu-id="4a6a6-109">The command creates a new custom rule with name of example-rule, priority 1 and the rule type will be MatchRule with condition defined in the condition variable, the action will the allow.</span></span> <span data-ttu-id="4a6a6-110">A nova regra personalizada de correspondência é salva em $customRule.</span><span class="sxs-lookup"><span data-stu-id="4a6a6-110">The new match custom rule is saved in $customRule.</span></span>

## <span data-ttu-id="4a6a6-111">OS</span><span class="sxs-lookup"><span data-stu-id="4a6a6-111">PARAMETERS</span></span>

### <span data-ttu-id="4a6a6-112">-Ação</span><span class="sxs-lookup"><span data-stu-id="4a6a6-112">-Action</span></span>
<span data-ttu-id="4a6a6-113">Tipo de ações.</span><span class="sxs-lookup"><span data-stu-id="4a6a6-113">Type of Actions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6a6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a6a6-114">-DefaultProfile</span></span>
<span data-ttu-id="4a6a6-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4a6a6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a6a6-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="4a6a6-116">-MatchCondition</span></span>
<span data-ttu-id="4a6a6-117">Lista de condições de correspondência.</span><span class="sxs-lookup"><span data-stu-id="4a6a6-117">List of match conditions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6a6-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a6a6-118">-Name</span></span>
<span data-ttu-id="4a6a6-119">O nome da regra.</span><span class="sxs-lookup"><span data-stu-id="4a6a6-119">The Name of the Rule.</span></span>

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

### <span data-ttu-id="4a6a6-120">-Priority</span><span class="sxs-lookup"><span data-stu-id="4a6a6-120">-Priority</span></span>
<span data-ttu-id="4a6a6-121">Descreve a prioridade da regra.</span><span class="sxs-lookup"><span data-stu-id="4a6a6-121">Describes priority of the rule.</span></span>
<span data-ttu-id="4a6a6-122">As regras com um valor menor serão avaliadas antes das regras com um valor mais alto.</span><span class="sxs-lookup"><span data-stu-id="4a6a6-122">Rules with a lower value will be evaluated before rules with a higher value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6a6-123">-RuleType</span><span class="sxs-lookup"><span data-stu-id="4a6a6-123">-RuleType</span></span>
<span data-ttu-id="4a6a6-124">Descreve o tipo de regra.</span><span class="sxs-lookup"><span data-stu-id="4a6a6-124">Describes type of rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MatchRule

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6a6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a6a6-125">CommonParameters</span></span>
<span data-ttu-id="4a6a6-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a6a6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a6a6-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a6a6-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a6a6-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4a6a6-128">INPUTS</span></span>

### <span data-ttu-id="4a6a6-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4a6a6-129">None</span></span>

## <span data-ttu-id="4a6a6-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4a6a6-130">OUTPUTS</span></span>

### <span data-ttu-id="4a6a6-131">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="4a6a6-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="4a6a6-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4a6a6-132">NOTES</span></span>

## <span data-ttu-id="4a6a6-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a6a6-133">RELATED LINKS</span></span>
