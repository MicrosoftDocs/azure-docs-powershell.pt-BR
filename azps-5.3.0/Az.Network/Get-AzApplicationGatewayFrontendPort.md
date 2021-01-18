---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 404a9ff22f6b6af480e167c5a4f958b9ac4b5d52
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434735"
---
# <span data-ttu-id="ce8db-101">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ce8db-101">Get-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="ce8db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce8db-102">SYNOPSIS</span></span>
<span data-ttu-id="ce8db-103">Obtém a porta de front-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ce8db-103">Gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="ce8db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce8db-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce8db-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce8db-105">DESCRIPTION</span></span>
<span data-ttu-id="ce8db-106">O cmdlet **Get-AzApplicationGatewayFrontendPort** Obtém a porta de front-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ce8db-106">The **Get-AzApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="ce8db-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce8db-107">EXAMPLES</span></span>

### <span data-ttu-id="ce8db-108">Exemplo 1: obter uma porta de front-end especificada</span><span class="sxs-lookup"><span data-stu-id="ce8db-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="ce8db-109">O primeiro comando obtém um gateway do aplicativo denominado ApplicationGateway01 do grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ce8db-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ce8db-110">O segundo comando obtém a porta de front-end chamada FrontEndPort01 da $AppGw e a armazena na variável $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="ce8db-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="ce8db-111">Exemplo 2: obter uma lista de portas de front-end</span><span class="sxs-lookup"><span data-stu-id="ce8db-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="ce8db-112">O primeiro comando obtém um gateway do aplicativo denominado ApplicationGateway01 do grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ce8db-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ce8db-113">O segundo comando obtém uma lista das portas de front-end do $AppGw e a armazena na variável $FrontEndPorts.</span><span class="sxs-lookup"><span data-stu-id="ce8db-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="ce8db-114">OS</span><span class="sxs-lookup"><span data-stu-id="ce8db-114">PARAMETERS</span></span>

### <span data-ttu-id="ce8db-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce8db-115">-ApplicationGateway</span></span>
<span data-ttu-id="ce8db-116">Especifica o objeto do gateway do aplicativo que contém a porta de front-end.</span><span class="sxs-lookup"><span data-stu-id="ce8db-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="ce8db-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce8db-117">-DefaultProfile</span></span>
<span data-ttu-id="ce8db-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ce8db-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce8db-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce8db-119">-Name</span></span>
<span data-ttu-id="ce8db-120">Especifica o nome da porta de front-end a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="ce8db-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="ce8db-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce8db-121">CommonParameters</span></span>
<span data-ttu-id="ce8db-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce8db-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce8db-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce8db-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce8db-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce8db-124">INPUTS</span></span>

### <span data-ttu-id="ce8db-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce8db-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ce8db-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce8db-126">OUTPUTS</span></span>

### <span data-ttu-id="ce8db-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ce8db-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="ce8db-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce8db-128">NOTES</span></span>

## <span data-ttu-id="ce8db-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce8db-129">RELATED LINKS</span></span>

[<span data-ttu-id="ce8db-130">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ce8db-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="ce8db-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ce8db-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="ce8db-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ce8db-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="ce8db-133">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ce8db-133">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


