---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2BF5BDF8-3743-46FC-8E04-1A4EA920A2AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77b4d184ffbdb1d054f3d14aa3c51c8d2afc928b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946310"
---
# Get-AzureSchedulerJobHistory

## Sinopse
Obtém o histórico de um trabalho do Agendador.

## SYNTAX

```
Get-AzureSchedulerJobHistory -Location <String> -JobCollectionName <String> -JobName <String>
 [-JobStatus <String>] [-Profile <AzureSMProfile>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## DESCRITIVO
Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.
Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

O cmdlet **Get-AzureSchedulerJobHistory** Obtém o histórico de um trabalho do Agendador.

## EXEMPLOS

### Exemplo 1: obter histórico de um trabalho usando seu nome
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

Esse comando obtém o histórico do trabalho chamado Job01.
Esse trabalho pertence à coleção de trabalhos chamada JobCollection01 no local especificado.

### Exemplo 2: obter histórico de um trabalho com falha usando seu nome
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job12" -JobStatus "Failed"
```

Esse comando obtém o histórico do trabalho chamado Job12 que tem um status de falha.
Esse trabalho pertence à coleção de trabalhos chamada JobCollection01 no local especificado.

## OS

### -Primeiro
Obtém apenas o número especificado de objetos.
Digite o número de objetos a serem obtidos.

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeTotalCount
Relata o número total de objetos no conjunto de dados (um número inteiro) seguido pelos objetos selecionados.
Se o cmdlet não puder determinar a contagem total, ele exibirá "contagem total desconhecida". O inteiro tem uma propriedade exactidão que indica a confiabilidade do valor total de contagem.
O valor de precisão varia de 0,0 a 1,0, onde 0,0 significa que o cmdlet não pôde contar os objetos, 1,0 significa que a contagem é exata e um valor entre 0,0 e 1,0 indica uma estimativa mais confiável.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobCollectionName
Especifica o nome de um conjunto de trabalhos do Agendador.
Esse cmdlet obtém o histórico de um trabalho que pertence à coleção que esse parâmetro especifica.

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

### -JobName
Especifica o nome de um trabalho do Agendador para o qual obter o histórico.

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

### -JobStatus
Especifica o status do trabalho do Agendador para o qual obter o histórico.
Os valores aceitáveis para esse parâmetro são:

- Feito
- Conseguiu

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

### -Skip
Ignora o número especificado de objetos e obtém os objetos restantes.
Digite o número de objetos a serem ignorados.

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureSchedulerJob](./Get-AzureSchedulerJob.md)

[Get-AzureSchedulerJobCollection](./Get-AzureSchedulerJobCollection.md)


