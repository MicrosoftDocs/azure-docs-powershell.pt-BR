---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 70ee1aaf9fb082819c626c43ba5c08ad01f0f1d6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776668"
---
# <span data-ttu-id="fa12e-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fa12e-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="fa12e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fa12e-102">SYNOPSIS</span></span>
<span data-ttu-id="fa12e-103">Obtém contas de armazenamento do Azure gerenciadas do Key Vault.</span><span class="sxs-lookup"><span data-stu-id="fa12e-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="fa12e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa12e-104">SYNTAX</span></span>

### <span data-ttu-id="fa12e-105">ByVaultName (padrão)</span><span class="sxs-lookup"><span data-stu-id="fa12e-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fa12e-106">ByAccountName</span><span class="sxs-lookup"><span data-stu-id="fa12e-106">ByAccountName</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa12e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fa12e-107">DESCRIPTION</span></span>
<span data-ttu-id="fa12e-108">Obtém uma conta de armazenamento gerenciada do Key Vault, se o nome da conta for especificado e as chaves da conta forem gerenciadas pelo cofre especificado.</span><span class="sxs-lookup"><span data-stu-id="fa12e-108">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="fa12e-109">Se o nome da conta não for especificado, todas as contas cujas chaves são gerenciadas pelo cofre especificado são listadas.</span><span class="sxs-lookup"><span data-stu-id="fa12e-109">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="fa12e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa12e-110">EXAMPLES</span></span>

### <span data-ttu-id="fa12e-111">Exemplo 1: lista todas as contas de armazenamento gerenciado do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="fa12e-111">Example 1: List all Key Vault managed Storage Accounts</span></span>
```
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault'
```

<span data-ttu-id="fa12e-112">Lista todas as contas cujas chaves são gerenciadas pelo cofre ' myvault '</span><span class="sxs-lookup"><span data-stu-id="fa12e-112">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="fa12e-113">Exemplo 2: obter uma conta de armazenamento gerenciado do Key Vault</span><span class="sxs-lookup"><span data-stu-id="fa12e-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'
```

<span data-ttu-id="fa12e-114">Obtém os detalhes da conta de armazenamento gerenciado do Key Vault de ' mystorageaccount ' se suas chaves forem gerenciadas pelo cofre ' myvault '</span><span class="sxs-lookup"><span data-stu-id="fa12e-114">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

## <span data-ttu-id="fa12e-115">OS</span><span class="sxs-lookup"><span data-stu-id="fa12e-115">PARAMETERS</span></span>

### <span data-ttu-id="fa12e-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fa12e-116">-AccountName</span></span>
<span data-ttu-id="fa12e-117">Nome da conta de armazenamento gerenciado do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="fa12e-117">Key Vault managed storage account name.</span></span> <span data-ttu-id="fa12e-118">O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, ambiente selecionado atualmente e nome da conta de armazenamento gerenciada.</span><span class="sxs-lookup"><span data-stu-id="fa12e-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa12e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa12e-119">-DefaultProfile</span></span>
<span data-ttu-id="fa12e-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fa12e-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa12e-121">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="fa12e-121">-VaultName</span></span>
<span data-ttu-id="fa12e-122">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="fa12e-122">Vault name.</span></span>
<span data-ttu-id="fa12e-123">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="fa12e-123">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="fa12e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa12e-124">CommonParameters</span></span>
<span data-ttu-id="fa12e-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa12e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa12e-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa12e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa12e-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fa12e-127">INPUTS</span></span>

### <span data-ttu-id="fa12e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fa12e-128">System.String</span></span>

## <span data-ttu-id="fa12e-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fa12e-129">OUTPUTS</span></span>

### <span data-ttu-id="fa12e-130">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount, Microsoft. Azure. Commands. keyvault, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fa12e-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="fa12e-131">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fa12e-131">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="fa12e-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fa12e-132">NOTES</span></span>

## <span data-ttu-id="fa12e-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa12e-133">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

