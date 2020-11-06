---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3A7B0280-CE6E-4374-87AF-4C1015EB88FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 4ea286ae6e3aec7f3eca961b5dc1452c717f3c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432957"
---
# <span data-ttu-id="68cd1-101">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="68cd1-101">New-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="68cd1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="68cd1-102">SYNOPSIS</span></span>
<span data-ttu-id="68cd1-103">Cria uma política de backup.</span><span class="sxs-lookup"><span data-stu-id="68cd1-103">Creates a Backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68cd1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="68cd1-104">SYNTAX</span></span>

### <span data-ttu-id="68cd1-105">NoScheduleParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="68cd1-105">NoScheduleParamSet (Default)</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-BackupTime] <DateTime>
 [[-DaysOfWeek] <String[]>] [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68cd1-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="68cd1-106">DailyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Daily] [-BackupTime] <DateTime>
 [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68cd1-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="68cd1-107">WeeklyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Weekly] [-BackupTime] <DateTime>
 [-DaysOfWeek] <String[]> [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68cd1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="68cd1-108">DESCRIPTION</span></span>
<span data-ttu-id="68cd1-109">O cmdlet **New-AzureRmBackupProtectionPolicy** cria uma política de backup do Azure como um objeto do PowerShell do Azure.</span><span class="sxs-lookup"><span data-stu-id="68cd1-109">The **New-AzureRmBackupProtectionPolicy** cmdlet creates an Azure Backup policy as an Azure PowerShell object.</span></span>

<span data-ttu-id="68cd1-110">Uma política de backup define quando e com que frequência o backup faz backup de um item.</span><span class="sxs-lookup"><span data-stu-id="68cd1-110">A backup policy defines when and how often Backup backs up an item.</span></span>
<span data-ttu-id="68cd1-111">O cmdlet Enable-AzureRmBackupProtection usa uma política de backup.</span><span class="sxs-lookup"><span data-stu-id="68cd1-111">The Enable-AzureRmBackupProtection cmdlet uses a backup policy.</span></span>

## <span data-ttu-id="68cd1-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="68cd1-112">EXAMPLES</span></span>

### <span data-ttu-id="68cd1-113">Exemplo 1: criar uma política de backup diária com retenção diária e mensal</span><span class="sxs-lookup"><span data-stu-id="68cd1-113">Example 1: Create a daily backup policy with daily and monthly retention</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $ProtectionPolicy = New-AzureRmBackupProtectionPolicy -Name DailyBackup01 -Type AzureVM -Daily -BackupTime ([datetime]"3:30 PM") -RetentionPolicy ($Daily,$Monthly) -Vault $Vault
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
```

<span data-ttu-id="68cd1-114">O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="68cd1-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="68cd1-115">O comando armazena esse objeto na variável $Vault.</span><span class="sxs-lookup"><span data-stu-id="68cd1-115">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="68cd1-116">O segundo comando cria uma política de retenção por 30 dias de retenção diária e, em seguida, armazena-a na variável $Daily.</span><span class="sxs-lookup"><span data-stu-id="68cd1-116">The second command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="68cd1-117">O terceiro comando cria uma política de retenção que mantém o backup no décimo e no vigésimo de cada mês por 12 meses.</span><span class="sxs-lookup"><span data-stu-id="68cd1-117">The third command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="68cd1-118">O comando armazena a política de retenção na variável $Monthly.</span><span class="sxs-lookup"><span data-stu-id="68cd1-118">The command stores the retention policy in the $Monthly variable.</span></span>

<span data-ttu-id="68cd1-119">O comando final cria uma política de backup para o cofre em $Vault que tenha uma hora de backup diária de 3:00 PM.</span><span class="sxs-lookup"><span data-stu-id="68cd1-119">The final command creates a backup policy for the vault in $Vault that has a daily backup time of 3:00 PM.</span></span>
<span data-ttu-id="68cd1-120">O comando atribui as políticas de retenção armazenadas em $Daily e $Monthly.</span><span class="sxs-lookup"><span data-stu-id="68cd1-120">The command assigns the retention policies stored in $Daily and $Monthly.</span></span>
<span data-ttu-id="68cd1-121">O comando armazena o resultado na variável $ProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="68cd1-121">The command stores the result in the $ProtectionPolicy variable.</span></span>

## <span data-ttu-id="68cd1-122">OS</span><span class="sxs-lookup"><span data-stu-id="68cd1-122">PARAMETERS</span></span>

### <span data-ttu-id="68cd1-123">-Backuptime</span><span class="sxs-lookup"><span data-stu-id="68cd1-123">-BackupTime</span></span>
<span data-ttu-id="68cd1-124">Especifica a hora do dia, como um objeto **DateTime** , para a operação de backup.</span><span class="sxs-lookup"><span data-stu-id="68cd1-124">Specifies the time of day, as a **DateTime** object, for the backup operation.</span></span>
<span data-ttu-id="68cd1-125">Para obter um **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="68cd1-125">To obtain a **DateTime** , use the Get-Date cmdlet.</span></span>
<span data-ttu-id="68cd1-126">Para obter informações sobre objetos **DateTime** , digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="68cd1-126">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68cd1-127">-Diariamente</span><span class="sxs-lookup"><span data-stu-id="68cd1-127">-Daily</span></span>
<span data-ttu-id="68cd1-128">Indica que a operação de backup é executada em um cronograma diário.</span><span class="sxs-lookup"><span data-stu-id="68cd1-128">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68cd1-129">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="68cd1-129">-DaysOfWeek</span></span>
<span data-ttu-id="68cd1-130">Especifica uma matriz de dias da semana.</span><span class="sxs-lookup"><span data-stu-id="68cd1-130">Specifies an array of days of the week.</span></span>
<span data-ttu-id="68cd1-131">Esta política executa backups nos dias especificados por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="68cd1-131">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="68cd1-132">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="68cd1-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="68cd1-133">Sexta</span><span class="sxs-lookup"><span data-stu-id="68cd1-133">Monday</span></span> 
- <span data-ttu-id="68cd1-134">-</span><span class="sxs-lookup"><span data-stu-id="68cd1-134">Tuesday</span></span> 
- <span data-ttu-id="68cd1-135">Feira</span><span class="sxs-lookup"><span data-stu-id="68cd1-135">Wednesday</span></span> 
- <span data-ttu-id="68cd1-136">Terça</span><span class="sxs-lookup"><span data-stu-id="68cd1-136">Thursday</span></span> 
- <span data-ttu-id="68cd1-137">Às</span><span class="sxs-lookup"><span data-stu-id="68cd1-137">Friday</span></span> 
- <span data-ttu-id="68cd1-138">Sábado</span><span class="sxs-lookup"><span data-stu-id="68cd1-138">Saturday</span></span> 
- <span data-ttu-id="68cd1-139">Domingo</span><span class="sxs-lookup"><span data-stu-id="68cd1-139">Sunday</span></span>

<span data-ttu-id="68cd1-140">Se você especificar o parâmetro *Weekly* , especifique esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="68cd1-140">If you specify the *Weekly* parameter, specify this parameter.</span></span>

```yaml
Type: String[]
Parameter Sets: NoScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68cd1-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68cd1-141">-DefaultProfile</span></span>
<span data-ttu-id="68cd1-142">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="68cd1-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68cd1-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="68cd1-143">-Name</span></span>
<span data-ttu-id="68cd1-144">Especifica um nome para a política de backup.</span><span class="sxs-lookup"><span data-stu-id="68cd1-144">Specifies a name for the backup policy.</span></span>
<span data-ttu-id="68cd1-145">Selecione um nome exclusivo no cofre.</span><span class="sxs-lookup"><span data-stu-id="68cd1-145">Select a name that is unique in the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68cd1-146">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="68cd1-146">-RetentionPolicy</span></span>
<span data-ttu-id="68cd1-147">Especifica uma matriz de políticas de retenção para a política de backup.</span><span class="sxs-lookup"><span data-stu-id="68cd1-147">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="68cd1-148">Para obter um **AzureRmBackupRetentionPolicy** , use o cmdlet New-AzureRmBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="68cd1-148">To obtain an **AzureRmBackupRetentionPolicy** , use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68cd1-149">-Digite</span><span class="sxs-lookup"><span data-stu-id="68cd1-149">-Type</span></span>
<span data-ttu-id="68cd1-150">Especifica o tipo de item de backup ao qual a política se aplica.</span><span class="sxs-lookup"><span data-stu-id="68cd1-150">Specifies the type of backup item to which the policy applies.</span></span>
<span data-ttu-id="68cd1-151">Atualmente, o único valor com suporte é AzureVM.</span><span class="sxs-lookup"><span data-stu-id="68cd1-151">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68cd1-152">-Cofre</span><span class="sxs-lookup"><span data-stu-id="68cd1-152">-Vault</span></span>
<span data-ttu-id="68cd1-153">Especifica o cofre do Azure backup ao qual a política de backup pertence.</span><span class="sxs-lookup"><span data-stu-id="68cd1-153">Specifies the Azure Backup vault to which the backup policy belongs.</span></span>
<span data-ttu-id="68cd1-154">Para obter um objeto **AzureRmBackupVault** , use o cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="68cd1-154">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68cd1-155">-Semanal</span><span class="sxs-lookup"><span data-stu-id="68cd1-155">-Weekly</span></span>
<span data-ttu-id="68cd1-156">Indica que a política de backup é disparada semanalmente em um ou mais dias da semana.</span><span class="sxs-lookup"><span data-stu-id="68cd1-156">Indicates that the backup policy is triggered weekly on one or more days of the week.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68cd1-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68cd1-157">CommonParameters</span></span>
<span data-ttu-id="68cd1-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68cd1-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68cd1-159">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68cd1-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68cd1-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="68cd1-160">INPUTS</span></span>

### <span data-ttu-id="68cd1-161">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="68cd1-161">None</span></span>

## <span data-ttu-id="68cd1-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="68cd1-162">OUTPUTS</span></span>

### <span data-ttu-id="68cd1-163">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="68cd1-163">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="68cd1-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="68cd1-164">NOTES</span></span>
* <span data-ttu-id="68cd1-165">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="68cd1-165">None</span></span>

## <span data-ttu-id="68cd1-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="68cd1-166">RELATED LINKS</span></span>

[<span data-ttu-id="68cd1-167">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="68cd1-167">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="68cd1-168">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="68cd1-168">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="68cd1-169">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="68cd1-169">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="68cd1-170">New-AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="68cd1-170">New-AzureRmBackupRetentionPolicyObject</span></span>](./New-AzureRmBackupRetentionPolicyObject.md)

[<span data-ttu-id="68cd1-171">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="68cd1-171">Remove-AzureRmBackupProtectionPolicy</span></span>](./Remove-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="68cd1-172">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="68cd1-172">Set-AzureRmBackupProtectionPolicy</span></span>](./Set-AzureRmBackupProtectionPolicy.md)


