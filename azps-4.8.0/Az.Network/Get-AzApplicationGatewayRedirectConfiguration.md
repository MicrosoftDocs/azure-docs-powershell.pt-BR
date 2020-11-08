---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 8a49bdeed095ee277d632559402c55ca3baf784c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112507"
---
# <span data-ttu-id="bfe6e-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfe6e-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="bfe6e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bfe6e-102">SYNOPSIS</span></span>
<span data-ttu-id="bfe6e-103">Obtém uma configuração de redirecionamento existente de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="bfe6e-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="bfe6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bfe6e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfe6e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bfe6e-105">DESCRIPTION</span></span>
<span data-ttu-id="bfe6e-106">O cmdlet **Get-AzApplicationGatewayRedirectConfiguration** Obtém uma configuração de redirecionamento existente de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="bfe6e-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="bfe6e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bfe6e-107">EXAMPLES</span></span>

### <span data-ttu-id="bfe6e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bfe6e-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="bfe6e-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="bfe6e-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="bfe6e-110">O segundo comando obtém a configuração de redirecionamento chamada Redirect01 do gateway do aplicativo armazenado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="bfe6e-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="bfe6e-111">OS</span><span class="sxs-lookup"><span data-stu-id="bfe6e-111">PARAMETERS</span></span>

### <span data-ttu-id="bfe6e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bfe6e-112">-ApplicationGateway</span></span>
<span data-ttu-id="bfe6e-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="bfe6e-113">The applicationGateway</span></span>

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

### <span data-ttu-id="bfe6e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfe6e-114">-DefaultProfile</span></span>
<span data-ttu-id="bfe6e-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bfe6e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfe6e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="bfe6e-116">-Name</span></span>
<span data-ttu-id="bfe6e-117">O nome da regra de roteamento de solicitação</span><span class="sxs-lookup"><span data-stu-id="bfe6e-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="bfe6e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfe6e-118">CommonParameters</span></span>
<span data-ttu-id="bfe6e-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfe6e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfe6e-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bfe6e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfe6e-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bfe6e-121">INPUTS</span></span>

### <span data-ttu-id="bfe6e-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bfe6e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bfe6e-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bfe6e-123">OUTPUTS</span></span>

### <span data-ttu-id="bfe6e-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfe6e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="bfe6e-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bfe6e-125">NOTES</span></span>

## <span data-ttu-id="bfe6e-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfe6e-126">RELATED LINKS</span></span>

[<span data-ttu-id="bfe6e-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfe6e-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="bfe6e-128">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfe6e-128">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="bfe6e-129">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfe6e-129">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="bfe6e-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfe6e-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
