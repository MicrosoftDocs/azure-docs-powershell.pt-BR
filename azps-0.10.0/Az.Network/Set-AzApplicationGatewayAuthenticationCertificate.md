---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 23b337779da46169be29e3dd6fef55fc70f4f035
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776583"
---
# <span data-ttu-id="b3cc2-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b3cc2-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="b3cc2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b3cc2-102">SYNOPSIS</span></span>
<span data-ttu-id="b3cc2-103">Atualiza um certificado de autenticação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b3cc2-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="b3cc2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3cc2-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3cc2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b3cc2-105">DESCRIPTION</span></span>
<span data-ttu-id="b3cc2-106">O cmdlet **set-AzApplicationGatewayAuthenticationCertificate** atualiza um certificado de autenticação para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="b3cc2-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="b3cc2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b3cc2-107">EXAMPLES</span></span>

### <span data-ttu-id="b3cc2-108">1:</span><span class="sxs-lookup"><span data-stu-id="b3cc2-108">1:</span></span>
```

```

## <span data-ttu-id="b3cc2-109">OS</span><span class="sxs-lookup"><span data-stu-id="b3cc2-109">PARAMETERS</span></span>

### <span data-ttu-id="b3cc2-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b3cc2-110">-ApplicationGateway</span></span>
<span data-ttu-id="b3cc2-111">Especifica o nome do gateway do aplicativo para o qual esse cmdlet atualiza um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="b3cc2-111">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="b3cc2-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b3cc2-112">-CertificateFile</span></span>
<span data-ttu-id="b3cc2-113">Especifica o caminho do arquivo de certificado de autenticação com o qual esse cmdlet atualiza o certificado.</span><span class="sxs-lookup"><span data-stu-id="b3cc2-113">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="b3cc2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3cc2-114">-DefaultProfile</span></span>
<span data-ttu-id="b3cc2-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b3cc2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3cc2-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3cc2-116">-Name</span></span>
<span data-ttu-id="b3cc2-117">Especifica o nome do certificado de autenticação que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="b3cc2-117">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="b3cc2-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b3cc2-118">-Confirm</span></span>
<span data-ttu-id="b3cc2-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3cc2-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3cc2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3cc2-120">-WhatIf</span></span>
<span data-ttu-id="b3cc2-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b3cc2-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3cc2-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b3cc2-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3cc2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3cc2-123">CommonParameters</span></span>
<span data-ttu-id="b3cc2-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3cc2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3cc2-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3cc2-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3cc2-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b3cc2-126">INPUTS</span></span>

### <span data-ttu-id="b3cc2-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b3cc2-127">System.String</span></span>

## <span data-ttu-id="b3cc2-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b3cc2-128">OUTPUTS</span></span>

### <span data-ttu-id="b3cc2-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b3cc2-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b3cc2-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b3cc2-130">NOTES</span></span>
* <span data-ttu-id="b3cc2-131">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="b3cc2-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b3cc2-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3cc2-132">RELATED LINKS</span></span>

[<span data-ttu-id="b3cc2-133">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b3cc2-133">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b3cc2-134">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b3cc2-134">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b3cc2-135">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b3cc2-135">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b3cc2-136">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b3cc2-136">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)


