---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
ms.openlocfilehash: 6a1994979cc6521cee083b07f336a76a54dd7cb7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785931"
---
# <span data-ttu-id="11094-101">Get-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="11094-101">Get-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="11094-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11094-102">SYNOPSIS</span></span>
<span data-ttu-id="11094-103">Obtém definições de SAS de armazenamento gerenciado do Key Vault.</span><span class="sxs-lookup"><span data-stu-id="11094-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11094-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11094-104">SYNTAX</span></span>

### <span data-ttu-id="11094-105">ByAccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="11094-105">ByAccountName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11094-106">ByDefinitionName</span><span class="sxs-lookup"><span data-stu-id="11094-106">ByDefinitionName</span></span>
```
Get-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11094-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="11094-107">DESCRIPTION</span></span>
<span data-ttu-id="11094-108">Obtém uma definição de SAS de armazenamento gerenciado de um cofre de chaves se o nome da definição for especificado.</span><span class="sxs-lookup"><span data-stu-id="11094-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="11094-109">Se o nome da definição não for especificado, todas as definições de SAS associadas à conta de armazenamento gerenciado do cofre de chaves especificado no cofre serão listadas.</span><span class="sxs-lookup"><span data-stu-id="11094-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="11094-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11094-110">EXAMPLES</span></span>

### <span data-ttu-id="11094-111">Exemplo 1: listar todas as definições de SAS de armazenamento gerenciado do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="11094-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="11094-112">Lista todas as definições de SAS associadas à conta de armazenamento gerenciado do Key Vault ' mystorageaccount ' gerenciada pelo cofre ' myvault '</span><span class="sxs-lookup"><span data-stu-id="11094-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="11094-113">Exemplo 2: obter uma conta de armazenamento gerenciado do Key Vault</span><span class="sxs-lookup"><span data-stu-id="11094-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasDef'
```

<span data-ttu-id="11094-114">Obtém os detalhes da definição de SAS ' mysasDef ' associada à conta de armazenamento gerenciado do Key Vault ' mystorageaccount ' gerenciada pelo cofre ' myvault '.</span><span class="sxs-lookup"><span data-stu-id="11094-114">Gets the details of SAS Definition 'mysasDef' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

## <span data-ttu-id="11094-115">OS</span><span class="sxs-lookup"><span data-stu-id="11094-115">PARAMETERS</span></span>

### <span data-ttu-id="11094-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="11094-116">-AccountName</span></span>
<span data-ttu-id="11094-117">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="11094-117">Vault name.</span></span>
<span data-ttu-id="11094-118">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="11094-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="11094-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11094-119">-DefaultProfile</span></span>
<span data-ttu-id="11094-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="11094-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11094-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="11094-121">-Name</span></span>
<span data-ttu-id="11094-122">Nome da definição de SAS de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="11094-122">Storage sas definition name.</span></span>
<span data-ttu-id="11094-123">O cmdlet constrói o FQDN de uma definição de SAS de armazenamento do nome do cofre, ambiente selecionado atualmente, nome da conta de armazenamento e nome da definição da SAS.</span><span class="sxs-lookup"><span data-stu-id="11094-123">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: ByDefinitionName
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11094-124">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="11094-124">-VaultName</span></span>
<span data-ttu-id="11094-125">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="11094-125">Vault name.</span></span>
<span data-ttu-id="11094-126">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="11094-126">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="11094-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11094-127">CommonParameters</span></span>
<span data-ttu-id="11094-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11094-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11094-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11094-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11094-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="11094-130">INPUTS</span></span>

### <span data-ttu-id="11094-131">System. String</span><span class="sxs-lookup"><span data-stu-id="11094-131">System.String</span></span>

## <span data-ttu-id="11094-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="11094-132">OUTPUTS</span></span>

### <span data-ttu-id="11094-133">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. ManagedStorageSasDefinitionListItem, Microsoft. Azure. Commands. keyvault, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="11094-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinitionListItem, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="11094-134">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="11094-134">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="11094-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="11094-135">NOTES</span></span>

## <span data-ttu-id="11094-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11094-136">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

