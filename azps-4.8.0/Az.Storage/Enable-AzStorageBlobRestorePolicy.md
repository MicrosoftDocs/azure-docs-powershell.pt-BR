---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: a5b5b1c761bb6e3c23a5dd5f0525d2d6627b3ab2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93956135"
---
# <span data-ttu-id="db3b8-101">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="db3b8-101">Enable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="db3b8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db3b8-102">SYNOPSIS</span></span>
<span data-ttu-id="db3b8-103">Habilita a política de restauração de BLOB em uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="db3b8-103">Enables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="db3b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db3b8-104">SYNTAX</span></span>

### <span data-ttu-id="db3b8-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="db3b8-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RestoreDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db3b8-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="db3b8-106">AccountObject</span></span>
```
Enable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db3b8-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="db3b8-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceId] <String> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db3b8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db3b8-108">DESCRIPTION</span></span>
<span data-ttu-id="db3b8-109">O cmdlet **Enable-AzStorageBlobRestorePolicy** habilita a política de restauração de BLOB para o serviço de blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="db3b8-109">The **Enable-AzStorageBlobRestorePolicy** cmdlet enables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="db3b8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db3b8-110">EXAMPLES</span></span>

### <span data-ttu-id="db3b8-111">Exemplo 1: habilita a política de restauração de BLOB para o serviço de blob de armazenamento do Azure em uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="db3b8-111">Example 1: Enables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
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

<span data-ttu-id="db3b8-112">Esse comando primeiro habilite blob SoftDelete e changefeed e, em seguida, habilite a política de restauração de BLOB, por fim, verifique a configuração nas propriedades do serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="db3b8-112">This command first enable Blob softdelete and changefeed, then enables Blob Restore Policy, finally check the setting in Blob service properties.</span></span>
<span data-ttu-id="db3b8-113">O serviço blob RestorePolicy. Days deve ser menor do que DeleteRetentionPolicy. Days.</span><span class="sxs-lookup"><span data-stu-id="db3b8-113">The Blob service RestorePolicy.Days must be smaller than DeleteRetentionPolicy.Days.</span></span>
<span data-ttu-id="db3b8-114">Blob SoftDelete e ChangeFeed devem ser habilitados antes de habilitar a política de restauração de BLOB.</span><span class="sxs-lookup"><span data-stu-id="db3b8-114">Blob softdelete and ChangeFeed must be enabled before enable blob Restore Policy.</span></span>
<span data-ttu-id="db3b8-115">Se SoftDelete e changefeed estiverem habilitados, talvez seja necessário esperar por algum tempo para que o servidor manipule a configuração antes de habilitar a política de restauração de BLOB.</span><span class="sxs-lookup"><span data-stu-id="db3b8-115">If softdelete and Changefeed are just enabled, might need wait for some time for server to handle the setting, before enable Blob restore policy.</span></span>

## <span data-ttu-id="db3b8-116">OS</span><span class="sxs-lookup"><span data-stu-id="db3b8-116">PARAMETERS</span></span>

### <span data-ttu-id="db3b8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db3b8-117">-DefaultProfile</span></span>
<span data-ttu-id="db3b8-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db3b8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db3b8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db3b8-119">-PassThru</span></span>
<span data-ttu-id="db3b8-120">Display Serviceproperties</span><span class="sxs-lookup"><span data-stu-id="db3b8-120">Display ServiceProperties</span></span>

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

### <span data-ttu-id="db3b8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db3b8-121">-ResourceGroupName</span></span>
<span data-ttu-id="db3b8-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="db3b8-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="db3b8-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db3b8-123">-ResourceId</span></span>
<span data-ttu-id="db3b8-124">Insira uma ID de recurso da conta de armazenamento ou uma ID do recurso de propriedades do serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="db3b8-124">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="db3b8-125">-RestoreDays</span><span class="sxs-lookup"><span data-stu-id="db3b8-125">-RestoreDays</span></span>
<span data-ttu-id="db3b8-126">Define o número de dias para o blob poder ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="db3b8-126">Sets the number of days for the blob can be restored..</span></span>

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

### <span data-ttu-id="db3b8-127">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="db3b8-127">-StorageAccount</span></span>
<span data-ttu-id="db3b8-128">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="db3b8-128">Storage account object</span></span>

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

### <span data-ttu-id="db3b8-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="db3b8-129">-StorageAccountName</span></span>
<span data-ttu-id="db3b8-130">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="db3b8-130">Storage Account Name.</span></span>

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

### <span data-ttu-id="db3b8-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="db3b8-131">-Confirm</span></span>
<span data-ttu-id="db3b8-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db3b8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db3b8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db3b8-133">-WhatIf</span></span>
<span data-ttu-id="db3b8-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="db3b8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db3b8-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db3b8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db3b8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db3b8-136">CommonParameters</span></span>
<span data-ttu-id="db3b8-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db3b8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db3b8-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db3b8-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db3b8-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db3b8-139">INPUTS</span></span>

### <span data-ttu-id="db3b8-140">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="db3b8-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="db3b8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="db3b8-141">System.String</span></span>

## <span data-ttu-id="db3b8-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db3b8-142">OUTPUTS</span></span>

### <span data-ttu-id="db3b8-143">Microsoft. Azure. Commands. Management. Storage. Models. PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="db3b8-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="db3b8-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db3b8-144">NOTES</span></span>

## <span data-ttu-id="db3b8-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db3b8-145">RELATED LINKS</span></span>
