---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 6652da4491bc503ecc2d0c8ee016416cefbff172
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775668"
---
# <span data-ttu-id="ae939-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ae939-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="ae939-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae939-102">SYNOPSIS</span></span>
<span data-ttu-id="ae939-103">Adiciona um certificado de autenticação a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ae939-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="ae939-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae939-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae939-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae939-105">DESCRIPTION</span></span>
<span data-ttu-id="ae939-106">O cmdlet **Add-AzApplicationGatewayAuthenticationCertificate** adiciona um certificado de autenticação a um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="ae939-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="ae939-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae939-107">EXAMPLES</span></span>

### <span data-ttu-id="ae939-108">1:</span><span class="sxs-lookup"><span data-stu-id="ae939-108">1:</span></span>
```

```

## <span data-ttu-id="ae939-109">OS</span><span class="sxs-lookup"><span data-stu-id="ae939-109">PARAMETERS</span></span>

### <span data-ttu-id="ae939-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae939-110">-ApplicationGateway</span></span>
<span data-ttu-id="ae939-111">Especifica o nome do gateway do aplicativo para o qual esse cmdlet adiciona um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="ae939-111">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="ae939-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="ae939-112">-CertificateFile</span></span>
<span data-ttu-id="ae939-113">Especifica o caminho do certificado de autenticação que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="ae939-113">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="ae939-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae939-114">-DefaultProfile</span></span>
<span data-ttu-id="ae939-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae939-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae939-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae939-116">-Name</span></span>
<span data-ttu-id="ae939-117">Especifica o nome de um certificado que o cmdlet adiciona ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ae939-117">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="ae939-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ae939-118">-Confirm</span></span>
<span data-ttu-id="ae939-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae939-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae939-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae939-120">-WhatIf</span></span>
<span data-ttu-id="ae939-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae939-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae939-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae939-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae939-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae939-123">CommonParameters</span></span>
<span data-ttu-id="ae939-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae939-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae939-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae939-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae939-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae939-126">INPUTS</span></span>

### <span data-ttu-id="ae939-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ae939-127">System.String</span></span>

## <span data-ttu-id="ae939-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae939-128">OUTPUTS</span></span>

### <span data-ttu-id="ae939-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae939-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ae939-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae939-130">NOTES</span></span>
* <span data-ttu-id="ae939-131">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="ae939-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ae939-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae939-132">RELATED LINKS</span></span>

[<span data-ttu-id="ae939-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ae939-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ae939-134">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ae939-134">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ae939-135">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ae939-135">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ae939-136">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ae939-136">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


