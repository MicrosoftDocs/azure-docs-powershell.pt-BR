---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/restore-azstorageblobrange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
ms.openlocfilehash: 0d742c257927c06686dc9ce799cdc3e4a5b92340
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901556"
---
# <span data-ttu-id="c6eb5-101">Restore-AzStorageBlobRange</span><span class="sxs-lookup"><span data-stu-id="c6eb5-101">Restore-AzStorageBlobRange</span></span>

## <span data-ttu-id="c6eb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6eb5-102">SYNOPSIS</span></span>
<span data-ttu-id="c6eb5-103">Restaura uma conta de armazenamento para intervalos de blob específicos.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-103">Restores a Storage account for specific blob ranges.</span></span>

## <span data-ttu-id="c6eb5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c6eb5-104">SYNTAX</span></span>

### <span data-ttu-id="c6eb5-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c6eb5-105">AccountName (Default)</span></span>
```
Restore-AzStorageBlobRange [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -TimeToRestore <DateTime> [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6eb5-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="c6eb5-106">AccountResourceId</span></span>
```
Restore-AzStorageBlobRange [-ResourceId] <String> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6eb5-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="c6eb5-107">AccountObject</span></span>
```
Restore-AzStorageBlobRange -StorageAccount <PSStorageAccount> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6eb5-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c6eb5-108">DESCRIPTION</span></span>
<span data-ttu-id="c6eb5-109">O cmdlet **Restore-AzStorageBlobRange** restaura blobs em uma conta de Armazenamento para intervalos de blob específicos.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-109">The **Restore-AzStorageBlobRange** cmdlet restores blobs in a Storage account for specific blob ranges.</span></span>
<span data-ttu-id="c6eb5-110">O intervalo inicial está incluído e o intervalo final é excluído na restauração de blob.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-110">The start range is included, and the end range is excluded in blob restore.</span></span>

## <span data-ttu-id="c6eb5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6eb5-111">EXAMPLES</span></span>

### <span data-ttu-id="c6eb5-112">Exemplo 1: Iniciar restaura blobs em uma conta de armazenamento com intervalos de blob específicos</span><span class="sxs-lookup"><span data-stu-id="c6eb5-112">Example 1: Start restores blobs in a Storage account with specific blob ranges</span></span>
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

<span data-ttu-id="c6eb5-113">Este comando primeiro cria 2 intervalos de blob e, em seguida, inicia restaura blobs em uma conta de Armazenamento com os intervalos de 2 blob de 1 dia atrás.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-113">This command first creates 2 blob ranges, then start restores blobs in a Storage account with the 2 blob ranges from 1 day ago.</span></span> <span data-ttu-id="c6eb5-114">O usuário pode usar Get-AzStorageAccount para rastrear o status de restauração mais tarde.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-114">User can use Get-AzStorageAccount to trace the restore status later.</span></span>

### <span data-ttu-id="c6eb5-115">Exemplo 2: restaura todos os blobs em uma conta de armazenamento no back-end</span><span class="sxs-lookup"><span data-stu-id="c6eb5-115">Example 2: Restores all blobs in a Storage account in the backend</span></span>
```powershell
PS C:\> $job = Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddMinutes(-30) -WaitForComplete -asjob

PS C:\> $job | Wait-Job

PS C:\> $job.Output

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges
------   ---------                            ------------- ------------------------     ---------------------
Complete 0387953a-bbe6-4602-818d-e661581ee44b               2020-08-28T07:11:33.9843100Z ["" -> ""]
```

<span data-ttu-id="c6eb5-116">Este comando restaura todos os blobs em uma conta de Armazenamento de 30 minutos atrás e aguarda a restauração ser concluída.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-116">This command restores all blobs in a Storage account from 30 minutes ago, and wait for the restore complete.</span></span> <span data-ttu-id="c6eb5-117">Como a restauração de blobs pode levar muito tempo, execute-a no back-end com o parâmetro -Asjob e aguarde a conclusão do trabalho e mostre o resultado.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-117">Since restore blobs might take a long time, run it in the backend with -Asjob parameter, and then wait for the job complete and show the result.</span></span>

### <span data-ttu-id="c6eb5-118">Exemplo 3: restaura blobs por intervalos de blob de entrada diretamente e aguarda a conclusão</span><span class="sxs-lookup"><span data-stu-id="c6eb5-118">Example 3: Restores blobs by input blob ranges directly, and wait for complete</span></span>
```powershell
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -WaitForComplete `
    -TimeToRestore (Get-Date).AddSeconds(-1) `
    -BlobRestoreRange @{StartRange="aaa/abc";EndRange="bbb/abc"},@{StartRange="bbb/acc";EndRange=""}
WARNING: Restore blob rang with Id 'd66d1d02-6e48-47ef-b516-0155dd8319c6' started. Restore blob ranges time to complete is dependent on the size of the restore.

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges   
------   ---------                            ------------- ------------------------     ---------------------   
Complete d66d1d02-6e48-47ef-b516-0155dd8319c6               2020-02-10T14:17:46.8189116Z ["aaa/abc" -> "bbb/abc",...]
```

<span data-ttu-id="c6eb5-119">Este comando restaura blobs em uma conta de Armazenamento de 1 dia atrás, por meio de intervalos de blob de entrada 2 diretamente para o cmdlet Restore-AzStorageBlobRange de dados.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-119">This command restores blobs in a Storage account from 1 day ago, by input 2 blob ranges directly to the Restore-AzStorageBlobRange cmdlet.</span></span> <span data-ttu-id="c6eb5-120">Este comando aguardará a restauração concluída.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-120">This command will wait for the restore complete.</span></span>

## <span data-ttu-id="c6eb5-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c6eb5-121">PARAMETERS</span></span>

### <span data-ttu-id="c6eb5-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6eb5-122">-AsJob</span></span>
<span data-ttu-id="c6eb5-123">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c6eb5-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c6eb5-124">-BlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="c6eb5-124">-BlobRestoreRange</span></span>
<span data-ttu-id="c6eb5-125">O intervalo de blob para Restaurar.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-125">The blob range to Restore.</span></span>
<span data-ttu-id="c6eb5-126">Se não especificar esse parâmetro, restaurará todos os blobs.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-126">If not specify this parameter, will restore all blobs.</span></span>

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

### <span data-ttu-id="c6eb5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6eb5-127">-DefaultProfile</span></span>
<span data-ttu-id="c6eb5-128">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6eb5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6eb5-129">-ResourceGroupName</span></span>
<span data-ttu-id="c6eb5-130">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="c6eb5-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6eb5-131">-ResourceId</span></span>
<span data-ttu-id="c6eb5-132">ID do Recurso de Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-132">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="c6eb5-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c6eb5-133">-StorageAccount</span></span>
<span data-ttu-id="c6eb5-134">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="c6eb5-134">Storage account object</span></span>

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

### <span data-ttu-id="c6eb5-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c6eb5-135">-StorageAccountName</span></span>
<span data-ttu-id="c6eb5-136">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="c6eb5-137">-TimeToRestore</span><span class="sxs-lookup"><span data-stu-id="c6eb5-137">-TimeToRestore</span></span>
<span data-ttu-id="c6eb5-138">O Tempo para Restaurar Blob.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-138">The Time to Restore Blob.</span></span>

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

### <span data-ttu-id="c6eb5-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="c6eb5-139">-WaitForComplete</span></span>
<span data-ttu-id="c6eb5-140">Aguarde a conclusão da tarefa Restaurar</span><span class="sxs-lookup"><span data-stu-id="c6eb5-140">Wait for Restore task complete</span></span>

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

### <span data-ttu-id="c6eb5-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6eb5-141">-Confirm</span></span>
<span data-ttu-id="c6eb5-142">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6eb5-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6eb5-143">-WhatIf</span></span>
<span data-ttu-id="c6eb5-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6eb5-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6eb5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6eb5-146">CommonParameters</span></span>
<span data-ttu-id="c6eb5-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6eb5-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6eb5-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6eb5-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c6eb5-149">INPUTS</span></span>

### <span data-ttu-id="c6eb5-150">System.String</span><span class="sxs-lookup"><span data-stu-id="c6eb5-150">System.String</span></span>

### <span data-ttu-id="c6eb5-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c6eb5-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="c6eb5-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c6eb5-152">OUTPUTS</span></span>

### <span data-ttu-id="c6eb5-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="c6eb5-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span></span>

## <span data-ttu-id="c6eb5-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="c6eb5-154">NOTES</span></span>

## <span data-ttu-id="c6eb5-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6eb5-155">RELATED LINKS</span></span>
