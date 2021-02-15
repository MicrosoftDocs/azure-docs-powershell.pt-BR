---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5eafcfc825b710e31954e247e4114d0f90e97c41
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111663"
---
# <span data-ttu-id="cef2a-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="cef2a-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="cef2a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cef2a-102">SYNOPSIS</span></span>
<span data-ttu-id="cef2a-103">Cria uma nova configuração de grupo de regras desabilitada.</span><span class="sxs-lookup"><span data-stu-id="cef2a-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="cef2a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cef2a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String> [-Rules <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cef2a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="cef2a-105">DESCRIPTION</span></span>
<span data-ttu-id="cef2a-106">O cmdlet **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cria uma nova configuração de grupo de regras desabilitada.</span><span class="sxs-lookup"><span data-stu-id="cef2a-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="cef2a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cef2a-107">EXAMPLES</span></span>

### <span data-ttu-id="cef2a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cef2a-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="cef2a-109">O comando cria uma nova configuração de grupo de regras desabilitada para o grupo de regras chamado "REQUEST-942-APPLICATION-ATTACK-SQLI" com a regra 942130 e a regra 942140 desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="cef2a-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="cef2a-110">A nova configuração de grupo de regras desabilitada é salva no $disabledRuleGroup 1.</span><span class="sxs-lookup"><span data-stu-id="cef2a-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="cef2a-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cef2a-111">PARAMETERS</span></span>

### <span data-ttu-id="cef2a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef2a-112">-DefaultProfile</span></span>
<span data-ttu-id="cef2a-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="cef2a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cef2a-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="cef2a-114">-RuleGroupName</span></span>
<span data-ttu-id="cef2a-115">O nome do grupo de regras que será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="cef2a-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="cef2a-116">-Regras</span><span class="sxs-lookup"><span data-stu-id="cef2a-116">-Rules</span></span>
<span data-ttu-id="cef2a-117">A lista de regras que serão desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="cef2a-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="cef2a-118">Se nulo, todas as regras do grupo de regras serão desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="cef2a-118">If null, all rules of the rule group will be disabled.</span></span>

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

### <span data-ttu-id="cef2a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef2a-119">CommonParameters</span></span>
<span data-ttu-id="cef2a-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cef2a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef2a-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cef2a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef2a-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="cef2a-122">INPUTS</span></span>

### <span data-ttu-id="cef2a-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="cef2a-123">None</span></span>

## <span data-ttu-id="cef2a-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="cef2a-124">OUTPUTS</span></span>

### <span data-ttu-id="cef2a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="cef2a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="cef2a-126">Notas</span><span class="sxs-lookup"><span data-stu-id="cef2a-126">NOTES</span></span>

## <span data-ttu-id="cef2a-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cef2a-127">RELATED LINKS</span></span>

[<span data-ttu-id="cef2a-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="cef2a-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="cef2a-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="cef2a-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

