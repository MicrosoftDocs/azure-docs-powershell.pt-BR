---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultmanagedstoragesasdefinitionremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
ms.openlocfilehash: a8f90c2314ad645a8de3a72abc92928759e3b828
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886476"
---
# <span data-ttu-id="8c67a-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span><span class="sxs-lookup"><span data-stu-id="8c67a-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span></span>

## <span data-ttu-id="8c67a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c67a-102">SYNOPSIS</span></span>
<span data-ttu-id="8c67a-103">Recupera uma definição de SAS de armazenamento gerenciado por KeyVault excluída anteriormente.</span><span class="sxs-lookup"><span data-stu-id="8c67a-103">Recovers a previously deleted KeyVault-managed storage SAS definition.</span></span>

## <span data-ttu-id="8c67a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8c67a-104">SYNTAX</span></span>

### <span data-ttu-id="8c67a-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8c67a-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-VaultName] <String> [-AccountName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c67a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8c67a-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-AccountName] <String>
 [-InputObject] <PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c67a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8c67a-107">DESCRIPTION</span></span>
<span data-ttu-id="8c67a-108">O comando **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** recupera uma definição de SAS de armazenamento gerenciado excluída anteriormente, desde que a exclusão suave seja habilitada para esse cofre e que a tentativa de recuperação ocorra durante o intervalo de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8c67a-108">The **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** command recovers a previously deleted managed storage SAS definition, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="8c67a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c67a-109">EXAMPLES</span></span>

### <span data-ttu-id="8c67a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8c67a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName myVault -AccountName myAccount -Name mySasName -InRemovedState
PS C:\> Undo-AzKeyVaultManagedStorageSasDefinitionRemoval -VaultName myVault -AccountName myAccount -Name mySasName

Id          : https://myvault.vault.azure.net:443/storage/myaccount/sas/mysasname
Secret Id   : https://myvault.vault.azure.net/secrets/myaccount-mysasname
Vault Name  : myVault
AccountName : myAccount
Name        : mySasName
Parameter   :
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="8c67a-111">Essa sequência de comandos determina se a definição do SAS de armazenamento especificado existe no cofre em um estado excluído; o comando subsequente recupera a definição de sas excluída, trazendo-a de volta para um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="8c67a-111">This sequence of commands determines whether the specified storage SAS definition exists in the vault in a deleted state; the subsequent command recovers the deleted sas definition, bringing it back into an active state.</span></span>

## <span data-ttu-id="8c67a-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8c67a-112">PARAMETERS</span></span>

### <span data-ttu-id="8c67a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8c67a-113">-AccountName</span></span>
<span data-ttu-id="8c67a-114">Nome da conta de armazenamento gerenciado por KeyVault.</span><span class="sxs-lookup"><span data-stu-id="8c67a-114">KeyVault-managed storage account name.</span></span>
<span data-ttu-id="8c67a-115">O cmdlet constrói o FQDN de uma definição de SAS de armazenamento gerenciado a partir do nome do cofre, do ambiente selecionado no momento e do nome da conta de armazenamento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="8c67a-115">Cmdlet constructs the FQDN of a managed storage SAS definition from vault name, currently-selected environment and managed storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c67a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c67a-116">-DefaultProfile</span></span>
<span data-ttu-id="8c67a-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8c67a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c67a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c67a-118">-InputObject</span></span>
<span data-ttu-id="8c67a-119">Objeto de definição de SAS de armazenamento gerenciado excluído</span><span class="sxs-lookup"><span data-stu-id="8c67a-119">Deleted managed storage SAS definition object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c67a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8c67a-120">-Name</span></span>
<span data-ttu-id="8c67a-121">Nome da definição do SAS de armazenamento gerenciado por KeyVault.</span><span class="sxs-lookup"><span data-stu-id="8c67a-121">Name of the KeyVault-managed storage SAS definition.</span></span>
<span data-ttu-id="8c67a-122">O cmdlet constrói o FQDN do destino a partir do nome do cofre, do ambiente selecionado no momento, do nome da conta de armazenamento gerenciado e do nome da definição do SAS.</span><span class="sxs-lookup"><span data-stu-id="8c67a-122">Cmdlet constructs the FQDN of the target from vault name, currently-selected environment, the name of the managed storage account and the name of the SAS definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c67a-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8c67a-123">-VaultName</span></span>
<span data-ttu-id="8c67a-124">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="8c67a-124">Vault name.</span></span>
<span data-ttu-id="8c67a-125">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="8c67a-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="8c67a-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c67a-126">-Confirm</span></span>
<span data-ttu-id="8c67a-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c67a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c67a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c67a-128">-WhatIf</span></span>
<span data-ttu-id="8c67a-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8c67a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c67a-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8c67a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c67a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c67a-131">CommonParameters</span></span>
<span data-ttu-id="8c67a-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c67a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c67a-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c67a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c67a-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c67a-134">INPUTS</span></span>

### <span data-ttu-id="8c67a-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8c67a-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="8c67a-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8c67a-136">OUTPUTS</span></span>

### <span data-ttu-id="8c67a-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="8c67a-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="8c67a-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="8c67a-138">NOTES</span></span>

## <span data-ttu-id="8c67a-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c67a-139">RELATED LINKS</span></span>
