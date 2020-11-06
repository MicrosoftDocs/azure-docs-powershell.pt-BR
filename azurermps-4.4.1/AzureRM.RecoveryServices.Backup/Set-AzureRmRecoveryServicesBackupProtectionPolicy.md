---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: f17ce0a23c2b91cd00f2a12bb2451c4e235169ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440580"
---
# <span data-ttu-id="bbc51-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="bbc51-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="bbc51-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bbc51-102">SYNOPSIS</span></span>
<span data-ttu-id="bbc51-103">Modifica uma política de proteção de backup.</span><span class="sxs-lookup"><span data-stu-id="bbc51-103">Modifies a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbc51-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bbc51-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase>
 [[-RetentionPolicy] <RetentionPolicyBase>] [[-SchedulePolicy] <SchedulePolicyBase>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbc51-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bbc51-105">DESCRIPTION</span></span>
<span data-ttu-id="bbc51-106">O cmdlet **set-AzureRmBackupProtectionPolicy** modifica uma política de proteção de backup do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="bbc51-106">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="bbc51-107">Você pode modificar o agendamento de backup e os componentes da política de retenção.</span><span class="sxs-lookup"><span data-stu-id="bbc51-107">You can modify the Backup schedule and retention policy components.</span></span>

<span data-ttu-id="bbc51-108">Todas as alterações feitas afetam o backup e a retenção dos itens associados à política.</span><span class="sxs-lookup"><span data-stu-id="bbc51-108">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>

<span data-ttu-id="bbc51-109">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="bbc51-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="bbc51-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bbc51-110">EXAMPLES</span></span>

### <span data-ttu-id="bbc51-111">Exemplo 1: modificar uma política de proteção de backup</span><span class="sxs-lookup"><span data-stu-id="bbc51-111">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="bbc51-112">O primeiro comando obtém um objeto SchedulePolicy base e, em seguida, armazena-o na variável $SchPol.</span><span class="sxs-lookup"><span data-stu-id="bbc51-112">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="bbc51-113">O segundo comando Remove todos os horários de execução agendados da política de agendamento em $SchPol.</span><span class="sxs-lookup"><span data-stu-id="bbc51-113">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>

<span data-ttu-id="bbc51-114">O terceiro comando usa o cmdlet Get-Date para obter a data e hora atuais e, em seguida, armazena-o na variável $DT.</span><span class="sxs-lookup"><span data-stu-id="bbc51-114">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>

<span data-ttu-id="bbc51-115">O quarto comando adiciona a data e a hora no $DT ao tempo de execução do cronograma para a política de agendamento.</span><span class="sxs-lookup"><span data-stu-id="bbc51-115">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>

<span data-ttu-id="bbc51-116">O quinto comando obtém um objeto de política de retenção base e, em seguida, armazena-o na variável $RetPol.</span><span class="sxs-lookup"><span data-stu-id="bbc51-116">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="bbc51-117">O sexto comando define a duração da retenção para 365 dias.</span><span class="sxs-lookup"><span data-stu-id="bbc51-117">The sixth command sets the retention duration to 365 days.</span></span>

<span data-ttu-id="bbc51-118">O sétimo comando obtém a política de proteção de backup chamada NewPolicy e a armazena na variável $Pol.</span><span class="sxs-lookup"><span data-stu-id="bbc51-118">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="bbc51-119">O comando final modifica a política de proteção de backup no $Pol usando a política de agendamento em $SchPol e a política de retenção em $RetPol.</span><span class="sxs-lookup"><span data-stu-id="bbc51-119">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="bbc51-120">OS</span><span class="sxs-lookup"><span data-stu-id="bbc51-120">PARAMETERS</span></span>

### <span data-ttu-id="bbc51-121">-Política</span><span class="sxs-lookup"><span data-stu-id="bbc51-121">-Policy</span></span>
<span data-ttu-id="bbc51-122">Especifica a política de proteção de backup que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="bbc51-122">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="bbc51-123">Para obter um objeto **BackupProtectionPolicy** , use o cmdlet Get-AzureRmRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="bbc51-123">To obtain a **BackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="bbc51-124">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bbc51-124">-RetentionPolicy</span></span>
<span data-ttu-id="bbc51-125">Especifica a política de retenção básica.</span><span class="sxs-lookup"><span data-stu-id="bbc51-125">Specifies the base retention policy.</span></span>
<span data-ttu-id="bbc51-126">Para obter um objeto **RetentionPolicy** , use o cmdlet Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="bbc51-126">To obtain a **RetentionPolicy** object, use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

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

### <span data-ttu-id="bbc51-127">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="bbc51-127">-SchedulePolicy</span></span>
<span data-ttu-id="bbc51-128">Especifica o objeto da política de cronograma básico.</span><span class="sxs-lookup"><span data-stu-id="bbc51-128">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="bbc51-129">Para obter um objeto **SchedulePolicy** , use o objeto Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.</span><span class="sxs-lookup"><span data-stu-id="bbc51-129">To obtain a **SchedulePolicy** object, use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject object.</span></span>

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

### <span data-ttu-id="bbc51-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbc51-130">-DefaultProfile</span></span>
<span data-ttu-id="bbc51-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bbc51-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbc51-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbc51-132">CommonParameters</span></span>
<span data-ttu-id="bbc51-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbc51-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbc51-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbc51-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbc51-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bbc51-135">INPUTS</span></span>

### <span data-ttu-id="bbc51-136">PolicyBase</span><span class="sxs-lookup"><span data-stu-id="bbc51-136">PolicyBase</span></span>
<span data-ttu-id="bbc51-137">O parâmetro "política" aceita o valor do tipo "PolicyBase" da pipeline</span><span class="sxs-lookup"><span data-stu-id="bbc51-137">Parameter 'Policy' accepts value of type 'PolicyBase' from the pipeline</span></span>

## <span data-ttu-id="bbc51-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bbc51-138">OUTPUTS</span></span>

### <span data-ttu-id="bbc51-139">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase]</span><span class="sxs-lookup"><span data-stu-id="bbc51-139">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="bbc51-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bbc51-140">NOTES</span></span>

## <span data-ttu-id="bbc51-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bbc51-141">RELATED LINKS</span></span>

[<span data-ttu-id="bbc51-142">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="bbc51-142">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="bbc51-143">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="bbc51-143">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="bbc51-144">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="bbc51-144">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="bbc51-145">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="bbc51-145">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)


