---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysku
schema: 2.0.0
ms.openlocfilehash: 2359459688dbae2c718e4a5d5f65bf68b2c8c5ea
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786476"
---
# <span data-ttu-id="7fbd5-101">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7fbd5-101">Get-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="7fbd5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7fbd5-102">SYNOPSIS</span></span>
<span data-ttu-id="7fbd5-103">Obtém a SKU de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7fbd5-103">Gets the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fbd5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7fbd5-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fbd5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7fbd5-105">DESCRIPTION</span></span>
<span data-ttu-id="7fbd5-106">O cmdlet **Get-AzureRmApplicationGatewaySku** Obtém a SKU (unidade de manutenção de estoque) de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7fbd5-106">The **Get-AzureRmApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="7fbd5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7fbd5-107">EXAMPLES</span></span>

### <span data-ttu-id="7fbd5-108">Exemplo 1: obter uma SKU do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="7fbd5-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzureRmApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="7fbd5-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="7fbd5-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="7fbd5-110">O segundo comando obtém a SKU de um gateway de aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $SKU.</span><span class="sxs-lookup"><span data-stu-id="7fbd5-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="7fbd5-111">OS</span><span class="sxs-lookup"><span data-stu-id="7fbd5-111">PARAMETERS</span></span>

### <span data-ttu-id="7fbd5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7fbd5-112">-ApplicationGateway</span></span>
<span data-ttu-id="7fbd5-113">Especifica o objeto do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7fbd5-113">Specifies the application gateway object.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fbd5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fbd5-114">-DefaultProfile</span></span>
<span data-ttu-id="7fbd5-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7fbd5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fbd5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fbd5-116">CommonParameters</span></span>
<span data-ttu-id="7fbd5-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fbd5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fbd5-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fbd5-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fbd5-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7fbd5-119">INPUTS</span></span>

### <span data-ttu-id="7fbd5-120">System. String</span><span class="sxs-lookup"><span data-stu-id="7fbd5-120">System.String</span></span>

## <span data-ttu-id="7fbd5-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7fbd5-121">OUTPUTS</span></span>

### <span data-ttu-id="7fbd5-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7fbd5-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="7fbd5-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7fbd5-123">NOTES</span></span>

## <span data-ttu-id="7fbd5-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7fbd5-124">RELATED LINKS</span></span>

[<span data-ttu-id="7fbd5-125">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7fbd5-125">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="7fbd5-126">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7fbd5-126">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)


