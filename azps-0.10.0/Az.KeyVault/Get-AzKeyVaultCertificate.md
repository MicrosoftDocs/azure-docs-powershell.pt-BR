---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: 40514bdd6ed8d37679d3002f80146e622a0614e9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775803"
---
# <span data-ttu-id="5db9f-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="5db9f-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="5db9f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5db9f-102">SYNOPSIS</span></span>
<span data-ttu-id="5db9f-103">Obtém um certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5db9f-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="5db9f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5db9f-104">SYNTAX</span></span>

### <span data-ttu-id="5db9f-105">ByVaultName (padrão)</span><span class="sxs-lookup"><span data-stu-id="5db9f-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5db9f-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="5db9f-106">ByCertificateName</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5db9f-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="5db9f-107">ByCertificateVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5db9f-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="5db9f-108">ByDeletedCertificates</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5db9f-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5db9f-109">DESCRIPTION</span></span>
<span data-ttu-id="5db9f-110">O cmdlet **Get-AzKeyVaultCertificate** Obtém o certificado especificado ou as versões de um certificado de um cofre de chaves no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="5db9f-110">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="5db9f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5db9f-111">EXAMPLES</span></span>

### <span data-ttu-id="5db9f-112">Exemplo 1: obter um certificado</span><span class="sxs-lookup"><span data-stu-id="5db9f-112">Example 1: Get a certificate</span></span>
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

<span data-ttu-id="5db9f-113">Esse comando obtém o certificado chamado TestCert01 do cofre de chaves chamado ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="5db9f-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="5db9f-114">Exemplo 2: obter todos os certificados que foram excluídos, mas não foram removidos deste cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5db9f-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="5db9f-115">Esse comando obtém todos os certificados que foram excluídos anteriormente, mas não foram removidos, no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="5db9f-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="5db9f-116">Exemplo 3: Obtém o certificado MyCert que foi excluído, mas não foi removido para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5db9f-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="5db9f-117">Esse comando obtém o certificado chamado ' MyCert ' que foi excluído anteriormente, mas não foi removido, no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="5db9f-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="5db9f-118">Esse comando retornará metadados como a data de exclusão e a data de descarte programada desse certificado excluído.</span><span class="sxs-lookup"><span data-stu-id="5db9f-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="5db9f-119">OS</span><span class="sxs-lookup"><span data-stu-id="5db9f-119">PARAMETERS</span></span>

### <span data-ttu-id="5db9f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5db9f-120">-DefaultProfile</span></span>
<span data-ttu-id="5db9f-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5db9f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5db9f-122">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="5db9f-122">-IncludeVersions</span></span>
<span data-ttu-id="5db9f-123">Indica que essa operação obtém todas as versões do certificado.</span><span class="sxs-lookup"><span data-stu-id="5db9f-123">Indicates that this operation gets all versions of the certificate.</span></span>

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

### <span data-ttu-id="5db9f-124">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="5db9f-124">-InRemovedState</span></span>
<span data-ttu-id="5db9f-125">Especifica se devem ser incluídos certificados excluídos anteriormente na saída</span><span class="sxs-lookup"><span data-stu-id="5db9f-125">Specifies whether to include previously deleted certificates in the output</span></span>

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

### <span data-ttu-id="5db9f-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="5db9f-126">-Name</span></span>
<span data-ttu-id="5db9f-127">Especifica o nome do certificado a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="5db9f-127">Specifies the name of the certificate to get.</span></span>

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

### <span data-ttu-id="5db9f-128">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="5db9f-128">-VaultName</span></span>
<span data-ttu-id="5db9f-129">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5db9f-129">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="5db9f-130">-Versão</span><span class="sxs-lookup"><span data-stu-id="5db9f-130">-Version</span></span>
<span data-ttu-id="5db9f-131">Especifica a versão de um certificado.</span><span class="sxs-lookup"><span data-stu-id="5db9f-131">Specifies the version of a certificate.</span></span>

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

### <span data-ttu-id="5db9f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5db9f-132">CommonParameters</span></span>
<span data-ttu-id="5db9f-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5db9f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5db9f-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5db9f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5db9f-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5db9f-135">INPUTS</span></span>

### <span data-ttu-id="5db9f-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5db9f-136">None</span></span>
<span data-ttu-id="5db9f-137">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="5db9f-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5db9f-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5db9f-138">OUTPUTS</span></span>

### <span data-ttu-id="5db9f-139">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. CertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="5db9f-139">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="5db9f-140">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="5db9f-140">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="5db9f-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5db9f-141">NOTES</span></span>

## <span data-ttu-id="5db9f-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5db9f-142">RELATED LINKS</span></span>

[<span data-ttu-id="5db9f-143">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="5db9f-143">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="5db9f-144">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="5db9f-144">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="5db9f-145">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="5db9f-145">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="5db9f-146">Desfazer-AzKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="5db9f-146">Undo-AzKeyVaultSecretCertificate</span></span>](./Undo-AzKeyVaultSecretCertificate.md)
