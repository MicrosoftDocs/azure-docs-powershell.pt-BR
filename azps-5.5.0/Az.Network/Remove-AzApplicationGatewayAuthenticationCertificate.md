---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 02416fdb18f01c9a2af6c091b0be109b479ce45d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112803"
---
# <span data-ttu-id="0a01a-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0a01a-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="0a01a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a01a-102">SYNOPSIS</span></span>
<span data-ttu-id="0a01a-103">Remove um certificado de autenticação de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0a01a-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="0a01a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a01a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a01a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a01a-105">DESCRIPTION</span></span>
<span data-ttu-id="0a01a-106">O cmdlet **Remove-AzApplicationGatewayAuthenticationCertificate** remove um certificado de autenticação de um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="0a01a-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="0a01a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0a01a-107">EXAMPLES</span></span>

### <span data-ttu-id="0a01a-108">Exemplo 1: Remover um certificado de autenticação de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="0a01a-108">Example 1: Remove an authentication certificate from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="0a01a-109">O primeiro comando obtém o gateway de aplicativo chamado appGwName e armazena o resultado na variável $appgw aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0a01a-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="0a01a-110">O segundo comando remove o certificado de autenticação chamado cert01 do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0a01a-110">The second command removes the authentication certificate named cert01 from the application gateway.</span></span>
<span data-ttu-id="0a01a-111">O terceiro comando atualiza o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0a01a-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="0a01a-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a01a-112">PARAMETERS</span></span>

### <span data-ttu-id="0a01a-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a01a-113">-ApplicationGateway</span></span>
<span data-ttu-id="0a01a-114">Especifica o nome do gateway de aplicativo do qual este cmdlet remove um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="0a01a-114">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="0a01a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a01a-115">-DefaultProfile</span></span>
<span data-ttu-id="0a01a-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0a01a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a01a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a01a-117">-Name</span></span>
<span data-ttu-id="0a01a-118">Especifica o nome do certificado de autenticação que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="0a01a-118">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0a01a-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0a01a-119">-Confirm</span></span>
<span data-ttu-id="0a01a-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a01a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a01a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a01a-121">-WhatIf</span></span>
<span data-ttu-id="0a01a-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0a01a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a01a-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0a01a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a01a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a01a-124">CommonParameters</span></span>
<span data-ttu-id="0a01a-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a01a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a01a-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a01a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a01a-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="0a01a-127">INPUTS</span></span>

### <span data-ttu-id="0a01a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a01a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0a01a-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="0a01a-129">OUTPUTS</span></span>

### <span data-ttu-id="0a01a-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a01a-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0a01a-131">Notas</span><span class="sxs-lookup"><span data-stu-id="0a01a-131">NOTES</span></span>
* <span data-ttu-id="0a01a-132">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="0a01a-132">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="0a01a-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a01a-133">RELATED LINKS</span></span>

[<span data-ttu-id="0a01a-134">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0a01a-134">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="0a01a-135">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0a01a-135">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="0a01a-136">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0a01a-136">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="0a01a-137">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0a01a-137">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


