---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 3fb6b89f5708c951731c45e0d32e0f7a379cf754
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440981"
---
# <span data-ttu-id="7e817-101">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="7e817-101">Get-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="7e817-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e817-102">SYNOPSIS</span></span>
<span data-ttu-id="7e817-103">Obtém trabalhos de backup.</span><span class="sxs-lookup"><span data-stu-id="7e817-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e817-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e817-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e817-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7e817-105">DESCRIPTION</span></span>
<span data-ttu-id="7e817-106">O cmdlet **Get-AzureRmRecoveryServicesBackupJob** Obtém trabalhos de backup do Azure para um cofre específico.</span><span class="sxs-lookup"><span data-stu-id="7e817-106">The **Get-AzureRmRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

<span data-ttu-id="7e817-107">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="7e817-107">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="7e817-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e817-108">EXAMPLES</span></span>

### <span data-ttu-id="7e817-109">Exemplo 1: obter todos os trabalhos em andamento</span><span class="sxs-lookup"><span data-stu-id="7e817-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzureRMRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="7e817-110">O primeiro comando obtém o status de um trabalho em andamento como uma matriz e, em seguida, armazena-o na variável $Joblist.</span><span class="sxs-lookup"><span data-stu-id="7e817-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>

<span data-ttu-id="7e817-111">O segundo comando exibe o primeiro item na matriz de $Joblist.</span><span class="sxs-lookup"><span data-stu-id="7e817-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="7e817-112">Exemplo 2: obter todos os trabalhos com falha nos últimos 7 dias</span><span class="sxs-lookup"><span data-stu-id="7e817-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="7e817-113">Esse comando obtém trabalhos com falha da semana passada no cofre.</span><span class="sxs-lookup"><span data-stu-id="7e817-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="7e817-114">O parâmetro *from* especifica um período de sete dias no passado especificado em UTC.</span><span class="sxs-lookup"><span data-stu-id="7e817-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="7e817-115">O comando não especifica um valor para o parâmetro *to* .</span><span class="sxs-lookup"><span data-stu-id="7e817-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="7e817-116">Portanto, ele usa o valor padrão do tempo atual.</span><span class="sxs-lookup"><span data-stu-id="7e817-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="7e817-117">Exemplo 3: obter um trabalho em andamento e esperar a conclusão</span><span class="sxs-lookup"><span data-stu-id="7e817-117">Example 3: Get an in-progress job and wait for completion</span></span>
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

<span data-ttu-id="7e817-118">Este script sonda o primeiro trabalho que está em andamento até que o trabalho seja concluído.</span><span class="sxs-lookup"><span data-stu-id="7e817-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="7e817-119">OS</span><span class="sxs-lookup"><span data-stu-id="7e817-119">PARAMETERS</span></span>

### <span data-ttu-id="7e817-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="7e817-120">-BackupManagementType</span></span>
<span data-ttu-id="7e817-121">Especifica o tipo de gerenciamento de backup.</span><span class="sxs-lookup"><span data-stu-id="7e817-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="7e817-122">No momento, somente há suporte para AzureVM.</span><span class="sxs-lookup"><span data-stu-id="7e817-122">Currently, only AzureVM is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e817-123">-De</span><span class="sxs-lookup"><span data-stu-id="7e817-123">-From</span></span>
<span data-ttu-id="7e817-124">Especifica o início, como um objeto **DateTime** , de um intervalo de tempo para os trabalhos que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="7e817-124">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="7e817-125">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="7e817-125">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="7e817-126">Para obter mais informações sobre objetos **DateTime** , digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="7e817-126">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="7e817-127">Use o formato UTC para datas.</span><span class="sxs-lookup"><span data-stu-id="7e817-127">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="7e817-128">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="7e817-128">-Job</span></span>
<span data-ttu-id="7e817-129">Especifica o nome do trabalho de backup a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="7e817-129">Specifies the name of the Backup job to get.</span></span>

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

### <span data-ttu-id="7e817-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="7e817-130">-JobId</span></span>
<span data-ttu-id="7e817-131">Especifica a ID de um trabalho que o cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="7e817-131">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="7e817-132">A ID é a propriedade InstanceId de um objeto **AzureRmRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="7e817-132">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="7e817-133">Para obter um objeto **AzureRmRecoveryServicesBackupJob** , use Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="7e817-133">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="7e817-134">-Operação</span><span class="sxs-lookup"><span data-stu-id="7e817-134">-Operation</span></span>
<span data-ttu-id="7e817-135">Especifica uma operação dos trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="7e817-135">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="7e817-136">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7e817-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7e817-137">Fazer</span><span class="sxs-lookup"><span data-stu-id="7e817-137">Backup</span></span>
- <span data-ttu-id="7e817-138">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="7e817-138">ConfigureBackup</span></span>
- <span data-ttu-id="7e817-139">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="7e817-139">DeleteBackupData</span></span>
- <span data-ttu-id="7e817-140">Inscrição</span><span class="sxs-lookup"><span data-stu-id="7e817-140">Register</span></span>
- <span data-ttu-id="7e817-141">Restaurar</span><span class="sxs-lookup"><span data-stu-id="7e817-141">Restore</span></span>
- <span data-ttu-id="7e817-142">Desproteger</span><span class="sxs-lookup"><span data-stu-id="7e817-142">UnProtect</span></span>
- <span data-ttu-id="7e817-143">Cancele</span><span class="sxs-lookup"><span data-stu-id="7e817-143">Unregister</span></span>

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

### <span data-ttu-id="7e817-144">-Status</span><span class="sxs-lookup"><span data-stu-id="7e817-144">-Status</span></span>
<span data-ttu-id="7e817-145">Especifica um status dos trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="7e817-145">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="7e817-146">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7e817-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7e817-147">InProgress</span><span class="sxs-lookup"><span data-stu-id="7e817-147">InProgress</span></span>
- <span data-ttu-id="7e817-148">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="7e817-148">Failed</span></span>
- <span data-ttu-id="7e817-149">Cela</span><span class="sxs-lookup"><span data-stu-id="7e817-149">Cancelled</span></span>
- <span data-ttu-id="7e817-150">Cancelamento</span><span class="sxs-lookup"><span data-stu-id="7e817-150">Cancelling</span></span>
- <span data-ttu-id="7e817-151">Feito</span><span class="sxs-lookup"><span data-stu-id="7e817-151">Completed</span></span>
- <span data-ttu-id="7e817-152">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="7e817-152">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="7e817-153">-To</span><span class="sxs-lookup"><span data-stu-id="7e817-153">-To</span></span>
<span data-ttu-id="7e817-154">Especifica o fim, como um objeto **DateTime** , de um intervalo de tempo para os trabalhos que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="7e817-154">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="7e817-155">O valor padrão é a hora atual do sistema.</span><span class="sxs-lookup"><span data-stu-id="7e817-155">The default value is the current system time.</span></span>
<span data-ttu-id="7e817-156">Se você especificar esse parâmetro, também deverá especificar o parâmetro *from* .</span><span class="sxs-lookup"><span data-stu-id="7e817-156">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="7e817-157">Use o formato UTC para datas.</span><span class="sxs-lookup"><span data-stu-id="7e817-157">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="7e817-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e817-158">-DefaultProfile</span></span>
<span data-ttu-id="7e817-159">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7e817-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e817-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e817-160">CommonParameters</span></span>
<span data-ttu-id="7e817-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e817-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e817-162">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e817-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e817-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7e817-163">INPUTS</span></span>

## <span data-ttu-id="7e817-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7e817-164">OUTPUTS</span></span>

### <span data-ttu-id="7e817-165">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="7e817-165">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

### <span data-ttu-id="7e817-166">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase]</span><span class="sxs-lookup"><span data-stu-id="7e817-166">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="7e817-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7e817-167">NOTES</span></span>

## <span data-ttu-id="7e817-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e817-168">RELATED LINKS</span></span>

[<span data-ttu-id="7e817-169">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="7e817-169">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>](./Get-AzureRmRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="7e817-170">Parar-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="7e817-170">Stop-AzureRmRecoveryServicesBackupJob</span></span>](./Stop-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="7e817-171">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="7e817-171">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


