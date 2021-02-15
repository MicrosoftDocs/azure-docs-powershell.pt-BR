---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
ms.openlocfilehash: 51d322ea738a56e4b1fa24cccdb7bb59a6cd0d21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111835"
---
# <span data-ttu-id="620da-101">Backup-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="620da-101">Backup-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="620da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="620da-102">SYNOPSIS</span></span>
<span data-ttu-id="620da-103">Fazer o back up de um certificado em um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="620da-103">Backs up a certificate in a key vault.</span></span>

## <span data-ttu-id="620da-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="620da-104">SYNTAX</span></span>

### <span data-ttu-id="620da-105">ByCertificateName (Default)</span><span class="sxs-lookup"><span data-stu-id="620da-105">ByCertificateName (Default)</span></span>
```
Backup-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="620da-106">ByCertificate</span><span class="sxs-lookup"><span data-stu-id="620da-106">ByCertificate</span></span>
```
Backup-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="620da-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="620da-107">DESCRIPTION</span></span>
<span data-ttu-id="620da-108">O cmdlet **Backup-AzKeyVaultCertificate** faz backup de um certificado especificado em um cofre de teclas baixando-o e armazenar-o em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="620da-108">The **Backup-AzKeyVaultCertificate** cmdlet backs up a specified certificate in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="620da-109">Se o certificado tiver várias versões, todas as suas versões serão incluídas no backup.</span><span class="sxs-lookup"><span data-stu-id="620da-109">If the certificate has multiple versions, all its versions will be included in the backup.</span></span>
<span data-ttu-id="620da-110">Como o conteúdo baixado é criptografado, ele não pode ser usado fora do Cofre de Teclas do Azure.</span><span class="sxs-lookup"><span data-stu-id="620da-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="620da-111">Você pode restaurar um certificado em backup para qualquer cofre de chave na assinatura da onde ele foi feito backup, desde que o cofre se mantenha na mesma geografia do Azure.</span><span class="sxs-lookup"><span data-stu-id="620da-111">You can restore a backed-up certificate to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="620da-112">Os motivos típicos para usar este cmdlet são:</span><span class="sxs-lookup"><span data-stu-id="620da-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="620da-113">Você deseja manter uma cópia offline do certificado caso exclua acidentalmente o original do cofre.</span><span class="sxs-lookup"><span data-stu-id="620da-113">You want to retain an offline copy of the certificate in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="620da-114">Você criou um certificado usando o Cofre de Teclas e agora deseja clonar o objeto em uma região diferente do Azure, para poder usá-lo em todas as instâncias do aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="620da-114">You created a certificate using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="620da-115">Use o cmdlet **Backup-AzKeyVaultCertificate** para recuperar o certificado em formato criptografado e use o cmdlet **Restore-AzKeyVaultCertificate** e especifique um cofre de chave na segunda região.</span><span class="sxs-lookup"><span data-stu-id="620da-115">Use the **Backup-AzKeyVaultCertificate** cmdlet to retrieve the certificate in encrypted format and then use the **Restore-AzKeyVaultCertificate** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="620da-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="620da-116">EXAMPLES</span></span>

### <span data-ttu-id="620da-117">Exemplo 1: Fazer o back up de um certificado com um nome de arquivo gerado automaticamente</span><span class="sxs-lookup"><span data-stu-id="620da-117">Example 1: Back up a certificate with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

<span data-ttu-id="620da-118">Esse comando recupera o certificado MyCert do cofre de chave chamado MyKeyVault e salva um backup desse certificado em um arquivo que é nomeado automaticamente para você e exibe o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="620da-118">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="620da-119">Exemplo 2: Fazer o back up de um certificado para um nome de arquivo especificado</span><span class="sxs-lookup"><span data-stu-id="620da-119">Example 2: Back up a certificate to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="620da-120">Esse comando recupera o certificado MyCert do cofre de chave chamado MyKeyVault e salva um backup desse certificado em um arquivo chamado Backup.blob.</span><span class="sxs-lookup"><span data-stu-id="620da-120">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file named Backup.blob.</span></span>

### <span data-ttu-id="620da-121">Exemplo 3: Fazer o back up de um certificado recuperado anteriormente em um nome de arquivo especificado, sobrescrever o arquivo de destino sem solicitar.</span><span class="sxs-lookup"><span data-stu-id="620da-121">Example 3: Back up a previously retrieved certificate to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $cert = Get-AzKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="620da-122">Esse comando cria um backup do certificado chamado $cert. Nome no cofre chamado $cert. VaultName para um arquivo chamado Backup.blob, sobrescrever silenciosamente o arquivo se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="620da-122">This command creates a backup of the certificate named $cert.Name in the vault named $cert.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="620da-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="620da-123">PARAMETERS</span></span>

### <span data-ttu-id="620da-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="620da-124">-DefaultProfile</span></span>
<span data-ttu-id="620da-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="620da-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="620da-126">-Forçar</span><span class="sxs-lookup"><span data-stu-id="620da-126">-Force</span></span>
<span data-ttu-id="620da-127">Substituir o arquivo determinado se ele existir</span><span class="sxs-lookup"><span data-stu-id="620da-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="620da-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="620da-128">-InputObject</span></span>
<span data-ttu-id="620da-129">Segredo para ser feito backup, com pipeline a partir da saída de uma chamada de recuperação.</span><span class="sxs-lookup"><span data-stu-id="620da-129">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByCertificate
Aliases: Certificate

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="620da-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="620da-130">-Name</span></span>
<span data-ttu-id="620da-131">Nome secreto.</span><span class="sxs-lookup"><span data-stu-id="620da-131">Secret name.</span></span>
<span data-ttu-id="620da-132">O cmdlet constrói o FQDN de um segredo do nome do cofre, do ambiente selecionado no momento e do nome secreto.</span><span class="sxs-lookup"><span data-stu-id="620da-132">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="620da-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="620da-133">-OutputFile</span></span>
<span data-ttu-id="620da-134">Arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="620da-134">Output file.</span></span>
<span data-ttu-id="620da-135">O arquivo de saída para armazenar o backup do certificado.</span><span class="sxs-lookup"><span data-stu-id="620da-135">The output file to store the backup of the certificate.</span></span>
<span data-ttu-id="620da-136">Se não especificado, será gerado um nome de arquivo padrão.</span><span class="sxs-lookup"><span data-stu-id="620da-136">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="620da-137">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="620da-137">-VaultName</span></span>
<span data-ttu-id="620da-138">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="620da-138">Vault name.</span></span>
<span data-ttu-id="620da-139">O Cmdlet construirá o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="620da-139">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="620da-140">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="620da-140">-Confirm</span></span>
<span data-ttu-id="620da-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="620da-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="620da-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="620da-142">-WhatIf</span></span>
<span data-ttu-id="620da-143">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="620da-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="620da-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="620da-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="620da-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="620da-145">CommonParameters</span></span>
<span data-ttu-id="620da-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="620da-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="620da-147">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="620da-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="620da-148">Entradas</span><span class="sxs-lookup"><span data-stu-id="620da-148">INPUTS</span></span>

### <span data-ttu-id="620da-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="620da-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="620da-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="620da-150">OUTPUTS</span></span>

### <span data-ttu-id="620da-151">System.String</span><span class="sxs-lookup"><span data-stu-id="620da-151">System.String</span></span>

## <span data-ttu-id="620da-152">Notas</span><span class="sxs-lookup"><span data-stu-id="620da-152">NOTES</span></span>

## <span data-ttu-id="620da-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="620da-153">RELATED LINKS</span></span>
