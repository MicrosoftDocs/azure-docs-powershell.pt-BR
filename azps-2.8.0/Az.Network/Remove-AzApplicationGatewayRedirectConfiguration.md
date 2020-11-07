---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: d75cbcbf89fde83419b9a1f97c0f66805258c82d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772308"
---
# <span data-ttu-id="59b9a-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="59b9a-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="59b9a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59b9a-102">SYNOPSIS</span></span>
<span data-ttu-id="59b9a-103">Remove uma configuração de redirecionamento de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="59b9a-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="59b9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59b9a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59b9a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="59b9a-105">DESCRIPTION</span></span>
<span data-ttu-id="59b9a-106">O cmdlet **Remove-AzApplicationGatewayRedirectConfiguration** remove uma configuração de redirecionamento de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="59b9a-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="59b9a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59b9a-107">EXAMPLES</span></span>

### <span data-ttu-id="59b9a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="59b9a-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="59b9a-109">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="59b9a-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="59b9a-110">O segundo comando Remove a configuração de redirecionamento chamada Redirect01 do gateway do aplicativo armazenado em $AppGw.</span><span class="sxs-lookup"><span data-stu-id="59b9a-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="59b9a-111">OS</span><span class="sxs-lookup"><span data-stu-id="59b9a-111">PARAMETERS</span></span>

### <span data-ttu-id="59b9a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="59b9a-112">-ApplicationGateway</span></span>
<span data-ttu-id="59b9a-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="59b9a-113">The applicationGateway</span></span>

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

### <span data-ttu-id="59b9a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59b9a-114">-DefaultProfile</span></span>
<span data-ttu-id="59b9a-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="59b9a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59b9a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="59b9a-116">-Name</span></span>
<span data-ttu-id="59b9a-117">O nome da configuração de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="59b9a-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="59b9a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59b9a-118">CommonParameters</span></span>
<span data-ttu-id="59b9a-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59b9a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59b9a-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59b9a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59b9a-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="59b9a-121">INPUTS</span></span>

### <span data-ttu-id="59b9a-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="59b9a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="59b9a-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="59b9a-123">OUTPUTS</span></span>

### <span data-ttu-id="59b9a-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="59b9a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="59b9a-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="59b9a-125">NOTES</span></span>

## <span data-ttu-id="59b9a-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59b9a-126">RELATED LINKS</span></span>

[<span data-ttu-id="59b9a-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="59b9a-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="59b9a-128">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="59b9a-128">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="59b9a-129">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="59b9a-129">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="59b9a-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="59b9a-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
