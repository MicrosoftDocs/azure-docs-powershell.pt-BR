---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 21498e13490b22b58621e2100dcc885442db7607
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599706"
---
# <span data-ttu-id="9ed9b-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="9ed9b-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="9ed9b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ed9b-102">SYNOPSIS</span></span>
<span data-ttu-id="9ed9b-103">Obtém trabalhos de backup.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="9ed9b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ed9b-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ed9b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9ed9b-105">DESCRIPTION</span></span>
<span data-ttu-id="9ed9b-106">O cmdlet **Get-AzRecoveryServicesBackupJob** Obtém trabalhos de backup do Azure para um cofre específico.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="9ed9b-107">Defina o contexto do cofre usando o cmdlet Set-AzRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="9ed9b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9ed9b-108">EXAMPLES</span></span>

### <span data-ttu-id="9ed9b-109">Exemplo 1: obter todos os trabalhos em andamento</span><span class="sxs-lookup"><span data-stu-id="9ed9b-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="9ed9b-110">O primeiro comando obtém o status de um trabalho em andamento como uma matriz e, em seguida, armazena-o na variável $Joblist.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="9ed9b-111">O segundo comando exibe o primeiro item na matriz de $Joblist.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="9ed9b-112">Exemplo 2: obter todos os trabalhos com falha nos últimos 7 dias</span><span class="sxs-lookup"><span data-stu-id="9ed9b-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="9ed9b-113">Esse comando obtém trabalhos com falha da semana passada no cofre.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="9ed9b-114">O parâmetro *from* especifica um período de sete dias no passado especificado em UTC.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="9ed9b-115">O comando não especifica um valor para o parâmetro *to* .</span><span class="sxs-lookup"><span data-stu-id="9ed9b-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="9ed9b-116">Portanto, ele usa o valor padrão do tempo atual.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="9ed9b-117">Exemplo 3: obter um trabalho em andamento e esperar a conclusão</span><span class="sxs-lookup"><span data-stu-id="9ed9b-117">Example 3: Get an in-progress job and wait for completion</span></span>
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

<span data-ttu-id="9ed9b-118">Este script sonda o primeiro trabalho que está em andamento até que o trabalho seja concluído.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="9ed9b-119">OS</span><span class="sxs-lookup"><span data-stu-id="9ed9b-119">PARAMETERS</span></span>

### <span data-ttu-id="9ed9b-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="9ed9b-120">-BackupManagementType</span></span>
<span data-ttu-id="9ed9b-121">Especifica o tipo de gerenciamento de backup.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="9ed9b-122">No momento, só há suporte para AzureVM, AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-122">Currently, only AzureVM, AzureStorage is supported.</span></span>

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

### <span data-ttu-id="9ed9b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ed9b-123">-DefaultProfile</span></span>
<span data-ttu-id="9ed9b-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ed9b-125">-De</span><span class="sxs-lookup"><span data-stu-id="9ed9b-125">-From</span></span>
<span data-ttu-id="9ed9b-126">Especifica o início, como um objeto **DateTime** , de um intervalo de tempo para os trabalhos que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-126">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9ed9b-127">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-127">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="9ed9b-128">Para obter mais informações sobre objetos **DateTime** , digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="9ed9b-128">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="9ed9b-129">Use o formato UTC para datas.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-129">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="9ed9b-130">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="9ed9b-130">-Job</span></span>
<span data-ttu-id="9ed9b-131">Especifica o nome do trabalho de backup a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-131">Specifies the name of the Backup job to get.</span></span>

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

### <span data-ttu-id="9ed9b-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="9ed9b-132">-JobId</span></span>
<span data-ttu-id="9ed9b-133">Especifica a ID de um trabalho que o cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-133">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="9ed9b-134">A ID é a propriedade InstanceId de um objeto **AzureRmRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="9ed9b-134">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="9ed9b-135">Para obter um objeto **AzureRmRecoveryServicesBackupJob** , use Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-135">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="9ed9b-136">-Operação</span><span class="sxs-lookup"><span data-stu-id="9ed9b-136">-Operation</span></span>
<span data-ttu-id="9ed9b-137">Especifica uma operação dos trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9ed9b-138">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9ed9b-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9ed9b-139">Fazer</span><span class="sxs-lookup"><span data-stu-id="9ed9b-139">Backup</span></span>
- <span data-ttu-id="9ed9b-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="9ed9b-140">ConfigureBackup</span></span>
- <span data-ttu-id="9ed9b-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="9ed9b-141">DeleteBackupData</span></span>
- <span data-ttu-id="9ed9b-142">Inscrição</span><span class="sxs-lookup"><span data-stu-id="9ed9b-142">Register</span></span>
- <span data-ttu-id="9ed9b-143">Restaurar</span><span class="sxs-lookup"><span data-stu-id="9ed9b-143">Restore</span></span>
- <span data-ttu-id="9ed9b-144">Desproteger</span><span class="sxs-lookup"><span data-stu-id="9ed9b-144">UnProtect</span></span>
- <span data-ttu-id="9ed9b-145">Cancele</span><span class="sxs-lookup"><span data-stu-id="9ed9b-145">Unregister</span></span>

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

### <span data-ttu-id="9ed9b-146">-Status</span><span class="sxs-lookup"><span data-stu-id="9ed9b-146">-Status</span></span>
<span data-ttu-id="9ed9b-147">Especifica um status dos trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-147">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9ed9b-148">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9ed9b-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9ed9b-149">InProgress</span><span class="sxs-lookup"><span data-stu-id="9ed9b-149">InProgress</span></span>
- <span data-ttu-id="9ed9b-150">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="9ed9b-150">Failed</span></span>
- <span data-ttu-id="9ed9b-151">Cela</span><span class="sxs-lookup"><span data-stu-id="9ed9b-151">Cancelled</span></span>
- <span data-ttu-id="9ed9b-152">Cancelamento</span><span class="sxs-lookup"><span data-stu-id="9ed9b-152">Cancelling</span></span>
- <span data-ttu-id="9ed9b-153">Feito</span><span class="sxs-lookup"><span data-stu-id="9ed9b-153">Completed</span></span>
- <span data-ttu-id="9ed9b-154">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="9ed9b-154">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="9ed9b-155">-To</span><span class="sxs-lookup"><span data-stu-id="9ed9b-155">-To</span></span>
<span data-ttu-id="9ed9b-156">Especifica o fim, como um objeto **DateTime** , de um intervalo de tempo para os trabalhos que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-156">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9ed9b-157">O valor padrão é a hora atual do sistema.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-157">The default value is the current system time.</span></span>
<span data-ttu-id="9ed9b-158">Se você especificar esse parâmetro, também deverá especificar o parâmetro *from* .</span><span class="sxs-lookup"><span data-stu-id="9ed9b-158">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="9ed9b-159">Use o formato UTC para datas.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-159">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="9ed9b-160">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="9ed9b-160">-VaultId</span></span>
<span data-ttu-id="9ed9b-161">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-161">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="9ed9b-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ed9b-162">CommonParameters</span></span>
<span data-ttu-id="9ed9b-163">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ed9b-164">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ed9b-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ed9b-165">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9ed9b-165">INPUTS</span></span>

### <span data-ttu-id="9ed9b-166">System. String</span><span class="sxs-lookup"><span data-stu-id="9ed9b-166">System.String</span></span>

## <span data-ttu-id="9ed9b-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9ed9b-167">OUTPUTS</span></span>

### <span data-ttu-id="9ed9b-168">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="9ed9b-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="9ed9b-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9ed9b-169">NOTES</span></span>

## <span data-ttu-id="9ed9b-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ed9b-170">RELATED LINKS</span></span>

[<span data-ttu-id="9ed9b-171">Get-AzRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="9ed9b-171">Get-AzRecoveryServicesBackupJobDetails</span></span>](./Get-AzRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="9ed9b-172">Parar-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="9ed9b-172">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="9ed9b-173">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="9ed9b-173">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


