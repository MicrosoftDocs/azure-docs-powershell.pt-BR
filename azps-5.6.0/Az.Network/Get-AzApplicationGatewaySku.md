---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: cf869a0de5847b1930879dbd610749746370791b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890817"
---
# <span data-ttu-id="2adb2-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="2adb2-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="2adb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2adb2-102">SYNOPSIS</span></span>
<span data-ttu-id="2adb2-103">Obtém a SKU de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2adb2-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="2adb2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2adb2-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2adb2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2adb2-105">DESCRIPTION</span></span>
<span data-ttu-id="2adb2-106">O cmdlet **Get-AzApplicationGatewaySku** obtém a unidade de manutenção de ações (SKU) de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2adb2-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="2adb2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2adb2-107">EXAMPLES</span></span>

### <span data-ttu-id="2adb2-108">Exemplo 1: Obter um SKU de gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="2adb2-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="2adb2-109">O primeiro comando obtém o Gateway de Aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="2adb2-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="2adb2-110">O segundo comando obtém a SKU de um gateway de aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $SKU.</span><span class="sxs-lookup"><span data-stu-id="2adb2-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="2adb2-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2adb2-111">PARAMETERS</span></span>

### <span data-ttu-id="2adb2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2adb2-112">-ApplicationGateway</span></span>
<span data-ttu-id="2adb2-113">Especifica o objeto gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2adb2-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="2adb2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2adb2-114">-DefaultProfile</span></span>
<span data-ttu-id="2adb2-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="2adb2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2adb2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2adb2-116">CommonParameters</span></span>
<span data-ttu-id="2adb2-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2adb2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2adb2-118">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2adb2-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2adb2-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2adb2-119">INPUTS</span></span>

### <span data-ttu-id="2adb2-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2adb2-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2adb2-121">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2adb2-121">OUTPUTS</span></span>

### <span data-ttu-id="2adb2-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="2adb2-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="2adb2-123">NOTES</span><span class="sxs-lookup"><span data-stu-id="2adb2-123">NOTES</span></span>

## <span data-ttu-id="2adb2-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2adb2-124">RELATED LINKS</span></span>

[<span data-ttu-id="2adb2-125">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="2adb2-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="2adb2-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="2adb2-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


