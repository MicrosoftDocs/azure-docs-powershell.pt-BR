---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 160c98b141dbde36786404b58c694772dc86d323
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776653"
---
# <span data-ttu-id="fb9ae-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fb9ae-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="fb9ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb9ae-102">SYNOPSIS</span></span>
<span data-ttu-id="fb9ae-103">Cria ou atualiza a política de um certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="fb9ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb9ae-104">SYNTAX</span></span>

### <span data-ttu-id="fb9ae-105">Expandido (padrão)</span><span class="sxs-lookup"><span data-stu-id="fb9ae-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-SecretContentType <String>]
 [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb9ae-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="fb9ae-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb9ae-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb9ae-107">DESCRIPTION</span></span>
<span data-ttu-id="fb9ae-108">O cmdlet **set-AzKeyVaultCertificatePolicy** cria ou atualiza a política de um certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-108">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="fb9ae-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb9ae-109">EXAMPLES</span></span>

### <span data-ttu-id="fb9ae-110">Exemplo 1: definir uma política de certificado</span><span class="sxs-lookup"><span data-stu-id="fb9ae-110">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="fb9ae-111">Este comando define a política do certificado TestCert01 no cofre da chave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-111">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="fb9ae-112">OS</span><span class="sxs-lookup"><span data-stu-id="fb9ae-112">PARAMETERS</span></span>

### <span data-ttu-id="fb9ae-113">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fb9ae-113">-CertificatePolicy</span></span>
<span data-ttu-id="fb9ae-114">Especifica a política de certificado.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-114">Specifies the certificate policy.</span></span>

```yaml
Type: KeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ae-115">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="fb9ae-115">-CertificateType</span></span>
<span data-ttu-id="fb9ae-116">Especifica o tipo de certificado para o emissor.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-116">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb9ae-117">-DefaultProfile</span></span>
<span data-ttu-id="fb9ae-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fb9ae-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb9ae-119">-Desabilitado</span><span class="sxs-lookup"><span data-stu-id="fb9ae-119">-Disabled</span></span>
<span data-ttu-id="fb9ae-120">Indica que a política de certificado está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-120">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ae-121">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="fb9ae-121">-DnsNames</span></span>
<span data-ttu-id="fb9ae-122">Especifica os nomes DNS no certificado.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-122">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="fb9ae-123">-Ekus</span><span class="sxs-lookup"><span data-stu-id="fb9ae-123">-Ekus</span></span>
<span data-ttu-id="fb9ae-124">Especifica os usos avançados da chave (EKUs) no certificado.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-124">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="fb9ae-125">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="fb9ae-125">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="fb9ae-126">Especifica o número de dias antes do vencimento do início do processo de notificação automática.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-126">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="fb9ae-127">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="fb9ae-127">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="fb9ae-128">Especifica a porcentagem do tempo de vida após o qual o processo automático para a notificação é iniciado.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-128">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="fb9ae-129">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="fb9ae-129">-IssuerName</span></span>
<span data-ttu-id="fb9ae-130">Especifica o nome do emissor para este certificado.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-130">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ae-131">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="fb9ae-131">-KeyNotExportable</span></span>
<span data-ttu-id="fb9ae-132">Indica que a chave não é exportável.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-132">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ae-133">-KeyType</span><span class="sxs-lookup"><span data-stu-id="fb9ae-133">-KeyType</span></span>
<span data-ttu-id="fb9ae-134">Especifica o tipo de chave da chave que faz a backup do certificado.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-134">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="fb9ae-135">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="fb9ae-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fb9ae-136">RSA</span><span class="sxs-lookup"><span data-stu-id="fb9ae-136">RSA</span></span>
- <span data-ttu-id="fb9ae-137">RSA – HSM</span><span class="sxs-lookup"><span data-stu-id="fb9ae-137">RSA-HSM</span></span>

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

### <span data-ttu-id="fb9ae-138">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="fb9ae-138">-KeyUsage</span></span>
<span data-ttu-id="fb9ae-139">Especifica os usos da chave no certificado.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-139">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="fb9ae-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb9ae-140">-Name</span></span>
<span data-ttu-id="fb9ae-141">Especifica o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-141">Specifies the name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ae-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb9ae-142">-PassThru</span></span>
<span data-ttu-id="fb9ae-143">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-143">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fb9ae-144">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-144">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ae-145">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="fb9ae-145">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="fb9ae-146">Especifica o número de dias antes da expiração após o início do processo automático para a renovação do certificado.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-146">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ae-147">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="fb9ae-147">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="fb9ae-148">Especifica a porcentagem do tempo de vida após o qual o processo automático para a renovação do certificado é iniciado.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-148">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ae-149">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="fb9ae-149">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="fb9ae-150">Indica que o certificado reutiliza a chave durante a renovação.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-150">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: Boolean
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ae-151">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="fb9ae-151">-SecretContentType</span></span>
<span data-ttu-id="fb9ae-152">Especifica o tipo de conteúdo do novo segredo do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-152">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="fb9ae-153">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="fb9ae-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fb9ae-154">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="fb9ae-154">application/x-pkcs12</span></span>
- <span data-ttu-id="fb9ae-155">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="fb9ae-155">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ae-156">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="fb9ae-156">-SubjectName</span></span>
<span data-ttu-id="fb9ae-157">Especifica o nome do requerente do certificado.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-157">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ae-158">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="fb9ae-158">-ValidityInMonths</span></span>
<span data-ttu-id="fb9ae-159">Especifica o número de meses para o qual o certificado é válido.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-159">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ae-160">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="fb9ae-160">-VaultName</span></span>
<span data-ttu-id="fb9ae-161">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-161">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="fb9ae-162">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fb9ae-162">-Confirm</span></span>
<span data-ttu-id="fb9ae-163">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb9ae-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb9ae-164">-WhatIf</span></span>
<span data-ttu-id="fb9ae-165">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb9ae-166">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb9ae-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb9ae-167">CommonParameters</span></span>
<span data-ttu-id="fb9ae-168">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb9ae-169">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb9ae-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb9ae-170">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb9ae-170">INPUTS</span></span>

### <span data-ttu-id="fb9ae-171">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fb9ae-171">None</span></span>
<span data-ttu-id="fb9ae-172">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="fb9ae-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fb9ae-173">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb9ae-173">OUTPUTS</span></span>

### <span data-ttu-id="fb9ae-174">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fb9ae-174">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="fb9ae-175">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb9ae-175">NOTES</span></span>

## <span data-ttu-id="fb9ae-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb9ae-176">RELATED LINKS</span></span>

[<span data-ttu-id="fb9ae-177">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fb9ae-177">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="fb9ae-178">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fb9ae-178">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

