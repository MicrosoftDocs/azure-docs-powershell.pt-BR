---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e816d29784ea8b2e69ba4b36162938f7a82007d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426142"
---
# Get-AzureStorageShare

## Sinopse
Obtém uma lista de compartilhamentos de arquivos.

## SYNTAX

### MatchingPrefix (padrão)
```
Get-AzureStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### Especifica
```
Get-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureStorageShare** Obtém uma lista de compartilhamentos de arquivos para uma conta de armazenamento.

## EXEMPLOS

### Exemplo 1: obter um compartilhamento de arquivos
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06"
```

Esse comando obtém o compartilhamento de arquivos chamado ContosoShare06.

### Exemplo 2: obter todos os compartilhamentos de arquivos que começam com uma cadeia de caracteres
```
PS C:\>Get-AzureStorageShare -Prefix "Contoso"
```

Esse comando obtém todos os compartilhamentos de arquivos que têm nomes que começam com contoso.

### Exemplo 3: obter todos os compartilhamentos de arquivos em um contexto especificado
```
PS C:\>$Context = New-AzureStorageContext -Local
PS C:\> Get-AzureStorageShare -Context $Context
```

O primeiro comando usa o cmdlet **New-AzureStorageContext** para criar um contexto usando o parâmetro *local* e, em seguida, armazena esse objeto Context na variável $Context.

O segundo comando obtém os compartilhamentos de arquivos para o objeto de contexto armazenado em $Context.

## OS

### -ClientTimeoutPerRequest
Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.
Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.
Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.

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

### -ConcurrentTaskCount
Especifica o número máximo de chamadas de rede simultâneas.
Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.
O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.
Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.
O valor padrão é 10.

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

### -Contexto
Especifica um contexto de armazenamento do Azure.
Para obter um contexto, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .

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

### -Nome
Especifica o nome do compartilhamento de arquivos.
Esse cmdlet obtém o compartilhamento de arquivo que esse parâmetro especifica ou nada se você especificar o nome de um compartilhamento de arquivos que não existe.

```yaml
Type: String
Parameter Sets: Specific
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Prefix
Especifica o prefixo dos compartilhamentos de arquivos.
Esse cmdlet obtém os compartilhamentos de arquivos que correspondem ao prefixo que esse parâmetro especifica, ou nenhum compartilhamento de arquivos se nenhum compartilhamento de arquivos corresponder ao prefixo especificado.

```yaml
Type: String
Parameter Sets: MatchingPrefix
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[New-AzureStorageShare](./New-AzureStorageShare.md)

[Remove-AzureStorageShare](./Remove-AzureStorageShare.md)
