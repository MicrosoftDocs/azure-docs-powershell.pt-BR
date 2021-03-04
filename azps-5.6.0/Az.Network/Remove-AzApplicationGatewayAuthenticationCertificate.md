---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: aa8bd1b8850c1aa7f859d1797a961e32c22aa9e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885607"
---
# <span data-ttu-id="410b8-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="410b8-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="410b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="410b8-102">SYNOPSIS</span></span>
<span data-ttu-id="410b8-103">Remove um certificado de autenticação de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="410b8-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="410b8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="410b8-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="410b8-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="410b8-105">DESCRIPTION</span></span>
<span data-ttu-id="410b8-106">O cmdlet **Remove-AzApplicationGatewayAuthenticationCertificate** remove um certificado de autenticação de um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="410b8-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="410b8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="410b8-107">EXAMPLES</span></span>

### <span data-ttu-id="410b8-108">Exemplo 1: Remover um certificado de autenticação de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="410b8-108">Example 1: Remove an authentication certificate from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="410b8-109">O primeiro comando obtém o gateway de aplicativo chamado appGwName e armazena o resultado na $appgw variável.</span><span class="sxs-lookup"><span data-stu-id="410b8-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="410b8-110">O segundo comando remove o certificado de autenticação chamado cert01 do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="410b8-110">The second command removes the authentication certificate named cert01 from the application gateway.</span></span>
<span data-ttu-id="410b8-111">O terceiro comando atualiza o gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="410b8-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="410b8-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="410b8-112">PARAMETERS</span></span>

### <span data-ttu-id="410b8-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="410b8-113">-ApplicationGateway</span></span>
<span data-ttu-id="410b8-114">Especifica o nome do gateway de aplicativo do qual este cmdlet remove um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="410b8-114">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="410b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="410b8-115">-DefaultProfile</span></span>
<span data-ttu-id="410b8-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="410b8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="410b8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="410b8-117">-Name</span></span>
<span data-ttu-id="410b8-118">Especifica o nome do certificado de autenticação que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="410b8-118">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="410b8-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="410b8-119">-Confirm</span></span>
<span data-ttu-id="410b8-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="410b8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="410b8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="410b8-121">-WhatIf</span></span>
<span data-ttu-id="410b8-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="410b8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="410b8-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="410b8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="410b8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="410b8-124">CommonParameters</span></span>
<span data-ttu-id="410b8-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="410b8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="410b8-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="410b8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="410b8-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="410b8-127">INPUTS</span></span>

### <span data-ttu-id="410b8-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="410b8-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="410b8-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="410b8-129">OUTPUTS</span></span>

### <span data-ttu-id="410b8-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="410b8-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="410b8-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="410b8-131">NOTES</span></span>
* <span data-ttu-id="410b8-132">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="410b8-132">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="410b8-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="410b8-133">RELATED LINKS</span></span>

[<span data-ttu-id="410b8-134">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="410b8-134">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="410b8-135">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="410b8-135">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="410b8-136">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="410b8-136">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="410b8-137">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="410b8-137">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


