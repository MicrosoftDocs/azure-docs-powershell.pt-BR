---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 94f8b6e136925956faf4402b583d80f6a675cca3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440635"
---
# <span data-ttu-id="1c6b5-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1c6b5-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="1c6b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c6b5-102">SYNOPSIS</span></span>
<span data-ttu-id="1c6b5-103">Cria ou atualiza a política de um certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c6b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c6b5-104">SYNTAX</span></span>

### <span data-ttu-id="1c6b5-105">Expandido (padrão)</span><span class="sxs-lookup"><span data-stu-id="1c6b5-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-SecretContentType <String>]
 [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c6b5-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="1c6b5-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c6b5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c6b5-107">DESCRIPTION</span></span>
<span data-ttu-id="1c6b5-108">O cmdlet **set-AzureKeyVaultCertificatePolicy** cria ou atualiza a política de um certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-108">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="1c6b5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c6b5-109">EXAMPLES</span></span>

### <span data-ttu-id="1c6b5-110">Exemplo 1: definir uma política de certificado</span><span class="sxs-lookup"><span data-stu-id="1c6b5-110">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="1c6b5-111">Este comando define a política do certificado TestCert01 no cofre da chave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-111">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="1c6b5-112">OS</span><span class="sxs-lookup"><span data-stu-id="1c6b5-112">PARAMETERS</span></span>

### <span data-ttu-id="1c6b5-113">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1c6b5-113">-CertificatePolicy</span></span>
<span data-ttu-id="1c6b5-114">Especifica a política de certificado.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-114">Specifies the certificate policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c6b5-115">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="1c6b5-115">-CertificateType</span></span>
<span data-ttu-id="1c6b5-116">Especifica o tipo de certificado para o emissor.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-116">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c6b5-117">-Desabilitado</span><span class="sxs-lookup"><span data-stu-id="1c6b5-117">-Disabled</span></span>
<span data-ttu-id="1c6b5-118">Indica que a política de certificado está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-118">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c6b5-119">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="1c6b5-119">-DnsNames</span></span>
<span data-ttu-id="1c6b5-120">Especifica os nomes DNS no certificado.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-120">Specifies the DNS names in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c6b5-121">-Ekus</span><span class="sxs-lookup"><span data-stu-id="1c6b5-121">-Ekus</span></span>
<span data-ttu-id="1c6b5-122">Especifica os usos avançados da chave (EKUs) no certificado.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c6b5-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="1c6b5-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="1c6b5-124">Especifica o número de dias antes do vencimento do início do processo de notificação automática.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="1c6b5-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="1c6b5-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="1c6b5-126">Especifica a porcentagem do tempo de vida após o qual o processo automático para a notificação é iniciado.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="1c6b5-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="1c6b5-127">-IssuerName</span></span>
<span data-ttu-id="1c6b5-128">Especifica o nome do emissor para este certificado.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-128">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c6b5-129">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="1c6b5-129">-KeyNotExportable</span></span>
<span data-ttu-id="1c6b5-130">Indica que a chave não é exportável.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-130">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c6b5-131">-KeyType</span><span class="sxs-lookup"><span data-stu-id="1c6b5-131">-KeyType</span></span>
<span data-ttu-id="1c6b5-132">Especifica o tipo de chave da chave que faz a backup do certificado.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-132">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="1c6b5-133">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1c6b5-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1c6b5-134">RSA</span><span class="sxs-lookup"><span data-stu-id="1c6b5-134">RSA</span></span>
- <span data-ttu-id="1c6b5-135">RSA – HSM</span><span class="sxs-lookup"><span data-stu-id="1c6b5-135">RSA-HSM</span></span>

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

### <span data-ttu-id="1c6b5-136">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="1c6b5-136">-KeyUsage</span></span>
<span data-ttu-id="1c6b5-137">Especifica os usos da chave no certificado.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-137">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c6b5-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c6b5-138">-Name</span></span>
<span data-ttu-id="1c6b5-139">Especifica o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-139">Specifies the name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c6b5-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c6b5-140">-PassThru</span></span>
<span data-ttu-id="1c6b5-141">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1c6b5-142">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1c6b5-143">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="1c6b5-143">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="1c6b5-144">Especifica o número de dias antes da expiração após o início do processo automático para a renovação do certificado.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-144">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c6b5-145">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="1c6b5-145">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="1c6b5-146">Especifica a porcentagem do tempo de vida após o qual o processo automático para a renovação do certificado é iniciado.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-146">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c6b5-147">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="1c6b5-147">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="1c6b5-148">Indica que o certificado reutiliza a chave durante a renovação.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-148">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c6b5-149">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="1c6b5-149">-SecretContentType</span></span>
<span data-ttu-id="1c6b5-150">Especifica o tipo de conteúdo do novo segredo do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-150">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="1c6b5-151">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1c6b5-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1c6b5-152">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="1c6b5-152">application/x-pkcs12</span></span>
- <span data-ttu-id="1c6b5-153">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="1c6b5-153">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c6b5-154">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="1c6b5-154">-SubjectName</span></span>
<span data-ttu-id="1c6b5-155">Especifica o nome do requerente do certificado.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-155">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c6b5-156">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="1c6b5-156">-ValidityInMonths</span></span>
<span data-ttu-id="1c6b5-157">Especifica o número de meses para o qual o certificado é válido.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-157">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c6b5-158">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="1c6b5-158">-VaultName</span></span>
<span data-ttu-id="1c6b5-159">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-159">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c6b5-160">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1c6b5-160">-Confirm</span></span>
<span data-ttu-id="1c6b5-161">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c6b5-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c6b5-162">-WhatIf</span></span>
<span data-ttu-id="1c6b5-163">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c6b5-164">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c6b5-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c6b5-165">-DefaultProfile</span></span>
<span data-ttu-id="1c6b5-166">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c6b5-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c6b5-167">CommonParameters</span></span>
<span data-ttu-id="1c6b5-168">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c6b5-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c6b5-169">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c6b5-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c6b5-170">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c6b5-170">INPUTS</span></span>

## <span data-ttu-id="1c6b5-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c6b5-171">OUTPUTS</span></span>

### <span data-ttu-id="1c6b5-172">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1c6b5-172">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="1c6b5-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c6b5-173">NOTES</span></span>

## <span data-ttu-id="1c6b5-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c6b5-174">RELATED LINKS</span></span>

[<span data-ttu-id="1c6b5-175">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1c6b5-175">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="1c6b5-176">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1c6b5-176">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)
