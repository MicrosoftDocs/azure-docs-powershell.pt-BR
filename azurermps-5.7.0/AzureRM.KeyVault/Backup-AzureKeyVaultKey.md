---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultKey.md
ms.openlocfilehash: 2eecb6d4bb069b1578b3080c04de4c9df1e42f09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428911"
---
# <span data-ttu-id="83913-101">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="83913-101">Backup-AzureKeyVaultKey</span></span>

## <span data-ttu-id="83913-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="83913-102">SYNOPSIS</span></span>
<span data-ttu-id="83913-103">Faz o backup de uma chave em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="83913-103">Backs up a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83913-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="83913-104">SYNTAX</span></span>

### <span data-ttu-id="83913-105">ByKeyName (padrão)</span><span class="sxs-lookup"><span data-stu-id="83913-105">ByKeyName (Default)</span></span>
```
Backup-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83913-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="83913-106">ByKey</span></span>
```
Backup-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83913-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="83913-107">DESCRIPTION</span></span>
<span data-ttu-id="83913-108">O cmdlet **backup-AzureKeyVaultKey** faz backup de uma chave especificada em um cofre de chaves, baixando-a e armazenando-a em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="83913-108">The **Backup-AzureKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="83913-109">Se houver várias versões da chave, todas as versões serão incluídas no backup.</span><span class="sxs-lookup"><span data-stu-id="83913-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="83913-110">Como o conteúdo baixado é criptografado, ele não pode ser usado fora do cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="83913-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="83913-111">Você pode restaurar uma chave em backup para qualquer cofre de chaves na assinatura da qual foi feito o backup.</span><span class="sxs-lookup"><span data-stu-id="83913-111">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>

<span data-ttu-id="83913-112">Os motivos típicos para usar este cmdlet são:</span><span class="sxs-lookup"><span data-stu-id="83913-112">Typical reasons to use this cmdlet are:</span></span> 

- <span data-ttu-id="83913-113">Você deseja fazer a caução de uma cópia da sua chave para que você tenha uma cópia offline em caso de excluir acidentalmente a chave no seu cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="83913-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="83913-114">Você criou uma chave usando o Key Vault e agora deseja clonar a chave para uma região diferente do Azure, de modo que você possa usá-la em todas as instâncias do seu aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="83913-114">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="83913-115">Use o cmdlet **backup-AzureKeyVaultKey** para recuperar a chave no formato criptografado e, em seguida, use o cmdlet Restore-AzureKeyVaultKey e especifique um cofre de chaves na segunda região.</span><span class="sxs-lookup"><span data-stu-id="83913-115">Use the **Backup-AzureKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzureKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="83913-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="83913-116">EXAMPLES</span></span>

### <span data-ttu-id="83913-117">Exemplo 1: fazer backup de uma chave com um nome de arquivo gerado automaticamente</span><span class="sxs-lookup"><span data-stu-id="83913-117">Example 1: Back up a key with an automatically generated file name</span></span>
```
PS C:\>Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="83913-118">Esse comando recupera a chave chamada MyKey do cofre de chaves chamado MyKeyVault e salva um backup dessa chave em um arquivo que é automaticamente nomeado para você e exibe o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="83913-118">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="83913-119">Exemplo 2: fazer backup de uma chave em um nome de arquivo especificado</span><span class="sxs-lookup"><span data-stu-id="83913-119">Example 2: Back up a key to a specified file name</span></span>
```
PS C:\>Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'
```

<span data-ttu-id="83913-120">Esse comando recupera a chave chamada MyKey da chave vaultnamed MyKeyVault e salva um backup dessa chave em um arquivo chamado backup. blob.</span><span class="sxs-lookup"><span data-stu-id="83913-120">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="83913-121">Exemplo 3: fazer backup de uma chave recuperada anteriormente para um nome de arquivo especificado, substituindo o arquivo de destino sem solicitação.</span><span class="sxs-lookup"><span data-stu-id="83913-121">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```
PS C:\>$key = Get-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\>Backup-AzureKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force
```

<span data-ttu-id="83913-122">Esse comando cria um backup da chave chamada $key. Nome no cofre chamado $key. Compartimentalizaname para um arquivo chamado backup. blob, substituindo o arquivo silenciosamente se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="83913-122">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="83913-123">OS</span><span class="sxs-lookup"><span data-stu-id="83913-123">PARAMETERS</span></span>

### <span data-ttu-id="83913-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83913-124">-DefaultProfile</span></span>
<span data-ttu-id="83913-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="83913-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83913-126">-Force</span><span class="sxs-lookup"><span data-stu-id="83913-126">-Force</span></span>
<span data-ttu-id="83913-127">Substituir o arquivo fornecido se ele existir</span><span class="sxs-lookup"><span data-stu-id="83913-127">Overwrite the given file if it exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83913-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83913-128">-InputObject</span></span>
<span data-ttu-id="83913-129">Pacote de chaves para backup, em pipeline a partir da saída de uma chamada de recuperação.</span><span class="sxs-lookup"><span data-stu-id="83913-129">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83913-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="83913-130">-Name</span></span>
<span data-ttu-id="83913-131">Especifica o nome da chave para fazer backup.</span><span class="sxs-lookup"><span data-stu-id="83913-131">Specifies the name of the key to back up.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83913-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="83913-132">-OutputFile</span></span>
<span data-ttu-id="83913-133">Especifica o arquivo de saída no qual o blob de backup é armazenado.</span><span class="sxs-lookup"><span data-stu-id="83913-133">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="83913-134">Se você não especificar esse parâmetro, esse cmdlet gerará um nome de arquivo para você.</span><span class="sxs-lookup"><span data-stu-id="83913-134">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="83913-135">Se você especificar o nome de um arquivo de saída existente, a operação não será concluída e retornará uma mensagem de erro informando que o arquivo de backup já existe.</span><span class="sxs-lookup"><span data-stu-id="83913-135">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83913-136">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="83913-136">-VaultName</span></span>
<span data-ttu-id="83913-137">Especifica o nome do cofre de chaves que contém a chave para fazer backup.</span><span class="sxs-lookup"><span data-stu-id="83913-137">Specifies the name of the key vault that contains the key to back up.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83913-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="83913-138">-Confirm</span></span>
<span data-ttu-id="83913-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83913-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83913-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83913-140">-WhatIf</span></span>
<span data-ttu-id="83913-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="83913-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83913-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="83913-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83913-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83913-143">CommonParameters</span></span>
<span data-ttu-id="83913-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83913-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83913-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83913-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83913-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="83913-146">INPUTS</span></span>

### <span data-ttu-id="83913-147">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="83913-147">None</span></span>
<span data-ttu-id="83913-148">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="83913-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="83913-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="83913-149">OUTPUTS</span></span>

### <span data-ttu-id="83913-150">String</span><span class="sxs-lookup"><span data-stu-id="83913-150">String</span></span>
<span data-ttu-id="83913-151">O cmdlet retorna o caminho do arquivo de saída que contém o backup da chave.</span><span class="sxs-lookup"><span data-stu-id="83913-151">The cmdlet returns the path of the output file containing the backup of the key.</span></span>

## <span data-ttu-id="83913-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="83913-152">NOTES</span></span>

## <span data-ttu-id="83913-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="83913-153">RELATED LINKS</span></span>

[<span data-ttu-id="83913-154">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="83913-154">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="83913-155">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="83913-155">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="83913-156">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="83913-156">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="83913-157">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="83913-157">Restore-AzureKeyVaultKey</span></span>](./Restore-AzureKeyVaultKey.md)

