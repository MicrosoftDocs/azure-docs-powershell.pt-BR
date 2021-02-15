---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 6ca7bc3e5d1af477c7d6750f674272ff64d54889
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114184"
---
# <span data-ttu-id="efb32-101">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="efb32-101">Get-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="efb32-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="efb32-102">SYNOPSIS</span></span>
<span data-ttu-id="efb32-103">Obtém um pool de endereços back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="efb32-103">Gets a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="efb32-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="efb32-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efb32-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="efb32-105">DESCRIPTION</span></span>
<span data-ttu-id="efb32-106">O cmdlet **Get-AzApplicationGatewayBackendAddressPool** obtém uma ou mais configurações de pool de endereços back-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="efb32-106">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets one or more backend address pool configurations from an application gateway.</span></span>

## <span data-ttu-id="efb32-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="efb32-107">EXAMPLES</span></span>

### <span data-ttu-id="efb32-108">Exemplo 1: Obter um pool de servidor back-end especificado</span><span class="sxs-lookup"><span data-stu-id="efb32-108">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="efb32-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="efb32-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="efb32-110">O segundo comando obtém o pool de endereços back-end associado $AppGw pool01 e o armazena na variável $BackendPool back-end.</span><span class="sxs-lookup"><span data-stu-id="efb32-110">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="efb32-111">Exemplo 2: Obter uma lista de pool de servidor back-end</span><span class="sxs-lookup"><span data-stu-id="efb32-111">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="efb32-112">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="efb32-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="efb32-113">O segundo comando obtém uma lista dos pools de endereços back-end associados ao $AppGw e armazena a lista na variável $BackendPools back-end.</span><span class="sxs-lookup"><span data-stu-id="efb32-113">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="efb32-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="efb32-114">PARAMETERS</span></span>

### <span data-ttu-id="efb32-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="efb32-115">-ApplicationGateway</span></span>
<span data-ttu-id="efb32-116">O cmdlet **Get-AzApplicationGatewayBackendAddressPool** obtém um pool de endereços back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="efb32-116">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="efb32-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efb32-117">-DefaultProfile</span></span>
<span data-ttu-id="efb32-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="efb32-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efb32-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="efb32-119">-Name</span></span>
<span data-ttu-id="efb32-120">Especifica o nome do pool de endereços back-end que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="efb32-120">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="efb32-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efb32-121">CommonParameters</span></span>
<span data-ttu-id="efb32-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efb32-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efb32-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="efb32-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efb32-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="efb32-124">INPUTS</span></span>

### <span data-ttu-id="efb32-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="efb32-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="efb32-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="efb32-126">OUTPUTS</span></span>

### <span data-ttu-id="efb32-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="efb32-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="efb32-128">Notas</span><span class="sxs-lookup"><span data-stu-id="efb32-128">NOTES</span></span>

## <span data-ttu-id="efb32-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="efb32-129">RELATED LINKS</span></span>

[<span data-ttu-id="efb32-130">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="efb32-130">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="efb32-131">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="efb32-131">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="efb32-132">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="efb32-132">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="efb32-133">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="efb32-133">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


