---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 262c539d9ff97983494de0951c9a5d47510b0d28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596185"
---
# <span data-ttu-id="a6dc1-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="a6dc1-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="a6dc1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6dc1-102">SYNOPSIS</span></span>
<span data-ttu-id="a6dc1-103">Cria um objeto de política de certificado na memória.</span><span class="sxs-lookup"><span data-stu-id="a6dc1-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="a6dc1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6dc1-104">SYNTAX</span></span>

### <span data-ttu-id="a6dc1-105">SubjectName (padrão)</span><span class="sxs-lookup"><span data-stu-id="a6dc1-105">SubjectName (Default)</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeySize <Int32>] [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6dc1-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="a6dc1-106">DNSNames</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeySize <Int32>] [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6dc1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6dc1-107">DESCRIPTION</span></span>
<span data-ttu-id="a6dc1-108">O cmdlet **New-AzKeyVaultCertificatePolicy** cria um objeto de política de certificado na memória para o Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a6dc1-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="a6dc1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6dc1-109">EXAMPLES</span></span>

### <span data-ttu-id="a6dc1-110">Exemplo 1: criar uma política de certificado</span><span class="sxs-lookup"><span data-stu-id="a6dc1-110">Example 1: Create a certificate policy</span></span>
```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal

SecretContentType               : application/x-pkcs12
Kty                             :
KeySize                         : 2048
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

<span data-ttu-id="a6dc1-111">Esse comando cria uma política de certificado válida por seis meses e reutiliza a chave para renovar o certificado.</span><span class="sxs-lookup"><span data-stu-id="a6dc1-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="a6dc1-112">OS</span><span class="sxs-lookup"><span data-stu-id="a6dc1-112">PARAMETERS</span></span>

### <span data-ttu-id="a6dc1-113">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="a6dc1-113">-CertificateType</span></span>
<span data-ttu-id="a6dc1-114">Especifica o tipo de certificado para o emissor.</span><span class="sxs-lookup"><span data-stu-id="a6dc1-114">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="a6dc1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6dc1-115">-DefaultProfile</span></span>
<span data-ttu-id="a6dc1-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a6dc1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6dc1-117">-Desabilitado</span><span class="sxs-lookup"><span data-stu-id="a6dc1-117">-Disabled</span></span>
<span data-ttu-id="a6dc1-118">Indica que a política de certificado está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="a6dc1-118">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="a6dc1-119">-DnsName</span><span class="sxs-lookup"><span data-stu-id="a6dc1-119">-DnsName</span></span>
<span data-ttu-id="a6dc1-120">Especifica os nomes DNS no certificado.</span><span class="sxs-lookup"><span data-stu-id="a6dc1-120">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="a6dc1-121">-Ekus</span><span class="sxs-lookup"><span data-stu-id="a6dc1-121">-Ekus</span></span>
<span data-ttu-id="a6dc1-122">Especifica os usos avançados da chave (EKUs) no certificado.</span><span class="sxs-lookup"><span data-stu-id="a6dc1-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="a6dc1-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="a6dc1-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="a6dc1-124">Especifica o número de dias antes do vencimento do início do processo de notificação automática.</span><span class="sxs-lookup"><span data-stu-id="a6dc1-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="a6dc1-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="a6dc1-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="a6dc1-126">Especifica a porcentagem do tempo de vida após o qual o processo automático para a notificação é iniciado.</span><span class="sxs-lookup"><span data-stu-id="a6dc1-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="a6dc1-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="a6dc1-127">-IssuerName</span></span>
<span data-ttu-id="a6dc1-128">Especifica o nome do emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="a6dc1-128">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="a6dc1-129">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="a6dc1-129">-KeyNotExportable</span></span>
<span data-ttu-id="a6dc1-130">Indica que a chave não é exportável.</span><span class="sxs-lookup"><span data-stu-id="a6dc1-130">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="a6dc1-131">-KeySize</span><span class="sxs-lookup"><span data-stu-id="a6dc1-131">-KeySize</span></span>
<span data-ttu-id="a6dc1-132">Especifica o tamanho da chave do certificado.</span><span class="sxs-lookup"><span data-stu-id="a6dc1-132">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="a6dc1-133">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a6dc1-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a6dc1-134">2048</span><span class="sxs-lookup"><span data-stu-id="a6dc1-134">2048</span></span>
- <span data-ttu-id="a6dc1-135">3072</span><span class="sxs-lookup"><span data-stu-id="a6dc1-135">3072</span></span>
- <span data-ttu-id="a6dc1-136">4096</span><span class="sxs-lookup"><span data-stu-id="a6dc1-136">4096</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6dc1-137">-KeyType</span><span class="sxs-lookup"><span data-stu-id="a6dc1-137">-KeyType</span></span>
<span data-ttu-id="a6dc1-138">Especifica o tipo de chave da chave que faz a backup do certificado.</span><span class="sxs-lookup"><span data-stu-id="a6dc1-138">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="a6dc1-139">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a6dc1-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a6dc1-140">RSA</span><span class="sxs-lookup"><span data-stu-id="a6dc1-140">RSA</span></span>
- <span data-ttu-id="a6dc1-141">RSA – HSM</span><span class="sxs-lookup"><span data-stu-id="a6dc1-141">RSA-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6dc1-142">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="a6dc1-142">-KeyUsage</span></span>
<span data-ttu-id="a6dc1-143">Especifica os usos da chave no certificado.</span><span class="sxs-lookup"><span data-stu-id="a6dc1-143">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="a6dc1-144">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="a6dc1-144">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="a6dc1-145">Especifica o número de dias antes da expiração após o início do processo automático para a renovação do certificado.</span><span class="sxs-lookup"><span data-stu-id="a6dc1-145">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="a6dc1-146">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="a6dc1-146">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="a6dc1-147">Especifica a porcentagem do tempo de vida após o qual o processo automático para a renovação do certificado é iniciado.</span><span class="sxs-lookup"><span data-stu-id="a6dc1-147">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="a6dc1-148">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="a6dc1-148">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="a6dc1-149">Indica que o certificado reutiliza a chave durante a renovação.</span><span class="sxs-lookup"><span data-stu-id="a6dc1-149">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="a6dc1-150">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="a6dc1-150">-SecretContentType</span></span>
<span data-ttu-id="a6dc1-151">Especifica o tipo de conteúdo do novo segredo do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="a6dc1-151">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="a6dc1-152">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a6dc1-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a6dc1-153">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="a6dc1-153">application/x-pkcs12</span></span>
- <span data-ttu-id="a6dc1-154">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="a6dc1-154">application/x-pem-file</span></span>

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

### <span data-ttu-id="a6dc1-155">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="a6dc1-155">-SubjectName</span></span>
<span data-ttu-id="a6dc1-156">Especifica o nome do requerente do certificado.</span><span class="sxs-lookup"><span data-stu-id="a6dc1-156">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="a6dc1-157">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="a6dc1-157">-ValidityInMonths</span></span>
<span data-ttu-id="a6dc1-158">Especifica o número de meses para o qual o certificado é válido.</span><span class="sxs-lookup"><span data-stu-id="a6dc1-158">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="a6dc1-159">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a6dc1-159">-Confirm</span></span>
<span data-ttu-id="a6dc1-160">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6dc1-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6dc1-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6dc1-161">-WhatIf</span></span>
<span data-ttu-id="a6dc1-162">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a6dc1-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6dc1-163">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a6dc1-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6dc1-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6dc1-164">CommonParameters</span></span>
<span data-ttu-id="a6dc1-165">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6dc1-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6dc1-166">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6dc1-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6dc1-167">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6dc1-167">INPUTS</span></span>

### <span data-ttu-id="a6dc1-168">System. String</span><span class="sxs-lookup"><span data-stu-id="a6dc1-168">System.String</span></span>

### <span data-ttu-id="a6dc1-169">System. Collections. Generic. List ' 1 [System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a6dc1-169">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a6dc1-170">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a6dc1-170">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a6dc1-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a6dc1-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a6dc1-172">System. Collections. Generic. List ' 1 [System. Security. Cryptography. X509Certificates. X509KeyUsageFlags, System. Security. Cryptography. X509Certificates, Version = 4.2.1.0, Culture = neutral, PublicKeyToken = b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="a6dc1-172">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="a6dc1-173">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6dc1-173">OUTPUTS</span></span>

### <span data-ttu-id="a6dc1-174">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="a6dc1-174">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="a6dc1-175">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6dc1-175">NOTES</span></span>

## <span data-ttu-id="a6dc1-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6dc1-176">RELATED LINKS</span></span>

[<span data-ttu-id="a6dc1-177">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="a6dc1-177">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="a6dc1-178">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="a6dc1-178">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

