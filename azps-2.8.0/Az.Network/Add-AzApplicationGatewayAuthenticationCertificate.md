---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 1a1d484d3b8d23633393c0f300f84091b06c1d0e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772124"
---
# <span data-ttu-id="5ff9c-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5ff9c-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="5ff9c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5ff9c-102">SYNOPSIS</span></span>
<span data-ttu-id="5ff9c-103">Adiciona um certificado de autenticação a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5ff9c-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="5ff9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ff9c-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ff9c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5ff9c-105">DESCRIPTION</span></span>
<span data-ttu-id="5ff9c-106">O cmdlet **Add-AzApplicationGatewayAuthenticationCertificate** adiciona um certificado de autenticação a um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="5ff9c-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="5ff9c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5ff9c-107">EXAMPLES</span></span>

### <span data-ttu-id="5ff9c-108">Exemplo 1: Adicionar certificado de autenticação a um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="5ff9c-108">Example 1: Add authentication certificate to an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="5ff9c-109">O primeiro comando obtém um gateway do aplicativo chamado appGwName e o armazena em $appgw variável.</span><span class="sxs-lookup"><span data-stu-id="5ff9c-109">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="5ff9c-110">O segundo comando adiciona um certificado de autenticação chamado cert01 ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5ff9c-110">The second command adds authentication certificate named cert01 to the application gateway.</span></span>
<span data-ttu-id="5ff9c-111">O terceiro comando atualiza o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="5ff9c-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="5ff9c-112">OS</span><span class="sxs-lookup"><span data-stu-id="5ff9c-112">PARAMETERS</span></span>

### <span data-ttu-id="5ff9c-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ff9c-113">-ApplicationGateway</span></span>
<span data-ttu-id="5ff9c-114">Especifica o nome do gateway do aplicativo para o qual esse cmdlet adiciona um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="5ff9c-114">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="5ff9c-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="5ff9c-115">-CertificateFile</span></span>
<span data-ttu-id="5ff9c-116">Especifica o caminho do certificado de autenticação que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="5ff9c-116">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="5ff9c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ff9c-117">-DefaultProfile</span></span>
<span data-ttu-id="5ff9c-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5ff9c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff9c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ff9c-119">-Name</span></span>
<span data-ttu-id="5ff9c-120">Especifica o nome de um certificado que o cmdlet adiciona ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5ff9c-120">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="5ff9c-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5ff9c-121">-Confirm</span></span>
<span data-ttu-id="5ff9c-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ff9c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ff9c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ff9c-123">-WhatIf</span></span>
<span data-ttu-id="5ff9c-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5ff9c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ff9c-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5ff9c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ff9c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ff9c-126">CommonParameters</span></span>
<span data-ttu-id="5ff9c-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ff9c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ff9c-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ff9c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ff9c-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5ff9c-129">INPUTS</span></span>

### <span data-ttu-id="5ff9c-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ff9c-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5ff9c-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5ff9c-131">OUTPUTS</span></span>

### <span data-ttu-id="5ff9c-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ff9c-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5ff9c-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5ff9c-133">NOTES</span></span>
* <span data-ttu-id="5ff9c-134">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="5ff9c-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="5ff9c-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ff9c-135">RELATED LINKS</span></span>

[<span data-ttu-id="5ff9c-136">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5ff9c-136">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5ff9c-137">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5ff9c-137">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5ff9c-138">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5ff9c-138">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5ff9c-139">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5ff9c-139">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


