---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 4b3acad1f0a9d5a516ee541f61bfee93fca532b8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772067"
---
# <span data-ttu-id="43b43-101">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="43b43-101">Get-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="43b43-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43b43-102">SYNOPSIS</span></span>
<span data-ttu-id="43b43-103">Obtém um pool de endereços back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="43b43-103">Gets a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="43b43-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43b43-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43b43-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="43b43-105">DESCRIPTION</span></span>
<span data-ttu-id="43b43-106">O cmdlet **Get-AzApplicationGatewayBackendAddressPool** Obtém uma ou mais configurações de pool de endereços back-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="43b43-106">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets one or more backend address pool configurations from an application gateway.</span></span>

## <span data-ttu-id="43b43-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="43b43-107">EXAMPLES</span></span>

### <span data-ttu-id="43b43-108">Exemplo 1: obter um pool de servidores back-end especificado</span><span class="sxs-lookup"><span data-stu-id="43b43-108">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="43b43-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="43b43-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="43b43-110">O segundo comando obtém o pool de endereços back-end associado a $AppGw chamado Pool01 e o armazena na variável $BackendPool.</span><span class="sxs-lookup"><span data-stu-id="43b43-110">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="43b43-111">Exemplo 2: obter uma lista de pool de servidores back-end</span><span class="sxs-lookup"><span data-stu-id="43b43-111">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="43b43-112">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="43b43-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="43b43-113">O segundo comando obtém uma lista dos pools de endereços back-end associados a $AppGw e armazena a lista na variável $BackendPools.</span><span class="sxs-lookup"><span data-stu-id="43b43-113">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="43b43-114">OS</span><span class="sxs-lookup"><span data-stu-id="43b43-114">PARAMETERS</span></span>

### <span data-ttu-id="43b43-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="43b43-115">-ApplicationGateway</span></span>
<span data-ttu-id="43b43-116">O cmdlet **Get-AzApplicationGatewayBackendAddressPool** Obtém um pool de endereços back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="43b43-116">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="43b43-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43b43-117">-DefaultProfile</span></span>
<span data-ttu-id="43b43-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="43b43-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43b43-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="43b43-119">-Name</span></span>
<span data-ttu-id="43b43-120">Especifica o nome do pool de endereços back-end que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="43b43-120">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="43b43-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43b43-121">CommonParameters</span></span>
<span data-ttu-id="43b43-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43b43-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43b43-123">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43b43-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43b43-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="43b43-124">INPUTS</span></span>

### <span data-ttu-id="43b43-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="43b43-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="43b43-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="43b43-126">OUTPUTS</span></span>

### <span data-ttu-id="43b43-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="43b43-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="43b43-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="43b43-128">NOTES</span></span>

## <span data-ttu-id="43b43-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43b43-129">RELATED LINKS</span></span>

[<span data-ttu-id="43b43-130">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="43b43-130">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="43b43-131">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="43b43-131">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="43b43-132">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="43b43-132">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="43b43-133">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="43b43-133">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)

