---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: caa0961c1b7aebd5fd2f9883831d733a0fa69f1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439866"
---
# <span data-ttu-id="0deb0-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0deb0-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="0deb0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0deb0-102">SYNOPSIS</span></span>
<span data-ttu-id="0deb0-103">Cria um objeto de política de certificado na memória.</span><span class="sxs-lookup"><span data-stu-id="0deb0-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0deb0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0deb0-104">SYNTAX</span></span>

### <span data-ttu-id="0deb0-105">SubjectName (padrão)</span><span class="sxs-lookup"><span data-stu-id="0deb0-105">SubjectName (Default)</span></span>
```
New-AzureKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled] [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0deb0-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="0deb0-106">DNSNames</span></span>
```
New-AzureKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0deb0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0deb0-107">DESCRIPTION</span></span>
<span data-ttu-id="0deb0-108">O cmdlet **New-AzureKeyVaultCertificatePolicy** cria um objeto de política de certificado na memória para o Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="0deb0-108">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="0deb0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0deb0-109">EXAMPLES</span></span>

### <span data-ttu-id="0deb0-110">Exemplo 1: criar uma política de certificado</span><span class="sxs-lookup"><span data-stu-id="0deb0-110">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="0deb0-111">Esse comando cria uma política de certificado válida por seis meses e reutiliza a chave para renovar o certificado.</span><span class="sxs-lookup"><span data-stu-id="0deb0-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="0deb0-112">OS</span><span class="sxs-lookup"><span data-stu-id="0deb0-112">PARAMETERS</span></span>

### <span data-ttu-id="0deb0-113">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="0deb0-113">-CertificateType</span></span>
<span data-ttu-id="0deb0-114">Especifica o tipo de certificado para o emissor.</span><span class="sxs-lookup"><span data-stu-id="0deb0-114">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0deb0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0deb0-115">-DefaultProfile</span></span>
<span data-ttu-id="0deb0-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0deb0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0deb0-117">-Desabilitado</span><span class="sxs-lookup"><span data-stu-id="0deb0-117">-Disabled</span></span>
<span data-ttu-id="0deb0-118">Indica que a política de certificado está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="0deb0-118">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0deb0-119">-DnsName</span><span class="sxs-lookup"><span data-stu-id="0deb0-119">-DnsName</span></span>
<span data-ttu-id="0deb0-120">Especifica os nomes DNS no certificado.</span><span class="sxs-lookup"><span data-stu-id="0deb0-120">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="0deb0-121">-Ekus</span><span class="sxs-lookup"><span data-stu-id="0deb0-121">-Ekus</span></span>
<span data-ttu-id="0deb0-122">Especifica os usos avançados da chave (EKUs) no certificado.</span><span class="sxs-lookup"><span data-stu-id="0deb0-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="0deb0-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="0deb0-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="0deb0-124">Especifica o número de dias antes do vencimento do início do processo de notificação automática.</span><span class="sxs-lookup"><span data-stu-id="0deb0-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0deb0-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="0deb0-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="0deb0-126">Especifica a porcentagem do tempo de vida após o qual o processo automático para a notificação é iniciado.</span><span class="sxs-lookup"><span data-stu-id="0deb0-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0deb0-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="0deb0-127">-IssuerName</span></span>
<span data-ttu-id="0deb0-128">Especifica o nome do emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="0deb0-128">Specifies the name of the issuer for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0deb0-129">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="0deb0-129">-KeyNotExportable</span></span>
<span data-ttu-id="0deb0-130">Indica que a chave não é exportável.</span><span class="sxs-lookup"><span data-stu-id="0deb0-130">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0deb0-131">-KeyType</span><span class="sxs-lookup"><span data-stu-id="0deb0-131">-KeyType</span></span>
<span data-ttu-id="0deb0-132">Especifica o tipo de chave da chave que faz a backup do certificado.</span><span class="sxs-lookup"><span data-stu-id="0deb0-132">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="0deb0-133">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="0deb0-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0deb0-134">RSA</span><span class="sxs-lookup"><span data-stu-id="0deb0-134">RSA</span></span>
- <span data-ttu-id="0deb0-135">RSA – HSM</span><span class="sxs-lookup"><span data-stu-id="0deb0-135">RSA-HSM</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0deb0-136">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="0deb0-136">-KeyUsage</span></span>
<span data-ttu-id="0deb0-137">Especifica os usos da chave no certificado.</span><span class="sxs-lookup"><span data-stu-id="0deb0-137">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="0deb0-138">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="0deb0-138">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="0deb0-139">Especifica o número de dias antes da expiração após o início do processo automático para a renovação do certificado.</span><span class="sxs-lookup"><span data-stu-id="0deb0-139">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0deb0-140">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="0deb0-140">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="0deb0-141">Especifica a porcentagem do tempo de vida após o qual o processo automático para a renovação do certificado é iniciado.</span><span class="sxs-lookup"><span data-stu-id="0deb0-141">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0deb0-142">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="0deb0-142">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="0deb0-143">Indica que o certificado reutiliza a chave durante a renovação.</span><span class="sxs-lookup"><span data-stu-id="0deb0-143">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0deb0-144">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="0deb0-144">-SecretContentType</span></span>
<span data-ttu-id="0deb0-145">Especifica o tipo de conteúdo do novo segredo do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="0deb0-145">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="0deb0-146">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="0deb0-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0deb0-147">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="0deb0-147">application/x-pkcs12</span></span>
- <span data-ttu-id="0deb0-148">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="0deb0-148">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0deb0-149">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="0deb0-149">-SubjectName</span></span>
<span data-ttu-id="0deb0-150">Especifica o nome do requerente do certificado.</span><span class="sxs-lookup"><span data-stu-id="0deb0-150">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: SubjectName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DNSNames
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0deb0-151">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="0deb0-151">-ValidityInMonths</span></span>
<span data-ttu-id="0deb0-152">Especifica o número de meses para o qual o certificado é válido.</span><span class="sxs-lookup"><span data-stu-id="0deb0-152">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0deb0-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0deb0-153">-Confirm</span></span>
<span data-ttu-id="0deb0-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0deb0-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0deb0-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0deb0-155">-WhatIf</span></span>
<span data-ttu-id="0deb0-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0deb0-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0deb0-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0deb0-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0deb0-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0deb0-158">CommonParameters</span></span>
<span data-ttu-id="0deb0-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0deb0-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0deb0-160">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0deb0-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0deb0-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0deb0-161">INPUTS</span></span>

### <span data-ttu-id="0deb0-162">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0deb0-162">None</span></span>
<span data-ttu-id="0deb0-163">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="0deb0-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0deb0-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0deb0-164">OUTPUTS</span></span>

### <span data-ttu-id="0deb0-165">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0deb0-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="0deb0-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0deb0-166">NOTES</span></span>

## <span data-ttu-id="0deb0-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0deb0-167">RELATED LINKS</span></span>

[<span data-ttu-id="0deb0-168">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0deb0-168">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="0deb0-169">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0deb0-169">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

