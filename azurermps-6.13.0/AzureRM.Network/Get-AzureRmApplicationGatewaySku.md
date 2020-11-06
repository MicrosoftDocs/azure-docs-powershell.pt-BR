---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: 5d0409ae5be910f2e4480ac61f36d907e7736f0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432772"
---
# <span data-ttu-id="e1ab8-101">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e1ab8-101">Get-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="e1ab8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e1ab8-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ab8-103">Obtém a SKU de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-103">Gets the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1ab8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1ab8-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1ab8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e1ab8-105">DESCRIPTION</span></span>
<span data-ttu-id="e1ab8-106">O cmdlet **Get-AzureRmApplicationGatewaySku** Obtém a SKU (unidade de manutenção de estoque) de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-106">The **Get-AzureRmApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="e1ab8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1ab8-107">EXAMPLES</span></span>

### <span data-ttu-id="e1ab8-108">Exemplo 1: obter uma SKU do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e1ab8-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzureRmApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="e1ab8-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="e1ab8-110">O segundo comando obtém a SKU de um gateway de aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $SKU.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="e1ab8-111">OS</span><span class="sxs-lookup"><span data-stu-id="e1ab8-111">PARAMETERS</span></span>

### <span data-ttu-id="e1ab8-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1ab8-112">-ApplicationGateway</span></span>
<span data-ttu-id="e1ab8-113">Especifica o objeto do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="e1ab8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ab8-114">-DefaultProfile</span></span>
<span data-ttu-id="e1ab8-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1ab8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ab8-116">CommonParameters</span></span>
<span data-ttu-id="e1ab8-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1ab8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ab8-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1ab8-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ab8-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e1ab8-119">INPUTS</span></span>

### <span data-ttu-id="e1ab8-120">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1ab8-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="e1ab8-121">Parâmetros: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e1ab8-121">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="e1ab8-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e1ab8-122">OUTPUTS</span></span>

### <span data-ttu-id="e1ab8-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e1ab8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="e1ab8-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e1ab8-124">NOTES</span></span>

## <span data-ttu-id="e1ab8-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1ab8-125">RELATED LINKS</span></span>

[<span data-ttu-id="e1ab8-126">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e1ab8-126">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="e1ab8-127">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e1ab8-127">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)


