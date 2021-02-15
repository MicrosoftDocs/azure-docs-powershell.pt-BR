---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: a9b0d41ad700d0591e38fa339c38efb85cb00859
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112850"
---
# <span data-ttu-id="f0192-101">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f0192-101">New-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="f0192-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f0192-102">SYNOPSIS</span></span>
<span data-ttu-id="f0192-103">Cria perfil SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f0192-103">Creates SSL profile for an application gateway.</span></span>

## <span data-ttu-id="f0192-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0192-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslProfile -Name <String> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0192-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f0192-105">DESCRIPTION</span></span>
<span data-ttu-id="f0192-106">O **cmdlet New-AzApplicationGatewaySslProfile** cria perfil SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f0192-106">The **New-AzApplicationGatewaySslProfile** cmdlet creates SSL profile for an application gateway.</span></span> <span data-ttu-id="f0192-107">O perfil SSL está configurado nos ouvintes HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f0192-107">The ssl profile is configured on the HTTPS listeners.</span></span>

## <span data-ttu-id="f0192-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f0192-108">EXAMPLES</span></span>

### <span data-ttu-id="f0192-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f0192-109">Example 1</span></span>
```powershell
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $profile = New-AzApplicationGatewaySslProfile -Name $sslProfile01Name -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01
```
<span data-ttu-id="f0192-110">O primeiro comando cria uma nova política SSL e a armazena na $sslPolicy variável.</span><span class="sxs-lookup"><span data-stu-id="f0192-110">The first command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="f0192-111">O segundo comando cria uma cadeia de certificados de AC de cliente confiável e as armazena na variável $ClientCert 01.</span><span class="sxs-lookup"><span data-stu-id="f0192-111">The second command creates a trusted client CA certificate chains and stores them in the $ClientCert01 variable.</span></span>
<span data-ttu-id="f0192-112">O terceiro comando cria um novo perfil SSL com a política ssl e a cadeia de certificados de CA de cliente confiável.</span><span class="sxs-lookup"><span data-stu-id="f0192-112">The third command create a new SSL profile with the the ssl policy and trusted client CA certificate chain.</span></span>

## <span data-ttu-id="f0192-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0192-113">PARAMETERS</span></span>

### <span data-ttu-id="f0192-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0192-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="f0192-115">Configurações de configuração de autenticação do cliente</span><span class="sxs-lookup"><span data-stu-id="f0192-115">Client authentication configuration settings</span></span>

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

### <span data-ttu-id="f0192-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0192-116">-DefaultProfile</span></span>
<span data-ttu-id="f0192-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f0192-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0192-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0192-118">-Name</span></span>
<span data-ttu-id="f0192-119">O nome do perfil SSL</span><span class="sxs-lookup"><span data-stu-id="f0192-119">The name of the SSL profile</span></span>

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

### <span data-ttu-id="f0192-120">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="f0192-120">-SslPolicy</span></span>
<span data-ttu-id="f0192-121">Política SSL</span><span class="sxs-lookup"><span data-stu-id="f0192-121">SSL policy</span></span>

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

### <span data-ttu-id="f0192-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="f0192-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="f0192-123">As cadeias de certificados de certificação de cliente confiáveis</span><span class="sxs-lookup"><span data-stu-id="f0192-123">The trusted client CA certificate chains</span></span>

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

### <span data-ttu-id="f0192-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0192-124">CommonParameters</span></span>
<span data-ttu-id="f0192-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0192-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0192-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0192-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0192-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="f0192-127">INPUTS</span></span>

### <span data-ttu-id="f0192-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f0192-128">None</span></span>

## <span data-ttu-id="f0192-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="f0192-129">OUTPUTS</span></span>

### <span data-ttu-id="f0192-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f0192-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="f0192-131">Notas</span><span class="sxs-lookup"><span data-stu-id="f0192-131">NOTES</span></span>

## <span data-ttu-id="f0192-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0192-132">RELATED LINKS</span></span>

[<span data-ttu-id="f0192-133">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f0192-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="f0192-134">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f0192-134">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="f0192-135">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f0192-135">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="f0192-136">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f0192-136">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)