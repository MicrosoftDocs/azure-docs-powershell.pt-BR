---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: 425955dd9b39b78c599262f7681c97dd15c93fb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427538"
---
# <span data-ttu-id="06007-101">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="06007-101">Get-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="06007-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06007-102">SYNOPSIS</span></span>
<span data-ttu-id="06007-103">Obtém a SKU de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="06007-103">Gets the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06007-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06007-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06007-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="06007-105">DESCRIPTION</span></span>
<span data-ttu-id="06007-106">O cmdlet **Get-AzureRmApplicationGatewaySku** Obtém a SKU (unidade de manutenção de estoque) de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="06007-106">The **Get-AzureRmApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="06007-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06007-107">EXAMPLES</span></span>

### <span data-ttu-id="06007-108">Exemplo 1: obter uma SKU do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="06007-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzureRmApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="06007-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="06007-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="06007-110">O segundo comando obtém a SKU de um gateway de aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $SKU.</span><span class="sxs-lookup"><span data-stu-id="06007-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="06007-111">OS</span><span class="sxs-lookup"><span data-stu-id="06007-111">PARAMETERS</span></span>

### <span data-ttu-id="06007-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06007-112">-ApplicationGateway</span></span>
<span data-ttu-id="06007-113">Especifica o objeto do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="06007-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="06007-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06007-114">-DefaultProfile</span></span>
<span data-ttu-id="06007-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="06007-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06007-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06007-116">CommonParameters</span></span>
<span data-ttu-id="06007-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06007-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06007-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06007-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06007-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="06007-119">INPUTS</span></span>

### <span data-ttu-id="06007-120">System. String</span><span class="sxs-lookup"><span data-stu-id="06007-120">System.String</span></span>

## <span data-ttu-id="06007-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="06007-121">OUTPUTS</span></span>

### <span data-ttu-id="06007-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="06007-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="06007-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="06007-123">NOTES</span></span>

## <span data-ttu-id="06007-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06007-124">RELATED LINKS</span></span>

[<span data-ttu-id="06007-125">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="06007-125">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="06007-126">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="06007-126">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)

