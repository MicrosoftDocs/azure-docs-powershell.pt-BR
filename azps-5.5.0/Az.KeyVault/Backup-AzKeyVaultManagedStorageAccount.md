---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c01d07f9408804b229921394c24e444b2a4deb8b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117598"
---
# <span data-ttu-id="d233e-101">Backup-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d233e-101">Backup-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="d233e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d233e-102">SYNOPSIS</span></span>
<span data-ttu-id="d233e-103">Fazer o back up de uma conta de armazenamento gerenciada pelo KeyVault.</span><span class="sxs-lookup"><span data-stu-id="d233e-103">Backs up a KeyVault-managed storage account.</span></span>

## <span data-ttu-id="d233e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d233e-104">SYNTAX</span></span>

### <span data-ttu-id="d233e-105">ByStorageAccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d233e-105">ByStorageAccountName (Default)</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d233e-106">ByStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d233e-106">ByStorageAccount</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d233e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d233e-107">DESCRIPTION</span></span>
<span data-ttu-id="d233e-108">O cmdlet **Backup-AzKeyVaultManagedStorageAccount** faz backup de uma conta de armazenamento gerenciada especificada em um cofre de chave baixando-a e armazenado-a em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="d233e-108">The **Backup-AzKeyVaultManagedStorageAccount** cmdlet backs up a specified managed storage account in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="d233e-109">Como o conteúdo baixado é criptografado, ele não pode ser usado fora do Cofre de Teclas do Azure.</span><span class="sxs-lookup"><span data-stu-id="d233e-109">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="d233e-110">Você pode restaurar uma conta de armazenamento em backup em qualquer cofre de chave da assinatura da sua assinatura, desde que o cofre se mantenha na mesma geografia do Azure.</span><span class="sxs-lookup"><span data-stu-id="d233e-110">You can restore a backed-up storage account to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="d233e-111">Os motivos típicos para usar este cmdlet são:</span><span class="sxs-lookup"><span data-stu-id="d233e-111">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="d233e-112">Você deseja manter uma cópia offline da conta de armazenamento caso exclua acidentalmente o original do cofre.</span><span class="sxs-lookup"><span data-stu-id="d233e-112">You want to retain an offline copy of the storage account in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="d233e-113">Você criou uma conta de armazenamento gerenciado usando o Cofre de Teclas e agora deseja clonar o objeto em uma região diferente do Azure, para poder usá-lo em todas as instâncias do aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="d233e-113">You created a managed storage account using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="d233e-114">Use o cmdlet **Backup-AzKeyVaultManagedStorageAccount** para recuperar a conta de armazenamento gerenciado em formato criptografado e use o cmdlet **Restore-AzKeyVaultManagedStorageAccount** e especifique um cofre de chave na segunda região.</span><span class="sxs-lookup"><span data-stu-id="d233e-114">Use the **Backup-AzKeyVaultManagedStorageAccount** cmdlet to retrieve the managed storage account in encrypted format and then use the **Restore-AzKeyVaultManagedStorageAccount** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="d233e-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d233e-115">EXAMPLES</span></span>

### <span data-ttu-id="d233e-116">Exemplo 1: Fazer o back up de uma conta de armazenamento gerenciado com um nome de arquivo gerado automaticamente</span><span class="sxs-lookup"><span data-stu-id="d233e-116">Example 1: Back up a managed storage account with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

<span data-ttu-id="d233e-117">Esse comando recupera a conta de armazenamento gerenciada chamada MyMSAK do cofre de chave MyKeyVault e salva um backup dessa conta de armazenamento gerenciado em um arquivo que é nomeado automaticamente para você e exibe o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="d233e-117">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="d233e-118">Exemplo 2: Fazer o back up de uma conta de armazenamento gerenciada para um nome de arquivo especificado</span><span class="sxs-lookup"><span data-stu-id="d233e-118">Example 2: Back up a managed storage account to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="d233e-119">Esse comando recupera a conta de armazenamento gerenciada chamada MyMSAK do cofre de chave MyKeyVault e salva um backup dessa conta de armazenamento gerenciado em um arquivo chamado Backup.blob.</span><span class="sxs-lookup"><span data-stu-id="d233e-119">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file named Backup.blob.</span></span>

### <span data-ttu-id="d233e-120">Exemplo 3: Fazer o back up de uma conta de armazenamento gerenciada recuperada anteriormente para um nome de arquivo especificado, sobrescrever o arquivo de destino sem solicitar.</span><span class="sxs-lookup"><span data-stu-id="d233e-120">Example 3: Back up a previously retrieved managed storage account to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="d233e-121">Esse comando cria um backup da conta de armazenamento gerenciada chamada $msak. Nome no cofre chamado $msak. VaultName para um arquivo chamado Backup.blob, sobrescrever silenciosamente o arquivo se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="d233e-121">This command creates a backup of the managed storage account named $msak.Name in the vault named $msak.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="d233e-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d233e-122">PARAMETERS</span></span>

### <span data-ttu-id="d233e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d233e-123">-DefaultProfile</span></span>
<span data-ttu-id="d233e-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d233e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d233e-125">-Forçar</span><span class="sxs-lookup"><span data-stu-id="d233e-125">-Force</span></span>
<span data-ttu-id="d233e-126">Substituir o arquivo determinado se ele existir</span><span class="sxs-lookup"><span data-stu-id="d233e-126">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="d233e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d233e-127">-InputObject</span></span>
<span data-ttu-id="d233e-128">Pacote de conta de armazenamento a ser feito backup, com pipeline a partir da saída de uma chamada de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d233e-128">Storage account bundle to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="d233e-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="d233e-129">-Name</span></span>
<span data-ttu-id="d233e-130">Nome secreto.</span><span class="sxs-lookup"><span data-stu-id="d233e-130">Secret name.</span></span>
<span data-ttu-id="d233e-131">O cmdlet constrói o FQDN de um segredo do nome do cofre, do ambiente selecionado no momento e do nome secreto.</span><span class="sxs-lookup"><span data-stu-id="d233e-131">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="d233e-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="d233e-132">-OutputFile</span></span>
<span data-ttu-id="d233e-133">Arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="d233e-133">Output file.</span></span>
<span data-ttu-id="d233e-134">O arquivo de saída para armazenar o backup da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d233e-134">The output file to store the storage account backup.</span></span>
<span data-ttu-id="d233e-135">Se não especificado, será gerado um nome de arquivo padrão.</span><span class="sxs-lookup"><span data-stu-id="d233e-135">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="d233e-136">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="d233e-136">-VaultName</span></span>
<span data-ttu-id="d233e-137">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="d233e-137">Vault name.</span></span>
<span data-ttu-id="d233e-138">O Cmdlet construirá o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="d233e-138">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="d233e-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d233e-139">-Confirm</span></span>
<span data-ttu-id="d233e-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d233e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d233e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d233e-141">-WhatIf</span></span>
<span data-ttu-id="d233e-142">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d233e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d233e-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d233e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d233e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d233e-144">CommonParameters</span></span>
<span data-ttu-id="d233e-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d233e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d233e-146">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d233e-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d233e-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="d233e-147">INPUTS</span></span>

### <span data-ttu-id="d233e-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d233e-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="d233e-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="d233e-149">OUTPUTS</span></span>

### <span data-ttu-id="d233e-150">System.String</span><span class="sxs-lookup"><span data-stu-id="d233e-150">System.String</span></span>

## <span data-ttu-id="d233e-151">Notas</span><span class="sxs-lookup"><span data-stu-id="d233e-151">NOTES</span></span>

## <span data-ttu-id="d233e-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d233e-152">RELATED LINKS</span></span>
