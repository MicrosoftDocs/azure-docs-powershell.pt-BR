---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 465567242c0ff13ea695c767cf1dda7f04f54174
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775604"
---
# <span data-ttu-id="39824-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="39824-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="39824-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="39824-102">SYNOPSIS</span></span>
<span data-ttu-id="39824-103">Obtém um certificado de autenticação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="39824-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="39824-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39824-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39824-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="39824-105">DESCRIPTION</span></span>
<span data-ttu-id="39824-106">O cmdlet **Get-AzApplicationGatewayAuthenticationCertificate** Obtém um certificado de autenticação para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="39824-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="39824-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="39824-107">EXAMPLES</span></span>

### <span data-ttu-id="39824-108">1:</span><span class="sxs-lookup"><span data-stu-id="39824-108">1:</span></span>
```

```

## <span data-ttu-id="39824-109">OS</span><span class="sxs-lookup"><span data-stu-id="39824-109">PARAMETERS</span></span>

### <span data-ttu-id="39824-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="39824-110">-ApplicationGateway</span></span>
<span data-ttu-id="39824-111">Especifica o nome do gateway do aplicativo para o qual esse cmdlet obtém um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="39824-111">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="39824-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39824-112">-DefaultProfile</span></span>
<span data-ttu-id="39824-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="39824-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39824-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="39824-114">-Name</span></span>
<span data-ttu-id="39824-115">Especifica o nome do certificado de autenticação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="39824-115">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39824-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39824-116">CommonParameters</span></span>
<span data-ttu-id="39824-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39824-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39824-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39824-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39824-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="39824-119">INPUTS</span></span>

### <span data-ttu-id="39824-120">System. String</span><span class="sxs-lookup"><span data-stu-id="39824-120">System.String</span></span>

## <span data-ttu-id="39824-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="39824-121">OUTPUTS</span></span>

### <span data-ttu-id="39824-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="39824-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="39824-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="39824-123">NOTES</span></span>
* <span data-ttu-id="39824-124">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="39824-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="39824-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="39824-125">RELATED LINKS</span></span>

[<span data-ttu-id="39824-126">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="39824-126">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="39824-127">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="39824-127">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="39824-128">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="39824-128">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="39824-129">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="39824-129">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


