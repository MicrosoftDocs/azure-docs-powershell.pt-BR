---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 5af778b84981b5b15acaa688bd8ad1702e5ab7e3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284259"
---
# <span data-ttu-id="34947-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="34947-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="34947-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34947-102">SYNOPSIS</span></span>
<span data-ttu-id="34947-103">Atualiza um certificado de autenticação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="34947-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="34947-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34947-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34947-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="34947-105">DESCRIPTION</span></span>
<span data-ttu-id="34947-106">O cmdlet **set-AzApplicationGatewayAuthenticationCertificate** atualiza um certificado de autenticação para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="34947-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="34947-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34947-107">EXAMPLES</span></span>

### <span data-ttu-id="34947-108">Exemplo 1: atualizar um certificado de autenticação</span><span class="sxs-lookup"><span data-stu-id="34947-108">Example 1: Update an authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert2.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="34947-109">O primeiro comando obtém o gateway do aplicativo chamado appGwName e armazena o resultado na variável $appgw.</span><span class="sxs-lookup"><span data-stu-id="34947-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="34947-110">O segundo comando atualiza o certificado de autenticação chamado cert01 no gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="34947-110">The second command updates the authentication certificate named cert01 in the application gateway.</span></span>
<span data-ttu-id="34947-111">O terceiro comando atualiza o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="34947-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="34947-112">OS</span><span class="sxs-lookup"><span data-stu-id="34947-112">PARAMETERS</span></span>

### <span data-ttu-id="34947-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34947-113">-ApplicationGateway</span></span>
<span data-ttu-id="34947-114">Especifica o nome do gateway do aplicativo para o qual esse cmdlet atualiza um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="34947-114">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="34947-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="34947-115">-CertificateFile</span></span>
<span data-ttu-id="34947-116">Especifica o caminho do arquivo de certificado de autenticação com o qual esse cmdlet atualiza o certificado.</span><span class="sxs-lookup"><span data-stu-id="34947-116">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="34947-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34947-117">-DefaultProfile</span></span>
<span data-ttu-id="34947-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="34947-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34947-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="34947-119">-Name</span></span>
<span data-ttu-id="34947-120">Especifica o nome do certificado de autenticação que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="34947-120">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="34947-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="34947-121">-Confirm</span></span>
<span data-ttu-id="34947-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34947-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34947-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34947-123">-WhatIf</span></span>
<span data-ttu-id="34947-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="34947-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34947-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="34947-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34947-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34947-126">CommonParameters</span></span>
<span data-ttu-id="34947-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34947-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34947-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34947-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34947-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="34947-129">INPUTS</span></span>

### <span data-ttu-id="34947-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34947-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="34947-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="34947-131">OUTPUTS</span></span>

### <span data-ttu-id="34947-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34947-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="34947-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="34947-133">NOTES</span></span>
* <span data-ttu-id="34947-134">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="34947-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="34947-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34947-135">RELATED LINKS</span></span>

[<span data-ttu-id="34947-136">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="34947-136">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="34947-137">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="34947-137">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="34947-138">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="34947-138">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="34947-139">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="34947-139">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)


