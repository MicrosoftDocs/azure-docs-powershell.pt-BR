---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 0fa72c48693335dd3df6ab3c1cf8040c5343cc84
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282142"
---
# <span data-ttu-id="04ed6-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="04ed6-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="04ed6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04ed6-102">SYNOPSIS</span></span>
<span data-ttu-id="04ed6-103">Atualiza um certificado SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04ed6-103">Updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="04ed6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04ed6-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04ed6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04ed6-105">DESCRIPTION</span></span>
<span data-ttu-id="04ed6-106">O cmdlet **set-AzApplicationGatewaySslCertificate** atualiza um certificado SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04ed6-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="04ed6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04ed6-107">EXAMPLES</span></span>

### <span data-ttu-id="04ed6-108">Exemplo 1: atualizar um certificado SSL existente no Application Gateway</span><span class="sxs-lookup"><span data-stu-id="04ed6-108">Example 1: Update an existing SSL certificate on Application Gateway</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="04ed6-109">Atualize um certificado SSL existente para o Application Gateway chamado ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="04ed6-109">Update an existing SSL certificate for the application gateway named ApplicationGateway01.</span></span>

### <span data-ttu-id="04ed6-110">Exemplo 2: atualizar um certificado SSL existente usando o segredo do keyvault (versão menos secreta) no gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="04ed6-110">Example 2: Update an existing SSL certificate using KeyVault Secret (version-less secretId) on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="04ed6-111">Obtenha o segredo e atualize um certificado SSL existente usando o `Set-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="04ed6-111">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>

### <span data-ttu-id="04ed6-112">Exemplo 3: atualizar um certificado SSL existente usando o segredo do keyvault no gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="04ed6-112">Example 3: Update an existing SSL certificate using KeyVault Secret on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="04ed6-113">Obtenha o segredo e atualize um certificado SSL existente usando o `Set-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="04ed6-113">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="04ed6-114">Observação: se for necessário que o Application Gateway Sincronize o certificado com o keyvault, forneça o nome secreto sem versão.</span><span class="sxs-lookup"><span data-stu-id="04ed6-114">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="04ed6-115">OS</span><span class="sxs-lookup"><span data-stu-id="04ed6-115">PARAMETERS</span></span>

### <span data-ttu-id="04ed6-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="04ed6-116">-ApplicationGateway</span></span>
<span data-ttu-id="04ed6-117">Especifica o gateway do aplicativo com o qual o certificado SSL (Secure Socket Layer) está associado.</span><span class="sxs-lookup"><span data-stu-id="04ed6-117">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="04ed6-118">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="04ed6-118">-CertificateFile</span></span>
<span data-ttu-id="04ed6-119">Especifica o caminho do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="04ed6-119">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="04ed6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04ed6-120">-DefaultProfile</span></span>
<span data-ttu-id="04ed6-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04ed6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04ed6-122">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="04ed6-122">-KeyVaultSecretId</span></span>
<span data-ttu-id="04ed6-123">Secretid (URI) do segredo do keyvault.</span><span class="sxs-lookup"><span data-stu-id="04ed6-123">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="04ed6-124">Use esta opção quando for preciso usar uma versão específica do segredo.</span><span class="sxs-lookup"><span data-stu-id="04ed6-124">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="04ed6-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="04ed6-125">-Name</span></span>
<span data-ttu-id="04ed6-126">Especifica o nome do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="04ed6-126">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="04ed6-127">-Senha</span><span class="sxs-lookup"><span data-stu-id="04ed6-127">-Password</span></span>
<span data-ttu-id="04ed6-128">Especifica a senha do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="04ed6-128">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="04ed6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04ed6-129">CommonParameters</span></span>
<span data-ttu-id="04ed6-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04ed6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04ed6-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04ed6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04ed6-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04ed6-132">INPUTS</span></span>

### <span data-ttu-id="04ed6-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="04ed6-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="04ed6-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04ed6-134">OUTPUTS</span></span>

### <span data-ttu-id="04ed6-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="04ed6-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="04ed6-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04ed6-136">NOTES</span></span>

## <span data-ttu-id="04ed6-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04ed6-137">RELATED LINKS</span></span>

[<span data-ttu-id="04ed6-138">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="04ed6-138">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="04ed6-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="04ed6-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="04ed6-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="04ed6-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="04ed6-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="04ed6-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


