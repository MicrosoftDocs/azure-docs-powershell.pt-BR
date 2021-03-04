---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 65bda3a4829971ce3d073c672b578099130fae6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885550"
---
# <span data-ttu-id="42724-101">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="42724-101">New-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="42724-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42724-102">SYNOPSIS</span></span>
<span data-ttu-id="42724-103">Cria uma política de proteção de backup.</span><span class="sxs-lookup"><span data-stu-id="42724-103">Creates a Backup protection policy.</span></span>

## <span data-ttu-id="42724-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="42724-104">SYNTAX</span></span>

```
New-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42724-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="42724-105">DESCRIPTION</span></span>
<span data-ttu-id="42724-106">O cmdlet **New-AzRecoveryServicesBackupProtectionPolicy** cria uma política de proteção de backup em um cofre.</span><span class="sxs-lookup"><span data-stu-id="42724-106">The **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="42724-107">Uma política de proteção está associada a pelo menos uma política de retenção.</span><span class="sxs-lookup"><span data-stu-id="42724-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="42724-108">A política de retenção define por quanto tempo um ponto de recuperação é mantido com o Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="42724-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>
<span data-ttu-id="42724-109">Você pode usar o cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject para obter a política de retenção padrão.</span><span class="sxs-lookup"><span data-stu-id="42724-109">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="42724-110">E você pode usar o cmdlet Get-AzRecoveryServicesBackupSchedulePolicyObject para obter a política de agendamento padrão.</span><span class="sxs-lookup"><span data-stu-id="42724-110">And you can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="42724-111">Os **objetos SchedulePolicy** e **RetentionPolicy** são usados como entradas para o cmdlet **New-AzRecoveryServicesBackupProtectionPolicy.**</span><span class="sxs-lookup"><span data-stu-id="42724-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="42724-112">De definir o contexto do cofre usando o cmdlet Set-AzRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="42724-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="42724-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="42724-113">EXAMPLES</span></span>

### <span data-ttu-id="42724-114">Exemplo 1: Criar uma política de proteção de backup</span><span class="sxs-lookup"><span data-stu-id="42724-114">Example 1: Create a Backup protection policy</span></span>
```powershell
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="42724-115">O primeiro comando obtém um **SchedulePolicyObject** base e o armazena na variável $SchPol base.</span><span class="sxs-lookup"><span data-stu-id="42724-115">The first command gets a base **SchedulePolicyObject**, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="42724-116">O segundo comando remove todos os horários de executar agendados da política de agendamento $SchPol.</span><span class="sxs-lookup"><span data-stu-id="42724-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="42724-117">O terceiro comando usa o cmdlet Get-Date para obter a data e a hora atuais.</span><span class="sxs-lookup"><span data-stu-id="42724-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>
<span data-ttu-id="42724-118">O quarto comando adiciona a data e a hora atuais $Dt como o tempo de executar agendado à política de agendamento.</span><span class="sxs-lookup"><span data-stu-id="42724-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>
<span data-ttu-id="42724-119">O quinto comando obtém um **objeto RetentionPolicy** base e o armazena na variável $RetPol base.</span><span class="sxs-lookup"><span data-stu-id="42724-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="42724-120">O sexto comando define a política de duração de retenção como 365 dias.</span><span class="sxs-lookup"><span data-stu-id="42724-120">The sixth command sets the retention duration policy to 365 days.</span></span>
<span data-ttu-id="42724-121">O comando final cria um **objeto BackupProtectionPolicy** com base na agenda e nas políticas de retenção criadas pelos comandos anteriores.</span><span class="sxs-lookup"><span data-stu-id="42724-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

### <span data-ttu-id="42724-122">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="42724-122">Example 2</span></span>

<span data-ttu-id="42724-123">Cria uma política de proteção de backup.</span><span class="sxs-lookup"><span data-stu-id="42724-123">Creates a Backup protection policy.</span></span> <span data-ttu-id="42724-124">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="42724-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzRecoveryServicesBackupProtectionPolicy -Name 'NewPolicy' -RetentionPolicy $RetPol -SchedulePolicy $SchPol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="42724-125">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="42724-125">PARAMETERS</span></span>

### <span data-ttu-id="42724-126">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="42724-126">-BackupManagementType</span></span>
<span data-ttu-id="42724-127">A classe de recursos que está sendo protegida.</span><span class="sxs-lookup"><span data-stu-id="42724-127">The class of resources being protected.</span></span> <span data-ttu-id="42724-128">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="42724-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42724-129">AzureVM</span><span class="sxs-lookup"><span data-stu-id="42724-129">AzureVM</span></span> 
- <span data-ttu-id="42724-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="42724-130">AzureStorage</span></span>
- <span data-ttu-id="42724-131">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="42724-131">AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42724-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42724-132">-DefaultProfile</span></span>
<span data-ttu-id="42724-133">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="42724-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42724-134">-Name</span><span class="sxs-lookup"><span data-stu-id="42724-134">-Name</span></span>
<span data-ttu-id="42724-135">Especifica o nome da política.</span><span class="sxs-lookup"><span data-stu-id="42724-135">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="42724-136">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="42724-136">-RetentionPolicy</span></span>
<span data-ttu-id="42724-137">Especifica o objeto **RetentionPolicy** base.</span><span class="sxs-lookup"><span data-stu-id="42724-137">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="42724-138">Você pode usar o cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject para obter um **objeto RetentionPolicy.**</span><span class="sxs-lookup"><span data-stu-id="42724-138">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

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

### <span data-ttu-id="42724-139">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="42724-139">-SchedulePolicy</span></span>
<span data-ttu-id="42724-140">Especifica o objeto **SchedulePolicy** base.</span><span class="sxs-lookup"><span data-stu-id="42724-140">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="42724-141">Você pode usar o cmdlet Get-AzRecoveryServicesBackupSchedulePolicyObject para obter um **objeto SchedulePolicy.**</span><span class="sxs-lookup"><span data-stu-id="42724-141">You can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

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

### <span data-ttu-id="42724-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="42724-142">-VaultId</span></span>
<span data-ttu-id="42724-143">ARM ID do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="42724-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="42724-144">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="42724-144">-WorkloadType</span></span>
<span data-ttu-id="42724-145">Tipo de carga de trabalho do recurso.</span><span class="sxs-lookup"><span data-stu-id="42724-145">Workload type of the resource.</span></span> <span data-ttu-id="42724-146">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="42724-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42724-147">AzureVM</span><span class="sxs-lookup"><span data-stu-id="42724-147">AzureVM</span></span> 
- <span data-ttu-id="42724-148">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="42724-148">AzureFiles</span></span>
- <span data-ttu-id="42724-149">MSSQL</span><span class="sxs-lookup"><span data-stu-id="42724-149">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42724-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42724-150">-Confirm</span></span>
<span data-ttu-id="42724-151">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42724-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42724-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42724-152">-WhatIf</span></span>
<span data-ttu-id="42724-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="42724-153">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="42724-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42724-154">CommonParameters</span></span>
<span data-ttu-id="42724-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42724-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42724-156">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42724-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42724-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="42724-157">INPUTS</span></span>

### <span data-ttu-id="42724-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span><span class="sxs-lookup"><span data-stu-id="42724-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span></span>

### <span data-ttu-id="42724-159">System.Nullable'1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="42724-159">System.Nullable\`1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="42724-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="42724-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

### <span data-ttu-id="42724-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="42724-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

### <span data-ttu-id="42724-162">System.String</span><span class="sxs-lookup"><span data-stu-id="42724-162">System.String</span></span>

## <span data-ttu-id="42724-163">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="42724-163">OUTPUTS</span></span>

### <span data-ttu-id="42724-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="42724-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="42724-165">NOTES</span><span class="sxs-lookup"><span data-stu-id="42724-165">NOTES</span></span>

## <span data-ttu-id="42724-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42724-166">RELATED LINKS</span></span>

[<span data-ttu-id="42724-167">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="42724-167">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="42724-168">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="42724-168">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="42724-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="42724-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="42724-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="42724-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="42724-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="42724-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="42724-172">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="42724-172">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


