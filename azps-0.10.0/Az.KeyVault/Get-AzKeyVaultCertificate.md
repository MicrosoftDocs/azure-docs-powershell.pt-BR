---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: babd3d8a42ddbd740c8189a41de76c78170ecae5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398811"
---
# <span data-ttu-id="7b9d0-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7b9d0-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="7b9d0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b9d0-102">SYNOPSIS</span></span>
<span data-ttu-id="7b9d0-103">Obtém um certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="7b9d0-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="7b9d0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b9d0-104">SYNTAX</span></span>

### <span data-ttu-id="7b9d0-105">ByVaultName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7b9d0-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b9d0-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="7b9d0-106">ByCertificateName</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b9d0-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="7b9d0-107">ByCertificateVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b9d0-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="7b9d0-108">ByDeletedCertificates</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b9d0-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="7b9d0-109">DESCRIPTION</span></span>
<span data-ttu-id="7b9d0-110">O cmdlet **Get-AzKeyVaultCertificate** obtém o certificado especificado ou as versões de um certificado de um cofre de chave no Cofre de Teclas do Azure.</span><span class="sxs-lookup"><span data-stu-id="7b9d0-110">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="7b9d0-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7b9d0-111">EXAMPLES</span></span>

### <span data-ttu-id="7b9d0-112">Exemplo 1: Obter um certificado</span><span class="sxs-lookup"><span data-stu-id="7b9d0-112">Example 1: Get a certificate</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
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
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="7b9d0-113">Esse comando obtém o certificado testCert01 do cofre de chave chamado ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="7b9d0-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="7b9d0-114">Exemplo 2: Obter todos os certificados que foram excluídos, mas não limpos para esse cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="7b9d0-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="7b9d0-115">Esse comando obtém todos os certificados que foram excluídos anteriormente, mas não limpos, no cofre de chave chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="7b9d0-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="7b9d0-116">Exemplo 3: Obtém o certificado MyCert que foi excluído, mas não limpo para este cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="7b9d0-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="7b9d0-117">Esse comando obtém o certificado chamado "MeuCert" que foi excluído anteriormente, mas não limpo, no cofre de chave chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="7b9d0-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="7b9d0-118">Esse comando retornará metadados, como a data de exclusão e a data de purgação agendada deste certificado excluído.</span><span class="sxs-lookup"><span data-stu-id="7b9d0-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="7b9d0-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b9d0-119">PARAMETERS</span></span>

### <span data-ttu-id="7b9d0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b9d0-120">-DefaultProfile</span></span>
<span data-ttu-id="7b9d0-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7b9d0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b9d0-122">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="7b9d0-122">-IncludeVersions</span></span>
<span data-ttu-id="7b9d0-123">Indica que essa operação obtém todas as versões do certificado.</span><span class="sxs-lookup"><span data-stu-id="7b9d0-123">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByCertificateVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b9d0-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="7b9d0-124">-InRemovedState</span></span>
<span data-ttu-id="7b9d0-125">Especifica se você deve incluir certificados excluídos anteriormente na saída</span><span class="sxs-lookup"><span data-stu-id="7b9d0-125">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedCertificates
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b9d0-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b9d0-126">-Name</span></span>
<span data-ttu-id="7b9d0-127">Especifica o nome do certificado a ser obter.</span><span class="sxs-lookup"><span data-stu-id="7b9d0-127">Specifies the name of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName, ByCertificateVersions
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedCertificates
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b9d0-128">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="7b9d0-128">-VaultName</span></span>
<span data-ttu-id="7b9d0-129">Especifica o nome de um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="7b9d0-129">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="7b9d0-130">-Versão</span><span class="sxs-lookup"><span data-stu-id="7b9d0-130">-Version</span></span>
<span data-ttu-id="7b9d0-131">Especifica a versão de um certificado.</span><span class="sxs-lookup"><span data-stu-id="7b9d0-131">Specifies the version of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b9d0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b9d0-132">CommonParameters</span></span>
<span data-ttu-id="7b9d0-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b9d0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b9d0-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b9d0-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b9d0-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="7b9d0-135">INPUTS</span></span>

### <span data-ttu-id="7b9d0-136">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7b9d0-136">None</span></span>
<span data-ttu-id="7b9d0-137">Este cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="7b9d0-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7b9d0-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="7b9d0-138">OUTPUTS</span></span>

### <span data-ttu-id="7b9d0-139">System.Collections.Generic.List'1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="7b9d0-139">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="7b9d0-140">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7b9d0-140">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="7b9d0-141">Notas</span><span class="sxs-lookup"><span data-stu-id="7b9d0-141">NOTES</span></span>

## <span data-ttu-id="7b9d0-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b9d0-142">RELATED LINKS</span></span>

[<span data-ttu-id="7b9d0-143">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7b9d0-143">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="7b9d0-144">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7b9d0-144">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="7b9d0-145">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7b9d0-145">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

