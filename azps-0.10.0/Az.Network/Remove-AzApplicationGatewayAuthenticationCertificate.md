---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: bf11b2b3010a7f7683d670c3c5e95d4248b83cd6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775339"
---
# <span data-ttu-id="ce988-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ce988-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="ce988-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce988-102">SYNOPSIS</span></span>
<span data-ttu-id="ce988-103">Remove um certificado de autenticação de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ce988-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="ce988-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce988-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce988-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce988-105">DESCRIPTION</span></span>
<span data-ttu-id="ce988-106">O cmdlet **Remove-AzApplicationGatewayAuthenticationCertificate** remove um certificado de autenticação de um Application Gateway do Azure.</span><span class="sxs-lookup"><span data-stu-id="ce988-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="ce988-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce988-107">EXAMPLES</span></span>

### <span data-ttu-id="ce988-108">1:</span><span class="sxs-lookup"><span data-stu-id="ce988-108">1:</span></span>
```

```

## <span data-ttu-id="ce988-109">OS</span><span class="sxs-lookup"><span data-stu-id="ce988-109">PARAMETERS</span></span>

### <span data-ttu-id="ce988-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce988-110">-ApplicationGateway</span></span>
<span data-ttu-id="ce988-111">Especifica o nome do aplicativo de gateway do qual esse cmdlet Remove um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="ce988-111">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="ce988-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce988-112">-DefaultProfile</span></span>
<span data-ttu-id="ce988-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ce988-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce988-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce988-114">-Name</span></span>
<span data-ttu-id="ce988-115">Especifica o nome do certificado de autenticação que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="ce988-115">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ce988-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ce988-116">-Confirm</span></span>
<span data-ttu-id="ce988-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce988-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce988-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce988-118">-WhatIf</span></span>
<span data-ttu-id="ce988-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ce988-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce988-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ce988-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce988-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce988-121">CommonParameters</span></span>
<span data-ttu-id="ce988-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce988-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce988-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce988-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce988-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce988-124">INPUTS</span></span>

### <span data-ttu-id="ce988-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ce988-125">System.String</span></span>

## <span data-ttu-id="ce988-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce988-126">OUTPUTS</span></span>

### <span data-ttu-id="ce988-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce988-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ce988-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce988-128">NOTES</span></span>
* <span data-ttu-id="ce988-129">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="ce988-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ce988-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce988-130">RELATED LINKS</span></span>

[<span data-ttu-id="ce988-131">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ce988-131">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ce988-132">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ce988-132">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ce988-133">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ce988-133">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ce988-134">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ce988-134">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


