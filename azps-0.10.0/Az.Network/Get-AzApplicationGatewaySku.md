---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: e8ad9974096f633cd829c4d933f092fd869a4103
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775582"
---
# <span data-ttu-id="50964-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="50964-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="50964-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="50964-102">SYNOPSIS</span></span>
<span data-ttu-id="50964-103">Obtém a SKU de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="50964-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="50964-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50964-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50964-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="50964-105">DESCRIPTION</span></span>
<span data-ttu-id="50964-106">O cmdlet **Get-AzApplicationGatewaySku** Obtém a SKU (unidade de manutenção de estoque) de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="50964-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="50964-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="50964-107">EXAMPLES</span></span>

### <span data-ttu-id="50964-108">Exemplo 1: obter uma SKU do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="50964-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="50964-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="50964-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="50964-110">O segundo comando obtém a SKU de um gateway de aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $SKU.</span><span class="sxs-lookup"><span data-stu-id="50964-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="50964-111">OS</span><span class="sxs-lookup"><span data-stu-id="50964-111">PARAMETERS</span></span>

### <span data-ttu-id="50964-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50964-112">-ApplicationGateway</span></span>
<span data-ttu-id="50964-113">Especifica o objeto do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="50964-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="50964-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50964-114">-DefaultProfile</span></span>
<span data-ttu-id="50964-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="50964-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50964-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50964-116">CommonParameters</span></span>
<span data-ttu-id="50964-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50964-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50964-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50964-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50964-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="50964-119">INPUTS</span></span>

### <span data-ttu-id="50964-120">System. String</span><span class="sxs-lookup"><span data-stu-id="50964-120">System.String</span></span>

## <span data-ttu-id="50964-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="50964-121">OUTPUTS</span></span>

### <span data-ttu-id="50964-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="50964-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="50964-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="50964-123">NOTES</span></span>

## <span data-ttu-id="50964-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="50964-124">RELATED LINKS</span></span>

[<span data-ttu-id="50964-125">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="50964-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="50964-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="50964-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


