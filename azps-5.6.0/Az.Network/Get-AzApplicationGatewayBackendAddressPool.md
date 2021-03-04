---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 458788041ce833cacb30616a7aa8268ed485c65b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888676"
---
# <span data-ttu-id="ffeb8-101">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ffeb8-101">Get-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="ffeb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffeb8-102">SYNOPSIS</span></span>
<span data-ttu-id="ffeb8-103">Obtém um pool de endereços back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ffeb8-103">Gets a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="ffeb8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ffeb8-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffeb8-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ffeb8-105">DESCRIPTION</span></span>
<span data-ttu-id="ffeb8-106">O cmdlet **Get-AzApplicationGatewayBackendAddressPool** obtém uma ou mais configurações de pool de endereços back-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ffeb8-106">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets one or more backend address pool configurations from an application gateway.</span></span>

## <span data-ttu-id="ffeb8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ffeb8-107">EXAMPLES</span></span>

### <span data-ttu-id="ffeb8-108">Exemplo 1: Obter um pool de servidores back-end especificado</span><span class="sxs-lookup"><span data-stu-id="ffeb8-108">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="ffeb8-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ffeb8-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ffeb8-110">O segundo comando obtém o pool de endereços back-end associado ao $AppGw chamado Pool01 e o armazena na variável $BackendPool back-end.</span><span class="sxs-lookup"><span data-stu-id="ffeb8-110">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="ffeb8-111">Exemplo 2: Obter uma lista de pool de servidores back-end</span><span class="sxs-lookup"><span data-stu-id="ffeb8-111">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="ffeb8-112">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ffeb8-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ffeb8-113">O segundo comando obtém uma lista dos pools de endereços back-end associados ao $AppGw e armazena a lista na variável $BackendPools back-end.</span><span class="sxs-lookup"><span data-stu-id="ffeb8-113">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="ffeb8-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ffeb8-114">PARAMETERS</span></span>

### <span data-ttu-id="ffeb8-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ffeb8-115">-ApplicationGateway</span></span>
<span data-ttu-id="ffeb8-116">O cmdlet **Get-AzApplicationGatewayBackendAddressPool** obtém um pool de endereços back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ffeb8-116">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="ffeb8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffeb8-117">-DefaultProfile</span></span>
<span data-ttu-id="ffeb8-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ffeb8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffeb8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ffeb8-119">-Name</span></span>
<span data-ttu-id="ffeb8-120">Especifica o nome do pool de endereços back-end que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="ffeb8-120">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ffeb8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffeb8-121">CommonParameters</span></span>
<span data-ttu-id="ffeb8-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffeb8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffeb8-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ffeb8-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffeb8-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ffeb8-124">INPUTS</span></span>

### <span data-ttu-id="ffeb8-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ffeb8-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ffeb8-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ffeb8-126">OUTPUTS</span></span>

### <span data-ttu-id="ffeb8-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ffeb8-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="ffeb8-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="ffeb8-128">NOTES</span></span>

## <span data-ttu-id="ffeb8-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ffeb8-129">RELATED LINKS</span></span>

[<span data-ttu-id="ffeb8-130">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ffeb8-130">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ffeb8-131">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ffeb8-131">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ffeb8-132">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ffeb8-132">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ffeb8-133">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ffeb8-133">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


