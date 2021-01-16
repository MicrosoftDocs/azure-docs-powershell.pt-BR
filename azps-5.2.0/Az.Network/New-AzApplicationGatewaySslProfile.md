---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: a9b0d41ad700d0591e38fa339c38efb85cb00859
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263959"
---
# <span data-ttu-id="d484c-101">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d484c-101">New-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="d484c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d484c-102">SYNOPSIS</span></span>
<span data-ttu-id="d484c-103">Cria um perfil SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d484c-103">Creates SSL profile for an application gateway.</span></span>

## <span data-ttu-id="d484c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d484c-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslProfile -Name <String> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d484c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d484c-105">DESCRIPTION</span></span>
<span data-ttu-id="d484c-106">O cmdlet **New-AzApplicationGatewaySslProfile** cria um perfil SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d484c-106">The **New-AzApplicationGatewaySslProfile** cmdlet creates SSL profile for an application gateway.</span></span> <span data-ttu-id="d484c-107">O perfil SSL está configurado nos ouvintes HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d484c-107">The ssl profile is configured on the HTTPS listeners.</span></span>

## <span data-ttu-id="d484c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d484c-108">EXAMPLES</span></span>

### <span data-ttu-id="d484c-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d484c-109">Example 1</span></span>
```powershell
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $profile = New-AzApplicationGatewaySslProfile -Name $sslProfile01Name -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01
```
<span data-ttu-id="d484c-110">O primeiro comando cria uma nova política SSL e a armazena na variável $sslPolicy.</span><span class="sxs-lookup"><span data-stu-id="d484c-110">The first command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="d484c-111">O segundo comando cria uma cadeia de certificados de autoridade de certificação de cliente confiável e a armazena na variável $ClientCert 01.</span><span class="sxs-lookup"><span data-stu-id="d484c-111">The second command creates a trusted client CA certificate chains and stores them in the $ClientCert01 variable.</span></span>
<span data-ttu-id="d484c-112">O terceiro comando cria um novo perfil SSL com a cadeia de certificados política SSL e certificado de autoridade de certificação de cliente confiável.</span><span class="sxs-lookup"><span data-stu-id="d484c-112">The third command create a new SSL profile with the the ssl policy and trusted client CA certificate chain.</span></span>

## <span data-ttu-id="d484c-113">OS</span><span class="sxs-lookup"><span data-stu-id="d484c-113">PARAMETERS</span></span>

### <span data-ttu-id="d484c-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="d484c-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="d484c-115">Definições de configuração de autenticação do cliente</span><span class="sxs-lookup"><span data-stu-id="d484c-115">Client authentication configuration settings</span></span>

```yaml
Type: PSApplicationGatewayClientAuthConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d484c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d484c-116">-DefaultProfile</span></span>
<span data-ttu-id="d484c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d484c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d484c-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d484c-118">-Name</span></span>
<span data-ttu-id="d484c-119">O nome do perfil SSL</span><span class="sxs-lookup"><span data-stu-id="d484c-119">The name of the SSL profile</span></span>

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

### <span data-ttu-id="d484c-120">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="d484c-120">-SslPolicy</span></span>
<span data-ttu-id="d484c-121">Política SSL</span><span class="sxs-lookup"><span data-stu-id="d484c-121">SSL policy</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d484c-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="d484c-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="d484c-123">Cadeias de certificados de autoridade de certificação do cliente confiável</span><span class="sxs-lookup"><span data-stu-id="d484c-123">The trusted client CA certificate chains</span></span>

```yaml
Type: PSApplicationGatewayTrustedClientCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d484c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d484c-124">CommonParameters</span></span>
<span data-ttu-id="d484c-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d484c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d484c-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d484c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d484c-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d484c-127">INPUTS</span></span>

### <span data-ttu-id="d484c-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d484c-128">None</span></span>

## <span data-ttu-id="d484c-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d484c-129">OUTPUTS</span></span>

### <span data-ttu-id="d484c-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d484c-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="d484c-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d484c-131">NOTES</span></span>

## <span data-ttu-id="d484c-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d484c-132">RELATED LINKS</span></span>

[<span data-ttu-id="d484c-133">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d484c-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="d484c-134">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d484c-134">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="d484c-135">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d484c-135">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="d484c-136">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d484c-136">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)