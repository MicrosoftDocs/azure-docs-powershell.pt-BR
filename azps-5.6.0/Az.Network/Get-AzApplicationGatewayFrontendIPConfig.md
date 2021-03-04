---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: cab20e2b92343549b5138f14f88505c70624effb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891172"
---
# <span data-ttu-id="50d53-101">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="50d53-101">Get-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="50d53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50d53-102">SYNOPSIS</span></span>
<span data-ttu-id="50d53-103">Obtém a configuração de IP front-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="50d53-103">Gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="50d53-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="50d53-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50d53-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="50d53-105">DESCRIPTION</span></span>
<span data-ttu-id="50d53-106">O cmdlet **Get-AzApplicationGatewayFrontendIPConfig obtém** a configuração de IP front-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="50d53-106">The **Get-AzApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="50d53-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="50d53-107">EXAMPLES</span></span>

### <span data-ttu-id="50d53-108">Exemplo 1: Obter uma configuração IP front-end especificada</span><span class="sxs-lookup"><span data-stu-id="50d53-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="50d53-109">O primeiro comando obtém um gateway de aplicativo chamado ApplicationGateway01 do grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando obtém a configuração de IP front-end chamada FrontEndIP01 $AppGw e armazena-a na variável $FrontEndIP front-end.</span><span class="sxs-lookup"><span data-stu-id="50d53-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="50d53-110">Exemplo 2: Obter uma lista de configurações de IP front-end</span><span class="sxs-lookup"><span data-stu-id="50d53-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="50d53-111">O primeiro comando obtém um gateway de aplicativo chamado ApplicationGateway01 do grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando obtém uma lista das configurações de IP front-end $AppGw o armazena na variável $FrontEndIPs front-end.</span><span class="sxs-lookup"><span data-stu-id="50d53-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="50d53-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="50d53-112">PARAMETERS</span></span>

### <span data-ttu-id="50d53-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50d53-113">-ApplicationGateway</span></span>
<span data-ttu-id="50d53-114">Especifica o objeto gateway de aplicativo que contém a configuração de IP front-end.</span><span class="sxs-lookup"><span data-stu-id="50d53-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="50d53-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50d53-115">-DefaultProfile</span></span>
<span data-ttu-id="50d53-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="50d53-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50d53-117">-Name</span><span class="sxs-lookup"><span data-stu-id="50d53-117">-Name</span></span>
<span data-ttu-id="50d53-118">Especifica o nome da configuração de IP front-end que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="50d53-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50d53-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50d53-119">CommonParameters</span></span>
<span data-ttu-id="50d53-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50d53-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50d53-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50d53-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50d53-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50d53-122">INPUTS</span></span>

### <span data-ttu-id="50d53-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50d53-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="50d53-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="50d53-124">OUTPUTS</span></span>

### <span data-ttu-id="50d53-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="50d53-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="50d53-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="50d53-126">NOTES</span></span>

## <span data-ttu-id="50d53-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="50d53-127">RELATED LINKS</span></span>

[<span data-ttu-id="50d53-128">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="50d53-128">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="50d53-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="50d53-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="50d53-130">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="50d53-130">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="50d53-131">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="50d53-131">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


