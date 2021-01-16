---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 02416fdb18f01c9a2af6c091b0be109b479ce45d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257666"
---
# <span data-ttu-id="12813-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="12813-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="12813-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12813-102">SYNOPSIS</span></span>
<span data-ttu-id="12813-103">Remove um certificado de autenticação de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="12813-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="12813-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12813-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12813-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12813-105">DESCRIPTION</span></span>
<span data-ttu-id="12813-106">O cmdlet **Remove-AzApplicationGatewayAuthenticationCertificate** remove um certificado de autenticação de um Application Gateway do Azure.</span><span class="sxs-lookup"><span data-stu-id="12813-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="12813-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12813-107">EXAMPLES</span></span>

### <span data-ttu-id="12813-108">Exemplo 1: remover um certificado de autenticação de um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="12813-108">Example 1: Remove an authentication certificate from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="12813-109">O primeiro comando obtém o gateway do aplicativo chamado appGwName e armazena o resultado na variável $appgw.</span><span class="sxs-lookup"><span data-stu-id="12813-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="12813-110">O segundo comando Remove o certificado de autenticação chamado cert01 do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="12813-110">The second command removes the authentication certificate named cert01 from the application gateway.</span></span>
<span data-ttu-id="12813-111">O terceiro comando atualiza o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="12813-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="12813-112">OS</span><span class="sxs-lookup"><span data-stu-id="12813-112">PARAMETERS</span></span>

### <span data-ttu-id="12813-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12813-113">-ApplicationGateway</span></span>
<span data-ttu-id="12813-114">Especifica o nome do aplicativo de gateway do qual esse cmdlet Remove um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="12813-114">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="12813-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12813-115">-DefaultProfile</span></span>
<span data-ttu-id="12813-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12813-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12813-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="12813-117">-Name</span></span>
<span data-ttu-id="12813-118">Especifica o nome do certificado de autenticação que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="12813-118">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="12813-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="12813-119">-Confirm</span></span>
<span data-ttu-id="12813-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12813-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12813-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12813-121">-WhatIf</span></span>
<span data-ttu-id="12813-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="12813-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12813-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="12813-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12813-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12813-124">CommonParameters</span></span>
<span data-ttu-id="12813-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12813-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12813-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12813-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12813-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12813-127">INPUTS</span></span>

### <span data-ttu-id="12813-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12813-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="12813-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12813-129">OUTPUTS</span></span>

### <span data-ttu-id="12813-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12813-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="12813-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12813-131">NOTES</span></span>
* <span data-ttu-id="12813-132">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="12813-132">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="12813-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12813-133">RELATED LINKS</span></span>

[<span data-ttu-id="12813-134">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="12813-134">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="12813-135">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="12813-135">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="12813-136">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="12813-136">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="12813-137">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="12813-137">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


