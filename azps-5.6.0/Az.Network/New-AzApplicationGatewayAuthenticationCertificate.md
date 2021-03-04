---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: c4c2c2041c6bf21aa6bf8b13055d0dac5ffbc64a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892954"
---
# <span data-ttu-id="1cb0c-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1cb0c-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="1cb0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cb0c-102">SYNOPSIS</span></span>
<span data-ttu-id="1cb0c-103">Cria um certificado de autenticação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1cb0c-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="1cb0c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1cb0c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cb0c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1cb0c-105">DESCRIPTION</span></span>
<span data-ttu-id="1cb0c-106">O cmdlet **New-AzApplicationGatewayAuthenticationCertificate** cria um certificado de autenticação para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="1cb0c-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="1cb0c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1cb0c-107">EXAMPLES</span></span>

### <span data-ttu-id="1cb0c-108">Exemplo 1: Criar um certificado de autenticação</span><span class="sxs-lookup"><span data-stu-id="1cb0c-108">Example 1: Create an authentication certificate</span></span>
```
PS C:\> $cert = New-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -CertificateFile "C:\cert.cer"
```

<span data-ttu-id="1cb0c-109">O primeiro comando cria um certificado de autenticação chamado cert01.</span><span class="sxs-lookup"><span data-stu-id="1cb0c-109">The first command creates authentication certificate named cert01.</span></span>

## <span data-ttu-id="1cb0c-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1cb0c-110">PARAMETERS</span></span>

### <span data-ttu-id="1cb0c-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="1cb0c-111">-CertificateFile</span></span>
<span data-ttu-id="1cb0c-112">Especifica o caminho do certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="1cb0c-112">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="1cb0c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cb0c-113">-DefaultProfile</span></span>
<span data-ttu-id="1cb0c-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1cb0c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cb0c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1cb0c-115">-Name</span></span>
<span data-ttu-id="1cb0c-116">Especifica um nome para o certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="1cb0c-116">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="1cb0c-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cb0c-117">-Confirm</span></span>
<span data-ttu-id="1cb0c-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cb0c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cb0c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cb0c-119">-WhatIf</span></span>
<span data-ttu-id="1cb0c-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1cb0c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cb0c-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1cb0c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cb0c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cb0c-122">CommonParameters</span></span>
<span data-ttu-id="1cb0c-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cb0c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cb0c-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cb0c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cb0c-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1cb0c-125">INPUTS</span></span>

### <span data-ttu-id="1cb0c-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1cb0c-126">None</span></span>

## <span data-ttu-id="1cb0c-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1cb0c-127">OUTPUTS</span></span>

### <span data-ttu-id="1cb0c-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1cb0c-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="1cb0c-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="1cb0c-129">NOTES</span></span>
* <span data-ttu-id="1cb0c-130">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="1cb0c-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="1cb0c-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1cb0c-131">RELATED LINKS</span></span>

[<span data-ttu-id="1cb0c-132">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1cb0c-132">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="1cb0c-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1cb0c-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="1cb0c-134">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1cb0c-134">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="1cb0c-135">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1cb0c-135">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


