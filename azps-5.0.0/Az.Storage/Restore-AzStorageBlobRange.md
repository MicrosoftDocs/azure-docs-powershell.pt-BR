---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azstorageblobrange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
ms.openlocfilehash: ee8a8bd6a12d3f4aa1dc1624d0dc5c11de972b11
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115787"
---
# <span data-ttu-id="fde13-101">Restore-AzStorageBlobRange</span><span class="sxs-lookup"><span data-stu-id="fde13-101">Restore-AzStorageBlobRange</span></span>

## <span data-ttu-id="fde13-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fde13-102">SYNOPSIS</span></span>
<span data-ttu-id="fde13-103">Restaura uma conta de armazenamento para intervalos de blob específicos.</span><span class="sxs-lookup"><span data-stu-id="fde13-103">Restores a Storage account for specific blob ranges.</span></span>

## <span data-ttu-id="fde13-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fde13-104">SYNTAX</span></span>

### <span data-ttu-id="fde13-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="fde13-105">AccountName (Default)</span></span>
```
Restore-AzStorageBlobRange [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -TimeToRestore <DateTime> [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fde13-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="fde13-106">AccountResourceId</span></span>
```
Restore-AzStorageBlobRange [-ResourceId] <String> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fde13-107">Accountobject</span><span class="sxs-lookup"><span data-stu-id="fde13-107">AccountObject</span></span>
```
Restore-AzStorageBlobRange -StorageAccount <PSStorageAccount> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fde13-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fde13-108">DESCRIPTION</span></span>
<span data-ttu-id="fde13-109">O cmdlet **Restore-AzStorageBlobRange** restaura BLOBs em uma conta de armazenamento para intervalos de blob específicos.</span><span class="sxs-lookup"><span data-stu-id="fde13-109">The **Restore-AzStorageBlobRange** cmdlet restores blobs in a Storage account for specific blob ranges.</span></span>
<span data-ttu-id="fde13-110">O intervalo inicial é incluído, e o intervalo final é excluído na restauração de BLOB.</span><span class="sxs-lookup"><span data-stu-id="fde13-110">The start range is included, and the end range is excluded in blob restore.</span></span>

## <span data-ttu-id="fde13-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fde13-111">EXAMPLES</span></span>

### <span data-ttu-id="fde13-112">Exemplo 1: iniciar restaura BLOBs em uma conta de armazenamento com intervalos de blob específicos</span><span class="sxs-lookup"><span data-stu-id="fde13-112">Example 1: Start restores blobs in a Storage account with specific blob ranges</span></span>
```powershell
PS C:\> $range1 = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
PS C:\> $range2 = New-AzStorageBlobRangeToRestore -StartRange container3/blob3 -EndRange container4/blob4
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddDays(-1) -BlobRestoreRange $range1,$range2

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                     
------     ---------                            ------------- ------------------------     ---------------------                     
InProgress 6ca55a8b-fca0-461a-8e4c-13927a9707e6               2020-02-10T13:58:44.6841810Z ["container1/blob1" -> "container2/blob2",...]

PS C:\> (Get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName -IncludeBlobRestoreStatus).BlobRestoreStatus 

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                     
------   ---------                            ------------- ------------------------     ---------------------                     
Complete 6ca55a8b-fca0-461a-8e4c-13927a9707e6               2020-02-10T13:58:44.6841810Z ["container1/blob1" -> "container2/blob2",...]
```

<span data-ttu-id="fde13-113">Esse comando primeiro cria 2 intervalos de BLOB e, em seguida, inicia a restauração de BLOBs em uma conta de armazenamento com os 2 intervalos de blob de 1 dia atrás.</span><span class="sxs-lookup"><span data-stu-id="fde13-113">This command first creates 2 blob ranges, then start restores blobs in a Storage account with the 2 blob ranges from 1 day ago.</span></span> <span data-ttu-id="fde13-114">O usuário pode usar Get-AzStorageAccount para rastrear o status da restauração mais tarde.</span><span class="sxs-lookup"><span data-stu-id="fde13-114">User can use Get-AzStorageAccount to trace the restore status later.</span></span>

### <span data-ttu-id="fde13-115">Exemplo 2: restaura todos os BLOBs em uma conta de armazenamento no back-end</span><span class="sxs-lookup"><span data-stu-id="fde13-115">Example 2: Restores all blobs in a Storage account in the backend</span></span>
```powershell
PS C:\> $job = Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddMinutes(-30) -WaitForComplete -asjob

PS C:\> $job | Wait-Job

PS C:\> $job.Output

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges
------   ---------                            ------------- ------------------------     ---------------------
Complete 0387953a-bbe6-4602-818d-e661581ee44b               2020-08-28T07:11:33.9843100Z ["" -> ""]
```

<span data-ttu-id="fde13-116">Esse comando restaura todos os BLOBs em uma conta de armazenamento de 30 minutos atrás e aguarde até que a restauração seja concluída.</span><span class="sxs-lookup"><span data-stu-id="fde13-116">This command restores all blobs in a Storage account from 30 minutes ago, and wait for the restore complete.</span></span> <span data-ttu-id="fde13-117">Como os blobs de restauração podem levar muito tempo, execute-o no back-end com o parâmetro AsJob e aguarde a conclusão do trabalho e mostre o resultado.</span><span class="sxs-lookup"><span data-stu-id="fde13-117">Since restore blobs might take a long time, run it in the backend with -Asjob parameter, and then wait for the job complete and show the result.</span></span>

### <span data-ttu-id="fde13-118">Exemplo 3: restaura os blobs por entrada de intervalos de blob diretamente e aguardar conclusão</span><span class="sxs-lookup"><span data-stu-id="fde13-118">Example 3: Restores blobs by input blob ranges directly, and wait for complete</span></span>
```powershell
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -WaitForComplete `
    -TimeToRestore (Get-Date).AddSeconds(-1) `
    -BlobRestoreRange @{StartRange="aaa/abc";EndRange="bbb/abc"},@{StartRange="bbb/acc";EndRange=""}
WARNING: Restore blob rang with Id 'd66d1d02-6e48-47ef-b516-0155dd8319c6' started. Restore blob ranges time to complete is dependent on the size of the restore.

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges   
------   ---------                            ------------- ------------------------     ---------------------   
Complete d66d1d02-6e48-47ef-b516-0155dd8319c6               2020-02-10T14:17:46.8189116Z ["aaa/abc" -> "bbb/abc",...]
```

<span data-ttu-id="fde13-119">Esse comando restaura os BLOBs em uma conta de armazenamento a partir de um dia atrás, por entrada 2 intervalos de blob diretamente para o cmdlet Restore-AzStorageBlobRange.</span><span class="sxs-lookup"><span data-stu-id="fde13-119">This command restores blobs in a Storage account from 1 day ago, by input 2 blob ranges directly to the Restore-AzStorageBlobRange cmdlet.</span></span> <span data-ttu-id="fde13-120">Esse comando irá aguardar a restauração ser concluída.</span><span class="sxs-lookup"><span data-stu-id="fde13-120">This command will wait for the restore complete.</span></span>

## <span data-ttu-id="fde13-121">OS</span><span class="sxs-lookup"><span data-stu-id="fde13-121">PARAMETERS</span></span>

### <span data-ttu-id="fde13-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fde13-122">-AsJob</span></span>
<span data-ttu-id="fde13-123">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fde13-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fde13-124">-BlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="fde13-124">-BlobRestoreRange</span></span>
<span data-ttu-id="fde13-125">O intervalo de BLOBs a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="fde13-125">The blob range to Restore.</span></span>
<span data-ttu-id="fde13-126">Se você não especificar esse parâmetro, restaurará todos os BLOBs.</span><span class="sxs-lookup"><span data-stu-id="fde13-126">If not specify this parameter, will restore all blobs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde13-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fde13-127">-DefaultProfile</span></span>
<span data-ttu-id="fde13-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fde13-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fde13-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fde13-129">-ResourceGroupName</span></span>
<span data-ttu-id="fde13-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fde13-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="fde13-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fde13-131">-ResourceId</span></span>
<span data-ttu-id="fde13-132">ID do recurso da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fde13-132">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fde13-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="fde13-133">-StorageAccount</span></span>
<span data-ttu-id="fde13-134">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="fde13-134">Storage account object</span></span>

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

### <span data-ttu-id="fde13-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fde13-135">-StorageAccountName</span></span>
<span data-ttu-id="fde13-136">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fde13-136">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde13-137">-TimeToRestore</span><span class="sxs-lookup"><span data-stu-id="fde13-137">-TimeToRestore</span></span>
<span data-ttu-id="fde13-138">O tempo para restaurar o blob.</span><span class="sxs-lookup"><span data-stu-id="fde13-138">The Time to Restore Blob.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde13-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="fde13-139">-WaitForComplete</span></span>
<span data-ttu-id="fde13-140">Aguarde a conclusão da tarefa de restauração</span><span class="sxs-lookup"><span data-stu-id="fde13-140">Wait for Restore task complete</span></span>

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

### <span data-ttu-id="fde13-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fde13-141">-Confirm</span></span>
<span data-ttu-id="fde13-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fde13-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fde13-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fde13-143">-WhatIf</span></span>
<span data-ttu-id="fde13-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fde13-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fde13-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fde13-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fde13-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fde13-146">CommonParameters</span></span>
<span data-ttu-id="fde13-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fde13-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fde13-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fde13-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fde13-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fde13-149">INPUTS</span></span>

### <span data-ttu-id="fde13-150">System. String</span><span class="sxs-lookup"><span data-stu-id="fde13-150">System.String</span></span>

### <span data-ttu-id="fde13-151">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fde13-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="fde13-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fde13-152">OUTPUTS</span></span>

### <span data-ttu-id="fde13-153">Microsoft. Azure. Commands. Management. Storage. Models. PSBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="fde13-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span></span>

## <span data-ttu-id="fde13-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fde13-154">NOTES</span></span>

## <span data-ttu-id="fde13-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fde13-155">RELATED LINKS</span></span>
