---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVault.md
ms.openlocfilehash: 7d2bb9d961b5fba7ecd5e0d83f8d86ac1a930c75
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111840"
---
# <span data-ttu-id="fd2d2-101">Backup-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="fd2d2-101">Backup-AzKeyVault</span></span>

## <span data-ttu-id="fd2d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd2d2-102">SYNOPSIS</span></span>
<span data-ttu-id="fd2d2-103">Faça backup completo de um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="fd2d2-103">Fully backup a managed HSM.</span></span>

## <span data-ttu-id="fd2d2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd2d2-104">SYNTAX</span></span>

### <span data-ttu-id="fd2d2-105">InteractiveStorageName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fd2d2-105">InteractiveStorageName (Default)</span></span>
```
Backup-AzKeyVault [-HsmName] <String> -StorageAccountName <String> -StorageContainerName <String>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd2d2-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="fd2d2-106">InteractiveStorageUri</span></span>
```
Backup-AzKeyVault [-HsmName] <String> -StorageContainerUri <Uri> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd2d2-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="fd2d2-107">InputObjectStorageUri</span></span>
```
Backup-AzKeyVault -StorageContainerUri <Uri> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd2d2-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="fd2d2-108">InputObjectStorageName</span></span>
```
Backup-AzKeyVault -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd2d2-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd2d2-109">DESCRIPTION</span></span>
<span data-ttu-id="fd2d2-110">Faça backup completo de um HSM gerenciado em uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fd2d2-110">Fully backup a managed HSM to a storage account.</span></span>
<span data-ttu-id="fd2d2-111">Use `Restore-AzKeyVault` para restaurar o backup.</span><span class="sxs-lookup"><span data-stu-id="fd2d2-111">Use `Restore-AzKeyVault` to restore the backup.</span></span>

## <span data-ttu-id="fd2d2-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fd2d2-112">EXAMPLES</span></span>

### <span data-ttu-id="fd2d2-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fd2d2-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"

PS C:\> Backup-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -SasToken $sasToken

https://{accountName}.blob.core.windows.net/{containerName}/{backupFolder}
```

<span data-ttu-id="fd2d2-114">O cmdlet criará uma pasta (normalmente nomeada) no contêiner de armazenamento, armazenará o backup nessa pasta e gerará a saída do `mhsm-{name}-{timestamp}` URI da pasta.</span><span class="sxs-lookup"><span data-stu-id="fd2d2-114">The cmdlet will create a folder (typically named `mhsm-{name}-{timestamp}`) in the storage container, store the backup in that folder and output the folder URI.</span></span>

## <span data-ttu-id="fd2d2-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd2d2-115">PARAMETERS</span></span>

### <span data-ttu-id="fd2d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd2d2-116">-DefaultProfile</span></span>
<span data-ttu-id="fd2d2-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fd2d2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd2d2-118">-HsmName</span><span class="sxs-lookup"><span data-stu-id="fd2d2-118">-HsmName</span></span>
<span data-ttu-id="fd2d2-119">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="fd2d2-119">Name of the HSM.</span></span>

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

### <span data-ttu-id="fd2d2-120">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="fd2d2-120">-HsmObject</span></span>
<span data-ttu-id="fd2d2-121">Objeto HSM gerenciado</span><span class="sxs-lookup"><span data-stu-id="fd2d2-121">Managed HSM object</span></span>

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

### <span data-ttu-id="fd2d2-122">-SasToken</span><span class="sxs-lookup"><span data-stu-id="fd2d2-122">-SasToken</span></span>
<span data-ttu-id="fd2d2-123">O token de assinatura de acesso compartilhado (SAS) para autenticar a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fd2d2-123">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="fd2d2-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fd2d2-124">-StorageAccountName</span></span>
<span data-ttu-id="fd2d2-125">Nome da conta de armazenamento onde o backup será armazenado.</span><span class="sxs-lookup"><span data-stu-id="fd2d2-125">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="fd2d2-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="fd2d2-126">-StorageContainerName</span></span>
<span data-ttu-id="fd2d2-127">Nome do contêiner de blob onde o backup será armazenado.</span><span class="sxs-lookup"><span data-stu-id="fd2d2-127">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="fd2d2-128">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="fd2d2-128">-StorageContainerUri</span></span>
<span data-ttu-id="fd2d2-129">URI do contêiner de armazenamento onde o backup será armazenado.</span><span class="sxs-lookup"><span data-stu-id="fd2d2-129">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="fd2d2-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fd2d2-130">-Confirm</span></span>
<span data-ttu-id="fd2d2-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd2d2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd2d2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd2d2-132">-WhatIf</span></span>
<span data-ttu-id="fd2d2-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fd2d2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd2d2-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fd2d2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd2d2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd2d2-135">CommonParameters</span></span>
<span data-ttu-id="fd2d2-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd2d2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd2d2-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd2d2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd2d2-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="fd2d2-138">INPUTS</span></span>

### <span data-ttu-id="fd2d2-139">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fd2d2-139">None</span></span>

## <span data-ttu-id="fd2d2-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="fd2d2-140">OUTPUTS</span></span>

### <span data-ttu-id="fd2d2-141">System.String</span><span class="sxs-lookup"><span data-stu-id="fd2d2-141">System.String</span></span>

## <span data-ttu-id="fd2d2-142">Notas</span><span class="sxs-lookup"><span data-stu-id="fd2d2-142">NOTES</span></span>

## <span data-ttu-id="fd2d2-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd2d2-143">RELATED LINKS</span></span>
