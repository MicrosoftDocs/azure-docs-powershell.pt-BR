---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 370662b1d24f9b5b71653506be7a3add5a3801f8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111730"
---
# <span data-ttu-id="91f07-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="91f07-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="91f07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91f07-102">SYNOPSIS</span></span>
<span data-ttu-id="91f07-103">Cria um objeto de política de certificado na memória.</span><span class="sxs-lookup"><span data-stu-id="91f07-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="91f07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91f07-104">SYNTAX</span></span>

### <span data-ttu-id="91f07-105">SubjectName (padrão)</span><span class="sxs-lookup"><span data-stu-id="91f07-105">SubjectName (Default)</span></span>
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

### <span data-ttu-id="91f07-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="91f07-106">DNSNames</span></span>
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

## <span data-ttu-id="91f07-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="91f07-107">DESCRIPTION</span></span>
<span data-ttu-id="91f07-108">O cmdlet **New-AzKeyVaultCertificatePolicy** cria um objeto de política de certificado na memória para o Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="91f07-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="91f07-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91f07-109">EXAMPLES</span></span>

### <span data-ttu-id="91f07-110">Exemplo 1: criar uma política de certificado</span><span class="sxs-lookup"><span data-stu-id="91f07-110">Example 1: Create a certificate policy</span></span>
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

<span data-ttu-id="91f07-111">Esse comando cria uma política de certificado válida por seis meses e reutiliza a chave para renovar o certificado.</span><span class="sxs-lookup"><span data-stu-id="91f07-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

### <span data-ttu-id="91f07-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="91f07-112">Example 2</span></span>

<span data-ttu-id="91f07-113">Cria um objeto de política de certificado na memória.</span><span class="sxs-lookup"><span data-stu-id="91f07-113">Creates an in-memory certificate policy object.</span></span> <span data-ttu-id="91f07-114">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="91f07-114">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzKeyVaultCertificatePolicy -IssuerName 'Self' -KeyType RSA -RenewAtNumberOfDaysBeforeExpiry <Int32> -SecretContentType application/x-pkcs12 -SubjectName 'CN=contoso.com' -ValidityInMonths 6
```

### <span data-ttu-id="91f07-115">Exemplo 3: criar um certificado alternativo de nome (ou SAN) de assunto</span><span class="sxs-lookup"><span data-stu-id="91f07-115">Example 3: Create a Subject Alternate Name (or SAN) certificate</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -DnsName "contoso.com","support.contoso.com","docs.contoso.com" -IssuerName "Self"

SecretContentType               : application/x-pkcs12
Kty                             : RSA
KeySize                         : 2048
Curve                           :
Exportable                      :
ReuseKeyOnRenewal               : False
SubjectName                     : CN=contoso.com
DnsNames                        : {contoso.com, support.contoso.com, docs.contoso.com}
KeyUsage                        :
Ekus                            :
ValidityInMonths                :
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

<span data-ttu-id="91f07-116">Este exemplo cria um certificado de SAN com 3 nomes DNS.</span><span class="sxs-lookup"><span data-stu-id="91f07-116">This example creates a SAN certificate with 3 DNS names.</span></span>

## <span data-ttu-id="91f07-117">OS</span><span class="sxs-lookup"><span data-stu-id="91f07-117">PARAMETERS</span></span>

### <span data-ttu-id="91f07-118">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="91f07-118">-CertificateTransparency</span></span>
<span data-ttu-id="91f07-119">Indica se a transparência do certificado está habilitada para este certificado/emissor; Se não for especificado, o padrão será ' true '</span><span class="sxs-lookup"><span data-stu-id="91f07-119">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="91f07-120">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="91f07-120">-CertificateType</span></span>
<span data-ttu-id="91f07-121">Especifica o tipo de certificado para o emissor.</span><span class="sxs-lookup"><span data-stu-id="91f07-121">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="91f07-122">-Curve</span><span class="sxs-lookup"><span data-stu-id="91f07-122">-Curve</span></span>
<span data-ttu-id="91f07-123">Especifica o nome da curva elíptica da chave do certificado.</span><span class="sxs-lookup"><span data-stu-id="91f07-123">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="91f07-124">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="91f07-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91f07-125">P a 256</span><span class="sxs-lookup"><span data-stu-id="91f07-125">P-256</span></span>
- <span data-ttu-id="91f07-126">P a 384</span><span class="sxs-lookup"><span data-stu-id="91f07-126">P-384</span></span>
- <span data-ttu-id="91f07-127">P a 521</span><span class="sxs-lookup"><span data-stu-id="91f07-127">P-521</span></span>
- <span data-ttu-id="91f07-128">P A 256K</span><span class="sxs-lookup"><span data-stu-id="91f07-128">P-256K</span></span>
- <span data-ttu-id="91f07-129">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="91f07-129">SECP256K1</span></span>

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

### <span data-ttu-id="91f07-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91f07-130">-DefaultProfile</span></span>
<span data-ttu-id="91f07-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="91f07-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91f07-132">-Desabilitado</span><span class="sxs-lookup"><span data-stu-id="91f07-132">-Disabled</span></span>
<span data-ttu-id="91f07-133">Indica que a política de certificado está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="91f07-133">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="91f07-134">-DnsName</span><span class="sxs-lookup"><span data-stu-id="91f07-134">-DnsName</span></span>
<span data-ttu-id="91f07-135">Especifica os nomes DNS no certificado.</span><span class="sxs-lookup"><span data-stu-id="91f07-135">Specifies the DNS names in the certificate.</span></span> <span data-ttu-id="91f07-136">Nomes alternativos de entidades (SANs) podem ser especificados como nomes DNS.</span><span class="sxs-lookup"><span data-stu-id="91f07-136">Subject Alternative Names (SANs) can be specified as DNS names.</span></span>

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

### <span data-ttu-id="91f07-137">-Ekus</span><span class="sxs-lookup"><span data-stu-id="91f07-137">-Ekus</span></span>
<span data-ttu-id="91f07-138">Especifica os usos avançados da chave (EKUs) no certificado.</span><span class="sxs-lookup"><span data-stu-id="91f07-138">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="91f07-139">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="91f07-139">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="91f07-140">Especifica o número de dias antes do vencimento do início do processo de notificação automática.</span><span class="sxs-lookup"><span data-stu-id="91f07-140">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="91f07-141">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="91f07-141">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="91f07-142">Especifica a porcentagem do tempo de vida após o qual o processo automático para a notificação é iniciado.</span><span class="sxs-lookup"><span data-stu-id="91f07-142">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="91f07-143">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="91f07-143">-IssuerName</span></span>
<span data-ttu-id="91f07-144">Especifica o nome do emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="91f07-144">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="91f07-145">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="91f07-145">-KeyNotExportable</span></span>
<span data-ttu-id="91f07-146">Indica que a chave não é exportável.</span><span class="sxs-lookup"><span data-stu-id="91f07-146">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="91f07-147">-KeySize</span><span class="sxs-lookup"><span data-stu-id="91f07-147">-KeySize</span></span>
<span data-ttu-id="91f07-148">Especifica o tamanho da chave do certificado.</span><span class="sxs-lookup"><span data-stu-id="91f07-148">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="91f07-149">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="91f07-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91f07-150">2048</span><span class="sxs-lookup"><span data-stu-id="91f07-150">2048</span></span>
- <span data-ttu-id="91f07-151">3072</span><span class="sxs-lookup"><span data-stu-id="91f07-151">3072</span></span>
- <span data-ttu-id="91f07-152">4096</span><span class="sxs-lookup"><span data-stu-id="91f07-152">4096</span></span>
- <span data-ttu-id="91f07-153">256</span><span class="sxs-lookup"><span data-stu-id="91f07-153">256</span></span>
- <span data-ttu-id="91f07-154">384</span><span class="sxs-lookup"><span data-stu-id="91f07-154">384</span></span>
- <span data-ttu-id="91f07-155">521</span><span class="sxs-lookup"><span data-stu-id="91f07-155">521</span></span>

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

### <span data-ttu-id="91f07-156">-KeyType</span><span class="sxs-lookup"><span data-stu-id="91f07-156">-KeyType</span></span>
<span data-ttu-id="91f07-157">Especifica o tipo de chave da chave que faz a backup do certificado.</span><span class="sxs-lookup"><span data-stu-id="91f07-157">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="91f07-158">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="91f07-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91f07-159">RSA</span><span class="sxs-lookup"><span data-stu-id="91f07-159">RSA</span></span>
- <span data-ttu-id="91f07-160">RSA – HSM</span><span class="sxs-lookup"><span data-stu-id="91f07-160">RSA-HSM</span></span>
- <span data-ttu-id="91f07-161">EC</span><span class="sxs-lookup"><span data-stu-id="91f07-161">EC</span></span>
- <span data-ttu-id="91f07-162">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="91f07-162">EC-HSM</span></span>

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

### <span data-ttu-id="91f07-163">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="91f07-163">-KeyUsage</span></span>
<span data-ttu-id="91f07-164">Especifica os usos da chave no certificado.</span><span class="sxs-lookup"><span data-stu-id="91f07-164">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="91f07-165">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="91f07-165">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="91f07-166">Especifica o número de dias antes da expiração após o início do processo automático para a renovação do certificado.</span><span class="sxs-lookup"><span data-stu-id="91f07-166">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="91f07-167">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="91f07-167">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="91f07-168">Especifica a porcentagem do tempo de vida após o qual o processo automático para a renovação do certificado é iniciado.</span><span class="sxs-lookup"><span data-stu-id="91f07-168">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="91f07-169">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="91f07-169">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="91f07-170">Indica que o certificado reutiliza a chave durante a renovação.</span><span class="sxs-lookup"><span data-stu-id="91f07-170">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="91f07-171">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="91f07-171">-SecretContentType</span></span>
<span data-ttu-id="91f07-172">Especifica o tipo de conteúdo do novo segredo do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="91f07-172">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="91f07-173">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="91f07-173">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91f07-174">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="91f07-174">application/x-pkcs12</span></span>
- <span data-ttu-id="91f07-175">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="91f07-175">application/x-pem-file</span></span>

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

### <span data-ttu-id="91f07-176">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="91f07-176">-SubjectName</span></span>
<span data-ttu-id="91f07-177">Especifica o nome do requerente do certificado.</span><span class="sxs-lookup"><span data-stu-id="91f07-177">Specifies the subject name of the certificate.</span></span> 

> [!NOTE]
> <span data-ttu-id="91f07-178">Se você deve usar uma vírgula (,) ou um ponto (.) dentro de uma propriedade no `SubjectName` parâmetro, você deve colocar o campo de propriedade entre aspas.</span><span class="sxs-lookup"><span data-stu-id="91f07-178">If you must use a comma (,) or a period (.) within a property in the `SubjectName` parameter, you must enclose the property field in quotation marks.</span></span> <span data-ttu-id="91f07-179">Por exemplo, você pode usar O = "contoso, Ltd."</span><span class="sxs-lookup"><span data-stu-id="91f07-179">For example, you may use O="Contoso, Ltd."</span></span> <span data-ttu-id="91f07-180">no campo nome da organização.</span><span class="sxs-lookup"><span data-stu-id="91f07-180">in the Organization Name field.</span></span>

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

### <span data-ttu-id="91f07-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="91f07-181">-ValidityInMonths</span></span>
<span data-ttu-id="91f07-182">Especifica o número de meses para o qual o certificado é válido.</span><span class="sxs-lookup"><span data-stu-id="91f07-182">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="91f07-183">-Confirme</span><span class="sxs-lookup"><span data-stu-id="91f07-183">-Confirm</span></span>
<span data-ttu-id="91f07-184">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91f07-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91f07-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91f07-185">-WhatIf</span></span>
<span data-ttu-id="91f07-186">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="91f07-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91f07-187">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="91f07-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91f07-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91f07-188">CommonParameters</span></span>
<span data-ttu-id="91f07-189">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91f07-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91f07-190">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91f07-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91f07-191">SENSORES</span><span class="sxs-lookup"><span data-stu-id="91f07-191">INPUTS</span></span>

### <span data-ttu-id="91f07-192">System. String</span><span class="sxs-lookup"><span data-stu-id="91f07-192">System.String</span></span>

### <span data-ttu-id="91f07-193">System. Collections. Generic. List ' 1 [System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="91f07-193">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="91f07-194">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="91f07-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="91f07-195">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="91f07-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="91f07-196">System. Collections. Generic. List ' 1 [System. Security. Cryptography. X509Certificates. X509KeyUsageFlags, System. Security. Cryptography. X509Certificates, Version = 4.2.1.0, Culture = neutral, PublicKeyToken = b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="91f07-196">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="91f07-197">EXIBE</span><span class="sxs-lookup"><span data-stu-id="91f07-197">OUTPUTS</span></span>

### <span data-ttu-id="91f07-198">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="91f07-198">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="91f07-199">INFORMA</span><span class="sxs-lookup"><span data-stu-id="91f07-199">NOTES</span></span>

## <span data-ttu-id="91f07-200">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91f07-200">RELATED LINKS</span></span>

[<span data-ttu-id="91f07-201">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="91f07-201">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="91f07-202">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="91f07-202">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

