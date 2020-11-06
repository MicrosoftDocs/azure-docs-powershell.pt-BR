---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 271da96d18628c899b10ac17185fd4c3a921d8a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428101"
---
# <span data-ttu-id="5b46f-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="5b46f-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="5b46f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5b46f-102">SYNOPSIS</span></span>
<span data-ttu-id="5b46f-103">Cria ou atualiza a política de um certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5b46f-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b46f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b46f-104">SYNTAX</span></span>

### <span data-ttu-id="5b46f-105">ExpandedRenewPercentage (padrão)</span><span class="sxs-lookup"><span data-stu-id="5b46f-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b46f-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="5b46f-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b46f-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="5b46f-107">ExpandedRenewNumber</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 -RenewAtNumberOfDaysBeforeExpiry <Int32> [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>]
 [-Disabled] [-SubjectName <String>] [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b46f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5b46f-108">DESCRIPTION</span></span>
<span data-ttu-id="5b46f-109">O cmdlet **set-AzureKeyVaultCertificatePolicy** cria ou atualiza a política de um certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5b46f-109">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="5b46f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5b46f-110">EXAMPLES</span></span>

### <span data-ttu-id="5b46f-111">Exemplo 1: definir uma política de certificado</span><span class="sxs-lookup"><span data-stu-id="5b46f-111">Example 1: Set a certificate policy</span></span>
```powershell
PS C:\> Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True -PassThru

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

<span data-ttu-id="5b46f-112">Este comando define a política do certificado TestCert01 no cofre da chave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="5b46f-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="5b46f-113">OS</span><span class="sxs-lookup"><span data-stu-id="5b46f-113">PARAMETERS</span></span>

### <span data-ttu-id="5b46f-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="5b46f-114">-CertificateTransparency</span></span>
<span data-ttu-id="5b46f-115">Indica se a transparência do certificado está habilitada para este certificado/emissor; Se não for especificado, o padrão será ' true '</span><span class="sxs-lookup"><span data-stu-id="5b46f-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="5b46f-116">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="5b46f-116">-CertificateType</span></span>
<span data-ttu-id="5b46f-117">Especifica o tipo de certificado para o emissor.</span><span class="sxs-lookup"><span data-stu-id="5b46f-117">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="5b46f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b46f-118">-DefaultProfile</span></span>
<span data-ttu-id="5b46f-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5b46f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b46f-120">-Desabilitado</span><span class="sxs-lookup"><span data-stu-id="5b46f-120">-Disabled</span></span>
<span data-ttu-id="5b46f-121">Indica que a política de certificado está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="5b46f-121">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="5b46f-122">-DnsName</span><span class="sxs-lookup"><span data-stu-id="5b46f-122">-DnsName</span></span>
<span data-ttu-id="5b46f-123">Especifica o nome do requerente do certificado.</span><span class="sxs-lookup"><span data-stu-id="5b46f-123">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="5b46f-124">-Ekus</span><span class="sxs-lookup"><span data-stu-id="5b46f-124">-Ekus</span></span>
<span data-ttu-id="5b46f-125">Especifica os usos avançados da chave (EKUs) no certificado.</span><span class="sxs-lookup"><span data-stu-id="5b46f-125">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="5b46f-126">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="5b46f-126">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="5b46f-127">Especifica o número de dias antes do vencimento quando a renovação automática deve começar.</span><span class="sxs-lookup"><span data-stu-id="5b46f-127">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="5b46f-128">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="5b46f-128">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="5b46f-129">Especifica a porcentagem do tempo de vida após o qual o processo automático para a notificação é iniciado.</span><span class="sxs-lookup"><span data-stu-id="5b46f-129">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="5b46f-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b46f-130">-InputObject</span></span>
<span data-ttu-id="5b46f-131">Especifica a política de certificado.</span><span class="sxs-lookup"><span data-stu-id="5b46f-131">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="5b46f-132">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="5b46f-132">-IssuerName</span></span>
<span data-ttu-id="5b46f-133">Especifica o nome do emissor para este certificado.</span><span class="sxs-lookup"><span data-stu-id="5b46f-133">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="5b46f-134">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="5b46f-134">-KeyNotExportable</span></span>
<span data-ttu-id="5b46f-135">Indica que a chave não é exportável.</span><span class="sxs-lookup"><span data-stu-id="5b46f-135">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="5b46f-136">-KeyType</span><span class="sxs-lookup"><span data-stu-id="5b46f-136">-KeyType</span></span>
<span data-ttu-id="5b46f-137">Especifica o tipo de chave da chave que faz a backup do certificado.</span><span class="sxs-lookup"><span data-stu-id="5b46f-137">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="5b46f-138">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="5b46f-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5b46f-139">RSA</span><span class="sxs-lookup"><span data-stu-id="5b46f-139">RSA</span></span>
- <span data-ttu-id="5b46f-140">RSA – HSM</span><span class="sxs-lookup"><span data-stu-id="5b46f-140">RSA-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b46f-141">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="5b46f-141">-KeyUsage</span></span>
<span data-ttu-id="5b46f-142">Especifica os usos da chave no certificado.</span><span class="sxs-lookup"><span data-stu-id="5b46f-142">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="5b46f-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b46f-143">-Name</span></span>
<span data-ttu-id="5b46f-144">Especifica o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="5b46f-144">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="5b46f-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b46f-145">-PassThru</span></span>
<span data-ttu-id="5b46f-146">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="5b46f-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5b46f-147">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="5b46f-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5b46f-148">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="5b46f-148">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="5b46f-149">Especifica o número de dias antes da expiração após o início do processo automático para a renovação do certificado.</span><span class="sxs-lookup"><span data-stu-id="5b46f-149">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="5b46f-150">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="5b46f-150">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="5b46f-151">Especifica a porcentagem do tempo de vida após o qual o processo automático para a renovação do certificado é iniciado.</span><span class="sxs-lookup"><span data-stu-id="5b46f-151">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="5b46f-152">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="5b46f-152">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="5b46f-153">Indica que o certificado reutiliza a chave durante a renovação.</span><span class="sxs-lookup"><span data-stu-id="5b46f-153">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="5b46f-154">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="5b46f-154">-SecretContentType</span></span>
<span data-ttu-id="5b46f-155">Especifica o tipo de conteúdo do novo segredo do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5b46f-155">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="5b46f-156">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="5b46f-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5b46f-157">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="5b46f-157">application/x-pkcs12</span></span>
- <span data-ttu-id="5b46f-158">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="5b46f-158">application/x-pem-file</span></span>

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

### <span data-ttu-id="5b46f-159">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="5b46f-159">-SubjectName</span></span>
<span data-ttu-id="5b46f-160">Especifica o nome do requerente do certificado.</span><span class="sxs-lookup"><span data-stu-id="5b46f-160">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="5b46f-161">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="5b46f-161">-ValidityInMonths</span></span>
<span data-ttu-id="5b46f-162">Especifica o número de meses para o qual o certificado é válido.</span><span class="sxs-lookup"><span data-stu-id="5b46f-162">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="5b46f-163">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="5b46f-163">-VaultName</span></span>
<span data-ttu-id="5b46f-164">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5b46f-164">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="5b46f-165">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5b46f-165">-Confirm</span></span>
<span data-ttu-id="5b46f-166">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b46f-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b46f-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b46f-167">-WhatIf</span></span>
<span data-ttu-id="5b46f-168">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5b46f-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b46f-169">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5b46f-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b46f-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b46f-170">CommonParameters</span></span>
<span data-ttu-id="5b46f-171">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b46f-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b46f-172">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b46f-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b46f-173">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5b46f-173">INPUTS</span></span>

### <span data-ttu-id="5b46f-174">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="5b46f-174">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="5b46f-175">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5b46f-175">OUTPUTS</span></span>

### <span data-ttu-id="5b46f-176">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="5b46f-176">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="5b46f-177">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5b46f-177">NOTES</span></span>

## <span data-ttu-id="5b46f-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b46f-178">RELATED LINKS</span></span>

[<span data-ttu-id="5b46f-179">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="5b46f-179">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="5b46f-180">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="5b46f-180">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

