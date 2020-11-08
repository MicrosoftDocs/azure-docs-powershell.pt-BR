---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: f9cd7064c1949639526f2e7b84f01fb6355b584f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115702"
---
# <span data-ttu-id="db070-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="db070-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="db070-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db070-102">SYNOPSIS</span></span>
<span data-ttu-id="db070-103">Modifica uma política de proteção de backup.</span><span class="sxs-lookup"><span data-stu-id="db070-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="db070-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db070-104">SYNTAX</span></span>

### <span data-ttu-id="db070-105">ModifyPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="db070-105">ModifyPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db070-106">FixPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="db070-106">FixPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-FixForInconsistentItems]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db070-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db070-107">DESCRIPTION</span></span>
<span data-ttu-id="db070-108">O cmdlet **set-AzRecoveryServicesBackupProtectionPolicy** modifica uma política de proteção de backup do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="db070-108">The **Set-AzRecoveryServicesBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="db070-109">Você pode modificar o agendamento de backup e os componentes da política de retenção.</span><span class="sxs-lookup"><span data-stu-id="db070-109">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="db070-110">Todas as alterações feitas afetam o backup e a retenção dos itens associados à política.</span><span class="sxs-lookup"><span data-stu-id="db070-110">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="db070-111">Defina o contexto do cofre usando o cmdlet Set-AzRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="db070-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="db070-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db070-112">EXAMPLES</span></span>

### <span data-ttu-id="db070-113">Exemplo 1: modificar uma política de proteção de backup</span><span class="sxs-lookup"><span data-stu-id="db070-113">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> $Pol.AzureBackupRGName = "RG_prefix"
PS C:\> $Pol.AzureBackupRGNameSuffix = "RG_suffix"
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="db070-114">O primeiro comando obtém um objeto SchedulePolicy base e, em seguida, armazena-o na variável $SchPol.</span><span class="sxs-lookup"><span data-stu-id="db070-114">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="db070-115">O segundo comando Remove todos os horários de execução agendados da política de agendamento em $SchPol.</span><span class="sxs-lookup"><span data-stu-id="db070-115">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="db070-116">O terceiro comando usa o cmdlet Get-Date para obter a data e hora atuais e, em seguida, armazena-o na variável $DT.</span><span class="sxs-lookup"><span data-stu-id="db070-116">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="db070-117">O quarto comando adiciona a data e a hora no $DT ao tempo de execução do cronograma para a política de agendamento.</span><span class="sxs-lookup"><span data-stu-id="db070-117">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>
<span data-ttu-id="db070-118">O quinto comando obtém um objeto de política de retenção base e, em seguida, armazena-o na variável $RetPol.</span><span class="sxs-lookup"><span data-stu-id="db070-118">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="db070-119">O sexto comando define a duração da retenção para 365 dias.</span><span class="sxs-lookup"><span data-stu-id="db070-119">The sixth command sets the retention duration to 365 days.</span></span>
<span data-ttu-id="db070-120">O sétimo comando obtém a política de proteção de backup chamada NewPolicy e a armazena na variável $Pol.</span><span class="sxs-lookup"><span data-stu-id="db070-120">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="db070-121">O oitavo e nono define os parâmetros do grupo de recursos associados à política que armazena os pontos de restauração.</span><span class="sxs-lookup"><span data-stu-id="db070-121">The eighth and ninth sets the resource group parameters associated with policy which stores the restore points.</span></span>
<span data-ttu-id="db070-122">O comando final modifica a política de proteção de backup no $Pol usando a política de agendamento em $SchPol e a política de retenção em $RetPol.</span><span class="sxs-lookup"><span data-stu-id="db070-122">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="db070-123">OS</span><span class="sxs-lookup"><span data-stu-id="db070-123">PARAMETERS</span></span>

### <span data-ttu-id="db070-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db070-124">-DefaultProfile</span></span>
<span data-ttu-id="db070-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db070-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db070-126">-FixForInconsistentItems</span><span class="sxs-lookup"><span data-stu-id="db070-126">-FixForInconsistentItems</span></span>
<span data-ttu-id="db070-127">Parâmetro de opção que indica se a atualização de política para itens com falha deve ou não ser repetida.</span><span class="sxs-lookup"><span data-stu-id="db070-127">Switch Parameter indicating whether or not to retry Policy Update for failed items.</span></span>

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

### <span data-ttu-id="db070-128">-Política</span><span class="sxs-lookup"><span data-stu-id="db070-128">-Policy</span></span>
<span data-ttu-id="db070-129">Especifica a política de proteção de backup que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="db070-129">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="db070-130">Para obter um objeto **BackupProtectionPolicy** , use o cmdlet Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="db070-130">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="db070-131">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="db070-131">-RetentionPolicy</span></span>
<span data-ttu-id="db070-132">Especifica a política de retenção básica.</span><span class="sxs-lookup"><span data-stu-id="db070-132">Specifies the base retention policy.</span></span>
<span data-ttu-id="db070-133">Para obter um objeto **RetentionPolicy** , use o cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="db070-133">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

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

### <span data-ttu-id="db070-134">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="db070-134">-SchedulePolicy</span></span>
<span data-ttu-id="db070-135">Especifica o objeto da política de cronograma básico.</span><span class="sxs-lookup"><span data-stu-id="db070-135">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="db070-136">Para obter um objeto **SchedulePolicy** , use o objeto Get-AzRecoveryServicesBackupSchedulePolicyObject.</span><span class="sxs-lookup"><span data-stu-id="db070-136">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

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

### <span data-ttu-id="db070-137">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="db070-137">-VaultId</span></span>
<span data-ttu-id="db070-138">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="db070-138">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="db070-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="db070-139">-Confirm</span></span>
<span data-ttu-id="db070-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db070-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db070-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db070-141">-WhatIf</span></span>
<span data-ttu-id="db070-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="db070-142">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="db070-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db070-143">CommonParameters</span></span>
<span data-ttu-id="db070-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db070-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db070-145">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db070-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db070-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db070-146">INPUTS</span></span>

### <span data-ttu-id="db070-147">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="db070-147">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="db070-148">System. String</span><span class="sxs-lookup"><span data-stu-id="db070-148">System.String</span></span>

## <span data-ttu-id="db070-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db070-149">OUTPUTS</span></span>

### <span data-ttu-id="db070-150">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="db070-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="db070-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db070-151">NOTES</span></span>

## <span data-ttu-id="db070-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db070-152">RELATED LINKS</span></span>

[<span data-ttu-id="db070-153">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="db070-153">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="db070-154">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="db070-154">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="db070-155">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="db070-155">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="db070-156">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="db070-156">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


