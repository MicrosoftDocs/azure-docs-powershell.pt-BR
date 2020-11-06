---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: e233c523e5fd9372b1e7dd86b5b5e73eb3f7091e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425848"
---
# Disable-AzureRmDataCollection

## Sinopse
Opta pela coleta de dados para melhorar os cmdlets do AzurePowerShell. Os dados não são coletados, a menos que você explicitamente opte por você.

## SYNTAX

```
Disable-AzureRmDataCollection [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
Você pode melhorar a experiência de usar o Microsoft Cloud e o PowerShell do Azure, optando pela coleta de dados.
O PowerShell do Azure não coleta dados sem o seu consentimento-você deve optar explicitamente por meio da execução de Enable-AzureRmDataCollection ou respondendo Sim quando o PowerShell do Azure solicitar a coleta de dados na primeira vez que você executar um cmdlet.
A Microsoft agrega dados coletados para identificar padrões de uso, identificar problemas comuns e melhorar a experiência de usar o PowerShell do Azure.
O Microsoft Azure PowerShell não coleta dados particulares nem qualquer informação que possa identificá-lo pessoalmente.

Execute o cmdlet Disable-AzureRMDataCollection para desabilitar a coleta de dados para o usuário atual.
Isso impedirá que o usuário atual seja avisado sobre a coleta de dados na primeira vez que cmdlets são executados.

Para habilitar a coleta de dados para o usuário atual, execute o cmdlet Enable-AzureRmDataCollection.

## EXEMPLOS

### Exemplo 1: desabilitando a coleta de dados para o usuário atual
```
PS C:\> Disable-AzureRmDataCollection
```

Este exemplo mostra como desabilitar a coleta de dados para o usuário atual. 

## OS

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### Nenhuma

## INFORMA

## LINKS RELACIONADOS

[Enable-AzureRmDataCollection]()

