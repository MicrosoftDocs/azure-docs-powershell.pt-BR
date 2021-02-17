---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: 92409b30e7a81f5d41a0af8ebb6466eb1e3053c9
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405152"
---
# <span data-ttu-id="5a964-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="5a964-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="5a964-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5a964-102">SYNOPSIS</span></span>
<span data-ttu-id="5a964-103">Obtém um certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5a964-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="5a964-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a964-104">SYNTAX</span></span>

### <span data-ttu-id="5a964-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="5a964-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a964-106">ByCertificateNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="5a964-106">ByCertificateNameAndVersion</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a964-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="5a964-107">ByCertificateAllVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a964-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="5a964-108">ByNameInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a964-109">ByCertificateNameAndVersionInputObject</span><span class="sxs-lookup"><span data-stu-id="5a964-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a964-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="5a964-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a964-111">ByNameResourceId</span><span class="sxs-lookup"><span data-stu-id="5a964-111">ByNameResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a964-112">ByCertificateNameAndVersionResourceId</span><span class="sxs-lookup"><span data-stu-id="5a964-112">ByCertificateNameAndVersionResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a964-113">ByCertificateAllVersionsResourceId</span><span class="sxs-lookup"><span data-stu-id="5a964-113">ByCertificateAllVersionsResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a964-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a964-114">DESCRIPTION</span></span>
<span data-ttu-id="5a964-115">O cmdlet **Get-AzKeyVaultCertificate** obtém o certificado especificado ou as versões de um certificado de um cofre de chave no Cofre de Teclas do Azure.</span><span class="sxs-lookup"><span data-stu-id="5a964-115">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="5a964-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5a964-116">EXAMPLES</span></span>

### <span data-ttu-id="5a964-117">Exemplo 1: Obter um certificado</span><span class="sxs-lookup"><span data-stu-id="5a964-117">Example 1: Get a certificate</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject] 
                CN=contoso.com

              [Issuer] 
                CN=contoso.com

              [Serial Number] 
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before] 
                2/8/2016 3:11:45 PM

              [Not After] 
                8/8/2016 4:21:45 PM

              [Thumbprint] 
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId       : https://contoso.vault.azure.net:443/keys/TestCert01/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
SecretId    : https://contoso.vault.azure.net:443/secrets/TestCert01/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

### <span data-ttu-id="5a964-118">Exemplo 2: Obter certificado e salvá-lo como pfx</span><span class="sxs-lookup"><span data-stu-id="5a964-118">Example 2: Get cert and save it as pfx</span></span>
<span data-ttu-id="5a964-119">Esse comando obtém o certificado testCert01 do cofre de chave chamado ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="5a964-119">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span> <span data-ttu-id="5a964-120">Para baixar o certificado como arquivo pfx, execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="5a964-120">To download the certificate as pfx file, run following command.</span></span> <span data-ttu-id="5a964-121">Esses comandos acessam o SecretId e, em seguida, salvam o conteúdo como um arquivo pfx.</span><span class="sxs-lookup"><span data-stu-id="5a964-121">These commands access SecretId and then save the content as a pfx file.</span></span>

```powershell
$cert = Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
$secret = Get-AzKeyVaultSecret -VaultName $vaultName -Name $cert.Name -AsPlainText
$secretByte = [Convert]::FromBase64String($secret)
$x509Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($secretByte, "", "Exportable,PersistKeySet")
$type = [System.Security.Cryptography.X509Certificates.X509ContentType]::Pfx
$pfxFileByte = $x509Cert.Export($type, $password)

# Write to a file
[System.IO.File]::WriteAllBytes("KeyVault.pfx", $pfxFileByte)
```

### <span data-ttu-id="5a964-122">Exemplo 3: Obter todos os certificados que foram excluídos, mas não limpos para esse cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="5a964-122">Example 3: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName 'contoso' -InRemovedState

DeletedDate        : 5/24/2018 6:08:32 PM
Enabled            : True
Expires            : 11/24/2018 6:08:13 PM
NotBefore          : 5/24/2018 5:58:13 PM
Created            : 5/24/2018 6:08:13 PM
Updated            : 5/24/2018 6:08:13 PM
Tags               :
VaultName          : contoso
Name               : test1
Version            :
Id                 : https://contoso.vault.azure.net:443/certificates/test1

ScheduledPurgeDate : 8/22/2018 6:10:47 PM
DeletedDate        : 5/24/2018 6:10:47 PM
Enabled            : True
Expires            : 11/24/2018 6:09:44 PM
NotBefore          : 5/24/2018 5:59:44 PM
Created            : 5/24/2018 6:09:44 PM
Updated            : 5/24/2018 6:09:44 PM
Tags               :
VaultName          : contoso
Name               : test2
Version            :
Id                 : https://contoso.vault.azure.net:443/certificates/test2
```

<span data-ttu-id="5a964-123">Esse comando obtém todos os certificados que foram excluídos anteriormente, mas não limpos, no cofre de chave chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="5a964-123">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="5a964-124">Exemplo 4: Obtém o certificado MyCert que foi excluído, mas não limpo para este cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="5a964-124">Example 4: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName 'contoso' -Name 'test1' -InRemovedState

Certificate        : [Subject]
                       CN=contoso.com

                     [Issuer]
                       CN=contoso.com

                     [Serial Number]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                     [Not Before]
                       5/24/2018 10:58:13 AM

                     [Not After]
                       11/24/2018 10:08:13 AM

                     [Thumbprint]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId              : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
SecretId           : https://contoso.vault.azure.net:443/secrets/test1/7fe415d5518240c1a6fce89986b8d334
Thumbprint         : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel      : Recoverable+Purgeable
ScheduledPurgeDate : 8/22/2018 6:08:32 PM
DeletedDate        : 5/24/2018 6:08:32 PM
Enabled            : True
Expires            : 11/24/2018 6:08:13 PM
NotBefore          : 5/24/2018 5:58:13 PM
Created            : 5/24/2018 6:08:13 PM
Updated            : 5/24/2018 6:08:13 PM
Tags               :
VaultName          : contoso
Name               : test1
Version            : 7fe415d5518240c1a6fce89986b8d334
Id                 : https://contoso.vault.azure.net:443/certificates/test1/7fe415d5518240c1a6fce89986b8d334
```

<span data-ttu-id="5a964-125">Esse comando obtém o certificado chamado 'MyCert' que foi excluído anteriormente, mas não limpo, no cofre de chave chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="5a964-125">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="5a964-126">Esse comando retornará metadados, como a data de exclusão e a data de purgação agendada deste certificado excluído.</span><span class="sxs-lookup"><span data-stu-id="5a964-126">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

### <span data-ttu-id="5a964-127">Exemplo 5: Certificados de lista usando filtragem</span><span class="sxs-lookup"><span data-stu-id="5a964-127">Example 5: List certificates using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "test*"

Enabled   : True
Expires   : 8/5/2019 2:39:25 AM
NotBefore : 2/5/2019 2:29:25 AM
Created   : 2/5/2019 2:39:25 AM
Updated   : 2/5/2019 2:39:25 AM
Tags      :
VaultName : ContosoKV01
Name      : test1
Version   :
Id        : https://ContosoKV01.vault.azure.net:443/certificates/test1

Enabled   : True
Expires   : 8/5/2019 2:39:25 AM
NotBefore : 2/5/2019 2:29:25 AM
Created   : 2/5/2019 2:39:25 AM
Updated   : 2/5/2019 2:39:25 AM
Tags      :
VaultName : ContosoKV01
Name      : test2
Version   :
Id        : https://ContosoKV01.vault.azure.net:443/certificates/test2

This command gets all certificates starting with "test" from the key vault named ContosoKV01.
```

## <span data-ttu-id="5a964-128">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a964-128">PARAMETERS</span></span>

### <span data-ttu-id="5a964-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a964-129">-DefaultProfile</span></span>
<span data-ttu-id="5a964-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5a964-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a964-131">-IncludePending</span><span class="sxs-lookup"><span data-stu-id="5a964-131">-IncludePending</span></span>
<span data-ttu-id="5a964-132">Especifica se você deve incluir certificados pendentes na saída</span><span class="sxs-lookup"><span data-stu-id="5a964-132">Specifies whether to include pending certificates in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a964-133">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="5a964-133">-IncludeVersions</span></span>
<span data-ttu-id="5a964-134">Indica que essa operação obtém todas as versões do certificado.</span><span class="sxs-lookup"><span data-stu-id="5a964-134">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByCertificateAllVersions, ByCertificateAllVersionsInputObject, ByCertificateAllVersionsResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a964-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a964-135">-InputObject</span></span>
<span data-ttu-id="5a964-136">Objeto KeyVault.</span><span class="sxs-lookup"><span data-stu-id="5a964-136">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByNameInputObject, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a964-137">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="5a964-137">-InRemovedState</span></span>
<span data-ttu-id="5a964-138">Especifica se você deve incluir certificados excluídos anteriormente na saída</span><span class="sxs-lookup"><span data-stu-id="5a964-138">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a964-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a964-139">-Name</span></span>
<span data-ttu-id="5a964-140">Especifica o nome do certificado a ser obter.</span><span class="sxs-lookup"><span data-stu-id="5a964-140">Specifies the name of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="5a964-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a964-141">-ResourceId</span></span>
<span data-ttu-id="5a964-142">ID do Recurso KeyVault.</span><span class="sxs-lookup"><span data-stu-id="5a964-142">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameResourceId, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a964-143">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="5a964-143">-VaultName</span></span>
<span data-ttu-id="5a964-144">Especifica o nome de um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="5a964-144">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByCertificateNameAndVersion, ByCertificateAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a964-145">-Versão</span><span class="sxs-lookup"><span data-stu-id="5a964-145">-Version</span></span>
<span data-ttu-id="5a964-146">Especifica a versão de um certificado.</span><span class="sxs-lookup"><span data-stu-id="5a964-146">Specifies the version of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateNameAndVersionInputObject, ByCertificateNameAndVersionResourceId
Aliases: CertificateVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a964-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a964-147">CommonParameters</span></span>
<span data-ttu-id="5a964-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a964-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a964-149">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a964-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a964-150">Entradas</span><span class="sxs-lookup"><span data-stu-id="5a964-150">INPUTS</span></span>

### <span data-ttu-id="5a964-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="5a964-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="5a964-152">System.String</span><span class="sxs-lookup"><span data-stu-id="5a964-152">System.String</span></span>

## <span data-ttu-id="5a964-153">Saídas</span><span class="sxs-lookup"><span data-stu-id="5a964-153">OUTPUTS</span></span>

### <span data-ttu-id="5a964-154">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="5a964-154">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

### <span data-ttu-id="5a964-155">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="5a964-155">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

### <span data-ttu-id="5a964-156">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="5a964-156">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

### <span data-ttu-id="5a964-157">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="5a964-157">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="5a964-158">Notas</span><span class="sxs-lookup"><span data-stu-id="5a964-158">NOTES</span></span>

## <span data-ttu-id="5a964-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a964-159">RELATED LINKS</span></span>

[<span data-ttu-id="5a964-160">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="5a964-160">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="5a964-161">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="5a964-161">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="5a964-162">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="5a964-162">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

