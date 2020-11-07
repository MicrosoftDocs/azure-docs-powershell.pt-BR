---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: d57f672ef440515e69535503f006e08b4c924646
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775773"
---
# <span data-ttu-id="1377d-101">Remove-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1377d-101">Remove-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="1377d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1377d-102">SYNOPSIS</span></span>
<span data-ttu-id="1377d-103">Remove uma conta de armazenamento gerenciada do Key Vault e todas as definições de SAS associadas.</span><span class="sxs-lookup"><span data-stu-id="1377d-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

## <span data-ttu-id="1377d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1377d-104">SYNTAX</span></span>

```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1377d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1377d-105">DESCRIPTION</span></span>
<span data-ttu-id="1377d-106">Desassocia uma conta de armazenamento do Azure do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="1377d-106">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="1377d-107">Isso não remove uma conta de armazenamento do Azure, mas remove as chaves da conta de serem gerenciadas pelo cofre de chave do Azure.</span><span class="sxs-lookup"><span data-stu-id="1377d-107">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="1377d-108">Todas as definições de SAS de armazenamento gerenciado de Key Vault também são removidas.</span><span class="sxs-lookup"><span data-stu-id="1377d-108">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="1377d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1377d-109">EXAMPLES</span></span>

### <span data-ttu-id="1377d-110">Exemplo 1: remover uma conta de armazenamento gerenciada do repositório de chaves e todas as definições de SAS associadas.</span><span class="sxs-lookup"><span data-stu-id="1377d-110">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="1377d-111">Desassocia a conta de armazenamento do Azure ' mystorageaccount ' do cofre de chaves ' myvault ' e impede que o cofre de chaves gerenciem suas chaves.</span><span class="sxs-lookup"><span data-stu-id="1377d-111">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="1377d-112">A conta "mystorageaccount" não será removida.</span><span class="sxs-lookup"><span data-stu-id="1377d-112">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="1377d-113">Todas as definições de SAS de armazenamento gerenciado de cofre de chaves associadas a essa conta serão removidas.</span><span class="sxs-lookup"><span data-stu-id="1377d-113">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="1377d-114">Exemplo 2: remover uma conta de armazenamento gerenciada do repositório de chaves e todas as definições de SAS associadas sem confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="1377d-114">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Force -Confirm:$False
```

<span data-ttu-id="1377d-115">Desassocia a conta de armazenamento do Azure ' mystorageaccount ' do cofre de chaves ' myvault ' e impede que o cofre de chaves gerenciem suas chaves.</span><span class="sxs-lookup"><span data-stu-id="1377d-115">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="1377d-116">A conta "mystorageaccount" não será removida.</span><span class="sxs-lookup"><span data-stu-id="1377d-116">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="1377d-117">Todas as definições de SAS de armazenamento gerenciado de cofre de chaves associadas a essa conta serão removidas.</span><span class="sxs-lookup"><span data-stu-id="1377d-117">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

## <span data-ttu-id="1377d-118">OS</span><span class="sxs-lookup"><span data-stu-id="1377d-118">PARAMETERS</span></span>

### <span data-ttu-id="1377d-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1377d-119">-AccountName</span></span>
<span data-ttu-id="1377d-120">Nome da conta de armazenamento gerenciado do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="1377d-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="1377d-121">O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, ambiente selecionado atualmente e nome da conta de armazenamento gerenciada.</span><span class="sxs-lookup"><span data-stu-id="1377d-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1377d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1377d-122">-DefaultProfile</span></span>
<span data-ttu-id="1377d-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1377d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1377d-124">-Force</span><span class="sxs-lookup"><span data-stu-id="1377d-124">-Force</span></span>
<span data-ttu-id="1377d-125">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="1377d-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1377d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1377d-126">-PassThru</span></span>
<span data-ttu-id="1377d-127">O cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="1377d-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1377d-128">Se essa opção for especificada, o cmdlet retornará a conta de armazenamento gerenciada que foi excluída.</span><span class="sxs-lookup"><span data-stu-id="1377d-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="1377d-129">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="1377d-129">-VaultName</span></span>
<span data-ttu-id="1377d-130">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="1377d-130">Vault name.</span></span>
<span data-ttu-id="1377d-131">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="1377d-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="1377d-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1377d-132">-Confirm</span></span>
<span data-ttu-id="1377d-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1377d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1377d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1377d-134">-WhatIf</span></span>
<span data-ttu-id="1377d-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1377d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1377d-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1377d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1377d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1377d-137">CommonParameters</span></span>
<span data-ttu-id="1377d-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1377d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1377d-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1377d-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1377d-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1377d-140">INPUTS</span></span>

### <span data-ttu-id="1377d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1377d-141">System.String</span></span>

## <span data-ttu-id="1377d-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1377d-142">OUTPUTS</span></span>

### <span data-ttu-id="1377d-143">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1377d-143">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="1377d-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1377d-144">NOTES</span></span>

## <span data-ttu-id="1377d-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1377d-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

