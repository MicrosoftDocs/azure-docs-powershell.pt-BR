---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 8930041959712b7533651262a39409e884ffb177
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117478"
---
# <span data-ttu-id="63c20-101">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="63c20-101">Add-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="63c20-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63c20-102">SYNOPSIS</span></span>
<span data-ttu-id="63c20-103">Adiciona perfil SSL a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="63c20-103">Adds SSL profile to an application gateway.</span></span>

## <span data-ttu-id="63c20-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63c20-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslProfile -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63c20-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="63c20-105">DESCRIPTION</span></span>
<span data-ttu-id="63c20-106">O **cmdlet Add-AzApplicationGatewaySslProfile** adiciona um perfil SSL a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="63c20-106">The **Add-AzApplicationGatewaySslProfile** cmdlet adds a SSL profile to an application gateway.</span></span> <span data-ttu-id="63c20-107">O perfil SSL é aplicado aos Ouvintes HTTPS.</span><span class="sxs-lookup"><span data-stu-id="63c20-107">The SSL profile is applied to HTTPS Listeners.</span></span>

## <span data-ttu-id="63c20-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="63c20-108">EXAMPLES</span></span>

### <span data-ttu-id="63c20-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="63c20-109">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $trustedClient02 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert02" -CertificateFile "C:\clientCAChain2.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfile01Name -ApplicationGateway $AppGw -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01,$trustedClient02
```

<span data-ttu-id="63c20-110">O primeiro comando obtém o gateway do aplicativo e o armazena na variável $AppGw usuário.</span><span class="sxs-lookup"><span data-stu-id="63c20-110">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="63c20-111">O segundo comando cria uma nova política SSL e a armazena na variável $sslPolicy dados.</span><span class="sxs-lookup"><span data-stu-id="63c20-111">The second command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="63c20-112">O terceiro e quarto comando cria duas novas cadeias de certificados de certificação de cliente confiáveis e as armazena nas variáveis $ClientCert 01 e $ClientCert 02.</span><span class="sxs-lookup"><span data-stu-id="63c20-112">The third and fourth command creates two new trusted client CA certificate chains and stores them in the $ClientCert01 and $ClientCert02 variables.</span></span>
<span data-ttu-id="63c20-113">O quinto comando adiciona o perfil SSL com a política SSL e as cadeias de certificados de CA de cliente confiáveis ao gateway de aplicativos $AppGw.</span><span class="sxs-lookup"><span data-stu-id="63c20-113">The fifth command adds the SSL profile with the the ssl policy and trusted client CA certificate chains to the application gateway $AppGw.</span></span>

## <span data-ttu-id="63c20-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63c20-114">PARAMETERS</span></span>

### <span data-ttu-id="63c20-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63c20-115">-ApplicationGateway</span></span>
<span data-ttu-id="63c20-116">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="63c20-116">The applicationGateway</span></span>

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

### <span data-ttu-id="63c20-117">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="63c20-117">-ClientAuthConfiguration</span></span>
<span data-ttu-id="63c20-118">Configurações de configuração de autenticação do cliente</span><span class="sxs-lookup"><span data-stu-id="63c20-118">Client authentication configuration settings</span></span>

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

### <span data-ttu-id="63c20-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63c20-119">-DefaultProfile</span></span>
<span data-ttu-id="63c20-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="63c20-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63c20-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="63c20-121">-Name</span></span>
<span data-ttu-id="63c20-122">O nome do perfil SSL</span><span class="sxs-lookup"><span data-stu-id="63c20-122">The name of the SSL profile</span></span>

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

### <span data-ttu-id="63c20-123">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="63c20-123">-SslPolicy</span></span>
<span data-ttu-id="63c20-124">Política SSL</span><span class="sxs-lookup"><span data-stu-id="63c20-124">SSL policy</span></span>

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

### <span data-ttu-id="63c20-125">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="63c20-125">-TrustedClientCertificates</span></span>
<span data-ttu-id="63c20-126">As cadeias de certificados de certificação de cliente confiáveis</span><span class="sxs-lookup"><span data-stu-id="63c20-126">The trusted client CA certificate chains</span></span>

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

### <span data-ttu-id="63c20-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63c20-127">CommonParameters</span></span>
<span data-ttu-id="63c20-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63c20-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63c20-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63c20-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63c20-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="63c20-130">INPUTS</span></span>

### <span data-ttu-id="63c20-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63c20-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="63c20-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="63c20-132">OUTPUTS</span></span>

### <span data-ttu-id="63c20-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63c20-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="63c20-134">Notas</span><span class="sxs-lookup"><span data-stu-id="63c20-134">NOTES</span></span>

## <span data-ttu-id="63c20-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63c20-135">RELATED LINKS</span></span>

[<span data-ttu-id="63c20-136">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="63c20-136">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="63c20-137">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="63c20-137">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="63c20-138">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="63c20-138">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="63c20-139">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="63c20-139">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)