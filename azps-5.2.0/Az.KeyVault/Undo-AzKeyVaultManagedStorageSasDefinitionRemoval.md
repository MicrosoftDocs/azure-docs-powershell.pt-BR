---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstoragesasdefinitionremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
ms.openlocfilehash: bb44bc8f5e4537691d1e5d5493a29111ceaf42a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258550"
---
# <span data-ttu-id="fd802-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span><span class="sxs-lookup"><span data-stu-id="fd802-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span></span>

## <span data-ttu-id="fd802-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd802-102">SYNOPSIS</span></span>
<span data-ttu-id="fd802-103">Recupera uma definição de SAS de armazenamento gerenciado anteriormente excluída do keyvault.</span><span class="sxs-lookup"><span data-stu-id="fd802-103">Recovers a previously deleted KeyVault-managed storage SAS definition.</span></span>

## <span data-ttu-id="fd802-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd802-104">SYNTAX</span></span>

### <span data-ttu-id="fd802-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="fd802-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-VaultName] <String> [-AccountName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd802-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fd802-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-AccountName] <String>
 [-InputObject] <PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd802-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fd802-107">DESCRIPTION</span></span>
<span data-ttu-id="fd802-108">O comando **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** recupera uma definição de SAS de armazenamento gerenciado anteriormente excluída, desde que a exclusão suave esteja habilitada para esse cofre e que a tentativa de recuperação ocorra durante o intervalo de recuperação.</span><span class="sxs-lookup"><span data-stu-id="fd802-108">The **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** command recovers a previously deleted managed storage SAS definition, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="fd802-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd802-109">EXAMPLES</span></span>

### <span data-ttu-id="fd802-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fd802-110">Example 1</span></span>
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

<span data-ttu-id="fd802-111">Essa sequência de comandos determina se a definição de SAS de armazenamento especificada existe no cofre em um estado excluído; o comando subsequente recupera a definição de SAS excluída, trazendo-a de volta para um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="fd802-111">This sequence of commands determines whether the specified storage SAS definition exists in the vault in a deleted state; the subsequent command recovers the deleted sas definition, bringing it back into an active state.</span></span>

## <span data-ttu-id="fd802-112">OS</span><span class="sxs-lookup"><span data-stu-id="fd802-112">PARAMETERS</span></span>

### <span data-ttu-id="fd802-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fd802-113">-AccountName</span></span>
<span data-ttu-id="fd802-114">Keyvault-nome da conta de armazenamento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="fd802-114">KeyVault-managed storage account name.</span></span>
<span data-ttu-id="fd802-115">O cmdlet cria um FQDN de uma definição de SAS de armazenamento gerenciado a partir do nome do cofre, ambiente selecionado atualmente e nome da conta de armazenamento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="fd802-115">Cmdlet constructs the FQDN of a managed storage SAS definition from vault name, currently-selected environment and managed storage account name.</span></span>

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

### <span data-ttu-id="fd802-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd802-116">-DefaultProfile</span></span>
<span data-ttu-id="fd802-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fd802-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd802-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd802-118">-InputObject</span></span>
<span data-ttu-id="fd802-119">Objeto de definição SAS de armazenamento gerenciado excluído</span><span class="sxs-lookup"><span data-stu-id="fd802-119">Deleted managed storage SAS definition object</span></span>

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

### <span data-ttu-id="fd802-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd802-120">-Name</span></span>
<span data-ttu-id="fd802-121">Nome da definição de SAS de armazenamento gerenciado pelo keyvault.</span><span class="sxs-lookup"><span data-stu-id="fd802-121">Name of the KeyVault-managed storage SAS definition.</span></span>
<span data-ttu-id="fd802-122">O cmdlet constrói o FQDN do destino do nome do cofre, ambiente selecionado atualmente, o nome da conta de armazenamento gerenciado e o nome da definição de SAS.</span><span class="sxs-lookup"><span data-stu-id="fd802-122">Cmdlet constructs the FQDN of the target from vault name, currently-selected environment, the name of the managed storage account and the name of the SAS definition.</span></span>

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

### <span data-ttu-id="fd802-123">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="fd802-123">-VaultName</span></span>
<span data-ttu-id="fd802-124">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="fd802-124">Vault name.</span></span>
<span data-ttu-id="fd802-125">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="fd802-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="fd802-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fd802-126">-Confirm</span></span>
<span data-ttu-id="fd802-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd802-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd802-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd802-128">-WhatIf</span></span>
<span data-ttu-id="fd802-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fd802-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd802-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fd802-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd802-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd802-131">CommonParameters</span></span>
<span data-ttu-id="fd802-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd802-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd802-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd802-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd802-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fd802-134">INPUTS</span></span>

### <span data-ttu-id="fd802-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="fd802-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="fd802-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fd802-136">OUTPUTS</span></span>

### <span data-ttu-id="fd802-137">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="fd802-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="fd802-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fd802-138">NOTES</span></span>

## <span data-ttu-id="fd802-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd802-139">RELATED LINKS</span></span>
