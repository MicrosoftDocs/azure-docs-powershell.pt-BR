---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/import-azurekeyvaultcertificate
schema: 2.0.0
ms.openlocfilehash: 2903aa294830b8f9a39578374c1c108fe91c36e4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786105"
---
# <span data-ttu-id="30001-101">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="30001-101">Import-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="30001-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="30001-102">SYNOPSIS</span></span>
<span data-ttu-id="30001-103">Importa um certificado para um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="30001-103">Imports a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30001-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30001-104">SYNTAX</span></span>

### <span data-ttu-id="30001-105">ImportCertificateFromFile (padrão)</span><span class="sxs-lookup"><span data-stu-id="30001-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30001-106">ImportWithPrivateKeyFromFile</span><span class="sxs-lookup"><span data-stu-id="30001-106">ImportWithPrivateKeyFromFile</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30001-107">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="30001-107">ImportWithPrivateKeyFromString</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30001-108">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="30001-108">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 -CertificateCollection <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30001-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="30001-109">DESCRIPTION</span></span>
<span data-ttu-id="30001-110">O cmdlet **Import-AzureKeyVaultCertificate** importa um certificado para um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="30001-110">The **Import-AzureKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>

<span data-ttu-id="30001-111">Você pode criar o certificado a ser importado usando um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="30001-111">You can create the certificate to import by using one of the following methods:</span></span>

- <span data-ttu-id="30001-112">Use o cmdlet New-AzureKeyVaultCertificateSigningRequest para criar uma solicitação de assinatura de certificado e enviá-la a uma autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="30001-112">Use the New-AzureKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="30001-113">Use um arquivo de pacote de certificado existente, como um arquivo. pfx ou. p12, que contém tanto o certificado quanto a chave privada.</span><span class="sxs-lookup"><span data-stu-id="30001-113">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="30001-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="30001-114">EXAMPLES</span></span>

### <span data-ttu-id="30001-115">Exemplo 1: importar um certificado de cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="30001-115">Example 1: Import a key vault certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password
Name        : importCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        :
Enabled     : True
Created     : 2/8/2016 11:50:43 PM
Updated     : 2/8/2016 11:50:43 PM
```

<span data-ttu-id="30001-116">O primeiro comando usa o cmdlet ConvertTo-SecureString para criar uma senha segura e, em seguida, armazena-a na variável $Password.</span><span class="sxs-lookup"><span data-stu-id="30001-116">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>

<span data-ttu-id="30001-117">O segundo comando importa o certificado chamado ImportCert01 para o cofre da chave CosotosoKV01.</span><span class="sxs-lookup"><span data-stu-id="30001-117">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="30001-118">OS</span><span class="sxs-lookup"><span data-stu-id="30001-118">PARAMETERS</span></span>

### <span data-ttu-id="30001-119">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="30001-119">-CertificateCollection</span></span>
<span data-ttu-id="30001-120">Especifica a coleção de certificados a ser adicionada a um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="30001-120">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30001-121">-Certificatestring</span><span class="sxs-lookup"><span data-stu-id="30001-121">-CertificateString</span></span>
<span data-ttu-id="30001-122">Especifica uma cadeia de caracteres de certificado.</span><span class="sxs-lookup"><span data-stu-id="30001-122">Specifies a certificate string.</span></span>

```yaml
Type: String
Parameter Sets: ImportWithPrivateKeyFromString
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30001-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30001-123">-DefaultProfile</span></span>
<span data-ttu-id="30001-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="30001-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30001-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="30001-125">-FilePath</span></span>
<span data-ttu-id="30001-126">Especifica o caminho do arquivo de certificado que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="30001-126">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30001-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="30001-127">-Name</span></span>
<span data-ttu-id="30001-128">Especifica o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="30001-128">Specifies the certificate name.</span></span> <span data-ttu-id="30001-129">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de um certificado do nome do cofre de chaves, do ambiente selecionado no momento e do nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="30001-129">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

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

### <span data-ttu-id="30001-130">-Senha</span><span class="sxs-lookup"><span data-stu-id="30001-130">-Password</span></span>
<span data-ttu-id="30001-131">Especifica a senha de um arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="30001-131">Specifies the password for a certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: ImportWithPrivateKeyFromFile, ImportWithPrivateKeyFromString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30001-132">-Marca</span><span class="sxs-lookup"><span data-stu-id="30001-132">-Tag</span></span>
<span data-ttu-id="30001-133">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="30001-133">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="30001-134">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="30001-134">For example:</span></span>

<span data-ttu-id="30001-135">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="30001-135">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30001-136">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="30001-136">-VaultName</span></span>
<span data-ttu-id="30001-137">Especifica o nome do cofre de chaves em que esse cmdlet importa certificados.</span><span class="sxs-lookup"><span data-stu-id="30001-137">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="30001-138">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de um cofre de chaves com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="30001-138">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="30001-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="30001-139">-Confirm</span></span>
<span data-ttu-id="30001-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30001-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30001-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30001-141">-WhatIf</span></span>
<span data-ttu-id="30001-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="30001-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30001-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="30001-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30001-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30001-144">CommonParameters</span></span>
<span data-ttu-id="30001-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30001-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30001-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30001-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30001-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="30001-147">INPUTS</span></span>

## <span data-ttu-id="30001-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="30001-148">OUTPUTS</span></span>

### <span data-ttu-id="30001-149">Microsoft. Azure. Commands. keyvault. Models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="30001-149">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="30001-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="30001-150">NOTES</span></span>

## <span data-ttu-id="30001-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="30001-151">RELATED LINKS</span></span>

[<span data-ttu-id="30001-152">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="30001-152">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)
