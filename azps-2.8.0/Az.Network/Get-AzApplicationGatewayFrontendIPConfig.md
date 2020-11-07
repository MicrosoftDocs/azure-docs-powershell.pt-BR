---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 88393e7c40ba9888602f144410263e7210a3db9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772059"
---
# <span data-ttu-id="0e64c-101">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0e64c-101">Get-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="0e64c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e64c-102">SYNOPSIS</span></span>
<span data-ttu-id="0e64c-103">Obtém a configuração de IP de front-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0e64c-103">Gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="0e64c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e64c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e64c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0e64c-105">DESCRIPTION</span></span>
<span data-ttu-id="0e64c-106">O cmdlet **Get-AzApplicationGatewayFrontendIPConfig** Obtém a configuração de IP de front-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0e64c-106">The **Get-AzApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="0e64c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0e64c-107">EXAMPLES</span></span>

### <span data-ttu-id="0e64c-108">Exemplo 1: obter uma configuração de IP front-end especificada</span><span class="sxs-lookup"><span data-stu-id="0e64c-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="0e64c-109">O primeiro comando obtém um gateway do aplicativo denominado ApplicationGateway01 do grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando obtém a configuração de IP de front-end chamada FrontEndIP01 da $AppGw e a armazena na variável $FrontEndIP.</span><span class="sxs-lookup"><span data-stu-id="0e64c-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="0e64c-110">Exemplo 2: obter uma lista de configurações de IP front-end</span><span class="sxs-lookup"><span data-stu-id="0e64c-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="0e64c-111">O primeiro comando obtém um gateway do aplicativo denominado ApplicationGateway01 do grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando obtém uma lista das configurações de IP de front-end da $AppGw e a armazena na variável $FrontEndIPs.</span><span class="sxs-lookup"><span data-stu-id="0e64c-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="0e64c-112">OS</span><span class="sxs-lookup"><span data-stu-id="0e64c-112">PARAMETERS</span></span>

### <span data-ttu-id="0e64c-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e64c-113">-ApplicationGateway</span></span>
<span data-ttu-id="0e64c-114">Especifica o objeto do gateway do aplicativo que contém a configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="0e64c-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="0e64c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e64c-115">-DefaultProfile</span></span>
<span data-ttu-id="0e64c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0e64c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e64c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e64c-117">-Name</span></span>
<span data-ttu-id="0e64c-118">Especifica o nome da configuração de IP de front-end que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="0e64c-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0e64c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e64c-119">CommonParameters</span></span>
<span data-ttu-id="0e64c-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e64c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e64c-121">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e64c-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e64c-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0e64c-122">INPUTS</span></span>

### <span data-ttu-id="0e64c-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e64c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0e64c-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0e64c-124">OUTPUTS</span></span>

### <span data-ttu-id="0e64c-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e64c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="0e64c-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0e64c-126">NOTES</span></span>

## <span data-ttu-id="0e64c-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e64c-127">RELATED LINKS</span></span>

[<span data-ttu-id="0e64c-128">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0e64c-128">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="0e64c-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0e64c-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="0e64c-130">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0e64c-130">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="0e64c-131">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="0e64c-131">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)

