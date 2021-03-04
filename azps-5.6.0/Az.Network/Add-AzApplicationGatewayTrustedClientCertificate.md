---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: ac4da06b2f90f9d7bb5c3cbccbde98c8c65db481
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889195"
---
# <span data-ttu-id="1049f-101">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1049f-101">Add-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="1049f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1049f-102">SYNOPSIS</span></span>
<span data-ttu-id="1049f-103">Adiciona uma cadeia de certificados de AC de cliente confiável a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1049f-103">Adds a trusted client CA certificate chain to an application gateway.</span></span>

## <span data-ttu-id="1049f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1049f-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1049f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1049f-105">DESCRIPTION</span></span>
<span data-ttu-id="1049f-106">O cmdlet **Add-AzApplicationGatewayTrustedClientCertificate** adiciona uma cadeia de certificados DE cliente confiável a um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="1049f-106">The **Add-AzApplicationGatewayTrustedClientCertificate** cmdlet adds a trusted client CA certificate chain to an Azure application gateway.</span></span>

## <span data-ttu-id="1049f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1049f-107">EXAMPLES</span></span>

### <span data-ttu-id="1049f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1049f-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfileName -ApplicationGateway $gw -TrustedClientCertificates $trustedClient
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="1049f-109">O primeiro comando obtém o gateway do aplicativo e o armazena $gw variável.</span><span class="sxs-lookup"><span data-stu-id="1049f-109">The first command gets the application gateway and stores it in $gw variable.</span></span> <span data-ttu-id="1049f-110">O segundo comando cria uma nova cadeia de certificados de AC de cliente confiável que está tomando o caminho do certificado ca do cliente como entrada.</span><span class="sxs-lookup"><span data-stu-id="1049f-110">The second command creates a new trusted client CA certificate chain taking path of the client CA certificate as input.</span></span> <span data-ttu-id="1049f-111">O terceiro comando cria um perfil SSL usando certificado de cliente confiável.</span><span class="sxs-lookup"><span data-stu-id="1049f-111">The third command creates a SSL profile using trusted client certificate.</span></span> <span data-ttu-id="1049f-112">O quarto comando atualiza o Gateway de Aplicativos.</span><span class="sxs-lookup"><span data-stu-id="1049f-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="1049f-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1049f-113">PARAMETERS</span></span>

### <span data-ttu-id="1049f-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1049f-114">-ApplicationGateway</span></span>
<span data-ttu-id="1049f-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1049f-115">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1049f-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="1049f-116">-CertificateFile</span></span>
<span data-ttu-id="1049f-117">Caminho do arquivo de cadeia de certificados de CA do cliente confiável</span><span class="sxs-lookup"><span data-stu-id="1049f-117">Path of the trusted client CA certificate chain file</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1049f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1049f-118">-DefaultProfile</span></span>
<span data-ttu-id="1049f-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1049f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1049f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1049f-120">-Name</span></span>
<span data-ttu-id="1049f-121">O nome da cadeia de certificados ca de cliente confiável</span><span class="sxs-lookup"><span data-stu-id="1049f-121">The name of the trusted client CA certificate chain</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1049f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1049f-122">-Confirm</span></span>
<span data-ttu-id="1049f-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1049f-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1049f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1049f-124">-WhatIf</span></span>
<span data-ttu-id="1049f-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1049f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1049f-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1049f-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1049f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1049f-127">CommonParameters</span></span>
<span data-ttu-id="1049f-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1049f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1049f-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1049f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1049f-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1049f-130">INPUTS</span></span>

### <span data-ttu-id="1049f-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1049f-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1049f-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1049f-132">OUTPUTS</span></span>

### <span data-ttu-id="1049f-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1049f-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1049f-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="1049f-134">NOTES</span></span>

## <span data-ttu-id="1049f-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1049f-135">RELATED LINKS</span></span>

[<span data-ttu-id="1049f-136">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1049f-136">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="1049f-137">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1049f-137">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="1049f-138">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1049f-138">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="1049f-139">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1049f-139">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)