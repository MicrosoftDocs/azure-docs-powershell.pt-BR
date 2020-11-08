---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 08637412afafe9220107e95dd3cb7dcc5154ba26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125568"
---
# <span data-ttu-id="b8f7e-101">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b8f7e-101">Set-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="b8f7e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8f7e-102">SYNOPSIS</span></span>
<span data-ttu-id="b8f7e-103">Modifica uma porta de front-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b8f7e-103">Modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="b8f7e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8f7e-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8f7e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b8f7e-105">DESCRIPTION</span></span>
<span data-ttu-id="b8f7e-106">O cmdlet **set-AzApplicationGatewayFrontendPort** modifica uma porta de front-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b8f7e-106">The **Set-AzApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="b8f7e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8f7e-107">EXAMPLES</span></span>

### <span data-ttu-id="b8f7e-108">Exemplo 1: definir uma porta de front-end do Application Gateway para o 80</span><span class="sxs-lookup"><span data-stu-id="b8f7e-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="b8f7e-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b8f7e-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b8f7e-110">O segundo comando modifica o gateway em $AppGw para usar a porta 80 para a porta de front-end chamada FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="b8f7e-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="b8f7e-111">OS</span><span class="sxs-lookup"><span data-stu-id="b8f7e-111">PARAMETERS</span></span>

### <span data-ttu-id="b8f7e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8f7e-112">-ApplicationGateway</span></span>
<span data-ttu-id="b8f7e-113">Especifica o objeto do gateway do aplicativo com o qual esse cmdlet associa a porta de front-end.</span><span class="sxs-lookup"><span data-stu-id="b8f7e-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

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

### <span data-ttu-id="b8f7e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8f7e-114">-DefaultProfile</span></span>
<span data-ttu-id="b8f7e-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8f7e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8f7e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8f7e-116">-Name</span></span>
<span data-ttu-id="b8f7e-117">Especifica o nome da porta de front-end a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="b8f7e-117">Specifies the name of the front-end port to modify.</span></span>

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

### <span data-ttu-id="b8f7e-118">-Porta</span><span class="sxs-lookup"><span data-stu-id="b8f7e-118">-Port</span></span>
<span data-ttu-id="b8f7e-119">Especifica o número da porta a ser usada para a porta de front-end.</span><span class="sxs-lookup"><span data-stu-id="b8f7e-119">Specifies the port number to use for the front-end port.</span></span>

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

### <span data-ttu-id="b8f7e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8f7e-120">CommonParameters</span></span>
<span data-ttu-id="b8f7e-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8f7e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8f7e-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8f7e-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8f7e-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b8f7e-123">INPUTS</span></span>

### <span data-ttu-id="b8f7e-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8f7e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b8f7e-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b8f7e-125">OUTPUTS</span></span>

### <span data-ttu-id="b8f7e-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8f7e-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b8f7e-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b8f7e-127">NOTES</span></span>

## <span data-ttu-id="b8f7e-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8f7e-128">RELATED LINKS</span></span>

[<span data-ttu-id="b8f7e-129">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b8f7e-129">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b8f7e-130">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b8f7e-130">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b8f7e-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b8f7e-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b8f7e-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b8f7e-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)
