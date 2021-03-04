---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 4b28feb85ebc8f4d5669f28609aa4723061c1709
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890598"
---
# <span data-ttu-id="614b2-101">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="614b2-101">Remove-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="614b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="614b2-102">SYNOPSIS</span></span>
<span data-ttu-id="614b2-103">Remove uma porta front-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="614b2-103">Removes a front-end port from an application gateway.</span></span>

## <span data-ttu-id="614b2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="614b2-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="614b2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="614b2-105">DESCRIPTION</span></span>
<span data-ttu-id="614b2-106">O cmdlet **Remove-AzApplicationGatewayFrontendPort** remove uma porta front-end de um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="614b2-106">The **Remove-AzApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="614b2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="614b2-107">EXAMPLES</span></span>

### <span data-ttu-id="614b2-108">Exemplo: remover uma porta front-end de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="614b2-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="614b2-109">O primeiro comando obtém um gateway de aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e armazena o gateway $AppGw variável.</span><span class="sxs-lookup"><span data-stu-id="614b2-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>
<span data-ttu-id="614b2-110">O segundo comando remove a porta chamada FrontEndPort02 do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="614b2-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="614b2-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="614b2-111">PARAMETERS</span></span>

### <span data-ttu-id="614b2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="614b2-112">-ApplicationGateway</span></span>
<span data-ttu-id="614b2-113">Especifica o gateway de aplicativo do qual remover uma porta front-end.</span><span class="sxs-lookup"><span data-stu-id="614b2-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="614b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="614b2-114">-DefaultProfile</span></span>
<span data-ttu-id="614b2-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="614b2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="614b2-116">-Name</span><span class="sxs-lookup"><span data-stu-id="614b2-116">-Name</span></span>
<span data-ttu-id="614b2-117">Especifica o nome da porta front-end a ser removido.</span><span class="sxs-lookup"><span data-stu-id="614b2-117">Specifies name of the frontend port to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="614b2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="614b2-118">CommonParameters</span></span>
<span data-ttu-id="614b2-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="614b2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="614b2-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="614b2-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="614b2-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="614b2-121">INPUTS</span></span>

### <span data-ttu-id="614b2-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="614b2-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="614b2-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="614b2-123">OUTPUTS</span></span>

### <span data-ttu-id="614b2-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="614b2-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="614b2-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="614b2-125">NOTES</span></span>

## <span data-ttu-id="614b2-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="614b2-126">RELATED LINKS</span></span>

[<span data-ttu-id="614b2-127">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="614b2-127">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="614b2-128">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="614b2-128">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="614b2-129">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="614b2-129">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="614b2-130">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="614b2-130">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


