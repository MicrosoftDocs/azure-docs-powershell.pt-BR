---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-AzKeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 83eea8c8a030c5d22368bc0ede42c71e92df14a2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775787"
---
# <span data-ttu-id="80d7d-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="80d7d-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="80d7d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="80d7d-102">SYNOPSIS</span></span>
<span data-ttu-id="80d7d-103">Cria um objeto de política de certificado na memória.</span><span class="sxs-lookup"><span data-stu-id="80d7d-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="80d7d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80d7d-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificatePolicy [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-SubjectName <String>] [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] -IssuerName <String>
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80d7d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="80d7d-105">DESCRIPTION</span></span>
<span data-ttu-id="80d7d-106">O cmdlet **New-AzKeyVaultCertificatePolicy** cria um objeto de política de certificado na memória para o Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="80d7d-106">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="80d7d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80d7d-107">EXAMPLES</span></span>

### <span data-ttu-id="80d7d-108">Exemplo 1: criar uma política de certificado</span><span class="sxs-lookup"><span data-stu-id="80d7d-108">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="80d7d-109">Esse comando cria uma política de certificado válida por seis meses e reutiliza a chave para renovar o certificado.</span><span class="sxs-lookup"><span data-stu-id="80d7d-109">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="80d7d-110">OS</span><span class="sxs-lookup"><span data-stu-id="80d7d-110">PARAMETERS</span></span>

### <span data-ttu-id="80d7d-111">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="80d7d-111">-CertificateType</span></span>
<span data-ttu-id="80d7d-112">Especifica o tipo de certificado para o emissor.</span><span class="sxs-lookup"><span data-stu-id="80d7d-112">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="80d7d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80d7d-113">-DefaultProfile</span></span>
<span data-ttu-id="80d7d-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="80d7d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80d7d-115">-Desabilitado</span><span class="sxs-lookup"><span data-stu-id="80d7d-115">-Disabled</span></span>
<span data-ttu-id="80d7d-116">Indica que a política de certificado está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="80d7d-116">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="80d7d-117">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="80d7d-117">-DnsNames</span></span>
<span data-ttu-id="80d7d-118">Especifica os nomes DNS no certificado.</span><span class="sxs-lookup"><span data-stu-id="80d7d-118">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="80d7d-119">-Ekus</span><span class="sxs-lookup"><span data-stu-id="80d7d-119">-Ekus</span></span>
<span data-ttu-id="80d7d-120">Especifica os usos avançados da chave (EKUs) no certificado.</span><span class="sxs-lookup"><span data-stu-id="80d7d-120">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="80d7d-121">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="80d7d-121">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="80d7d-122">Especifica o número de dias antes do vencimento do início do processo de notificação automática.</span><span class="sxs-lookup"><span data-stu-id="80d7d-122">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="80d7d-123">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="80d7d-123">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="80d7d-124">Especifica a porcentagem do tempo de vida após o qual o processo automático para a notificação é iniciado.</span><span class="sxs-lookup"><span data-stu-id="80d7d-124">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="80d7d-125">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="80d7d-125">-IssuerName</span></span>
<span data-ttu-id="80d7d-126">Especifica o nome do emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="80d7d-126">Specifies the name of the issuer for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80d7d-127">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="80d7d-127">-KeyNotExportable</span></span>
<span data-ttu-id="80d7d-128">Indica que a chave não é exportável.</span><span class="sxs-lookup"><span data-stu-id="80d7d-128">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="80d7d-129">-KeyType</span><span class="sxs-lookup"><span data-stu-id="80d7d-129">-KeyType</span></span>
<span data-ttu-id="80d7d-130">Especifica o tipo de chave da chave que faz a backup do certificado.</span><span class="sxs-lookup"><span data-stu-id="80d7d-130">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="80d7d-131">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="80d7d-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="80d7d-132">RSA</span><span class="sxs-lookup"><span data-stu-id="80d7d-132">RSA</span></span>
- <span data-ttu-id="80d7d-133">RSA – HSM</span><span class="sxs-lookup"><span data-stu-id="80d7d-133">RSA-HSM</span></span>

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

### <span data-ttu-id="80d7d-134">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="80d7d-134">-KeyUsage</span></span>
<span data-ttu-id="80d7d-135">Especifica os usos da chave no certificado.</span><span class="sxs-lookup"><span data-stu-id="80d7d-135">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="80d7d-136">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="80d7d-136">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="80d7d-137">Especifica o número de dias antes da expiração após o início do processo automático para a renovação do certificado.</span><span class="sxs-lookup"><span data-stu-id="80d7d-137">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="80d7d-138">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="80d7d-138">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="80d7d-139">Especifica a porcentagem do tempo de vida após o qual o processo automático para a renovação do certificado é iniciado.</span><span class="sxs-lookup"><span data-stu-id="80d7d-139">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="80d7d-140">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="80d7d-140">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="80d7d-141">Indica que o certificado reutiliza a chave durante a renovação.</span><span class="sxs-lookup"><span data-stu-id="80d7d-141">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="80d7d-142">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="80d7d-142">-SecretContentType</span></span>
<span data-ttu-id="80d7d-143">Especifica o tipo de conteúdo do novo segredo do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="80d7d-143">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="80d7d-144">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="80d7d-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="80d7d-145">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="80d7d-145">application/x-pkcs12</span></span>
- <span data-ttu-id="80d7d-146">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="80d7d-146">application/x-pem-file</span></span>

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

### <span data-ttu-id="80d7d-147">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="80d7d-147">-SubjectName</span></span>
<span data-ttu-id="80d7d-148">Especifica o nome do requerente do certificado.</span><span class="sxs-lookup"><span data-stu-id="80d7d-148">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="80d7d-149">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="80d7d-149">-ValidityInMonths</span></span>
<span data-ttu-id="80d7d-150">Especifica o número de meses para o qual o certificado é válido.</span><span class="sxs-lookup"><span data-stu-id="80d7d-150">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="80d7d-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="80d7d-151">-Confirm</span></span>
<span data-ttu-id="80d7d-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80d7d-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80d7d-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80d7d-153">-WhatIf</span></span>
<span data-ttu-id="80d7d-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="80d7d-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80d7d-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="80d7d-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80d7d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80d7d-156">CommonParameters</span></span>
<span data-ttu-id="80d7d-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80d7d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80d7d-158">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80d7d-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80d7d-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="80d7d-159">INPUTS</span></span>

### <span data-ttu-id="80d7d-160">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="80d7d-160">None</span></span>
<span data-ttu-id="80d7d-161">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="80d7d-161">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="80d7d-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="80d7d-162">OUTPUTS</span></span>

### <span data-ttu-id="80d7d-163">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="80d7d-163">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="80d7d-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="80d7d-164">NOTES</span></span>

## <span data-ttu-id="80d7d-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80d7d-165">RELATED LINKS</span></span>

[<span data-ttu-id="80d7d-166">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="80d7d-166">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="80d7d-167">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="80d7d-167">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)
