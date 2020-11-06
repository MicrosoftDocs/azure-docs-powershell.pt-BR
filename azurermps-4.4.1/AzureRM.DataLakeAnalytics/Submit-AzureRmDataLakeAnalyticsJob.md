---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: bb0ad536d738facdfe50bc7983517f4505ab4ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432236"
---
# Submit-AzureRmDataLakeAnalyticsJob

## Sinopse
Envia um trabalho.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Enviar trabalho com caminho de script para U-SQL
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Enviar o trabalho U-SQL
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Enviar trabalho com caminho de script para o U-SQL com informações reucurrence
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Enviar o trabalho U-SQL com informações de recorrência
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Enviar trabalho com caminho de script para U-SQL com reucurrence e informações de pipeline
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Enviar o trabalho U-SQL com informações de recorrência e pipeline
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Submit-AzureRmDataLakeAnalyticsJob** envia um trabalho do Azure data Lake Analytics.

## EXEMPLOS

### Exemplo 1: enviar um trabalho
```
PS C:\>Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -DegreeOfParallelism 32
```

Esse comando envia um trabalho do data Lake Analytics.

## OS

### -Conta
Especifica o nome da conta do data Lake Analytics.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Comcompilemode
Especifica o modo de compilação do trabalho.
Os valores aceitáveis para esse parâmetro são:

- Semântico
- Integral
- SingleBox

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Semantic, Full, SingleBox

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CompileOnly
Indica que esse cmdlet compila o trabalho sem executá-lo.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DegreeOfParallelism
Especifica as unidades de análise de data Lake (DLAU) do trabalho, que indica o paralelismo máximo permitido do trabalho.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome do trabalho.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pipelineid
Uma ID que indica que o envio desse trabalho é parte de um conjunto de trabalhos recorrentes e também associado a um pipeline de trabalho.

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pipelinename
Um nome amigável opcional para o pipeline associado a esse trabalho.

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PipelineUri
Um URI opcional que se vincula ao serviço de origem associado a esse pipeline.

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Priority
Especifica a prioridade do trabalho.
Se não for especificado, a prioridade será 1000.
Um número baixo indica uma prioridade de trabalho mais alta.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecurrenceType
Uma ID que indica o envio desse trabalho é uma parte de um conjunto de trabalhos recorrentes com a mesma ID de recorrência.

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecurrenceType
Um nome amigável opcional para a correlação de recorrência entre trabalhos.

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RunId
Uma ID que identifica essa iteração de execução específica do pipeline.

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Runtime
Especifica a versão do tempo de execução do trabalho.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Script
Especifica o conteúdo do script a ser executado.

```yaml
Type: System.String
Parameter Sets: Submit U-SQL Job, Submit U-SQL Job with recurrence information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ScriptPath
Especifica o caminho do arquivo local para o script a ser executado.

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL, Submit job with script path for U-SQL with reucurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### String
O parâmetro ' script ' aceita o valor do tipo ' String ' do pipeline

## EXIBE

### JobInformation
Os detalhes iniciais do trabalho para o trabalho enviado.

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmDataLakeAnalyticsJob](./Get-AzureRmDataLakeAnalyticsJob.md)

[Parar-AzureRmDataLakeAnalyticsJob](./Stop-AzureRmDataLakeAnalyticsJob.md)

[Wait-AzureRmDataLakeAnalyticsJob](./Wait-AzureRmDataLakeAnalyticsJob.md)


