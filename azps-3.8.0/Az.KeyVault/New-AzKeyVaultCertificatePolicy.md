---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: b0d690358fb5598b1a88ecb7fe169c8ef3d2718f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944881"
---
# <span data-ttu-id="4248d-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4248d-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="4248d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4248d-102">SYNOPSIS</span></span>
<span data-ttu-id="4248d-103">Cria um objeto de política de certificado na memória.</span><span class="sxs-lookup"><span data-stu-id="4248d-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="4248d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4248d-104">SYNTAX</span></span>

### <span data-ttu-id="4248d-105">SubjectName (padrão)</span><span class="sxs-lookup"><span data-stu-id="4248d-105">SubjectName (Default)</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4248d-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="4248d-106">DNSNames</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4248d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4248d-107">DESCRIPTION</span></span>
<span data-ttu-id="4248d-108">O cmdlet **New-AzKeyVaultCertificatePolicy** cria um objeto de política de certificado na memória para o Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="4248d-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="4248d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4248d-109">EXAMPLES</span></span>

### <span data-ttu-id="4248d-110">Exemplo 1: criar uma política de certificado</span><span class="sxs-lookup"><span data-stu-id="4248d-110">Example 1: Create a certificate policy</span></span>
```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal

SecretContentType               : application/x-pkcs12
Kty                             :
KeySize                         : 2048
Curve                           :
Exportable                      :
ReuseKeyOnRenewal               : True
SubjectName                     : CN=contoso.com
DnsNames                        :
KeyUsage                        :
Ekus                            :
ValidityInMonths                : 6
IssuerName                      : Self
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry :
RenewAtPercentageLifetime       :
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
CertificateTransparency         :
Enabled                         : True
Created                         :
Updated                         :
```

<span data-ttu-id="4248d-111">Esse comando cria uma política de certificado válida por seis meses e reutiliza a chave para renovar o certificado.</span><span class="sxs-lookup"><span data-stu-id="4248d-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="4248d-112">OS</span><span class="sxs-lookup"><span data-stu-id="4248d-112">PARAMETERS</span></span>

### <span data-ttu-id="4248d-113">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="4248d-113">-CertificateTransparency</span></span>
<span data-ttu-id="4248d-114">Indica se a transparência do certificado está habilitada para este certificado/emissor; Se não for especificado, o padrão será ' true '</span><span class="sxs-lookup"><span data-stu-id="4248d-114">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4248d-115">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="4248d-115">-CertificateType</span></span>
<span data-ttu-id="4248d-116">Especifica o tipo de certificado para o emissor.</span><span class="sxs-lookup"><span data-stu-id="4248d-116">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4248d-117">-Curve</span><span class="sxs-lookup"><span data-stu-id="4248d-117">-Curve</span></span>
<span data-ttu-id="4248d-118">Especifica o nome da curva elíptica da chave do certificado.</span><span class="sxs-lookup"><span data-stu-id="4248d-118">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="4248d-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4248d-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4248d-120">P a 256</span><span class="sxs-lookup"><span data-stu-id="4248d-120">P-256</span></span>
- <span data-ttu-id="4248d-121">P a 384</span><span class="sxs-lookup"><span data-stu-id="4248d-121">P-384</span></span>
- <span data-ttu-id="4248d-122">P a 521</span><span class="sxs-lookup"><span data-stu-id="4248d-122">P-521</span></span>
- <span data-ttu-id="4248d-123">P A 256K</span><span class="sxs-lookup"><span data-stu-id="4248d-123">P-256K</span></span>
- <span data-ttu-id="4248d-124">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="4248d-124">SECP256K1</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: P-256, P-384, P-521, P-256K, SECP256K1

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4248d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4248d-125">-DefaultProfile</span></span>
<span data-ttu-id="4248d-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4248d-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4248d-127">-Desabilitado</span><span class="sxs-lookup"><span data-stu-id="4248d-127">-Disabled</span></span>
<span data-ttu-id="4248d-128">Indica que a política de certificado está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="4248d-128">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4248d-129">-DnsName</span><span class="sxs-lookup"><span data-stu-id="4248d-129">-DnsName</span></span>
<span data-ttu-id="4248d-130">Especifica os nomes DNS no certificado.</span><span class="sxs-lookup"><span data-stu-id="4248d-130">Specifies the DNS names in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: DNSNames
Aliases: DnsNames

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4248d-131">-Ekus</span><span class="sxs-lookup"><span data-stu-id="4248d-131">-Ekus</span></span>
<span data-ttu-id="4248d-132">Especifica os usos avançados da chave (EKUs) no certificado.</span><span class="sxs-lookup"><span data-stu-id="4248d-132">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4248d-133">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="4248d-133">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="4248d-134">Especifica o número de dias antes do vencimento do início do processo de notificação automática.</span><span class="sxs-lookup"><span data-stu-id="4248d-134">Specifies how many days before expiry the automatic notification process begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4248d-135">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="4248d-135">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="4248d-136">Especifica a porcentagem do tempo de vida após o qual o processo automático para a notificação é iniciado.</span><span class="sxs-lookup"><span data-stu-id="4248d-136">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4248d-137">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="4248d-137">-IssuerName</span></span>
<span data-ttu-id="4248d-138">Especifica o nome do emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="4248d-138">Specifies the name of the issuer for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4248d-139">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="4248d-139">-KeyNotExportable</span></span>
<span data-ttu-id="4248d-140">Indica que a chave não é exportável.</span><span class="sxs-lookup"><span data-stu-id="4248d-140">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4248d-141">-KeySize</span><span class="sxs-lookup"><span data-stu-id="4248d-141">-KeySize</span></span>
<span data-ttu-id="4248d-142">Especifica o tamanho da chave do certificado.</span><span class="sxs-lookup"><span data-stu-id="4248d-142">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="4248d-143">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4248d-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4248d-144">2048</span><span class="sxs-lookup"><span data-stu-id="4248d-144">2048</span></span>
- <span data-ttu-id="4248d-145">3072</span><span class="sxs-lookup"><span data-stu-id="4248d-145">3072</span></span>
- <span data-ttu-id="4248d-146">4096</span><span class="sxs-lookup"><span data-stu-id="4248d-146">4096</span></span>
- <span data-ttu-id="4248d-147">256</span><span class="sxs-lookup"><span data-stu-id="4248d-147">256</span></span>
- <span data-ttu-id="4248d-148">384</span><span class="sxs-lookup"><span data-stu-id="4248d-148">384</span></span>
- <span data-ttu-id="4248d-149">521</span><span class="sxs-lookup"><span data-stu-id="4248d-149">521</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096, 256, 384, 521

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4248d-150">-KeyType</span><span class="sxs-lookup"><span data-stu-id="4248d-150">-KeyType</span></span>
<span data-ttu-id="4248d-151">Especifica o tipo de chave da chave que faz a backup do certificado.</span><span class="sxs-lookup"><span data-stu-id="4248d-151">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="4248d-152">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4248d-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4248d-153">RSA</span><span class="sxs-lookup"><span data-stu-id="4248d-153">RSA</span></span>
- <span data-ttu-id="4248d-154">RSA – HSM</span><span class="sxs-lookup"><span data-stu-id="4248d-154">RSA-HSM</span></span>
- <span data-ttu-id="4248d-155">EC</span><span class="sxs-lookup"><span data-stu-id="4248d-155">EC</span></span>
- <span data-ttu-id="4248d-156">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="4248d-156">EC-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM, EC, EC-HSM

Required: False
Position: Named
Default value: RSA
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4248d-157">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="4248d-157">-KeyUsage</span></span>
<span data-ttu-id="4248d-158">Especifica os usos da chave no certificado.</span><span class="sxs-lookup"><span data-stu-id="4248d-158">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]
Parameter Sets: (All)
Aliases:
Accepted values: None, EncipherOnly, CrlSign, KeyCertSign, KeyAgreement, DataEncipherment, KeyEncipherment, NonRepudiation, DigitalSignature, DecipherOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4248d-159">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="4248d-159">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="4248d-160">Especifica o número de dias antes da expiração após o início do processo automático para a renovação do certificado.</span><span class="sxs-lookup"><span data-stu-id="4248d-160">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4248d-161">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="4248d-161">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="4248d-162">Especifica a porcentagem do tempo de vida após o qual o processo automático para a renovação do certificado é iniciado.</span><span class="sxs-lookup"><span data-stu-id="4248d-162">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4248d-163">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="4248d-163">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="4248d-164">Indica que o certificado reutiliza a chave durante a renovação.</span><span class="sxs-lookup"><span data-stu-id="4248d-164">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4248d-165">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="4248d-165">-SecretContentType</span></span>
<span data-ttu-id="4248d-166">Especifica o tipo de conteúdo do novo segredo do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="4248d-166">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="4248d-167">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4248d-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4248d-168">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="4248d-168">application/x-pkcs12</span></span>
- <span data-ttu-id="4248d-169">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="4248d-169">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4248d-170">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="4248d-170">-SubjectName</span></span>
<span data-ttu-id="4248d-171">Especifica o nome do requerente do certificado.</span><span class="sxs-lookup"><span data-stu-id="4248d-171">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SubjectName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DNSNames
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4248d-172">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="4248d-172">-ValidityInMonths</span></span>
<span data-ttu-id="4248d-173">Especifica o número de meses para o qual o certificado é válido.</span><span class="sxs-lookup"><span data-stu-id="4248d-173">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4248d-174">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4248d-174">-Confirm</span></span>
<span data-ttu-id="4248d-175">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4248d-175">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4248d-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4248d-176">-WhatIf</span></span>
<span data-ttu-id="4248d-177">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4248d-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4248d-178">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4248d-178">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4248d-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4248d-179">CommonParameters</span></span>
<span data-ttu-id="4248d-180">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4248d-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4248d-181">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4248d-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4248d-182">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4248d-182">INPUTS</span></span>

### <span data-ttu-id="4248d-183">System. String</span><span class="sxs-lookup"><span data-stu-id="4248d-183">System.String</span></span>

### <span data-ttu-id="4248d-184">System. Collections. Generic. List ' 1 [System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4248d-184">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4248d-185">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4248d-185">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4248d-186">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4248d-186">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4248d-187">System. Collections. Generic. List ' 1 [System. Security. Cryptography. X509Certificates. X509KeyUsageFlags, System. Security. Cryptography. X509Certificates, Version = 4.2.1.0, Culture = neutral, PublicKeyToken = b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="4248d-187">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="4248d-188">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4248d-188">OUTPUTS</span></span>

### <span data-ttu-id="4248d-189">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4248d-189">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="4248d-190">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4248d-190">NOTES</span></span>

## <span data-ttu-id="4248d-191">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4248d-191">RELATED LINKS</span></span>

[<span data-ttu-id="4248d-192">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4248d-192">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="4248d-193">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="4248d-193">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

