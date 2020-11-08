---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsm.md
ms.openlocfilehash: 5353adade342b7f73cf60ff6b0befa88f4a3da73
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115320"
---
# <span data-ttu-id="d55b1-101">Backup-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="d55b1-101">Backup-AzManagedHsm</span></span>

## <span data-ttu-id="d55b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d55b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d55b1-103">Fazer backup completo de um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="d55b1-103">Fully backup a managed HSM.</span></span>

## <span data-ttu-id="d55b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d55b1-104">SYNTAX</span></span>

### <span data-ttu-id="d55b1-105">InteractiveStorageName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d55b1-105">InteractiveStorageName (Default)</span></span>
```
Backup-AzManagedHsm [-Name] <String> -StorageAccountName <String> -StorageContainerName <String>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d55b1-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="d55b1-106">InteractiveStorageUri</span></span>
```
Backup-AzManagedHsm [-Name] <String> -StorageContainerUri <Uri> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d55b1-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="d55b1-107">InputObjectStorageUri</span></span>
```
Backup-AzManagedHsm -StorageContainerUri <Uri> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d55b1-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="d55b1-108">InputObjectStorageName</span></span>
```
Backup-AzManagedHsm -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d55b1-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d55b1-109">DESCRIPTION</span></span>
<span data-ttu-id="d55b1-110">Fazer backup completo de um HSM gerenciado para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d55b1-110">Fully backup a managed HSM to a storage account.</span></span>
<span data-ttu-id="d55b1-111">Use `Restore-AzManagedHsm` para restaurar o backup.</span><span class="sxs-lookup"><span data-stu-id="d55b1-111">Use `Restore-AzManagedHsm` to restore the backup.</span></span>

## <span data-ttu-id="d55b1-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d55b1-112">EXAMPLES</span></span>

### <span data-ttu-id="d55b1-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d55b1-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"

PS C:\> Backup-AzManagedHsm -Name myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -SasToken $sasToken

https://{accountName}.blob.core.windows.net/{containerName}/{backupFolder}
```

<span data-ttu-id="d55b1-114">O cmdlet criará uma pasta (geralmente nomeada `mhsm-{name}-{timestamp}` ) no contêiner de armazenamento, armazenará o backup nessa pasta e produzirá o URI da pasta.</span><span class="sxs-lookup"><span data-stu-id="d55b1-114">The cmdlet will create a folder (typically named `mhsm-{name}-{timestamp}`) in the storage container, store the backup in that folder and output the folder URI.</span></span>

## <span data-ttu-id="d55b1-115">OS</span><span class="sxs-lookup"><span data-stu-id="d55b1-115">PARAMETERS</span></span>

### <span data-ttu-id="d55b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d55b1-116">-DefaultProfile</span></span>
<span data-ttu-id="d55b1-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d55b1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d55b1-118">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="d55b1-118">-HsmObject</span></span>
<span data-ttu-id="d55b1-119">Objeto HSM gerenciado</span><span class="sxs-lookup"><span data-stu-id="d55b1-119">Managed HSM object</span></span>

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

### <span data-ttu-id="d55b1-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d55b1-120">-Name</span></span>
<span data-ttu-id="d55b1-121">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="d55b1-121">Name of the HSM.</span></span>

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

### <span data-ttu-id="d55b1-122">-SasToken</span><span class="sxs-lookup"><span data-stu-id="d55b1-122">-SasToken</span></span>
<span data-ttu-id="d55b1-123">O token de assinatura de acesso compartilhado (SAS) para autenticar a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d55b1-123">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="d55b1-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d55b1-124">-StorageAccountName</span></span>
<span data-ttu-id="d55b1-125">Nome da conta de armazenamento na qual o backup será armazenado.</span><span class="sxs-lookup"><span data-stu-id="d55b1-125">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="d55b1-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="d55b1-126">-StorageContainerName</span></span>
<span data-ttu-id="d55b1-127">Nome do contêiner de BLOB em que o backup será armazenado.</span><span class="sxs-lookup"><span data-stu-id="d55b1-127">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="d55b1-128">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="d55b1-128">-StorageContainerUri</span></span>
<span data-ttu-id="d55b1-129">URI do contêiner de armazenamento em que o backup será armazenado.</span><span class="sxs-lookup"><span data-stu-id="d55b1-129">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="d55b1-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d55b1-130">-Confirm</span></span>
<span data-ttu-id="d55b1-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d55b1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d55b1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d55b1-132">-WhatIf</span></span>
<span data-ttu-id="d55b1-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d55b1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d55b1-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d55b1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d55b1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d55b1-135">CommonParameters</span></span>
<span data-ttu-id="d55b1-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d55b1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d55b1-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d55b1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d55b1-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d55b1-138">INPUTS</span></span>

### <span data-ttu-id="d55b1-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d55b1-139">None</span></span>

## <span data-ttu-id="d55b1-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d55b1-140">OUTPUTS</span></span>

### <span data-ttu-id="d55b1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d55b1-141">System.String</span></span>

## <span data-ttu-id="d55b1-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d55b1-142">NOTES</span></span>

## <span data-ttu-id="d55b1-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d55b1-143">RELATED LINKS</span></span>
