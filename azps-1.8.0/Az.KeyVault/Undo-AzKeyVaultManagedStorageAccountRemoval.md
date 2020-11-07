---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstorageaccountremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
ms.openlocfilehash: 642c5ff36fb0647907cf72218bd626bcdafe19ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770593"
---
# <span data-ttu-id="37cf3-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="37cf3-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span></span>

## <span data-ttu-id="37cf3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="37cf3-102">SYNOPSIS</span></span>
<span data-ttu-id="37cf3-103">Recupera uma conta de armazenamento gerenciado anteriormente excluída do keyvault.</span><span class="sxs-lookup"><span data-stu-id="37cf3-103">Recovers a previously deleted KeyVault-managed storage account.</span></span>

## <span data-ttu-id="37cf3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37cf3-104">SYNTAX</span></span>

### <span data-ttu-id="37cf3-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="37cf3-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37cf3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="37cf3-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-InputObject] <PSDeletedKeyVaultManagedStorageAccountIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37cf3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="37cf3-107">DESCRIPTION</span></span>
<span data-ttu-id="37cf3-108">O comando **Undo-AzKeyVaultManagedStorageAccountRemoval** recupera uma conta de armazenamento gerenciado anteriormente excluída, desde que a exclusão suave esteja habilitada para esse cofre e que a tentativa de recuperação ocorra durante o intervalo de recuperação.</span><span class="sxs-lookup"><span data-stu-id="37cf3-108">The **Undo-AzKeyVaultManagedStorageAccountRemoval** command recovers a previously deleted managed storage account, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="37cf3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="37cf3-109">EXAMPLES</span></span>

### <span data-ttu-id="37cf3-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="37cf3-110">Example 1</span></span>
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

<span data-ttu-id="37cf3-111">Essa sequência de comandos determina se a conta de armazenamento especificada existe no cofre em um estado excluído; o comando subsequente recupera a conta de armazenamento excluída, trazendo-a de volta para um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="37cf3-111">This sequence of commands determines whether the specified storage account exists in the vault in a deleted state; the subsequent command recovers the deleted storage account, bringing it back into an active state.</span></span>

## <span data-ttu-id="37cf3-112">OS</span><span class="sxs-lookup"><span data-stu-id="37cf3-112">PARAMETERS</span></span>

### <span data-ttu-id="37cf3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37cf3-113">-DefaultProfile</span></span>
<span data-ttu-id="37cf3-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="37cf3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37cf3-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37cf3-115">-InputObject</span></span>
<span data-ttu-id="37cf3-116">Objeto da conta de armazenamento gerenciado excluído</span><span class="sxs-lookup"><span data-stu-id="37cf3-116">Deleted Managed Storage Account object</span></span>

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

### <span data-ttu-id="37cf3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="37cf3-117">-Name</span></span>
<span data-ttu-id="37cf3-118">Nome da conta de armazenamento gerenciado do keyvault.</span><span class="sxs-lookup"><span data-stu-id="37cf3-118">Name of the KeyVault managed storage account.</span></span>
<span data-ttu-id="37cf3-119">O cmdlet constrói o FQDN do destino do nome do cofre, o ambiente selecionado no momento e o nome da conta de armazenamento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="37cf3-119">Cmdlet constructs the FQDN of the target from vault name, currently selected environment and the name of the managed storage account.</span></span>

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

### <span data-ttu-id="37cf3-120">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="37cf3-120">-VaultName</span></span>
<span data-ttu-id="37cf3-121">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="37cf3-121">Vault name.</span></span>
<span data-ttu-id="37cf3-122">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="37cf3-122">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="37cf3-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="37cf3-123">-Confirm</span></span>
<span data-ttu-id="37cf3-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37cf3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37cf3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37cf3-125">-WhatIf</span></span>
<span data-ttu-id="37cf3-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="37cf3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37cf3-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="37cf3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37cf3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37cf3-128">CommonParameters</span></span>
<span data-ttu-id="37cf3-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37cf3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37cf3-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37cf3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37cf3-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="37cf3-131">INPUTS</span></span>

### <span data-ttu-id="37cf3-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="37cf3-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="37cf3-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="37cf3-133">OUTPUTS</span></span>

### <span data-ttu-id="37cf3-134">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37cf3-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="37cf3-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="37cf3-135">NOTES</span></span>

## <span data-ttu-id="37cf3-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37cf3-136">RELATED LINKS</span></span>
