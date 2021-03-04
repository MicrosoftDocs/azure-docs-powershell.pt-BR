---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: ba0d82ab04f8e0c990c7bbf15facb3ee725f7609
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887393"
---
# <span data-ttu-id="7574f-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7574f-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="7574f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7574f-102">SYNOPSIS</span></span>
<span data-ttu-id="7574f-103">Adiciona um certificado de autenticação a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7574f-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="7574f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7574f-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7574f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7574f-105">DESCRIPTION</span></span>
<span data-ttu-id="7574f-106">O cmdlet **Add-AzApplicationGatewayAuthenticationCertificate** adiciona um certificado de autenticação a um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="7574f-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="7574f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7574f-107">EXAMPLES</span></span>

### <span data-ttu-id="7574f-108">Exemplo 1: Adicionar certificado de autenticação a um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="7574f-108">Example 1: Add authentication certificate to an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="7574f-109">O primeiro comando obtém um gateway de aplicativo chamado appGwName e o armazena $appgw variável.</span><span class="sxs-lookup"><span data-stu-id="7574f-109">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="7574f-110">O segundo comando adiciona o certificado de autenticação chamado cert01 ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7574f-110">The second command adds authentication certificate named cert01 to the application gateway.</span></span>
<span data-ttu-id="7574f-111">O terceiro comando atualiza o gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7574f-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="7574f-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7574f-112">PARAMETERS</span></span>

### <span data-ttu-id="7574f-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7574f-113">-ApplicationGateway</span></span>
<span data-ttu-id="7574f-114">Especifica o nome do gateway de aplicativo para o qual este cmdlet adiciona um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="7574f-114">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="7574f-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="7574f-115">-CertificateFile</span></span>
<span data-ttu-id="7574f-116">Especifica o caminho do certificado de autenticação que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="7574f-116">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="7574f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7574f-117">-DefaultProfile</span></span>
<span data-ttu-id="7574f-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7574f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7574f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7574f-119">-Name</span></span>
<span data-ttu-id="7574f-120">Especifica o nome de um certificado que este cmdlet adiciona ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7574f-120">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="7574f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7574f-121">-Confirm</span></span>
<span data-ttu-id="7574f-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7574f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7574f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7574f-123">-WhatIf</span></span>
<span data-ttu-id="7574f-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7574f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7574f-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7574f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7574f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7574f-126">CommonParameters</span></span>
<span data-ttu-id="7574f-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7574f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7574f-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7574f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7574f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7574f-129">INPUTS</span></span>

### <span data-ttu-id="7574f-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7574f-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7574f-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7574f-131">OUTPUTS</span></span>

### <span data-ttu-id="7574f-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7574f-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7574f-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="7574f-133">NOTES</span></span>
* <span data-ttu-id="7574f-134">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="7574f-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7574f-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7574f-135">RELATED LINKS</span></span>

[<span data-ttu-id="7574f-136">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7574f-136">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7574f-137">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7574f-137">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7574f-138">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7574f-138">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7574f-139">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7574f-139">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


