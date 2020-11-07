---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 7e1c5c301b13f37086f4b6fc96e7254230684d10
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771948"
---
# <span data-ttu-id="5be7d-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5be7d-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="5be7d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5be7d-102">SYNOPSIS</span></span>
<span data-ttu-id="5be7d-103">Cria um certificado de autenticação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5be7d-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="5be7d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5be7d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5be7d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5be7d-105">DESCRIPTION</span></span>
<span data-ttu-id="5be7d-106">O cmdlet **New-AzApplicationGatewayAuthenticationCertificate** cria um certificado de autenticação para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="5be7d-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="5be7d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5be7d-107">EXAMPLES</span></span>

### <span data-ttu-id="5be7d-108">Exemplo 1: criar um certificado de autenticação</span><span class="sxs-lookup"><span data-stu-id="5be7d-108">Example 1: Create an authentication certificate</span></span>
```
PS C:\> $cert = New-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -CertificateFile "C:\cert.cer"
```

<span data-ttu-id="5be7d-109">O primeiro comando cria um certificado de autenticação chamado cert01.</span><span class="sxs-lookup"><span data-stu-id="5be7d-109">The first command creates authentication certificate named cert01.</span></span>

## <span data-ttu-id="5be7d-110">OS</span><span class="sxs-lookup"><span data-stu-id="5be7d-110">PARAMETERS</span></span>

### <span data-ttu-id="5be7d-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="5be7d-111">-CertificateFile</span></span>
<span data-ttu-id="5be7d-112">Especifica o caminho do certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="5be7d-112">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="5be7d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5be7d-113">-DefaultProfile</span></span>
<span data-ttu-id="5be7d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5be7d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5be7d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5be7d-115">-Name</span></span>
<span data-ttu-id="5be7d-116">Especifica um nome para o certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="5be7d-116">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="5be7d-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5be7d-117">-Confirm</span></span>
<span data-ttu-id="5be7d-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5be7d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5be7d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5be7d-119">-WhatIf</span></span>
<span data-ttu-id="5be7d-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5be7d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5be7d-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5be7d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5be7d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5be7d-122">CommonParameters</span></span>
<span data-ttu-id="5be7d-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5be7d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5be7d-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5be7d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5be7d-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5be7d-125">INPUTS</span></span>

### <span data-ttu-id="5be7d-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5be7d-126">None</span></span>

## <span data-ttu-id="5be7d-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5be7d-127">OUTPUTS</span></span>

### <span data-ttu-id="5be7d-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5be7d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="5be7d-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5be7d-129">NOTES</span></span>
* <span data-ttu-id="5be7d-130">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="5be7d-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="5be7d-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5be7d-131">RELATED LINKS</span></span>

[<span data-ttu-id="5be7d-132">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5be7d-132">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5be7d-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5be7d-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5be7d-134">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5be7d-134">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5be7d-135">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5be7d-135">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)

