---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsm.md
ms.openlocfilehash: 97e5c836d7d6b209d31851264047c6df894d77a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126148"
---
# <span data-ttu-id="97b52-101">Restore-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="97b52-101">Restore-AzManagedHsm</span></span>

## <span data-ttu-id="97b52-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97b52-102">SYNOPSIS</span></span>
<span data-ttu-id="97b52-103">Restaura completamente um HSM gerenciado do backup.</span><span class="sxs-lookup"><span data-stu-id="97b52-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="97b52-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97b52-104">SYNTAX</span></span>

### <span data-ttu-id="97b52-105">InteractiveStorageName (padrão)</span><span class="sxs-lookup"><span data-stu-id="97b52-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] [-Name] <String> -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97b52-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="97b52-106">InteractiveStorageUri</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] [-Name] <String> -StorageContainerUri <Uri>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97b52-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="97b52-107">InputObjectStorageUri</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] -StorageContainerUri <Uri> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97b52-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="97b52-108">InputObjectStorageName</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97b52-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="97b52-109">DESCRIPTION</span></span>
<span data-ttu-id="97b52-110">Restaura completamente um HSM gerenciado de um backup armazenado em uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="97b52-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="97b52-111">Use `Backup-AzManagedHsm` para fazer backup.</span><span class="sxs-lookup"><span data-stu-id="97b52-111">Use `Backup-AzManagedHsm` to backup.</span></span>

## <span data-ttu-id="97b52-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97b52-112">EXAMPLES</span></span>

### <span data-ttu-id="97b52-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="97b52-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzManagedHsm -Name myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="97b52-114">O exemplo restaura um backup armazenado em uma pasta chamada "mhsm-myHsm-2020101308504935" de um contêiner de armazenamento "https://{accountName}. blob. Core. Windows. net/{ContainerName}".</span><span class="sxs-lookup"><span data-stu-id="97b52-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="97b52-115">OS</span><span class="sxs-lookup"><span data-stu-id="97b52-115">PARAMETERS</span></span>

### <span data-ttu-id="97b52-116">-BackupFolder</span><span class="sxs-lookup"><span data-stu-id="97b52-116">-BackupFolder</span></span>
<span data-ttu-id="97b52-117">Nome da pasta do backup, por exemplo, ' mhsm- *-2020101309020403 '. Ele também pode ser aninhado como ' backups/mhsm-* -2020101309020403 '.</span><span class="sxs-lookup"><span data-stu-id="97b52-117">Folder name of the backup, e.g. 'mhsm- *-2020101309020403'. It can also be nested such as 'backups/mhsm-* -2020101309020403'.</span></span>

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

### <span data-ttu-id="97b52-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97b52-118">-DefaultProfile</span></span>
<span data-ttu-id="97b52-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="97b52-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97b52-120">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="97b52-120">-HsmObject</span></span>
<span data-ttu-id="97b52-121">Objeto HSM gerenciado</span><span class="sxs-lookup"><span data-stu-id="97b52-121">Managed HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectStorageUri, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b52-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="97b52-122">-Name</span></span>
<span data-ttu-id="97b52-123">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="97b52-123">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InteractiveStorageUri
Aliases: HsmName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b52-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97b52-124">-PassThru</span></span>
<span data-ttu-id="97b52-125">Retorne verdadeiro quando o HSM for restaurado.</span><span class="sxs-lookup"><span data-stu-id="97b52-125">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="97b52-126">-SasToken</span><span class="sxs-lookup"><span data-stu-id="97b52-126">-SasToken</span></span>
<span data-ttu-id="97b52-127">O token de assinatura de acesso compartilhado (SAS) para autenticar a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="97b52-127">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="97b52-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="97b52-128">-StorageAccountName</span></span>
<span data-ttu-id="97b52-129">Nome da conta de armazenamento na qual o backup será armazenado.</span><span class="sxs-lookup"><span data-stu-id="97b52-129">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="97b52-130">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="97b52-130">-StorageContainerName</span></span>
<span data-ttu-id="97b52-131">Nome do contêiner de BLOB em que o backup será armazenado.</span><span class="sxs-lookup"><span data-stu-id="97b52-131">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="97b52-132">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="97b52-132">-StorageContainerUri</span></span>
<span data-ttu-id="97b52-133">URI do contêiner de armazenamento em que o backup será armazenado.</span><span class="sxs-lookup"><span data-stu-id="97b52-133">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="97b52-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="97b52-134">-Confirm</span></span>
<span data-ttu-id="97b52-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97b52-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97b52-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97b52-136">-WhatIf</span></span>
<span data-ttu-id="97b52-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="97b52-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97b52-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="97b52-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97b52-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b52-139">CommonParameters</span></span>
<span data-ttu-id="97b52-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97b52-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b52-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97b52-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b52-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="97b52-142">INPUTS</span></span>

### <span data-ttu-id="97b52-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="97b52-143">None</span></span>

## <span data-ttu-id="97b52-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="97b52-144">OUTPUTS</span></span>

### <span data-ttu-id="97b52-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="97b52-145">System.Boolean</span></span>

## <span data-ttu-id="97b52-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="97b52-146">NOTES</span></span>

## <span data-ttu-id="97b52-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97b52-147">RELATED LINKS</span></span>
