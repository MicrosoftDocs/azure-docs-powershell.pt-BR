---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 3c70fcd0e04b566ff1cd3297525d3ed2c9ed95ba
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786395"
---
# <span data-ttu-id="df742-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="df742-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="df742-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df742-102">SYNOPSIS</span></span>
<span data-ttu-id="df742-103">Atualiza um certificado de autenticação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="df742-103">Updates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df742-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df742-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df742-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df742-105">DESCRIPTION</span></span>
<span data-ttu-id="df742-106">O cmdlet **set-AzureRmApplicationGatewayAuthenticationCertificate** atualiza um certificado de autenticação para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="df742-106">The **Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="df742-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df742-107">EXAMPLES</span></span>

### <span data-ttu-id="df742-108">1:</span><span class="sxs-lookup"><span data-stu-id="df742-108">1:</span></span>
```

```

## <span data-ttu-id="df742-109">OS</span><span class="sxs-lookup"><span data-stu-id="df742-109">PARAMETERS</span></span>

### <span data-ttu-id="df742-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="df742-110">-ApplicationGateway</span></span>
<span data-ttu-id="df742-111">Especifica o nome do gateway do aplicativo para o qual esse cmdlet atualiza um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="df742-111">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="df742-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="df742-112">-CertificateFile</span></span>
<span data-ttu-id="df742-113">Especifica o caminho do arquivo de certificado de autenticação com o qual esse cmdlet atualiza o certificado.</span><span class="sxs-lookup"><span data-stu-id="df742-113">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="df742-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df742-114">-DefaultProfile</span></span>
<span data-ttu-id="df742-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df742-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df742-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="df742-116">-Name</span></span>
<span data-ttu-id="df742-117">Especifica o nome do certificado de autenticação que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="df742-117">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="df742-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="df742-118">-Confirm</span></span>
<span data-ttu-id="df742-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df742-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df742-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df742-120">-WhatIf</span></span>
<span data-ttu-id="df742-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="df742-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df742-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="df742-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df742-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df742-123">CommonParameters</span></span>
<span data-ttu-id="df742-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df742-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df742-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df742-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df742-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df742-126">INPUTS</span></span>

### <span data-ttu-id="df742-127">System. String</span><span class="sxs-lookup"><span data-stu-id="df742-127">System.String</span></span>

## <span data-ttu-id="df742-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df742-128">OUTPUTS</span></span>

### <span data-ttu-id="df742-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="df742-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="df742-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df742-130">NOTES</span></span>
* <span data-ttu-id="df742-131">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="df742-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="df742-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df742-132">RELATED LINKS</span></span>

[<span data-ttu-id="df742-133">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="df742-133">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="df742-134">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="df742-134">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="df742-135">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="df742-135">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="df742-136">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="df742-136">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)


