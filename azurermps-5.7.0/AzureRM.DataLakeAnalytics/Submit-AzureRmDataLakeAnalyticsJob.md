---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/submit-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: fc09560bca0d825cc65d8a4f964119cd50898190
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427572"
---
# Submit-AzureRmDataLakeAnalyticsJob

## Sinopse
Envia um trabalho.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### SubmitUSqlJobWithScriptPath
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SubmitUSqlJob
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SubmitUSqlJobWithScriptPathAndRecurrence
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubmitUSqlJobWithRecurrence
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubmitUSqlJobWithScriptPathAndPipeline
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 -PipelineId <Guid> [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubmitUSqlJobWithPipeline
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 -PipelineId <Guid> [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Submit-AzureRmDataLakeAnalyticsJob** envia um trabalho do Azure data Lake Analytics.

## EXEMPLOS

### Exemplo 1: enviar um trabalho
```
PS C:\>Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

Esse comando envia um trabalho do data Lake Analytics.

### Exemplo 2: enviar um trabalho com parâmetros de script
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

Os parâmetros de script U-SQL são anexados acima do conteúdo principal do script, por exemplo:

DECLARE @Department String = "Sales"; DECLARAR @NumRecords int = 1000; DECLARAR @StartDateTime DateTime = novo DateTime (2017, 12, 6, 0, 0, 0, 0);

## OS

### -Conta
Nome da conta do data Lake Analytics na qual o trabalho será enviado.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Comcompilemode
O tipo de compilação a ser feita neste trabalho. Valores válidos: 

- Semântica (executa verificações semânticas e verificações de integridade necessárias)
- Completo (compilação completa)
- SingleBox (compilação completa realizada localmente)

```yaml
Type: String
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
Indica que o envio só deve compilar o trabalho e não executar se definido como true.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -AnalyticsUnits
As unidades de análise a serem usadas para esse trabalho. Geralmente, mais unidades de análise dedicadas a um script resultam em um tempo de execução de script mais rápido.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: DegreeOfParallelism

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
O nome amigável do trabalho a ser enviado.

```yaml
Type: String
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
Type: Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
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
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
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
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Priority
A prioridade do trabalho. Se não for especificado, a prioridade será 1000. Um número menor indica uma prioridade de trabalho mais alta.

```yaml
Type: Int32
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
Type: Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
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
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
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
Type: Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Runtime
Opcionalmente, defina a versão do tempo de execução para usar para o trabalho. Se esquerda não definida, o tempo de execução padrão será usado.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Script
Script para executar (Inline embutido).

```yaml
Type: String
Parameter Sets: SubmitUSqlJob, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithPipeline
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ScriptParameter
Os parâmetros de script para esse trabalho, como um dicionário de nomes de parâmetro (cadeia de caracteres) para valores (qualquer combinação de byte, SByte, int, uint (ou UInt32), Long, ULong (ou UInt64), float, Double, DateTime, bool, GUID ou byte []) (ou UInt16), Char, String, DateTime, bool, GUID ou byte [])

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScriptPath
Caminho para o arquivo de script a ser enviado.

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPath, SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithScriptPathAndPipeline
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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


