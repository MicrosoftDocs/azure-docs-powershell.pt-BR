---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 09e58a029d3011c2abcee035ee23640f801825b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887723"
---
# <span data-ttu-id="1e150-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1e150-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="1e150-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e150-102">SYNOPSIS</span></span>
<span data-ttu-id="1e150-103">Cria ou atualiza a política de um certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="1e150-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="1e150-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1e150-104">SYNTAX</span></span>

### <span data-ttu-id="1e150-105">ExpandedRenewPercentage (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1e150-105">ExpandedRenewPercentage (Default)</span></span>
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

### <span data-ttu-id="1e150-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="1e150-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-KeySize <Int32>]
 [-CertificateTransparency <Boolean>] [-PassThru] [-Curve <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e150-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="1e150-107">ExpandedRenewNumber</span></span>
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

## <span data-ttu-id="1e150-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1e150-108">DESCRIPTION</span></span>
<span data-ttu-id="1e150-109">O cmdlet **Set-AzKeyVaultCertificatePolicy** cria ou atualiza a política de um certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="1e150-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="1e150-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1e150-110">EXAMPLES</span></span>

### <span data-ttu-id="1e150-111">Exemplo 1: definir uma política de certificado</span><span class="sxs-lookup"><span data-stu-id="1e150-111">Example 1: Set a certificate policy</span></span>
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

<span data-ttu-id="1e150-112">Este comando define a política do certificado TestCert01 no cofre de chaves ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="1e150-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="1e150-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1e150-113">PARAMETERS</span></span>

### <span data-ttu-id="1e150-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="1e150-114">-CertificateTransparency</span></span>
<span data-ttu-id="1e150-115">Indica se a transparência do certificado está habilitada para esse certificado/emissor; se não for especificado, o padrão será 'true'.</span><span class="sxs-lookup"><span data-stu-id="1e150-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'.</span></span>
<span data-ttu-id="1e150-116">`-IssuerName` precisa ser especificado ao definir essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="1e150-116">`-IssuerName` needs to be specified when setting this property.</span></span>

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

### <span data-ttu-id="1e150-117">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="1e150-117">-CertificateType</span></span>
<span data-ttu-id="1e150-118">Especifica o tipo de certificado para o emissor.</span><span class="sxs-lookup"><span data-stu-id="1e150-118">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="1e150-119">-Curve</span><span class="sxs-lookup"><span data-stu-id="1e150-119">-Curve</span></span>
<span data-ttu-id="1e150-120">Especifica o nome da curva elíptica da chave do certificado.</span><span class="sxs-lookup"><span data-stu-id="1e150-120">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="1e150-121">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1e150-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1e150-122">P-256</span><span class="sxs-lookup"><span data-stu-id="1e150-122">P-256</span></span>
- <span data-ttu-id="1e150-123">P-384</span><span class="sxs-lookup"><span data-stu-id="1e150-123">P-384</span></span>
- <span data-ttu-id="1e150-124">P-521</span><span class="sxs-lookup"><span data-stu-id="1e150-124">P-521</span></span>
- <span data-ttu-id="1e150-125">P-256K</span><span class="sxs-lookup"><span data-stu-id="1e150-125">P-256K</span></span>
- <span data-ttu-id="1e150-126">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="1e150-126">SECP256K1</span></span>

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

### <span data-ttu-id="1e150-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e150-127">-DefaultProfile</span></span>
<span data-ttu-id="1e150-128">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1e150-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e150-129">-Disabled</span><span class="sxs-lookup"><span data-stu-id="1e150-129">-Disabled</span></span>
<span data-ttu-id="1e150-130">Indica que a política de certificado está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="1e150-130">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="1e150-131">-DnsName</span><span class="sxs-lookup"><span data-stu-id="1e150-131">-DnsName</span></span>
<span data-ttu-id="1e150-132">Especifica o nome do assunto do certificado.</span><span class="sxs-lookup"><span data-stu-id="1e150-132">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="1e150-133">-Ekus</span><span class="sxs-lookup"><span data-stu-id="1e150-133">-Ekus</span></span>
<span data-ttu-id="1e150-134">Especifica os usos de chave aprimorados (EKUs) no certificado.</span><span class="sxs-lookup"><span data-stu-id="1e150-134">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="1e150-135">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="1e150-135">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="1e150-136">Especifica o número de dias antes da expiração quando a renovação automática deve começar.</span><span class="sxs-lookup"><span data-stu-id="1e150-136">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="1e150-137">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="1e150-137">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="1e150-138">Especifica a porcentagem do tempo de vida após o qual o processo automático para a notificação começa.</span><span class="sxs-lookup"><span data-stu-id="1e150-138">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="1e150-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e150-139">-InputObject</span></span>
<span data-ttu-id="1e150-140">Especifica a política de certificado.</span><span class="sxs-lookup"><span data-stu-id="1e150-140">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="1e150-141">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="1e150-141">-IssuerName</span></span>
<span data-ttu-id="1e150-142">Especifica o nome do emissor desse certificado.</span><span class="sxs-lookup"><span data-stu-id="1e150-142">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="1e150-143">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="1e150-143">-KeyNotExportable</span></span>
<span data-ttu-id="1e150-144">Indica que a chave não é exportável.</span><span class="sxs-lookup"><span data-stu-id="1e150-144">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="1e150-145">-KeySize</span><span class="sxs-lookup"><span data-stu-id="1e150-145">-KeySize</span></span>
<span data-ttu-id="1e150-146">Especifica o tamanho da chave do certificado.</span><span class="sxs-lookup"><span data-stu-id="1e150-146">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="1e150-147">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1e150-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1e150-148">2048</span><span class="sxs-lookup"><span data-stu-id="1e150-148">2048</span></span>
- <span data-ttu-id="1e150-149">3072</span><span class="sxs-lookup"><span data-stu-id="1e150-149">3072</span></span>
- <span data-ttu-id="1e150-150">4096</span><span class="sxs-lookup"><span data-stu-id="1e150-150">4096</span></span>
- <span data-ttu-id="1e150-151">256</span><span class="sxs-lookup"><span data-stu-id="1e150-151">256</span></span>
- <span data-ttu-id="1e150-152">384</span><span class="sxs-lookup"><span data-stu-id="1e150-152">384</span></span>
- <span data-ttu-id="1e150-153">521</span><span class="sxs-lookup"><span data-stu-id="1e150-153">521</span></span>

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

### <span data-ttu-id="1e150-154">-KeyType</span><span class="sxs-lookup"><span data-stu-id="1e150-154">-KeyType</span></span>
<span data-ttu-id="1e150-155">Especifica o tipo de chave da chave que ressalte o certificado.</span><span class="sxs-lookup"><span data-stu-id="1e150-155">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="1e150-156">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1e150-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1e150-157">RSA</span><span class="sxs-lookup"><span data-stu-id="1e150-157">RSA</span></span>
- <span data-ttu-id="1e150-158">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="1e150-158">RSA-HSM</span></span>
- <span data-ttu-id="1e150-159">EC</span><span class="sxs-lookup"><span data-stu-id="1e150-159">EC</span></span>
- <span data-ttu-id="1e150-160">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="1e150-160">EC-HSM</span></span>

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

### <span data-ttu-id="1e150-161">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="1e150-161">-KeyUsage</span></span>
<span data-ttu-id="1e150-162">Especifica os principais usos no certificado.</span><span class="sxs-lookup"><span data-stu-id="1e150-162">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="1e150-163">-Name</span><span class="sxs-lookup"><span data-stu-id="1e150-163">-Name</span></span>
<span data-ttu-id="1e150-164">Especifica o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="1e150-164">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="1e150-165">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e150-165">-PassThru</span></span>
<span data-ttu-id="1e150-166">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="1e150-166">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1e150-167">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="1e150-167">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1e150-168">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="1e150-168">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="1e150-169">Especifica o número de dias antes do vencimento após o qual o processo automático para renovação de certificado começa.</span><span class="sxs-lookup"><span data-stu-id="1e150-169">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="1e150-170">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="1e150-170">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="1e150-171">Especifica a porcentagem do tempo de vida após o qual o processo automático para renovação de certificados começa.</span><span class="sxs-lookup"><span data-stu-id="1e150-171">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="1e150-172">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="1e150-172">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="1e150-173">Indica que o certificado reutiliza a chave durante a renovação.</span><span class="sxs-lookup"><span data-stu-id="1e150-173">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="1e150-174">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="1e150-174">-SecretContentType</span></span>
<span data-ttu-id="1e150-175">Especifica o tipo de conteúdo do novo segredo do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="1e150-175">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="1e150-176">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1e150-176">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1e150-177">application/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="1e150-177">application/x-pkcs12</span></span>
- <span data-ttu-id="1e150-178">application/x-pem-file</span><span class="sxs-lookup"><span data-stu-id="1e150-178">application/x-pem-file</span></span>

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

### <span data-ttu-id="1e150-179">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="1e150-179">-SubjectName</span></span>
<span data-ttu-id="1e150-180">Especifica o nome do assunto do certificado.</span><span class="sxs-lookup"><span data-stu-id="1e150-180">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="1e150-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="1e150-181">-ValidityInMonths</span></span>
<span data-ttu-id="1e150-182">Especifica o número de meses em que o certificado é válido.</span><span class="sxs-lookup"><span data-stu-id="1e150-182">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="1e150-183">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1e150-183">-VaultName</span></span>
<span data-ttu-id="1e150-184">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="1e150-184">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="1e150-185">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e150-185">-Confirm</span></span>
<span data-ttu-id="1e150-186">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e150-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e150-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e150-187">-WhatIf</span></span>
<span data-ttu-id="1e150-188">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1e150-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e150-189">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1e150-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e150-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e150-190">CommonParameters</span></span>
<span data-ttu-id="1e150-191">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e150-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e150-192">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e150-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e150-193">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1e150-193">INPUTS</span></span>

### <span data-ttu-id="1e150-194">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1e150-194">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="1e150-195">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1e150-195">OUTPUTS</span></span>

### <span data-ttu-id="1e150-196">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1e150-196">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="1e150-197">NOTES</span><span class="sxs-lookup"><span data-stu-id="1e150-197">NOTES</span></span>

## <span data-ttu-id="1e150-198">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e150-198">RELATED LINKS</span></span>

[<span data-ttu-id="1e150-199">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1e150-199">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="1e150-200">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1e150-200">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

