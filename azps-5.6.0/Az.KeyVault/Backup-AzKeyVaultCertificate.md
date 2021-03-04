---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
ms.openlocfilehash: e4692d9b623ce285a2be50d51a450fd8da39a5ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887506"
---
# <span data-ttu-id="f2501-101">Backup-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f2501-101">Backup-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="f2501-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2501-102">SYNOPSIS</span></span>
<span data-ttu-id="f2501-103">Backs up a certificate in a key vault.</span><span class="sxs-lookup"><span data-stu-id="f2501-103">Backs up a certificate in a key vault.</span></span>

## <span data-ttu-id="f2501-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f2501-104">SYNTAX</span></span>

### <span data-ttu-id="f2501-105">ByCertificateName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f2501-105">ByCertificateName (Default)</span></span>
```
Backup-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2501-106">ByCertificate</span><span class="sxs-lookup"><span data-stu-id="f2501-106">ByCertificate</span></span>
```
Backup-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2501-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f2501-107">DESCRIPTION</span></span>
<span data-ttu-id="f2501-108">O cmdlet **Backup-AzKeyVaultCertificate** faz backup de um certificado especificado em um cofre de chaves baixando-o e armazenar-o em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="f2501-108">The **Backup-AzKeyVaultCertificate** cmdlet backs up a specified certificate in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="f2501-109">Se o certificado tiver várias versões, todas as versões serão incluídas no backup.</span><span class="sxs-lookup"><span data-stu-id="f2501-109">If the certificate has multiple versions, all its versions will be included in the backup.</span></span>
<span data-ttu-id="f2501-110">Como o conteúdo baixado é criptografado, ele não pode ser usado fora do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f2501-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="f2501-111">Você pode restaurar um certificado com backup em qualquer cofre de chaves na assinatura da assinatura da onde ele foi feito backup, desde que o cofre seja na mesma geografia do Azure.</span><span class="sxs-lookup"><span data-stu-id="f2501-111">You can restore a backed-up certificate to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="f2501-112">Os motivos típicos para usar esse cmdlet são:</span><span class="sxs-lookup"><span data-stu-id="f2501-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="f2501-113">Você deseja manter uma cópia offline do certificado caso exclua acidentalmente o original do cofre.</span><span class="sxs-lookup"><span data-stu-id="f2501-113">You want to retain an offline copy of the certificate in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="f2501-114">Você criou um certificado usando o Cofre de Chaves e agora deseja clonar o objeto em uma região diferente do Azure, para que você possa usá-lo de todas as instâncias do seu aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="f2501-114">You created a certificate using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="f2501-115">Use o cmdlet **Backup-AzKeyVaultCertificate** para recuperar o certificado em formato criptografado e, em seguida, use o cmdlet **Restore-AzKeyVaultCertificate** e especifique um cofre de chaves na segunda região.</span><span class="sxs-lookup"><span data-stu-id="f2501-115">Use the **Backup-AzKeyVaultCertificate** cmdlet to retrieve the certificate in encrypted format and then use the **Restore-AzKeyVaultCertificate** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="f2501-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2501-116">EXAMPLES</span></span>

### <span data-ttu-id="f2501-117">Exemplo 1: Fazer o back up de um certificado com um nome de arquivo gerado automaticamente</span><span class="sxs-lookup"><span data-stu-id="f2501-117">Example 1: Back up a certificate with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

<span data-ttu-id="f2501-118">Este comando recupera o certificado chamado MyCert do cofre de chaves chamado MyKeyVault e salva um backup desse certificado em um arquivo que é nomeado automaticamente para você e exibe o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f2501-118">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="f2501-119">Exemplo 2: Fazer o back up de um certificado para um nome de arquivo especificado</span><span class="sxs-lookup"><span data-stu-id="f2501-119">Example 2: Back up a certificate to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="f2501-120">Este comando recupera o certificado chamado MyCert do cofre de chaves chamado MyKeyVault e salva um backup desse certificado em um arquivo chamado Backup.blob.</span><span class="sxs-lookup"><span data-stu-id="f2501-120">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file named Backup.blob.</span></span>

### <span data-ttu-id="f2501-121">Exemplo 3: Fazer o back up de um certificado recuperado anteriormente para um nome de arquivo especificado, sobrescrevendo o arquivo de destino sem solicitar.</span><span class="sxs-lookup"><span data-stu-id="f2501-121">Example 3: Back up a previously retrieved certificate to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $cert = Get-AzKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="f2501-122">Este comando cria um backup do certificado chamado $cert. Nome no cofre chamado $cert. VaultName para um arquivo chamado Backup.blob, sobrescrevendo silenciosamente o arquivo se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="f2501-122">This command creates a backup of the certificate named $cert.Name in the vault named $cert.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="f2501-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f2501-123">PARAMETERS</span></span>

### <span data-ttu-id="f2501-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2501-124">-DefaultProfile</span></span>
<span data-ttu-id="f2501-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2501-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2501-126">-Force</span><span class="sxs-lookup"><span data-stu-id="f2501-126">-Force</span></span>
<span data-ttu-id="f2501-127">Substituir o arquivo determinado se ele existir</span><span class="sxs-lookup"><span data-stu-id="f2501-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="f2501-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2501-128">-InputObject</span></span>
<span data-ttu-id="f2501-129">Segredo a ser feito backup, canalizou a partir da saída de uma chamada de recuperação.</span><span class="sxs-lookup"><span data-stu-id="f2501-129">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="f2501-130">-Name</span><span class="sxs-lookup"><span data-stu-id="f2501-130">-Name</span></span>
<span data-ttu-id="f2501-131">Nome secreto.</span><span class="sxs-lookup"><span data-stu-id="f2501-131">Secret name.</span></span>
<span data-ttu-id="f2501-132">O cmdlet constrói o FQDN de um segredo do nome do cofre, do ambiente selecionado no momento e do nome secreto.</span><span class="sxs-lookup"><span data-stu-id="f2501-132">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="f2501-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="f2501-133">-OutputFile</span></span>
<span data-ttu-id="f2501-134">Arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="f2501-134">Output file.</span></span>
<span data-ttu-id="f2501-135">O arquivo de saída para armazenar o backup do certificado.</span><span class="sxs-lookup"><span data-stu-id="f2501-135">The output file to store the backup of the certificate.</span></span>
<span data-ttu-id="f2501-136">Se não for especificado, um nome de arquivo padrão será gerado.</span><span class="sxs-lookup"><span data-stu-id="f2501-136">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="f2501-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f2501-137">-VaultName</span></span>
<span data-ttu-id="f2501-138">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="f2501-138">Vault name.</span></span>
<span data-ttu-id="f2501-139">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="f2501-139">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="f2501-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2501-140">-Confirm</span></span>
<span data-ttu-id="f2501-141">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2501-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2501-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2501-142">-WhatIf</span></span>
<span data-ttu-id="f2501-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f2501-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2501-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f2501-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2501-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2501-145">CommonParameters</span></span>
<span data-ttu-id="f2501-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2501-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2501-147">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2501-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2501-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2501-148">INPUTS</span></span>

### <span data-ttu-id="f2501-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f2501-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="f2501-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f2501-150">OUTPUTS</span></span>

### <span data-ttu-id="f2501-151">System.String</span><span class="sxs-lookup"><span data-stu-id="f2501-151">System.String</span></span>

## <span data-ttu-id="f2501-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="f2501-152">NOTES</span></span>

## <span data-ttu-id="f2501-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2501-153">RELATED LINKS</span></span>
