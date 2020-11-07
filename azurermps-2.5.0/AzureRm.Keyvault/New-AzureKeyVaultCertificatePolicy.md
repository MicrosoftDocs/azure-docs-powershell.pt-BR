---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificatepolicy
schema: 2.0.0
ms.openlocfilehash: b10dd0e034db53af35c930ce1c4588dee2576c75
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785528"
---
# <span data-ttu-id="d2150-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="d2150-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="d2150-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2150-102">SYNOPSIS</span></span>
<span data-ttu-id="d2150-103">Cria um objeto de política de certificado na memória.</span><span class="sxs-lookup"><span data-stu-id="d2150-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2150-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2150-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificatePolicy [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-SubjectName <String>] [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] -IssuerName <String>
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2150-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2150-105">DESCRIPTION</span></span>
<span data-ttu-id="d2150-106">O cmdlet **New-AzureKeyVaultCertificatePolicy** cria um objeto de política de certificado na memória para o Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="d2150-106">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="d2150-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2150-107">EXAMPLES</span></span>

### <span data-ttu-id="d2150-108">Exemplo 1: criar uma política de certificado</span><span class="sxs-lookup"><span data-stu-id="d2150-108">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="d2150-109">Esse comando cria uma política de certificado válida por seis meses e reutiliza a chave para renovar o certificado.</span><span class="sxs-lookup"><span data-stu-id="d2150-109">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="d2150-110">OS</span><span class="sxs-lookup"><span data-stu-id="d2150-110">PARAMETERS</span></span>

### <span data-ttu-id="d2150-111">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="d2150-111">-CertificateType</span></span>
<span data-ttu-id="d2150-112">Especifica o tipo de certificado para o emissor.</span><span class="sxs-lookup"><span data-stu-id="d2150-112">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="d2150-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2150-113">-DefaultProfile</span></span>
<span data-ttu-id="d2150-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d2150-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2150-115">-Desabilitado</span><span class="sxs-lookup"><span data-stu-id="d2150-115">-Disabled</span></span>
<span data-ttu-id="d2150-116">Indica que a política de certificado está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="d2150-116">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="d2150-117">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="d2150-117">-DnsNames</span></span>
<span data-ttu-id="d2150-118">Especifica os nomes DNS no certificado.</span><span class="sxs-lookup"><span data-stu-id="d2150-118">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="d2150-119">-Ekus</span><span class="sxs-lookup"><span data-stu-id="d2150-119">-Ekus</span></span>
<span data-ttu-id="d2150-120">Especifica os usos avançados da chave (EKUs) no certificado.</span><span class="sxs-lookup"><span data-stu-id="d2150-120">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="d2150-121">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="d2150-121">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="d2150-122">Especifica o número de dias antes do vencimento do início do processo de notificação automática.</span><span class="sxs-lookup"><span data-stu-id="d2150-122">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="d2150-123">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="d2150-123">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="d2150-124">Especifica a porcentagem do tempo de vida após o qual o processo automático para a notificação é iniciado.</span><span class="sxs-lookup"><span data-stu-id="d2150-124">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="d2150-125">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="d2150-125">-IssuerName</span></span>
<span data-ttu-id="d2150-126">Especifica o nome do emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="d2150-126">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="d2150-127">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="d2150-127">-KeyNotExportable</span></span>
<span data-ttu-id="d2150-128">Indica que a chave não é exportável.</span><span class="sxs-lookup"><span data-stu-id="d2150-128">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="d2150-129">-KeyType</span><span class="sxs-lookup"><span data-stu-id="d2150-129">-KeyType</span></span>
<span data-ttu-id="d2150-130">Especifica o tipo de chave da chave que faz a backup do certificado.</span><span class="sxs-lookup"><span data-stu-id="d2150-130">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="d2150-131">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d2150-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d2150-132">RSA</span><span class="sxs-lookup"><span data-stu-id="d2150-132">RSA</span></span>
- <span data-ttu-id="d2150-133">RSA – HSM</span><span class="sxs-lookup"><span data-stu-id="d2150-133">RSA-HSM</span></span>

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

### <span data-ttu-id="d2150-134">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="d2150-134">-KeyUsage</span></span>
<span data-ttu-id="d2150-135">Especifica os usos da chave no certificado.</span><span class="sxs-lookup"><span data-stu-id="d2150-135">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="d2150-136">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="d2150-136">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="d2150-137">Especifica o número de dias antes da expiração após o início do processo automático para a renovação do certificado.</span><span class="sxs-lookup"><span data-stu-id="d2150-137">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="d2150-138">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="d2150-138">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="d2150-139">Especifica a porcentagem do tempo de vida após o qual o processo automático para a renovação do certificado é iniciado.</span><span class="sxs-lookup"><span data-stu-id="d2150-139">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="d2150-140">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="d2150-140">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="d2150-141">Indica que o certificado reutiliza a chave durante a renovação.</span><span class="sxs-lookup"><span data-stu-id="d2150-141">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="d2150-142">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="d2150-142">-SecretContentType</span></span>
<span data-ttu-id="d2150-143">Especifica o tipo de conteúdo do novo segredo do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="d2150-143">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="d2150-144">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d2150-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d2150-145">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="d2150-145">application/x-pkcs12</span></span>
- <span data-ttu-id="d2150-146">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="d2150-146">application/x-pem-file</span></span>

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

### <span data-ttu-id="d2150-147">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="d2150-147">-SubjectName</span></span>
<span data-ttu-id="d2150-148">Especifica o nome do requerente do certificado.</span><span class="sxs-lookup"><span data-stu-id="d2150-148">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="d2150-149">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="d2150-149">-ValidityInMonths</span></span>
<span data-ttu-id="d2150-150">Especifica o número de meses para o qual o certificado é válido.</span><span class="sxs-lookup"><span data-stu-id="d2150-150">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="d2150-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d2150-151">-Confirm</span></span>
<span data-ttu-id="d2150-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2150-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2150-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2150-153">-WhatIf</span></span>
<span data-ttu-id="d2150-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2150-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2150-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2150-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2150-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2150-156">CommonParameters</span></span>
<span data-ttu-id="d2150-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2150-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2150-158">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2150-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2150-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2150-159">INPUTS</span></span>

## <span data-ttu-id="d2150-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2150-160">OUTPUTS</span></span>

### <span data-ttu-id="d2150-161">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="d2150-161">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="d2150-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2150-162">NOTES</span></span>

## <span data-ttu-id="d2150-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2150-163">RELATED LINKS</span></span>

[<span data-ttu-id="d2150-164">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="d2150-164">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="d2150-165">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="d2150-165">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

