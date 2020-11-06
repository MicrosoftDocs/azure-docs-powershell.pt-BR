---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 89299823-3382-402D-9458-519466748051
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificate.md
ms.openlocfilehash: 79f8516bbcd33c17e708af1625062e08fb21ebb7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596225"
---
# <span data-ttu-id="67ac8-101">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="67ac8-101">Add-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="67ac8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67ac8-102">SYNOPSIS</span></span>
<span data-ttu-id="67ac8-103">Adiciona um certificado a um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="67ac8-103">Adds a certificate to a key vault.</span></span>

## <span data-ttu-id="67ac8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67ac8-104">SYNTAX</span></span>

```
Add-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificatePolicy] <PSKeyVaultCertificatePolicy> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67ac8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="67ac8-105">DESCRIPTION</span></span>
<span data-ttu-id="67ac8-106">O cmdlet **Add-AzKeyVaultCertificate** inicia o processo de registrar um certificado em um cofre de chaves no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="67ac8-106">The **Add-AzKeyVaultCertificate** cmdlet starts the process of enrolling for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="67ac8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67ac8-107">EXAMPLES</span></span>

### <span data-ttu-id="67ac8-108">Exemplo 1: adicionar um certificado</span><span class="sxs-lookup"><span data-stu-id="67ac8-108">Example 1: Add a certificate</span></span>
```powershell
PS C:\> $Policy = New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
PS C:\> Add-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -CertificatePolicy $Policy

Status                    : inProgress
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : 

PS C:\> Get-AzKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01"
Status                    : completed
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : 

PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"

Name        : testCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        :
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="67ac8-109">O primeiro comando usa o cmdlet New-AzKeyVaultCertificatePolicy para criar uma política de certificado e, em seguida, armazena-o na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="67ac8-109">The first command uses the New-AzKeyVaultCertificatePolicy cmdlet to create a certificate policy, and then stores it in the $Policy variable.</span></span>
<span data-ttu-id="67ac8-110">O segundo comando usa **Add-AzKeyVaultCertificate** para iniciar o processo de criação de um certificado.</span><span class="sxs-lookup"><span data-stu-id="67ac8-110">The second command uses **Add-AzKeyVaultCertificate** to start the process to create a certificate.</span></span>
<span data-ttu-id="67ac8-111">O terceiro comando usa o cmdlet Get-AzKeyVaultCertificateOperation para sondar a operação e verificar se ela está completa.</span><span class="sxs-lookup"><span data-stu-id="67ac8-111">The third command uses the Get-AzKeyVaultCertificateOperation cmdlet to poll the operation to verify that it's complete.</span></span>
<span data-ttu-id="67ac8-112">O comando final usa o cmdlet Get-AzKeyVaultCertificate para obter o certificado.</span><span class="sxs-lookup"><span data-stu-id="67ac8-112">The final command uses the Get-AzKeyVaultCertificate cmdlet to get the certificate.</span></span>

## <span data-ttu-id="67ac8-113">OS</span><span class="sxs-lookup"><span data-stu-id="67ac8-113">PARAMETERS</span></span>

### <span data-ttu-id="67ac8-114">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="67ac8-114">-CertificatePolicy</span></span>
<span data-ttu-id="67ac8-115">Especifica um objeto **KeyVaultCertificatePolicy** .</span><span class="sxs-lookup"><span data-stu-id="67ac8-115">Specifies a **KeyVaultCertificatePolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67ac8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ac8-116">-DefaultProfile</span></span>
<span data-ttu-id="67ac8-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="67ac8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67ac8-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="67ac8-118">-Name</span></span>
<span data-ttu-id="67ac8-119">Especifica o nome do certificado a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="67ac8-119">Specifies the name of the certificate to add.</span></span>

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

### <span data-ttu-id="67ac8-120">-Marca</span><span class="sxs-lookup"><span data-stu-id="67ac8-120">-Tag</span></span>
<span data-ttu-id="67ac8-121">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="67ac8-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="67ac8-122">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="67ac8-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ac8-123">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="67ac8-123">-VaultName</span></span>
<span data-ttu-id="67ac8-124">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="67ac8-124">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="67ac8-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="67ac8-125">-Confirm</span></span>
<span data-ttu-id="67ac8-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67ac8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67ac8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67ac8-127">-WhatIf</span></span>
<span data-ttu-id="67ac8-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="67ac8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67ac8-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="67ac8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67ac8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ac8-130">CommonParameters</span></span>
<span data-ttu-id="67ac8-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67ac8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ac8-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67ac8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ac8-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="67ac8-133">INPUTS</span></span>

### <span data-ttu-id="67ac8-134">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="67ac8-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="67ac8-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="67ac8-135">OUTPUTS</span></span>

### <span data-ttu-id="67ac8-136">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="67ac8-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="67ac8-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="67ac8-137">NOTES</span></span>

## <span data-ttu-id="67ac8-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67ac8-138">RELATED LINKS</span></span>

[<span data-ttu-id="67ac8-139">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="67ac8-139">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="67ac8-140">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="67ac8-140">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="67ac8-141">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="67ac8-141">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)
