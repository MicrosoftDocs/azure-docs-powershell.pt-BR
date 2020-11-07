---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: a171f967a937873b85adcfca732987037e6db0a6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778231"
---
# <span data-ttu-id="5bd61-101">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5bd61-101">Backup-AzKeyVaultSecret</span></span>

## <span data-ttu-id="5bd61-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5bd61-102">SYNOPSIS</span></span>
<span data-ttu-id="5bd61-103">Faz o backup de um segredo em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5bd61-103">Backs up a secret in a key vault.</span></span>

## <span data-ttu-id="5bd61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5bd61-104">SYNTAX</span></span>

### <span data-ttu-id="5bd61-105">BySecretName (padrão)</span><span class="sxs-lookup"><span data-stu-id="5bd61-105">BySecretName (Default)</span></span>
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bd61-106">BySecret</span><span class="sxs-lookup"><span data-stu-id="5bd61-106">BySecret</span></span>
```
Backup-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bd61-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5bd61-107">DESCRIPTION</span></span>
<span data-ttu-id="5bd61-108">O cmdlet **backup-AzKeyVaultSecret** faz backup de um segredo especificado em um cofre de chaves, baixando-o e armazenando-o em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="5bd61-108">The **Backup-AzKeyVaultSecret** cmdlet backs up a specified secret in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="5bd61-109">Se houver várias versões do segredo, todas as versões serão incluídas no backup.</span><span class="sxs-lookup"><span data-stu-id="5bd61-109">If there are multiple versions of the secret, all versions are included in the backup.</span></span>
<span data-ttu-id="5bd61-110">Como o conteúdo baixado é criptografado, ele não pode ser usado fora do cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="5bd61-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="5bd61-111">Você pode restaurar um segredo em backup para qualquer cofre de chaves na assinatura do qual foi feito o backup.</span><span class="sxs-lookup"><span data-stu-id="5bd61-111">You can restore a backed-up secret to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="5bd61-112">Os motivos típicos para usar este cmdlet são:</span><span class="sxs-lookup"><span data-stu-id="5bd61-112">Typical reasons to use this cmdlet are:</span></span>
- <span data-ttu-id="5bd61-113">Você deseja fazer a caução de uma cópia do seu segredo, para que você tenha uma cópia offline, caso você exclua acidentalmente seu segredo no seu cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5bd61-113">You want to escrow a copy of your secret, so that you have an offline copy in case you accidentally delete your secret in your key vault.</span></span>
- <span data-ttu-id="5bd61-114">Você adicionou um segredo a um cofre de chaves e agora deseja clonar o segredo para uma região diferente do Azure, de modo que você possa usá-lo em todas as instâncias do seu aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="5bd61-114">You added a secret to a key vault and now want to clone the secret into a different Azure region, so that you can use it from all instances of your distributed application.</span></span> <span data-ttu-id="5bd61-115">Use o cmdlet Backup-AzKeyVaultSecret para recuperar o segredo no formato criptografado e use o cmdlet Restore-AzKeyVaultSecret e especifique um cofre de chaves na segunda região.</span><span class="sxs-lookup"><span data-stu-id="5bd61-115">Use the Backup-AzKeyVaultSecret cmdlet to retrieve the secret in encrypted format and then use the Restore-AzKeyVaultSecret cmdlet and specify a key vault in the second region.</span></span> <span data-ttu-id="5bd61-116">(Observe que as regiões devem pertencer à mesma geografia.)</span><span class="sxs-lookup"><span data-stu-id="5bd61-116">(Note that the regions must belong to the same geography.)</span></span>

## <span data-ttu-id="5bd61-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5bd61-117">EXAMPLES</span></span>

### <span data-ttu-id="5bd61-118">Exemplo 1: fazer backup de um segredo com um nome de arquivo gerado automaticamente</span><span class="sxs-lookup"><span data-stu-id="5bd61-118">Example 1: Back up a secret with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

<span data-ttu-id="5bd61-119">Esse comando recupera o segredo nomeado MySecret do cofre de chaves chamado MyKeyVault e salva um backup desse segredo em um arquivo que é automaticamente nomeado para você e exibe o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5bd61-119">This command retrieves the secret named MySecret from the key vault named MyKeyVault and saves a backup of that secret to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="5bd61-120">Exemplo 2: fazer backup de um segredo em um nome de arquivo especificado, substituindo o arquivo existente sem avisar</span><span class="sxs-lookup"><span data-stu-id="5bd61-120">Example 2: Back up a secret to a specified file name, overwriting the existing file without prompting</span></span>
```powershell
PS C:\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="5bd61-121">Esse comando recupera o segredo chamado MySecret da chave vaultnamed MyKeyVault e salva um backup desse segredo em um arquivo chamado backup. blob.</span><span class="sxs-lookup"><span data-stu-id="5bd61-121">This command retrieves the secret named MySecret from the key vaultnamed MyKeyVault and saves a backup of that secret to a file named Backup.blob.</span></span>

### <span data-ttu-id="5bd61-122">Exemplo 3: fazer backup de um segredo anteriormente recuperado para um nome de arquivo especificado</span><span class="sxs-lookup"><span data-stu-id="5bd61-122">Example 3: Back up a secret previously retrieved to a specified file name</span></span>
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="5bd61-123">Esse comando usa o nome e o nome do cofre do objeto de $secret para recuperar o segredo e salva o backup em um arquivo chamado backup. blob.</span><span class="sxs-lookup"><span data-stu-id="5bd61-123">This command uses the $secret object's vault name and name to retrieves the secret and saves its backup to a file named Backup.blob.</span></span>

## <span data-ttu-id="5bd61-124">OS</span><span class="sxs-lookup"><span data-stu-id="5bd61-124">PARAMETERS</span></span>

### <span data-ttu-id="5bd61-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bd61-125">-DefaultProfile</span></span>
<span data-ttu-id="5bd61-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5bd61-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bd61-127">-Force</span><span class="sxs-lookup"><span data-stu-id="5bd61-127">-Force</span></span>
<span data-ttu-id="5bd61-128">Solicita confirmação antes de substituir o arquivo de saída, se houver.</span><span class="sxs-lookup"><span data-stu-id="5bd61-128">Prompts you for confirmation before overwriting the output file, if that exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd61-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5bd61-129">-InputObject</span></span>
<span data-ttu-id="5bd61-130">Segredo para backup, em pipeline a partir da saída de uma chamada de recuperação.</span><span class="sxs-lookup"><span data-stu-id="5bd61-130">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: BySecret
Aliases: Secret

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bd61-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="5bd61-131">-Name</span></span>
<span data-ttu-id="5bd61-132">Especifica o nome do segredo para fazer backup.</span><span class="sxs-lookup"><span data-stu-id="5bd61-132">Specifies the name of the secret to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd61-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="5bd61-133">-OutputFile</span></span>
<span data-ttu-id="5bd61-134">Especifica o arquivo de saída no qual o blob de backup é armazenado.</span><span class="sxs-lookup"><span data-stu-id="5bd61-134">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="5bd61-135">Se você não especificar esse parâmetro, esse cmdlet gerará um nome de arquivo para você.</span><span class="sxs-lookup"><span data-stu-id="5bd61-135">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="5bd61-136">Se você especificar o nome de um arquivo de saída existente, a operação não será concluída e retornará uma mensagem de erro informando que o arquivo de backup já existe.</span><span class="sxs-lookup"><span data-stu-id="5bd61-136">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="5bd61-137">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="5bd61-137">-VaultName</span></span>
<span data-ttu-id="5bd61-138">Especifica o nome do cofre de chaves que contém o segredo para fazer backup.</span><span class="sxs-lookup"><span data-stu-id="5bd61-138">Specifies the name of the key vault that contains the secret to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd61-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5bd61-139">-Confirm</span></span>
<span data-ttu-id="5bd61-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bd61-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd61-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bd61-141">-WhatIf</span></span>
<span data-ttu-id="5bd61-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5bd61-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bd61-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5bd61-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd61-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bd61-144">CommonParameters</span></span>
<span data-ttu-id="5bd61-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bd61-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bd61-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5bd61-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bd61-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5bd61-147">INPUTS</span></span>

### <span data-ttu-id="5bd61-148">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="5bd61-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="5bd61-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5bd61-149">OUTPUTS</span></span>

### <span data-ttu-id="5bd61-150">System. String</span><span class="sxs-lookup"><span data-stu-id="5bd61-150">System.String</span></span>

## <span data-ttu-id="5bd61-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5bd61-151">NOTES</span></span>

## <span data-ttu-id="5bd61-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5bd61-152">RELATED LINKS</span></span>

[<span data-ttu-id="5bd61-153">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5bd61-153">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="5bd61-154">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5bd61-154">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="5bd61-155">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5bd61-155">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="5bd61-156">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5bd61-156">Restore-AzKeyVaultSecret</span></span>](./Restore-AzKeyVaultSecret.md)

