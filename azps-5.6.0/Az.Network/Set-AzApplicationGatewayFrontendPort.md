---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: e134fafb8f7089b803b09a0202d3c43b0948f7ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885981"
---
# <span data-ttu-id="b01b8-101">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b01b8-101">Set-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="b01b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b01b8-102">SYNOPSIS</span></span>
<span data-ttu-id="b01b8-103">Modifica uma porta front-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b01b8-103">Modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="b01b8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b01b8-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b01b8-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b01b8-105">DESCRIPTION</span></span>
<span data-ttu-id="b01b8-106">O cmdlet **Set-AzApplicationGatewayFrontendPort** modifica uma porta front-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b01b8-106">The **Set-AzApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="b01b8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b01b8-107">EXAMPLES</span></span>

### <span data-ttu-id="b01b8-108">Exemplo 1: definir uma porta front-end do gateway de aplicativo como 80</span><span class="sxs-lookup"><span data-stu-id="b01b8-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="b01b8-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b01b8-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b01b8-110">O segundo comando modifica o gateway no $AppGw para usar a porta 80 para a porta front-end chamada FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="b01b8-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="b01b8-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b01b8-111">PARAMETERS</span></span>

### <span data-ttu-id="b01b8-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b01b8-112">-ApplicationGateway</span></span>
<span data-ttu-id="b01b8-113">Especifica o objeto gateway de aplicativo com o qual esse cmdlet associa a porta front-end.</span><span class="sxs-lookup"><span data-stu-id="b01b8-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

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

### <span data-ttu-id="b01b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b01b8-114">-DefaultProfile</span></span>
<span data-ttu-id="b01b8-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b01b8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b01b8-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b01b8-116">-Name</span></span>
<span data-ttu-id="b01b8-117">Especifica o nome da porta front-end a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="b01b8-117">Specifies the name of the front-end port to modify.</span></span>

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

### <span data-ttu-id="b01b8-118">-Port</span><span class="sxs-lookup"><span data-stu-id="b01b8-118">-Port</span></span>
<span data-ttu-id="b01b8-119">Especifica o número da porta a ser usado para a porta front-end.</span><span class="sxs-lookup"><span data-stu-id="b01b8-119">Specifies the port number to use for the front-end port.</span></span>

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

### <span data-ttu-id="b01b8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b01b8-120">CommonParameters</span></span>
<span data-ttu-id="b01b8-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b01b8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b01b8-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b01b8-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b01b8-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b01b8-123">INPUTS</span></span>

### <span data-ttu-id="b01b8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b01b8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b01b8-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b01b8-125">OUTPUTS</span></span>

### <span data-ttu-id="b01b8-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b01b8-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b01b8-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="b01b8-127">NOTES</span></span>

## <span data-ttu-id="b01b8-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b01b8-128">RELATED LINKS</span></span>

[<span data-ttu-id="b01b8-129">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b01b8-129">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b01b8-130">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b01b8-130">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b01b8-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b01b8-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b01b8-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b01b8-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)
