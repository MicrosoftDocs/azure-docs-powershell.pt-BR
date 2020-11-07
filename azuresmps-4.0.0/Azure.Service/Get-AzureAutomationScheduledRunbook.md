---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2F66B0F2-37F3-4046-9FB0-B8C4B90D84A3
online version: ''
schema: 2.0.0
ms.openlocfilehash: d03364038a7a0563e5a8ab2f2f88d36b24da0ebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946357"
---
# Get-AzureAutomationScheduledRunbook

## Sinopse

Obtém os runbooks de automação do Azure e os cronogramas associados.

## SYNTAX

### ByAll (padrão)
```
Get-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByJobScheduleId
```
Get-AzureAutomationScheduledRunbook -JobScheduleId <Guid> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRunbookName
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRunbookNameAndScheduleName
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByScheduleName
```
Get-AzureAutomationScheduledRunbook -ScheduleName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

**Get-AzureAutomationScheduledRunbook** Obtém um ou mais Runbooks de automação do Azure e cronogramas associados.
Por padrão, todos os runbooks programados são retornados.

Para obter um runbook agendado específico, especifique o nome do runbook e o nome do cronograma.
Para obter todos os cronogramas associados a um runbook, especifique apenas o nome do runbook.
Para obter todos os runbooks associados a um cronograma, especifique apenas o nome do cronograma.

## EXEMPLOS

### Exemplo 1: obter todos os runbooks agendados
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17"
```

Esse comando obtém todos os runbooks agendados na conta de automação chamada Contoso17.

### Exemplo 2: obter todos os cronogramas associados a um runbook
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -RunbookName "Runbk01"
```

Esse comando obtém todos os runbooks agendados para o runbook Runbk01 na conta de automação chamada Contoso17.

### Exemplo 3: obter todos os runbooks associados a um cronograma
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ScheduleName "Schedule01"
```

Esse comando obtém todos os runbooks agendados para o cronograma Schedule01 na conta de automação chamada Contoso17.

## OS

### -AutomationAccountName
Especifica o nome de uma conta de automação do Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobScheduleId
Especifica a ID de um trabalho agendado.

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê.
Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunbookName
Especifica o nome de um runbook.

```yaml
Type: String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScheduleName
Especifica o nome de um cronograma.

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. Azure. Commands. Automation. Model. JobSchedule

## INFORMA

## LINKS RELACIONADOS

[Register-AzureAutomationScheduledRunbook](./Register-AzureAutomationScheduledRunbook.md)

[Cancelar registro-AzureAutomationScheduledRunbook](./Unregister-AzureAutomationScheduledRunbook.md)


