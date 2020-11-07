---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
ms.openlocfilehash: 7b83e7f8ca372faf8158e248d326595a0d162d6a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785336"
---
# <span data-ttu-id="26b1c-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="26b1c-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="26b1c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="26b1c-102">SYNOPSIS</span></span>
<span data-ttu-id="26b1c-103">Obtém a configuração WAF de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="26b1c-103">Gets the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26b1c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26b1c-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26b1c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="26b1c-105">DESCRIPTION</span></span>
<span data-ttu-id="26b1c-106">O cmdlet **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** Obtém a configuração WAF (firewall de aplicativo Web) de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="26b1c-106">The **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="26b1c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="26b1c-107">EXAMPLES</span></span>

### <span data-ttu-id="26b1c-108">Exemplo 1: obter uma configuração de firewall de aplicativo Web do aplicativo Web Gateway</span><span class="sxs-lookup"><span data-stu-id="26b1c-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="26b1c-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e, em seguida, armazena-o na variável $AppGW.</span><span class="sxs-lookup"><span data-stu-id="26b1c-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>

<span data-ttu-id="26b1c-110">O segundo comando obtém a configuração de firewall do gateway do aplicativo em $AppGW e, em seguida, armazena-a no $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="26b1c-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="26b1c-111">OS</span><span class="sxs-lookup"><span data-stu-id="26b1c-111">PARAMETERS</span></span>

### <span data-ttu-id="26b1c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26b1c-112">-ApplicationGateway</span></span>
<span data-ttu-id="26b1c-113">Especifica um objeto do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="26b1c-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="26b1c-114">Você pode usar o cmdlet Get-AzureRmApplicationGateway para obter um objeto de gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="26b1c-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26b1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26b1c-115">-DefaultProfile</span></span>
<span data-ttu-id="26b1c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="26b1c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26b1c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26b1c-117">CommonParameters</span></span>
<span data-ttu-id="26b1c-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26b1c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26b1c-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26b1c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26b1c-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="26b1c-120">INPUTS</span></span>

### <span data-ttu-id="26b1c-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26b1c-121">PSApplicationGateway</span></span>
<span data-ttu-id="26b1c-122">O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="26b1c-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="26b1c-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="26b1c-123">OUTPUTS</span></span>

### <span data-ttu-id="26b1c-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="26b1c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="26b1c-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="26b1c-125">NOTES</span></span>

## <span data-ttu-id="26b1c-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26b1c-126">RELATED LINKS</span></span>

[<span data-ttu-id="26b1c-127">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26b1c-127">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="26b1c-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="26b1c-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="26b1c-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="26b1c-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


