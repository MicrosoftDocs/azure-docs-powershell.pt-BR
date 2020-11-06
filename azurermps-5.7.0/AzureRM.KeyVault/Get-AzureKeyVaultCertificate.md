---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
ms.openlocfilehash: 87b030229eb2a1f4bb91122aaec8a119134d27fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428909"
---
# <span data-ttu-id="4b8fe-101">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4b8fe-101">Get-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="4b8fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b8fe-102">SYNOPSIS</span></span>
<span data-ttu-id="4b8fe-103">Obtém um certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="4b8fe-103">Gets a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b8fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b8fe-104">SYNTAX</span></span>

### <span data-ttu-id="4b8fe-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="4b8fe-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b8fe-106">ByCertificateNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="4b8fe-106">ByCertificateNameAndVersion</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b8fe-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="4b8fe-107">ByCertificateAllVersions</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b8fe-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="4b8fe-108">ByNameInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b8fe-109">ByCertificateNameAndVersionInputObject</span><span class="sxs-lookup"><span data-stu-id="4b8fe-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b8fe-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="4b8fe-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b8fe-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b8fe-111">DESCRIPTION</span></span>
<span data-ttu-id="4b8fe-112">O cmdlet **Get-AzureKeyVaultCertificate** Obtém o certificado especificado ou as versões de um certificado de um cofre de chaves no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="4b8fe-112">The **Get-AzureKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="4b8fe-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b8fe-113">EXAMPLES</span></span>

### <span data-ttu-id="4b8fe-114">Exemplo 1: obter um certificado</span><span class="sxs-lookup"><span data-stu-id="4b8fe-114">Example 1: Get a certificate</span></span>
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

<span data-ttu-id="4b8fe-115">Esse comando obtém o certificado chamado TestCert01 do cofre de chaves chamado ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="4b8fe-115">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="4b8fe-116">Exemplo 2: obter todos os certificados que foram excluídos, mas não foram removidos deste cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="4b8fe-116">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="4b8fe-117">Esse comando obtém todos os certificados que foram excluídos anteriormente, mas não foram removidos, no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="4b8fe-117">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="4b8fe-118">Exemplo 3: Obtém o certificado MyCert que foi excluído, mas não foi removido para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="4b8fe-118">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="4b8fe-119">Esse comando obtém o certificado chamado ' MyCert ' que foi excluído anteriormente, mas não foi removido, no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="4b8fe-119">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="4b8fe-120">Esse comando retornará metadados como a data de exclusão e a data de descarte programada desse certificado excluído.</span><span class="sxs-lookup"><span data-stu-id="4b8fe-120">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="4b8fe-121">OS</span><span class="sxs-lookup"><span data-stu-id="4b8fe-121">PARAMETERS</span></span>

### <span data-ttu-id="4b8fe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b8fe-122">-DefaultProfile</span></span>
<span data-ttu-id="4b8fe-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4b8fe-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b8fe-124">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="4b8fe-124">-IncludeVersions</span></span>
<span data-ttu-id="4b8fe-125">Indica que essa operação obtém todas as versões do certificado.</span><span class="sxs-lookup"><span data-stu-id="4b8fe-125">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByCertificateAllVersions, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b8fe-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b8fe-126">-InputObject</span></span>
<span data-ttu-id="4b8fe-127">Objeto do keyvault.</span><span class="sxs-lookup"><span data-stu-id="4b8fe-127">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByNameInputObject, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b8fe-128">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="4b8fe-128">-InRemovedState</span></span>
<span data-ttu-id="4b8fe-129">Especifica se devem ser incluídos certificados excluídos anteriormente na saída</span><span class="sxs-lookup"><span data-stu-id="4b8fe-129">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByName, ByNameInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b8fe-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b8fe-130">-Name</span></span>
<span data-ttu-id="4b8fe-131">Especifica o nome do certificado a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="4b8fe-131">Specifies the name of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByNameInputObject
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b8fe-132">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="4b8fe-132">-VaultName</span></span>
<span data-ttu-id="4b8fe-133">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="4b8fe-133">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByCertificateNameAndVersion, ByCertificateAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b8fe-134">-Versão</span><span class="sxs-lookup"><span data-stu-id="4b8fe-134">-Version</span></span>
<span data-ttu-id="4b8fe-135">Especifica a versão de um certificado.</span><span class="sxs-lookup"><span data-stu-id="4b8fe-135">Specifies the version of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateNameAndVersionInputObject
Aliases: CertificateVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b8fe-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b8fe-136">CommonParameters</span></span>
<span data-ttu-id="4b8fe-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b8fe-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b8fe-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b8fe-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b8fe-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b8fe-139">INPUTS</span></span>

### <span data-ttu-id="4b8fe-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4b8fe-140">None</span></span>
<span data-ttu-id="4b8fe-141">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="4b8fe-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4b8fe-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b8fe-142">OUTPUTS</span></span>

### <span data-ttu-id="4b8fe-143">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="4b8fe-143">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem]</span></span>

### <span data-ttu-id="4b8fe-144">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4b8fe-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="4b8fe-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b8fe-145">NOTES</span></span>

## <span data-ttu-id="4b8fe-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b8fe-146">RELATED LINKS</span></span>

[<span data-ttu-id="4b8fe-147">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4b8fe-147">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="4b8fe-148">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4b8fe-148">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="4b8fe-149">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4b8fe-149">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="4b8fe-150">Desfazer-AzureKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="4b8fe-150">Undo-AzureKeyVaultSecretCertificate</span></span>](./Undo-AzureKeyVaultSecretCertificate.md)
