---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 9cd7cd0b859ff806b084ebfe1c76e07aed3a7c43
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947726"
---
# <span data-ttu-id="7749b-101">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7749b-101">Add-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="7749b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7749b-102">SYNOPSIS</span></span>
<span data-ttu-id="7749b-103">Adiciona uma porta de front-end a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7749b-103">Adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="7749b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7749b-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7749b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7749b-105">DESCRIPTION</span></span>
<span data-ttu-id="7749b-106">O cmdlet **Add-AzApplicationGatewayFrontendPort** adiciona uma porta de front-end a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7749b-106">The **Add-AzApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="7749b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7749b-107">EXAMPLES</span></span>

### <span data-ttu-id="7749b-108">Exemplo 1: adicionar uma porta de front-end a um gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="7749b-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="7749b-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7749b-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7749b-110">O segundo comando adiciona a porta 80 como uma porta de front-end do gateway do aplicativo armazenado no $AppGw e nomeia a porta FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="7749b-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="7749b-111">OS</span><span class="sxs-lookup"><span data-stu-id="7749b-111">PARAMETERS</span></span>

### <span data-ttu-id="7749b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7749b-112">-ApplicationGateway</span></span>
<span data-ttu-id="7749b-113">Especifica o gateway do aplicativo para o qual esse cmdlet adiciona uma porta de front-end.</span><span class="sxs-lookup"><span data-stu-id="7749b-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="7749b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7749b-114">-DefaultProfile</span></span>
<span data-ttu-id="7749b-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7749b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7749b-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="7749b-116">-Name</span></span>
<span data-ttu-id="7749b-117">Especifica o nome da porta de front-end.</span><span class="sxs-lookup"><span data-stu-id="7749b-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="7749b-118">-Porta</span><span class="sxs-lookup"><span data-stu-id="7749b-118">-Port</span></span>
<span data-ttu-id="7749b-119">Especifica o número da porta.</span><span class="sxs-lookup"><span data-stu-id="7749b-119">Specifies the port number.</span></span>

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

### <span data-ttu-id="7749b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7749b-120">CommonParameters</span></span>
<span data-ttu-id="7749b-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7749b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7749b-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7749b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7749b-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7749b-123">INPUTS</span></span>

### <span data-ttu-id="7749b-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7749b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7749b-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7749b-125">OUTPUTS</span></span>

### <span data-ttu-id="7749b-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7749b-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7749b-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7749b-127">NOTES</span></span>

## <span data-ttu-id="7749b-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7749b-128">RELATED LINKS</span></span>

[<span data-ttu-id="7749b-129">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7749b-129">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="7749b-130">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7749b-130">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="7749b-131">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7749b-131">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="7749b-132">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7749b-132">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


