---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: 5bf91aafffb1c6fd650b5fd88f343897afc6c5d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888815"
---
# <span data-ttu-id="ba012-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="ba012-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="ba012-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba012-102">SYNOPSIS</span></span>
<span data-ttu-id="ba012-103">Obtém um objeto de política de agendamento base.</span><span class="sxs-lookup"><span data-stu-id="ba012-103">Gets a base schedule policy object.</span></span>

## <span data-ttu-id="ba012-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ba012-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba012-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ba012-105">DESCRIPTION</span></span>
<span data-ttu-id="ba012-106">O cmdlet **Get-AzRecoveryServicesBackupSchedulePolicyObject** obtém um **AzureRMRecoveryServicesSchedulePolicyObject**.</span><span class="sxs-lookup"><span data-stu-id="ba012-106">The **Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="ba012-107">Esse objeto não é persistente no sistema.</span><span class="sxs-lookup"><span data-stu-id="ba012-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="ba012-108">É um objeto temporário que você pode manipular e usar com o cmdlet New-AzRecoveryServicesBackupProtectionPolicy para criar uma nova política de proteção de backup.</span><span class="sxs-lookup"><span data-stu-id="ba012-108">It is temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="ba012-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ba012-109">EXAMPLES</span></span>

### <span data-ttu-id="ba012-110">Exemplo 1: definir a frequência de agendamento como semanal</span><span class="sxs-lookup"><span data-stu-id="ba012-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="ba012-111">O primeiro comando obtém o objeto de política de retenção e o armazena na variável $RetPol de retenção.</span><span class="sxs-lookup"><span data-stu-id="ba012-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="ba012-112">O segundo comando obtém o objeto de política de agendamento e o armazena na variável $SchPol de agendamento.</span><span class="sxs-lookup"><span data-stu-id="ba012-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="ba012-113">O terceiro comando altera a frequência da política de agendamento para semanalmente.</span><span class="sxs-lookup"><span data-stu-id="ba012-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="ba012-114">O último comando cria uma política de proteção de backup com a agenda atualizada.</span><span class="sxs-lookup"><span data-stu-id="ba012-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="ba012-115">Exemplo 2: definir o tempo de backup</span><span class="sxs-lookup"><span data-stu-id="ba012-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="ba012-116">O primeiro comando obtém o objeto de política de agendamento e o armazena na variável $SchPol de agendamento.</span><span class="sxs-lookup"><span data-stu-id="ba012-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="ba012-117">O segundo comando remove todos os horários de $SchPol.</span><span class="sxs-lookup"><span data-stu-id="ba012-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="ba012-118">O terceiro comando obtém a data e a hora atuais e o armazena na variável $DT.</span><span class="sxs-lookup"><span data-stu-id="ba012-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="ba012-119">O quarto comando substitui os horários de executar agendados pela hora atual.</span><span class="sxs-lookup"><span data-stu-id="ba012-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="ba012-120">Você só pode fazer backup do AzureVM uma vez por dia, portanto, para redefinir o tempo de backup, você deve substituir a agenda original.</span><span class="sxs-lookup"><span data-stu-id="ba012-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="ba012-121">O último comando cria uma política de proteção de backup usando a nova agenda.</span><span class="sxs-lookup"><span data-stu-id="ba012-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="ba012-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ba012-122">PARAMETERS</span></span>

### <span data-ttu-id="ba012-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="ba012-123">-BackupManagementType</span></span>
<span data-ttu-id="ba012-124">A classe de recursos que está sendo protegida.</span><span class="sxs-lookup"><span data-stu-id="ba012-124">The class of resources being protected.</span></span> <span data-ttu-id="ba012-125">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ba012-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ba012-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="ba012-126">AzureVM</span></span> 
- <span data-ttu-id="ba012-127">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="ba012-127">AzureStorage</span></span>
- <span data-ttu-id="ba012-128">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="ba012-128">AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba012-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba012-129">-DefaultProfile</span></span>
<span data-ttu-id="ba012-130">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ba012-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba012-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="ba012-131">-WorkloadType</span></span>
<span data-ttu-id="ba012-132">Tipo de carga de trabalho do recurso.</span><span class="sxs-lookup"><span data-stu-id="ba012-132">Workload type of the resource.</span></span> <span data-ttu-id="ba012-133">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ba012-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ba012-134">AzureVM</span><span class="sxs-lookup"><span data-stu-id="ba012-134">AzureVM</span></span> 
- <span data-ttu-id="ba012-135">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="ba012-135">AzureFiles</span></span>
- <span data-ttu-id="ba012-136">MSSQL</span><span class="sxs-lookup"><span data-stu-id="ba012-136">MSSQL</span></span>


```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba012-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba012-137">CommonParameters</span></span>
<span data-ttu-id="ba012-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba012-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba012-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba012-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba012-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba012-140">INPUTS</span></span>

### <span data-ttu-id="ba012-141">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ba012-141">None</span></span>

## <span data-ttu-id="ba012-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ba012-142">OUTPUTS</span></span>

### <span data-ttu-id="ba012-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="ba012-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="ba012-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="ba012-144">NOTES</span></span>

## <span data-ttu-id="ba012-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba012-145">RELATED LINKS</span></span>

[<span data-ttu-id="ba012-146">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ba012-146">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="ba012-147">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ba012-147">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


