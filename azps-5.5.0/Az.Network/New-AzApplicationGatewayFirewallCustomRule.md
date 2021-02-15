---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcustomrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
ms.openlocfilehash: b25c25b642f8c912f62f75788e69e96c3ebdc73c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111665"
---
# <span data-ttu-id="892df-101">New-AzApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="892df-101">New-AzApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="892df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="892df-102">SYNOPSIS</span></span>
<span data-ttu-id="892df-103">Cria uma nova regra personalizada para a política de firewall do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="892df-103">Creates a new custom rule for the application gateway firewall policy.</span></span>

## <span data-ttu-id="892df-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="892df-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCustomRule -Name <String> -Priority <Int32> -RuleType <String>
 -MatchCondition <PSApplicationGatewayFirewallCondition[]> -Action <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="892df-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="892df-105">DESCRIPTION</span></span>
<span data-ttu-id="892df-106">O **New-AzApplicationGatewayFirewallCustomRule** cria uma regra personalizada para a política de firewall.</span><span class="sxs-lookup"><span data-stu-id="892df-106">The **New-AzApplicationGatewayFirewallCustomRule** creates a custom rule for firewall policy.</span></span>

## <span data-ttu-id="892df-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="892df-107">EXAMPLES</span></span>

### <span data-ttu-id="892df-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="892df-108">Example 1</span></span>
```powershell
PS C:\> $customRule = New-AzApplicationGatewayFirewallCustomRule -Name example-rule -Priority 1 -RuleType MatchRule -MatchCondition $condtion -Action Allow
```

<span data-ttu-id="892df-109">O comando cria uma nova regra personalizada com o nome da regra de exemplo, prioridade 1 e o tipo de regra será MatchRule com condição definida na variável de condição, a ação permitirá.</span><span class="sxs-lookup"><span data-stu-id="892df-109">The command creates a new custom rule with name of example-rule, priority 1 and the rule type will be MatchRule with condition defined in the condition variable, the action will the allow.</span></span> <span data-ttu-id="892df-110">A nova regra personalizada de combinação é salva $customRule.</span><span class="sxs-lookup"><span data-stu-id="892df-110">The new match custom rule is saved in $customRule.</span></span>

## <span data-ttu-id="892df-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="892df-111">PARAMETERS</span></span>

### <span data-ttu-id="892df-112">-Ação</span><span class="sxs-lookup"><span data-stu-id="892df-112">-Action</span></span>
<span data-ttu-id="892df-113">Tipo de Ações.</span><span class="sxs-lookup"><span data-stu-id="892df-113">Type of Actions.</span></span>

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

### <span data-ttu-id="892df-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="892df-114">-DefaultProfile</span></span>
<span data-ttu-id="892df-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="892df-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="892df-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="892df-116">-MatchCondition</span></span>
<span data-ttu-id="892df-117">Lista de condições de combinação.</span><span class="sxs-lookup"><span data-stu-id="892df-117">List of match conditions.</span></span>

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

### <span data-ttu-id="892df-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="892df-118">-Name</span></span>
<span data-ttu-id="892df-119">O Nome da Regra.</span><span class="sxs-lookup"><span data-stu-id="892df-119">The Name of the Rule.</span></span>

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

### <span data-ttu-id="892df-120">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="892df-120">-Priority</span></span>
<span data-ttu-id="892df-121">Descreve a prioridade da regra.</span><span class="sxs-lookup"><span data-stu-id="892df-121">Describes priority of the rule.</span></span>
<span data-ttu-id="892df-122">As regras com um valor mais baixo serão avaliadas antes das regras com um valor mais alto.</span><span class="sxs-lookup"><span data-stu-id="892df-122">Rules with a lower value will be evaluated before rules with a higher value.</span></span>

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

### <span data-ttu-id="892df-123">-RuleType</span><span class="sxs-lookup"><span data-stu-id="892df-123">-RuleType</span></span>
<span data-ttu-id="892df-124">Descreve o tipo de regra.</span><span class="sxs-lookup"><span data-stu-id="892df-124">Describes type of rule.</span></span>

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

### <span data-ttu-id="892df-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="892df-125">CommonParameters</span></span>
<span data-ttu-id="892df-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="892df-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="892df-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="892df-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="892df-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="892df-128">INPUTS</span></span>

### <span data-ttu-id="892df-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="892df-129">None</span></span>

## <span data-ttu-id="892df-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="892df-130">OUTPUTS</span></span>

### <span data-ttu-id="892df-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="892df-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="892df-132">Notas</span><span class="sxs-lookup"><span data-stu-id="892df-132">NOTES</span></span>

## <span data-ttu-id="892df-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="892df-133">RELATED LINKS</span></span>
