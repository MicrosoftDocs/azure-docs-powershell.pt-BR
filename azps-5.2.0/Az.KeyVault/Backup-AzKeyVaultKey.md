---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: 88decaffa736f015b8e65aa1217eab4899b07c7c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261366"
---
# <span data-ttu-id="0438f-101">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0438f-101">Backup-AzKeyVaultKey</span></span>

## <span data-ttu-id="0438f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0438f-102">SYNOPSIS</span></span>
<span data-ttu-id="0438f-103">Faz o backup de uma chave em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="0438f-103">Backs up a key in a key vault.</span></span>

## <span data-ttu-id="0438f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0438f-104">SYNTAX</span></span>

### <span data-ttu-id="0438f-105">ByKeyName (padrão)</span><span class="sxs-lookup"><span data-stu-id="0438f-105">ByKeyName (Default)</span></span>
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0438f-106">HsmByKeyName</span><span class="sxs-lookup"><span data-stu-id="0438f-106">HsmByKeyName</span></span>
```
Backup-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0438f-107">ByKey</span><span class="sxs-lookup"><span data-stu-id="0438f-107">ByKey</span></span>
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0438f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0438f-108">DESCRIPTION</span></span>
<span data-ttu-id="0438f-109">O cmdlet **backup-AzKeyVaultKey** faz backup de uma chave especificada em um cofre de chaves, baixando-a e armazenando-a em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="0438f-109">The **Backup-AzKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="0438f-110">Se houver várias versões da chave, todas as versões serão incluídas no backup.</span><span class="sxs-lookup"><span data-stu-id="0438f-110">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="0438f-111">Como o conteúdo baixado é criptografado, ele não pode ser usado fora do cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="0438f-111">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="0438f-112">Você pode restaurar uma chave em backup para qualquer cofre de chaves na assinatura da qual foi feito o backup.</span><span class="sxs-lookup"><span data-stu-id="0438f-112">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="0438f-113">Os motivos típicos para usar este cmdlet são:</span><span class="sxs-lookup"><span data-stu-id="0438f-113">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="0438f-114">Você deseja fazer a caução de uma cópia da sua chave para que você tenha uma cópia offline em caso de excluir acidentalmente a chave no seu cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="0438f-114">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="0438f-115">Você criou uma chave usando o Key Vault e agora deseja clonar a chave para uma região diferente do Azure, de modo que você possa usá-la em todas as instâncias do seu aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="0438f-115">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="0438f-116">Use o cmdlet **backup-AzKeyVaultKey** para recuperar a chave no formato criptografado e, em seguida, use o cmdlet Restore-AzKeyVaultKey e especifique um cofre de chaves na segunda região.</span><span class="sxs-lookup"><span data-stu-id="0438f-116">Use the **Backup-AzKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="0438f-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0438f-117">EXAMPLES</span></span>

### <span data-ttu-id="0438f-118">Exemplo 1: fazer backup de uma chave com um nome de arquivo gerado automaticamente</span><span class="sxs-lookup"><span data-stu-id="0438f-118">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

<span data-ttu-id="0438f-119">Esse comando recupera a chave chamada MyKey do cofre de chaves chamado MyKeyVault e salva um backup dessa chave em um arquivo que é automaticamente nomeado para você e exibe o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="0438f-119">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="0438f-120">Exemplo 2: fazer backup de uma chave em um nome de arquivo especificado</span><span class="sxs-lookup"><span data-stu-id="0438f-120">Example 2: Back up a key to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="0438f-121">Esse comando recupera a chave chamada MyKey da chave vaultnamed MyKeyVault e salva um backup dessa chave em um arquivo chamado backup. blob.</span><span class="sxs-lookup"><span data-stu-id="0438f-121">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="0438f-122">Exemplo 3: fazer backup de uma chave recuperada anteriormente para um nome de arquivo especificado, substituindo o arquivo de destino sem solicitação.</span><span class="sxs-lookup"><span data-stu-id="0438f-122">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="0438f-123">Esse comando cria um backup da chave chamada $key. Nome no cofre chamado $key. Compartimentalizaname para um arquivo chamado backup. blob, substituindo o arquivo silenciosamente se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="0438f-123">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="0438f-124">OS</span><span class="sxs-lookup"><span data-stu-id="0438f-124">PARAMETERS</span></span>

### <span data-ttu-id="0438f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0438f-125">-DefaultProfile</span></span>
<span data-ttu-id="0438f-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0438f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0438f-127">-Force</span><span class="sxs-lookup"><span data-stu-id="0438f-127">-Force</span></span>
<span data-ttu-id="0438f-128">Substituir o arquivo fornecido se ele existir</span><span class="sxs-lookup"><span data-stu-id="0438f-128">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="0438f-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="0438f-129">-HsmName</span></span>
<span data-ttu-id="0438f-130">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="0438f-130">HSM name.</span></span> <span data-ttu-id="0438f-131">O cmdlet constrói o FQDN de um HSM gerenciado com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="0438f-131">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByKeyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0438f-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0438f-132">-InputObject</span></span>
<span data-ttu-id="0438f-133">Pacote de chaves para backup, em pipeline a partir da saída de uma chamada de recuperação.</span><span class="sxs-lookup"><span data-stu-id="0438f-133">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0438f-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="0438f-134">-Name</span></span>
<span data-ttu-id="0438f-135">Especifica o nome da chave para fazer backup.</span><span class="sxs-lookup"><span data-stu-id="0438f-135">Specifies the name of the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, HsmByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0438f-136">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="0438f-136">-OutputFile</span></span>
<span data-ttu-id="0438f-137">Especifica o arquivo de saída no qual o blob de backup é armazenado.</span><span class="sxs-lookup"><span data-stu-id="0438f-137">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="0438f-138">Se você não especificar esse parâmetro, esse cmdlet gerará um nome de arquivo para você.</span><span class="sxs-lookup"><span data-stu-id="0438f-138">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="0438f-139">Se você especificar o nome de um arquivo de saída existente, a operação não será concluída e retornará uma mensagem de erro informando que o arquivo de backup já existe.</span><span class="sxs-lookup"><span data-stu-id="0438f-139">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="0438f-140">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="0438f-140">-VaultName</span></span>
<span data-ttu-id="0438f-141">Especifica o nome do cofre de chaves que contém a chave para fazer backup.</span><span class="sxs-lookup"><span data-stu-id="0438f-141">Specifies the name of the key vault that contains the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0438f-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0438f-142">-Confirm</span></span>
<span data-ttu-id="0438f-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0438f-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0438f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0438f-144">-WhatIf</span></span>
<span data-ttu-id="0438f-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0438f-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0438f-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0438f-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0438f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0438f-147">CommonParameters</span></span>
<span data-ttu-id="0438f-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0438f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0438f-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0438f-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0438f-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0438f-150">INPUTS</span></span>

### <span data-ttu-id="0438f-151">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0438f-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="0438f-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0438f-152">OUTPUTS</span></span>

### <span data-ttu-id="0438f-153">System. String</span><span class="sxs-lookup"><span data-stu-id="0438f-153">System.String</span></span>

## <span data-ttu-id="0438f-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0438f-154">NOTES</span></span>

## <span data-ttu-id="0438f-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0438f-155">RELATED LINKS</span></span>

[<span data-ttu-id="0438f-156">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0438f-156">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="0438f-157">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0438f-157">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="0438f-158">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0438f-158">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="0438f-159">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0438f-159">Restore-AzKeyVaultKey</span></span>](./Restore-AzKeyVaultKey.md)

