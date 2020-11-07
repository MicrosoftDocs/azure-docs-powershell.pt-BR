---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 1743ed0427fdc0dd952c9b86d51c13c3ed855620
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771816"
---
# <span data-ttu-id="26bad-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="26bad-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="26bad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="26bad-102">SYNOPSIS</span></span>
<span data-ttu-id="26bad-103">Obtém um certificado de autenticação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="26bad-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="26bad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26bad-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26bad-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="26bad-105">DESCRIPTION</span></span>
<span data-ttu-id="26bad-106">O cmdlet **Get-AzApplicationGatewayAuthenticationCertificate** Obtém um certificado de autenticação para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="26bad-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="26bad-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="26bad-107">EXAMPLES</span></span>

### <span data-ttu-id="26bad-108">Exemplo 1: obter um certificado de autenticação especificado</span><span class="sxs-lookup"><span data-stu-id="26bad-108">Example 1: Get a specified authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -Name "pool01" -ApplicationGateway $appgw
```

<span data-ttu-id="26bad-109">O primeiro comando obtém o gateway do aplicativo chamado appGwName e o armazena na variável $appgw.</span><span class="sxs-lookup"><span data-stu-id="26bad-109">The first command gets the application gateway named appGwName and stores it in the $appgw variable.</span></span>
<span data-ttu-id="26bad-110">O segundo comando obtém o certificado de autenticação chamado pool01 e o armazena na variável $pool.</span><span class="sxs-lookup"><span data-stu-id="26bad-110">The second command gets the authentication certificate named pool01 and stores it in the $pool variable.</span></span>

## <span data-ttu-id="26bad-111">OS</span><span class="sxs-lookup"><span data-stu-id="26bad-111">PARAMETERS</span></span>

### <span data-ttu-id="26bad-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26bad-112">-ApplicationGateway</span></span>
<span data-ttu-id="26bad-113">Especifica o nome do gateway do aplicativo para o qual esse cmdlet obtém um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="26bad-113">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="26bad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26bad-114">-DefaultProfile</span></span>
<span data-ttu-id="26bad-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="26bad-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26bad-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="26bad-116">-Name</span></span>
<span data-ttu-id="26bad-117">Especifica o nome do certificado de autenticação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="26bad-117">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="26bad-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26bad-118">CommonParameters</span></span>
<span data-ttu-id="26bad-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26bad-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26bad-120">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26bad-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26bad-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="26bad-121">INPUTS</span></span>

### <span data-ttu-id="26bad-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26bad-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="26bad-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="26bad-123">OUTPUTS</span></span>

### <span data-ttu-id="26bad-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="26bad-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="26bad-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="26bad-125">NOTES</span></span>
* <span data-ttu-id="26bad-126">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="26bad-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="26bad-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26bad-127">RELATED LINKS</span></span>

[<span data-ttu-id="26bad-128">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="26bad-128">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="26bad-129">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="26bad-129">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="26bad-130">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="26bad-130">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="26bad-131">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="26bad-131">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


