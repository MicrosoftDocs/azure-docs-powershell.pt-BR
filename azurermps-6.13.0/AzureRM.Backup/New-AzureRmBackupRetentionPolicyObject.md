---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9574CEB5-B699-4606-8C5E-CE2C0D01092D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
ms.openlocfilehash: 740077def0ba0eccb1d962b88317fadb3c5c897c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427302"
---
# <span data-ttu-id="d46e3-101">New-AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="d46e3-101">New-AzureRmBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="d46e3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d46e3-102">SYNOPSIS</span></span>
<span data-ttu-id="d46e3-103">Cria uma política de retenção de backup.</span><span class="sxs-lookup"><span data-stu-id="d46e3-103">Creates a Backup retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d46e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d46e3-104">SYNTAX</span></span>

### <span data-ttu-id="d46e3-105">DailyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="d46e3-105">DailyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-DailyRetention] -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d46e3-106">WeeklyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="d46e3-106">WeeklyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-WeeklyRetention] -DaysOfWeek <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d46e3-107">MonthlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="d46e3-107">MonthlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d46e3-108">MonthlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="d46e3-108">MonthlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d46e3-109">YearlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="d46e3-109">YearlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -MonthsOfYear <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d46e3-110">YearlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="d46e3-110">YearlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -MonthsOfYear <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d46e3-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d46e3-111">DESCRIPTION</span></span>
<span data-ttu-id="d46e3-112">O cmdlet **New-AzureRmBackupRetentionPolicyObject** cria uma política de retenção de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="d46e3-112">The **New-AzureRmBackupRetentionPolicyObject** cmdlet creates an Azure Backup retention policy.</span></span>
<span data-ttu-id="d46e3-113">Uma política de retenção define por quanto tempo o backup mantém um ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d46e3-113">A retention policy defines how long Backup keeps a recovery point.</span></span>
<span data-ttu-id="d46e3-114">Os tipos de retenção são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="d46e3-114">The types of retention are the following:</span></span> 
- <span data-ttu-id="d46e3-115">Daily</span><span class="sxs-lookup"><span data-stu-id="d46e3-115">Daily</span></span> 
- <span data-ttu-id="d46e3-116">Mensal</span><span class="sxs-lookup"><span data-stu-id="d46e3-116">Weekly</span></span> 
- <span data-ttu-id="d46e3-117">Mensal</span><span class="sxs-lookup"><span data-stu-id="d46e3-117">Monthly</span></span> 
- <span data-ttu-id="d46e3-118">Crie anualmente uma política de retenção para cada tipo de retenção que você planeja usar.</span><span class="sxs-lookup"><span data-stu-id="d46e3-118">Yearly Create one retention policy for each type of retention that you plan to use.</span></span>
<span data-ttu-id="d46e3-119">Uma política de backup está associada a pelo menos uma política de retenção.</span><span class="sxs-lookup"><span data-stu-id="d46e3-119">A backup policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="d46e3-120">Para criar uma política de backup, use o cmdlet New-AzureRmBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="d46e3-120">To create a backup policy, use the New-AzureRmBackupProtectionPolicy cmdlet.</span></span>
<span data-ttu-id="d46e3-121">Em vez disso, você pode fornecer uma política de retenção para o cmdlet Enable-AzureRmBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="d46e3-121">You can instead provide a retention policy to the Enable-AzureRmBackupProtection cmdlet.</span></span>

## <span data-ttu-id="d46e3-122">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d46e3-122">EXAMPLES</span></span>

### <span data-ttu-id="d46e3-123">Exemplo 1: criar uma política de retenção para retenção diária</span><span class="sxs-lookup"><span data-stu-id="d46e3-123">Example 1: Create a retention policy for daily retention</span></span>
```
PS C:\>$Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Daily
RetentionType      Retention          RetentionTimes
-------------      ---------          --------------
Daily              30
```

<span data-ttu-id="d46e3-124">O primeiro comando cria uma política de retenção por 30 dias de retenção diária e, em seguida, armazena-a na variável $Daily.</span><span class="sxs-lookup"><span data-stu-id="d46e3-124">The first command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>
<span data-ttu-id="d46e3-125">O segundo comando exibe o conteúdo de $Daily.</span><span class="sxs-lookup"><span data-stu-id="d46e3-125">The second command displays the contents of $Daily.</span></span>

### <span data-ttu-id="d46e3-126">Exemplo 2: criar uma política de retenção mensal</span><span class="sxs-lookup"><span data-stu-id="d46e3-126">Example 2: Create a monthly retention policy</span></span>
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

<span data-ttu-id="d46e3-127">O primeiro comando cria uma política de retenção que mantém o backup no décimo e no vigésimo de cada mês por 12 meses.</span><span class="sxs-lookup"><span data-stu-id="d46e3-127">The first command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="d46e3-128">O comando armazena a política de retenção na variável $Monthly.</span><span class="sxs-lookup"><span data-stu-id="d46e3-128">The command stores the retention policy in the $Monthly variable.</span></span>
<span data-ttu-id="d46e3-129">O segundo comando exibe o conteúdo de $Monthly.</span><span class="sxs-lookup"><span data-stu-id="d46e3-129">The second command displays the contents of $Monthly.</span></span>

## <span data-ttu-id="d46e3-130">OS</span><span class="sxs-lookup"><span data-stu-id="d46e3-130">PARAMETERS</span></span>

### <span data-ttu-id="d46e3-131">-DailyRetention</span><span class="sxs-lookup"><span data-stu-id="d46e3-131">-DailyRetention</span></span>
<span data-ttu-id="d46e3-132">Indica que esse cmdlet cria uma política de retenção diária.</span><span class="sxs-lookup"><span data-stu-id="d46e3-132">Indicates that this cmdlet creates a Daily retention policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyRetentionParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46e3-133">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="d46e3-133">-DaysOfMonth</span></span>
<span data-ttu-id="d46e3-134">Especifica os dias do mês que identificam quais pontos de recuperação o backup mantém e por quanto tempo.</span><span class="sxs-lookup"><span data-stu-id="d46e3-134">Specifies the days of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="d46e3-135">Os valores aceitáveis para esse parâmetro são: inteiros de 1 a 28 e sobrenome.</span><span class="sxs-lookup"><span data-stu-id="d46e3-135">The acceptable values for this parameter are: integers from 1 through 28 and Last.</span></span>
<span data-ttu-id="d46e3-136">Especifique esse parâmetro se especificar os parâmetros *DailyRetention* , *MonthlyRetentionInDailyFormat* e *YearlyRetentionInDailyFormat* .</span><span class="sxs-lookup"><span data-stu-id="d46e3-136">Specify this parameter if you specify the *DailyRetention* , *MonthlyRetentionInDailyFormat* , and *YearlyRetentionInDailyFormat* parameters.</span></span>

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

### <span data-ttu-id="d46e3-137">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="d46e3-137">-DaysOfWeek</span></span>
<span data-ttu-id="d46e3-138">Especifica uma matriz de dias da semana.</span><span class="sxs-lookup"><span data-stu-id="d46e3-138">Specifies an array of days of the week.</span></span>
<span data-ttu-id="d46e3-139">Os dias em que esse cmdlet especifica identificar quais pontos de recuperação o backup manterá e por quanto tempo.</span><span class="sxs-lookup"><span data-stu-id="d46e3-139">The days that this cmdlet specifies identify which recovery points that Backup retains and for how long.</span></span>
<span data-ttu-id="d46e3-140">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d46e3-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d46e3-141">Sexta</span><span class="sxs-lookup"><span data-stu-id="d46e3-141">Monday</span></span> 
- <span data-ttu-id="d46e3-142">-</span><span class="sxs-lookup"><span data-stu-id="d46e3-142">Tuesday</span></span> 
- <span data-ttu-id="d46e3-143">Feira</span><span class="sxs-lookup"><span data-stu-id="d46e3-143">Wednesday</span></span> 
- <span data-ttu-id="d46e3-144">Terça</span><span class="sxs-lookup"><span data-stu-id="d46e3-144">Thursday</span></span> 
- <span data-ttu-id="d46e3-145">Às</span><span class="sxs-lookup"><span data-stu-id="d46e3-145">Friday</span></span> 
- <span data-ttu-id="d46e3-146">Sábado</span><span class="sxs-lookup"><span data-stu-id="d46e3-146">Saturday</span></span> 
- <span data-ttu-id="d46e3-147">Domingo Especifique esse parâmetro se você especificar os parâmetros *WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* e *YearlyRetentionInWeeklyFormat* .</span><span class="sxs-lookup"><span data-stu-id="d46e3-147">Sunday Specify this parameter if you specify the *WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* , and *YearlyRetentionInWeeklyFormat* parameters.</span></span>
<span data-ttu-id="d46e3-148">Certifique-se de que os dias da semana selecionados para backup e a retenção sejam alinhados.</span><span class="sxs-lookup"><span data-stu-id="d46e3-148">Be sure that the days of the week you select for backup and for retention are aligned.</span></span>
<span data-ttu-id="d46e3-149">Por exemplo, se o backup estiver definido para sábados, as políticas de retenção também deverão usar o sábado.</span><span class="sxs-lookup"><span data-stu-id="d46e3-149">For example, if your backup is set for Saturdays, the retention policies must also use Saturday.</span></span>

```yaml
Type: System.String[]
Parameter Sets: WeeklyRetentionParamSet, MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46e3-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d46e3-150">-DefaultProfile</span></span>
<span data-ttu-id="d46e3-151">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d46e3-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d46e3-152">-MonthlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="d46e3-152">-MonthlyRetentionInDailyFormat</span></span>
<span data-ttu-id="d46e3-153">Indica que esse cmdlet cria uma política mensal no formato diário.</span><span class="sxs-lookup"><span data-stu-id="d46e3-153">Indicates that this cmdlet creates a Monthly policy in Daily format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInDailyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46e3-154">-MonthlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="d46e3-154">-MonthlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="d46e3-155">Indica que esse cmdlet cria uma política mensal em formato semanal.</span><span class="sxs-lookup"><span data-stu-id="d46e3-155">Indicates that this cmdlet creates a Monthly policy in Weekly format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46e3-156">-MonthsOfYear</span><span class="sxs-lookup"><span data-stu-id="d46e3-156">-MonthsOfYear</span></span>
<span data-ttu-id="d46e3-157">Especifica quais meses do ano têm os pontos de recuperação que o backup retém anualmente.</span><span class="sxs-lookup"><span data-stu-id="d46e3-157">Specifies which months of the year have the recovery points that Backup retains on a yearly basis.</span></span>
<span data-ttu-id="d46e3-158">Os valores aceitáveis para esse parâmetro são: nomes de meses, como Janeiro ou fevereiro.</span><span class="sxs-lookup"><span data-stu-id="d46e3-158">The acceptable values for this parameter are: names of months, such as January or February.</span></span>

```yaml
Type: System.String[]
Parameter Sets: YearlyRetentionInDailyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases:
Accepted values: January, February, March, April, May, June, July, August, September, October, November, December

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46e3-159">-Retenção</span><span class="sxs-lookup"><span data-stu-id="d46e3-159">-Retention</span></span>
<span data-ttu-id="d46e3-160">Especifica o período de retenção, em dias, meses ou anos, para o qual o backup armazena um ponto de backup.</span><span class="sxs-lookup"><span data-stu-id="d46e3-160">Specifies the retention period, in days, months, or years, for which Backup stores a backup point.</span></span>
<span data-ttu-id="d46e3-161">A unidade depende se esse cmdlet seleciona uma opção de retenção diária, mensal ou anual.</span><span class="sxs-lookup"><span data-stu-id="d46e3-161">The unit depends on whether this cmdlet selects a daily, monthly, or yearly retention option.</span></span>
<span data-ttu-id="d46e3-162">Por exemplo, se especificar o parâmetro *DailyRetention* , o cmdlet interpretará o parâmetro atual como um número de dias.</span><span class="sxs-lookup"><span data-stu-id="d46e3-162">For example, if specify the *DailyRetention* parameter, the cmdlet interprets the current parameter as a number of days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46e3-163">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="d46e3-163">-WeeklyRetention</span></span>
<span data-ttu-id="d46e3-164">Indica que esse cmdlet cria uma política de retenção semanal.</span><span class="sxs-lookup"><span data-stu-id="d46e3-164">Indicates that this cmdlet creates a Weekly retention policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyRetentionParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46e3-165">-WeekNumber</span><span class="sxs-lookup"><span data-stu-id="d46e3-165">-WeekNumber</span></span>
<span data-ttu-id="d46e3-166">Especifica as semanas do mês que identificam quais pontos de recuperação o backup mantém e por quanto tempo.</span><span class="sxs-lookup"><span data-stu-id="d46e3-166">Specifies the weeks of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="d46e3-167">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d46e3-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d46e3-168">Primeiros</span><span class="sxs-lookup"><span data-stu-id="d46e3-168">First</span></span> 
- <span data-ttu-id="d46e3-169">Secundária</span><span class="sxs-lookup"><span data-stu-id="d46e3-169">Second</span></span> 
- <span data-ttu-id="d46e3-170">Terceiriza</span><span class="sxs-lookup"><span data-stu-id="d46e3-170">Third</span></span> 
- <span data-ttu-id="d46e3-171">Fourth</span><span class="sxs-lookup"><span data-stu-id="d46e3-171">Fourth</span></span> 
- <span data-ttu-id="d46e3-172">Nome</span><span class="sxs-lookup"><span data-stu-id="d46e3-172">Last</span></span>

```yaml
Type: System.String[]
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases:
Accepted values: First, Second, Third, Fourth, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46e3-173">-YearlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="d46e3-173">-YearlyRetentionInDailyFormat</span></span>
<span data-ttu-id="d46e3-174">Indica que esse cmdlet cria uma política de retenção anual em formato diário.</span><span class="sxs-lookup"><span data-stu-id="d46e3-174">Indicates that this cmdlet creates a Yearly retention policy in Daily format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInDailyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46e3-175">-YearlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="d46e3-175">-YearlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="d46e3-176">Indica que esse cmdlet cria uma política de retenção anual em formato semanal.</span><span class="sxs-lookup"><span data-stu-id="d46e3-176">Indicates that this cmdlet creates a Yearly retention policy in Weekly format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInWeeklyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46e3-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d46e3-177">CommonParameters</span></span>
<span data-ttu-id="d46e3-178">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d46e3-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d46e3-179">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d46e3-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d46e3-180">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d46e3-180">INPUTS</span></span>

### <span data-ttu-id="d46e3-181">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d46e3-181">None</span></span>

## <span data-ttu-id="d46e3-182">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d46e3-182">OUTPUTS</span></span>

### <span data-ttu-id="d46e3-183">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d46e3-183">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy</span></span>

## <span data-ttu-id="d46e3-184">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d46e3-184">NOTES</span></span>
* <span data-ttu-id="d46e3-185">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d46e3-185">None</span></span>

## <span data-ttu-id="d46e3-186">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d46e3-186">RELATED LINKS</span></span>

[<span data-ttu-id="d46e3-187">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="d46e3-187">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="d46e3-188">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d46e3-188">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


