---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 8b19edba06f41d4e1e7cf3c95dd1a52fa00f09e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433229"
---
# <span data-ttu-id="b9fc4-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b9fc4-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="b9fc4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9fc4-102">SYNOPSIS</span></span>
<span data-ttu-id="b9fc4-103">Adiciona um certificado de autenticação a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b9fc4-103">Adds an authentication certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9fc4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9fc4-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9fc4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9fc4-105">DESCRIPTION</span></span>
<span data-ttu-id="b9fc4-106">O cmdlet **Add-AzureRmApplicationGatewayAuthenticationCertificate** adiciona um certificado de autenticação a um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="b9fc4-106">The **Add-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="b9fc4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9fc4-107">EXAMPLES</span></span>

## <span data-ttu-id="b9fc4-108">OS</span><span class="sxs-lookup"><span data-stu-id="b9fc4-108">PARAMETERS</span></span>

### <span data-ttu-id="b9fc4-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9fc4-109">-ApplicationGateway</span></span>
<span data-ttu-id="b9fc4-110">Especifica o nome do gateway do aplicativo para o qual esse cmdlet adiciona um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="b9fc4-110">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="b9fc4-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b9fc4-111">-CertificateFile</span></span>
<span data-ttu-id="b9fc4-112">Especifica o caminho do certificado de autenticação que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="b9fc4-112">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="b9fc4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9fc4-113">-DefaultProfile</span></span>
<span data-ttu-id="b9fc4-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9fc4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9fc4-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9fc4-115">-Name</span></span>
<span data-ttu-id="b9fc4-116">Especifica o nome de um certificado que o cmdlet adiciona ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b9fc4-116">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="b9fc4-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b9fc4-117">-Confirm</span></span>
<span data-ttu-id="b9fc4-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9fc4-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9fc4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9fc4-119">-WhatIf</span></span>
<span data-ttu-id="b9fc4-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b9fc4-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9fc4-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b9fc4-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9fc4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9fc4-122">CommonParameters</span></span>
<span data-ttu-id="b9fc4-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9fc4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9fc4-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9fc4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9fc4-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9fc4-125">INPUTS</span></span>

### <span data-ttu-id="b9fc4-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9fc4-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="b9fc4-127">Parâmetros: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b9fc4-127">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="b9fc4-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9fc4-128">OUTPUTS</span></span>

### <span data-ttu-id="b9fc4-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9fc4-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9fc4-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9fc4-130">NOTES</span></span>
* <span data-ttu-id="b9fc4-131">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="b9fc4-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b9fc4-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9fc4-132">RELATED LINKS</span></span>

[<span data-ttu-id="b9fc4-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b9fc4-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b9fc4-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b9fc4-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b9fc4-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b9fc4-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b9fc4-136">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b9fc4-136">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


