---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 0ed0ed82c1f2c030ab10fc6a96d1582fdb34b7d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433192"
---
# <span data-ttu-id="abf6a-101">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="abf6a-101">Get-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="abf6a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="abf6a-102">SYNOPSIS</span></span>
<span data-ttu-id="abf6a-103">Obtém trabalhos de backup.</span><span class="sxs-lookup"><span data-stu-id="abf6a-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abf6a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="abf6a-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abf6a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="abf6a-105">DESCRIPTION</span></span>
<span data-ttu-id="abf6a-106">O cmdlet **Get-AzureRmRecoveryServicesBackupJob** Obtém trabalhos de backup do Azure para um cofre específico.</span><span class="sxs-lookup"><span data-stu-id="abf6a-106">The **Get-AzureRmRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="abf6a-107">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="abf6a-107">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="abf6a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="abf6a-108">EXAMPLES</span></span>

### <span data-ttu-id="abf6a-109">Exemplo 1: obter todos os trabalhos em andamento</span><span class="sxs-lookup"><span data-stu-id="abf6a-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzureRMRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="abf6a-110">O primeiro comando obtém o status de um trabalho em andamento como uma matriz e, em seguida, armazena-o na variável $Joblist.</span><span class="sxs-lookup"><span data-stu-id="abf6a-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="abf6a-111">O segundo comando exibe o primeiro item na matriz de $Joblist.</span><span class="sxs-lookup"><span data-stu-id="abf6a-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="abf6a-112">Exemplo 2: obter todos os trabalhos com falha nos últimos 7 dias</span><span class="sxs-lookup"><span data-stu-id="abf6a-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="abf6a-113">Esse comando obtém trabalhos com falha da semana passada no cofre.</span><span class="sxs-lookup"><span data-stu-id="abf6a-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="abf6a-114">O parâmetro *from* especifica um período de sete dias no passado especificado em UTC.</span><span class="sxs-lookup"><span data-stu-id="abf6a-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="abf6a-115">O comando não especifica um valor para o parâmetro *to* .</span><span class="sxs-lookup"><span data-stu-id="abf6a-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="abf6a-116">Portanto, ele usa o valor padrão do tempo atual.</span><span class="sxs-lookup"><span data-stu-id="abf6a-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="abf6a-117">Exemplo 3: obter um trabalho em andamento e esperar a conclusão</span><span class="sxs-lookup"><span data-stu-id="abf6a-117">Example 3: Get an in-progress job and wait for completion</span></span>
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

<span data-ttu-id="abf6a-118">Este script sonda o primeiro trabalho que está em andamento até que o trabalho seja concluído.</span><span class="sxs-lookup"><span data-stu-id="abf6a-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="abf6a-119">OS</span><span class="sxs-lookup"><span data-stu-id="abf6a-119">PARAMETERS</span></span>

### <span data-ttu-id="abf6a-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="abf6a-120">-BackupManagementType</span></span>
<span data-ttu-id="abf6a-121">Especifica o tipo de gerenciamento de backup.</span><span class="sxs-lookup"><span data-stu-id="abf6a-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="abf6a-122">No momento, só há suporte para AzureVM, AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="abf6a-122">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf6a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abf6a-123">-DefaultProfile</span></span>
<span data-ttu-id="abf6a-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="abf6a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abf6a-125">-De</span><span class="sxs-lookup"><span data-stu-id="abf6a-125">-From</span></span>
<span data-ttu-id="abf6a-126">Especifica o início, como um objeto **DateTime** , de um intervalo de tempo para os trabalhos que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="abf6a-126">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="abf6a-127">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="abf6a-127">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="abf6a-128">Para obter mais informações sobre objetos **DateTime** , digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="abf6a-128">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="abf6a-129">Use o formato UTC para datas.</span><span class="sxs-lookup"><span data-stu-id="abf6a-129">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="abf6a-130">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="abf6a-130">-Job</span></span>
<span data-ttu-id="abf6a-131">Especifica o nome do trabalho de backup a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="abf6a-131">Specifies the name of the Backup job to get.</span></span>

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

### <span data-ttu-id="abf6a-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="abf6a-132">-JobId</span></span>
<span data-ttu-id="abf6a-133">Especifica a ID de um trabalho que o cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="abf6a-133">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="abf6a-134">A ID é a propriedade InstanceId de um objeto **AzureRmRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="abf6a-134">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="abf6a-135">Para obter um objeto **AzureRmRecoveryServicesBackupJob** , use Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="abf6a-135">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="abf6a-136">-Operação</span><span class="sxs-lookup"><span data-stu-id="abf6a-136">-Operation</span></span>
<span data-ttu-id="abf6a-137">Especifica uma operação dos trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="abf6a-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="abf6a-138">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="abf6a-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="abf6a-139">Fazer</span><span class="sxs-lookup"><span data-stu-id="abf6a-139">Backup</span></span>
- <span data-ttu-id="abf6a-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="abf6a-140">ConfigureBackup</span></span>
- <span data-ttu-id="abf6a-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="abf6a-141">DeleteBackupData</span></span>
- <span data-ttu-id="abf6a-142">Inscrição</span><span class="sxs-lookup"><span data-stu-id="abf6a-142">Register</span></span>
- <span data-ttu-id="abf6a-143">Restaurar</span><span class="sxs-lookup"><span data-stu-id="abf6a-143">Restore</span></span>
- <span data-ttu-id="abf6a-144">Desproteger</span><span class="sxs-lookup"><span data-stu-id="abf6a-144">UnProtect</span></span>
- <span data-ttu-id="abf6a-145">Cancele</span><span class="sxs-lookup"><span data-stu-id="abf6a-145">Unregister</span></span>

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

### <span data-ttu-id="abf6a-146">-Status</span><span class="sxs-lookup"><span data-stu-id="abf6a-146">-Status</span></span>
<span data-ttu-id="abf6a-147">Especifica um status dos trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="abf6a-147">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="abf6a-148">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="abf6a-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="abf6a-149">InProgress</span><span class="sxs-lookup"><span data-stu-id="abf6a-149">InProgress</span></span>
- <span data-ttu-id="abf6a-150">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="abf6a-150">Failed</span></span>
- <span data-ttu-id="abf6a-151">Cela</span><span class="sxs-lookup"><span data-stu-id="abf6a-151">Cancelled</span></span>
- <span data-ttu-id="abf6a-152">Cancelamento</span><span class="sxs-lookup"><span data-stu-id="abf6a-152">Cancelling</span></span>
- <span data-ttu-id="abf6a-153">Feito</span><span class="sxs-lookup"><span data-stu-id="abf6a-153">Completed</span></span>
- <span data-ttu-id="abf6a-154">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="abf6a-154">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="abf6a-155">-To</span><span class="sxs-lookup"><span data-stu-id="abf6a-155">-To</span></span>
<span data-ttu-id="abf6a-156">Especifica o fim, como um objeto **DateTime** , de um intervalo de tempo para os trabalhos que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="abf6a-156">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="abf6a-157">O valor padrão é a hora atual do sistema.</span><span class="sxs-lookup"><span data-stu-id="abf6a-157">The default value is the current system time.</span></span>
<span data-ttu-id="abf6a-158">Se você especificar esse parâmetro, também deverá especificar o parâmetro *from* .</span><span class="sxs-lookup"><span data-stu-id="abf6a-158">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="abf6a-159">Use o formato UTC para datas.</span><span class="sxs-lookup"><span data-stu-id="abf6a-159">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="abf6a-160">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="abf6a-160">-VaultId</span></span>
<span data-ttu-id="abf6a-161">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="abf6a-161">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="abf6a-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf6a-162">CommonParameters</span></span>
<span data-ttu-id="abf6a-163">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abf6a-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abf6a-164">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abf6a-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf6a-165">SENSORES</span><span class="sxs-lookup"><span data-stu-id="abf6a-165">INPUTS</span></span>

### <span data-ttu-id="abf6a-166">System. String</span><span class="sxs-lookup"><span data-stu-id="abf6a-166">System.String</span></span>
<span data-ttu-id="abf6a-167">Parâmetros: Vaultid (ByValue)</span><span class="sxs-lookup"><span data-stu-id="abf6a-167">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="abf6a-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="abf6a-168">OUTPUTS</span></span>

### <span data-ttu-id="abf6a-169">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="abf6a-169">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="abf6a-170">INFORMA</span><span class="sxs-lookup"><span data-stu-id="abf6a-170">NOTES</span></span>

## <span data-ttu-id="abf6a-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="abf6a-171">RELATED LINKS</span></span>

[<span data-ttu-id="abf6a-172">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="abf6a-172">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>](./Get-AzureRmRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="abf6a-173">Parar-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="abf6a-173">Stop-AzureRmRecoveryServicesBackupJob</span></span>](./Stop-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="abf6a-174">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="abf6a-174">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


