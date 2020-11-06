---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 271eaf702165c3c1e80243efa080b3e4d981390d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432195"
---
# <span data-ttu-id="ed03c-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ed03c-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="ed03c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed03c-102">SYNOPSIS</span></span>
<span data-ttu-id="ed03c-103">Adiciona um certificado de autenticação a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ed03c-103">Adds an authentication certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed03c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed03c-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed03c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ed03c-105">DESCRIPTION</span></span>
<span data-ttu-id="ed03c-106">O cmdlet **Add-AzureRmApplicationGatewayAuthenticationCertificate** adiciona um certificado de autenticação a um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="ed03c-106">The **Add-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="ed03c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed03c-107">EXAMPLES</span></span>

## <span data-ttu-id="ed03c-108">OS</span><span class="sxs-lookup"><span data-stu-id="ed03c-108">PARAMETERS</span></span>

### <span data-ttu-id="ed03c-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ed03c-109">-ApplicationGateway</span></span>
<span data-ttu-id="ed03c-110">Especifica o nome do gateway do aplicativo para o qual esse cmdlet adiciona um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="ed03c-110">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="ed03c-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="ed03c-111">-CertificateFile</span></span>
<span data-ttu-id="ed03c-112">Especifica o caminho do certificado de autenticação que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="ed03c-112">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="ed03c-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed03c-113">-Name</span></span>
<span data-ttu-id="ed03c-114">Especifica o nome de um certificado que o cmdlet adiciona ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ed03c-114">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="ed03c-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ed03c-115">-Confirm</span></span>
<span data-ttu-id="ed03c-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed03c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed03c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed03c-117">-WhatIf</span></span>
<span data-ttu-id="ed03c-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ed03c-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed03c-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ed03c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed03c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed03c-120">-DefaultProfile</span></span>
<span data-ttu-id="ed03c-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed03c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed03c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed03c-122">CommonParameters</span></span>
<span data-ttu-id="ed03c-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed03c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed03c-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed03c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed03c-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ed03c-125">INPUTS</span></span>

### <span data-ttu-id="ed03c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ed03c-126">System.String</span></span>

## <span data-ttu-id="ed03c-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ed03c-127">OUTPUTS</span></span>

### <span data-ttu-id="ed03c-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ed03c-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ed03c-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ed03c-129">NOTES</span></span>
* <span data-ttu-id="ed03c-130">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="ed03c-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ed03c-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed03c-131">RELATED LINKS</span></span>

[<span data-ttu-id="ed03c-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ed03c-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ed03c-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ed03c-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ed03c-134">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ed03c-134">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ed03c-135">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ed03c-135">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


