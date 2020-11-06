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
# New-AzureRmBackupRetentionPolicyObject

## Sinopse
Cria uma política de retenção de backup.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### DailyRetentionParamSet
```
New-AzureRmBackupRetentionPolicyObject [-DailyRetention] -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WeeklyRetentionParamSet
```
New-AzureRmBackupRetentionPolicyObject [-WeeklyRetention] -DaysOfWeek <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### MonthlyRetentionInDailyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### MonthlyRetentionInWeeklyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### YearlyRetentionInDailyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -MonthsOfYear <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### YearlyRetentionInWeeklyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -MonthsOfYear <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmBackupRetentionPolicyObject** cria uma política de retenção de backup do Azure.
Uma política de retenção define por quanto tempo o backup mantém um ponto de recuperação.
Os tipos de retenção são os seguintes: 

- Daily 
- Mensal 
- Mensal 
- Anual 

Crie uma política de retenção para cada tipo de retenção que você planeja usar.

Uma política de backup está associada a pelo menos uma política de retenção.
Para criar uma política de backup, use o cmdlet New-AzureRmBackupProtectionPolicy.
Em vez disso, você pode fornecer uma política de retenção para o cmdlet Enable-AzureRmBackupProtection.

## EXEMPLOS

### Exemplo 1: criar uma política de retenção para retenção diária
```
PS C:\>$Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Daily
RetentionType      Retention          RetentionTimes
-------------      ---------          --------------
Daily              30
```

O primeiro comando cria uma política de retenção por 30 dias de retenção diária e, em seguida, armazena-a na variável $Daily.

O segundo comando exibe o conteúdo de $Daily.

### Exemplo 2: criar uma política de retenção mensal
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

O primeiro comando cria uma política de retenção que mantém o backup no décimo e no vigésimo de cada mês por 12 meses.
O comando armazena a política de retenção na variável $Monthly.

O segundo comando exibe o conteúdo de $Monthly.

## OS

### -DailyRetention
Indica que esse cmdlet cria uma política de retenção diária.

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

### -DaysOfMonth
Especifica os dias do mês que identificam quais pontos de recuperação o backup mantém e por quanto tempo.
Os valores aceitáveis para esse parâmetro são: inteiros de 1 a 28 e sobrenome.
Especifique esse parâmetro se especificar os parâmetros *DailyRetention* , *MonthlyRetentionInDailyFormat* e *YearlyRetentionInDailyFormat* .

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

### -DaysOfWeek
Especifica uma matriz de dias da semana.
Os dias em que esse cmdlet especifica identificar quais pontos de recuperação o backup manterá e por quanto tempo.
Os valores aceitáveis para esse parâmetro são:

- Sexta 
- - 
- Feira 
- Terça 
- Às 
- Sábado 
- Domingo

Especifique esse parâmetro se especificar os parâmetros *WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* e *YearlyRetentionInWeeklyFormat* .

Certifique-se de que os dias da semana selecionados para backup e a retenção sejam alinhados.
Por exemplo, se o backup estiver definido para sábados, as políticas de retenção também deverão usar o sábado.

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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### -MonthlyRetentionInDailyFormat
Indica que esse cmdlet cria uma política mensal no formato diário.

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

### -MonthlyRetentionInWeeklyFormat
Indica que esse cmdlet cria uma política mensal em formato semanal.

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

### -MonthsOfYear
Especifica quais meses do ano têm os pontos de recuperação que o backup retém anualmente.
Os valores aceitáveis para esse parâmetro são: nomes de meses, como Janeiro ou fevereiro.

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

### -Retenção
Especifica o período de retenção, em dias, meses ou anos, para o qual o backup armazena um ponto de backup.
A unidade depende se esse cmdlet seleciona uma opção de retenção diária, mensal ou anual.
Por exemplo, se especificar o parâmetro *DailyRetention* , o cmdlet interpretará o parâmetro atual como um número de dias.

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

### -WeeklyRetention
Indica que esse cmdlet cria uma política de retenção semanal.

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

### -WeekNumber
Especifica as semanas do mês que identificam quais pontos de recuperação o backup mantém e por quanto tempo.
Os valores aceitáveis para esse parâmetro são:

- Primeiros 
- Secundária 
- Terceiriza 
- Fourth 
- Nome

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

### -YearlyRetentionInDailyFormat
Indica que esse cmdlet cria uma política de retenção anual em formato diário.

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

### -YearlyRetentionInWeeklyFormat
Indica que esse cmdlet cria uma política de retenção anual em formato semanal.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### AzureRmBackupRetentionPolicy

## INFORMA
* Nenhuma

## LINKS RELACIONADOS

[Enable-AzureRmBackupProtection](./Enable-AzureRmBackupProtection.md)

[New-AzureRmBackupProtectionPolicy](./New-AzureRmBackupProtectionPolicy.md)


