---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/update-AzKeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: d73e9b02940f98db6734f851219399a2ba6c74a2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776635"
---
# <span data-ttu-id="63b0c-101">Update-AzKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="63b0c-101">Update-AzKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="63b0c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="63b0c-103">Regenera a chave especificada da conta de armazenamento do Azure gerenciada do Key Vault.</span><span class="sxs-lookup"><span data-stu-id="63b0c-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="63b0c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63b0c-104">SYNTAX</span></span>

```
Update-AzKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63b0c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="63b0c-105">DESCRIPTION</span></span>
<span data-ttu-id="63b0c-106">Regenera a chave especificada da conta de armazenamento do Azure gerenciada do Key Vault e define a chave como a chave ativa.</span><span class="sxs-lookup"><span data-stu-id="63b0c-106">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="63b0c-107">Os proxies do cofre de chaves chamam a chamada para o Azure Resource Manager para regenerar a chave.</span><span class="sxs-lookup"><span data-stu-id="63b0c-107">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="63b0c-108">O chamador deve possuem permissões para gerar novamente as chaves em uma determinada conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="63b0c-108">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="63b0c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63b0c-109">EXAMPLES</span></span>

### <span data-ttu-id="63b0c-110">Exemplo 1: regenerar uma chave</span><span class="sxs-lookup"><span data-stu-id="63b0c-110">Example 1: Regenerate a key</span></span>
```
PS C:\> Update-AzKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'
```

<span data-ttu-id="63b0c-111">Gera novamente ' key1 ' da conta ' mystorageaccount ' e define ' key1 ' como o ativo da conta de armazenamento do Azure gerenciada do compartimento de chaves.</span><span class="sxs-lookup"><span data-stu-id="63b0c-111">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="63b0c-112">OS</span><span class="sxs-lookup"><span data-stu-id="63b0c-112">PARAMETERS</span></span>

### <span data-ttu-id="63b0c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="63b0c-113">-AccountName</span></span>
<span data-ttu-id="63b0c-114">Nome da conta de armazenamento gerenciado do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="63b0c-114">Key Vault managed storage account name.</span></span> <span data-ttu-id="63b0c-115">O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, ambiente selecionado atualmente e nome da conta de armazenamento gerenciada.</span><span class="sxs-lookup"><span data-stu-id="63b0c-115">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="63b0c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63b0c-116">-DefaultProfile</span></span>
<span data-ttu-id="63b0c-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="63b0c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63b0c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="63b0c-118">-Force</span></span>
<span data-ttu-id="63b0c-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="63b0c-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="63b0c-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="63b0c-120">-KeyName</span></span>
<span data-ttu-id="63b0c-121">Nome da chave da conta de armazenamento para gerar novamente e ativar.</span><span class="sxs-lookup"><span data-stu-id="63b0c-121">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63b0c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63b0c-122">-PassThru</span></span>
<span data-ttu-id="63b0c-123">O cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="63b0c-123">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="63b0c-124">Se essa opção for especificada, o cmdlet retornará a conta de armazenamento gerenciada que foi excluída.</span><span class="sxs-lookup"><span data-stu-id="63b0c-124">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="63b0c-125">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="63b0c-125">-VaultName</span></span>
<span data-ttu-id="63b0c-126">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="63b0c-126">Vault name.</span></span>
<span data-ttu-id="63b0c-127">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="63b0c-127">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="63b0c-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="63b0c-128">-Confirm</span></span>
<span data-ttu-id="63b0c-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63b0c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63b0c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63b0c-130">-WhatIf</span></span>
<span data-ttu-id="63b0c-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="63b0c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63b0c-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="63b0c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63b0c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63b0c-133">CommonParameters</span></span>
<span data-ttu-id="63b0c-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63b0c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63b0c-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63b0c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63b0c-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="63b0c-136">INPUTS</span></span>

### <span data-ttu-id="63b0c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="63b0c-137">System.String</span></span>

## <span data-ttu-id="63b0c-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="63b0c-138">OUTPUTS</span></span>

### <span data-ttu-id="63b0c-139">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="63b0c-139">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="63b0c-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="63b0c-140">NOTES</span></span>

## <span data-ttu-id="63b0c-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63b0c-141">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

