---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: c1c630c39039d39b1957ccab78bb96d8f085176c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954823"
---
# <span data-ttu-id="c47fd-101">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c47fd-101">Remove-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="c47fd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c47fd-102">SYNOPSIS</span></span>
<span data-ttu-id="c47fd-103">Remove uma regra de roteamento de solicitação de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c47fd-103">Removes a request routing rule from an application gateway.</span></span>

## <span data-ttu-id="c47fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c47fd-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c47fd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c47fd-105">DESCRIPTION</span></span>
<span data-ttu-id="c47fd-106">O cmdlet **Remove-AzApplicationGatewayRequestRoutingRule** remove uma regra de roteamento de solicitação de um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="c47fd-106">The **Remove-AzApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="c47fd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c47fd-107">EXAMPLES</span></span>

### <span data-ttu-id="c47fd-108">Exemplo 1: remover uma regra de roteamento de solicitação de um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="c47fd-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="c47fd-109">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c47fd-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c47fd-110">O segundo comando Remove a regra de roteamento de solicitação chamada Rule02 do gateway do aplicativo armazenado em $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c47fd-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="c47fd-111">OS</span><span class="sxs-lookup"><span data-stu-id="c47fd-111">PARAMETERS</span></span>

### <span data-ttu-id="c47fd-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c47fd-112">-ApplicationGateway</span></span>
<span data-ttu-id="c47fd-113">Especifica o gateway do aplicativo do qual remover uma regra de roteamento de solicitações.</span><span class="sxs-lookup"><span data-stu-id="c47fd-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="c47fd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c47fd-114">-DefaultProfile</span></span>
<span data-ttu-id="c47fd-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c47fd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c47fd-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="c47fd-116">-Name</span></span>
<span data-ttu-id="c47fd-117">Especifica o nome da regra de roteamento de solicitação para a qual esse cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="c47fd-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="c47fd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c47fd-118">CommonParameters</span></span>
<span data-ttu-id="c47fd-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c47fd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c47fd-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c47fd-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c47fd-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c47fd-121">INPUTS</span></span>

### <span data-ttu-id="c47fd-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c47fd-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c47fd-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c47fd-123">OUTPUTS</span></span>

### <span data-ttu-id="c47fd-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c47fd-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="c47fd-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c47fd-125">NOTES</span></span>

## <span data-ttu-id="c47fd-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c47fd-126">RELATED LINKS</span></span>

[<span data-ttu-id="c47fd-127">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c47fd-127">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c47fd-128">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c47fd-128">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c47fd-129">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c47fd-129">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c47fd-130">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c47fd-130">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


