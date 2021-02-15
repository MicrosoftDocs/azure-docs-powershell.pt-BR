---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: c8bd4a0070aa0e5635fad7cb20a627a7d23f5922
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114173"
---
# <span data-ttu-id="5122e-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="5122e-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="5122e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5122e-102">SYNOPSIS</span></span>
<span data-ttu-id="5122e-103">Obtém a SKU de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5122e-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="5122e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5122e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5122e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="5122e-105">DESCRIPTION</span></span>
<span data-ttu-id="5122e-106">O cmdlet **Get-AzApplicationGatewaySku** obtém a unidade de manutenção de ações (SKU) de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5122e-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="5122e-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5122e-107">EXAMPLES</span></span>

### <span data-ttu-id="5122e-108">Exemplo 1: Obter uma SKU de gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="5122e-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="5122e-109">O primeiro comando obtém o Gateway de Aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="5122e-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="5122e-110">O segundo comando obtém a SKU de um gateway de aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $SKU.</span><span class="sxs-lookup"><span data-stu-id="5122e-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="5122e-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5122e-111">PARAMETERS</span></span>

### <span data-ttu-id="5122e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5122e-112">-ApplicationGateway</span></span>
<span data-ttu-id="5122e-113">Especifica o objeto do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5122e-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="5122e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5122e-114">-DefaultProfile</span></span>
<span data-ttu-id="5122e-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="5122e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5122e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5122e-116">CommonParameters</span></span>
<span data-ttu-id="5122e-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5122e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5122e-118">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5122e-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5122e-119">Entradas</span><span class="sxs-lookup"><span data-stu-id="5122e-119">INPUTS</span></span>

### <span data-ttu-id="5122e-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5122e-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5122e-121">Saídas</span><span class="sxs-lookup"><span data-stu-id="5122e-121">OUTPUTS</span></span>

### <span data-ttu-id="5122e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="5122e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="5122e-123">Notas</span><span class="sxs-lookup"><span data-stu-id="5122e-123">NOTES</span></span>

## <span data-ttu-id="5122e-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5122e-124">RELATED LINKS</span></span>

[<span data-ttu-id="5122e-125">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="5122e-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="5122e-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="5122e-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


