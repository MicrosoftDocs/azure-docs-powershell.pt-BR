---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: e960aa211b53c79087e67e2bd86504e597a718d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440855"
---
# <span data-ttu-id="8c6d3-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="8c6d3-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="8c6d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c6d3-102">SYNOPSIS</span></span>
<span data-ttu-id="8c6d3-103">Cria ou atualiza a política de um certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c6d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c6d3-104">SYNTAX</span></span>

### <span data-ttu-id="8c6d3-105">ExpandedRenewPercentage (padrão)</span><span class="sxs-lookup"><span data-stu-id="8c6d3-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c6d3-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="8c6d3-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c6d3-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="8c6d3-107">ExpandedRenewNumber</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 -RenewAtNumberOfDaysBeforeExpiry <Int32> [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>]
 [-Disabled] [-SubjectName <String>] [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c6d3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c6d3-108">DESCRIPTION</span></span>
<span data-ttu-id="8c6d3-109">O cmdlet **set-AzureKeyVaultCertificatePolicy** cria ou atualiza a política de um certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-109">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="8c6d3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c6d3-110">EXAMPLES</span></span>

### <span data-ttu-id="8c6d3-111">Exemplo 1: definir uma política de certificado</span><span class="sxs-lookup"><span data-stu-id="8c6d3-111">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="8c6d3-112">Este comando define a política do certificado TestCert01 no cofre da chave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="8c6d3-113">OS</span><span class="sxs-lookup"><span data-stu-id="8c6d3-113">PARAMETERS</span></span>

### <span data-ttu-id="8c6d3-114">-Certificatetype</span><span class="sxs-lookup"><span data-stu-id="8c6d3-114">-CertificateType</span></span>
<span data-ttu-id="8c6d3-115">Especifica o tipo de certificado para o emissor.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-115">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c6d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c6d3-116">-DefaultProfile</span></span>
<span data-ttu-id="8c6d3-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8c6d3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c6d3-118">-Desabilitado</span><span class="sxs-lookup"><span data-stu-id="8c6d3-118">-Disabled</span></span>
<span data-ttu-id="8c6d3-119">Indica que a política de certificado está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-119">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c6d3-120">-DnsName</span><span class="sxs-lookup"><span data-stu-id="8c6d3-120">-DnsName</span></span>
<span data-ttu-id="8c6d3-121">Especifica o nome do requerente do certificado.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-121">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases: DnsNames

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c6d3-122">-Ekus</span><span class="sxs-lookup"><span data-stu-id="8c6d3-122">-Ekus</span></span>
<span data-ttu-id="8c6d3-123">Especifica os usos avançados da chave (EKUs) no certificado.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-123">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c6d3-124">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="8c6d3-124">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="8c6d3-125">Especifica o número de dias antes do vencimento quando a renovação automática deve começar.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-125">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="8c6d3-126">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="8c6d3-126">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="8c6d3-127">Especifica a porcentagem do tempo de vida após o qual o processo automático para a notificação é iniciado.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-127">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="8c6d3-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c6d3-128">-InputObject</span></span>
<span data-ttu-id="8c6d3-129">Especifica a política de certificado.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-129">Specifies the certificate policy.</span></span>

```yaml
Type: PSKeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: CertificatePolicy

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c6d3-130">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="8c6d3-130">-IssuerName</span></span>
<span data-ttu-id="8c6d3-131">Especifica o nome do emissor para este certificado.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-131">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c6d3-132">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="8c6d3-132">-KeyNotExportable</span></span>
<span data-ttu-id="8c6d3-133">Indica que a chave não é exportável.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-133">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c6d3-134">-KeyType</span><span class="sxs-lookup"><span data-stu-id="8c6d3-134">-KeyType</span></span>
<span data-ttu-id="8c6d3-135">Especifica o tipo de chave da chave que faz a backup do certificado.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-135">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="8c6d3-136">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8c6d3-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8c6d3-137">RSA</span><span class="sxs-lookup"><span data-stu-id="8c6d3-137">RSA</span></span>
- <span data-ttu-id="8c6d3-138">RSA – HSM</span><span class="sxs-lookup"><span data-stu-id="8c6d3-138">RSA-HSM</span></span>

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

### <span data-ttu-id="8c6d3-139">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="8c6d3-139">-KeyUsage</span></span>
<span data-ttu-id="8c6d3-140">Especifica os usos da chave no certificado.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-140">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c6d3-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c6d3-141">-Name</span></span>
<span data-ttu-id="8c6d3-142">Especifica o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-142">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="8c6d3-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c6d3-143">-PassThru</span></span>
<span data-ttu-id="8c6d3-144">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8c6d3-145">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-145">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8c6d3-146">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="8c6d3-146">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="8c6d3-147">Especifica o número de dias antes da expiração após o início do processo automático para a renovação do certificado.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-147">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewNumber
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c6d3-148">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="8c6d3-148">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="8c6d3-149">Especifica a porcentagem do tempo de vida após o qual o processo automático para a renovação do certificado é iniciado.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-149">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewPercentage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c6d3-150">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="8c6d3-150">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="8c6d3-151">Indica que o certificado reutiliza a chave durante a renovação.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-151">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: Boolean
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c6d3-152">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="8c6d3-152">-SecretContentType</span></span>
<span data-ttu-id="8c6d3-153">Especifica o tipo de conteúdo do novo segredo do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-153">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="8c6d3-154">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8c6d3-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8c6d3-155">application/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="8c6d3-155">application/x-pkcs12</span></span>
- <span data-ttu-id="8c6d3-156">application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="8c6d3-156">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c6d3-157">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="8c6d3-157">-SubjectName</span></span>
<span data-ttu-id="8c6d3-158">Especifica o nome do requerente do certificado.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-158">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c6d3-159">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="8c6d3-159">-ValidityInMonths</span></span>
<span data-ttu-id="8c6d3-160">Especifica o número de meses para o qual o certificado é válido.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-160">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c6d3-161">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="8c6d3-161">-VaultName</span></span>
<span data-ttu-id="8c6d3-162">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-162">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="8c6d3-163">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8c6d3-163">-Confirm</span></span>
<span data-ttu-id="8c6d3-164">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c6d3-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c6d3-165">-WhatIf</span></span>
<span data-ttu-id="8c6d3-166">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c6d3-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c6d3-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c6d3-168">CommonParameters</span></span>
<span data-ttu-id="8c6d3-169">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c6d3-170">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c6d3-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c6d3-171">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c6d3-171">INPUTS</span></span>

### <span data-ttu-id="8c6d3-172">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8c6d3-172">None</span></span>
<span data-ttu-id="8c6d3-173">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="8c6d3-173">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8c6d3-174">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c6d3-174">OUTPUTS</span></span>

### <span data-ttu-id="8c6d3-175">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="8c6d3-175">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="8c6d3-176">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c6d3-176">NOTES</span></span>

## <span data-ttu-id="8c6d3-177">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c6d3-177">RELATED LINKS</span></span>

[<span data-ttu-id="8c6d3-178">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="8c6d3-178">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="8c6d3-179">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="8c6d3-179">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

