---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 5dab5eaca48152dc573caf75f5d80737802bfcdf
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399814"
---
# <span data-ttu-id="21707-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="21707-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="21707-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21707-102">SYNOPSIS</span></span>
<span data-ttu-id="21707-103">Obtém trabalhos de backup.</span><span class="sxs-lookup"><span data-stu-id="21707-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="21707-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21707-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21707-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="21707-105">DESCRIPTION</span></span>
<span data-ttu-id="21707-106">O cmdlet **Get-AzRecoveryServicesBackupService obtém** trabalhos de Backup do Azure para um cofre específico.</span><span class="sxs-lookup"><span data-stu-id="21707-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="21707-107">De definir o contexto do cofre usando o Set-AzRecoveryServicesVaultContext cmdlet antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="21707-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="21707-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="21707-108">EXAMPLES</span></span>

### <span data-ttu-id="21707-109">Exemplo 1: Obter todos os trabalhos em andamento</span><span class="sxs-lookup"><span data-stu-id="21707-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="21707-110">O primeiro comando obtém o status de um trabalho em andamento como uma matriz e o armazena na variável $Joblist dados.</span><span class="sxs-lookup"><span data-stu-id="21707-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="21707-111">O segundo comando exibe o primeiro item na matriz $Joblist dados.</span><span class="sxs-lookup"><span data-stu-id="21707-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="21707-112">Exemplo 2: Obter todos os trabalhos com falha nos últimos 7 dias</span><span class="sxs-lookup"><span data-stu-id="21707-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="21707-113">Esse comando recebe trabalhos com falha da semana passada no cofre.</span><span class="sxs-lookup"><span data-stu-id="21707-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="21707-114">O *parâmetro De* especifica uma hora sete dias no passado especificada em UTC.</span><span class="sxs-lookup"><span data-stu-id="21707-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="21707-115">O comando não especifica um valor para o *parâmetro* Para.</span><span class="sxs-lookup"><span data-stu-id="21707-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="21707-116">Portanto, ele usa o valor padrão da hora atual.</span><span class="sxs-lookup"><span data-stu-id="21707-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="21707-117">Exemplo 3: Obter um trabalho em andamento e aguardar a conclusão</span><span class="sxs-lookup"><span data-stu-id="21707-117">Example 3: Get an in-progress job and wait for completion</span></span>
```
PS C:\> 
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="21707-118">Este script vota no primeiro trabalho que está em andamento até que o trabalho seja concluído.</span><span class="sxs-lookup"><span data-stu-id="21707-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="21707-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21707-119">PARAMETERS</span></span>

### <span data-ttu-id="21707-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="21707-120">-BackupManagementType</span></span>
<span data-ttu-id="21707-121">Especifica o tipo de gerenciamento de backup.</span><span class="sxs-lookup"><span data-stu-id="21707-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="21707-122">Atualmente, apenas o AzureVM, o AzureStorage é suportado.</span><span class="sxs-lookup"><span data-stu-id="21707-122">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21707-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21707-123">-DefaultProfile</span></span>
<span data-ttu-id="21707-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="21707-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21707-125">-De</span><span class="sxs-lookup"><span data-stu-id="21707-125">-From</span></span>
<span data-ttu-id="21707-126">Especifica o início, como um objeto **DateTime,** de um intervalo de tempo para os trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="21707-126">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="21707-127">Para obter um **objeto DateTime,** use o cmdlet Get-Date dados.</span><span class="sxs-lookup"><span data-stu-id="21707-127">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="21707-128">Para obter mais informações sobre **objetos DateTime,** `Get-Help Get-Date` digite.</span><span class="sxs-lookup"><span data-stu-id="21707-128">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="21707-129">Use o formato UTC para datas.</span><span class="sxs-lookup"><span data-stu-id="21707-129">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="21707-130">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="21707-130">-Job</span></span>
<span data-ttu-id="21707-131">Especifica o nome do trabalho de Backup a ser feito.</span><span class="sxs-lookup"><span data-stu-id="21707-131">Specifies the name of the Backup job to get.</span></span>

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

### <span data-ttu-id="21707-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="21707-132">-JobId</span></span>
<span data-ttu-id="21707-133">Especifica a ID de um trabalho que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="21707-133">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="21707-134">A ID é a propriedade InstanceId de um objeto **AzureRmRecoveryServicesBackupService.**</span><span class="sxs-lookup"><span data-stu-id="21707-134">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="21707-135">Para obter um **objeto AzureRmRecoveryServicesBackupService,** use Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="21707-135">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="21707-136">-Operação</span><span class="sxs-lookup"><span data-stu-id="21707-136">-Operation</span></span>
<span data-ttu-id="21707-137">Especifica uma operação dos trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="21707-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="21707-138">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="21707-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="21707-139">Backup</span><span class="sxs-lookup"><span data-stu-id="21707-139">Backup</span></span>
- <span data-ttu-id="21707-140">ConfigurarBackup</span><span class="sxs-lookup"><span data-stu-id="21707-140">ConfigureBackup</span></span>
- <span data-ttu-id="21707-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="21707-141">DeleteBackupData</span></span>
- <span data-ttu-id="21707-142">Registrar</span><span class="sxs-lookup"><span data-stu-id="21707-142">Register</span></span>
- <span data-ttu-id="21707-143">Restaurar</span><span class="sxs-lookup"><span data-stu-id="21707-143">Restore</span></span>
- <span data-ttu-id="21707-144">Desproteger</span><span class="sxs-lookup"><span data-stu-id="21707-144">UnProtect</span></span>
- <span data-ttu-id="21707-145">Unregister</span><span class="sxs-lookup"><span data-stu-id="21707-145">Unregister</span></span>

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

### <span data-ttu-id="21707-146">-Status</span><span class="sxs-lookup"><span data-stu-id="21707-146">-Status</span></span>
<span data-ttu-id="21707-147">Especifica um status dos trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="21707-147">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="21707-148">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="21707-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="21707-149">Inprogress</span><span class="sxs-lookup"><span data-stu-id="21707-149">InProgress</span></span>
- <span data-ttu-id="21707-150">Falhou</span><span class="sxs-lookup"><span data-stu-id="21707-150">Failed</span></span>
- <span data-ttu-id="21707-151">Cancelado</span><span class="sxs-lookup"><span data-stu-id="21707-151">Cancelled</span></span>
- <span data-ttu-id="21707-152">Cancelar</span><span class="sxs-lookup"><span data-stu-id="21707-152">Cancelling</span></span>
- <span data-ttu-id="21707-153">Concluído</span><span class="sxs-lookup"><span data-stu-id="21707-153">Completed</span></span>
- <span data-ttu-id="21707-154">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="21707-154">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="21707-155">-Para</span><span class="sxs-lookup"><span data-stu-id="21707-155">-To</span></span>
<span data-ttu-id="21707-156">Especifica o fim, como um objeto **DateTime,** de um intervalo de tempo para os trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="21707-156">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="21707-157">O valor padrão é o tempo atual do sistema.</span><span class="sxs-lookup"><span data-stu-id="21707-157">The default value is the current system time.</span></span>
<span data-ttu-id="21707-158">Se você especificar esse parâmetro, também deverá especificar o *parâmetro De.*</span><span class="sxs-lookup"><span data-stu-id="21707-158">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="21707-159">Use o formato UTC para datas.</span><span class="sxs-lookup"><span data-stu-id="21707-159">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="21707-160">-VaultId</span><span class="sxs-lookup"><span data-stu-id="21707-160">-VaultId</span></span>
<span data-ttu-id="21707-161">ID arm do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="21707-161">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="21707-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21707-162">CommonParameters</span></span>
<span data-ttu-id="21707-163">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21707-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21707-164">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21707-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21707-165">Entradas</span><span class="sxs-lookup"><span data-stu-id="21707-165">INPUTS</span></span>

### <span data-ttu-id="21707-166">System.String</span><span class="sxs-lookup"><span data-stu-id="21707-166">System.String</span></span>

## <span data-ttu-id="21707-167">Saídas</span><span class="sxs-lookup"><span data-stu-id="21707-167">OUTPUTS</span></span>

### <span data-ttu-id="21707-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="21707-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="21707-169">Notas</span><span class="sxs-lookup"><span data-stu-id="21707-169">NOTES</span></span>

## <span data-ttu-id="21707-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21707-170">RELATED LINKS</span></span>


[<span data-ttu-id="21707-171">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="21707-171">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="21707-172">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="21707-172">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


