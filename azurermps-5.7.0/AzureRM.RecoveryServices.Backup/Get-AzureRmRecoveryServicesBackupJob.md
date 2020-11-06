---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 5e6555095563fd5c0589835b28ad293f395fffaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427502"
---
# <span data-ttu-id="9c55a-101">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="9c55a-101">Get-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="9c55a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c55a-102">SYNOPSIS</span></span>
<span data-ttu-id="9c55a-103">Obtém trabalhos de backup.</span><span class="sxs-lookup"><span data-stu-id="9c55a-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c55a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c55a-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c55a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c55a-105">DESCRIPTION</span></span>
<span data-ttu-id="9c55a-106">O cmdlet **Get-AzureRmRecoveryServicesBackupJob** Obtém trabalhos de backup do Azure para um cofre específico.</span><span class="sxs-lookup"><span data-stu-id="9c55a-106">The **Get-AzureRmRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

<span data-ttu-id="9c55a-107">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="9c55a-107">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="9c55a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c55a-108">EXAMPLES</span></span>

### <span data-ttu-id="9c55a-109">Exemplo 1: obter todos os trabalhos em andamento</span><span class="sxs-lookup"><span data-stu-id="9c55a-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzureRMRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="9c55a-110">O primeiro comando obtém o status de um trabalho em andamento como uma matriz e, em seguida, armazena-o na variável $Joblist.</span><span class="sxs-lookup"><span data-stu-id="9c55a-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>

<span data-ttu-id="9c55a-111">O segundo comando exibe o primeiro item na matriz de $Joblist.</span><span class="sxs-lookup"><span data-stu-id="9c55a-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="9c55a-112">Exemplo 2: obter todos os trabalhos com falha nos últimos 7 dias</span><span class="sxs-lookup"><span data-stu-id="9c55a-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="9c55a-113">Esse comando obtém trabalhos com falha da semana passada no cofre.</span><span class="sxs-lookup"><span data-stu-id="9c55a-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="9c55a-114">O parâmetro *from* especifica um período de sete dias no passado especificado em UTC.</span><span class="sxs-lookup"><span data-stu-id="9c55a-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="9c55a-115">O comando não especifica um valor para o parâmetro *to* .</span><span class="sxs-lookup"><span data-stu-id="9c55a-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="9c55a-116">Portanto, ele usa o valor padrão do tempo atual.</span><span class="sxs-lookup"><span data-stu-id="9c55a-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="9c55a-117">Exemplo 3: obter um trabalho em andamento e esperar a conclusão</span><span class="sxs-lookup"><span data-stu-id="9c55a-117">Example 3: Get an in-progress job and wait for completion</span></span>
```
PS C:\> 
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="9c55a-118">Este script sonda o primeiro trabalho que está em andamento até que o trabalho seja concluído.</span><span class="sxs-lookup"><span data-stu-id="9c55a-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="9c55a-119">OS</span><span class="sxs-lookup"><span data-stu-id="9c55a-119">PARAMETERS</span></span>

### <span data-ttu-id="9c55a-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="9c55a-120">-BackupManagementType</span></span>
<span data-ttu-id="9c55a-121">Especifica o tipo de gerenciamento de backup.</span><span class="sxs-lookup"><span data-stu-id="9c55a-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="9c55a-122">No momento, somente há suporte para AzureVM.</span><span class="sxs-lookup"><span data-stu-id="9c55a-122">Currently, only AzureVM is supported.</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c55a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c55a-123">-DefaultProfile</span></span>
<span data-ttu-id="9c55a-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c55a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c55a-125">-De</span><span class="sxs-lookup"><span data-stu-id="9c55a-125">-From</span></span>
<span data-ttu-id="9c55a-126">Especifica o início, como um objeto **DateTime** , de um intervalo de tempo para os trabalhos que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="9c55a-126">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9c55a-127">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="9c55a-127">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="9c55a-128">Para obter mais informações sobre objetos **DateTime** , digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="9c55a-128">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="9c55a-129">Use o formato UTC para datas.</span><span class="sxs-lookup"><span data-stu-id="9c55a-129">Use UTC format for dates.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c55a-130">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="9c55a-130">-Job</span></span>
<span data-ttu-id="9c55a-131">Especifica o nome do trabalho de backup a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="9c55a-131">Specifies the name of the Backup job to get.</span></span>

```yaml
Type: JobBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c55a-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="9c55a-132">-JobId</span></span>
<span data-ttu-id="9c55a-133">Especifica a ID de um trabalho que o cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="9c55a-133">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="9c55a-134">A ID é a propriedade InstanceId de um objeto **AzureRmRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="9c55a-134">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="9c55a-135">Para obter um objeto **AzureRmRecoveryServicesBackupJob** , use Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="9c55a-135">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c55a-136">-Operação</span><span class="sxs-lookup"><span data-stu-id="9c55a-136">-Operation</span></span>
<span data-ttu-id="9c55a-137">Especifica uma operação dos trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="9c55a-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9c55a-138">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9c55a-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9c55a-139">Fazer</span><span class="sxs-lookup"><span data-stu-id="9c55a-139">Backup</span></span>
- <span data-ttu-id="9c55a-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="9c55a-140">ConfigureBackup</span></span>
- <span data-ttu-id="9c55a-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="9c55a-141">DeleteBackupData</span></span>
- <span data-ttu-id="9c55a-142">Inscrição</span><span class="sxs-lookup"><span data-stu-id="9c55a-142">Register</span></span>
- <span data-ttu-id="9c55a-143">Restaurar</span><span class="sxs-lookup"><span data-stu-id="9c55a-143">Restore</span></span>
- <span data-ttu-id="9c55a-144">Desproteger</span><span class="sxs-lookup"><span data-stu-id="9c55a-144">UnProtect</span></span>
- <span data-ttu-id="9c55a-145">Cancele</span><span class="sxs-lookup"><span data-stu-id="9c55a-145">Unregister</span></span>

```yaml
Type: JobOperation
Parameter Sets: (All)
Aliases: 
Accepted values: Backup, Restore, ConfigureBackup, DisableBackup, DeleteBackupData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c55a-146">-Status</span><span class="sxs-lookup"><span data-stu-id="9c55a-146">-Status</span></span>
<span data-ttu-id="9c55a-147">Especifica um status dos trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="9c55a-147">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9c55a-148">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9c55a-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9c55a-149">InProgress</span><span class="sxs-lookup"><span data-stu-id="9c55a-149">InProgress</span></span>
- <span data-ttu-id="9c55a-150">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="9c55a-150">Failed</span></span>
- <span data-ttu-id="9c55a-151">Cela</span><span class="sxs-lookup"><span data-stu-id="9c55a-151">Cancelled</span></span>
- <span data-ttu-id="9c55a-152">Cancelamento</span><span class="sxs-lookup"><span data-stu-id="9c55a-152">Cancelling</span></span>
- <span data-ttu-id="9c55a-153">Feito</span><span class="sxs-lookup"><span data-stu-id="9c55a-153">Completed</span></span>
- <span data-ttu-id="9c55a-154">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="9c55a-154">CompletedWithWarnings</span></span>

```yaml
Type: JobStatus
Parameter Sets: (All)
Aliases: 
Accepted values: InProgress, Cancelling, Cancelled, Completed, CompletedWithWarnings, Failed

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c55a-155">-To</span><span class="sxs-lookup"><span data-stu-id="9c55a-155">-To</span></span>
<span data-ttu-id="9c55a-156">Especifica o fim, como um objeto **DateTime** , de um intervalo de tempo para os trabalhos que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="9c55a-156">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9c55a-157">O valor padrão é a hora atual do sistema.</span><span class="sxs-lookup"><span data-stu-id="9c55a-157">The default value is the current system time.</span></span>
<span data-ttu-id="9c55a-158">Se você especificar esse parâmetro, também deverá especificar o parâmetro *from* .</span><span class="sxs-lookup"><span data-stu-id="9c55a-158">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="9c55a-159">Use o formato UTC para datas.</span><span class="sxs-lookup"><span data-stu-id="9c55a-159">Use UTC format for dates.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c55a-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c55a-160">CommonParameters</span></span>
<span data-ttu-id="9c55a-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c55a-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c55a-162">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c55a-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c55a-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c55a-163">INPUTS</span></span>

### <span data-ttu-id="9c55a-164">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9c55a-164">None</span></span>
<span data-ttu-id="9c55a-165">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="9c55a-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9c55a-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c55a-166">OUTPUTS</span></span>

### <span data-ttu-id="9c55a-167">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="9c55a-167">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

### <span data-ttu-id="9c55a-168">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase]</span><span class="sxs-lookup"><span data-stu-id="9c55a-168">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="9c55a-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c55a-169">NOTES</span></span>

## <span data-ttu-id="9c55a-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c55a-170">RELATED LINKS</span></span>

[<span data-ttu-id="9c55a-171">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="9c55a-171">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>](./Get-AzureRmRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="9c55a-172">Parar-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="9c55a-172">Stop-AzureRmRecoveryServicesBackupJob</span></span>](./Stop-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="9c55a-173">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="9c55a-173">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


