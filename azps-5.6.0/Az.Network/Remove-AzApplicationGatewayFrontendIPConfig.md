---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 0c226cf7dabbc170e137f1a809cee0afe3c7e76f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890599"
---
# <span data-ttu-id="ef5e6-101">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ef5e6-101">Remove-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="ef5e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef5e6-102">SYNOPSIS</span></span>
<span data-ttu-id="ef5e6-103">Remove uma configuração de IP front-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ef5e6-103">Removes a front-end IP configuration from an application gateway.</span></span>

## <span data-ttu-id="ef5e6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ef5e6-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef5e6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ef5e6-105">DESCRIPTION</span></span>
<span data-ttu-id="ef5e6-106">O cmdlet **Remove-AzApplicationGatewayFrontendIPConfig** remove o IP frontend de um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="ef5e6-106">The **Remove-AzApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="ef5e6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef5e6-107">EXAMPLES</span></span>

### <span data-ttu-id="ef5e6-108">Exemplo 1: Remover uma configuração de IP front-end</span><span class="sxs-lookup"><span data-stu-id="ef5e6-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="ef5e6-109">O primeiro comando obtém um gateway de aplicativo chamado ApplicationGateway01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ef5e6-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ef5e6-110">O segundo comando remove a configuração de IP front-end chamada FrontEndIP02 do gateway de aplicativo armazenado em $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ef5e6-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="ef5e6-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ef5e6-111">PARAMETERS</span></span>

### <span data-ttu-id="ef5e6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef5e6-112">-ApplicationGateway</span></span>
<span data-ttu-id="ef5e6-113">Especifica um gateway de aplicativo do qual remover uma configuração de IP front-end.</span><span class="sxs-lookup"><span data-stu-id="ef5e6-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="ef5e6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef5e6-114">-DefaultProfile</span></span>
<span data-ttu-id="ef5e6-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ef5e6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef5e6-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ef5e6-116">-Name</span></span>
<span data-ttu-id="ef5e6-117">Especifica o nome de uma configuração de IP front-end a ser removido.</span><span class="sxs-lookup"><span data-stu-id="ef5e6-117">Specifies the name of a front-end IP configuration to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef5e6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef5e6-118">CommonParameters</span></span>
<span data-ttu-id="ef5e6-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef5e6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef5e6-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef5e6-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef5e6-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef5e6-121">INPUTS</span></span>

### <span data-ttu-id="ef5e6-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef5e6-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ef5e6-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ef5e6-123">OUTPUTS</span></span>

### <span data-ttu-id="ef5e6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef5e6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ef5e6-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="ef5e6-125">NOTES</span></span>

## <span data-ttu-id="ef5e6-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef5e6-126">RELATED LINKS</span></span>

[<span data-ttu-id="ef5e6-127">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ef5e6-127">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ef5e6-128">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ef5e6-128">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ef5e6-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ef5e6-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ef5e6-130">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ef5e6-130">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


