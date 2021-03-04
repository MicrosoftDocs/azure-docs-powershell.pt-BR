---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: a060ddde57fc3d0cfadde487a147b8743acd5fbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892090"
---
# <span data-ttu-id="7398b-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7398b-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="7398b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7398b-102">SYNOPSIS</span></span>
<span data-ttu-id="7398b-103">Atualiza um certificado de autenticação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7398b-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="7398b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7398b-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7398b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7398b-105">DESCRIPTION</span></span>
<span data-ttu-id="7398b-106">O cmdlet **Set-AzApplicationGatewayAuthenticationCertificate** atualiza um certificado de autenticação para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="7398b-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="7398b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7398b-107">EXAMPLES</span></span>

### <span data-ttu-id="7398b-108">Exemplo 1: atualizar um certificado de autenticação</span><span class="sxs-lookup"><span data-stu-id="7398b-108">Example 1: Update an authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert2.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="7398b-109">O primeiro comando obtém o gateway de aplicativo chamado appGwName e armazena o resultado na $appgw variável.</span><span class="sxs-lookup"><span data-stu-id="7398b-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="7398b-110">O segundo comando atualiza o certificado de autenticação chamado cert01 no gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7398b-110">The second command updates the authentication certificate named cert01 in the application gateway.</span></span>
<span data-ttu-id="7398b-111">O terceiro comando atualiza o gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7398b-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="7398b-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7398b-112">PARAMETERS</span></span>

### <span data-ttu-id="7398b-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7398b-113">-ApplicationGateway</span></span>
<span data-ttu-id="7398b-114">Especifica o nome do gateway de aplicativo para o qual esse cmdlet atualiza um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="7398b-114">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="7398b-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="7398b-115">-CertificateFile</span></span>
<span data-ttu-id="7398b-116">Especifica o caminho do arquivo de certificado de autenticação com o qual esse cmdlet atualiza o certificado.</span><span class="sxs-lookup"><span data-stu-id="7398b-116">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="7398b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7398b-117">-DefaultProfile</span></span>
<span data-ttu-id="7398b-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7398b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7398b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7398b-119">-Name</span></span>
<span data-ttu-id="7398b-120">Especifica o nome do certificado de autenticação que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="7398b-120">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="7398b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7398b-121">-Confirm</span></span>
<span data-ttu-id="7398b-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7398b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7398b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7398b-123">-WhatIf</span></span>
<span data-ttu-id="7398b-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7398b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7398b-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7398b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7398b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7398b-126">CommonParameters</span></span>
<span data-ttu-id="7398b-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7398b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7398b-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7398b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7398b-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7398b-129">INPUTS</span></span>

### <span data-ttu-id="7398b-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7398b-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7398b-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7398b-131">OUTPUTS</span></span>

### <span data-ttu-id="7398b-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7398b-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7398b-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="7398b-133">NOTES</span></span>
* <span data-ttu-id="7398b-134">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="7398b-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7398b-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7398b-135">RELATED LINKS</span></span>

[<span data-ttu-id="7398b-136">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7398b-136">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7398b-137">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7398b-137">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7398b-138">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7398b-138">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7398b-139">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7398b-139">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)


