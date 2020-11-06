---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 388c2d06f7ff62bfe5fc2f6fcf47d5fa9fa16877
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441260"
---
# <span data-ttu-id="c1b50-101">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c1b50-101">Get-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="c1b50-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1b50-102">SYNOPSIS</span></span>
<span data-ttu-id="c1b50-103">Obtém a porta de front-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1b50-103">Gets the front-end port of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1b50-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1b50-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1b50-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c1b50-105">DESCRIPTION</span></span>
<span data-ttu-id="c1b50-106">O cmdlet **Get-AzureRmApplicationGatewayFrontendPort** Obtém a porta de front-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1b50-106">The **Get-AzureRmApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="c1b50-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1b50-107">EXAMPLES</span></span>

### <span data-ttu-id="c1b50-108">Exemplo 1: obter uma porta de front-end especificada</span><span class="sxs-lookup"><span data-stu-id="c1b50-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="c1b50-109">O primeiro comando obtém um gateway do aplicativo denominado ApplicationGateway01 do grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c1b50-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c1b50-110">O segundo comando obtém a porta de front-end chamada FrontEndPort01 da $AppGw e a armazena na variável $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="c1b50-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="c1b50-111">Exemplo 2: obter uma lista de portas de front-end</span><span class="sxs-lookup"><span data-stu-id="c1b50-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzureRmApplicationGatewayFrontendPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="c1b50-112">O primeiro comando obtém um gateway do aplicativo denominado ApplicationGateway01 do grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c1b50-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c1b50-113">O segundo comando obtém uma lista das portas de front-end do $AppGw e a armazena na variável $FrontEndPorts.</span><span class="sxs-lookup"><span data-stu-id="c1b50-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="c1b50-114">OS</span><span class="sxs-lookup"><span data-stu-id="c1b50-114">PARAMETERS</span></span>

### <span data-ttu-id="c1b50-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1b50-115">-ApplicationGateway</span></span>
<span data-ttu-id="c1b50-116">Especifica o objeto do gateway do aplicativo que contém a porta de front-end.</span><span class="sxs-lookup"><span data-stu-id="c1b50-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="c1b50-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1b50-117">-DefaultProfile</span></span>
<span data-ttu-id="c1b50-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1b50-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b50-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1b50-119">-Name</span></span>
<span data-ttu-id="c1b50-120">Especifica o nome da porta de front-end a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="c1b50-120">Specifies the name of the front-end port to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b50-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1b50-121">CommonParameters</span></span>
<span data-ttu-id="c1b50-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1b50-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1b50-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1b50-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1b50-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c1b50-124">INPUTS</span></span>

### <span data-ttu-id="c1b50-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1b50-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="c1b50-126">Parâmetros: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c1b50-126">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="c1b50-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c1b50-127">OUTPUTS</span></span>

### <span data-ttu-id="c1b50-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c1b50-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="c1b50-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c1b50-129">NOTES</span></span>

## <span data-ttu-id="c1b50-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1b50-130">RELATED LINKS</span></span>

[<span data-ttu-id="c1b50-131">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c1b50-131">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c1b50-132">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c1b50-132">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c1b50-133">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c1b50-133">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c1b50-134">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c1b50-134">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


