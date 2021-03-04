---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/enable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: cd3a8b12b6dbd6aec6dbc157aa3ff4d4ce398002
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888054"
---
# <span data-ttu-id="39321-101">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="39321-101">Enable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="39321-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39321-102">SYNOPSIS</span></span>
<span data-ttu-id="39321-103">Habilita a Política de Restauração de Blob em uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="39321-103">Enables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="39321-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="39321-104">SYNTAX</span></span>

### <span data-ttu-id="39321-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="39321-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RestoreDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39321-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="39321-106">AccountObject</span></span>
```
Enable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39321-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="39321-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceId] <String> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39321-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="39321-108">DESCRIPTION</span></span>
<span data-ttu-id="39321-109">O cmdlet **Enable-AzStorageBlobRestorePolicy** habilita a Política de Restauração de Blob para o serviço blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="39321-109">The **Enable-AzStorageBlobRestorePolicy** cmdlet enables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="39321-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="39321-110">EXAMPLES</span></span>

### <span data-ttu-id="39321-111">Exemplo 1: Habilita a Política de Restauração de Blob para o serviço blob de armazenamento do Azure em uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="39321-111">Example 1: Enables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
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

<span data-ttu-id="39321-112">Este comando primeiro habilita o Blob softdelete e changefeed, depois habilita a Política de Restauração de Blob e, finalmente, verifica a configuração nas propriedades do serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="39321-112">This command first enable Blob softdelete and changefeed, then enables Blob Restore Policy, finally check the setting in Blob service properties.</span></span>
<span data-ttu-id="39321-113">O serviço Blob RestorePolicy.Days deve ser menor que DeleteRetentionPolicy.Days.</span><span class="sxs-lookup"><span data-stu-id="39321-113">The Blob service RestorePolicy.Days must be smaller than DeleteRetentionPolicy.Days.</span></span>
<span data-ttu-id="39321-114">Blob softdelete e ChangeFeed devem ser habilitados antes de habilitar a Política de Restauração de blob.</span><span class="sxs-lookup"><span data-stu-id="39321-114">Blob softdelete and ChangeFeed must be enabled before enable blob Restore Policy.</span></span>
<span data-ttu-id="39321-115">Se softdelete e Changefeed estão apenas habilitados, talvez seja necessário aguardar algum tempo para o servidor manipular a configuração, antes de habilitar a política de restauração de Blob.</span><span class="sxs-lookup"><span data-stu-id="39321-115">If softdelete and Changefeed are just enabled, might need wait for some time for server to handle the setting, before enable Blob restore policy.</span></span>

## <span data-ttu-id="39321-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="39321-116">PARAMETERS</span></span>

### <span data-ttu-id="39321-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39321-117">-DefaultProfile</span></span>
<span data-ttu-id="39321-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="39321-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39321-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39321-119">-PassThru</span></span>
<span data-ttu-id="39321-120">Exibir ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="39321-120">Display ServiceProperties</span></span>

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

### <span data-ttu-id="39321-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39321-121">-ResourceGroupName</span></span>
<span data-ttu-id="39321-122">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="39321-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="39321-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39321-123">-ResourceId</span></span>
<span data-ttu-id="39321-124">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span><span class="sxs-lookup"><span data-stu-id="39321-124">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="39321-125">-RestoreDays</span><span class="sxs-lookup"><span data-stu-id="39321-125">-RestoreDays</span></span>
<span data-ttu-id="39321-126">Define o número de dias para que o blob possa ser restaurado..</span><span class="sxs-lookup"><span data-stu-id="39321-126">Sets the number of days for the blob can be restored..</span></span>

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

### <span data-ttu-id="39321-127">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="39321-127">-StorageAccount</span></span>
<span data-ttu-id="39321-128">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="39321-128">Storage account object</span></span>

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

### <span data-ttu-id="39321-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="39321-129">-StorageAccountName</span></span>
<span data-ttu-id="39321-130">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="39321-130">Storage Account Name.</span></span>

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

### <span data-ttu-id="39321-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39321-131">-Confirm</span></span>
<span data-ttu-id="39321-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39321-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39321-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39321-133">-WhatIf</span></span>
<span data-ttu-id="39321-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="39321-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39321-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="39321-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39321-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39321-136">CommonParameters</span></span>
<span data-ttu-id="39321-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39321-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39321-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39321-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39321-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39321-139">INPUTS</span></span>

### <span data-ttu-id="39321-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39321-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="39321-141">System.String</span><span class="sxs-lookup"><span data-stu-id="39321-141">System.String</span></span>

## <span data-ttu-id="39321-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="39321-142">OUTPUTS</span></span>

### <span data-ttu-id="39321-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="39321-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="39321-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="39321-144">NOTES</span></span>

## <span data-ttu-id="39321-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="39321-145">RELATED LINKS</span></span>
