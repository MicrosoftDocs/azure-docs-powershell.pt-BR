---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: f1b944e2673c9682a0194c4996fa4d2b34fae97b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885405"
---
# <span data-ttu-id="8e874-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8e874-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="8e874-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e874-102">SYNOPSIS</span></span>
<span data-ttu-id="8e874-103">Atualiza um certificado SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8e874-103">Updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="8e874-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8e874-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e874-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8e874-105">DESCRIPTION</span></span>
<span data-ttu-id="8e874-106">O cmdlet **Set-AzApplicationGatewaySslCertificate** atualiza um certificado SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8e874-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="8e874-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e874-107">EXAMPLES</span></span>

### <span data-ttu-id="8e874-108">Exemplo 1: atualizar um certificado SSL existente no Application Gateway</span><span class="sxs-lookup"><span data-stu-id="8e874-108">Example 1: Update an existing SSL certificate on Application Gateway</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="8e874-109">Atualize um certificado SSL existente para o gateway de aplicativo chamado ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="8e874-109">Update an existing SSL certificate for the application gateway named ApplicationGateway01.</span></span>

### <span data-ttu-id="8e874-110">Exemplo 2: atualizar um certificado SSL existente usando KeyVault Secret (secretId sem versão) no Gateway de Aplicativos</span><span class="sxs-lookup"><span data-stu-id="8e874-110">Example 2: Update an existing SSL certificate using KeyVault Secret (version-less secretId) on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="8e874-111">Obter o segredo e atualizar um Certificado SSL existente usando `Set-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="8e874-111">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>

### <span data-ttu-id="8e874-112">Exemplo 3: atualizar um certificado SSL existente usando KeyVault Secret no Application Gateway</span><span class="sxs-lookup"><span data-stu-id="8e874-112">Example 3: Update an existing SSL certificate using KeyVault Secret on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="8e874-113">Obter o segredo e atualizar um Certificado SSL existente usando `Set-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="8e874-113">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="8e874-114">Observação: se for necessário que o Gateway de Aplicativo sincronize o certificado com o KeyVault, forneça o secretId sem versão.</span><span class="sxs-lookup"><span data-stu-id="8e874-114">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="8e874-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8e874-115">PARAMETERS</span></span>

### <span data-ttu-id="8e874-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e874-116">-ApplicationGateway</span></span>
<span data-ttu-id="8e874-117">Especifica o gateway de aplicativo com o qual o certificado SSL (Secure Socket Layer) está associado.</span><span class="sxs-lookup"><span data-stu-id="8e874-117">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e874-118">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="8e874-118">-CertificateFile</span></span>
<span data-ttu-id="8e874-119">Especifica o caminho do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="8e874-119">Specifies the path of the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e874-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e874-120">-DefaultProfile</span></span>
<span data-ttu-id="8e874-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8e874-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e874-122">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="8e874-122">-KeyVaultSecretId</span></span>
<span data-ttu-id="8e874-123">SecretId (uri) do Segredo KeyVault.</span><span class="sxs-lookup"><span data-stu-id="8e874-123">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="8e874-124">Use essa opção quando uma versão específica do segredo precisar ser usada.</span><span class="sxs-lookup"><span data-stu-id="8e874-124">Use this option when a specific version of secret needs to be used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e874-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8e874-125">-Name</span></span>
<span data-ttu-id="8e874-126">Especifica o nome do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="8e874-126">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="8e874-127">-Password</span><span class="sxs-lookup"><span data-stu-id="8e874-127">-Password</span></span>
<span data-ttu-id="8e874-128">Especifica a senha do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="8e874-128">Specifies the password of the SSL certificate.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e874-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e874-129">CommonParameters</span></span>
<span data-ttu-id="8e874-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e874-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e874-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e874-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e874-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e874-132">INPUTS</span></span>

### <span data-ttu-id="8e874-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e874-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8e874-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8e874-134">OUTPUTS</span></span>

### <span data-ttu-id="8e874-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e874-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8e874-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="8e874-136">NOTES</span></span>

## <span data-ttu-id="8e874-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e874-137">RELATED LINKS</span></span>

[<span data-ttu-id="8e874-138">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8e874-138">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8e874-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8e874-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8e874-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8e874-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="8e874-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8e874-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


