---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: c43fe72f8f3669b7e6e123a7f1d606771b161084
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117430"
---
# <span data-ttu-id="8d53a-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8d53a-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="8d53a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d53a-102">SYNOPSIS</span></span>
<span data-ttu-id="8d53a-103">Cria um certificado de autenticação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8d53a-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="8d53a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d53a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d53a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d53a-105">DESCRIPTION</span></span>
<span data-ttu-id="8d53a-106">O cmdlet **New-AzApplicationGatewayAuthenticationCertificate** cria um certificado de autenticação para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="8d53a-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="8d53a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8d53a-107">EXAMPLES</span></span>

### <span data-ttu-id="8d53a-108">Exemplo 1: Criar um certificado de autenticação</span><span class="sxs-lookup"><span data-stu-id="8d53a-108">Example 1: Create an authentication certificate</span></span>
```
PS C:\> $cert = New-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -CertificateFile "C:\cert.cer"
```

<span data-ttu-id="8d53a-109">O primeiro comando cria um certificado de autenticação chamado cert01.</span><span class="sxs-lookup"><span data-stu-id="8d53a-109">The first command creates authentication certificate named cert01.</span></span>

## <span data-ttu-id="8d53a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d53a-110">PARAMETERS</span></span>

### <span data-ttu-id="8d53a-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="8d53a-111">-CertificateFile</span></span>
<span data-ttu-id="8d53a-112">Especifica o caminho do certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="8d53a-112">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="8d53a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d53a-113">-DefaultProfile</span></span>
<span data-ttu-id="8d53a-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8d53a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d53a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8d53a-115">-Name</span></span>
<span data-ttu-id="8d53a-116">Especifica um nome para o certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="8d53a-116">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="8d53a-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8d53a-117">-Confirm</span></span>
<span data-ttu-id="8d53a-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d53a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d53a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d53a-119">-WhatIf</span></span>
<span data-ttu-id="8d53a-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8d53a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d53a-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8d53a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d53a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d53a-122">CommonParameters</span></span>
<span data-ttu-id="8d53a-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d53a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d53a-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d53a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d53a-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="8d53a-125">INPUTS</span></span>

### <span data-ttu-id="8d53a-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8d53a-126">None</span></span>

## <span data-ttu-id="8d53a-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="8d53a-127">OUTPUTS</span></span>

### <span data-ttu-id="8d53a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8d53a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="8d53a-129">Notas</span><span class="sxs-lookup"><span data-stu-id="8d53a-129">NOTES</span></span>
* <span data-ttu-id="8d53a-130">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="8d53a-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8d53a-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d53a-131">RELATED LINKS</span></span>

[<span data-ttu-id="8d53a-132">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8d53a-132">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="8d53a-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8d53a-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="8d53a-134">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8d53a-134">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="8d53a-135">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8d53a-135">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


