---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjobrecurrence
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: 34d2921526f54e20697a11cf17708fef50e49fc2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428956"
---
# Get-AzureRmDataLakeAnalyticsJobRecurrence

## Sinopse
Obtém uma recorrência ou recorrências de trabalho do data Lake Analytics.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### GetAllInAccount (padrão)
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetBySpecificJobRecurrence
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
**Get-AzureRmDataLakeAnalyticsJobRecurrence** Obtém uma recorrência de trabalho do Azure data Lake Analytics especificada ou uma lista de recorrência.

## EXEMPLOS

### Exemplo 1: obter uma recorrência especificada
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

Este comando obtém a recorrência do trabalho especificado com a ID ' 83cb7ad2-3523-4b82-b909-d478b0d8aea3 ' na conta ' contosoadla '.

### Exemplo 2: obter uma lista de todas as recorrências na conta
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

Esse comando obtém uma lista de todas as recorrências na conta "contosoadla"

## OS

### -Conta
Nome do nome da conta do data Lake Analytics sob a qual deseja recuperar a recorrência do trabalho.

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

### -RecurrenceType
ID da recorrência de trabalho específica para a qual as informações são retornadas.

```yaml
Type: Guid
Parameter Sets: GetBySpecificJobRecurrence
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -SubmittedAfter
Um filtro opcional que retorna as recorrências de trabalho somente enviadas após a hora especificada.

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubmittedBefore
Um filtro opcional que retorna as recorrências de trabalho somente enviadas antes do tempo especificado.

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String
System. GUID

## EXIBE

### Microsoft. Azure. Commands. DataLakeAnalytics. Models. PSJobRecurrenceInformation

## INFORMA

## LINKS RELACIONADOS

