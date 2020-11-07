---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: b14e97ba09cba70a9ec571b2fbf1273de7157930
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776667"
---
# <span data-ttu-id="16811-101">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="16811-101">Get-AzKeyVaultSecret</span></span>

## <span data-ttu-id="16811-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16811-102">SYNOPSIS</span></span>
<span data-ttu-id="16811-103">Obtém os segredos em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="16811-103">Gets the secrets in a key vault.</span></span>

## <span data-ttu-id="16811-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16811-104">SYNTAX</span></span>

### <span data-ttu-id="16811-105">ByVaultName (padrão)</span><span class="sxs-lookup"><span data-stu-id="16811-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16811-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="16811-106">BySecretName</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16811-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="16811-107">BySecretVersions</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16811-108">ByDeletedSecrets</span><span class="sxs-lookup"><span data-stu-id="16811-108">ByDeletedSecrets</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16811-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="16811-109">DESCRIPTION</span></span>
<span data-ttu-id="16811-110">O cmdlet **Get-AzKeyVaultSecret** Obtém segredos em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="16811-110">The **Get-AzKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="16811-111">Esse cmdlet obtém um segredo específico ou todos os segredos em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="16811-111">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="16811-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16811-112">EXAMPLES</span></span>

### <span data-ttu-id="16811-113">Exemplo 1: obter todas as versões atuais de todos os segredos em um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="16811-113">Example 1: Get all current versions of all secrets in a key vault</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso'
```

<span data-ttu-id="16811-114">Esse comando obtém as versões atuais de todos os segredos no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="16811-114">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="16811-115">Exemplo 2: obter todas as versões de um segredo específico</span><span class="sxs-lookup"><span data-stu-id="16811-115">Example 2: Get all versions of a specific secret</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

<span data-ttu-id="16811-116">Este comando obtém todas as versões do segredo chamado ITSecret no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="16811-116">This command gets all versions of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="16811-117">Exemplo 3: obter a versão atual de um segredo específico</span><span class="sxs-lookup"><span data-stu-id="16811-117">Example 3: Get the current version of a specific secret</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

<span data-ttu-id="16811-118">Esse comando obtém a versão atual do segredo chamado ITSecret no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="16811-118">This command gets the current version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="16811-119">Exemplo 4: obter uma versão específica de um segredo específico</span><span class="sxs-lookup"><span data-stu-id="16811-119">Example 4: Get a specific version of a specific secret</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

<span data-ttu-id="16811-120">Esse comando obtém uma versão específica do segredo chamado ITSecret no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="16811-120">This command gets a specific version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="16811-121">Exemplo 5: obter o valor de texto sem formatação da versão atual de um segredo específico</span><span class="sxs-lookup"><span data-stu-id="16811-121">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```
PS C:\>$secret = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

<span data-ttu-id="16811-122">Esses comandos obtêm a versão atual de um segredo chamado ITSecret e exibem o valor de texto sem formatação desse segredo.</span><span class="sxs-lookup"><span data-stu-id="16811-122">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="16811-123">Exemplo 6: obter todos os segredos que foram excluídos, mas não foram removidos para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="16811-123">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="16811-124">Esse comando obtém todos os segredos que foram excluídos anteriormente, mas não foram removidos, no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="16811-124">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="16811-125">Exemplo 7: Obtém a ITSecret secreta que foi excluída, mas não é eliminada para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="16811-125">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

<span data-ttu-id="16811-126">Esse comando obtém o segredo ITSecret que foi excluído anteriormente, mas não é removido, no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="16811-126">This command gets the secret ITSecret that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="16811-127">Esse comando retornará metadados como a data de exclusão e a data de descarte programada desse segredo excluído.</span><span class="sxs-lookup"><span data-stu-id="16811-127">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

## <span data-ttu-id="16811-128">OS</span><span class="sxs-lookup"><span data-stu-id="16811-128">PARAMETERS</span></span>

### <span data-ttu-id="16811-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16811-129">-DefaultProfile</span></span>
<span data-ttu-id="16811-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="16811-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16811-131">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="16811-131">-IncludeVersions</span></span>
<span data-ttu-id="16811-132">Indica que esse cmdlet obtém todas as versões de um segredo.</span><span class="sxs-lookup"><span data-stu-id="16811-132">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="16811-133">A versão atual de um segredo é a primeira na lista.</span><span class="sxs-lookup"><span data-stu-id="16811-133">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="16811-134">Se você especificar esse parâmetro, também deverá especificar o *nome* e os parâmetros de *cofrename* .</span><span class="sxs-lookup"><span data-stu-id="16811-134">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="16811-135">Se você não especificar o parâmetro *IncludeVersions* , esse cmdlet obtém a versão atual do segredo com o *nome* especificado.</span><span class="sxs-lookup"><span data-stu-id="16811-135">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySecretVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16811-136">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="16811-136">-InRemovedState</span></span>
<span data-ttu-id="16811-137">Especifica se os segredos excluídos anteriormente na saída devem ser mostrados</span><span class="sxs-lookup"><span data-stu-id="16811-137">Specifies whether to show the previously deleted secrets in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedSecrets
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16811-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="16811-138">-Name</span></span>
<span data-ttu-id="16811-139">Especifica o nome do segredo a obter.</span><span class="sxs-lookup"><span data-stu-id="16811-139">Specifies the name of the secret to get.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName, BySecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedSecrets
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16811-140">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="16811-140">-VaultName</span></span>
<span data-ttu-id="16811-141">Especifica o nome do cofre de chaves ao qual o segredo pertence.</span><span class="sxs-lookup"><span data-stu-id="16811-141">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="16811-142">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de um cofre de chaves com base no nome que esse parâmetro especifica e seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="16811-142">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="16811-143">-Versão</span><span class="sxs-lookup"><span data-stu-id="16811-143">-Version</span></span>
<span data-ttu-id="16811-144">Especifica a versão secreta.</span><span class="sxs-lookup"><span data-stu-id="16811-144">Specifies the secret version.</span></span>
<span data-ttu-id="16811-145">Esse cmdlet constrói o FQDN de um segredo com base no nome do cofre de chaves, no ambiente selecionado atualmente, no nome do segredo e na versão secreta.</span><span class="sxs-lookup"><span data-stu-id="16811-145">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16811-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16811-146">CommonParameters</span></span>
<span data-ttu-id="16811-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16811-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16811-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16811-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16811-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="16811-149">INPUTS</span></span>

### <span data-ttu-id="16811-150">String</span><span class="sxs-lookup"><span data-stu-id="16811-150">String</span></span>

## <span data-ttu-id="16811-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="16811-151">OUTPUTS</span></span>

### <span data-ttu-id="16811-152">List<Microsoft. Azure. Commands. keyvault. Models. SecretIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. Secret, List<Microsoft. Azure. Commands. keyvault. Models. DeletedSecretIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. DeletedSecret</span><span class="sxs-lookup"><span data-stu-id="16811-152">List<Microsoft.Azure.Commands.KeyVault.Models.SecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.Secret, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedSecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>

## <span data-ttu-id="16811-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="16811-153">NOTES</span></span>

## <span data-ttu-id="16811-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16811-154">RELATED LINKS</span></span>

[<span data-ttu-id="16811-155">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="16811-155">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="16811-156">Desfazer-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="16811-156">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

[<span data-ttu-id="16811-157">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="16811-157">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)
