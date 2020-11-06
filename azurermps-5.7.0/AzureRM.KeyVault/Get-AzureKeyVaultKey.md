---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
ms.openlocfilehash: eaddfaa6be725d588c8856031a34e1bdefcc3892
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432491"
---
# <span data-ttu-id="3d1f9-101">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3d1f9-101">Get-AzureKeyVaultKey</span></span>

## <span data-ttu-id="3d1f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d1f9-102">SYNOPSIS</span></span>
<span data-ttu-id="3d1f9-103">Obtém chaves do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="3d1f9-103">Gets Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d1f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d1f9-104">SYNTAX</span></span>

### <span data-ttu-id="3d1f9-105">ByVaultName (padrão)</span><span class="sxs-lookup"><span data-stu-id="3d1f9-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d1f9-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="3d1f9-106">ByKeyName</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d1f9-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="3d1f9-107">ByKeyVersions</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d1f9-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="3d1f9-108">ByInputObjectVaultName</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d1f9-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="3d1f9-109">ByInputObjectKeyName</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d1f9-110">ByKInputObjecteyVersions</span><span class="sxs-lookup"><span data-stu-id="3d1f9-110">ByKInputObjecteyVersions</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d1f9-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3d1f9-111">DESCRIPTION</span></span>
<span data-ttu-id="3d1f9-112">O cmdlet **Get-AzureKeyVaultKey** Obtém as chaves do cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="3d1f9-112">The **Get-AzureKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="3d1f9-113">Esse cmdlet obtém um determinado **Microsoft. Azure. Commands. subvault. Models. keybundle** ou uma lista de todos os objetos **keybundle** em um cofre de chaves ou por versão.</span><span class="sxs-lookup"><span data-stu-id="3d1f9-113">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="3d1f9-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d1f9-114">EXAMPLES</span></span>

### <span data-ttu-id="3d1f9-115">Exemplo 1: obter todas as chaves em um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="3d1f9-115">Example 1: Get all the keys in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso'
```

<span data-ttu-id="3d1f9-116">Esse comando obtém todas as chaves no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="3d1f9-116">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="3d1f9-117">Exemplo 2: obter a versão atual de uma chave</span><span class="sxs-lookup"><span data-stu-id="3d1f9-117">Example 2: Get the current version of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

<span data-ttu-id="3d1f9-118">Esse comando obtém a versão atual da chave chamada ITPfx no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="3d1f9-118">This command gets the current version of the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="3d1f9-119">Exemplo 3: obter todas as versões de uma chave</span><span class="sxs-lookup"><span data-stu-id="3d1f9-119">Example 3: Get all versions of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

<span data-ttu-id="3d1f9-120">Este comando obtém todas as versões a chave chamada ITPfx na chave vaultnamed contoso.</span><span class="sxs-lookup"><span data-stu-id="3d1f9-120">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="3d1f9-121">Exemplo 4: obter uma versão específica de uma chave</span><span class="sxs-lookup"><span data-stu-id="3d1f9-121">Example 4: Get a specific version of a key</span></span>
```
PS C:\>$Key = Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

<span data-ttu-id="3d1f9-122">Esse comando obtém uma versão específica da chave chamada ITPfx no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="3d1f9-122">This command gets a specific version of the key named ITPfx in the key vault named Contoso.</span></span>
<span data-ttu-id="3d1f9-123">Depois de executar esse comando, você pode inspecionar várias propriedades da chave navegando no objeto $Key.</span><span class="sxs-lookup"><span data-stu-id="3d1f9-123">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="3d1f9-124">Exemplo 5: obter todas as chaves que foram excluídas, mas não eliminadas para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="3d1f9-124">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="3d1f9-125">Esse comando obtém todas as chaves que foram excluídas anteriormente, mas não foram limpas, no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="3d1f9-125">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="3d1f9-126">Exemplo 6: Obtém a chave ITPfx que foi excluída, mas não é eliminada para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="3d1f9-126">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

<span data-ttu-id="3d1f9-127">Esse comando obtém a chave ITPfx que foi excluída anteriormente, mas não foi eliminada, no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="3d1f9-127">This command gets the key ITPfx that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="3d1f9-128">Esse comando retornará metadados como a data de exclusão e a data de descarte programada dessa chave excluída.</span><span class="sxs-lookup"><span data-stu-id="3d1f9-128">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

## <span data-ttu-id="3d1f9-129">OS</span><span class="sxs-lookup"><span data-stu-id="3d1f9-129">PARAMETERS</span></span>

### <span data-ttu-id="3d1f9-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d1f9-130">-DefaultProfile</span></span>
<span data-ttu-id="3d1f9-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3d1f9-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d1f9-132">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="3d1f9-132">-IncludeVersions</span></span>
<span data-ttu-id="3d1f9-133">Indica que esse cmdlet obtém todas as versões de uma chave.</span><span class="sxs-lookup"><span data-stu-id="3d1f9-133">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="3d1f9-134">A versão atual de uma chave é a primeira na lista.</span><span class="sxs-lookup"><span data-stu-id="3d1f9-134">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="3d1f9-135">Se você especificar esse parâmetro, também deverá especificar o *nome* e os parâmetros de *cofrename* .</span><span class="sxs-lookup"><span data-stu-id="3d1f9-135">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="3d1f9-136">Se você não especificar o parâmetro *IncludeVersions* , esse cmdlet obtém a versão atual da chave com o *nome* especificado.</span><span class="sxs-lookup"><span data-stu-id="3d1f9-136">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByKeyVersions, ByKInputObjecteyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d1f9-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d1f9-137">-InputObject</span></span>
<span data-ttu-id="3d1f9-138">Objeto do keyvault.</span><span class="sxs-lookup"><span data-stu-id="3d1f9-138">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectKeyName, ByKInputObjecteyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d1f9-139">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="3d1f9-139">-InRemovedState</span></span>
<span data-ttu-id="3d1f9-140">Especifica se as chaves excluídas anteriormente devem ser mostradas na saída</span><span class="sxs-lookup"><span data-stu-id="3d1f9-140">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d1f9-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d1f9-141">-Name</span></span>
<span data-ttu-id="3d1f9-142">Especifica o nome do pacote de chaves a obter.</span><span class="sxs-lookup"><span data-stu-id="3d1f9-142">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByKInputObjecteyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d1f9-143">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="3d1f9-143">-VaultName</span></span>
<span data-ttu-id="3d1f9-144">Especifica o nome do cofre de chaves do qual este cmdlet obtém chaves.</span><span class="sxs-lookup"><span data-stu-id="3d1f9-144">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="3d1f9-145">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de um cofre de chaves com base no nome especificado por esse parâmetro e no ambiente selecionado.</span><span class="sxs-lookup"><span data-stu-id="3d1f9-145">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName, ByKeyName, ByKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d1f9-146">-Versão</span><span class="sxs-lookup"><span data-stu-id="3d1f9-146">-Version</span></span>
<span data-ttu-id="3d1f9-147">Especifica a versão da chave.</span><span class="sxs-lookup"><span data-stu-id="3d1f9-147">Specifies the key version.</span></span>
<span data-ttu-id="3d1f9-148">Esse cmdlet constrói o FQDN de uma chave com base no nome do cofre de chaves, no ambiente selecionado atualmente, no nome da chave e na versão de chave.</span><span class="sxs-lookup"><span data-stu-id="3d1f9-148">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName, ByInputObjectKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d1f9-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d1f9-149">CommonParameters</span></span>
<span data-ttu-id="3d1f9-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d1f9-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d1f9-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d1f9-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d1f9-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3d1f9-152">INPUTS</span></span>

### <span data-ttu-id="3d1f9-153">String</span><span class="sxs-lookup"><span data-stu-id="3d1f9-153">String</span></span>

## <span data-ttu-id="3d1f9-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3d1f9-154">OUTPUTS</span></span>

### <span data-ttu-id="3d1f9-155">List<Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey, List<Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3d1f9-155">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey, List<Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="3d1f9-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3d1f9-156">NOTES</span></span>

## <span data-ttu-id="3d1f9-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d1f9-157">RELATED LINKS</span></span>

[<span data-ttu-id="3d1f9-158">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3d1f9-158">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="3d1f9-159">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3d1f9-159">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="3d1f9-160">Desfazer-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="3d1f9-160">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

[<span data-ttu-id="3d1f9-161">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="3d1f9-161">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

