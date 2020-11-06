---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 1520acb94ffe587fb96eaa9c2ba565bcf31cc87e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440399"
---
# <span data-ttu-id="2e956-101">Backup-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2e956-101">Backup-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="2e956-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e956-102">SYNOPSIS</span></span>
<span data-ttu-id="2e956-103">Faz backup de uma conta de armazenamento gerenciado pelo keyvault.</span><span class="sxs-lookup"><span data-stu-id="2e956-103">Backs up a KeyVault-managed storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e956-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e956-104">SYNTAX</span></span>

### <span data-ttu-id="2e956-105">ByStorageAccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="2e956-105">ByStorageAccountName (Default)</span></span>
```
Backup-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e956-106">ByStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2e956-106">ByStorageAccount</span></span>
```
Backup-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e956-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e956-107">DESCRIPTION</span></span>
<span data-ttu-id="2e956-108">O cmdlet **backup-AzureKeyVaultManagedStorageAccount** faz a cópia de uma conta de armazenamento gerenciada especificada em um cofre, baixando-a e armazenando-a em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="2e956-108">The **Backup-AzureKeyVaultManagedStorageAccount** cmdlet backs up a specified managed storage account in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="2e956-109">Como o conteúdo baixado é criptografado, ele não pode ser usado fora do cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="2e956-109">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="2e956-110">Você pode restaurar uma conta de armazenamento com backup em qualquer cofre de chaves na assinatura do qual tenha sido feito o backup, desde que o cofre esteja na mesma Geografia do Azure.</span><span class="sxs-lookup"><span data-stu-id="2e956-110">You can restore a backed-up storage account to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="2e956-111">Os motivos típicos para usar este cmdlet são:</span><span class="sxs-lookup"><span data-stu-id="2e956-111">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="2e956-112">Você deseja manter uma cópia offline da conta de armazenamento, caso você exclua acidentalmente o original do cofre.</span><span class="sxs-lookup"><span data-stu-id="2e956-112">You want to retain an offline copy of the storage account in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="2e956-113">Você criou uma conta de armazenamento gerenciado usando o Key Vault e agora deseja clonar o objeto para uma região diferente do Azure, de modo que você possa usá-lo em todas as instâncias do seu aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="2e956-113">You created a managed storage account using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="2e956-114">Use o cmdlet **backup-AzureKeyVaultManagedStorageAccount** para recuperar a conta de armazenamento gerenciado em formato criptografado e, em seguida, use o cmdlet **Restore-AzureKeyVaultManagedStorageAccount** e especifique um cofre de chaves na segunda região.</span><span class="sxs-lookup"><span data-stu-id="2e956-114">Use the **Backup-AzureKeyVaultManagedStorageAccount** cmdlet to retrieve the managed storage account in encrypted format and then use the **Restore-AzureKeyVaultManagedStorageAccount** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="2e956-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e956-115">EXAMPLES</span></span>

### <span data-ttu-id="2e956-116">Exemplo 1: fazer backup de uma conta de armazenamento gerenciado com um nome de arquivo gerado automaticamente</span><span class="sxs-lookup"><span data-stu-id="2e956-116">Example 1: Back up a managed storage account with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

<span data-ttu-id="2e956-117">Esse comando recupera a conta de armazenamento gerenciado chamada MyMSAK do cofre de chaves chamado MyKeyVault e salva um backup dessa conta de armazenamento gerenciado em um arquivo que é automaticamente nomeado para você e exibe o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2e956-117">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="2e956-118">Exemplo 2: fazer backup de uma conta de armazenamento gerenciado para um nome de arquivo especificado</span><span class="sxs-lookup"><span data-stu-id="2e956-118">Example 2: Back up a managed storage account to a specified file name</span></span>
```powershell
PS C:\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="2e956-119">Esse comando recupera a conta de armazenamento gerenciado chamada MyMSAK do cofre de chaves chamado MyKeyVault e salva um backup dessa conta de armazenamento gerenciado em um arquivo chamado backup. blob.</span><span class="sxs-lookup"><span data-stu-id="2e956-119">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file named Backup.blob.</span></span>

### <span data-ttu-id="2e956-120">Exemplo 3: fazer backup de uma conta de armazenamento gerenciado anteriormente recuperada para um nome de arquivo especificado, substituindo o arquivo de destino sem solicitação.</span><span class="sxs-lookup"><span data-stu-id="2e956-120">Example 3: Back up a previously retrieved managed storage account to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $msak = Get-AzureKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzureKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="2e956-121">Esse comando cria um backup da conta de armazenamento gerenciado chamada $msak. Nome no cofre chamado $msak. Compartimentalizaname para um arquivo chamado backup. blob, substituindo o arquivo silenciosamente se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="2e956-121">This command creates a backup of the managed storage account named $msak.Name in the vault named $msak.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="2e956-122">OS</span><span class="sxs-lookup"><span data-stu-id="2e956-122">PARAMETERS</span></span>

### <span data-ttu-id="2e956-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e956-123">-DefaultProfile</span></span>
<span data-ttu-id="2e956-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e956-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e956-125">-Force</span><span class="sxs-lookup"><span data-stu-id="2e956-125">-Force</span></span>
<span data-ttu-id="2e956-126">Substituir o arquivo fornecido se ele existir</span><span class="sxs-lookup"><span data-stu-id="2e956-126">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="2e956-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e956-127">-InputObject</span></span>
<span data-ttu-id="2e956-128">Pacote de conta de armazenamento para backup, em pipeline a partir da saída de uma chamada de recuperação.</span><span class="sxs-lookup"><span data-stu-id="2e956-128">Storage account bundle to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByStorageAccount
Aliases: StorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e956-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e956-129">-Name</span></span>
<span data-ttu-id="2e956-130">Nome do segredo.</span><span class="sxs-lookup"><span data-stu-id="2e956-130">Secret name.</span></span>
<span data-ttu-id="2e956-131">O cmdlet constrói o FQDN de um segredo do nome do cofre, do ambiente selecionado no momento e do nome do segredo.</span><span class="sxs-lookup"><span data-stu-id="2e956-131">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e956-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="2e956-132">-OutputFile</span></span>
<span data-ttu-id="2e956-133">Arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="2e956-133">Output file.</span></span>
<span data-ttu-id="2e956-134">O arquivo de saída para armazenar o backup da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2e956-134">The output file to store the storage account backup.</span></span>
<span data-ttu-id="2e956-135">Se não for especificado, um nome de arquivo padrão será gerado.</span><span class="sxs-lookup"><span data-stu-id="2e956-135">If not specified, a default filename will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e956-136">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="2e956-136">-VaultName</span></span>
<span data-ttu-id="2e956-137">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="2e956-137">Vault name.</span></span>
<span data-ttu-id="2e956-138">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="2e956-138">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e956-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2e956-139">-Confirm</span></span>
<span data-ttu-id="2e956-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e956-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e956-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e956-141">-WhatIf</span></span>
<span data-ttu-id="2e956-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2e956-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e956-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2e956-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e956-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e956-144">CommonParameters</span></span>
<span data-ttu-id="2e956-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e956-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e956-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e956-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e956-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e956-147">INPUTS</span></span>

### <span data-ttu-id="2e956-148">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="2e956-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="2e956-149">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2e956-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="2e956-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e956-150">OUTPUTS</span></span>

### <span data-ttu-id="2e956-151">System. String</span><span class="sxs-lookup"><span data-stu-id="2e956-151">System.String</span></span>

## <span data-ttu-id="2e956-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e956-152">NOTES</span></span>

## <span data-ttu-id="2e956-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e956-153">RELATED LINKS</span></span>
