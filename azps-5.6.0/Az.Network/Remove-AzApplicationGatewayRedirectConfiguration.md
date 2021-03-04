---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: d1364bd101a5963dfa33927ad12c43f116dd2c5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890380"
---
# <span data-ttu-id="f17d7-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f17d7-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="f17d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f17d7-102">SYNOPSIS</span></span>
<span data-ttu-id="f17d7-103">Remove uma configuração de redirecionamento de um Gateway de Aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="f17d7-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="f17d7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f17d7-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f17d7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f17d7-105">DESCRIPTION</span></span>
<span data-ttu-id="f17d7-106">O cmdlet **Remove-AzApplicationGatewayRedirectConfiguration** remove uma configuração de redirecionamento de um Gateway de Aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="f17d7-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="f17d7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f17d7-107">EXAMPLES</span></span>

### <span data-ttu-id="f17d7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f17d7-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="f17d7-109">O primeiro comando obtém um gateway de aplicativo e o armazena na $AppGw variável.</span><span class="sxs-lookup"><span data-stu-id="f17d7-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f17d7-110">O segundo comando remove a configuração de redirecionamento chamada Redirect01 do gateway de aplicativo armazenado $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f17d7-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="f17d7-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f17d7-111">PARAMETERS</span></span>

### <span data-ttu-id="f17d7-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f17d7-112">-ApplicationGateway</span></span>
<span data-ttu-id="f17d7-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f17d7-113">The applicationGateway</span></span>

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

### <span data-ttu-id="f17d7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f17d7-114">-DefaultProfile</span></span>
<span data-ttu-id="f17d7-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f17d7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f17d7-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f17d7-116">-Name</span></span>
<span data-ttu-id="f17d7-117">O nome da configuração de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="f17d7-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="f17d7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f17d7-118">CommonParameters</span></span>
<span data-ttu-id="f17d7-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f17d7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f17d7-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f17d7-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f17d7-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f17d7-121">INPUTS</span></span>

### <span data-ttu-id="f17d7-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f17d7-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f17d7-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f17d7-123">OUTPUTS</span></span>

### <span data-ttu-id="f17d7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f17d7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f17d7-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="f17d7-125">NOTES</span></span>

## <span data-ttu-id="f17d7-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f17d7-126">RELATED LINKS</span></span>

[<span data-ttu-id="f17d7-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f17d7-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="f17d7-128">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f17d7-128">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="f17d7-129">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f17d7-129">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="f17d7-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f17d7-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
