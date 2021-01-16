---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
ms.openlocfilehash: d1cf3757596a56336c25c46bd6c4e38687888d6e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428303"
---
# <span data-ttu-id="a2b49-101">Restore-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="a2b49-101">Restore-AzKeyVault</span></span>

## <span data-ttu-id="a2b49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a2b49-102">SYNOPSIS</span></span>
<span data-ttu-id="a2b49-103">Restaura completamente um HSM gerenciado do backup.</span><span class="sxs-lookup"><span data-stu-id="a2b49-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="a2b49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2b49-104">SYNTAX</span></span>

### <span data-ttu-id="a2b49-105">InteractiveStorageName (padrão)</span><span class="sxs-lookup"><span data-stu-id="a2b49-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] [-HsmName] <String>
 -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2b49-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="a2b49-106">InteractiveStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] [-HsmName] <String>
 -StorageContainerUri <Uri> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2b49-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="a2b49-107">InputObjectStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] -StorageContainerUri <Uri>
 -SasToken <SecureString> -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2b49-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="a2b49-108">InputObjectStorageName</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2b49-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a2b49-109">DESCRIPTION</span></span>
<span data-ttu-id="a2b49-110">Restaura completamente um HSM gerenciado de um backup armazenado em uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a2b49-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="a2b49-111">Use `Backup-AzKeyVault` para fazer backup.</span><span class="sxs-lookup"><span data-stu-id="a2b49-111">Use `Backup-AzKeyVault` to backup.</span></span>

## <span data-ttu-id="a2b49-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a2b49-112">EXAMPLES</span></span>

### <span data-ttu-id="a2b49-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a2b49-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="a2b49-114">O exemplo restaura um backup armazenado em uma pasta chamada "mhsm-myHsm-2020101308504935" de um contêiner de armazenamento "https://{accountName}. blob. Core. Windows. net/{ContainerName}".</span><span class="sxs-lookup"><span data-stu-id="a2b49-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="a2b49-115">OS</span><span class="sxs-lookup"><span data-stu-id="a2b49-115">PARAMETERS</span></span>

### <span data-ttu-id="a2b49-116">-BackupFolder</span><span class="sxs-lookup"><span data-stu-id="a2b49-116">-BackupFolder</span></span>
<span data-ttu-id="a2b49-117">Nome da pasta do backup, por exemplo, ' mhsm-*-2020101309020403 '. Ele também pode ser aninhado como ' backups/mhsm-*-2020101309020403 '.</span><span class="sxs-lookup"><span data-stu-id="a2b49-117">Folder name of the backup, e.g. 'mhsm-*-2020101309020403'. It can also be nested such as 'backups/mhsm-*-2020101309020403'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2b49-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2b49-118">-DefaultProfile</span></span>
<span data-ttu-id="a2b49-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a2b49-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2b49-120">-HsmName</span><span class="sxs-lookup"><span data-stu-id="a2b49-120">-HsmName</span></span>
<span data-ttu-id="a2b49-121">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="a2b49-121">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InteractiveStorageUri
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2b49-122">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="a2b49-122">-HsmObject</span></span>
<span data-ttu-id="a2b49-123">Objeto HSM gerenciado</span><span class="sxs-lookup"><span data-stu-id="a2b49-123">Managed HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectStorageUri, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2b49-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="a2b49-124">-KeyName</span></span>
<span data-ttu-id="a2b49-125">Nome da chave a ser restaurada.</span><span class="sxs-lookup"><span data-stu-id="a2b49-125">Key name to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2b49-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2b49-126">-PassThru</span></span>
<span data-ttu-id="a2b49-127">Retorne verdadeiro quando o HSM for restaurado.</span><span class="sxs-lookup"><span data-stu-id="a2b49-127">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="a2b49-128">-SasToken</span><span class="sxs-lookup"><span data-stu-id="a2b49-128">-SasToken</span></span>
<span data-ttu-id="a2b49-129">O token de assinatura de acesso compartilhado (SAS) para autenticar a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a2b49-129">The shared access signature (SAS) token to authenticate the storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2b49-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a2b49-130">-StorageAccountName</span></span>
<span data-ttu-id="a2b49-131">Nome da conta de armazenamento na qual o backup será armazenado.</span><span class="sxs-lookup"><span data-stu-id="a2b49-131">Name of the storage account where the backup is going to be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2b49-132">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="a2b49-132">-StorageContainerName</span></span>
<span data-ttu-id="a2b49-133">Nome do contêiner de BLOB em que o backup será armazenado.</span><span class="sxs-lookup"><span data-stu-id="a2b49-133">Name of the blob container where the backup is going to be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2b49-134">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="a2b49-134">-StorageContainerUri</span></span>
<span data-ttu-id="a2b49-135">URI do contêiner de armazenamento em que o backup será armazenado.</span><span class="sxs-lookup"><span data-stu-id="a2b49-135">URI of the storage container where the backup is going to be stored.</span></span>

```yaml
Type: System.Uri
Parameter Sets: InteractiveStorageUri, InputObjectStorageUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2b49-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a2b49-136">-Confirm</span></span>
<span data-ttu-id="a2b49-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2b49-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2b49-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2b49-138">-WhatIf</span></span>
<span data-ttu-id="a2b49-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a2b49-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2b49-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a2b49-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2b49-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2b49-141">CommonParameters</span></span>
<span data-ttu-id="a2b49-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2b49-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2b49-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2b49-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2b49-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a2b49-144">INPUTS</span></span>

### <span data-ttu-id="a2b49-145">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a2b49-145">None</span></span>

## <span data-ttu-id="a2b49-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a2b49-146">OUTPUTS</span></span>

### <span data-ttu-id="a2b49-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a2b49-147">System.Boolean</span></span>

## <span data-ttu-id="a2b49-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a2b49-148">NOTES</span></span>

## <span data-ttu-id="a2b49-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a2b49-149">RELATED LINKS</span></span>
