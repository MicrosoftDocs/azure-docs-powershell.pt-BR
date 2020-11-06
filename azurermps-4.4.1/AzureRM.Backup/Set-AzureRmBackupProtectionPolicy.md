---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 70e6cf359f81911d8dff2e96944e93c388cfc80e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431154"
---
# <span data-ttu-id="772cf-101">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="772cf-101">Set-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="772cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="772cf-102">SYNOPSIS</span></span>
<span data-ttu-id="772cf-103">Modifica uma política de proteção existente.</span><span class="sxs-lookup"><span data-stu-id="772cf-103">Modifies an existing protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="772cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="772cf-104">SYNTAX</span></span>

### <span data-ttu-id="772cf-105">NoScheduleParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="772cf-105">NoScheduleParamSet (Default)</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="772cf-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="772cf-106">DailyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="772cf-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="772cf-107">WeeklyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="772cf-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="772cf-108">DESCRIPTION</span></span>
<span data-ttu-id="772cf-109">O cmdlet **set-AzureRmBackupProtectionPolicy** modifica uma política de proteção existente no Azure backup.</span><span class="sxs-lookup"><span data-stu-id="772cf-109">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing protection policy in Azure Backup.</span></span>
<span data-ttu-id="772cf-110">Você pode modificar os seguintes componentes da política de proteção:</span><span class="sxs-lookup"><span data-stu-id="772cf-110">You can modify the following protection policy components:</span></span> 

- <span data-ttu-id="772cf-111">Sobrenome</span><span class="sxs-lookup"><span data-stu-id="772cf-111">Name</span></span>
- <span data-ttu-id="772cf-112">Agendamento de backup</span><span class="sxs-lookup"><span data-stu-id="772cf-112">Backup schedule</span></span>
- <span data-ttu-id="772cf-113">Políticas de retenção</span><span class="sxs-lookup"><span data-stu-id="772cf-113">Retention policies</span></span>

<span data-ttu-id="772cf-114">Qualquer alteração pode afetar o backup e a retenção dos itens associados à política.</span><span class="sxs-lookup"><span data-stu-id="772cf-114">Any change might affect the backup and retention of the items associated with the policy.</span></span>

## <span data-ttu-id="772cf-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="772cf-115">EXAMPLES</span></span>

## <span data-ttu-id="772cf-116">OS</span><span class="sxs-lookup"><span data-stu-id="772cf-116">PARAMETERS</span></span>

### <span data-ttu-id="772cf-117">-Backuptime</span><span class="sxs-lookup"><span data-stu-id="772cf-117">-BackupTime</span></span>
<span data-ttu-id="772cf-118">Especifica o novo horário de backup do dia, como um objeto **DateTime** , para a política.</span><span class="sxs-lookup"><span data-stu-id="772cf-118">Specifies the new backup time of day, as a **DateTime** object, for the policy.</span></span>
<span data-ttu-id="772cf-119">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="772cf-119">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="772cf-120">Para obter informações sobre objetos **DateTime** , digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="772cf-120">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="772cf-121">-Diariamente</span><span class="sxs-lookup"><span data-stu-id="772cf-121">-Daily</span></span>
<span data-ttu-id="772cf-122">Indica que a operação de backup é executada em um cronograma diário.</span><span class="sxs-lookup"><span data-stu-id="772cf-122">Indicates that the backup operation runs on a Daily schedule.</span></span>

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

### <span data-ttu-id="772cf-123">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="772cf-123">-DaysOfWeek</span></span>
<span data-ttu-id="772cf-124">Especifica uma matriz de dias da semana.</span><span class="sxs-lookup"><span data-stu-id="772cf-124">Specifies an array of days of the week.</span></span>
<span data-ttu-id="772cf-125">Esta política executa backups nos dias especificados por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="772cf-125">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="772cf-126">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="772cf-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="772cf-127">Sexta</span><span class="sxs-lookup"><span data-stu-id="772cf-127">Monday</span></span> 
- <span data-ttu-id="772cf-128">-</span><span class="sxs-lookup"><span data-stu-id="772cf-128">Tuesday</span></span> 
- <span data-ttu-id="772cf-129">Feira</span><span class="sxs-lookup"><span data-stu-id="772cf-129">Wednesday</span></span> 
- <span data-ttu-id="772cf-130">Terça</span><span class="sxs-lookup"><span data-stu-id="772cf-130">Thursday</span></span> 
- <span data-ttu-id="772cf-131">Às</span><span class="sxs-lookup"><span data-stu-id="772cf-131">Friday</span></span> 
- <span data-ttu-id="772cf-132">Sábado</span><span class="sxs-lookup"><span data-stu-id="772cf-132">Saturday</span></span> 
- <span data-ttu-id="772cf-133">Domingo</span><span class="sxs-lookup"><span data-stu-id="772cf-133">Sunday</span></span>

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

### <span data-ttu-id="772cf-134">-NewName</span><span class="sxs-lookup"><span data-stu-id="772cf-134">-NewName</span></span>
<span data-ttu-id="772cf-135">Especifica o novo nome para a política.</span><span class="sxs-lookup"><span data-stu-id="772cf-135">Specifies the new name for the policy.</span></span>
<span data-ttu-id="772cf-136">Esse nome deve ser exclusivo em um cofre.</span><span class="sxs-lookup"><span data-stu-id="772cf-136">This name must be unique in a vault.</span></span>

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

### <span data-ttu-id="772cf-137">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="772cf-137">-ProtectionPolicy</span></span>
<span data-ttu-id="772cf-138">Especifica a política de proteção que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="772cf-138">Specifies protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="772cf-139">Para obter um objeto **AzureRmBackupProtectionPolicy** , use o cmdlet Get-AzureRmBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="772cf-139">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="772cf-140">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="772cf-140">-RetentionPolicy</span></span>
<span data-ttu-id="772cf-141">Especifica uma matriz de políticas de retenção para a política de backup.</span><span class="sxs-lookup"><span data-stu-id="772cf-141">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="772cf-142">Para obter objetos **AzureRmBackupRetentionPolicy** , use o cmdlet New-AzureRmBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="772cf-142">To obtain **AzureRmBackupRetentionPolicy** objects, use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

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

### <span data-ttu-id="772cf-143">-Semanal</span><span class="sxs-lookup"><span data-stu-id="772cf-143">-Weekly</span></span>
<span data-ttu-id="772cf-144">Indica que a operação de backup é executada em um cronograma semanal.</span><span class="sxs-lookup"><span data-stu-id="772cf-144">Indicates that the backup operation runs on a Weekly schedule.</span></span>

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

### <span data-ttu-id="772cf-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="772cf-145">-DefaultProfile</span></span>
<span data-ttu-id="772cf-146">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="772cf-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="772cf-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="772cf-147">CommonParameters</span></span>
<span data-ttu-id="772cf-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="772cf-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="772cf-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="772cf-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="772cf-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="772cf-150">INPUTS</span></span>

### <span data-ttu-id="772cf-151">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="772cf-151">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="772cf-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="772cf-152">OUTPUTS</span></span>

### <span data-ttu-id="772cf-153">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="772cf-153">None</span></span>

## <span data-ttu-id="772cf-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="772cf-154">NOTES</span></span>

## <span data-ttu-id="772cf-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="772cf-155">RELATED LINKS</span></span>

[<span data-ttu-id="772cf-156">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="772cf-156">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


