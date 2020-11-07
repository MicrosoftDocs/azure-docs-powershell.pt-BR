---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccountkey
schema: 2.0.0
ms.openlocfilehash: d7bd1e776cc0593f57a17e8d83ecde3f6981973b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785745"
---
# <span data-ttu-id="e7ec3-101">Update-AzureKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e7ec3-101">Update-AzureKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="e7ec3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7ec3-102">SYNOPSIS</span></span>
<span data-ttu-id="e7ec3-103">Regenera a chave especificada da conta de armazenamento do Azure gerenciada do Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e7ec3-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7ec3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7ec3-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7ec3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7ec3-105">DESCRIPTION</span></span>
<span data-ttu-id="e7ec3-106">Regenera a chave especificada da conta de armazenamento do Azure gerenciada do Key Vault e define a chave como a chave ativa.</span><span class="sxs-lookup"><span data-stu-id="e7ec3-106">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="e7ec3-107">Os proxies do cofre de chaves chamam a chamada para o Azure Resource Manager para regenerar a chave.</span><span class="sxs-lookup"><span data-stu-id="e7ec3-107">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="e7ec3-108">O chamador deve possuem permissões para gerar novamente as chaves em uma determinada conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e7ec3-108">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="e7ec3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7ec3-109">EXAMPLES</span></span>

### <span data-ttu-id="e7ec3-110">Exemplo 1: regenerar uma chave</span><span class="sxs-lookup"><span data-stu-id="e7ec3-110">Example 1: Regenerate a key</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'
```

<span data-ttu-id="e7ec3-111">Gera novamente ' key1 ' da conta ' mystorageaccount ' e define ' key1 ' como o ativo da conta de armazenamento do Azure gerenciada do compartimento de chaves.</span><span class="sxs-lookup"><span data-stu-id="e7ec3-111">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="e7ec3-112">OS</span><span class="sxs-lookup"><span data-stu-id="e7ec3-112">PARAMETERS</span></span>

### <span data-ttu-id="e7ec3-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e7ec3-113">-AccountName</span></span>
<span data-ttu-id="e7ec3-114">Nome da conta de armazenamento gerenciado do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="e7ec3-114">Key Vault managed storage account name.</span></span> <span data-ttu-id="e7ec3-115">O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, ambiente selecionado atualmente e nome da conta de armazenamento gerenciada.</span><span class="sxs-lookup"><span data-stu-id="e7ec3-115">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="e7ec3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7ec3-116">-DefaultProfile</span></span>
<span data-ttu-id="e7ec3-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e7ec3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7ec3-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e7ec3-118">-Force</span></span>
<span data-ttu-id="e7ec3-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="e7ec3-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e7ec3-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e7ec3-120">-KeyName</span></span>
<span data-ttu-id="e7ec3-121">Nome da chave da conta de armazenamento para gerar novamente e ativar.</span><span class="sxs-lookup"><span data-stu-id="e7ec3-121">Name of storage account key to regenerate and make active.</span></span>

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

### <span data-ttu-id="e7ec3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7ec3-122">-PassThru</span></span>
<span data-ttu-id="e7ec3-123">O cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="e7ec3-123">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e7ec3-124">Se essa opção for especificada, o cmdlet retornará a conta de armazenamento gerenciada que foi excluída.</span><span class="sxs-lookup"><span data-stu-id="e7ec3-124">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="e7ec3-125">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="e7ec3-125">-VaultName</span></span>
<span data-ttu-id="e7ec3-126">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="e7ec3-126">Vault name.</span></span>
<span data-ttu-id="e7ec3-127">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="e7ec3-127">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="e7ec3-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e7ec3-128">-Confirm</span></span>
<span data-ttu-id="e7ec3-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7ec3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7ec3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7ec3-130">-WhatIf</span></span>
<span data-ttu-id="e7ec3-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e7ec3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7ec3-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e7ec3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7ec3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7ec3-133">CommonParameters</span></span>
<span data-ttu-id="e7ec3-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7ec3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7ec3-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7ec3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7ec3-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7ec3-136">INPUTS</span></span>

### <span data-ttu-id="e7ec3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e7ec3-137">System.String</span></span>

## <span data-ttu-id="e7ec3-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7ec3-138">OUTPUTS</span></span>

### <span data-ttu-id="e7ec3-139">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e7ec3-139">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="e7ec3-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7ec3-140">NOTES</span></span>

## <span data-ttu-id="e7ec3-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7ec3-141">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

