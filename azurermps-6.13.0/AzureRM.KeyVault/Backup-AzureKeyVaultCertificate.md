---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultCertificate.md
ms.openlocfilehash: 7f75f07ee8f53a57cdb2e359fb4addb51b1d7f76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428110"
---
# <span data-ttu-id="66fb1-101">Backup-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="66fb1-101">Backup-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="66fb1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="66fb1-103">Faz backup de um certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="66fb1-103">Backs up a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66fb1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66fb1-104">SYNTAX</span></span>

### <span data-ttu-id="66fb1-105">ByCertificateName (padrão)</span><span class="sxs-lookup"><span data-stu-id="66fb1-105">ByCertificateName (Default)</span></span>
```
Backup-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66fb1-106">ByCertificate</span><span class="sxs-lookup"><span data-stu-id="66fb1-106">ByCertificate</span></span>
```
Backup-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66fb1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="66fb1-107">DESCRIPTION</span></span>
<span data-ttu-id="66fb1-108">O cmdlet **backup-AzureKeyVaultCertificate** faz backup de um certificado especificado em um cofre de chaves, fazendo o download dele e armazenando-o em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="66fb1-108">The **Backup-AzureKeyVaultCertificate** cmdlet backs up a specified certificate in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="66fb1-109">Se o certificado tiver várias versões, todas as suas versões serão incluídas no backup.</span><span class="sxs-lookup"><span data-stu-id="66fb1-109">If the certificate has multiple versions, all its versions will be included in the backup.</span></span>
<span data-ttu-id="66fb1-110">Como o conteúdo baixado é criptografado, ele não pode ser usado fora do cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="66fb1-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="66fb1-111">Você pode restaurar um certificado de backup para qualquer cofre de chaves na assinatura a partir da qual o backup foi feito, desde que o cofre esteja na mesma Geografia do Azure.</span><span class="sxs-lookup"><span data-stu-id="66fb1-111">You can restore a backed-up certificate to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="66fb1-112">Os motivos típicos para usar este cmdlet são:</span><span class="sxs-lookup"><span data-stu-id="66fb1-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="66fb1-113">Você deseja manter uma cópia offline do certificado caso você exclua acidentalmente o original do cofre.</span><span class="sxs-lookup"><span data-stu-id="66fb1-113">You want to retain an offline copy of the certificate in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="66fb1-114">Você criou um certificado usando o Key Vault e agora deseja clonar o objeto para uma região diferente do Azure, de modo que você possa usá-lo em todas as instâncias do seu aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="66fb1-114">You created a certificate using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="66fb1-115">Use o cmdlet **backup-AzureKeyVaultCertificate** para recuperar o certificado em formato criptografado e, em seguida, use o cmdlet **Restore-AzureKeyVaultCertificate** e especifique um cofre de chaves na segunda região.</span><span class="sxs-lookup"><span data-stu-id="66fb1-115">Use the **Backup-AzureKeyVaultCertificate** cmdlet to retrieve the certificate in encrypted format and then use the **Restore-AzureKeyVaultCertificate** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="66fb1-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="66fb1-116">EXAMPLES</span></span>

### <span data-ttu-id="66fb1-117">Exemplo 1: fazer backup de um certificado com um nome de arquivo gerado automaticamente</span><span class="sxs-lookup"><span data-stu-id="66fb1-117">Example 1: Back up a certificate with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

<span data-ttu-id="66fb1-118">Esse comando recupera o certificado chamado MyCert do cofre de chaves chamado MyKeyVault e salva um backup desse certificado em um arquivo que é automaticamente nomeado para você e exibe o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="66fb1-118">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="66fb1-119">Exemplo 2: fazer backup de um certificado em um nome de arquivo especificado</span><span class="sxs-lookup"><span data-stu-id="66fb1-119">Example 2: Back up a certificate to a specified file name</span></span>
```powershell
PS C:\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="66fb1-120">Esse comando recupera o certificado chamado MyCert do cofre de chaves chamado MyKeyVault e salva um backup desse certificado em um arquivo chamado backup. blob.</span><span class="sxs-lookup"><span data-stu-id="66fb1-120">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file named Backup.blob.</span></span>

### <span data-ttu-id="66fb1-121">Exemplo 3: fazer backup de um certificado recuperado anteriormente em um nome de arquivo especificado, substituindo o arquivo de destino sem solicitação.</span><span class="sxs-lookup"><span data-stu-id="66fb1-121">Example 3: Back up a previously retrieved certificate to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $cert = Get-AzureKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzureKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="66fb1-122">Esse comando cria um backup do certificado chamado $cert. Nome no cofre chamado $cert. Compartimentalizaname para um arquivo chamado backup. blob, substituindo o arquivo silenciosamente se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="66fb1-122">This command creates a backup of the certificate named $cert.Name in the vault named $cert.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="66fb1-123">OS</span><span class="sxs-lookup"><span data-stu-id="66fb1-123">PARAMETERS</span></span>

### <span data-ttu-id="66fb1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66fb1-124">-DefaultProfile</span></span>
<span data-ttu-id="66fb1-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66fb1-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66fb1-126">-Force</span><span class="sxs-lookup"><span data-stu-id="66fb1-126">-Force</span></span>
<span data-ttu-id="66fb1-127">Substituir o arquivo fornecido se ele existir</span><span class="sxs-lookup"><span data-stu-id="66fb1-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="66fb1-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66fb1-128">-InputObject</span></span>
<span data-ttu-id="66fb1-129">Segredo para backup, em pipeline a partir da saída de uma chamada de recuperação.</span><span class="sxs-lookup"><span data-stu-id="66fb1-129">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="66fb1-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="66fb1-130">-Name</span></span>
<span data-ttu-id="66fb1-131">Nome do segredo.</span><span class="sxs-lookup"><span data-stu-id="66fb1-131">Secret name.</span></span>
<span data-ttu-id="66fb1-132">O cmdlet constrói o FQDN de um segredo do nome do cofre, do ambiente selecionado no momento e do nome do segredo.</span><span class="sxs-lookup"><span data-stu-id="66fb1-132">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="66fb1-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="66fb1-133">-OutputFile</span></span>
<span data-ttu-id="66fb1-134">Arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="66fb1-134">Output file.</span></span>
<span data-ttu-id="66fb1-135">O arquivo de saída para armazenar o backup do certificado.</span><span class="sxs-lookup"><span data-stu-id="66fb1-135">The output file to store the backup of the certificate.</span></span>
<span data-ttu-id="66fb1-136">Se não for especificado, um nome de arquivo padrão será gerado.</span><span class="sxs-lookup"><span data-stu-id="66fb1-136">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="66fb1-137">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="66fb1-137">-VaultName</span></span>
<span data-ttu-id="66fb1-138">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="66fb1-138">Vault name.</span></span>
<span data-ttu-id="66fb1-139">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="66fb1-139">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="66fb1-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="66fb1-140">-Confirm</span></span>
<span data-ttu-id="66fb1-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66fb1-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66fb1-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66fb1-142">-WhatIf</span></span>
<span data-ttu-id="66fb1-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="66fb1-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66fb1-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="66fb1-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66fb1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66fb1-145">CommonParameters</span></span>
<span data-ttu-id="66fb1-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66fb1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66fb1-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66fb1-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66fb1-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="66fb1-148">INPUTS</span></span>

### <span data-ttu-id="66fb1-149">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="66fb1-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="66fb1-150">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="66fb1-150">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="66fb1-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="66fb1-151">OUTPUTS</span></span>

### <span data-ttu-id="66fb1-152">System. String</span><span class="sxs-lookup"><span data-stu-id="66fb1-152">System.String</span></span>

## <span data-ttu-id="66fb1-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="66fb1-153">NOTES</span></span>

## <span data-ttu-id="66fb1-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66fb1-154">RELATED LINKS</span></span>