---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 00d5d84f3f9895aec42f9728de6eec1bf2ff9b06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114197"
---
# <span data-ttu-id="c7195-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c7195-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="c7195-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7195-102">SYNOPSIS</span></span>
<span data-ttu-id="c7195-103">Obtém um certificado de autenticação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7195-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="c7195-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7195-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7195-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c7195-105">DESCRIPTION</span></span>
<span data-ttu-id="c7195-106">O cmdlet **Get-AzApplicationGatewayAuthenticationCertificate** recebe um certificado de autenticação para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="c7195-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="c7195-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c7195-107">EXAMPLES</span></span>

### <span data-ttu-id="c7195-108">Exemplo 1: obter um certificado de autenticação especificado</span><span class="sxs-lookup"><span data-stu-id="c7195-108">Example 1: Get a specified authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $cert = Get-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -ApplicationGateway $appgw
```

<span data-ttu-id="c7195-109">O primeiro comando obtém o gateway do aplicativo chamado appGwName e o armazena na variável $appgw aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7195-109">The first command gets the application gateway named appGwName and stores it in the $appgw variable.</span></span>
<span data-ttu-id="c7195-110">O segundo comando obtém o certificado de autenticação chamado cert01 e o armazena na variável $cert dados.</span><span class="sxs-lookup"><span data-stu-id="c7195-110">The second command gets the authentication certificate named cert01 and stores it in the $cert variable.</span></span>

## <span data-ttu-id="c7195-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7195-111">PARAMETERS</span></span>

### <span data-ttu-id="c7195-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c7195-112">-ApplicationGateway</span></span>
<span data-ttu-id="c7195-113">Especifica o nome do gateway de aplicativo para o qual este cmdlet recebe um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="c7195-113">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="c7195-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7195-114">-DefaultProfile</span></span>
<span data-ttu-id="c7195-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c7195-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7195-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7195-116">-Name</span></span>
<span data-ttu-id="c7195-117">Especifica o nome do certificado de autenticação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="c7195-117">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c7195-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7195-118">CommonParameters</span></span>
<span data-ttu-id="c7195-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7195-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7195-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7195-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7195-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="c7195-121">INPUTS</span></span>

### <span data-ttu-id="c7195-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c7195-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c7195-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="c7195-123">OUTPUTS</span></span>

### <span data-ttu-id="c7195-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c7195-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="c7195-125">Notas</span><span class="sxs-lookup"><span data-stu-id="c7195-125">NOTES</span></span>
* <span data-ttu-id="c7195-126">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="c7195-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c7195-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7195-127">RELATED LINKS</span></span>

[<span data-ttu-id="c7195-128">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c7195-128">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c7195-129">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c7195-129">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c7195-130">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c7195-130">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c7195-131">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c7195-131">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


