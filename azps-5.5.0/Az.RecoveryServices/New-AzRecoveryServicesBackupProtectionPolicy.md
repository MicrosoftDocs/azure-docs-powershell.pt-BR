---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 0a60e3bd7f07f69687766b95eb3d56be3ef1d56f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114041"
---
# <span data-ttu-id="6538b-101">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6538b-101">New-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="6538b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6538b-102">SYNOPSIS</span></span>
<span data-ttu-id="6538b-103">Cria uma política de proteção de backup.</span><span class="sxs-lookup"><span data-stu-id="6538b-103">Creates a Backup protection policy.</span></span>

## <span data-ttu-id="6538b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6538b-104">SYNTAX</span></span>

```
New-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6538b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6538b-105">DESCRIPTION</span></span>
<span data-ttu-id="6538b-106">O **cmdlet New-AzRecoveryServicesBackupProtectionPolicy** cria uma política de proteção de backup em um cofre.</span><span class="sxs-lookup"><span data-stu-id="6538b-106">The **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="6538b-107">Uma política de proteção está associada a pelo menos uma política de retenção.</span><span class="sxs-lookup"><span data-stu-id="6538b-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="6538b-108">A política de retenção define por quanto tempo um ponto de recuperação é mantido com o Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="6538b-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>
<span data-ttu-id="6538b-109">Você pode usar o cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject para obter a política de retenção padrão.</span><span class="sxs-lookup"><span data-stu-id="6538b-109">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="6538b-110">E você pode usar o cmdlet Get-AzRecoveryServicesBackupSchedulePolicyObject para obter a política de agendamento padrão.</span><span class="sxs-lookup"><span data-stu-id="6538b-110">And you can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="6538b-111">Os **objetos SchedulePolicy** e **RetentionPolicy** são usados como entradas para o cmdlet **New-AzRecoveryServicesBackupProtectionPolicy.**</span><span class="sxs-lookup"><span data-stu-id="6538b-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="6538b-112">De definir o contexto do cofre usando o Set-AzRecoveryServicesVaultContext cmdlet antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="6538b-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="6538b-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6538b-113">EXAMPLES</span></span>

### <span data-ttu-id="6538b-114">Exemplo 1: Criar uma política de proteção de backup</span><span class="sxs-lookup"><span data-stu-id="6538b-114">Example 1: Create a Backup protection policy</span></span>
```powershell
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="6538b-115">O primeiro comando obtém um **SchedulePolicyObject** base e o armazena na variável $SchPol dados.</span><span class="sxs-lookup"><span data-stu-id="6538b-115">The first command gets a base **SchedulePolicyObject**, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="6538b-116">O segundo comando remove todos os tempos de executar agendados da política de agendamento $SchPol.</span><span class="sxs-lookup"><span data-stu-id="6538b-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="6538b-117">O terceiro comando usa o Get-Date cmdlet para obter a data e a hora atuais.</span><span class="sxs-lookup"><span data-stu-id="6538b-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>
<span data-ttu-id="6538b-118">O quarto comando adiciona a data e a hora atuais $Dt como o tempo de executar agendado à política de agendamento.</span><span class="sxs-lookup"><span data-stu-id="6538b-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>
<span data-ttu-id="6538b-119">O quinto comando obtém um objeto **Base RetentionPolicy** e o armazena na variável $RetPol dados.</span><span class="sxs-lookup"><span data-stu-id="6538b-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="6538b-120">O sexto comando define a política de duração de retenção para 365 dias.</span><span class="sxs-lookup"><span data-stu-id="6538b-120">The sixth command sets the retention duration policy to 365 days.</span></span>
<span data-ttu-id="6538b-121">O comando final cria um **objeto BackupProtectionPolicy** com base nas políticas de agendamento e retenção criadas pelos comandos anteriores.</span><span class="sxs-lookup"><span data-stu-id="6538b-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

### <span data-ttu-id="6538b-122">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6538b-122">Example 2</span></span>

<span data-ttu-id="6538b-123">Cria uma política de proteção de backup.</span><span class="sxs-lookup"><span data-stu-id="6538b-123">Creates a Backup protection policy.</span></span> <span data-ttu-id="6538b-124">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="6538b-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzRecoveryServicesBackupProtectionPolicy -Name 'NewPolicy' -RetentionPolicy $RetPol -SchedulePolicy $SchPol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="6538b-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6538b-125">PARAMETERS</span></span>

### <span data-ttu-id="6538b-126">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="6538b-126">-BackupManagementType</span></span>
<span data-ttu-id="6538b-127">A classe de recursos que está sendo protegida.</span><span class="sxs-lookup"><span data-stu-id="6538b-127">The class of resources being protected.</span></span> <span data-ttu-id="6538b-128">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6538b-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6538b-129">AzureVM</span><span class="sxs-lookup"><span data-stu-id="6538b-129">AzureVM</span></span> 
- <span data-ttu-id="6538b-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="6538b-130">AzureStorage</span></span>
- <span data-ttu-id="6538b-131">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="6538b-131">AzureWorkload</span></span>

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

### <span data-ttu-id="6538b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6538b-132">-DefaultProfile</span></span>
<span data-ttu-id="6538b-133">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6538b-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6538b-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="6538b-134">-Name</span></span>
<span data-ttu-id="6538b-135">Especifica o nome da política.</span><span class="sxs-lookup"><span data-stu-id="6538b-135">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="6538b-136">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6538b-136">-RetentionPolicy</span></span>
<span data-ttu-id="6538b-137">Especifica o objeto **Base RetentionPolicy.**</span><span class="sxs-lookup"><span data-stu-id="6538b-137">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="6538b-138">Você pode usar o cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject para obter um objeto **RetentionPolicy.**</span><span class="sxs-lookup"><span data-stu-id="6538b-138">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

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

### <span data-ttu-id="6538b-139">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="6538b-139">-SchedulePolicy</span></span>
<span data-ttu-id="6538b-140">Especifica o objeto **base SchedulePolicy.**</span><span class="sxs-lookup"><span data-stu-id="6538b-140">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="6538b-141">Você pode usar o cmdlet Get-AzRecoveryServicesBackupSchedulePolicyObject para obter um **objeto SchedulePolicy.**</span><span class="sxs-lookup"><span data-stu-id="6538b-141">You can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

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

### <span data-ttu-id="6538b-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6538b-142">-VaultId</span></span>
<span data-ttu-id="6538b-143">ID arm do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="6538b-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6538b-144">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="6538b-144">-WorkloadType</span></span>
<span data-ttu-id="6538b-145">Tipo de carga de trabalho do recurso.</span><span class="sxs-lookup"><span data-stu-id="6538b-145">Workload type of the resource.</span></span> <span data-ttu-id="6538b-146">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6538b-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6538b-147">AzureVM</span><span class="sxs-lookup"><span data-stu-id="6538b-147">AzureVM</span></span> 
- <span data-ttu-id="6538b-148">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="6538b-148">AzureFiles</span></span>
- <span data-ttu-id="6538b-149">Mssql</span><span class="sxs-lookup"><span data-stu-id="6538b-149">MSSQL</span></span>

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

### <span data-ttu-id="6538b-150">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6538b-150">-Confirm</span></span>
<span data-ttu-id="6538b-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6538b-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6538b-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6538b-152">-WhatIf</span></span>
<span data-ttu-id="6538b-153">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6538b-153">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="6538b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6538b-154">CommonParameters</span></span>
<span data-ttu-id="6538b-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6538b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6538b-156">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6538b-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6538b-157">Entradas</span><span class="sxs-lookup"><span data-stu-id="6538b-157">INPUTS</span></span>

### <span data-ttu-id="6538b-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span><span class="sxs-lookup"><span data-stu-id="6538b-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span></span>

### <span data-ttu-id="6538b-159">System.Nullable'1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0,0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="6538b-159">System.Nullable\`1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6538b-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="6538b-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

### <span data-ttu-id="6538b-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="6538b-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

### <span data-ttu-id="6538b-162">System.String</span><span class="sxs-lookup"><span data-stu-id="6538b-162">System.String</span></span>

## <span data-ttu-id="6538b-163">Saídas</span><span class="sxs-lookup"><span data-stu-id="6538b-163">OUTPUTS</span></span>

### <span data-ttu-id="6538b-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="6538b-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="6538b-165">Notas</span><span class="sxs-lookup"><span data-stu-id="6538b-165">NOTES</span></span>

## <span data-ttu-id="6538b-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6538b-166">RELATED LINKS</span></span>

[<span data-ttu-id="6538b-167">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="6538b-167">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="6538b-168">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6538b-168">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="6538b-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="6538b-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="6538b-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="6538b-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="6538b-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6538b-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="6538b-172">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6538b-172">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


