---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 5a6b88ce85b8b9296d9666955a93d1240b631634
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942542"
---
# <span data-ttu-id="33498-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="33498-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="33498-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33498-102">SYNOPSIS</span></span>
<span data-ttu-id="33498-103">Cria ou atualiza a política de um certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="33498-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="33498-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33498-104">SYNTAX</span></span>

### <span data-ttu-id="33498-105">ExpandedRenewPercentage (padrão)</span><span class="sxs-lookup"><span data-stu-id="33498-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33498-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="33498-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-KeySize <Int32>]
 [-CertificateTransparency <Boolean>] [-PassThru] [-Curve <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33498-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="33498-107">ExpandedRenewNumber</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> -RenewAtNumberOfDaysBeforeExpiry <Int32>
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33498-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="33498-108">DESCRIPTION</span></span>
<span data-ttu-id="33498-109">O cmdlet **set-AzKeyVaultCertificatePolicy** cria ou atualiza a política de um certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="33498-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="33498-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33498-110">EXAMPLES</span></span>

### <span data-ttu-id="33498-111">Exemplo 1: definir uma política de certificado</span><span class="sxs-lookup"><span data-stu-id="33498-111">Example 1: Set a certificate policy</span></span>
```powershell
PS C:\> Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True -PassThru

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

<span data-ttu-id="33498-112">Este comando define a política do certificado TestCert01 no cofre da chave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="33498-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="33498-113">OS</span><span class="sxs-lookup"><span data-stu-id="33498-113">PARAMETERS</span></span>

### <span data-ttu-id="33498-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="33498-114">-CertificateTransparency</span></span>
<span data-ttu-id="33498-115">Indica se a transparência do certificado está habilitada para este certificado/emissor; Se não for especificado, o padrão será ' true '</span><span class="sxs-lookup"><span data-stu-id="33498-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33498-116">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="33498-116">-CertificateType</span></span>
<span data-ttu-id="33498-117">Especifica o tipo de certificado para o emissor.</span><span class="sxs-lookup"><span data-stu-id="33498-117">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33498-118">-Curve</span><span class="sxs-lookup"><span data-stu-id="33498-118">-Curve</span></span>
<span data-ttu-id="33498-119">Especifica o nome da curva elíptica da chave do certificado.</span><span class="sxs-lookup"><span data-stu-id="33498-119">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="33498-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="33498-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="33498-121">P a 256</span><span class="sxs-lookup"><span data-stu-id="33498-121">P-256</span></span>
- <span data-ttu-id="33498-122">P a 384</span><span class="sxs-lookup"><span data-stu-id="33498-122">P-384</span></span>
- <span data-ttu-id="33498-123">P a 521</span><span class="sxs-lookup"><span data-stu-id="33498-123">P-521</span></span>
- <span data-ttu-id="33498-124">P A 256K</span><span class="sxs-lookup"><span data-stu-id="33498-124">P-256K</span></span>
- <span data-ttu-id="33498-125">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="33498-125">SECP256K1</span></span>

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

### <span data-ttu-id="33498-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33498-126">-DefaultProfile</span></span>
<span data-ttu-id="33498-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="33498-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33498-128">-Desabilitado</span><span class="sxs-lookup"><span data-stu-id="33498-128">-Disabled</span></span>
<span data-ttu-id="33498-129">Indica que a política de certificado está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="33498-129">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33498-130">-DnsName</span><span class="sxs-lookup"><span data-stu-id="33498-130">-DnsName</span></span>
<span data-ttu-id="33498-131">Especifica o nome do requerente do certificado.</span><span class="sxs-lookup"><span data-stu-id="33498-131">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases: DnsNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33498-132">-Ekus</span><span class="sxs-lookup"><span data-stu-id="33498-132">-Ekus</span></span>
<span data-ttu-id="33498-133">Especifica os usos avançados da chave (EKUs) no certificado.</span><span class="sxs-lookup"><span data-stu-id="33498-133">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33498-134">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="33498-134">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="33498-135">Especifica o número de dias antes do vencimento quando a renovação automática deve começar.</span><span class="sxs-lookup"><span data-stu-id="33498-135">Specifies the number of days before expiration when automatic renewal should start.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33498-136">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="33498-136">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="33498-137">Especifica a porcentagem do tempo de vida após o qual o processo automático para a notificação é iniciado.</span><span class="sxs-lookup"><span data-stu-id="33498-137">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33498-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33498-138">-InputObject</span></span>
<span data-ttu-id="33498-139">Especifica a política de certificado.</span><span class="sxs-lookup"><span data-stu-id="33498-139">Specifies the certificate policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: CertificatePolicy

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33498-140">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="33498-140">-IssuerName</span></span>
<span data-ttu-id="33498-141">Especifica o nome do emissor para este certificado.</span><span class="sxs-lookup"><span data-stu-id="33498-141">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33498-142">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="33498-142">-KeyNotExportable</span></span>
<span data-ttu-id="33498-143">Indica que a chave não é exportável.</span><span class="sxs-lookup"><span data-stu-id="33498-143">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33498-144">-KeySize</span><span class="sxs-lookup"><span data-stu-id="33498-144">-KeySize</span></span>
<span data-ttu-id="33498-145">Especifica o tamanho da chave do certificado.</span><span class="sxs-lookup"><span data-stu-id="33498-145">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="33498-146">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="33498-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="33498-147">2048</span><span class="sxs-lookup"><span data-stu-id="33498-147">2048</span></span>
- <span data-ttu-id="33498-148">3072</span><span class="sxs-lookup"><span data-stu-id="33498-148">3072</span></span>
- <span data-ttu-id="33498-149">4096</span><span class="sxs-lookup"><span data-stu-id="33498-149">4096</span></span>
- <span data-ttu-id="33498-150">256</span><span class="sxs-lookup"><span data-stu-id="33498-150">256</span></span>
- <span data-ttu-id="33498-151">384</span><span class="sxs-lookup"><span data-stu-id="33498-151">384</span></span>
- <span data-ttu-id="33498-152">521</span><span class="sxs-lookup"><span data-stu-id="33498-152">521</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096, 256, 384, 521

Required: False
Position: Named
Default value: 2048
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33498-153">-KeyType</span><span class="sxs-lookup"><span data-stu-id="33498-153">-KeyType</span></span>
<span data-ttu-id="33498-154">Especifica o tipo de chave da chave que faz a backup do certificado.</span><span class="sxs-lookup"><span data-stu-id="33498-154">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="33498-155">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="33498-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="33498-156">RSA</span><span class="sxs-lookup"><span data-stu-id="33498-156">RSA</span></span>
- <span data-ttu-id="33498-157">RSA – HSM</span><span class="sxs-lookup"><span data-stu-id="33498-157">RSA-HSM</span></span>
- <span data-ttu-id="33498-158">EC</span><span class="sxs-lookup"><span data-stu-id="33498-158">EC</span></span>
- <span data-ttu-id="33498-159">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="33498-159">EC-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM, EC, EC-HSM

Required: False
Position: Named
Default value: RSA
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33498-160">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="33498-160">-KeyUsage</span></span>
<span data-ttu-id="33498-161">Especifica os usos da chave no certificado.</span><span class="sxs-lookup"><span data-stu-id="33498-161">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: None, EncipherOnly, CrlSign, KeyCertSign, KeyAgreement, DataEncipherment, KeyEncipherment, NonRepudiation, DigitalSignature, DecipherOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33498-162">-Nome</span><span class="sxs-lookup"><span data-stu-id="33498-162">-Name</span></span>
<span data-ttu-id="33498-163">Especifica o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="33498-163">Specifies the name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33498-164">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33498-164">-PassThru</span></span>
<span data-ttu-id="33498-165">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="33498-165">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="33498-166">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="33498-166">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33498-167">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="33498-167">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="33498-168">Especifica o número de dias antes da expiração após o início do processo automático para a renovação do certificado.</span><span class="sxs-lookup"><span data-stu-id="33498-168">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewNumber
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33498-169">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="33498-169">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="33498-170">Especifica a porcentagem do tempo de vida após o qual o processo automático para a renovação do certificado é iniciado.</span><span class="sxs-lookup"><span data-stu-id="33498-170">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewPercentage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33498-171">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="33498-171">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="33498-172">Indica que o certificado reutiliza a chave durante a renovação.</span><span class="sxs-lookup"><span data-stu-id="33498-172">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33498-173">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="33498-173">-SecretContentType</span></span>
<span data-ttu-id="33498-174">Especifica o tipo de conteúdo do novo segredo do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="33498-174">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="33498-175">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="33498-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="33498-176">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="33498-176">application/x-pkcs12</span></span>
- <span data-ttu-id="33498-177">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="33498-177">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33498-178">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="33498-178">-SubjectName</span></span>
<span data-ttu-id="33498-179">Especifica o nome do requerente do certificado.</span><span class="sxs-lookup"><span data-stu-id="33498-179">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33498-180">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="33498-180">-ValidityInMonths</span></span>
<span data-ttu-id="33498-181">Especifica o número de meses para o qual o certificado é válido.</span><span class="sxs-lookup"><span data-stu-id="33498-181">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33498-182">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="33498-182">-VaultName</span></span>
<span data-ttu-id="33498-183">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="33498-183">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33498-184">-Confirme</span><span class="sxs-lookup"><span data-stu-id="33498-184">-Confirm</span></span>
<span data-ttu-id="33498-185">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33498-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33498-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33498-186">-WhatIf</span></span>
<span data-ttu-id="33498-187">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="33498-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33498-188">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="33498-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33498-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33498-189">CommonParameters</span></span>
<span data-ttu-id="33498-190">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33498-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33498-191">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33498-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33498-192">SENSORES</span><span class="sxs-lookup"><span data-stu-id="33498-192">INPUTS</span></span>

### <span data-ttu-id="33498-193">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="33498-193">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="33498-194">EXIBE</span><span class="sxs-lookup"><span data-stu-id="33498-194">OUTPUTS</span></span>

### <span data-ttu-id="33498-195">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="33498-195">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="33498-196">INFORMA</span><span class="sxs-lookup"><span data-stu-id="33498-196">NOTES</span></span>

## <span data-ttu-id="33498-197">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33498-197">RELATED LINKS</span></span>

[<span data-ttu-id="33498-198">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="33498-198">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="33498-199">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="33498-199">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

