---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: fe21bc83fce1e43e036f68ea64c8a10cf2f3c90e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111605"
---
# <span data-ttu-id="a68d3-101">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a68d3-101">Remove-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="a68d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a68d3-102">SYNOPSIS</span></span>
<span data-ttu-id="a68d3-103">Remove uma porta front-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a68d3-103">Removes a front-end port from an application gateway.</span></span>

## <span data-ttu-id="a68d3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a68d3-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a68d3-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a68d3-105">DESCRIPTION</span></span>
<span data-ttu-id="a68d3-106">O cmdlet **Remove-AzApplicationGatewayFrontendPort** remove uma porta front-end de um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="a68d3-106">The **Remove-AzApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="a68d3-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a68d3-107">EXAMPLES</span></span>

### <span data-ttu-id="a68d3-108">Exemplo: Remover uma porta front-end de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="a68d3-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="a68d3-109">O primeiro comando obtém um gateway de aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e armazena o gateway na $AppGw variável.</span><span class="sxs-lookup"><span data-stu-id="a68d3-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>
<span data-ttu-id="a68d3-110">O segundo comando remove a porta chamada FrontEndPort02 do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a68d3-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="a68d3-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a68d3-111">PARAMETERS</span></span>

### <span data-ttu-id="a68d3-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a68d3-112">-ApplicationGateway</span></span>
<span data-ttu-id="a68d3-113">Especifica o gateway de aplicativo do qual remover uma porta front-end.</span><span class="sxs-lookup"><span data-stu-id="a68d3-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="a68d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a68d3-114">-DefaultProfile</span></span>
<span data-ttu-id="a68d3-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a68d3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a68d3-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a68d3-116">-Name</span></span>
<span data-ttu-id="a68d3-117">Especifica o nome da porta frontend a ser removido.</span><span class="sxs-lookup"><span data-stu-id="a68d3-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="a68d3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a68d3-118">CommonParameters</span></span>
<span data-ttu-id="a68d3-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a68d3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a68d3-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a68d3-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a68d3-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="a68d3-121">INPUTS</span></span>

### <span data-ttu-id="a68d3-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a68d3-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a68d3-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="a68d3-123">OUTPUTS</span></span>

### <span data-ttu-id="a68d3-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a68d3-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a68d3-125">Notas</span><span class="sxs-lookup"><span data-stu-id="a68d3-125">NOTES</span></span>

## <span data-ttu-id="a68d3-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a68d3-126">RELATED LINKS</span></span>

[<span data-ttu-id="a68d3-127">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a68d3-127">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="a68d3-128">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a68d3-128">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="a68d3-129">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a68d3-129">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="a68d3-130">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a68d3-130">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


