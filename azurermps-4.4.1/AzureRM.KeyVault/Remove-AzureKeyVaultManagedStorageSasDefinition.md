---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: fadf6b15eb25f07d88254a5d3a998f1692e5cf29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609996"
---
# <span data-ttu-id="78966-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="78966-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="78966-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78966-102">SYNOPSIS</span></span>
<span data-ttu-id="78966-103">Remove as definições de SAS de armazenamento do Azure que foram gerenciadas do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="78966-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78966-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78966-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78966-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="78966-105">DESCRIPTION</span></span>
<span data-ttu-id="78966-106">Remove as definições de SAS de armazenamento do Azure que foram gerenciadas do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="78966-106">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="78966-107">Isso também remove o segredo usado para obter o token SAS por essa definição de SAS.</span><span class="sxs-lookup"><span data-stu-id="78966-107">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="78966-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78966-108">EXAMPLES</span></span>

### <span data-ttu-id="78966-109">Exemplo 1: remover uma definição da SAS de armazenamento do Azure gerenciada do Key Vault.</span><span class="sxs-lookup"><span data-stu-id="78966-109">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef'
```

<span data-ttu-id="78966-110">Remove uma definição de SAS do repositório gerenciado do Key Vault ' mysasdef ' associada à conta ' mystorageaccount ' no cofre ' myvault '.</span><span class="sxs-lookup"><span data-stu-id="78966-110">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="78966-111">Exemplo 2: remover uma definição de SAS de armazenamento do Azure Managed Vault sem confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="78966-111">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -Force -Confirm:$False
```

<span data-ttu-id="78966-112">Remove uma definição de SAS do repositório gerenciado do Key Vault ' mysasdef ' associada à conta ' mystorageaccount ' no cofre ' myvault '.</span><span class="sxs-lookup"><span data-stu-id="78966-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="78966-113">OS</span><span class="sxs-lookup"><span data-stu-id="78966-113">PARAMETERS</span></span>

### <span data-ttu-id="78966-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="78966-114">-AccountName</span></span>
<span data-ttu-id="78966-115">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="78966-115">Storage account name.</span></span>
<span data-ttu-id="78966-116">O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, do ambiente selecionado no momento e do nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="78966-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78966-117">-Force</span><span class="sxs-lookup"><span data-stu-id="78966-117">-Force</span></span>
<span data-ttu-id="78966-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="78966-118">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78966-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="78966-119">-Name</span></span>
<span data-ttu-id="78966-120">Nome da definição de SAS de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="78966-120">Storage sas definition name.</span></span>
<span data-ttu-id="78966-121">O cmdlet constrói o FQDN de uma definição de SAS de armazenamento do nome do cofre, ambiente selecionado atualmente, nome da conta de armazenamento e nome da definição da SAS.</span><span class="sxs-lookup"><span data-stu-id="78966-121">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78966-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78966-122">-PassThru</span></span>
<span data-ttu-id="78966-123">O cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="78966-123">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="78966-124">Se essa opção for especificada, o cmdlet retornará a conta de armazenamento gerenciada que foi excluída.</span><span class="sxs-lookup"><span data-stu-id="78966-124">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78966-125">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="78966-125">-VaultName</span></span>
<span data-ttu-id="78966-126">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="78966-126">Vault name.</span></span>
<span data-ttu-id="78966-127">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="78966-127">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78966-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="78966-128">-Confirm</span></span>
<span data-ttu-id="78966-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78966-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78966-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78966-130">-WhatIf</span></span>
<span data-ttu-id="78966-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="78966-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78966-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="78966-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78966-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78966-133">-DefaultProfile</span></span>
<span data-ttu-id="78966-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="78966-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78966-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78966-135">CommonParameters</span></span>
<span data-ttu-id="78966-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78966-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78966-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78966-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78966-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="78966-138">INPUTS</span></span>

### <span data-ttu-id="78966-139">System. String</span><span class="sxs-lookup"><span data-stu-id="78966-139">System.String</span></span>

## <span data-ttu-id="78966-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="78966-140">OUTPUTS</span></span>

### <span data-ttu-id="78966-141">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="78966-141">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="78966-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="78966-142">NOTES</span></span>

## <span data-ttu-id="78966-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78966-143">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

