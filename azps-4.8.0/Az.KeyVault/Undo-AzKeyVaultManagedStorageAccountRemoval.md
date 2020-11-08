---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstorageaccountremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
ms.openlocfilehash: 3d854d6b820f6c2e23d99e3397173ec45d5b7697
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111876"
---
# <span data-ttu-id="04643-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="04643-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span></span>

## <span data-ttu-id="04643-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04643-102">SYNOPSIS</span></span>
<span data-ttu-id="04643-103">Recupera uma conta de armazenamento gerenciado anteriormente excluída do keyvault.</span><span class="sxs-lookup"><span data-stu-id="04643-103">Recovers a previously deleted KeyVault-managed storage account.</span></span>

## <span data-ttu-id="04643-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04643-104">SYNTAX</span></span>

### <span data-ttu-id="04643-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="04643-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04643-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="04643-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-InputObject] <PSDeletedKeyVaultManagedStorageAccountIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04643-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04643-107">DESCRIPTION</span></span>
<span data-ttu-id="04643-108">O comando **Undo-AzKeyVaultManagedStorageAccountRemoval** recupera uma conta de armazenamento gerenciado anteriormente excluída, desde que a exclusão suave esteja habilitada para esse cofre e que a tentativa de recuperação ocorra durante o intervalo de recuperação.</span><span class="sxs-lookup"><span data-stu-id="04643-108">The **Undo-AzKeyVaultManagedStorageAccountRemoval** command recovers a previously deleted managed storage account, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="04643-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04643-109">EXAMPLES</span></span>

### <span data-ttu-id="04643-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="04643-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName myVault -Name myAccount -InRemovedState
PS C:\> Undo-AzKeyVaultManagedStorageAccountRemoval -VaultName myVault -Name myAccount

Id                  : https://myvault.vault.azure.net:443/storage/myaccount
Vault Name          : myVault
AccountName         : myAccount
Account Resource Id : /subscriptions/8bc48661-1801-4b7a-8ca1-6a3cadfb4870/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/myaccount
Active Key Name     : key2
Auto Regenerate Key : False
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="04643-111">Essa sequência de comandos determina se a conta de armazenamento especificada existe no cofre em um estado excluído; o comando subsequente recupera a conta de armazenamento excluída, trazendo-a de volta para um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="04643-111">This sequence of commands determines whether the specified storage account exists in the vault in a deleted state; the subsequent command recovers the deleted storage account, bringing it back into an active state.</span></span>

## <span data-ttu-id="04643-112">OS</span><span class="sxs-lookup"><span data-stu-id="04643-112">PARAMETERS</span></span>

### <span data-ttu-id="04643-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04643-113">-DefaultProfile</span></span>
<span data-ttu-id="04643-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04643-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04643-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04643-115">-InputObject</span></span>
<span data-ttu-id="04643-116">Objeto da conta de armazenamento gerenciado excluído</span><span class="sxs-lookup"><span data-stu-id="04643-116">Deleted Managed Storage Account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04643-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="04643-117">-Name</span></span>
<span data-ttu-id="04643-118">Nome da conta de armazenamento gerenciado do keyvault.</span><span class="sxs-lookup"><span data-stu-id="04643-118">Name of the KeyVault managed storage account.</span></span>
<span data-ttu-id="04643-119">O cmdlet constrói o FQDN do destino do nome do cofre, o ambiente selecionado no momento e o nome da conta de armazenamento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="04643-119">Cmdlet constructs the FQDN of the target from vault name, currently selected environment and the name of the managed storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04643-120">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="04643-120">-VaultName</span></span>
<span data-ttu-id="04643-121">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="04643-121">Vault name.</span></span>
<span data-ttu-id="04643-122">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="04643-122">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04643-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="04643-123">-Confirm</span></span>
<span data-ttu-id="04643-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04643-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04643-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04643-125">-WhatIf</span></span>
<span data-ttu-id="04643-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="04643-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04643-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="04643-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04643-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04643-128">CommonParameters</span></span>
<span data-ttu-id="04643-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04643-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04643-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04643-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04643-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04643-131">INPUTS</span></span>

### <span data-ttu-id="04643-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="04643-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="04643-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04643-133">OUTPUTS</span></span>

### <span data-ttu-id="04643-134">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04643-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="04643-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04643-135">NOTES</span></span>

## <span data-ttu-id="04643-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04643-136">RELATED LINKS</span></span>
