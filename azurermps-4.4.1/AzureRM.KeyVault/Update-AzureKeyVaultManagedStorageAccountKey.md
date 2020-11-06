---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: 94e1b297879e31ff42f9c12c0e4ad4a601e5e163
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433104"
---
# <span data-ttu-id="0b6ac-101">Update-AzureKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0b6ac-101">Update-AzureKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="0b6ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b6ac-102">SYNOPSIS</span></span>
<span data-ttu-id="0b6ac-103">Regenera a chave especificada da conta de armazenamento do Azure gerenciada do Key Vault.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b6ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b6ac-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b6ac-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b6ac-105">DESCRIPTION</span></span>
<span data-ttu-id="0b6ac-106">Regenera a chave especificada da conta de armazenamento do Azure gerenciada do Key Vault e define a chave como a chave ativa.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-106">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="0b6ac-107">Os proxies do cofre de chaves chamam a chamada para o Azure Resource Manager para regenerar a chave.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-107">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="0b6ac-108">O chamador deve possuem permissões para gerar novamente as chaves em uma determinada conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-108">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="0b6ac-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b6ac-109">EXAMPLES</span></span>

### <span data-ttu-id="0b6ac-110">Exemplo 1: regenerar uma chave</span><span class="sxs-lookup"><span data-stu-id="0b6ac-110">Example 1: Regenerate a key</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'
```

<span data-ttu-id="0b6ac-111">Gera novamente ' key1 ' da conta ' mystorageaccount ' e define ' key1 ' como o ativo da conta de armazenamento do Azure gerenciada do compartimento de chaves.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-111">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="0b6ac-112">OS</span><span class="sxs-lookup"><span data-stu-id="0b6ac-112">PARAMETERS</span></span>

### <span data-ttu-id="0b6ac-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0b6ac-113">-AccountName</span></span>
<span data-ttu-id="0b6ac-114">Nome da conta de armazenamento gerenciado do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-114">Key Vault managed storage account name.</span></span> <span data-ttu-id="0b6ac-115">O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, ambiente selecionado atualmente e nome da conta de armazenamento gerenciada.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-115">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b6ac-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0b6ac-116">-Force</span></span>
<span data-ttu-id="0b6ac-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0b6ac-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="0b6ac-118">-KeyName</span></span>
<span data-ttu-id="0b6ac-119">Nome da chave da conta de armazenamento para gerar novamente e ativar.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-119">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b6ac-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b6ac-120">-PassThru</span></span>
<span data-ttu-id="0b6ac-121">O cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-121">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="0b6ac-122">Se essa opção for especificada, o cmdlet retornará a conta de armazenamento gerenciada que foi excluída.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-122">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="0b6ac-123">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="0b6ac-123">-VaultName</span></span>
<span data-ttu-id="0b6ac-124">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-124">Vault name.</span></span>
<span data-ttu-id="0b6ac-125">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="0b6ac-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0b6ac-126">-Confirm</span></span>
<span data-ttu-id="0b6ac-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b6ac-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b6ac-128">-WhatIf</span></span>
<span data-ttu-id="0b6ac-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b6ac-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b6ac-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b6ac-131">-DefaultProfile</span></span>
<span data-ttu-id="0b6ac-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b6ac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b6ac-133">CommonParameters</span></span>
<span data-ttu-id="0b6ac-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b6ac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b6ac-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b6ac-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b6ac-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b6ac-136">INPUTS</span></span>

### <span data-ttu-id="0b6ac-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0b6ac-137">System.String</span></span>

## <span data-ttu-id="0b6ac-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b6ac-138">OUTPUTS</span></span>

### <span data-ttu-id="0b6ac-139">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b6ac-139">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="0b6ac-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b6ac-140">NOTES</span></span>

## <span data-ttu-id="0b6ac-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b6ac-141">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

