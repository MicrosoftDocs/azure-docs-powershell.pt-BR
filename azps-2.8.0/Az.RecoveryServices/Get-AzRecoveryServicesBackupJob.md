---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: cc23d8535e7aaca656379811121ed09bad2f64bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773018"
---
# <span data-ttu-id="f6982-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f6982-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="f6982-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6982-102">SYNOPSIS</span></span>

<span data-ttu-id="f6982-103">Obtém trabalhos de backup.</span><span class="sxs-lookup"><span data-stu-id="f6982-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="f6982-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6982-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6982-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f6982-105">DESCRIPTION</span></span>

<span data-ttu-id="f6982-106">O cmdlet **Get-AzRecoveryServicesBackupJob** Obtém trabalhos de backup do Azure para um cofre específico.</span><span class="sxs-lookup"><span data-stu-id="f6982-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="f6982-107">Defina o contexto do cofre usando o parâmetro-Cofreid.</span><span class="sxs-lookup"><span data-stu-id="f6982-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="f6982-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6982-108">EXAMPLES</span></span>

### <span data-ttu-id="f6982-109">Exemplo 1: obter todos os trabalhos em andamento</span><span class="sxs-lookup"><span data-stu-id="f6982-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="f6982-110">O primeiro comando obtém o status de um trabalho em andamento como uma matriz e, em seguida, armazena-o na variável $Joblist.</span><span class="sxs-lookup"><span data-stu-id="f6982-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="f6982-111">O segundo comando exibe o primeiro item na matriz de $Joblist.</span><span class="sxs-lookup"><span data-stu-id="f6982-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="f6982-112">Exemplo 2: obter todos os trabalhos com falha nos últimos 7 dias</span><span class="sxs-lookup"><span data-stu-id="f6982-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="f6982-113">Esse comando obtém trabalhos com falha da semana passada no cofre.</span><span class="sxs-lookup"><span data-stu-id="f6982-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="f6982-114">O parâmetro *from* especifica um período de sete dias no passado especificado em UTC.</span><span class="sxs-lookup"><span data-stu-id="f6982-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="f6982-115">O comando não especifica um valor para o parâmetro *to* .</span><span class="sxs-lookup"><span data-stu-id="f6982-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="f6982-116">Portanto, ele usa o valor padrão do tempo atual.</span><span class="sxs-lookup"><span data-stu-id="f6982-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="f6982-117">Exemplo 3: obter um trabalho em andamento e esperar a conclusão</span><span class="sxs-lookup"><span data-stu-id="f6982-117">Example 3: Get an in-progress job and wait for completion</span></span>

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

<span data-ttu-id="f6982-118">Este script sonda o primeiro trabalho que está em andamento até que o trabalho seja concluído.</span><span class="sxs-lookup"><span data-stu-id="f6982-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="f6982-119">Observação: você pode usar o cmdlet **Wait-AzRecoveryServicesBackupJob** para esperar que um trabalho de backup do Azure seja concluído em vez de While.</span><span class="sxs-lookup"><span data-stu-id="f6982-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

## <span data-ttu-id="f6982-120">OS</span><span class="sxs-lookup"><span data-stu-id="f6982-120">PARAMETERS</span></span>

### <span data-ttu-id="f6982-121">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="f6982-121">-BackupManagementType</span></span>

<span data-ttu-id="f6982-122">Especifica o tipo de gerenciamento de backup.</span><span class="sxs-lookup"><span data-stu-id="f6982-122">Specifies the Backup management type.</span></span>
<span data-ttu-id="f6982-123">No momento, só há suporte para AzureVM, AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="f6982-123">Currently, only AzureVM, AzureStorage is supported.</span></span>

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

### <span data-ttu-id="f6982-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6982-124">-DefaultProfile</span></span>

<span data-ttu-id="f6982-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6982-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6982-126">-De</span><span class="sxs-lookup"><span data-stu-id="f6982-126">-From</span></span>

<span data-ttu-id="f6982-127">Especifica o início, como um objeto **DateTime** , de um intervalo de tempo para os trabalhos que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="f6982-127">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="f6982-128">Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="f6982-128">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="f6982-129">Para obter mais informações sobre objetos **DateTime** , digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="f6982-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="f6982-130">Use o formato UTC para datas.</span><span class="sxs-lookup"><span data-stu-id="f6982-130">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="f6982-131">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="f6982-131">-Job</span></span>

<span data-ttu-id="f6982-132">Especifica o trabalho a obter.</span><span class="sxs-lookup"><span data-stu-id="f6982-132">Specifies the job to get.</span></span>

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

### <span data-ttu-id="f6982-133">-JobId</span><span class="sxs-lookup"><span data-stu-id="f6982-133">-JobId</span></span>

<span data-ttu-id="f6982-134">Especifica a ID de um trabalho que o cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="f6982-134">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="f6982-135">A ID é a propriedade JobId de um objeto **Microsoft. Azure. Commands. recoveryservices. backup. cmdlets. Models. JobBase** .</span><span class="sxs-lookup"><span data-stu-id="f6982-135">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="f6982-136">-Operação</span><span class="sxs-lookup"><span data-stu-id="f6982-136">-Operation</span></span>

<span data-ttu-id="f6982-137">Especifica uma operação dos trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="f6982-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="f6982-138">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f6982-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f6982-139">Fazer</span><span class="sxs-lookup"><span data-stu-id="f6982-139">Backup</span></span>
- <span data-ttu-id="f6982-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="f6982-140">ConfigureBackup</span></span>
- <span data-ttu-id="f6982-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="f6982-141">DeleteBackupData</span></span>
- <span data-ttu-id="f6982-142">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="f6982-142">DisableBackup</span></span>
- <span data-ttu-id="f6982-143">Restaurar</span><span class="sxs-lookup"><span data-stu-id="f6982-143">Restore</span></span>

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

### <span data-ttu-id="f6982-144">-Status</span><span class="sxs-lookup"><span data-stu-id="f6982-144">-Status</span></span>

<span data-ttu-id="f6982-145">Especifica um status dos trabalhos que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="f6982-145">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="f6982-146">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f6982-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f6982-147">InProgress</span><span class="sxs-lookup"><span data-stu-id="f6982-147">InProgress</span></span>
- <span data-ttu-id="f6982-148">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="f6982-148">Failed</span></span>
- <span data-ttu-id="f6982-149">Cela</span><span class="sxs-lookup"><span data-stu-id="f6982-149">Cancelled</span></span>
- <span data-ttu-id="f6982-150">Cancelamento</span><span class="sxs-lookup"><span data-stu-id="f6982-150">Cancelling</span></span>
- <span data-ttu-id="f6982-151">Feito</span><span class="sxs-lookup"><span data-stu-id="f6982-151">Completed</span></span>
- <span data-ttu-id="f6982-152">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="f6982-152">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="f6982-153">-To</span><span class="sxs-lookup"><span data-stu-id="f6982-153">-To</span></span>

<span data-ttu-id="f6982-154">Especifica o fim, como um objeto **DateTime** , de um intervalo de tempo para os trabalhos que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="f6982-154">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="f6982-155">O valor padrão é a hora atual do sistema.</span><span class="sxs-lookup"><span data-stu-id="f6982-155">The default value is the current system time.</span></span>
<span data-ttu-id="f6982-156">Se você especificar esse parâmetro, também deverá especificar o parâmetro **-from** .</span><span class="sxs-lookup"><span data-stu-id="f6982-156">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="f6982-157">Use o formato UTC para datas.</span><span class="sxs-lookup"><span data-stu-id="f6982-157">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="f6982-158">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="f6982-158">-VaultId</span></span>

<span data-ttu-id="f6982-159">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="f6982-159">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f6982-160">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6982-160">-CommonParameters</span></span>

<span data-ttu-id="f6982-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6982-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6982-162">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6982-162">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6982-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f6982-163">INPUTS</span></span>

### <span data-ttu-id="f6982-164">System. String</span><span class="sxs-lookup"><span data-stu-id="f6982-164">System.String</span></span>

## <span data-ttu-id="f6982-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f6982-165">OUTPUTS</span></span>

### <span data-ttu-id="f6982-166">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="f6982-166">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="f6982-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f6982-167">NOTES</span></span>

## <span data-ttu-id="f6982-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6982-168">RELATED LINKS</span></span>

[<span data-ttu-id="f6982-169">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="f6982-169">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="f6982-170">Parar-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f6982-170">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="f6982-171">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f6982-171">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
