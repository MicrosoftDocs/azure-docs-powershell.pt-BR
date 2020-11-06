---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://go.microsoft.com/fwlink/?LinkId=690296
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultSecret.md
ms.openlocfilehash: c53006a4f059fe1f243d9e0bf7a4c701a4c417a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611111"
---
# <span data-ttu-id="7d5fe-101">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7d5fe-101">Backup-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="7d5fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7d5fe-102">SYNOPSIS</span></span>
<span data-ttu-id="7d5fe-103">Faz o backup de um segredo em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="7d5fe-103">Backs up a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d5fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d5fe-104">SYNTAX</span></span>

### <span data-ttu-id="7d5fe-105">BySecretName (padrão)</span><span class="sxs-lookup"><span data-stu-id="7d5fe-105">BySecretName (Default)</span></span>
```
Backup-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d5fe-106">BySecret</span><span class="sxs-lookup"><span data-stu-id="7d5fe-106">BySecret</span></span>
```
Backup-AzureKeyVaultSecret [-Secret] <Secret> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d5fe-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7d5fe-107">DESCRIPTION</span></span>
<span data-ttu-id="7d5fe-108">O cmdlet **backup-AzureKeyVaultSecret** faz backup de um segredo especificado em um cofre de chaves, baixando-o e armazenando-o em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="7d5fe-108">The **Backup-AzureKeyVaultSecret** cmdlet backs up a specified secret in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="7d5fe-109">Se houver várias versões do segredo, todas as versões serão incluídas no backup.</span><span class="sxs-lookup"><span data-stu-id="7d5fe-109">If there are multiple versions of the secret, all versions are included in the backup.</span></span>
<span data-ttu-id="7d5fe-110">Como o conteúdo baixado é criptografado, ele não pode ser usado fora do cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="7d5fe-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="7d5fe-111">Você pode restaurar um segredo em backup para qualquer cofre de chaves na assinatura do qual foi feito o backup.</span><span class="sxs-lookup"><span data-stu-id="7d5fe-111">You can restore a backed-up secret to any key vault in the subscription that it was backed up from.</span></span>

<span data-ttu-id="7d5fe-112">Os motivos típicos para usar este cmdlet são:</span><span class="sxs-lookup"><span data-stu-id="7d5fe-112">Typical reasons to use this cmdlet are:</span></span>

- <span data-ttu-id="7d5fe-113">Você deseja fazer a caução de uma cópia do seu segredo, para que você tenha uma cópia offline, caso você exclua acidentalmente seu segredo no seu cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="7d5fe-113">You want to escrow a copy of your secret, so that you have an offline copy in case you accidentally delete your secret in your key vault.</span></span>
- <span data-ttu-id="7d5fe-114">Você adicionou um segredo a um cofre de chaves e agora deseja clonar o segredo para uma região diferente do Azure, de modo que você possa usá-lo em todas as instâncias do seu aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="7d5fe-114">You added a secret to a key vault and now want to clone the secret into a different Azure region, so that you can use it from all instances of your distributed application.</span></span> <span data-ttu-id="7d5fe-115">Use o cmdlet Backup-AzureKeyVaultSecret para recuperar o segredo no formato criptografado e use o cmdlet Restore-AzureKeyVaultSecret e especifique um cofre de chaves na segunda região.</span><span class="sxs-lookup"><span data-stu-id="7d5fe-115">Use the Backup-AzureKeyVaultSecret cmdlet to retrieve the secret in encrypted format and then use the Restore-AzureKeyVaultSecret cmdlet and specify a key vault in the second region.</span></span> <span data-ttu-id="7d5fe-116">(Observe que as regiões devem pertencer à mesma geografia.)</span><span class="sxs-lookup"><span data-stu-id="7d5fe-116">(Note that the regions must belong to the same geography.)</span></span>

## <span data-ttu-id="7d5fe-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7d5fe-117">EXAMPLES</span></span>

### <span data-ttu-id="7d5fe-118">Exemplo 1: fazer backup de um segredo com um nome de arquivo gerado automaticamente</span><span class="sxs-lookup"><span data-stu-id="7d5fe-118">Example 1: Back up a secret with an automatically generated file name</span></span>
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="7d5fe-119">Esse comando recupera o segredo nomeado MySecret do cofre de chaves chamado MyKeyVault e salva um backup desse segredo em um arquivo que é automaticamente nomeado para você e exibe o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="7d5fe-119">This command retrieves the secret named MySecret from the key vault named MyKeyVault and saves a backup of that secret to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="7d5fe-120">Exemplo 2: fazer backup de um segredo em um nome de arquivo especificado, substituindo o arquivo existente sem avisar</span><span class="sxs-lookup"><span data-stu-id="7d5fe-120">Example 2: Back up a secret to a specified file name, overwriting the existing file without prompting</span></span>
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force
```

<span data-ttu-id="7d5fe-121">Esse comando recupera o segredo chamado MySecret da chave vaultnamed MyKeyVault e salva um backup desse segredo em um arquivo chamado backup. blob.</span><span class="sxs-lookup"><span data-stu-id="7d5fe-121">This command retrieves the secret named MySecret from the key vaultnamed MyKeyVault and saves a backup of that secret to a file named Backup.blob.</span></span>

### <span data-ttu-id="7d5fe-122">Exemplo 3: fazer backup de um segredo anteriormente recuperado para um nome de arquivo especificado</span><span class="sxs-lookup"><span data-stu-id="7d5fe-122">Example 3: Back up a secret previously retrieved to a specified file name</span></span>
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\>Backup-AzureKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'
```

<span data-ttu-id="7d5fe-123">Esse comando usa o nome e o nome do cofre do objeto de $secret para recuperar o segredo e salva o backup em um arquivo chamado backup. blob.</span><span class="sxs-lookup"><span data-stu-id="7d5fe-123">This command uses the $secret object's vault name and name to retrieves the secret and saves its backup to a file named Backup.blob.</span></span>

## <span data-ttu-id="7d5fe-124">OS</span><span class="sxs-lookup"><span data-stu-id="7d5fe-124">PARAMETERS</span></span>

### <span data-ttu-id="7d5fe-125">-Force</span><span class="sxs-lookup"><span data-stu-id="7d5fe-125">-Force</span></span>
<span data-ttu-id="7d5fe-126">Solicita confirmação antes de substituir o arquivo de saída, se houver.</span><span class="sxs-lookup"><span data-stu-id="7d5fe-126">Prompts you for confirmation before overwriting the output file, if that exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d5fe-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d5fe-127">-Name</span></span>
<span data-ttu-id="7d5fe-128">Especifica o nome do segredo para fazer backup.</span><span class="sxs-lookup"><span data-stu-id="7d5fe-128">Specifies the name of the secret to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d5fe-129">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="7d5fe-129">-OutputFile</span></span>
<span data-ttu-id="7d5fe-130">Especifica o arquivo de saída no qual o blob de backup é armazenado.</span><span class="sxs-lookup"><span data-stu-id="7d5fe-130">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="7d5fe-131">Se você não especificar esse parâmetro, esse cmdlet gerará um nome de arquivo para você.</span><span class="sxs-lookup"><span data-stu-id="7d5fe-131">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="7d5fe-132">Se você especificar o nome de um arquivo de saída existente, a operação não será concluída e retornará uma mensagem de erro informando que o arquivo de backup já existe.</span><span class="sxs-lookup"><span data-stu-id="7d5fe-132">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d5fe-133">-Segredo</span><span class="sxs-lookup"><span data-stu-id="7d5fe-133">-Secret</span></span>
<span data-ttu-id="7d5fe-134">Especifica o objeto cujo nome e cofre devem ser usados para a operação de backup.</span><span class="sxs-lookup"><span data-stu-id="7d5fe-134">Specifies the object whose name and vault should be used for the backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.Secret
Parameter Sets: BySecret
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d5fe-135">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="7d5fe-135">-VaultName</span></span>
<span data-ttu-id="7d5fe-136">Especifica o nome do cofre de chaves que contém o segredo para fazer backup.</span><span class="sxs-lookup"><span data-stu-id="7d5fe-136">Specifies the name of the key vault that contains the secret to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d5fe-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7d5fe-137">-Confirm</span></span>
<span data-ttu-id="7d5fe-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d5fe-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d5fe-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d5fe-139">-WhatIf</span></span>
<span data-ttu-id="7d5fe-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7d5fe-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d5fe-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7d5fe-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d5fe-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d5fe-142">-DefaultProfile</span></span>
<span data-ttu-id="7d5fe-143">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7d5fe-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d5fe-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d5fe-144">CommonParameters</span></span>
<span data-ttu-id="7d5fe-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d5fe-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d5fe-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d5fe-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d5fe-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7d5fe-147">INPUTS</span></span>

## <span data-ttu-id="7d5fe-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7d5fe-148">OUTPUTS</span></span>

### <span data-ttu-id="7d5fe-149">String</span><span class="sxs-lookup"><span data-stu-id="7d5fe-149">String</span></span>
<span data-ttu-id="7d5fe-150">O cmdlet retorna o caminho do arquivo de saída que contém o backup da chave.</span><span class="sxs-lookup"><span data-stu-id="7d5fe-150">The cmdlet returns the path of the output file containing the backup of the key.</span></span>

## <span data-ttu-id="7d5fe-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7d5fe-151">NOTES</span></span>

## <span data-ttu-id="7d5fe-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d5fe-152">RELATED LINKS</span></span>

[<span data-ttu-id="7d5fe-153">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7d5fe-153">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="7d5fe-154">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7d5fe-154">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="7d5fe-155">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7d5fe-155">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="7d5fe-156">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7d5fe-156">Restore-AzureKeyVaultSecret</span></span>](./Restore-AzureKeyVaultSecret.md)

