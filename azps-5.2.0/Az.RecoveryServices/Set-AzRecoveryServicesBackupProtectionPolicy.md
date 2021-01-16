---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: e9f89a39b283f073c0fe826f22157570be29e74b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262253"
---
# <span data-ttu-id="9b05c-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9b05c-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="9b05c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b05c-102">SYNOPSIS</span></span>
<span data-ttu-id="9b05c-103">Modifica uma política de proteção de backup.</span><span class="sxs-lookup"><span data-stu-id="9b05c-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="9b05c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b05c-104">SYNTAX</span></span>

### <span data-ttu-id="9b05c-105">ModifyPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="9b05c-105">ModifyPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b05c-106">FixPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="9b05c-106">FixPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-FixForInconsistentItems]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b05c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9b05c-107">DESCRIPTION</span></span>
<span data-ttu-id="9b05c-108">O cmdlet **set-AzRecoveryServicesBackupProtectionPolicy** modifica uma política de proteção de backup do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="9b05c-108">The **Set-AzRecoveryServicesBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="9b05c-109">Você pode modificar o agendamento de backup e os componentes da política de retenção.</span><span class="sxs-lookup"><span data-stu-id="9b05c-109">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="9b05c-110">Todas as alterações feitas afetam o backup e a retenção dos itens associados à política.</span><span class="sxs-lookup"><span data-stu-id="9b05c-110">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="9b05c-111">Defina o contexto do cofre usando o cmdlet Set-AzRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="9b05c-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="9b05c-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b05c-112">EXAMPLES</span></span>

### <span data-ttu-id="9b05c-113">Exemplo 1: modificar uma política de proteção de backup</span><span class="sxs-lookup"><span data-stu-id="9b05c-113">Example 1: Modify a Backup protection policy</span></span>
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

<span data-ttu-id="9b05c-114">Aqui está a descrição de alto nível das etapas a serem seguidas para modificar uma política de proteção:</span><span class="sxs-lookup"><span data-stu-id="9b05c-114">Here is the high-level description of the steps to be followed for modifying a protection policy:</span></span> 
1.  <span data-ttu-id="9b05c-115">Obtenha uma base de SchedulePolicyObject e base de RetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="9b05c-115">Get a base SchedulePolicyObject and base RetentionPolicyObject.</span></span> <span data-ttu-id="9b05c-116">Armazene-os em alguma variável.</span><span class="sxs-lookup"><span data-stu-id="9b05c-116">Store them in some variable.</span></span>
2.  <span data-ttu-id="9b05c-117">Defina os diferentes parâmetros de objeto de política de retenção e agendamento de acordo com sua necessidade.</span><span class="sxs-lookup"><span data-stu-id="9b05c-117">Set the different parameters of schedule and retention policy object as per your requirement.</span></span> <span data-ttu-id="9b05c-118">Por exemplo, no script de exemplo acima, estamos tentando definir uma política de proteção semanal.</span><span class="sxs-lookup"><span data-stu-id="9b05c-118">For example- In the above sample script, we are trying to set a weekly protection policy.</span></span> <span data-ttu-id="9b05c-119">Portanto, alteramos a frequência de agendamento para "semanal" e também atualizamos o tempo de execução do cronograma.</span><span class="sxs-lookup"><span data-stu-id="9b05c-119">Hence, we changed the schedule frequency to "Weekly" and also updated the schedule run time.</span></span> <span data-ttu-id="9b05c-120">No objeto da política de retenção, atualizamos a duração da retenção semanal e definimos o sinalizador "cronograma semanal habilitado" correto.</span><span class="sxs-lookup"><span data-stu-id="9b05c-120">In the retention policy object, we updated the weekly retention duration and set the correct "weekly schedule enabled" flag.</span></span> <span data-ttu-id="9b05c-121">Caso você queira definir uma política diária, defina o sinalizador "agenda diária habilitada" como verdadeiro e atribua os valores apropriados para outros parâmetros do objeto.</span><span class="sxs-lookup"><span data-stu-id="9b05c-121">In case you want to set a Daily policy, set the "daily schedule enabled" flag to true and assign appropriate values for other object parameters.</span></span>
3.  <span data-ttu-id="9b05c-122">Obtenha a política de proteção de backup que você deseja modificar e armazene-a em uma variável.</span><span class="sxs-lookup"><span data-stu-id="9b05c-122">Get the backup protection policy that you want to modify and store it in a variable.</span></span> <span data-ttu-id="9b05c-123">No exemplo acima, recuperamos a política de backup com o nome "TestPolicy" que queremos modificar.</span><span class="sxs-lookup"><span data-stu-id="9b05c-123">In the above example, we retrieved the backup policy with the name "TestPolicy" that we wanted to modify.</span></span>
4.  <span data-ttu-id="9b05c-124">Modifique a política de proteção de backup recuperada na etapa 3 usando o objeto de política de agendamento modificado e o objeto da política de retenção.</span><span class="sxs-lookup"><span data-stu-id="9b05c-124">Modify the backup protection policy retrieved in step 3 using the modified schedule policy object and retention policy object.</span></span>

## <span data-ttu-id="9b05c-125">OS</span><span class="sxs-lookup"><span data-stu-id="9b05c-125">PARAMETERS</span></span>

### <span data-ttu-id="9b05c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b05c-126">-DefaultProfile</span></span>
<span data-ttu-id="9b05c-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b05c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b05c-128">-FixForInconsistentItems</span><span class="sxs-lookup"><span data-stu-id="9b05c-128">-FixForInconsistentItems</span></span>
<span data-ttu-id="9b05c-129">Parâmetro de opção que indica se a atualização de política para itens com falha deve ou não ser repetida.</span><span class="sxs-lookup"><span data-stu-id="9b05c-129">Switch Parameter indicating whether or not to retry Policy Update for failed items.</span></span>

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

### <span data-ttu-id="9b05c-130">-Política</span><span class="sxs-lookup"><span data-stu-id="9b05c-130">-Policy</span></span>
<span data-ttu-id="9b05c-131">Especifica a política de proteção de backup que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="9b05c-131">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="9b05c-132">Para obter um objeto **BackupProtectionPolicy** , use o cmdlet Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="9b05c-132">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="9b05c-133">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="9b05c-133">-RetentionPolicy</span></span>
<span data-ttu-id="9b05c-134">Especifica a política de retenção básica.</span><span class="sxs-lookup"><span data-stu-id="9b05c-134">Specifies the base retention policy.</span></span>
<span data-ttu-id="9b05c-135">Para obter um objeto **RetentionPolicy** , use o cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="9b05c-135">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

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

### <span data-ttu-id="9b05c-136">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="9b05c-136">-SchedulePolicy</span></span>
<span data-ttu-id="9b05c-137">Especifica o objeto da política de cronograma básico.</span><span class="sxs-lookup"><span data-stu-id="9b05c-137">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="9b05c-138">Para obter um objeto **SchedulePolicy** , use o objeto Get-AzRecoveryServicesBackupSchedulePolicyObject.</span><span class="sxs-lookup"><span data-stu-id="9b05c-138">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

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

### <span data-ttu-id="9b05c-139">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="9b05c-139">-VaultId</span></span>
<span data-ttu-id="9b05c-140">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="9b05c-140">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="9b05c-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9b05c-141">-Confirm</span></span>
<span data-ttu-id="9b05c-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b05c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b05c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b05c-143">-WhatIf</span></span>
<span data-ttu-id="9b05c-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9b05c-144">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="9b05c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b05c-145">CommonParameters</span></span>
<span data-ttu-id="9b05c-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b05c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b05c-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b05c-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b05c-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9b05c-148">INPUTS</span></span>

### <span data-ttu-id="9b05c-149">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="9b05c-149">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="9b05c-150">System. String</span><span class="sxs-lookup"><span data-stu-id="9b05c-150">System.String</span></span>

## <span data-ttu-id="9b05c-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9b05c-151">OUTPUTS</span></span>

### <span data-ttu-id="9b05c-152">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="9b05c-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="9b05c-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9b05c-153">NOTES</span></span>

## <span data-ttu-id="9b05c-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b05c-154">RELATED LINKS</span></span>

[<span data-ttu-id="9b05c-155">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9b05c-155">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="9b05c-156">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="9b05c-156">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="9b05c-157">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9b05c-157">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="9b05c-158">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9b05c-158">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


