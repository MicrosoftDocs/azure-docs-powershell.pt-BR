---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
ms.openlocfilehash: dd87a5b9abf6126fee71bbc308ec3a985c9da9de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611110"
---
# <span data-ttu-id="ab1f0-101">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ab1f0-101">Get-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="ab1f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab1f0-102">SYNOPSIS</span></span>
<span data-ttu-id="ab1f0-103">Obtém um certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-103">Gets a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab1f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab1f0-104">SYNTAX</span></span>

### <span data-ttu-id="ab1f0-105">ByVaultName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ab1f0-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab1f0-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="ab1f0-106">ByCertificateName</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab1f0-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="ab1f0-107">ByCertificateVersions</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab1f0-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="ab1f0-108">ByDeletedCertificates</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab1f0-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ab1f0-109">DESCRIPTION</span></span>
<span data-ttu-id="ab1f0-110">O cmdlet **Get-AzureKeyVaultCertificate** Obtém o certificado especificado ou as versões de um certificado de um cofre de chaves no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-110">The **Get-AzureKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="ab1f0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ab1f0-111">EXAMPLES</span></span>

### <span data-ttu-id="ab1f0-112">Exemplo 1: obter um certificado</span><span class="sxs-lookup"><span data-stu-id="ab1f0-112">Example 1: Get a certificate</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
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

<span data-ttu-id="ab1f0-113">Esse comando obtém o certificado chamado TestCert01 do cofre de chaves chamado ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="ab1f0-114">Exemplo 2: obter todos os certificados que foram excluídos, mas não foram removidos deste cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="ab1f0-115">Esse comando obtém todos os certificados que foram excluídos anteriormente, mas não foram removidos, no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="ab1f0-116">Exemplo 3: Obtém o certificado MyCert que foi excluído, mas não foi removido para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="ab1f0-117">Esse comando obtém o certificado chamado ' MyCert ' que foi excluído anteriormente, mas não foi removido, no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="ab1f0-118">Esse comando retornará metadados como a data de exclusão e a data de descarte programada desse certificado excluído.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="ab1f0-119">OS</span><span class="sxs-lookup"><span data-stu-id="ab1f0-119">PARAMETERS</span></span>

### <span data-ttu-id="ab1f0-120">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="ab1f0-120">-IncludeVersions</span></span>
<span data-ttu-id="ab1f0-121">Indica que essa operação obtém todas as versões do certificado.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-121">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByCertificateVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-122">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="ab1f0-122">-InRemovedState</span></span>
<span data-ttu-id="ab1f0-123">Especifica se devem ser incluídos certificados excluídos anteriormente na saída.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-123">Specifies whether to include previously deleted certificates in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedCertificates
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab1f0-124">-Name</span></span>
<span data-ttu-id="ab1f0-125">Especifica o nome do certificado a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-125">Specifies the name of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName, ByCertificateVersions
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedCertificates
Aliases: CertificateName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-126">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="ab1f0-126">-VaultName</span></span>
<span data-ttu-id="ab1f0-127">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-127">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="ab1f0-128">-Versão</span><span class="sxs-lookup"><span data-stu-id="ab1f0-128">-Version</span></span>
<span data-ttu-id="ab1f0-129">Especifica a versão de um certificado.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-129">Specifies the version of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: CertificateVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab1f0-130">-DefaultProfile</span></span>
<span data-ttu-id="ab1f0-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab1f0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab1f0-132">CommonParameters</span></span>
<span data-ttu-id="ab1f0-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab1f0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab1f0-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab1f0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab1f0-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ab1f0-135">INPUTS</span></span>

## <span data-ttu-id="ab1f0-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ab1f0-136">OUTPUTS</span></span>

### <span data-ttu-id="ab1f0-137">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. CertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="ab1f0-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="ab1f0-138">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ab1f0-138">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="ab1f0-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ab1f0-139">NOTES</span></span>

## <span data-ttu-id="ab1f0-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab1f0-140">RELATED LINKS</span></span>

[<span data-ttu-id="ab1f0-141">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ab1f0-141">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="ab1f0-142">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ab1f0-142">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="ab1f0-143">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ab1f0-143">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="ab1f0-144">Desfazer-AzureKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="ab1f0-144">Undo-AzureKeyVaultSecretCertificate</span></span>](./Undo-AzureKeyVaultSecretCertificate.md)
