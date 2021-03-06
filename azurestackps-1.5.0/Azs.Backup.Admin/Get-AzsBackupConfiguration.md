---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 500a8e28ceb4eb452d788574b8a80865b5e54b14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426009"
---
# Get-AzsBackupConfiguration

## Sinopse
Retorna a lista de configurações de backup.

## SYNTAX

### Lista (padrão)
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### Obter
```
Get-AzsBackupConfiguration [[-Location] <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### Identificação
```
Get-AzsBackupConfiguration -ResourceId <String> [<CommonParameters>]
```

## DESCRITIVO
Retorna a lista de configurações de backup.

## EXEMPLOS

### --------------------------EXEMPLO 1--------------------------
```
Get-AzsBackupConfiguration
```

Obtenha a configuração de backup do Azure Stack.

## OS

### -Local
Local de backup.

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos.

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
A ID do recurso.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Skip
Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -Início
Retorne os N principais itens conforme especificado pelo valor do parâmetro.
Aplica-se após o parâmetro-Skip.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. AzureStack. Management. backup. admin. Models. BackupLocation

## INFORMA

## LINKS RELACIONADOS

