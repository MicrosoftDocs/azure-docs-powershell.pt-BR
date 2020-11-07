---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: 71650d36c319536db5ad96aa142e2712e229d712
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772997"
---
# <span data-ttu-id="41974-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="41974-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="41974-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41974-102">SYNOPSIS</span></span>
<span data-ttu-id="41974-103">Obtém um objeto de política de cronograma básico.</span><span class="sxs-lookup"><span data-stu-id="41974-103">Gets a base schedule policy object.</span></span>

## <span data-ttu-id="41974-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41974-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41974-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41974-105">DESCRIPTION</span></span>
<span data-ttu-id="41974-106">O cmdlet **Get-AzRecoveryServicesBackupSchedulePolicyObject** tem um **AzureRMRecoveryServicesSchedulePolicyObject** base.</span><span class="sxs-lookup"><span data-stu-id="41974-106">The **Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="41974-107">Esse objeto não é mantido no sistema.</span><span class="sxs-lookup"><span data-stu-id="41974-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="41974-108">É um objeto temporário que você pode manipular e usar com o cmdlet New-AzRecoveryServicesBackupProtectionPolicy para criar uma nova política de proteção de backup.</span><span class="sxs-lookup"><span data-stu-id="41974-108">It is temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="41974-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41974-109">EXAMPLES</span></span>

### <span data-ttu-id="41974-110">Exemplo 1: definir a frequência do cronograma como semanal</span><span class="sxs-lookup"><span data-stu-id="41974-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="41974-111">O primeiro comando obtém o objeto da política de retenção e, em seguida, armazena-o na variável $RetPol.</span><span class="sxs-lookup"><span data-stu-id="41974-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="41974-112">O segundo comando obtém o objeto de política de agendamento e, em seguida, armazena-o na variável $SchPol.</span><span class="sxs-lookup"><span data-stu-id="41974-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="41974-113">O terceiro comando altera a frequência da política de agendamento para semanalmente.</span><span class="sxs-lookup"><span data-stu-id="41974-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="41974-114">O último comando cria uma política de proteção de backup com o cronograma atualizado.</span><span class="sxs-lookup"><span data-stu-id="41974-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="41974-115">Exemplo 2: definir o tempo de backup</span><span class="sxs-lookup"><span data-stu-id="41974-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="41974-116">O primeiro comando obtém o objeto de política de agendamento e, em seguida, armazena-o na variável $SchPol.</span><span class="sxs-lookup"><span data-stu-id="41974-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="41974-117">O segundo comando Remove todos os horários de execução agendados de $SchPol.</span><span class="sxs-lookup"><span data-stu-id="41974-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="41974-118">O terceiro comando obtém a data e a hora atuais e, em seguida, armazena-o na variável $DT.</span><span class="sxs-lookup"><span data-stu-id="41974-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="41974-119">O quarto comando substitui os tempos de execução agendados pelo tempo atual.</span><span class="sxs-lookup"><span data-stu-id="41974-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="41974-120">Você só pode fazer backup de AzureVM uma vez por dia, portanto, para redefinir o tempo de backup, você deve substituir o cronograma original.</span><span class="sxs-lookup"><span data-stu-id="41974-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="41974-121">O último comando cria uma política de proteção de backup usando o novo cronograma.</span><span class="sxs-lookup"><span data-stu-id="41974-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="41974-122">OS</span><span class="sxs-lookup"><span data-stu-id="41974-122">PARAMETERS</span></span>

### <span data-ttu-id="41974-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="41974-123">-BackupManagementType</span></span>
<span data-ttu-id="41974-124">Especifica o tipo de gerenciamento de backup.</span><span class="sxs-lookup"><span data-stu-id="41974-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="41974-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="41974-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="41974-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="41974-126">AzureVM</span></span> 
- <span data-ttu-id="41974-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="41974-127">AzureSQLDatabase</span></span>
- <span data-ttu-id="41974-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="41974-128">AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41974-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41974-129">-DefaultProfile</span></span>
<span data-ttu-id="41974-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="41974-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41974-131">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="41974-131">-WorkloadType</span></span>
<span data-ttu-id="41974-132">Especifica o tipo de carga de trabalho.</span><span class="sxs-lookup"><span data-stu-id="41974-132">Specifies the workload type.</span></span>
<span data-ttu-id="41974-133">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="41974-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="41974-134">AzureVM</span><span class="sxs-lookup"><span data-stu-id="41974-134">AzureVM</span></span> 
- <span data-ttu-id="41974-135">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="41974-135">AzureSQLDatabase</span></span>
- <span data-ttu-id="41974-136">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="41974-136">AzureFiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41974-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41974-137">CommonParameters</span></span>
<span data-ttu-id="41974-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41974-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41974-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41974-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41974-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41974-140">INPUTS</span></span>

### <span data-ttu-id="41974-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="41974-141">None</span></span>

## <span data-ttu-id="41974-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41974-142">OUTPUTS</span></span>

### <span data-ttu-id="41974-143">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="41974-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="41974-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41974-144">NOTES</span></span>

## <span data-ttu-id="41974-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41974-145">RELATED LINKS</span></span>

[<span data-ttu-id="41974-146">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="41974-146">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="41974-147">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="41974-147">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


