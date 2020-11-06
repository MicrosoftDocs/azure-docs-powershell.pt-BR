---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: ccef6b60dd33ebc584f782899134509a4e89f2be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602214"
---
# <span data-ttu-id="e58ea-101">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e58ea-101">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="e58ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e58ea-102">SYNOPSIS</span></span>
<span data-ttu-id="e58ea-103">Obtém um pool de endereços back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e58ea-103">Gets a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e58ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e58ea-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e58ea-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e58ea-105">DESCRIPTION</span></span>

## <span data-ttu-id="e58ea-106">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e58ea-106">EXAMPLES</span></span>

### <span data-ttu-id="e58ea-107">Exemplo 1: obter um pool de servidores back-end especificado</span><span class="sxs-lookup"><span data-stu-id="e58ea-107">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="e58ea-108">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e58ea-108">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e58ea-109">O segundo comando obtém o pool de endereços back-end associado a $AppGw chamado Pool01 e o armazena na variável $BackendPool.</span><span class="sxs-lookup"><span data-stu-id="e58ea-109">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="e58ea-110">Exemplo 2: obter uma lista de pool de servidores back-end</span><span class="sxs-lookup"><span data-stu-id="e58ea-110">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="e58ea-111">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e58ea-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e58ea-112">O segundo comando obtém uma lista dos pools de endereços back-end associados a $AppGw e armazena a lista na variável $BackendPools.</span><span class="sxs-lookup"><span data-stu-id="e58ea-112">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="e58ea-113">OS</span><span class="sxs-lookup"><span data-stu-id="e58ea-113">PARAMETERS</span></span>

### <span data-ttu-id="e58ea-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e58ea-114">-ApplicationGateway</span></span>
<span data-ttu-id="e58ea-115">O cmdlet **Get-AzureRmApplicationGatewayBackendAddressPool** Obtém um pool de endereços back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e58ea-115">The **Get-AzureRmApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="e58ea-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="e58ea-116">-Name</span></span>
<span data-ttu-id="e58ea-117">Especifica o nome do pool de endereços back-end que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="e58ea-117">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e58ea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e58ea-118">-DefaultProfile</span></span>
<span data-ttu-id="e58ea-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e58ea-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e58ea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e58ea-120">CommonParameters</span></span>
<span data-ttu-id="e58ea-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e58ea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e58ea-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e58ea-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e58ea-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e58ea-123">INPUTS</span></span>

### <span data-ttu-id="e58ea-124">System. String</span><span class="sxs-lookup"><span data-stu-id="e58ea-124">System.String</span></span>

## <span data-ttu-id="e58ea-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e58ea-125">OUTPUTS</span></span>

### <span data-ttu-id="e58ea-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e58ea-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="e58ea-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e58ea-127">NOTES</span></span>

## <span data-ttu-id="e58ea-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e58ea-128">RELATED LINKS</span></span>

[<span data-ttu-id="e58ea-129">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e58ea-129">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e58ea-130">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e58ea-130">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e58ea-131">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e58ea-131">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e58ea-132">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e58ea-132">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


