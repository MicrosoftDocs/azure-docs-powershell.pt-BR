---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: cc8b9017180c431caabc31970877d9fe0e4c346a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112697"
---
# <span data-ttu-id="8c0e8-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="8c0e8-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="8c0e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c0e8-102">SYNOPSIS</span></span>

<span data-ttu-id="8c0e8-103">Obtém trabalhos de backup.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="8c0e8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c0e8-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
  [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c0e8-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8c0e8-105">DESCRIPTION</span></span>

<span data-ttu-id="8c0e8-106">O cmdlet **Get-AzRecoveryServicesBackupJob obtém** trabalhos de Backup do Azure para um cofre específico.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="8c0e8-107">De definir o contexto do cofre usando o parâmetro -VaultId.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="8c0e8-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8c0e8-108">EXAMPLES</span></span>

### <span data-ttu-id="8c0e8-109">Exemplo 1: Obter todos os trabalhos em andamento</span><span class="sxs-lookup"><span data-stu-id="8c0e8-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="8c0e8-110">O primeiro comando obtém o status de um trabalho em andamento como uma matriz e, em seguida, o armazena na variável $Joblist dados.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="8c0e8-111">O segundo comando exibe o primeiro item na matriz $Joblist dados.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="8c0e8-112">Exemplo 2: Obter todos os trabalhos com falha nos últimos 7 dias</span><span class="sxs-lookup"><span data-stu-id="8c0e8-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="8c0e8-113">Esse comando recebe trabalhos com falha da última semana no cofre.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="8c0e8-114">O *parâmetro De* especifica uma hora sete dias no passado especificada em UTC.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="8c0e8-115">O comando não especifica um valor para o *parâmetro* Para.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="8c0e8-116">Portanto, ele usa o valor padrão da hora atual.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="8c0e8-117">Exemplo 3: Obter um trabalho em andamento e aguardar a conclusão</span><span class="sxs-lookup"><span data-stu-id="8c0e8-117">Example 3: Get an in-progress job and wait for completion</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
$Job = $Jobs[0]
While ( $Job.Status -ne Completed ) {
    Write-Host -Object "Waiting for completion..."
    Start-Sleep -Seconds 10
    $Job = Get-AzRecoveryServicesBackupJob -Job $Job -VaultId $vault.ID
}
Write-Host -Object "Done!"

Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

<span data-ttu-id="8c0e8-118">Este script vota no primeiro trabalho que está em andamento até que o trabalho seja concluído.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="8c0e8-119">Observação: você pode usar o cmdlet **Wait-AzRecoveryServicesBackup Job** para aguardar a finalização de um trabalho de Backup do Azure em vez de Enquanto.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

### <span data-ttu-id="8c0e8-120">Exemplo 4: Obter todos os trabalhos do AzureVM nos últimos 2 dias que foram concluídos com êxito</span><span class="sxs-lookup"><span data-stu-id="8c0e8-120">Example 4: Get all AzureVM jobs in last 2 days which finished successfully</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob  -VaultId $vault.ID  -Status Completed -From (Get-Date).AddDays(-2).ToUniversalTime() -BackupManagementType AzureVM
```
<span data-ttu-id="8c0e8-121">O primeiro cmdlet busca o objeto do cofre.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-121">First cmdlet fetches the vault object.</span></span> <span data-ttu-id="8c0e8-122">O segundo cmdlet armazena todos os trabalhos do AzureVM no cofre determinado que foi concluído nos últimos 2 dias para $jobs.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-122">Second cmdlet stores all the AzureVM jobs in the given vault which completed in last 2 days to $jobs.</span></span> <span data-ttu-id="8c0e8-123">Altere o valor do parâmetro BackupManagementType para MAB para buscar trabalhos de agente MAB.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-123">Change the value of BackupManagementType parameter to MAB in order to fetch MAB agent jobs.</span></span>

## <span data-ttu-id="8c0e8-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c0e8-124">PARAMETERS</span></span>

### <span data-ttu-id="8c0e8-125">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="8c0e8-125">-BackupManagementType</span></span>

<span data-ttu-id="8c0e8-126">A classe de recursos que está sendo protegida.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-126">The class of resources being protected.</span></span> <span data-ttu-id="8c0e8-127">Atualmente, os valores com suporte para este cmdlet são AzureVM, AzureStorage, AzureWorkload, MAB.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-127">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload, MAB.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload, MAB

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0e8-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c0e8-128">-DefaultProfile</span></span>

<span data-ttu-id="8c0e8-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c0e8-130">-De</span><span class="sxs-lookup"><span data-stu-id="8c0e8-130">-From</span></span>

<span data-ttu-id="8c0e8-131">Especifica o início, como um objeto **DateTime,** de um intervalo de tempo para os trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-131">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="8c0e8-132">Para obter um **objeto DateTime,** use o cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="8c0e8-132">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="8c0e8-133">Para obter mais informações sobre **objetos DateTime,** `Get-Help Get-Date` digite.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-133">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="8c0e8-134">Use o formato UTC para datas.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-134">Use UTC format for dates.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0e8-135">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="8c0e8-135">-Job</span></span>

<span data-ttu-id="8c0e8-136">Especifica o trabalho a ser feito.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-136">Specifies the job to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0e8-137">-JobId</span><span class="sxs-lookup"><span data-stu-id="8c0e8-137">-JobId</span></span>

<span data-ttu-id="8c0e8-138">Especifica a ID de um trabalho que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-138">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="8c0e8-139">A ID é a propriedade JobId de um objeto **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase.**</span><span class="sxs-lookup"><span data-stu-id="8c0e8-139">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0e8-140">-Operação</span><span class="sxs-lookup"><span data-stu-id="8c0e8-140">-Operation</span></span>

<span data-ttu-id="8c0e8-141">Especifica uma operação dos trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-141">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="8c0e8-142">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8c0e8-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8c0e8-143">Backup</span><span class="sxs-lookup"><span data-stu-id="8c0e8-143">Backup</span></span>
- <span data-ttu-id="8c0e8-144">ConfigurarBackup</span><span class="sxs-lookup"><span data-stu-id="8c0e8-144">ConfigureBackup</span></span>
- <span data-ttu-id="8c0e8-145">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="8c0e8-145">DeleteBackupData</span></span>
- <span data-ttu-id="8c0e8-146">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="8c0e8-146">DisableBackup</span></span>
- <span data-ttu-id="8c0e8-147">Restaurar</span><span class="sxs-lookup"><span data-stu-id="8c0e8-147">Restore</span></span>
- <span data-ttu-id="8c0e8-148">BackupDataMove</span><span class="sxs-lookup"><span data-stu-id="8c0e8-148">BackupDataMove</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobOperation]
Parameter Sets: (All)
Aliases:
Accepted values: Backup, Restore, ConfigureBackup, DisableBackup, DeleteBackupData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0e8-149">-Status</span><span class="sxs-lookup"><span data-stu-id="8c0e8-149">-Status</span></span>

<span data-ttu-id="8c0e8-150">Especifica um status dos trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-150">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="8c0e8-151">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8c0e8-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8c0e8-152">Inprogress</span><span class="sxs-lookup"><span data-stu-id="8c0e8-152">InProgress</span></span>
- <span data-ttu-id="8c0e8-153">Falhou</span><span class="sxs-lookup"><span data-stu-id="8c0e8-153">Failed</span></span>
- <span data-ttu-id="8c0e8-154">Cancelado</span><span class="sxs-lookup"><span data-stu-id="8c0e8-154">Cancelled</span></span>
- <span data-ttu-id="8c0e8-155">Cancelar</span><span class="sxs-lookup"><span data-stu-id="8c0e8-155">Cancelling</span></span>
- <span data-ttu-id="8c0e8-156">Concluído</span><span class="sxs-lookup"><span data-stu-id="8c0e8-156">Completed</span></span>
- <span data-ttu-id="8c0e8-157">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="8c0e8-157">CompletedWithWarnings</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobStatus]
Parameter Sets: (All)
Aliases:
Accepted values: InProgress, Cancelling, Cancelled, Completed, CompletedWithWarnings, Failed

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0e8-158">-Para</span><span class="sxs-lookup"><span data-stu-id="8c0e8-158">-To</span></span>

<span data-ttu-id="8c0e8-159">Especifica o fim, como um objeto **DateTime,** de um intervalo de tempo para os trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-159">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="8c0e8-160">O valor padrão é o tempo atual do sistema.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-160">The default value is the current system time.</span></span>
<span data-ttu-id="8c0e8-161">Se você especificar esse parâmetro, também deverá especificar o **parâmetro -From.**</span><span class="sxs-lookup"><span data-stu-id="8c0e8-161">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="8c0e8-162">Use o formato UTC para datas.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-162">Use UTC format for dates.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c0e8-163">-VaultId</span><span class="sxs-lookup"><span data-stu-id="8c0e8-163">-VaultId</span></span>

<span data-ttu-id="8c0e8-164">ID arm do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-164">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c0e8-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c0e8-165">CommonParameters</span></span>
<span data-ttu-id="8c0e8-166">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c0e8-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c0e8-167">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c0e8-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c0e8-168">Entradas</span><span class="sxs-lookup"><span data-stu-id="8c0e8-168">INPUTS</span></span>

### <span data-ttu-id="8c0e8-169">System.String</span><span class="sxs-lookup"><span data-stu-id="8c0e8-169">System.String</span></span>

## <span data-ttu-id="8c0e8-170">Saídas</span><span class="sxs-lookup"><span data-stu-id="8c0e8-170">OUTPUTS</span></span>

### <span data-ttu-id="8c0e8-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="8c0e8-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="8c0e8-172">Notas</span><span class="sxs-lookup"><span data-stu-id="8c0e8-172">NOTES</span></span>

## <span data-ttu-id="8c0e8-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c0e8-173">RELATED LINKS</span></span>

[<span data-ttu-id="8c0e8-174">Get-AzRecoveryServicesBackupServiceDetail</span><span class="sxs-lookup"><span data-stu-id="8c0e8-174">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="8c0e8-175">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="8c0e8-175">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="8c0e8-176">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="8c0e8-176">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
