---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: fe21bc83fce1e43e036f68ea64c8a10cf2f3c90e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264037"
---
# <span data-ttu-id="3344b-101">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="3344b-101">Remove-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="3344b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3344b-102">SYNOPSIS</span></span>
<span data-ttu-id="3344b-103">Remove uma porta de front-end de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="3344b-103">Removes a front-end port from an application gateway.</span></span>

## <span data-ttu-id="3344b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3344b-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3344b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3344b-105">DESCRIPTION</span></span>
<span data-ttu-id="3344b-106">O cmdlet **Remove-AzApplicationGatewayFrontendPort** remove uma porta de front-end de um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="3344b-106">The **Remove-AzApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="3344b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3344b-107">EXAMPLES</span></span>

### <span data-ttu-id="3344b-108">Exemplo: remover uma porta de front-end de um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="3344b-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="3344b-109">O primeiro comando obtém um gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e armazena o gateway em $AppGw variável.</span><span class="sxs-lookup"><span data-stu-id="3344b-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>
<span data-ttu-id="3344b-110">O segundo comando Remove a porta nomeada FrontEndPort02 do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3344b-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="3344b-111">OS</span><span class="sxs-lookup"><span data-stu-id="3344b-111">PARAMETERS</span></span>

### <span data-ttu-id="3344b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3344b-112">-ApplicationGateway</span></span>
<span data-ttu-id="3344b-113">Especifica o gateway do aplicativo do qual você deseja remover uma porta de front-end.</span><span class="sxs-lookup"><span data-stu-id="3344b-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="3344b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3344b-114">-DefaultProfile</span></span>
<span data-ttu-id="3344b-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3344b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3344b-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="3344b-116">-Name</span></span>
<span data-ttu-id="3344b-117">Especifica o nome da porta de front-end a ser removida.</span><span class="sxs-lookup"><span data-stu-id="3344b-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="3344b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3344b-118">CommonParameters</span></span>
<span data-ttu-id="3344b-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3344b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3344b-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3344b-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3344b-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3344b-121">INPUTS</span></span>

### <span data-ttu-id="3344b-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3344b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3344b-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3344b-123">OUTPUTS</span></span>

### <span data-ttu-id="3344b-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3344b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3344b-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3344b-125">NOTES</span></span>

## <span data-ttu-id="3344b-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3344b-126">RELATED LINKS</span></span>

[<span data-ttu-id="3344b-127">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="3344b-127">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="3344b-128">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="3344b-128">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="3344b-129">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="3344b-129">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="3344b-130">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="3344b-130">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


