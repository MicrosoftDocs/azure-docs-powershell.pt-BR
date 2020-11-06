---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9574CEB5-B699-4606-8C5E-CE2C0D01092D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
ms.openlocfilehash: 0673b0c98e263a0c947fa984267e0eb49ccf9f9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432956"
---
# <span data-ttu-id="33c6d-101">New-AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="33c6d-101">New-AzureRmBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="33c6d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33c6d-102">SYNOPSIS</span></span>
<span data-ttu-id="33c6d-103">Cria uma política de retenção de backup.</span><span class="sxs-lookup"><span data-stu-id="33c6d-103">Creates a Backup retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33c6d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33c6d-104">SYNTAX</span></span>

### <span data-ttu-id="33c6d-105">DailyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="33c6d-105">DailyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-DailyRetention] -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33c6d-106">WeeklyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="33c6d-106">WeeklyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-WeeklyRetention] -DaysOfWeek <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33c6d-107">MonthlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="33c6d-107">MonthlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33c6d-108">MonthlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="33c6d-108">MonthlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33c6d-109">YearlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="33c6d-109">YearlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -MonthsOfYear <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33c6d-110">YearlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="33c6d-110">YearlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -MonthsOfYear <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="33c6d-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="33c6d-111">DESCRIPTION</span></span>
<span data-ttu-id="33c6d-112">O cmdlet **New-AzureRmBackupRetentionPolicyObject** cria uma política de retenção de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="33c6d-112">The **New-AzureRmBackupRetentionPolicyObject** cmdlet creates an Azure Backup retention policy.</span></span>
<span data-ttu-id="33c6d-113">Uma política de retenção define por quanto tempo o backup mantém um ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="33c6d-113">A retention policy defines how long Backup keeps a recovery point.</span></span>
<span data-ttu-id="33c6d-114">Os tipos de retenção são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="33c6d-114">The types of retention are the following:</span></span> 

- <span data-ttu-id="33c6d-115">Daily</span><span class="sxs-lookup"><span data-stu-id="33c6d-115">Daily</span></span> 
- <span data-ttu-id="33c6d-116">Mensal</span><span class="sxs-lookup"><span data-stu-id="33c6d-116">Weekly</span></span> 
- <span data-ttu-id="33c6d-117">Mensal</span><span class="sxs-lookup"><span data-stu-id="33c6d-117">Monthly</span></span> 
- <span data-ttu-id="33c6d-118">Anual</span><span class="sxs-lookup"><span data-stu-id="33c6d-118">Yearly</span></span> 

<span data-ttu-id="33c6d-119">Crie uma política de retenção para cada tipo de retenção que você planeja usar.</span><span class="sxs-lookup"><span data-stu-id="33c6d-119">Create one retention policy for each type of retention that you plan to use.</span></span>

<span data-ttu-id="33c6d-120">Uma política de backup está associada a pelo menos uma política de retenção.</span><span class="sxs-lookup"><span data-stu-id="33c6d-120">A backup policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="33c6d-121">Para criar uma política de backup, use o cmdlet New-AzureRmBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="33c6d-121">To create a backup policy, use the New-AzureRmBackupProtectionPolicy cmdlet.</span></span>
<span data-ttu-id="33c6d-122">Em vez disso, você pode fornecer uma política de retenção para o cmdlet Enable-AzureRmBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="33c6d-122">You can instead provide a retention policy to the Enable-AzureRmBackupProtection cmdlet.</span></span>

## <span data-ttu-id="33c6d-123">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33c6d-123">EXAMPLES</span></span>

### <span data-ttu-id="33c6d-124">Exemplo 1: criar uma política de retenção para retenção diária</span><span class="sxs-lookup"><span data-stu-id="33c6d-124">Example 1: Create a retention policy for daily retention</span></span>
```
PS C:\>$Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Daily
RetentionType      Retention          RetentionTimes
-------------      ---------          --------------
Daily              30
```

<span data-ttu-id="33c6d-125">O primeiro comando cria uma política de retenção por 30 dias de retenção diária e, em seguida, armazena-a na variável $Daily.</span><span class="sxs-lookup"><span data-stu-id="33c6d-125">The first command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="33c6d-126">O segundo comando exibe o conteúdo de $Daily.</span><span class="sxs-lookup"><span data-stu-id="33c6d-126">The second command displays the contents of $Daily.</span></span>

### <span data-ttu-id="33c6d-127">Exemplo 2: criar uma política de retenção mensal</span><span class="sxs-lookup"><span data-stu-id="33c6d-127">Example 2: Create a monthly retention policy</span></span>
```
PS C:\>$Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $Monthly | select *
RetentionFormat : Daily
DaysOfMonth     : {10, 20}
WeekNumber      : 
DaysOfWeek      : 
RetentionType   : Monthly
Retention       : 12
RetentionTimes  :
```

<span data-ttu-id="33c6d-128">O primeiro comando cria uma política de retenção que mantém o backup no décimo e no vigésimo de cada mês por 12 meses.</span><span class="sxs-lookup"><span data-stu-id="33c6d-128">The first command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="33c6d-129">O comando armazena a política de retenção na variável $Monthly.</span><span class="sxs-lookup"><span data-stu-id="33c6d-129">The command stores the retention policy in the $Monthly variable.</span></span>

<span data-ttu-id="33c6d-130">O segundo comando exibe o conteúdo de $Monthly.</span><span class="sxs-lookup"><span data-stu-id="33c6d-130">The second command displays the contents of $Monthly.</span></span>

## <span data-ttu-id="33c6d-131">OS</span><span class="sxs-lookup"><span data-stu-id="33c6d-131">PARAMETERS</span></span>

### <span data-ttu-id="33c6d-132">-DailyRetention</span><span class="sxs-lookup"><span data-stu-id="33c6d-132">-DailyRetention</span></span>
<span data-ttu-id="33c6d-133">Indica que esse cmdlet cria uma política de retenção diária.</span><span class="sxs-lookup"><span data-stu-id="33c6d-133">Indicates that this cmdlet creates a Daily retention policy.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DailyRetentionParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33c6d-134">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="33c6d-134">-DaysOfMonth</span></span>
<span data-ttu-id="33c6d-135">Especifica os dias do mês que identificam quais pontos de recuperação o backup mantém e por quanto tempo.</span><span class="sxs-lookup"><span data-stu-id="33c6d-135">Specifies the days of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="33c6d-136">Os valores aceitáveis para esse parâmetro são: inteiros de 1 a 28 e sobrenome.</span><span class="sxs-lookup"><span data-stu-id="33c6d-136">The acceptable values for this parameter are: integers from 1 through 28 and Last.</span></span>
<span data-ttu-id="33c6d-137">Especifique esse parâmetro se especificar os parâmetros *DailyRetention* , *MonthlyRetentionInDailyFormat* e *YearlyRetentionInDailyFormat* .</span><span class="sxs-lookup"><span data-stu-id="33c6d-137">Specify this parameter if you specify the *DailyRetention* , *MonthlyRetentionInDailyFormat* , and *YearlyRetentionInDailyFormat* parameters.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: MonthlyRetentionInDailyFormatParamSet, YearlyRetentionInDailyFormatParamSet
Aliases: 
Accepted values: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33c6d-138">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="33c6d-138">-DaysOfWeek</span></span>
<span data-ttu-id="33c6d-139">Especifica uma matriz de dias da semana.</span><span class="sxs-lookup"><span data-stu-id="33c6d-139">Specifies an array of days of the week.</span></span>
<span data-ttu-id="33c6d-140">Os dias em que esse cmdlet especifica identificar quais pontos de recuperação o backup manterá e por quanto tempo.</span><span class="sxs-lookup"><span data-stu-id="33c6d-140">The days that this cmdlet specifies identify which recovery points that Backup retains and for how long.</span></span>
<span data-ttu-id="33c6d-141">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="33c6d-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="33c6d-142">Sexta</span><span class="sxs-lookup"><span data-stu-id="33c6d-142">Monday</span></span> 
- <span data-ttu-id="33c6d-143">-</span><span class="sxs-lookup"><span data-stu-id="33c6d-143">Tuesday</span></span> 
- <span data-ttu-id="33c6d-144">Feira</span><span class="sxs-lookup"><span data-stu-id="33c6d-144">Wednesday</span></span> 
- <span data-ttu-id="33c6d-145">Terça</span><span class="sxs-lookup"><span data-stu-id="33c6d-145">Thursday</span></span> 
- <span data-ttu-id="33c6d-146">Às</span><span class="sxs-lookup"><span data-stu-id="33c6d-146">Friday</span></span> 
- <span data-ttu-id="33c6d-147">Sábado</span><span class="sxs-lookup"><span data-stu-id="33c6d-147">Saturday</span></span> 
- <span data-ttu-id="33c6d-148">Domingo</span><span class="sxs-lookup"><span data-stu-id="33c6d-148">Sunday</span></span>

<span data-ttu-id="33c6d-149">Especifique esse parâmetro se especificar os parâmetros *WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* e *YearlyRetentionInWeeklyFormat* .</span><span class="sxs-lookup"><span data-stu-id="33c6d-149">Specify this parameter if you specify the *WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* , and *YearlyRetentionInWeeklyFormat* parameters.</span></span>

<span data-ttu-id="33c6d-150">Certifique-se de que os dias da semana selecionados para backup e a retenção sejam alinhados.</span><span class="sxs-lookup"><span data-stu-id="33c6d-150">Be sure that the days of the week you select for backup and for retention are aligned.</span></span>
<span data-ttu-id="33c6d-151">Por exemplo, se o backup estiver definido para sábados, as políticas de retenção também deverão usar o sábado.</span><span class="sxs-lookup"><span data-stu-id="33c6d-151">For example, if your backup is set for Saturdays, the retention policies must also use Saturday.</span></span>

```yaml
Type: String[]
Parameter Sets: WeeklyRetentionParamSet, MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33c6d-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33c6d-152">-DefaultProfile</span></span>
<span data-ttu-id="33c6d-153">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="33c6d-153">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33c6d-154">-MonthlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="33c6d-154">-MonthlyRetentionInDailyFormat</span></span>
<span data-ttu-id="33c6d-155">Indica que esse cmdlet cria uma política mensal no formato diário.</span><span class="sxs-lookup"><span data-stu-id="33c6d-155">Indicates that this cmdlet creates a Monthly policy in Daily format.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: MonthlyRetentionInDailyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33c6d-156">-MonthlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="33c6d-156">-MonthlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="33c6d-157">Indica que esse cmdlet cria uma política mensal em formato semanal.</span><span class="sxs-lookup"><span data-stu-id="33c6d-157">Indicates that this cmdlet creates a Monthly policy in Weekly format.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33c6d-158">-MonthsOfYear</span><span class="sxs-lookup"><span data-stu-id="33c6d-158">-MonthsOfYear</span></span>
<span data-ttu-id="33c6d-159">Especifica quais meses do ano têm os pontos de recuperação que o backup retém anualmente.</span><span class="sxs-lookup"><span data-stu-id="33c6d-159">Specifies which months of the year have the recovery points that Backup retains on a yearly basis.</span></span>
<span data-ttu-id="33c6d-160">Os valores aceitáveis para esse parâmetro são: nomes de meses, como Janeiro ou fevereiro.</span><span class="sxs-lookup"><span data-stu-id="33c6d-160">The acceptable values for this parameter are: names of months, such as January or February.</span></span>

```yaml
Type: String[]
Parameter Sets: YearlyRetentionInDailyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: January, February, March, April, May, June, July, August, September, October, November, December

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33c6d-161">-Retenção</span><span class="sxs-lookup"><span data-stu-id="33c6d-161">-Retention</span></span>
<span data-ttu-id="33c6d-162">Especifica o período de retenção, em dias, meses ou anos, para o qual o backup armazena um ponto de backup.</span><span class="sxs-lookup"><span data-stu-id="33c6d-162">Specifies the retention period, in days, months, or years, for which Backup stores a backup point.</span></span>
<span data-ttu-id="33c6d-163">A unidade depende se esse cmdlet seleciona uma opção de retenção diária, mensal ou anual.</span><span class="sxs-lookup"><span data-stu-id="33c6d-163">The unit depends on whether this cmdlet selects a daily, monthly, or yearly retention option.</span></span>
<span data-ttu-id="33c6d-164">Por exemplo, se especificar o parâmetro *DailyRetention* , o cmdlet interpretará o parâmetro atual como um número de dias.</span><span class="sxs-lookup"><span data-stu-id="33c6d-164">For example, if specify the *DailyRetention* parameter, the cmdlet interprets the current parameter as a number of days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33c6d-165">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="33c6d-165">-WeeklyRetention</span></span>
<span data-ttu-id="33c6d-166">Indica que esse cmdlet cria uma política de retenção semanal.</span><span class="sxs-lookup"><span data-stu-id="33c6d-166">Indicates that this cmdlet creates a Weekly retention policy.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WeeklyRetentionParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33c6d-167">-WeekNumber</span><span class="sxs-lookup"><span data-stu-id="33c6d-167">-WeekNumber</span></span>
<span data-ttu-id="33c6d-168">Especifica as semanas do mês que identificam quais pontos de recuperação o backup mantém e por quanto tempo.</span><span class="sxs-lookup"><span data-stu-id="33c6d-168">Specifies the weeks of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="33c6d-169">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="33c6d-169">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="33c6d-170">Primeiros</span><span class="sxs-lookup"><span data-stu-id="33c6d-170">First</span></span> 
- <span data-ttu-id="33c6d-171">Secundária</span><span class="sxs-lookup"><span data-stu-id="33c6d-171">Second</span></span> 
- <span data-ttu-id="33c6d-172">Terceiriza</span><span class="sxs-lookup"><span data-stu-id="33c6d-172">Third</span></span> 
- <span data-ttu-id="33c6d-173">Fourth</span><span class="sxs-lookup"><span data-stu-id="33c6d-173">Fourth</span></span> 
- <span data-ttu-id="33c6d-174">Nome</span><span class="sxs-lookup"><span data-stu-id="33c6d-174">Last</span></span>

```yaml
Type: String[]
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: First, Second, Third, Fourth, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33c6d-175">-YearlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="33c6d-175">-YearlyRetentionInDailyFormat</span></span>
<span data-ttu-id="33c6d-176">Indica que esse cmdlet cria uma política de retenção anual em formato diário.</span><span class="sxs-lookup"><span data-stu-id="33c6d-176">Indicates that this cmdlet creates a Yearly retention policy in Daily format.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: YearlyRetentionInDailyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33c6d-177">-YearlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="33c6d-177">-YearlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="33c6d-178">Indica que esse cmdlet cria uma política de retenção anual em formato semanal.</span><span class="sxs-lookup"><span data-stu-id="33c6d-178">Indicates that this cmdlet creates a Yearly retention policy in Weekly format.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: YearlyRetentionInWeeklyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33c6d-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33c6d-179">CommonParameters</span></span>
<span data-ttu-id="33c6d-180">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33c6d-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33c6d-181">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33c6d-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33c6d-182">SENSORES</span><span class="sxs-lookup"><span data-stu-id="33c6d-182">INPUTS</span></span>

### <span data-ttu-id="33c6d-183">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="33c6d-183">None</span></span>

## <span data-ttu-id="33c6d-184">EXIBE</span><span class="sxs-lookup"><span data-stu-id="33c6d-184">OUTPUTS</span></span>

### <span data-ttu-id="33c6d-185">AzureRmBackupRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="33c6d-185">AzureRmBackupRetentionPolicy</span></span>

## <span data-ttu-id="33c6d-186">INFORMA</span><span class="sxs-lookup"><span data-stu-id="33c6d-186">NOTES</span></span>
* <span data-ttu-id="33c6d-187">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="33c6d-187">None</span></span>

## <span data-ttu-id="33c6d-188">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33c6d-188">RELATED LINKS</span></span>

[<span data-ttu-id="33c6d-189">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="33c6d-189">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="33c6d-190">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="33c6d-190">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


