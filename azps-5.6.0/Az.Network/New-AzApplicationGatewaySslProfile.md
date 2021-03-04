---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 4e58ee2c2f9b7854234913f0cf6ce7c6923f3345
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887699"
---
# <span data-ttu-id="c44ae-101">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="c44ae-101">New-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="c44ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c44ae-102">SYNOPSIS</span></span>
<span data-ttu-id="c44ae-103">Cria perfil SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c44ae-103">Creates SSL profile for an application gateway.</span></span>

## <span data-ttu-id="c44ae-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c44ae-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslProfile -Name <String> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c44ae-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c44ae-105">DESCRIPTION</span></span>
<span data-ttu-id="c44ae-106">O cmdlet **New-AzApplicationGatewaySslProfile** cria o perfil SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c44ae-106">The **New-AzApplicationGatewaySslProfile** cmdlet creates SSL profile for an application gateway.</span></span> <span data-ttu-id="c44ae-107">O perfil ssl é configurado nos ouvintes HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c44ae-107">The ssl profile is configured on the HTTPS listeners.</span></span>

## <span data-ttu-id="c44ae-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c44ae-108">EXAMPLES</span></span>

### <span data-ttu-id="c44ae-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c44ae-109">Example 1</span></span>
```powershell
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $profile = New-AzApplicationGatewaySslProfile -Name $sslProfile01Name -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01
```
<span data-ttu-id="c44ae-110">O primeiro comando cria uma nova política SSL e a armazena na variável $sslPolicy.</span><span class="sxs-lookup"><span data-stu-id="c44ae-110">The first command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="c44ae-111">O segundo comando cria cadeias de certificados de AC de cliente confiáveis e as armazena na variável $ClientCert 01.</span><span class="sxs-lookup"><span data-stu-id="c44ae-111">The second command creates a trusted client CA certificate chains and stores them in the $ClientCert01 variable.</span></span>
<span data-ttu-id="c44ae-112">O terceiro comando cria um novo perfil SSL com a política ssl e a cadeia de certificados de CA de cliente confiáveis.</span><span class="sxs-lookup"><span data-stu-id="c44ae-112">The third command create a new SSL profile with the the ssl policy and trusted client CA certificate chain.</span></span>

## <span data-ttu-id="c44ae-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c44ae-113">PARAMETERS</span></span>

### <span data-ttu-id="c44ae-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c44ae-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="c44ae-115">Configurações de configuração de autenticação do cliente</span><span class="sxs-lookup"><span data-stu-id="c44ae-115">Client authentication configuration settings</span></span>

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

### <span data-ttu-id="c44ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c44ae-116">-DefaultProfile</span></span>
<span data-ttu-id="c44ae-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c44ae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c44ae-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c44ae-118">-Name</span></span>
<span data-ttu-id="c44ae-119">O nome do perfil SSL</span><span class="sxs-lookup"><span data-stu-id="c44ae-119">The name of the SSL profile</span></span>

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

### <span data-ttu-id="c44ae-120">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="c44ae-120">-SslPolicy</span></span>
<span data-ttu-id="c44ae-121">Política SSL</span><span class="sxs-lookup"><span data-stu-id="c44ae-121">SSL policy</span></span>

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

### <span data-ttu-id="c44ae-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="c44ae-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="c44ae-123">As cadeias de certificados de AC de cliente confiáveis</span><span class="sxs-lookup"><span data-stu-id="c44ae-123">The trusted client CA certificate chains</span></span>

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

### <span data-ttu-id="c44ae-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c44ae-124">CommonParameters</span></span>
<span data-ttu-id="c44ae-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c44ae-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c44ae-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c44ae-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c44ae-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c44ae-127">INPUTS</span></span>

### <span data-ttu-id="c44ae-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c44ae-128">None</span></span>

## <span data-ttu-id="c44ae-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c44ae-129">OUTPUTS</span></span>

### <span data-ttu-id="c44ae-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="c44ae-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="c44ae-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="c44ae-131">NOTES</span></span>

## <span data-ttu-id="c44ae-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c44ae-132">RELATED LINKS</span></span>

[<span data-ttu-id="c44ae-133">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="c44ae-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="c44ae-134">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="c44ae-134">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="c44ae-135">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="c44ae-135">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="c44ae-136">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="c44ae-136">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)