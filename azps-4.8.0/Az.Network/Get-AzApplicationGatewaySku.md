---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: c8bd4a0070aa0e5635fad7cb20a627a7d23f5922
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112494"
---
# <span data-ttu-id="eb55d-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="eb55d-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="eb55d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eb55d-102">SYNOPSIS</span></span>
<span data-ttu-id="eb55d-103">Obtém a SKU de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eb55d-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="eb55d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb55d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb55d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eb55d-105">DESCRIPTION</span></span>
<span data-ttu-id="eb55d-106">O cmdlet **Get-AzApplicationGatewaySku** Obtém a SKU (unidade de manutenção de estoque) de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eb55d-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="eb55d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb55d-107">EXAMPLES</span></span>

### <span data-ttu-id="eb55d-108">Exemplo 1: obter uma SKU do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="eb55d-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="eb55d-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="eb55d-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="eb55d-110">O segundo comando obtém a SKU de um gateway de aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $SKU.</span><span class="sxs-lookup"><span data-stu-id="eb55d-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="eb55d-111">OS</span><span class="sxs-lookup"><span data-stu-id="eb55d-111">PARAMETERS</span></span>

### <span data-ttu-id="eb55d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb55d-112">-ApplicationGateway</span></span>
<span data-ttu-id="eb55d-113">Especifica o objeto do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eb55d-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="eb55d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb55d-114">-DefaultProfile</span></span>
<span data-ttu-id="eb55d-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eb55d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb55d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb55d-116">CommonParameters</span></span>
<span data-ttu-id="eb55d-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb55d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb55d-118">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb55d-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb55d-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eb55d-119">INPUTS</span></span>

### <span data-ttu-id="eb55d-120">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb55d-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="eb55d-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eb55d-121">OUTPUTS</span></span>

### <span data-ttu-id="eb55d-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="eb55d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="eb55d-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eb55d-123">NOTES</span></span>

## <span data-ttu-id="eb55d-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb55d-124">RELATED LINKS</span></span>

[<span data-ttu-id="eb55d-125">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="eb55d-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="eb55d-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="eb55d-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


