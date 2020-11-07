---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 033ca62f766f854be27ad75a6b63a8f883ba58d0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786485"
---
# <span data-ttu-id="c7a60-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c7a60-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="c7a60-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7a60-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a60-103">Obtém um certificado de autenticação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7a60-103">Gets an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7a60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7a60-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7a60-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c7a60-105">DESCRIPTION</span></span>
<span data-ttu-id="c7a60-106">O cmdlet **Get-AzureRmApplicationGatewayAuthenticationCertificate** Obtém um certificado de autenticação para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="c7a60-106">The **Get-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="c7a60-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7a60-107">EXAMPLES</span></span>

### <span data-ttu-id="c7a60-108">1:</span><span class="sxs-lookup"><span data-stu-id="c7a60-108">1:</span></span>
```

```

## <span data-ttu-id="c7a60-109">OS</span><span class="sxs-lookup"><span data-stu-id="c7a60-109">PARAMETERS</span></span>

### <span data-ttu-id="c7a60-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c7a60-110">-ApplicationGateway</span></span>
<span data-ttu-id="c7a60-111">Especifica o nome do gateway do aplicativo para o qual esse cmdlet obtém um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="c7a60-111">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="c7a60-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a60-112">-DefaultProfile</span></span>
<span data-ttu-id="c7a60-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c7a60-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7a60-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7a60-114">-Name</span></span>
<span data-ttu-id="c7a60-115">Especifica o nome do certificado de autenticação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="c7a60-115">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c7a60-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a60-116">CommonParameters</span></span>
<span data-ttu-id="c7a60-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7a60-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a60-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7a60-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a60-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c7a60-119">INPUTS</span></span>

### <span data-ttu-id="c7a60-120">System. String</span><span class="sxs-lookup"><span data-stu-id="c7a60-120">System.String</span></span>

## <span data-ttu-id="c7a60-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c7a60-121">OUTPUTS</span></span>

### <span data-ttu-id="c7a60-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c7a60-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="c7a60-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c7a60-123">NOTES</span></span>
* <span data-ttu-id="c7a60-124">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="c7a60-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c7a60-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7a60-125">RELATED LINKS</span></span>

[<span data-ttu-id="c7a60-126">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c7a60-126">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c7a60-127">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c7a60-127">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c7a60-128">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c7a60-128">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c7a60-129">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c7a60-129">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


