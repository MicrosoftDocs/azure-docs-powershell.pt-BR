---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: a871aa624aaf8b7f24d06bd0ff04a45e29b95468
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429170"
---
# <span data-ttu-id="e27d0-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e27d0-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="e27d0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e27d0-102">SYNOPSIS</span></span>
<span data-ttu-id="e27d0-103">Cria uma política de proteção de backup.</span><span class="sxs-lookup"><span data-stu-id="e27d0-103">Creates a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e27d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e27d0-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e27d0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e27d0-105">DESCRIPTION</span></span>
<span data-ttu-id="e27d0-106">O cmdlet **New-AzureRmRecoveryServicesBackupProtectionPolicy** cria uma política de proteção de backup em um cofre.</span><span class="sxs-lookup"><span data-stu-id="e27d0-106">The **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="e27d0-107">Uma política de proteção está associada a pelo menos uma política de retenção.</span><span class="sxs-lookup"><span data-stu-id="e27d0-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="e27d0-108">A política de retenção define por quanto tempo um ponto de recuperação é mantido com o backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="e27d0-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>

<span data-ttu-id="e27d0-109">Você pode usar o cmdlet Get-AzureRmRecoveryServicesBackupRetentionPolicyObject para obter a política de retenção padrão.</span><span class="sxs-lookup"><span data-stu-id="e27d0-109">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="e27d0-110">E você pode usar o cmdlet Get-AzureRmRecoveryServicesBackupSchedulePolicyObject para obter a política de agendamento padrão.</span><span class="sxs-lookup"><span data-stu-id="e27d0-110">And you can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="e27d0-111">Os objetos **SchedulePolicy** e **RetentionPolicy** são usados como entradas para o cmdlet **New-AzureRmRecoveryServicesBackupProtectionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="e27d0-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>

<span data-ttu-id="e27d0-112">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="e27d0-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="e27d0-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e27d0-113">EXAMPLES</span></span>

### <span data-ttu-id="e27d0-114">Exemplo 1: criar uma política de proteção de backup</span><span class="sxs-lookup"><span data-stu-id="e27d0-114">Example 1: Create a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="e27d0-115">O primeiro comando obtém um **SchedulePolicyObject** base e, em seguida, armazena-o na variável $SchPol.</span><span class="sxs-lookup"><span data-stu-id="e27d0-115">The first command gets a base **SchedulePolicyObject** , and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="e27d0-116">O segundo comando Remove todos os horários de execução agendados da política de agendamento em $SchPol.</span><span class="sxs-lookup"><span data-stu-id="e27d0-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>

<span data-ttu-id="e27d0-117">O terceiro comando usa o cmdlet Get-Date para obter a data e hora atuais.</span><span class="sxs-lookup"><span data-stu-id="e27d0-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>

<span data-ttu-id="e27d0-118">O quarto comando adiciona a data e a hora atuais no $Dt como o tempo de execução programado para a política de agendamento.</span><span class="sxs-lookup"><span data-stu-id="e27d0-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>

<span data-ttu-id="e27d0-119">O quinto comando obtém um objeto **RetentionPolicy** base e, em seguida, armazena-o na variável $RetPol.</span><span class="sxs-lookup"><span data-stu-id="e27d0-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="e27d0-120">O sexto comando define a política de duração da retenção como 365 dias.</span><span class="sxs-lookup"><span data-stu-id="e27d0-120">The sixth command sets the retention duration policy to 365 days.</span></span>

<span data-ttu-id="e27d0-121">O comando final cria um objeto **BackupProtectionPolicy** com base no agendamento e nas políticas de retenção criados pelos comandos anteriores.</span><span class="sxs-lookup"><span data-stu-id="e27d0-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

## <span data-ttu-id="e27d0-122">OS</span><span class="sxs-lookup"><span data-stu-id="e27d0-122">PARAMETERS</span></span>

### <span data-ttu-id="e27d0-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="e27d0-123">-BackupManagementType</span></span>
<span data-ttu-id="e27d0-124">Especifica o tipo de gerenciamento de backup.</span><span class="sxs-lookup"><span data-stu-id="e27d0-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="e27d0-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e27d0-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e27d0-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="e27d0-126">AzureVM</span></span> 
- <span data-ttu-id="e27d0-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="e27d0-127">AzureSQLDatabase</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e27d0-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e27d0-128">-Name</span></span>
<span data-ttu-id="e27d0-129">Especifica o nome da política.</span><span class="sxs-lookup"><span data-stu-id="e27d0-129">Specifies the name of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e27d0-130">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e27d0-130">-RetentionPolicy</span></span>
<span data-ttu-id="e27d0-131">Especifica o objeto base **RetentionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="e27d0-131">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="e27d0-132">Você pode usar o cmdlet Get-AzureRmRecoveryServicesBackupRetentionPolicyObject para obter um objeto **RetentionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="e27d0-132">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e27d0-133">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="e27d0-133">-SchedulePolicy</span></span>
<span data-ttu-id="e27d0-134">Especifica o objeto base **SchedulePolicy** .</span><span class="sxs-lookup"><span data-stu-id="e27d0-134">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="e27d0-135">Você pode usar o cmdlet Get-AzureRmRecoveryServicesBackupSchedulePolicyObject para obter um objeto **SchedulePolicy** .</span><span class="sxs-lookup"><span data-stu-id="e27d0-135">You can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e27d0-136">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="e27d0-136">-WorkloadType</span></span>
<span data-ttu-id="e27d0-137">Especifica o tipo de carga de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e27d0-137">Specifies the workload type.</span></span>
<span data-ttu-id="e27d0-138">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e27d0-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e27d0-139">AzureVM</span><span class="sxs-lookup"><span data-stu-id="e27d0-139">AzureVM</span></span> 
- <span data-ttu-id="e27d0-140">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="e27d0-140">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e27d0-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e27d0-141">-DefaultProfile</span></span>
<span data-ttu-id="e27d0-142">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e27d0-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e27d0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e27d0-143">CommonParameters</span></span>
<span data-ttu-id="e27d0-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e27d0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e27d0-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e27d0-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e27d0-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e27d0-146">INPUTS</span></span>

## <span data-ttu-id="e27d0-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e27d0-147">OUTPUTS</span></span>

### <span data-ttu-id="e27d0-148">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="e27d0-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="e27d0-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e27d0-149">NOTES</span></span>

## <span data-ttu-id="e27d0-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e27d0-150">RELATED LINKS</span></span>

[<span data-ttu-id="e27d0-151">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="e27d0-151">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="e27d0-152">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e27d0-152">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="e27d0-153">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="e27d0-153">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="e27d0-154">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="e27d0-154">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="e27d0-155">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e27d0-155">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="e27d0-156">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e27d0-156">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


