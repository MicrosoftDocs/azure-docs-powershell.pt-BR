---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: caf6394ce84b18bd8e36b4504173fe7f7bb07fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428599"
---
# <span data-ttu-id="6b94d-101">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6b94d-101">Set-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="6b94d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b94d-102">SYNOPSIS</span></span>
<span data-ttu-id="6b94d-103">Modifica uma política de proteção existente.</span><span class="sxs-lookup"><span data-stu-id="6b94d-103">Modifies an existing protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b94d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b94d-104">SYNTAX</span></span>

### <span data-ttu-id="6b94d-105">NoScheduleParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6b94d-105">NoScheduleParamSet (Default)</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b94d-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="6b94d-106">DailyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b94d-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="6b94d-107">WeeklyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b94d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b94d-108">DESCRIPTION</span></span>
<span data-ttu-id="6b94d-109">O cmdlet **set-AzureRmBackupProtectionPolicy** modifica uma política de proteção existente no Azure backup.</span><span class="sxs-lookup"><span data-stu-id="6b94d-109">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing protection policy in Azure Backup.</span></span>
<span data-ttu-id="6b94d-110">Você pode modificar os seguintes componentes da política de proteção:</span><span class="sxs-lookup"><span data-stu-id="6b94d-110">You can modify the following protection policy components:</span></span> 
- <span data-ttu-id="6b94d-111">Sobrenome</span><span class="sxs-lookup"><span data-stu-id="6b94d-111">Name</span></span>
- <span data-ttu-id="6b94d-112">Agendamento de backup</span><span class="sxs-lookup"><span data-stu-id="6b94d-112">Backup schedule</span></span>
- <span data-ttu-id="6b94d-113">Políticas de retenção qualquer alteração pode afetar o backup e a retenção dos itens associados à política.</span><span class="sxs-lookup"><span data-stu-id="6b94d-113">Retention policies Any change might affect the backup and retention of the items associated with the policy.</span></span>

## <span data-ttu-id="6b94d-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b94d-114">EXAMPLES</span></span>

## <span data-ttu-id="6b94d-115">OS</span><span class="sxs-lookup"><span data-stu-id="6b94d-115">PARAMETERS</span></span>

### <span data-ttu-id="6b94d-116">-Backuptime</span><span class="sxs-lookup"><span data-stu-id="6b94d-116">-BackupTime</span></span>
<span data-ttu-id="6b94d-117">Especifica o novo horário de backup do dia, como um objeto **DateTime** , para a política.</span><span class="sxs-lookup"><span data-stu-id="6b94d-117">Specifies the new backup time of day, as a **DateTime** object, for the policy.</span></span>
<span data-ttu-id="6b94d-118">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="6b94d-118">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="6b94d-119">Para obter informações sobre objetos **DateTime** , digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="6b94d-119">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b94d-120">-Diariamente</span><span class="sxs-lookup"><span data-stu-id="6b94d-120">-Daily</span></span>
<span data-ttu-id="6b94d-121">Indica que a operação de backup é executada em um cronograma diário.</span><span class="sxs-lookup"><span data-stu-id="6b94d-121">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b94d-122">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="6b94d-122">-DaysOfWeek</span></span>
<span data-ttu-id="6b94d-123">Especifica uma matriz de dias da semana.</span><span class="sxs-lookup"><span data-stu-id="6b94d-123">Specifies an array of days of the week.</span></span>
<span data-ttu-id="6b94d-124">Esta política executa backups nos dias especificados por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6b94d-124">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="6b94d-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6b94d-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6b94d-126">Sexta</span><span class="sxs-lookup"><span data-stu-id="6b94d-126">Monday</span></span> 
- <span data-ttu-id="6b94d-127">-</span><span class="sxs-lookup"><span data-stu-id="6b94d-127">Tuesday</span></span> 
- <span data-ttu-id="6b94d-128">Feira</span><span class="sxs-lookup"><span data-stu-id="6b94d-128">Wednesday</span></span> 
- <span data-ttu-id="6b94d-129">Terça</span><span class="sxs-lookup"><span data-stu-id="6b94d-129">Thursday</span></span> 
- <span data-ttu-id="6b94d-130">Às</span><span class="sxs-lookup"><span data-stu-id="6b94d-130">Friday</span></span> 
- <span data-ttu-id="6b94d-131">Sábado</span><span class="sxs-lookup"><span data-stu-id="6b94d-131">Saturday</span></span> 
- <span data-ttu-id="6b94d-132">Domingo</span><span class="sxs-lookup"><span data-stu-id="6b94d-132">Sunday</span></span>

```yaml
Type: System.String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b94d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b94d-133">-DefaultProfile</span></span>
<span data-ttu-id="6b94d-134">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6b94d-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b94d-135">-NewName</span><span class="sxs-lookup"><span data-stu-id="6b94d-135">-NewName</span></span>
<span data-ttu-id="6b94d-136">Especifica o novo nome para a política.</span><span class="sxs-lookup"><span data-stu-id="6b94d-136">Specifies the new name for the policy.</span></span>
<span data-ttu-id="6b94d-137">Esse nome deve ser exclusivo em um cofre.</span><span class="sxs-lookup"><span data-stu-id="6b94d-137">This name must be unique in a vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b94d-138">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6b94d-138">-ProtectionPolicy</span></span>
<span data-ttu-id="6b94d-139">Especifica a política de proteção que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="6b94d-139">Specifies protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="6b94d-140">Para obter um objeto **AzureRmBackupProtectionPolicy** , use o cmdlet Get-AzureRmBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="6b94d-140">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b94d-141">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6b94d-141">-RetentionPolicy</span></span>
<span data-ttu-id="6b94d-142">Especifica uma matriz de políticas de retenção para a política de backup.</span><span class="sxs-lookup"><span data-stu-id="6b94d-142">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="6b94d-143">Para obter objetos **AzureRmBackupRetentionPolicy** , use o cmdlet New-AzureRmBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="6b94d-143">To obtain **AzureRmBackupRetentionPolicy** objects, use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b94d-144">-Semanal</span><span class="sxs-lookup"><span data-stu-id="6b94d-144">-Weekly</span></span>
<span data-ttu-id="6b94d-145">Indica que a operação de backup é executada em um cronograma semanal.</span><span class="sxs-lookup"><span data-stu-id="6b94d-145">Indicates that the backup operation runs on a Weekly schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b94d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b94d-146">CommonParameters</span></span>
<span data-ttu-id="6b94d-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b94d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b94d-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b94d-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b94d-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b94d-149">INPUTS</span></span>

### <span data-ttu-id="6b94d-150">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6b94d-150">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy</span></span>
<span data-ttu-id="6b94d-151">Parâmetros: ProtectionPolicy (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6b94d-151">Parameters: ProtectionPolicy (ByValue)</span></span>

## <span data-ttu-id="6b94d-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b94d-152">OUTPUTS</span></span>

### <span data-ttu-id="6b94d-153">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="6b94d-153">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="6b94d-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b94d-154">NOTES</span></span>

## <span data-ttu-id="6b94d-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b94d-155">RELATED LINKS</span></span>

[<span data-ttu-id="6b94d-156">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6b94d-156">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


