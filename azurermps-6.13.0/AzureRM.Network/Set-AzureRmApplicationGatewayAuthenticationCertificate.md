---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: d8f2fcb875503b6d6a8063007926690ef682bdc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440319"
---
# <span data-ttu-id="de95b-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="de95b-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="de95b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de95b-102">SYNOPSIS</span></span>
<span data-ttu-id="de95b-103">Atualiza um certificado de autenticação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="de95b-103">Updates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de95b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de95b-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de95b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de95b-105">DESCRIPTION</span></span>
<span data-ttu-id="de95b-106">O cmdlet **set-AzureRmApplicationGatewayAuthenticationCertificate** atualiza um certificado de autenticação para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="de95b-106">The **Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="de95b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de95b-107">EXAMPLES</span></span>

## <span data-ttu-id="de95b-108">OS</span><span class="sxs-lookup"><span data-stu-id="de95b-108">PARAMETERS</span></span>

### <span data-ttu-id="de95b-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="de95b-109">-ApplicationGateway</span></span>
<span data-ttu-id="de95b-110">Especifica o nome do gateway do aplicativo para o qual esse cmdlet atualiza um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="de95b-110">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="de95b-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="de95b-111">-CertificateFile</span></span>
<span data-ttu-id="de95b-112">Especifica o caminho do arquivo de certificado de autenticação com o qual esse cmdlet atualiza o certificado.</span><span class="sxs-lookup"><span data-stu-id="de95b-112">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="de95b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de95b-113">-DefaultProfile</span></span>
<span data-ttu-id="de95b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de95b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de95b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="de95b-115">-Name</span></span>
<span data-ttu-id="de95b-116">Especifica o nome do certificado de autenticação que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="de95b-116">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="de95b-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="de95b-117">-Confirm</span></span>
<span data-ttu-id="de95b-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de95b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de95b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de95b-119">-WhatIf</span></span>
<span data-ttu-id="de95b-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="de95b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de95b-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="de95b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de95b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de95b-122">CommonParameters</span></span>
<span data-ttu-id="de95b-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de95b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de95b-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de95b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de95b-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de95b-125">INPUTS</span></span>

### <span data-ttu-id="de95b-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="de95b-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="de95b-127">Parâmetros: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="de95b-127">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="de95b-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de95b-128">OUTPUTS</span></span>

### <span data-ttu-id="de95b-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="de95b-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="de95b-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de95b-130">NOTES</span></span>
* <span data-ttu-id="de95b-131">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="de95b-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="de95b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de95b-132">RELATED LINKS</span></span>

[<span data-ttu-id="de95b-133">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="de95b-133">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="de95b-134">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="de95b-134">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="de95b-135">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="de95b-135">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="de95b-136">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="de95b-136">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)


