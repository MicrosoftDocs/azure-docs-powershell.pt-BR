---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: d376bc1e70d0441f139b64c19466a88daf6877c4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433466"
---
# <span data-ttu-id="9811f-101">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9811f-101">Remove-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="9811f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9811f-102">SYNOPSIS</span></span>
<span data-ttu-id="9811f-103">Remove uma configuração de IP de front-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9811f-103">Removes a front-end IP configuration from an application gateway.</span></span>

## <span data-ttu-id="9811f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9811f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9811f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9811f-105">DESCRIPTION</span></span>
<span data-ttu-id="9811f-106">O cmdlet **Remove-AzApplicationGatewayFrontendIPConfig** remove o IP de front-end de um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="9811f-106">The **Remove-AzApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="9811f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9811f-107">EXAMPLES</span></span>

### <span data-ttu-id="9811f-108">Exemplo 1: remover uma configuração de IP de front-end</span><span class="sxs-lookup"><span data-stu-id="9811f-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="9811f-109">O primeiro comando obtém um gateway do aplicativo chamado ApplicationGateway01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9811f-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9811f-110">O segundo comando Remove a configuração de IP de front-end denominada FrontEndIP02 do gateway do aplicativo armazenado em $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9811f-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="9811f-111">OS</span><span class="sxs-lookup"><span data-stu-id="9811f-111">PARAMETERS</span></span>

### <span data-ttu-id="9811f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9811f-112">-ApplicationGateway</span></span>
<span data-ttu-id="9811f-113">Especifica um gateway do aplicativo do qual remover uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="9811f-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="9811f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9811f-114">-DefaultProfile</span></span>
<span data-ttu-id="9811f-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9811f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9811f-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="9811f-116">-Name</span></span>
<span data-ttu-id="9811f-117">Especifica o nome de uma configuração de IP de front-end a ser removida.</span><span class="sxs-lookup"><span data-stu-id="9811f-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="9811f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9811f-118">CommonParameters</span></span>
<span data-ttu-id="9811f-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9811f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9811f-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9811f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9811f-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9811f-121">INPUTS</span></span>

### <span data-ttu-id="9811f-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9811f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9811f-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9811f-123">OUTPUTS</span></span>

### <span data-ttu-id="9811f-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9811f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9811f-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9811f-125">NOTES</span></span>

## <span data-ttu-id="9811f-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9811f-126">RELATED LINKS</span></span>

[<span data-ttu-id="9811f-127">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9811f-127">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="9811f-128">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9811f-128">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="9811f-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9811f-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="9811f-130">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="9811f-130">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


