---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 7d41abd1d56bab4df0d716c3a9d11ea14140b784
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432943"
---
# <span data-ttu-id="dfff3-101">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="dfff3-101">Set-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="dfff3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dfff3-102">SYNOPSIS</span></span>
<span data-ttu-id="dfff3-103">Modifica uma política de proteção existente.</span><span class="sxs-lookup"><span data-stu-id="dfff3-103">Modifies an existing protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfff3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dfff3-104">SYNTAX</span></span>

### <span data-ttu-id="dfff3-105">NoScheduleParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="dfff3-105">NoScheduleParamSet (Default)</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfff3-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="dfff3-106">DailyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfff3-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="dfff3-107">WeeklyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dfff3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dfff3-108">DESCRIPTION</span></span>
<span data-ttu-id="dfff3-109">O cmdlet **set-AzureRmBackupProtectionPolicy** modifica uma política de proteção existente no Azure backup.</span><span class="sxs-lookup"><span data-stu-id="dfff3-109">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing protection policy in Azure Backup.</span></span>
<span data-ttu-id="dfff3-110">Você pode modificar os seguintes componentes da política de proteção:</span><span class="sxs-lookup"><span data-stu-id="dfff3-110">You can modify the following protection policy components:</span></span> 

- <span data-ttu-id="dfff3-111">Sobrenome</span><span class="sxs-lookup"><span data-stu-id="dfff3-111">Name</span></span>
- <span data-ttu-id="dfff3-112">Agendamento de backup</span><span class="sxs-lookup"><span data-stu-id="dfff3-112">Backup schedule</span></span>
- <span data-ttu-id="dfff3-113">Políticas de retenção</span><span class="sxs-lookup"><span data-stu-id="dfff3-113">Retention policies</span></span>

<span data-ttu-id="dfff3-114">Qualquer alteração pode afetar o backup e a retenção dos itens associados à política.</span><span class="sxs-lookup"><span data-stu-id="dfff3-114">Any change might affect the backup and retention of the items associated with the policy.</span></span>

## <span data-ttu-id="dfff3-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dfff3-115">EXAMPLES</span></span>

## <span data-ttu-id="dfff3-116">OS</span><span class="sxs-lookup"><span data-stu-id="dfff3-116">PARAMETERS</span></span>

### <span data-ttu-id="dfff3-117">-Backuptime</span><span class="sxs-lookup"><span data-stu-id="dfff3-117">-BackupTime</span></span>
<span data-ttu-id="dfff3-118">Especifica o novo horário de backup do dia, como um objeto **DateTime** , para a política.</span><span class="sxs-lookup"><span data-stu-id="dfff3-118">Specifies the new backup time of day, as a **DateTime** object, for the policy.</span></span>
<span data-ttu-id="dfff3-119">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="dfff3-119">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="dfff3-120">Para obter informações sobre objetos **DateTime** , digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="dfff3-120">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfff3-121">-Diariamente</span><span class="sxs-lookup"><span data-stu-id="dfff3-121">-Daily</span></span>
<span data-ttu-id="dfff3-122">Indica que a operação de backup é executada em um cronograma diário.</span><span class="sxs-lookup"><span data-stu-id="dfff3-122">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfff3-123">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="dfff3-123">-DaysOfWeek</span></span>
<span data-ttu-id="dfff3-124">Especifica uma matriz de dias da semana.</span><span class="sxs-lookup"><span data-stu-id="dfff3-124">Specifies an array of days of the week.</span></span>
<span data-ttu-id="dfff3-125">Esta política executa backups nos dias especificados por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="dfff3-125">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="dfff3-126">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="dfff3-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dfff3-127">Sexta</span><span class="sxs-lookup"><span data-stu-id="dfff3-127">Monday</span></span> 
- <span data-ttu-id="dfff3-128">-</span><span class="sxs-lookup"><span data-stu-id="dfff3-128">Tuesday</span></span> 
- <span data-ttu-id="dfff3-129">Feira</span><span class="sxs-lookup"><span data-stu-id="dfff3-129">Wednesday</span></span> 
- <span data-ttu-id="dfff3-130">Terça</span><span class="sxs-lookup"><span data-stu-id="dfff3-130">Thursday</span></span> 
- <span data-ttu-id="dfff3-131">Às</span><span class="sxs-lookup"><span data-stu-id="dfff3-131">Friday</span></span> 
- <span data-ttu-id="dfff3-132">Sábado</span><span class="sxs-lookup"><span data-stu-id="dfff3-132">Saturday</span></span> 
- <span data-ttu-id="dfff3-133">Domingo</span><span class="sxs-lookup"><span data-stu-id="dfff3-133">Sunday</span></span>

```yaml
Type: String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfff3-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfff3-134">-DefaultProfile</span></span>
<span data-ttu-id="dfff3-135">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="dfff3-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfff3-136">-NewName</span><span class="sxs-lookup"><span data-stu-id="dfff3-136">-NewName</span></span>
<span data-ttu-id="dfff3-137">Especifica o novo nome para a política.</span><span class="sxs-lookup"><span data-stu-id="dfff3-137">Specifies the new name for the policy.</span></span>
<span data-ttu-id="dfff3-138">Esse nome deve ser exclusivo em um cofre.</span><span class="sxs-lookup"><span data-stu-id="dfff3-138">This name must be unique in a vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfff3-139">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="dfff3-139">-ProtectionPolicy</span></span>
<span data-ttu-id="dfff3-140">Especifica a política de proteção que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="dfff3-140">Specifies protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="dfff3-141">Para obter um objeto **AzureRmBackupProtectionPolicy** , use o cmdlet Get-AzureRmBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="dfff3-141">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfff3-142">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dfff3-142">-RetentionPolicy</span></span>
<span data-ttu-id="dfff3-143">Especifica uma matriz de políticas de retenção para a política de backup.</span><span class="sxs-lookup"><span data-stu-id="dfff3-143">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="dfff3-144">Para obter objetos **AzureRmBackupRetentionPolicy** , use o cmdlet New-AzureRmBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="dfff3-144">To obtain **AzureRmBackupRetentionPolicy** objects, use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfff3-145">-Semanal</span><span class="sxs-lookup"><span data-stu-id="dfff3-145">-Weekly</span></span>
<span data-ttu-id="dfff3-146">Indica que a operação de backup é executada em um cronograma semanal.</span><span class="sxs-lookup"><span data-stu-id="dfff3-146">Indicates that the backup operation runs on a Weekly schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfff3-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfff3-147">CommonParameters</span></span>
<span data-ttu-id="dfff3-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfff3-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfff3-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfff3-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfff3-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dfff3-150">INPUTS</span></span>

### <span data-ttu-id="dfff3-151">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="dfff3-151">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="dfff3-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dfff3-152">OUTPUTS</span></span>

### <span data-ttu-id="dfff3-153">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="dfff3-153">None</span></span>

## <span data-ttu-id="dfff3-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dfff3-154">NOTES</span></span>

## <span data-ttu-id="dfff3-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dfff3-155">RELATED LINKS</span></span>

[<span data-ttu-id="dfff3-156">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="dfff3-156">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


