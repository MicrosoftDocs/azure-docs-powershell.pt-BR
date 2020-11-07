---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 98c4cca6b2de508ca48da4ccbc5cf9f9a31eaa0c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775772"
---
# <span data-ttu-id="67f91-101">Remove-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="67f91-101">Remove-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="67f91-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67f91-102">SYNOPSIS</span></span>
<span data-ttu-id="67f91-103">Remove as definições de SAS de armazenamento do Azure que foram gerenciadas do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="67f91-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

## <span data-ttu-id="67f91-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67f91-104">SYNTAX</span></span>

```
Remove-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67f91-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="67f91-105">DESCRIPTION</span></span>
<span data-ttu-id="67f91-106">Remove as definições de SAS de armazenamento do Azure que foram gerenciadas do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="67f91-106">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="67f91-107">Isso também remove o segredo usado para obter o token SAS por essa definição de SAS.</span><span class="sxs-lookup"><span data-stu-id="67f91-107">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="67f91-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67f91-108">EXAMPLES</span></span>

### <span data-ttu-id="67f91-109">Exemplo 1: remover uma definição da SAS de armazenamento do Azure gerenciada do Key Vault.</span><span class="sxs-lookup"><span data-stu-id="67f91-109">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef'
```

<span data-ttu-id="67f91-110">Remove uma definição de SAS do repositório gerenciado do Key Vault ' mysasdef ' associada à conta ' mystorageaccount ' no cofre ' myvault '.</span><span class="sxs-lookup"><span data-stu-id="67f91-110">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="67f91-111">Exemplo 2: remover uma definição de SAS de armazenamento do Azure Managed Vault sem confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="67f91-111">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -Force -Confirm:$False
```

<span data-ttu-id="67f91-112">Remove uma definição de SAS do repositório gerenciado do Key Vault ' mysasdef ' associada à conta ' mystorageaccount ' no cofre ' myvault '.</span><span class="sxs-lookup"><span data-stu-id="67f91-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="67f91-113">OS</span><span class="sxs-lookup"><span data-stu-id="67f91-113">PARAMETERS</span></span>

### <span data-ttu-id="67f91-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="67f91-114">-AccountName</span></span>
<span data-ttu-id="67f91-115">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="67f91-115">Storage account name.</span></span>
<span data-ttu-id="67f91-116">O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, do ambiente selecionado no momento e do nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="67f91-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67f91-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67f91-117">-DefaultProfile</span></span>
<span data-ttu-id="67f91-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="67f91-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67f91-119">-Force</span><span class="sxs-lookup"><span data-stu-id="67f91-119">-Force</span></span>
<span data-ttu-id="67f91-120">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="67f91-120">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67f91-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="67f91-121">-Name</span></span>
<span data-ttu-id="67f91-122">Nome da definição de SAS de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="67f91-122">Storage sas definition name.</span></span>
<span data-ttu-id="67f91-123">O cmdlet constrói o FQDN de uma definição de SAS de armazenamento do nome do cofre, ambiente selecionado atualmente, nome da conta de armazenamento e nome da definição da SAS.</span><span class="sxs-lookup"><span data-stu-id="67f91-123">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67f91-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67f91-124">-PassThru</span></span>
<span data-ttu-id="67f91-125">O cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="67f91-125">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="67f91-126">Se essa opção for especificada, o cmdlet retornará a conta de armazenamento gerenciada que foi excluída.</span><span class="sxs-lookup"><span data-stu-id="67f91-126">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67f91-127">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="67f91-127">-VaultName</span></span>
<span data-ttu-id="67f91-128">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="67f91-128">Vault name.</span></span>
<span data-ttu-id="67f91-129">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="67f91-129">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="67f91-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="67f91-130">-Confirm</span></span>
<span data-ttu-id="67f91-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67f91-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67f91-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67f91-132">-WhatIf</span></span>
<span data-ttu-id="67f91-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="67f91-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67f91-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="67f91-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67f91-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67f91-135">CommonParameters</span></span>
<span data-ttu-id="67f91-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67f91-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67f91-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67f91-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67f91-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="67f91-138">INPUTS</span></span>

### <span data-ttu-id="67f91-139">System. String</span><span class="sxs-lookup"><span data-stu-id="67f91-139">System.String</span></span>

## <span data-ttu-id="67f91-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="67f91-140">OUTPUTS</span></span>

### <span data-ttu-id="67f91-141">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="67f91-141">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="67f91-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="67f91-142">NOTES</span></span>

## <span data-ttu-id="67f91-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67f91-143">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

