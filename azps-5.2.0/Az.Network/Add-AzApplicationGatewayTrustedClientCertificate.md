---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: e3a92085c15116527e1b6c14d5403f68748f4f90
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260485"
---
# <span data-ttu-id="ef346-101">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ef346-101">Add-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="ef346-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ef346-102">SYNOPSIS</span></span>
<span data-ttu-id="ef346-103">Adiciona uma cadeia de certificados de autoridade de certificação de cliente confiável a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ef346-103">Adds a trusted client CA certificate chain to an application gateway.</span></span>

## <span data-ttu-id="ef346-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef346-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef346-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ef346-105">DESCRIPTION</span></span>
<span data-ttu-id="ef346-106">O cmdlet **Add-AzApplicationGatewayTrustedClientCertificate** adiciona uma cadeia de certificados de autoridade de certificação de cliente confiável a um aplicativo gateway do Azure.</span><span class="sxs-lookup"><span data-stu-id="ef346-106">The **Add-AzApplicationGatewayTrustedClientCertificate** cmdlet adds a trusted client CA certificate chain to an Azure application gateway.</span></span>

## <span data-ttu-id="ef346-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef346-107">EXAMPLES</span></span>

### <span data-ttu-id="ef346-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ef346-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfileName -ApplicationGateway $gw -TrustedClientCertificates $trustedClient
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="ef346-109">O primeiro comando obtém o gateway do aplicativo e o armazena em $gw variável.</span><span class="sxs-lookup"><span data-stu-id="ef346-109">The first command gets the application gateway and stores it in $gw variable.</span></span> <span data-ttu-id="ef346-110">O segundo comando cria uma nova cadeia de certificados de autoridade de certificação de cliente confiável fazendo o caminho do certificado de CA do cliente como entrada.</span><span class="sxs-lookup"><span data-stu-id="ef346-110">The second command creates a new trusted client CA certificate chain taking path of the client CA certificate as input.</span></span> <span data-ttu-id="ef346-111">O terceiro comando cria um perfil SSL usando um certificado de cliente confiável.</span><span class="sxs-lookup"><span data-stu-id="ef346-111">The third command creates a SSL profile using trusted client certificate.</span></span> <span data-ttu-id="ef346-112">O quarto comando atualiza o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ef346-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="ef346-113">OS</span><span class="sxs-lookup"><span data-stu-id="ef346-113">PARAMETERS</span></span>

### <span data-ttu-id="ef346-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef346-114">-ApplicationGateway</span></span>
<span data-ttu-id="ef346-115">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef346-115">The applicationGateway</span></span>

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

### <span data-ttu-id="ef346-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="ef346-116">-CertificateFile</span></span>
<span data-ttu-id="ef346-117">Caminho do arquivo de cadeia de certificados da autoridade de certificação do cliente confiável</span><span class="sxs-lookup"><span data-stu-id="ef346-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="ef346-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef346-118">-DefaultProfile</span></span>
<span data-ttu-id="ef346-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ef346-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef346-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ef346-120">-Name</span></span>
<span data-ttu-id="ef346-121">O nome da cadeia de certificados da autoridade de certificação do cliente confiável</span><span class="sxs-lookup"><span data-stu-id="ef346-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="ef346-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ef346-122">-Confirm</span></span>
<span data-ttu-id="ef346-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef346-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef346-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef346-124">-WhatIf</span></span>
<span data-ttu-id="ef346-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ef346-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef346-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ef346-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef346-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef346-127">CommonParameters</span></span>
<span data-ttu-id="ef346-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef346-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef346-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef346-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef346-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ef346-130">INPUTS</span></span>

### <span data-ttu-id="ef346-131">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef346-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ef346-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ef346-132">OUTPUTS</span></span>

### <span data-ttu-id="ef346-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef346-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ef346-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ef346-134">NOTES</span></span>

## <span data-ttu-id="ef346-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef346-135">RELATED LINKS</span></span>

[<span data-ttu-id="ef346-136">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ef346-136">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="ef346-137">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ef346-137">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="ef346-138">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ef346-138">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="ef346-139">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ef346-139">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)