---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://go.microsoft.com/fwlink/?LinkId=690297
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
ms.openlocfilehash: 48d050623ea75bed1aee1b78a26bf81bf3305e06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427922"
---
# <span data-ttu-id="cd938-101">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cd938-101">Get-AzureKeyVaultKey</span></span>

## <span data-ttu-id="cd938-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd938-102">SYNOPSIS</span></span>
<span data-ttu-id="cd938-103">Obtém chaves do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="cd938-103">Gets Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd938-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd938-104">SYNTAX</span></span>

### <span data-ttu-id="cd938-105">ByVaultName (padrão)</span><span class="sxs-lookup"><span data-stu-id="cd938-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd938-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="cd938-106">ByKeyName</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd938-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="cd938-107">ByKeyVersions</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd938-108">ByDeletedKey</span><span class="sxs-lookup"><span data-stu-id="cd938-108">ByDeletedKey</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd938-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cd938-109">DESCRIPTION</span></span>
<span data-ttu-id="cd938-110">O cmdlet **Get-AzureKeyVaultKey** Obtém as chaves do cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="cd938-110">The **Get-AzureKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="cd938-111">Esse cmdlet obtém um determinado **Microsoft. Azure. Commands. subvault. Models. keybundle** ou uma lista de todos os objetos **keybundle** em um cofre de chaves ou por versão.</span><span class="sxs-lookup"><span data-stu-id="cd938-111">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="cd938-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd938-112">EXAMPLES</span></span>

### <span data-ttu-id="cd938-113">Exemplo 1: obter todas as chaves em um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="cd938-113">Example 1: Get all the keys in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso'
```

<span data-ttu-id="cd938-114">Esse comando obtém todas as chaves no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="cd938-114">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="cd938-115">Exemplo 2: obter a versão atual de uma chave</span><span class="sxs-lookup"><span data-stu-id="cd938-115">Example 2: Get the current version of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

<span data-ttu-id="cd938-116">Esse comando obtém a versão atual da chave chamada ITPfx no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="cd938-116">This command gets the current version of the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="cd938-117">Exemplo 3: obter todas as versões de uma chave</span><span class="sxs-lookup"><span data-stu-id="cd938-117">Example 3: Get all versions of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

<span data-ttu-id="cd938-118">Este comando obtém todas as versões a chave chamada ITPfx na chave vaultnamed contoso.</span><span class="sxs-lookup"><span data-stu-id="cd938-118">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="cd938-119">Exemplo 4: obter uma versão específica de uma chave</span><span class="sxs-lookup"><span data-stu-id="cd938-119">Example 4: Get a specific version of a key</span></span>
```
PS C:\>$Key = Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

<span data-ttu-id="cd938-120">Esse comando obtém uma versão específica da chave chamada ITPfx no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="cd938-120">This command gets a specific version of the key named ITPfx in the key vault named Contoso.</span></span>
<span data-ttu-id="cd938-121">Depois de executar esse comando, você pode inspecionar várias propriedades da chave navegando no objeto $Key.</span><span class="sxs-lookup"><span data-stu-id="cd938-121">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="cd938-122">Exemplo 5: obter todas as chaves que foram excluídas, mas não eliminadas para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="cd938-122">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="cd938-123">Esse comando obtém todas as chaves que foram excluídas anteriormente, mas não foram limpas, no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="cd938-123">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="cd938-124">Exemplo 6: Obtém a chave ITPfx que foi excluída, mas não é eliminada para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="cd938-124">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

<span data-ttu-id="cd938-125">Esse comando obtém a chave ITPfx que foi excluída anteriormente, mas não foi eliminada, no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="cd938-125">This command gets the key ITPfx that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="cd938-126">Esse comando retornará metadados como a data de exclusão e a data de descarte programada dessa chave excluída.</span><span class="sxs-lookup"><span data-stu-id="cd938-126">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

## <span data-ttu-id="cd938-127">OS</span><span class="sxs-lookup"><span data-stu-id="cd938-127">PARAMETERS</span></span>

### <span data-ttu-id="cd938-128">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="cd938-128">-IncludeVersions</span></span>
<span data-ttu-id="cd938-129">Indica que esse cmdlet obtém todas as versões de uma chave.</span><span class="sxs-lookup"><span data-stu-id="cd938-129">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="cd938-130">A versão atual de uma chave é a primeira na lista.</span><span class="sxs-lookup"><span data-stu-id="cd938-130">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="cd938-131">Se você especificar esse parâmetro, também deverá especificar o *nome* e os parâmetros de *cofrename* .</span><span class="sxs-lookup"><span data-stu-id="cd938-131">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="cd938-132">Se você não especificar o parâmetro *IncludeVersions* , esse cmdlet obtém a versão atual da chave com o *nome* especificado.</span><span class="sxs-lookup"><span data-stu-id="cd938-132">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd938-133">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="cd938-133">-InRemovedState</span></span>
<span data-ttu-id="cd938-134">Especifica se as chaves excluídas anteriormente devem ser mostradas na saída.</span><span class="sxs-lookup"><span data-stu-id="cd938-134">Specifies whether to show the previously deleted keys in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedKey
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd938-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd938-135">-Name</span></span>
<span data-ttu-id="cd938-136">Especifica o nome do pacote de chaves a obter.</span><span class="sxs-lookup"><span data-stu-id="cd938-136">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedKey
Aliases: KeyName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd938-137">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="cd938-137">-VaultName</span></span>
<span data-ttu-id="cd938-138">Especifica o nome do cofre de chaves do qual este cmdlet obtém chaves.</span><span class="sxs-lookup"><span data-stu-id="cd938-138">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="cd938-139">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de um cofre de chaves com base no nome especificado por esse parâmetro e no ambiente selecionado.</span><span class="sxs-lookup"><span data-stu-id="cd938-139">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="cd938-140">-Versão</span><span class="sxs-lookup"><span data-stu-id="cd938-140">-Version</span></span>
<span data-ttu-id="cd938-141">Especifica a versão da chave.</span><span class="sxs-lookup"><span data-stu-id="cd938-141">Specifies the key version.</span></span>
<span data-ttu-id="cd938-142">Esse cmdlet constrói o FQDN de uma chave com base no nome do cofre de chaves, no ambiente selecionado atualmente, no nome da chave e na versão de chave.</span><span class="sxs-lookup"><span data-stu-id="cd938-142">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd938-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd938-143">-DefaultProfile</span></span>
<span data-ttu-id="cd938-144">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cd938-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd938-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd938-145">CommonParameters</span></span>
<span data-ttu-id="cd938-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd938-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd938-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd938-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd938-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cd938-148">INPUTS</span></span>

### <span data-ttu-id="cd938-149">String</span><span class="sxs-lookup"><span data-stu-id="cd938-149">String</span></span>

## <span data-ttu-id="cd938-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cd938-150">OUTPUTS</span></span>

### <span data-ttu-id="cd938-151">List<Microsoft. Azure. Commands. keyvault. Models. KeyIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. keybundle, List<Microsoft. Azure. Commands. keyvault. Models. DeletedKeyIdentityItem>, Microsoft. Azure. Commands. subvault. Models. DeletedKeyBundle</span><span class="sxs-lookup"><span data-stu-id="cd938-151">List<Microsoft.Azure.Commands.KeyVault.Models.KeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyBundle, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>

## <span data-ttu-id="cd938-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cd938-152">NOTES</span></span>

## <span data-ttu-id="cd938-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd938-153">RELATED LINKS</span></span>

[<span data-ttu-id="cd938-154">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cd938-154">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="cd938-155">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cd938-155">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="cd938-156">Desfazer-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="cd938-156">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

[<span data-ttu-id="cd938-157">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="cd938-157">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

