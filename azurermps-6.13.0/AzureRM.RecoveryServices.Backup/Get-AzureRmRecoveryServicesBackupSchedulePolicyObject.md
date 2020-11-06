---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: cc65ea2b2f050eb356d5be22c935aebb131f5cfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430080"
---
# <span data-ttu-id="9b08e-101">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="9b08e-101">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="9b08e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b08e-102">SYNOPSIS</span></span>
<span data-ttu-id="9b08e-103">Obtém um objeto de política de cronograma básico.</span><span class="sxs-lookup"><span data-stu-id="9b08e-103">Gets a base schedule policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b08e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b08e-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b08e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9b08e-105">DESCRIPTION</span></span>
<span data-ttu-id="9b08e-106">O cmdlet **Get-AzureRmRecoveryServicesBackupSchedulePolicyObject** tem um **AzureRMRecoveryServicesSchedulePolicyObject** base.</span><span class="sxs-lookup"><span data-stu-id="9b08e-106">The **Get-AzureRmRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="9b08e-107">Esse objeto não é mantido no sistema.</span><span class="sxs-lookup"><span data-stu-id="9b08e-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="9b08e-108">É um objeto temporário que você pode manipular e usar com o cmdlet New-AzureRmRecoveryServicesBackupProtectionPolicy para criar uma nova política de proteção de backup.</span><span class="sxs-lookup"><span data-stu-id="9b08e-108">It is temporary object that you can manipulate and use with the New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="9b08e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b08e-109">EXAMPLES</span></span>

### <span data-ttu-id="9b08e-110">Exemplo 1: definir a frequência do cronograma como semanal</span><span class="sxs-lookup"><span data-stu-id="9b08e-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="9b08e-111">O primeiro comando obtém o objeto da política de retenção e, em seguida, armazena-o na variável $RetPol.</span><span class="sxs-lookup"><span data-stu-id="9b08e-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="9b08e-112">O segundo comando obtém o objeto de política de agendamento e, em seguida, armazena-o na variável $SchPol.</span><span class="sxs-lookup"><span data-stu-id="9b08e-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="9b08e-113">O terceiro comando altera a frequência da política de agendamento para semanalmente.</span><span class="sxs-lookup"><span data-stu-id="9b08e-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="9b08e-114">O último comando cria uma política de proteção de backup com o cronograma atualizado.</span><span class="sxs-lookup"><span data-stu-id="9b08e-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="9b08e-115">Exemplo 2: definir o tempo de backup</span><span class="sxs-lookup"><span data-stu-id="9b08e-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="9b08e-116">O primeiro comando obtém o objeto de política de agendamento e, em seguida, armazena-o na variável $SchPol.</span><span class="sxs-lookup"><span data-stu-id="9b08e-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="9b08e-117">O segundo comando Remove todos os horários de execução agendados de $SchPol.</span><span class="sxs-lookup"><span data-stu-id="9b08e-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="9b08e-118">O terceiro comando obtém a data e a hora atuais e, em seguida, armazena-o na variável $DT.</span><span class="sxs-lookup"><span data-stu-id="9b08e-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="9b08e-119">O quarto comando substitui os tempos de execução agendados pelo tempo atual.</span><span class="sxs-lookup"><span data-stu-id="9b08e-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="9b08e-120">Você só pode fazer backup de AzureVM uma vez por dia, portanto, para redefinir o tempo de backup, você deve substituir o cronograma original.</span><span class="sxs-lookup"><span data-stu-id="9b08e-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="9b08e-121">O último comando cria uma política de proteção de backup usando o novo cronograma.</span><span class="sxs-lookup"><span data-stu-id="9b08e-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="9b08e-122">OS</span><span class="sxs-lookup"><span data-stu-id="9b08e-122">PARAMETERS</span></span>

### <span data-ttu-id="9b08e-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="9b08e-123">-BackupManagementType</span></span>
<span data-ttu-id="9b08e-124">Especifica o tipo de gerenciamento de backup.</span><span class="sxs-lookup"><span data-stu-id="9b08e-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="9b08e-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9b08e-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9b08e-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="9b08e-126">AzureVM</span></span> 
- <span data-ttu-id="9b08e-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="9b08e-127">AzureSQLDatabase</span></span>
- <span data-ttu-id="9b08e-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="9b08e-128">AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b08e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b08e-129">-DefaultProfile</span></span>
<span data-ttu-id="9b08e-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b08e-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b08e-131">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="9b08e-131">-WorkloadType</span></span>
<span data-ttu-id="9b08e-132">Especifica o tipo de carga de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9b08e-132">Specifies the workload type.</span></span>
<span data-ttu-id="9b08e-133">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9b08e-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9b08e-134">AzureVM</span><span class="sxs-lookup"><span data-stu-id="9b08e-134">AzureVM</span></span> 
- <span data-ttu-id="9b08e-135">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="9b08e-135">AzureSQLDatabase</span></span>
- <span data-ttu-id="9b08e-136">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="9b08e-136">AzureFiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b08e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b08e-137">CommonParameters</span></span>
<span data-ttu-id="9b08e-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b08e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b08e-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b08e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b08e-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9b08e-140">INPUTS</span></span>

### <span data-ttu-id="9b08e-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9b08e-141">None</span></span>

## <span data-ttu-id="9b08e-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9b08e-142">OUTPUTS</span></span>

### <span data-ttu-id="9b08e-143">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="9b08e-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="9b08e-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9b08e-144">NOTES</span></span>

## <span data-ttu-id="9b08e-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b08e-145">RELATED LINKS</span></span>

[<span data-ttu-id="9b08e-146">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9b08e-146">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="9b08e-147">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9b08e-147">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


