---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: c94c9b9d04745fe22c8836be1858c59c253d4b63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432704"
---
# Get-AzureStorageContainer

## Sinopse
Lista os contêineres de armazenamento.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ContainerName (padrão)
```
Get-AzureStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### ContainerPrefix
```
Get-AzureStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureStorageContainer** lista os contêineres de armazenamento associados à conta de armazenamento no Azure.

## EXEMPLOS

### Exemplo 1: obter blob de armazenamento do Azure por nome
```
PS C:\>Get-AzureStorageContainer -Name container*
```

Este exemplo usa um caractere curinga para retornar uma lista de todos os contêineres com um nome que começa com container.

### Exemplo 2: obter contêiner de armazenamento do Azure por prefixo do nome do contêiner
```
PS C:\>Get-AzureStorageContainer -Prefix "container"
```

Este exemplo usa o parâmetro *prefix* para retornar uma lista de todos os contêineres com um nome que começa com container.

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
Especifica o contexto de armazenamento.
Para criá-la, você pode usar o cmdlet New-AzureStorageContext.

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

### -ContinuationToken
Especifica um token de continuação para a lista de BLOBs.

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxCount
Especifica o número máximo de objetos que este cmdlet retorna.

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

### -Nome
Especifica o nome do contêiner.
Se o nome do contêiner estiver vazio, o cmdlet lista todos os contêineres.
Caso contrário, ele lista todos os contêineres que correspondem ao nome especificado ou ao padrão de nome normal.

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### -Prefix
Especifica um prefixo usado no nome do contêiner ou contêineres que você deseja obter.
Você pode usar isso para localizar todos os contêineres que começam com a mesma cadeia de caracteres, como "My" ou "Test".

```yaml
Type: String
Parameter Sets: ContainerPrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.
Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.

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

### IStorageContext

O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline

### String

O parâmetro ' name ' aceita o valor do tipo ' String ' do pipeline

## EXIBE

### Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageContainer

## INFORMA

## LINKS RELACIONADOS

[New-AzureStorageContainer](./New-AzureStorageContainer.md)

[Remove-AzureStorageContainer](./Remove-AzureStorageContainer.md)

[Set-AzureStorageContainerAcl](./Set-AzureStorageContainerAcl.md)


