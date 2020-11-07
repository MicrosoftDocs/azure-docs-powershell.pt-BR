---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 15e11e9deedbc8a2e442d9b3f006511a98fd6394
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775795"
---
# <span data-ttu-id="48fbe-101">Get-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="48fbe-101">Get-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="48fbe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48fbe-102">SYNOPSIS</span></span>
<span data-ttu-id="48fbe-103">Obtém definições de SAS de armazenamento gerenciado do Key Vault.</span><span class="sxs-lookup"><span data-stu-id="48fbe-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

## <span data-ttu-id="48fbe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48fbe-104">SYNTAX</span></span>

### <span data-ttu-id="48fbe-105">ByAccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="48fbe-105">ByAccountName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48fbe-106">ByDefinitionName</span><span class="sxs-lookup"><span data-stu-id="48fbe-106">ByDefinitionName</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48fbe-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="48fbe-107">DESCRIPTION</span></span>
<span data-ttu-id="48fbe-108">Obtém uma definição de SAS de armazenamento gerenciado de um cofre de chaves se o nome da definição for especificado.</span><span class="sxs-lookup"><span data-stu-id="48fbe-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="48fbe-109">Se o nome da definição não for especificado, todas as definições de SAS associadas à conta de armazenamento gerenciado do cofre de chaves especificado no cofre serão listadas.</span><span class="sxs-lookup"><span data-stu-id="48fbe-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="48fbe-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48fbe-110">EXAMPLES</span></span>

### <span data-ttu-id="48fbe-111">Exemplo 1: listar todas as definições de SAS de armazenamento gerenciado do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="48fbe-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="48fbe-112">Lista todas as definições de SAS associadas à conta de armazenamento gerenciado do Key Vault ' mystorageaccount ' gerenciada pelo cofre ' myvault '</span><span class="sxs-lookup"><span data-stu-id="48fbe-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="48fbe-113">Exemplo 2: obter uma conta de armazenamento gerenciado do Key Vault</span><span class="sxs-lookup"><span data-stu-id="48fbe-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasDef'
```

<span data-ttu-id="48fbe-114">Obtém os detalhes da definição de SAS ' mysasDef ' associada à conta de armazenamento gerenciado do Key Vault ' mystorageaccount ' gerenciada pelo cofre ' myvault '.</span><span class="sxs-lookup"><span data-stu-id="48fbe-114">Gets the details of SAS Definition 'mysasDef' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

## <span data-ttu-id="48fbe-115">OS</span><span class="sxs-lookup"><span data-stu-id="48fbe-115">PARAMETERS</span></span>

### <span data-ttu-id="48fbe-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="48fbe-116">-AccountName</span></span>
<span data-ttu-id="48fbe-117">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="48fbe-117">Vault name.</span></span>
<span data-ttu-id="48fbe-118">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="48fbe-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="48fbe-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48fbe-119">-DefaultProfile</span></span>
<span data-ttu-id="48fbe-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="48fbe-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48fbe-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="48fbe-121">-Name</span></span>
<span data-ttu-id="48fbe-122">Nome da definição de SAS de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="48fbe-122">Storage sas definition name.</span></span>
<span data-ttu-id="48fbe-123">O cmdlet constrói o FQDN de uma definição de SAS de armazenamento do nome do cofre, ambiente selecionado atualmente, nome da conta de armazenamento e nome da definição da SAS.</span><span class="sxs-lookup"><span data-stu-id="48fbe-123">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="48fbe-124">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="48fbe-124">-VaultName</span></span>
<span data-ttu-id="48fbe-125">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="48fbe-125">Vault name.</span></span>
<span data-ttu-id="48fbe-126">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="48fbe-126">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="48fbe-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48fbe-127">CommonParameters</span></span>
<span data-ttu-id="48fbe-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48fbe-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48fbe-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48fbe-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48fbe-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="48fbe-130">INPUTS</span></span>

### <span data-ttu-id="48fbe-131">System. String</span><span class="sxs-lookup"><span data-stu-id="48fbe-131">System.String</span></span>

## <span data-ttu-id="48fbe-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="48fbe-132">OUTPUTS</span></span>

### <span data-ttu-id="48fbe-133">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. ManagedStorageSasDefinitionListItem, Microsoft. Azure. Commands. keyvault, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="48fbe-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinitionListItem, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="48fbe-134">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="48fbe-134">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="48fbe-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="48fbe-135">NOTES</span></span>

## <span data-ttu-id="48fbe-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48fbe-136">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

