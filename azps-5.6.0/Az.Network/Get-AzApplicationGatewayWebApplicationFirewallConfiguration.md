---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: d3b8a57fcd170a2a1f1e4e4c539cff8a60885260
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890798"
---
# <span data-ttu-id="148aa-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="148aa-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="148aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="148aa-102">SYNOPSIS</span></span>
<span data-ttu-id="148aa-103">Obtém a configuração WAF de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="148aa-103">Gets the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="148aa-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="148aa-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="148aa-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="148aa-105">DESCRIPTION</span></span>
<span data-ttu-id="148aa-106">O cmdlet **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** obtém a configuração do waf (firewall de aplicativo web) de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="148aa-106">The **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="148aa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="148aa-107">EXAMPLES</span></span>

### <span data-ttu-id="148aa-108">Exemplo 1: obter uma configuração de firewall de aplicativo web de gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="148aa-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="148aa-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 e o armazena na variável $AppGW aplicativo.</span><span class="sxs-lookup"><span data-stu-id="148aa-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>
<span data-ttu-id="148aa-110">O segundo comando obtém a configuração de firewall do gateway de aplicativo no $AppGW e o armazena $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="148aa-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="148aa-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="148aa-111">PARAMETERS</span></span>

### <span data-ttu-id="148aa-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="148aa-112">-ApplicationGateway</span></span>
<span data-ttu-id="148aa-113">Especifica um objeto gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="148aa-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="148aa-114">Você pode usar o cmdlet Get-AzApplicationGateway para obter um objeto gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="148aa-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="148aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="148aa-115">-DefaultProfile</span></span>
<span data-ttu-id="148aa-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="148aa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="148aa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="148aa-117">CommonParameters</span></span>
<span data-ttu-id="148aa-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="148aa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="148aa-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="148aa-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="148aa-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="148aa-120">INPUTS</span></span>

### <span data-ttu-id="148aa-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="148aa-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="148aa-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="148aa-122">OUTPUTS</span></span>

### <span data-ttu-id="148aa-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="148aa-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="148aa-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="148aa-124">NOTES</span></span>

## <span data-ttu-id="148aa-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="148aa-125">RELATED LINKS</span></span>

[<span data-ttu-id="148aa-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="148aa-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="148aa-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="148aa-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="148aa-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="148aa-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


