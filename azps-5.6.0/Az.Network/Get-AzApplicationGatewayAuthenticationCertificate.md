---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 7f5dbd73158e5328ece78b1064a78ff5c4627035
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886736"
---
# <span data-ttu-id="07523-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="07523-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="07523-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07523-102">SYNOPSIS</span></span>
<span data-ttu-id="07523-103">Obtém um certificado de autenticação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="07523-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="07523-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="07523-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07523-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="07523-105">DESCRIPTION</span></span>
<span data-ttu-id="07523-106">O cmdlet **Get-AzApplicationGatewayAuthenticationCertificate** obtém um certificado de autenticação para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="07523-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="07523-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07523-107">EXAMPLES</span></span>

### <span data-ttu-id="07523-108">Exemplo 1: Obter um certificado de autenticação especificado</span><span class="sxs-lookup"><span data-stu-id="07523-108">Example 1: Get a specified authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $cert = Get-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -ApplicationGateway $appgw
```

<span data-ttu-id="07523-109">O primeiro comando obtém o gateway de aplicativo chamado appGwName e o armazena na variável $appgw de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="07523-109">The first command gets the application gateway named appGwName and stores it in the $appgw variable.</span></span>
<span data-ttu-id="07523-110">O segundo comando obtém o certificado de autenticação chamado cert01 e o armazena na variável $cert de autenticação.</span><span class="sxs-lookup"><span data-stu-id="07523-110">The second command gets the authentication certificate named cert01 and stores it in the $cert variable.</span></span>

## <span data-ttu-id="07523-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="07523-111">PARAMETERS</span></span>

### <span data-ttu-id="07523-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07523-112">-ApplicationGateway</span></span>
<span data-ttu-id="07523-113">Especifica o nome do gateway de aplicativo para o qual este cmdlet obtém um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="07523-113">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="07523-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07523-114">-DefaultProfile</span></span>
<span data-ttu-id="07523-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="07523-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07523-116">-Name</span><span class="sxs-lookup"><span data-stu-id="07523-116">-Name</span></span>
<span data-ttu-id="07523-117">Especifica o nome do certificado de autenticação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="07523-117">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="07523-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07523-118">CommonParameters</span></span>
<span data-ttu-id="07523-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07523-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07523-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07523-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07523-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07523-121">INPUTS</span></span>

### <span data-ttu-id="07523-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07523-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="07523-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="07523-123">OUTPUTS</span></span>

### <span data-ttu-id="07523-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="07523-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="07523-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="07523-125">NOTES</span></span>
* <span data-ttu-id="07523-126">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="07523-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="07523-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07523-127">RELATED LINKS</span></span>

[<span data-ttu-id="07523-128">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="07523-128">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="07523-129">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="07523-129">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="07523-130">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="07523-130">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="07523-131">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="07523-131">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


