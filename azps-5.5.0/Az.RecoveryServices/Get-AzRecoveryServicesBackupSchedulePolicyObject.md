---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: d66b8515c6b2c3782c6f6c2b49d462dbb7bd1660
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114956"
---
# <span data-ttu-id="5307a-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="5307a-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="5307a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5307a-102">SYNOPSIS</span></span>
<span data-ttu-id="5307a-103">Obtém um objeto de política de agendamento base.</span><span class="sxs-lookup"><span data-stu-id="5307a-103">Gets a base schedule policy object.</span></span>

## <span data-ttu-id="5307a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5307a-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5307a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="5307a-105">DESCRIPTION</span></span>
<span data-ttu-id="5307a-106">O cmdlet **Get-AzRecoveryServicesBackupSchedulePolicyObject** obtém uma base **AzureRMRecoveryServicesSchedulePolicyObject.**</span><span class="sxs-lookup"><span data-stu-id="5307a-106">The **Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="5307a-107">Este objeto não é persistente no sistema.</span><span class="sxs-lookup"><span data-stu-id="5307a-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="5307a-108">É um objeto temporário que você pode manipular e usar com o cmdlet New-AzRecoveryServicesBackupProtectionPolicy para criar uma nova política de proteção de backup.</span><span class="sxs-lookup"><span data-stu-id="5307a-108">It is temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="5307a-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5307a-109">EXAMPLES</span></span>

### <span data-ttu-id="5307a-110">Exemplo 1: Definir a frequência do cronograma para semanalmente</span><span class="sxs-lookup"><span data-stu-id="5307a-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="5307a-111">O primeiro comando obtém o objeto de política de retenção e o armazena na variável $RetPol retenção.</span><span class="sxs-lookup"><span data-stu-id="5307a-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="5307a-112">O segundo comando obtém o objeto de política de agendamento e o armazena na $SchPol variável.</span><span class="sxs-lookup"><span data-stu-id="5307a-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="5307a-113">O terceiro comando altera a frequência da política de agendamento para semanal.</span><span class="sxs-lookup"><span data-stu-id="5307a-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="5307a-114">O último comando cria uma política de proteção de backup com o cronograma atualizado.</span><span class="sxs-lookup"><span data-stu-id="5307a-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="5307a-115">Exemplo 2: Definir o tempo de backup</span><span class="sxs-lookup"><span data-stu-id="5307a-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="5307a-116">O primeiro comando obtém o objeto de política de agendamento e o armazena na variável $SchPol calendário.</span><span class="sxs-lookup"><span data-stu-id="5307a-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="5307a-117">O segundo comando remove todos os tempos de executar agendados $SchPol.</span><span class="sxs-lookup"><span data-stu-id="5307a-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="5307a-118">O terceiro comando obtém a data e a hora atuais e o armazena na variável $DT dados.</span><span class="sxs-lookup"><span data-stu-id="5307a-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="5307a-119">O quarto comando substitui os tempos de executar agendados pela hora atual.</span><span class="sxs-lookup"><span data-stu-id="5307a-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="5307a-120">Você só pode fazer backup do AzureVM uma vez por dia, portanto, para redefinir o tempo de backup, você deve substituir o cronograma original.</span><span class="sxs-lookup"><span data-stu-id="5307a-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="5307a-121">O último comando cria uma política de proteção de backup usando o novo cronograma.</span><span class="sxs-lookup"><span data-stu-id="5307a-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="5307a-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5307a-122">PARAMETERS</span></span>

### <span data-ttu-id="5307a-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="5307a-123">-BackupManagementType</span></span>
<span data-ttu-id="5307a-124">A classe de recursos que está sendo protegida.</span><span class="sxs-lookup"><span data-stu-id="5307a-124">The class of resources being protected.</span></span> <span data-ttu-id="5307a-125">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="5307a-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5307a-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="5307a-126">AzureVM</span></span> 
- <span data-ttu-id="5307a-127">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="5307a-127">AzureStorage</span></span>
- <span data-ttu-id="5307a-128">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="5307a-128">AzureWorkload</span></span>

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

### <span data-ttu-id="5307a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5307a-129">-DefaultProfile</span></span>
<span data-ttu-id="5307a-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="5307a-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5307a-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="5307a-131">-WorkloadType</span></span>
<span data-ttu-id="5307a-132">Tipo de carga de trabalho do recurso.</span><span class="sxs-lookup"><span data-stu-id="5307a-132">Workload type of the resource.</span></span> <span data-ttu-id="5307a-133">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="5307a-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5307a-134">AzureVM</span><span class="sxs-lookup"><span data-stu-id="5307a-134">AzureVM</span></span> 
- <span data-ttu-id="5307a-135">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="5307a-135">AzureFiles</span></span>
- <span data-ttu-id="5307a-136">Mssql</span><span class="sxs-lookup"><span data-stu-id="5307a-136">MSSQL</span></span>


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

### <span data-ttu-id="5307a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5307a-137">CommonParameters</span></span>
<span data-ttu-id="5307a-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5307a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5307a-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5307a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5307a-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="5307a-140">INPUTS</span></span>

### <span data-ttu-id="5307a-141">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5307a-141">None</span></span>

## <span data-ttu-id="5307a-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="5307a-142">OUTPUTS</span></span>

### <span data-ttu-id="5307a-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="5307a-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="5307a-144">Notas</span><span class="sxs-lookup"><span data-stu-id="5307a-144">NOTES</span></span>

## <span data-ttu-id="5307a-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5307a-145">RELATED LINKS</span></span>

[<span data-ttu-id="5307a-146">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5307a-146">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="5307a-147">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5307a-147">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


