---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 4d664018592f05203c684a896f0a0701940301a6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785925"
---
# <span data-ttu-id="a0c6a-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a0c6a-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="a0c6a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0c6a-102">SYNOPSIS</span></span>
<span data-ttu-id="a0c6a-103">Adiciona um certificado de autenticação a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-103">Adds an authentication certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0c6a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0c6a-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0c6a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a0c6a-105">DESCRIPTION</span></span>
<span data-ttu-id="a0c6a-106">O cmdlet **Add-AzureRmApplicationGatewayAuthenticationCertificate** adiciona um certificado de autenticação a um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-106">The **Add-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="a0c6a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0c6a-107">EXAMPLES</span></span>

### <span data-ttu-id="a0c6a-108">1:</span><span class="sxs-lookup"><span data-stu-id="a0c6a-108">1:</span></span>
```

```

## <span data-ttu-id="a0c6a-109">OS</span><span class="sxs-lookup"><span data-stu-id="a0c6a-109">PARAMETERS</span></span>

### <span data-ttu-id="a0c6a-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0c6a-110">-ApplicationGateway</span></span>
<span data-ttu-id="a0c6a-111">Especifica o nome do gateway do aplicativo para o qual esse cmdlet adiciona um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-111">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="a0c6a-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="a0c6a-112">-CertificateFile</span></span>
<span data-ttu-id="a0c6a-113">Especifica o caminho do certificado de autenticação que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-113">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="a0c6a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0c6a-114">-DefaultProfile</span></span>
<span data-ttu-id="a0c6a-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0c6a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0c6a-116">-Name</span></span>
<span data-ttu-id="a0c6a-117">Especifica o nome de um certificado que o cmdlet adiciona ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-117">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="a0c6a-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a0c6a-118">-Confirm</span></span>
<span data-ttu-id="a0c6a-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0c6a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0c6a-120">-WhatIf</span></span>
<span data-ttu-id="a0c6a-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0c6a-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0c6a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0c6a-123">CommonParameters</span></span>
<span data-ttu-id="a0c6a-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0c6a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0c6a-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0c6a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0c6a-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a0c6a-126">INPUTS</span></span>

### <span data-ttu-id="a0c6a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a0c6a-127">System.String</span></span>

## <span data-ttu-id="a0c6a-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a0c6a-128">OUTPUTS</span></span>

### <span data-ttu-id="a0c6a-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0c6a-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a0c6a-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a0c6a-130">NOTES</span></span>
* <span data-ttu-id="a0c6a-131">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="a0c6a-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="a0c6a-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0c6a-132">RELATED LINKS</span></span>

[<span data-ttu-id="a0c6a-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a0c6a-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="a0c6a-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a0c6a-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="a0c6a-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a0c6a-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="a0c6a-136">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a0c6a-136">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


