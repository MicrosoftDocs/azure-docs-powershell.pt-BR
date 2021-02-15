---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 687752d74e13030cd954736132dba845c2c55127
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117488"
---
# <span data-ttu-id="eed64-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="eed64-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="eed64-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eed64-102">SYNOPSIS</span></span>
<span data-ttu-id="eed64-103">Adiciona um certificado de autenticação a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eed64-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="eed64-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eed64-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eed64-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="eed64-105">DESCRIPTION</span></span>
<span data-ttu-id="eed64-106">O cmdlet **Add-AzApplicationGatewayAuthenticationCertificate** adiciona um certificado de autenticação a um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="eed64-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="eed64-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="eed64-107">EXAMPLES</span></span>

### <span data-ttu-id="eed64-108">Exemplo 1: Adicionar certificado de autenticação a um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="eed64-108">Example 1: Add authentication certificate to an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="eed64-109">O primeiro comando obtém um gateway de aplicativo chamado appGwName e o armazena $appgw variável.</span><span class="sxs-lookup"><span data-stu-id="eed64-109">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="eed64-110">O segundo comando adiciona um certificado de autenticação chamado cert01 ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eed64-110">The second command adds authentication certificate named cert01 to the application gateway.</span></span>
<span data-ttu-id="eed64-111">O terceiro comando atualiza o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eed64-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="eed64-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eed64-112">PARAMETERS</span></span>

### <span data-ttu-id="eed64-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eed64-113">-ApplicationGateway</span></span>
<span data-ttu-id="eed64-114">Especifica o nome do gateway de aplicativo para o qual este cmdlet adiciona um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="eed64-114">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="eed64-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="eed64-115">-CertificateFile</span></span>
<span data-ttu-id="eed64-116">Especifica o caminho do certificado de autenticação que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="eed64-116">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="eed64-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eed64-117">-DefaultProfile</span></span>
<span data-ttu-id="eed64-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="eed64-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eed64-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="eed64-119">-Name</span></span>
<span data-ttu-id="eed64-120">Especifica o nome de um certificado que este cmdlet adiciona ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eed64-120">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="eed64-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="eed64-121">-Confirm</span></span>
<span data-ttu-id="eed64-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eed64-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eed64-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eed64-123">-WhatIf</span></span>
<span data-ttu-id="eed64-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="eed64-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eed64-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eed64-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eed64-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eed64-126">CommonParameters</span></span>
<span data-ttu-id="eed64-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eed64-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eed64-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eed64-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eed64-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="eed64-129">INPUTS</span></span>

### <span data-ttu-id="eed64-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eed64-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="eed64-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="eed64-131">OUTPUTS</span></span>

### <span data-ttu-id="eed64-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eed64-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="eed64-133">Notas</span><span class="sxs-lookup"><span data-stu-id="eed64-133">NOTES</span></span>
* <span data-ttu-id="eed64-134">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="eed64-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="eed64-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eed64-135">RELATED LINKS</span></span>

[<span data-ttu-id="eed64-136">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="eed64-136">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="eed64-137">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="eed64-137">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="eed64-138">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="eed64-138">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="eed64-139">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="eed64-139">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


