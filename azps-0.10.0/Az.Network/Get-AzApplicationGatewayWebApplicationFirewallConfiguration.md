---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 77a87d80e656098eeb9450b0ed612d82a8b9e7fa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775566"
---
# <span data-ttu-id="43835-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="43835-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="43835-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43835-102">SYNOPSIS</span></span>
<span data-ttu-id="43835-103">Obtém a configuração WAF de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="43835-103">Gets the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="43835-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43835-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43835-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="43835-105">DESCRIPTION</span></span>
<span data-ttu-id="43835-106">O cmdlet **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** Obtém a configuração WAF (firewall de aplicativo Web) de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="43835-106">The **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="43835-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="43835-107">EXAMPLES</span></span>

### <span data-ttu-id="43835-108">Exemplo 1: obter uma configuração de firewall de aplicativo Web do aplicativo Web Gateway</span><span class="sxs-lookup"><span data-stu-id="43835-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="43835-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e, em seguida, armazena-o na variável $AppGW.</span><span class="sxs-lookup"><span data-stu-id="43835-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>

<span data-ttu-id="43835-110">O segundo comando obtém a configuração de firewall do gateway do aplicativo em $AppGW e, em seguida, armazena-a no $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="43835-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="43835-111">OS</span><span class="sxs-lookup"><span data-stu-id="43835-111">PARAMETERS</span></span>

### <span data-ttu-id="43835-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="43835-112">-ApplicationGateway</span></span>
<span data-ttu-id="43835-113">Especifica um objeto do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="43835-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="43835-114">Você pode usar o cmdlet Get-AzApplicationGateway para obter um objeto de gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="43835-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="43835-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43835-115">-DefaultProfile</span></span>
<span data-ttu-id="43835-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="43835-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43835-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43835-117">CommonParameters</span></span>
<span data-ttu-id="43835-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43835-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43835-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43835-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43835-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="43835-120">INPUTS</span></span>

### <span data-ttu-id="43835-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="43835-121">PSApplicationGateway</span></span>
<span data-ttu-id="43835-122">O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="43835-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="43835-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="43835-123">OUTPUTS</span></span>

### <span data-ttu-id="43835-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="43835-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="43835-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="43835-125">NOTES</span></span>

## <span data-ttu-id="43835-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43835-126">RELATED LINKS</span></span>

[<span data-ttu-id="43835-127">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="43835-127">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="43835-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="43835-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="43835-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="43835-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


