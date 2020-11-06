---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: a71ba6f6d9b45e0016589d5629f029998f33963f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611088"
---
# <span data-ttu-id="8bf9e-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8bf9e-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="8bf9e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8bf9e-102">SYNOPSIS</span></span>
<span data-ttu-id="8bf9e-103">Atualiza um certificado de autenticação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8bf9e-103">Updates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bf9e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8bf9e-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8bf9e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8bf9e-105">DESCRIPTION</span></span>
<span data-ttu-id="8bf9e-106">O cmdlet **set-AzureRmApplicationGatewayAuthenticationCertificate** atualiza um certificado de autenticação para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="8bf9e-106">The **Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="8bf9e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8bf9e-107">EXAMPLES</span></span>

## <span data-ttu-id="8bf9e-108">OS</span><span class="sxs-lookup"><span data-stu-id="8bf9e-108">PARAMETERS</span></span>

### <span data-ttu-id="8bf9e-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8bf9e-109">-ApplicationGateway</span></span>
<span data-ttu-id="8bf9e-110">Especifica o nome do gateway do aplicativo para o qual esse cmdlet atualiza um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="8bf9e-110">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="8bf9e-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="8bf9e-111">-CertificateFile</span></span>
<span data-ttu-id="8bf9e-112">Especifica o caminho do arquivo de certificado de autenticação com o qual esse cmdlet atualiza o certificado.</span><span class="sxs-lookup"><span data-stu-id="8bf9e-112">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="8bf9e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="8bf9e-113">-Name</span></span>
<span data-ttu-id="8bf9e-114">Especifica o nome do certificado de autenticação que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="8bf9e-114">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="8bf9e-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8bf9e-115">-Confirm</span></span>
<span data-ttu-id="8bf9e-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bf9e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bf9e-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bf9e-117">-WhatIf</span></span>
<span data-ttu-id="8bf9e-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8bf9e-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bf9e-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8bf9e-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bf9e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bf9e-120">-DefaultProfile</span></span>
<span data-ttu-id="8bf9e-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8bf9e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bf9e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bf9e-122">CommonParameters</span></span>
<span data-ttu-id="8bf9e-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bf9e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bf9e-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bf9e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bf9e-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8bf9e-125">INPUTS</span></span>

### <span data-ttu-id="8bf9e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8bf9e-126">System.String</span></span>

## <span data-ttu-id="8bf9e-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8bf9e-127">OUTPUTS</span></span>

### <span data-ttu-id="8bf9e-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8bf9e-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8bf9e-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8bf9e-129">NOTES</span></span>
* <span data-ttu-id="8bf9e-130">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="8bf9e-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8bf9e-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8bf9e-131">RELATED LINKS</span></span>

[<span data-ttu-id="8bf9e-132">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8bf9e-132">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="8bf9e-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8bf9e-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="8bf9e-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8bf9e-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="8bf9e-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8bf9e-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)


