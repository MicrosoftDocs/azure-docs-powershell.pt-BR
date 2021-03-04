---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 469b490b0f0c2bd37f7f58265108278322cbca60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889196"
---
# <span data-ttu-id="70dfb-101">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="70dfb-101">Add-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="70dfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="70dfb-103">Adiciona o perfil SSL a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="70dfb-103">Adds SSL profile to an application gateway.</span></span>

## <span data-ttu-id="70dfb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="70dfb-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslProfile -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70dfb-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="70dfb-105">DESCRIPTION</span></span>
<span data-ttu-id="70dfb-106">O cmdlet **Add-AzApplicationGatewaySslProfile** adiciona um perfil SSL a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="70dfb-106">The **Add-AzApplicationGatewaySslProfile** cmdlet adds a SSL profile to an application gateway.</span></span> <span data-ttu-id="70dfb-107">O perfil SSL é aplicado aos Ouvintes HTTPS.</span><span class="sxs-lookup"><span data-stu-id="70dfb-107">The SSL profile is applied to HTTPS Listeners.</span></span>

## <span data-ttu-id="70dfb-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="70dfb-108">EXAMPLES</span></span>

### <span data-ttu-id="70dfb-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="70dfb-109">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $trustedClient02 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert02" -CertificateFile "C:\clientCAChain2.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfile01Name -ApplicationGateway $AppGw -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01,$trustedClient02
```

<span data-ttu-id="70dfb-110">O primeiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="70dfb-110">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="70dfb-111">O segundo comando cria uma nova política SSL e a armazena na variável $sslPolicy.</span><span class="sxs-lookup"><span data-stu-id="70dfb-111">The second command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="70dfb-112">O terceiro e quarto comando cria duas novas cadeias de certificados de AC de cliente confiáveis e as armazena nas variáveis $ClientCert 01 e $ClientCert 02.</span><span class="sxs-lookup"><span data-stu-id="70dfb-112">The third and fourth command creates two new trusted client CA certificate chains and stores them in the $ClientCert01 and $ClientCert02 variables.</span></span>
<span data-ttu-id="70dfb-113">O quinto comando adiciona o perfil SSL com a política ssl e cadeias de certificados de CA de cliente confiáveis ao gateway de aplicativo $AppGw.</span><span class="sxs-lookup"><span data-stu-id="70dfb-113">The fifth command adds the SSL profile with the the ssl policy and trusted client CA certificate chains to the application gateway $AppGw.</span></span>

## <span data-ttu-id="70dfb-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="70dfb-114">PARAMETERS</span></span>

### <span data-ttu-id="70dfb-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="70dfb-115">-ApplicationGateway</span></span>
<span data-ttu-id="70dfb-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="70dfb-116">The applicationGateway</span></span>

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

### <span data-ttu-id="70dfb-117">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="70dfb-117">-ClientAuthConfiguration</span></span>
<span data-ttu-id="70dfb-118">Configurações de configuração de autenticação do cliente</span><span class="sxs-lookup"><span data-stu-id="70dfb-118">Client authentication configuration settings</span></span>

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

### <span data-ttu-id="70dfb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70dfb-119">-DefaultProfile</span></span>
<span data-ttu-id="70dfb-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="70dfb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70dfb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="70dfb-121">-Name</span></span>
<span data-ttu-id="70dfb-122">O nome do perfil SSL</span><span class="sxs-lookup"><span data-stu-id="70dfb-122">The name of the SSL profile</span></span>

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

### <span data-ttu-id="70dfb-123">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="70dfb-123">-SslPolicy</span></span>
<span data-ttu-id="70dfb-124">Política SSL</span><span class="sxs-lookup"><span data-stu-id="70dfb-124">SSL policy</span></span>

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

### <span data-ttu-id="70dfb-125">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="70dfb-125">-TrustedClientCertificates</span></span>
<span data-ttu-id="70dfb-126">As cadeias de certificados de AC de cliente confiáveis</span><span class="sxs-lookup"><span data-stu-id="70dfb-126">The trusted client CA certificate chains</span></span>

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

### <span data-ttu-id="70dfb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70dfb-127">CommonParameters</span></span>
<span data-ttu-id="70dfb-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70dfb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70dfb-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70dfb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70dfb-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="70dfb-130">INPUTS</span></span>

### <span data-ttu-id="70dfb-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="70dfb-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="70dfb-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="70dfb-132">OUTPUTS</span></span>

### <span data-ttu-id="70dfb-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="70dfb-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="70dfb-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="70dfb-134">NOTES</span></span>

## <span data-ttu-id="70dfb-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70dfb-135">RELATED LINKS</span></span>

[<span data-ttu-id="70dfb-136">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="70dfb-136">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="70dfb-137">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="70dfb-137">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="70dfb-138">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="70dfb-138">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="70dfb-139">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="70dfb-139">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)