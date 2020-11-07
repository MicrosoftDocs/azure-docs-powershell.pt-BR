---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 89B28B7C-CA61-4CAB-A4DD-69363AB48A65
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a33739cfad37269fc2f91654e82d6ea36eb2336
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945612"
---
# Get-AzureSchedulerJobCollection

## Sinopse
Obtém coletas de trabalho do Agendador.

## SYNTAX

```
Get-AzureSchedulerJobCollection [-Location <String>] [-JobCollectionName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## DESCRITIVO
Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.
Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

O cmdlet **Get-AzureSchedulerJobCollection** Obtém uma ou mais coleções de trabalho do Agendador.

## EXEMPLOS

### Exemplo 1: obter todas as coleções
```
PS C:\> Get-AzureSchedulerJobCollection
```

Este comando obtém todas as coleções de trabalhos do Agendador em todos os locais da assinatura atual.

### Exemplo 2: obter todas as coleções para um local
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US"
```

Esse comando obtém todas as coleções de trabalhos do Agendador no local chamado norte central dos EUA.

### Exemplo 3: obter uma coleção usando um nome
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

Esse comando obtém o conjunto de trabalhos do Agendador chamado JobCollection01.

## OS

### -JobCollectionName
Especifica o nome da coleção de trabalhos do Agendador a ser obtida.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Local
Especifica o nome do local que hospeda o serviço na nuvem.
Os valores válidos são: 

- Qualquer lugar da Ásia
- Em qualquer lugar da Europa
- Em qualquer lugar nos EUA
- Leste da Ásia
- Leste dos EUA
- Centro Norte dos EUA
- Norte da Europa
- Centro-Sul dos EUA
- Sudeste Asiático
- Oeste da Europa
- Oeste dos EUA

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[New-AzureSchedulerJobCollection](./New-AzureSchedulerJobCollection.md)

[Remove-AzureSchedulerJobCollection](./Remove-AzureSchedulerJobCollection.md)

[Set-AzureSchedulerJobCollection](./Set-AzureSchedulerJobCollection.md)


