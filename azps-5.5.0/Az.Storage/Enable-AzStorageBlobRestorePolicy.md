---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: a5b5b1c761bb6e3c23a5dd5f0525d2d6627b3ab2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112517"
---
# <span data-ttu-id="12cbc-101">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="12cbc-101">Enable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="12cbc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12cbc-102">SYNOPSIS</span></span>
<span data-ttu-id="12cbc-103">Habilita a Política de Restauração de Blob em uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="12cbc-103">Enables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="12cbc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12cbc-104">SYNTAX</span></span>

### <span data-ttu-id="12cbc-105">Nomeda Conta (Padrão)</span><span class="sxs-lookup"><span data-stu-id="12cbc-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RestoreDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12cbc-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="12cbc-106">AccountObject</span></span>
```
Enable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12cbc-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="12cbc-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceId] <String> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12cbc-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="12cbc-108">DESCRIPTION</span></span>
<span data-ttu-id="12cbc-109">O cmdlet **Enable-AzStorageBstorePolicy** habilita a Política de Restauração de Blob para o serviço blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="12cbc-109">The **Enable-AzStorageBlobRestorePolicy** cmdlet enables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="12cbc-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="12cbc-110">EXAMPLES</span></span>

### <span data-ttu-id="12cbc-111">Exemplo 1: Habilita a Política de Restauração de Blob para o serviço blob de armazenamento do Azure em uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="12cbc-111">Example 1: Enables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" $accountName -RetentionDays 5

PS C:\> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -EnableChangeFeed $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegoup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : True
DeleteRetentionPolicy.Days    : 5
RestorePolicy.Enabled         : False
RestorePolicy.Days            : 
RestorePolicy.MinRestoreTime  : 
ChangeFeed                    : True
IsVersioningEnabled           : True

PS C:\> Enable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -RestoreDays 4

PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegoup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : True
DeleteRetentionPolicy.Days    : 5
RestorePolicy.Enabled         : True
RestorePolicy.Days            : 4
RestorePolicy.MinRestoreTime  : 8/28/2020 6:00:59 AM
ChangeFeed                    : True
IsVersioningEnabled           : True
```

<span data-ttu-id="12cbc-112">Primeiro, esse comando habilita o blob softdelete e o changefeed, depois habilita a Política de Restauração de Blob e, por fim, verifique a configuração nas propriedades do serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="12cbc-112">This command first enable Blob softdelete and changefeed, then enables Blob Restore Policy, finally check the setting in Blob service properties.</span></span>
<span data-ttu-id="12cbc-113">O serviço Blob RestorePolicy.Days deve ser menor que DeleteRetentionPolicy.Days.</span><span class="sxs-lookup"><span data-stu-id="12cbc-113">The Blob service RestorePolicy.Days must be smaller than DeleteRetentionPolicy.Days.</span></span>
<span data-ttu-id="12cbc-114">O blob softdelete e o ChangeFeed devem ser habilitados antes de habilitar a Política de Restauração de Blob.</span><span class="sxs-lookup"><span data-stu-id="12cbc-114">Blob softdelete and ChangeFeed must be enabled before enable blob Restore Policy.</span></span>
<span data-ttu-id="12cbc-115">Se o softdelete e o ChangeFeed estão apenas habilitados, talvez seja necessário aguardar algum tempo para o servidor lidar com a configuração, antes de habilitar a política de restauração de Blob.</span><span class="sxs-lookup"><span data-stu-id="12cbc-115">If softdelete and Changefeed are just enabled, might need wait for some time for server to handle the setting, before enable Blob restore policy.</span></span>

## <span data-ttu-id="12cbc-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12cbc-116">PARAMETERS</span></span>

### <span data-ttu-id="12cbc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12cbc-117">-DefaultProfile</span></span>
<span data-ttu-id="12cbc-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12cbc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12cbc-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12cbc-119">-PassThru</span></span>
<span data-ttu-id="12cbc-120">Exibir ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="12cbc-120">Display ServiceProperties</span></span>

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

### <span data-ttu-id="12cbc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12cbc-121">-ResourceGroupName</span></span>
<span data-ttu-id="12cbc-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="12cbc-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12cbc-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12cbc-123">-ResourceId</span></span>
<span data-ttu-id="12cbc-124">Inserir uma ID de Recurso de conta de armazenamento ou uma ID de recurso de propriedades do serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="12cbc-124">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12cbc-125">-RestoreDays</span><span class="sxs-lookup"><span data-stu-id="12cbc-125">-RestoreDays</span></span>
<span data-ttu-id="12cbc-126">Define o número de dias para que a blob possa ser restaurada..</span><span class="sxs-lookup"><span data-stu-id="12cbc-126">Sets the number of days for the blob can be restored..</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12cbc-127">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="12cbc-127">-StorageAccount</span></span>
<span data-ttu-id="12cbc-128">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="12cbc-128">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12cbc-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="12cbc-129">-StorageAccountName</span></span>
<span data-ttu-id="12cbc-130">Nome da Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="12cbc-130">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12cbc-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="12cbc-131">-Confirm</span></span>
<span data-ttu-id="12cbc-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12cbc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12cbc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12cbc-133">-WhatIf</span></span>
<span data-ttu-id="12cbc-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="12cbc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12cbc-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="12cbc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12cbc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12cbc-136">CommonParameters</span></span>
<span data-ttu-id="12cbc-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12cbc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12cbc-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12cbc-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12cbc-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="12cbc-139">INPUTS</span></span>

### <span data-ttu-id="12cbc-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="12cbc-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="12cbc-141">System.String</span><span class="sxs-lookup"><span data-stu-id="12cbc-141">System.String</span></span>

## <span data-ttu-id="12cbc-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="12cbc-142">OUTPUTS</span></span>

### <span data-ttu-id="12cbc-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="12cbc-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="12cbc-144">Notas</span><span class="sxs-lookup"><span data-stu-id="12cbc-144">NOTES</span></span>

## <span data-ttu-id="12cbc-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12cbc-145">RELATED LINKS</span></span>
