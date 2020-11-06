---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 1f7dcd013bb91b8ba209cf3f7b031a90f7bb49cc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599605"
---
# <span data-ttu-id="f117d-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f117d-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="f117d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f117d-102">SYNOPSIS</span></span>
<span data-ttu-id="f117d-103">Modifica uma política de proteção de backup.</span><span class="sxs-lookup"><span data-stu-id="f117d-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="f117d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f117d-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f117d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f117d-105">DESCRIPTION</span></span>
<span data-ttu-id="f117d-106">O cmdlet **set-AzBackupProtectionPolicy** modifica uma política de proteção de backup do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="f117d-106">The **Set-AzBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="f117d-107">Você pode modificar o agendamento de backup e os componentes da política de retenção.</span><span class="sxs-lookup"><span data-stu-id="f117d-107">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="f117d-108">Todas as alterações feitas afetam o backup e a retenção dos itens associados à política.</span><span class="sxs-lookup"><span data-stu-id="f117d-108">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="f117d-109">Defina o contexto do cofre usando o cmdlet Set-AzRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="f117d-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="f117d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f117d-110">EXAMPLES</span></span>

### <span data-ttu-id="f117d-111">Exemplo 1: modificar uma política de proteção de backup</span><span class="sxs-lookup"><span data-stu-id="f117d-111">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="f117d-112">O primeiro comando obtém um objeto SchedulePolicy base e, em seguida, armazena-o na variável $SchPol.</span><span class="sxs-lookup"><span data-stu-id="f117d-112">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="f117d-113">O segundo comando Remove todos os horários de execução agendados da política de agendamento em $SchPol.</span><span class="sxs-lookup"><span data-stu-id="f117d-113">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="f117d-114">O terceiro comando usa o cmdlet Get-Date para obter a data e hora atuais e, em seguida, armazena-o na variável $DT.</span><span class="sxs-lookup"><span data-stu-id="f117d-114">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="f117d-115">O quarto comando adiciona a data e a hora no $DT ao tempo de execução do cronograma para a política de agendamento.</span><span class="sxs-lookup"><span data-stu-id="f117d-115">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>
<span data-ttu-id="f117d-116">O quinto comando obtém um objeto de política de retenção base e, em seguida, armazena-o na variável $RetPol.</span><span class="sxs-lookup"><span data-stu-id="f117d-116">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="f117d-117">O sexto comando define a duração da retenção para 365 dias.</span><span class="sxs-lookup"><span data-stu-id="f117d-117">The sixth command sets the retention duration to 365 days.</span></span>
<span data-ttu-id="f117d-118">O sétimo comando obtém a política de proteção de backup chamada NewPolicy e a armazena na variável $Pol.</span><span class="sxs-lookup"><span data-stu-id="f117d-118">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="f117d-119">O comando final modifica a política de proteção de backup no $Pol usando a política de agendamento em $SchPol e a política de retenção em $RetPol.</span><span class="sxs-lookup"><span data-stu-id="f117d-119">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="f117d-120">OS</span><span class="sxs-lookup"><span data-stu-id="f117d-120">PARAMETERS</span></span>

### <span data-ttu-id="f117d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f117d-121">-DefaultProfile</span></span>
<span data-ttu-id="f117d-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f117d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f117d-123">-Política</span><span class="sxs-lookup"><span data-stu-id="f117d-123">-Policy</span></span>
<span data-ttu-id="f117d-124">Especifica a política de proteção de backup que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="f117d-124">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="f117d-125">Para obter um objeto **BackupProtectionPolicy** , use o cmdlet Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="f117d-125">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f117d-126">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f117d-126">-RetentionPolicy</span></span>
<span data-ttu-id="f117d-127">Especifica a política de retenção básica.</span><span class="sxs-lookup"><span data-stu-id="f117d-127">Specifies the base retention policy.</span></span>
<span data-ttu-id="f117d-128">Para obter um objeto **RetentionPolicy** , use o cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="f117d-128">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f117d-129">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="f117d-129">-SchedulePolicy</span></span>
<span data-ttu-id="f117d-130">Especifica o objeto da política de cronograma básico.</span><span class="sxs-lookup"><span data-stu-id="f117d-130">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="f117d-131">Para obter um objeto **SchedulePolicy** , use o objeto Get-AzRecoveryServicesBackupSchedulePolicyObject.</span><span class="sxs-lookup"><span data-stu-id="f117d-131">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f117d-132">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="f117d-132">-VaultId</span></span>
<span data-ttu-id="f117d-133">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="f117d-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f117d-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f117d-134">-Confirm</span></span>
<span data-ttu-id="f117d-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f117d-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f117d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f117d-136">-WhatIf</span></span>
<span data-ttu-id="f117d-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f117d-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f117d-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f117d-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f117d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f117d-139">CommonParameters</span></span>
<span data-ttu-id="f117d-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f117d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f117d-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f117d-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f117d-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f117d-142">INPUTS</span></span>

### <span data-ttu-id="f117d-143">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="f117d-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="f117d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f117d-144">System.String</span></span>

## <span data-ttu-id="f117d-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f117d-145">OUTPUTS</span></span>

### <span data-ttu-id="f117d-146">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="f117d-146">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="f117d-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f117d-147">NOTES</span></span>

## <span data-ttu-id="f117d-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f117d-148">RELATED LINKS</span></span>

[<span data-ttu-id="f117d-149">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f117d-149">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="f117d-150">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="f117d-150">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="f117d-151">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f117d-151">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="f117d-152">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f117d-152">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


