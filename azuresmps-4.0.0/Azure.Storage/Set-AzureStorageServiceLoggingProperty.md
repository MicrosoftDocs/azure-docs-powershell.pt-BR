---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: ''
schema: 2.0.0
ms.openlocfilehash: dd1acb41a6f67fb281500ad8a0d37cb3c2e0a6dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426206"
---
# Set-AzureStorageServiceLoggingProperty

## Sinopse
Modifica o registro em log dos serviços de armazenamento do Azure.

## SYNTAX

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureStorageServiceLoggingProperty** modifica o registro em log dos serviços de armazenamento do Azure.

## EXEMPLOS

### Exemplo 1: modificar as propriedades de log do serviço blob
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

Esse comando modifica o log da versão 1,0 do armazenamento de BLOB para incluir operações de leitura e gravação.
O log do serviço de armazenamento do Azure retém as entradas por 10 dias.
Como esse comando especifica o parâmetro *PassThru* , o comando exibe as propriedades de registro em log modificadas.

## OS

### -Contexto
Especifica um contexto de armazenamento do Azure.
Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -LoggingOperations
Especifica uma matriz de operações do serviço de armazenamento do Azure.
O Azure Storage Services registra as operações que esse parâmetro especifica.
Os valores aceitáveis para esse parâmetro são:

- Nenhuma
- Ler
- Gravação
- Remover
- Todo

```yaml
Type: LoggingOperations[]
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Indica que esse cmdlet retorna as propriedades de log atualizadas.
Se você não especificar esse parâmetro, esse cmdlet não retornará um valor.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetentionDays
Especifica o número de dias durante os quais o serviço de armazenamento do Azure mantém as informações registradas.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceType
Especifica o tipo de serviço de armazenamento.
Esse cmdlet modifica as propriedades de log do tipo de serviço que esse parâmetro especifica.
Os valores aceitáveis para esse parâmetro são:

- Irregular 
- TableName
- Coloca
- Arquivos

Não há suporte para o valor do arquivo no momento.

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Versão
Especifica a versão do log do serviço de armazenamento do Azure.
O valor padrão é 1,0.

```yaml
Type: Double
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

[Get-AzureStorageServiceLoggingProperty](./Get-AzureStorageServiceLoggingProperty.md)

[New-AzureStorageContext](./New-AzureStorageContext.md)


