---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: e9f89a39b283f073c0fe826f22157570be29e74b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114541"
---
# <span data-ttu-id="76e3e-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="76e3e-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="76e3e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76e3e-102">SYNOPSIS</span></span>
<span data-ttu-id="76e3e-103">Modifica uma política de proteção de backup.</span><span class="sxs-lookup"><span data-stu-id="76e3e-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="76e3e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76e3e-104">SYNTAX</span></span>

### <span data-ttu-id="76e3e-105">ModifyPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="76e3e-105">ModifyPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76e3e-106">FixPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="76e3e-106">FixPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-FixForInconsistentItems]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76e3e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="76e3e-107">DESCRIPTION</span></span>
<span data-ttu-id="76e3e-108">O cmdlet **Set-AzRecoveryServicesBackupProtectionPolicy** modifica uma política de proteção de backup do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="76e3e-108">The **Set-AzRecoveryServicesBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="76e3e-109">Você pode modificar os componentes da política de retenção e agendamento de backup.</span><span class="sxs-lookup"><span data-stu-id="76e3e-109">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="76e3e-110">As alterações feitas afetam o backup e a retenção dos itens associados à política.</span><span class="sxs-lookup"><span data-stu-id="76e3e-110">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="76e3e-111">De definir o contexto do cofre usando o Set-AzRecoveryServicesVaultContext cmdlet antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="76e3e-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="76e3e-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="76e3e-112">EXAMPLES</span></span>

### <span data-ttu-id="76e3e-113">Exemplo 1: modificar uma política de proteção de backup</span><span class="sxs-lookup"><span data-stu-id="76e3e-113">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Time = Get-Date
PS C:\> $Time1 = Get-Date -Year $Time.Year -Month $Time.Month -Day $Time.Day -Hour $Time.Hour -Minute 0 -Second 0 -Millisecond 0
PS C:\> $Time1 = $Time1.ToUniversalTime()
PS C:\> $SchPol.ScheduleRunTimes.Add($Time1)
PS C:\> $SchPol.ScheduleRunFrequency.Clear
PS C:\> $SchPol.ScheduleRunDays.Add("Monday")
PS C:\> $SchPol.ScheduleRunFrequency="Weekly"
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.IsDailyScheduleEnabled=$false
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 0
PS C:\> $RetPol.IsWeeklyScheduleEnabled=$true 
PS C:\> $RetPol.WeeklySchedule.DaysOfTheWeek.Add("Monday")
PS C:\> $RetPol.WeeklySchedule.DurationCountInWeeks = 365
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "azurefiles" -Name "azurefilesvault"
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "TestPolicy" -VaultId $vault.ID
PS C:\> $Pol.SnapshotRetentionInDays=5
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="76e3e-114">Aqui está a descrição de alto nível das etapas a serem seguidas para modificar uma política de proteção:</span><span class="sxs-lookup"><span data-stu-id="76e3e-114">Here is the high-level description of the steps to be followed for modifying a protection policy:</span></span> 
1.  <span data-ttu-id="76e3e-115">Obter um SchedulePolicyObject base e base RetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="76e3e-115">Get a base SchedulePolicyObject and base RetentionPolicyObject.</span></span> <span data-ttu-id="76e3e-116">Armazene-os em alguma variável.</span><span class="sxs-lookup"><span data-stu-id="76e3e-116">Store them in some variable.</span></span>
2.  <span data-ttu-id="76e3e-117">De definir os diferentes parâmetros do objeto de política de retenção e agendamento de acordo com o seu requisito.</span><span class="sxs-lookup"><span data-stu-id="76e3e-117">Set the different parameters of schedule and retention policy object as per your requirement.</span></span> <span data-ttu-id="76e3e-118">Por exemplo, no exemplo de script acima, estamos tentando definir uma política de proteção semanal.</span><span class="sxs-lookup"><span data-stu-id="76e3e-118">For example- In the above sample script, we are trying to set a weekly protection policy.</span></span> <span data-ttu-id="76e3e-119">Portanto, nós alterámos a frequência do cronograma para "Semanal" e também atualizamos o tempo de executar o cronograma.</span><span class="sxs-lookup"><span data-stu-id="76e3e-119">Hence, we changed the schedule frequency to "Weekly" and also updated the schedule run time.</span></span> <span data-ttu-id="76e3e-120">No objeto de política de retenção, atualizamos a duração semanal de retenção e definimos o sinalizador correto de "agenda semanal habilitado".</span><span class="sxs-lookup"><span data-stu-id="76e3e-120">In the retention policy object, we updated the weekly retention duration and set the correct "weekly schedule enabled" flag.</span></span> <span data-ttu-id="76e3e-121">Caso você queira definir uma política Diária, de definir o sinalizador "agenda diária habilitado" como verdadeiro e atribuir valores apropriados para outros parâmetros de objeto.</span><span class="sxs-lookup"><span data-stu-id="76e3e-121">In case you want to set a Daily policy, set the "daily schedule enabled" flag to true and assign appropriate values for other object parameters.</span></span>
3.  <span data-ttu-id="76e3e-122">Obter a política de proteção de backup que você deseja modificar e armazená-la em uma variável.</span><span class="sxs-lookup"><span data-stu-id="76e3e-122">Get the backup protection policy that you want to modify and store it in a variable.</span></span> <span data-ttu-id="76e3e-123">No exemplo acima, recuperamos a política de backup com o nome "TestPolicy" que queríamos modificar.</span><span class="sxs-lookup"><span data-stu-id="76e3e-123">In the above example, we retrieved the backup policy with the name "TestPolicy" that we wanted to modify.</span></span>
4.  <span data-ttu-id="76e3e-124">Modifique a política de proteção de backup recuperada na etapa 3 usando o objeto de política de agendamento modificado e o objeto de política de retenção.</span><span class="sxs-lookup"><span data-stu-id="76e3e-124">Modify the backup protection policy retrieved in step 3 using the modified schedule policy object and retention policy object.</span></span>

## <span data-ttu-id="76e3e-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76e3e-125">PARAMETERS</span></span>

### <span data-ttu-id="76e3e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76e3e-126">-DefaultProfile</span></span>
<span data-ttu-id="76e3e-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="76e3e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76e3e-128">-FixForInconsistentItems</span><span class="sxs-lookup"><span data-stu-id="76e3e-128">-FixForInconsistentItems</span></span>
<span data-ttu-id="76e3e-129">Alternar Parâmetro indicando se você deve ou não tentar novamente a Atualização de Política para itens com falha.</span><span class="sxs-lookup"><span data-stu-id="76e3e-129">Switch Parameter indicating whether or not to retry Policy Update for failed items.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FixPolicyParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e3e-130">-Política</span><span class="sxs-lookup"><span data-stu-id="76e3e-130">-Policy</span></span>
<span data-ttu-id="76e3e-131">Especifica a política de proteção de backup que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="76e3e-131">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="76e3e-132">Para obter um **objeto BackupProtectionPolicy,** use o cmdlet Get-AzRecoveryServicesBackupProtectionPolicy backup.</span><span class="sxs-lookup"><span data-stu-id="76e3e-132">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="76e3e-133">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="76e3e-133">-RetentionPolicy</span></span>
<span data-ttu-id="76e3e-134">Especifica a política de retenção base.</span><span class="sxs-lookup"><span data-stu-id="76e3e-134">Specifies the base retention policy.</span></span>
<span data-ttu-id="76e3e-135">Para obter um **objeto RetentionPolicy,** use o cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject retenção.</span><span class="sxs-lookup"><span data-stu-id="76e3e-135">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: ModifyPolicyParamSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e3e-136">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="76e3e-136">-SchedulePolicy</span></span>
<span data-ttu-id="76e3e-137">Especifica o objeto de política de agendamento base.</span><span class="sxs-lookup"><span data-stu-id="76e3e-137">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="76e3e-138">Para obter um **objeto SchedulePolicy,** use o objeto Get-AzRecoveryServicesBackupSchedulePolicyObject dados.</span><span class="sxs-lookup"><span data-stu-id="76e3e-138">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: ModifyPolicyParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76e3e-139">-VaultId</span><span class="sxs-lookup"><span data-stu-id="76e3e-139">-VaultId</span></span>
<span data-ttu-id="76e3e-140">ID arm do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="76e3e-140">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="76e3e-141">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="76e3e-141">-Confirm</span></span>
<span data-ttu-id="76e3e-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76e3e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76e3e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76e3e-143">-WhatIf</span></span>
<span data-ttu-id="76e3e-144">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="76e3e-144">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="76e3e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76e3e-145">CommonParameters</span></span>
<span data-ttu-id="76e3e-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76e3e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76e3e-147">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76e3e-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76e3e-148">Entradas</span><span class="sxs-lookup"><span data-stu-id="76e3e-148">INPUTS</span></span>

### <span data-ttu-id="76e3e-149">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="76e3e-149">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="76e3e-150">System.String</span><span class="sxs-lookup"><span data-stu-id="76e3e-150">System.String</span></span>

## <span data-ttu-id="76e3e-151">Saídas</span><span class="sxs-lookup"><span data-stu-id="76e3e-151">OUTPUTS</span></span>

### <span data-ttu-id="76e3e-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="76e3e-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="76e3e-153">Notas</span><span class="sxs-lookup"><span data-stu-id="76e3e-153">NOTES</span></span>

## <span data-ttu-id="76e3e-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76e3e-154">RELATED LINKS</span></span>

[<span data-ttu-id="76e3e-155">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="76e3e-155">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="76e3e-156">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="76e3e-156">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="76e3e-157">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="76e3e-157">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="76e3e-158">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="76e3e-158">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


