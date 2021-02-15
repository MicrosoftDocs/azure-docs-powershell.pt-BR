---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: 88decaffa736f015b8e65aa1217eab4899b07c7c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111829"
---
# <span data-ttu-id="4bc53-101">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4bc53-101">Backup-AzKeyVaultKey</span></span>

## <span data-ttu-id="4bc53-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4bc53-102">SYNOPSIS</span></span>
<span data-ttu-id="4bc53-103">Fazer o back up de uma chave em um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="4bc53-103">Backs up a key in a key vault.</span></span>

## <span data-ttu-id="4bc53-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4bc53-104">SYNTAX</span></span>

### <span data-ttu-id="4bc53-105">ByKeyName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4bc53-105">ByKeyName (Default)</span></span>
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bc53-106">HsmByKeyName</span><span class="sxs-lookup"><span data-stu-id="4bc53-106">HsmByKeyName</span></span>
```
Backup-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bc53-107">ByKey</span><span class="sxs-lookup"><span data-stu-id="4bc53-107">ByKey</span></span>
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bc53-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4bc53-108">DESCRIPTION</span></span>
<span data-ttu-id="4bc53-109">O **cmdlet Backup-AzKeyVaultKey** faz backup de uma chave especificada em um cofre de teclas baixando-a e armazenar-a em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="4bc53-109">The **Backup-AzKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="4bc53-110">Se houver várias versões da chave, todas as versões serão incluídas no backup.</span><span class="sxs-lookup"><span data-stu-id="4bc53-110">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="4bc53-111">Como o conteúdo baixado é criptografado, ele não pode ser usado fora do Cofre de Teclas do Azure.</span><span class="sxs-lookup"><span data-stu-id="4bc53-111">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="4bc53-112">Você pode restaurar uma chave em backup para qualquer cofre de chave na assinatura da sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="4bc53-112">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="4bc53-113">Os motivos típicos para usar este cmdlet são:</span><span class="sxs-lookup"><span data-stu-id="4bc53-113">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="4bc53-114">Você deseja escrow uma cópia da sua chave, para que você tenha uma cópia offline caso exclua acidentalmente sua chave no seu cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="4bc53-114">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="4bc53-115">Você criou uma chave usando o Cofre de Teclas e agora deseja clonar a chave em uma região diferente do Azure, para poder usá-la em todas as instâncias do seu aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="4bc53-115">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="4bc53-116">Use o cmdlet **Backup-AzKeyVaultKey** para recuperar a chave em formato criptografado e, em seguida, use o cmdlet Restore-AzKeyVaultKey e especifique um cofre de chave na segunda região.</span><span class="sxs-lookup"><span data-stu-id="4bc53-116">Use the **Backup-AzKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="4bc53-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4bc53-117">EXAMPLES</span></span>

### <span data-ttu-id="4bc53-118">Exemplo 1: Fazer o back up de uma chave com um nome de arquivo gerado automaticamente</span><span class="sxs-lookup"><span data-stu-id="4bc53-118">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

<span data-ttu-id="4bc53-119">Esse comando recupera a chave Chamada MyKey do cofre de teclas chamado MyKeyVault e salva um backup dessa chave em um arquivo que é nomeado automaticamente para você e exibe o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="4bc53-119">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="4bc53-120">Exemplo 2: Fazer o back up de uma chave para um nome de arquivo especificado</span><span class="sxs-lookup"><span data-stu-id="4bc53-120">Example 2: Back up a key to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="4bc53-121">Esse comando recupera a chave chamada MyKey do cofre de tecla MyKeyVault e salva um backup dessa chave em um arquivo chamado Backup.blob.</span><span class="sxs-lookup"><span data-stu-id="4bc53-121">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="4bc53-122">Exemplo 3: Fazer o back up de uma chave recuperada anteriormente para um nome de arquivo especificado, sobrescrever o arquivo de destino sem solicitar.</span><span class="sxs-lookup"><span data-stu-id="4bc53-122">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="4bc53-123">Esse comando cria um backup da chave chamada $key. Nome no cofre chamado $key. VaultName para um arquivo chamado Backup.blob, sobrescrever silenciosamente o arquivo se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="4bc53-123">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="4bc53-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4bc53-124">PARAMETERS</span></span>

### <span data-ttu-id="4bc53-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bc53-125">-DefaultProfile</span></span>
<span data-ttu-id="4bc53-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4bc53-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4bc53-127">-Forçar</span><span class="sxs-lookup"><span data-stu-id="4bc53-127">-Force</span></span>
<span data-ttu-id="4bc53-128">Substituir o arquivo determinado se ele existir</span><span class="sxs-lookup"><span data-stu-id="4bc53-128">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="4bc53-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="4bc53-129">-HsmName</span></span>
<span data-ttu-id="4bc53-130">Nome HSM.</span><span class="sxs-lookup"><span data-stu-id="4bc53-130">HSM name.</span></span> <span data-ttu-id="4bc53-131">O Cmdlet construirá o FQDN de um HSM gerenciado com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="4bc53-131">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="4bc53-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bc53-132">-InputObject</span></span>
<span data-ttu-id="4bc53-133">Pacote de chaves para fazer o back-up, pipelined a partir da saída de uma chamada de recuperação.</span><span class="sxs-lookup"><span data-stu-id="4bc53-133">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="4bc53-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="4bc53-134">-Name</span></span>
<span data-ttu-id="4bc53-135">Especifica o nome da chave para fazer o back-up.</span><span class="sxs-lookup"><span data-stu-id="4bc53-135">Specifies the name of the key to back up.</span></span>

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

### <span data-ttu-id="4bc53-136">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="4bc53-136">-OutputFile</span></span>
<span data-ttu-id="4bc53-137">Especifica o arquivo de saída no qual o blob de backup está armazenado.</span><span class="sxs-lookup"><span data-stu-id="4bc53-137">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="4bc53-138">Se você não especificar esse parâmetro, esse cmdlet gerará um nome de arquivo para você.</span><span class="sxs-lookup"><span data-stu-id="4bc53-138">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="4bc53-139">Se você especificar o nome de um arquivo de saída existente, a operação não será concluída e retornará uma mensagem de erro de que o arquivo de backup já existe.</span><span class="sxs-lookup"><span data-stu-id="4bc53-139">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="4bc53-140">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="4bc53-140">-VaultName</span></span>
<span data-ttu-id="4bc53-141">Especifica o nome do cofre de chave que contém a chave para fazer o back-up.</span><span class="sxs-lookup"><span data-stu-id="4bc53-141">Specifies the name of the key vault that contains the key to back up.</span></span>

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

### <span data-ttu-id="4bc53-142">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4bc53-142">-Confirm</span></span>
<span data-ttu-id="4bc53-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bc53-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bc53-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bc53-144">-WhatIf</span></span>
<span data-ttu-id="4bc53-145">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4bc53-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bc53-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4bc53-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bc53-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bc53-147">CommonParameters</span></span>
<span data-ttu-id="4bc53-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bc53-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bc53-149">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4bc53-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bc53-150">Entradas</span><span class="sxs-lookup"><span data-stu-id="4bc53-150">INPUTS</span></span>

### <span data-ttu-id="4bc53-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4bc53-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="4bc53-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="4bc53-152">OUTPUTS</span></span>

### <span data-ttu-id="4bc53-153">System.String</span><span class="sxs-lookup"><span data-stu-id="4bc53-153">System.String</span></span>

## <span data-ttu-id="4bc53-154">Notas</span><span class="sxs-lookup"><span data-stu-id="4bc53-154">NOTES</span></span>

## <span data-ttu-id="4bc53-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4bc53-155">RELATED LINKS</span></span>

[<span data-ttu-id="4bc53-156">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4bc53-156">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="4bc53-157">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4bc53-157">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="4bc53-158">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4bc53-158">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="4bc53-159">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4bc53-159">Restore-AzKeyVaultKey</span></span>](./Restore-AzKeyVaultKey.md)

