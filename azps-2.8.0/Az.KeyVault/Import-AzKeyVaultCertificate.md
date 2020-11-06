---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
ms.openlocfilehash: 6591b96257a1c94cd2da9d0bc6f2995dc2034a40
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596187"
---
# <span data-ttu-id="9d06e-101">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="9d06e-101">Import-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="9d06e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d06e-102">SYNOPSIS</span></span>
<span data-ttu-id="9d06e-103">Importa um certificado para um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="9d06e-103">Imports a certificate to a key vault.</span></span>

## <span data-ttu-id="9d06e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d06e-104">SYNTAX</span></span>

### <span data-ttu-id="9d06e-105">ImportCertificateFromFile (padrão)</span><span class="sxs-lookup"><span data-stu-id="9d06e-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d06e-106">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="9d06e-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d06e-107">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="9d06e-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d06e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9d06e-108">DESCRIPTION</span></span>
<span data-ttu-id="9d06e-109">O cmdlet **Import-AzKeyVaultCertificate** importa um certificado para um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="9d06e-109">The **Import-AzKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>
<span data-ttu-id="9d06e-110">Você pode criar o certificado a ser importado usando um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="9d06e-110">You can create the certificate to import by using one of the following methods:</span></span>
- <span data-ttu-id="9d06e-111">Use o cmdlet New-AzKeyVaultCertificateSigningRequest para criar uma solicitação de assinatura de certificado e enviá-la a uma autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="9d06e-111">Use the New-AzKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="9d06e-112">Use um arquivo de pacote de certificado existente, como um arquivo. pfx ou. p12, que contém tanto o certificado quanto a chave privada.</span><span class="sxs-lookup"><span data-stu-id="9d06e-112">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="9d06e-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d06e-113">EXAMPLES</span></span>

### <span data-ttu-id="9d06e-114">Exemplo 1: importar um certificado de cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="9d06e-114">Example 1: Import a key vault certificate</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password

Name        : importCert01
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
Created     : 2/8/2016 11:50:43 PM
Updated     : 2/8/2016 11:50:43 PM
```

<span data-ttu-id="9d06e-115">O primeiro comando usa o cmdlet ConvertTo-SecureString para criar uma senha segura e, em seguida, armazena-a na variável $Password.</span><span class="sxs-lookup"><span data-stu-id="9d06e-115">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>
<span data-ttu-id="9d06e-116">O segundo comando importa o certificado chamado ImportCert01 para o cofre da chave CosotosoKV01.</span><span class="sxs-lookup"><span data-stu-id="9d06e-116">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="9d06e-117">OS</span><span class="sxs-lookup"><span data-stu-id="9d06e-117">PARAMETERS</span></span>

### <span data-ttu-id="9d06e-118">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="9d06e-118">-CertificateCollection</span></span>
<span data-ttu-id="9d06e-119">Especifica a coleção de certificados a ser adicionada a um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="9d06e-119">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: System.Security.Cryptography.X509Certificates.X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d06e-120">-Certificatestring</span><span class="sxs-lookup"><span data-stu-id="9d06e-120">-CertificateString</span></span>
<span data-ttu-id="9d06e-121">Especifica uma cadeia de caracteres de certificado.</span><span class="sxs-lookup"><span data-stu-id="9d06e-121">Specifies a certificate string.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportWithPrivateKeyFromString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d06e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d06e-122">-DefaultProfile</span></span>
<span data-ttu-id="9d06e-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9d06e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d06e-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="9d06e-124">-FilePath</span></span>
<span data-ttu-id="9d06e-125">Especifica o caminho do arquivo de certificado que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="9d06e-125">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d06e-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d06e-126">-Name</span></span>
<span data-ttu-id="9d06e-127">Especifica o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="9d06e-127">Specifies the certificate name.</span></span> <span data-ttu-id="9d06e-128">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de um certificado do nome do cofre de chaves, do ambiente selecionado no momento e do nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="9d06e-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d06e-129">-Senha</span><span class="sxs-lookup"><span data-stu-id="9d06e-129">-Password</span></span>
<span data-ttu-id="9d06e-130">Especifica a senha de um arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="9d06e-130">Specifies the password for a certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d06e-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="9d06e-131">-Tag</span></span>
<span data-ttu-id="9d06e-132">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9d06e-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9d06e-133">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="9d06e-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d06e-134">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="9d06e-134">-VaultName</span></span>
<span data-ttu-id="9d06e-135">Especifica o nome do cofre de chaves em que esse cmdlet importa certificados.</span><span class="sxs-lookup"><span data-stu-id="9d06e-135">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="9d06e-136">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de um cofre de chaves com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="9d06e-136">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d06e-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9d06e-137">-Confirm</span></span>
<span data-ttu-id="9d06e-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d06e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d06e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d06e-139">-WhatIf</span></span>
<span data-ttu-id="9d06e-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9d06e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d06e-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9d06e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d06e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d06e-142">CommonParameters</span></span>
<span data-ttu-id="9d06e-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d06e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d06e-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d06e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d06e-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9d06e-145">INPUTS</span></span>

### <span data-ttu-id="9d06e-146">System. String</span><span class="sxs-lookup"><span data-stu-id="9d06e-146">System.String</span></span>

### <span data-ttu-id="9d06e-147">System. Security. Cryptography. X509Certificates. X509Certificate2Collection</span><span class="sxs-lookup"><span data-stu-id="9d06e-147">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span></span>

### <span data-ttu-id="9d06e-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9d06e-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9d06e-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9d06e-149">OUTPUTS</span></span>

### <span data-ttu-id="9d06e-150">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="9d06e-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="9d06e-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9d06e-151">NOTES</span></span>

## <span data-ttu-id="9d06e-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d06e-152">RELATED LINKS</span></span>

[<span data-ttu-id="9d06e-153">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="9d06e-153">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)
