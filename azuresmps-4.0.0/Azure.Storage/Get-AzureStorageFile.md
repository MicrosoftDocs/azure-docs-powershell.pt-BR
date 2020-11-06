---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d3b84deae0307114efa274cdfa6fc708d1b268ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426158"
---
# Get-AzureStorageFile

## Sinopse
Lista os diretórios e arquivos de um caminho.

## SYNTAX

### Nome_do_compartilhamento (padrão)
```
Get-AzureStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### Compartilhar
```
Get-AzureStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### Diretório
```
Get-AzureStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureStorageFile** lista os diretórios e arquivos do compartilhamento ou do diretório que você especificar.
Especifique o parâmetro *path* para obter uma instância de um diretório ou arquivo no caminho especificado.

Esse cmdlet retorna objetos **AzureStorageFile** e **AzureStorageDirectory** .
Você pode usar a propriedade **IsDirectory** para distinguir entre pastas e arquivos.

## EXEMPLOS

### Exemplo 1: listar diretórios em um compartilhamento
```
PS C:\>Get-AzureStorageFile -ShareName "share1" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

Esse comando lista apenas as pastas no compartilhamento ContosoShare06.
Ele primeiro recupera arquivos e diretórios, passa-os para o operador **Where** usando o operador pipeline e, em seguida, descarta todos os objetos cujo tipo não é "CloudFileDirectory".

### Exemplo 2: listar um diretório de arquivos
```
PS C:\> Get-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzureStorageFile
```

Esse comando lista os arquivos e pastas no diretório ContosoWorkingFolder sob o compartilhamento ContosoShare06.
Primeiro, ele obtém a instância do diretório e, em seguida, a canaliza para o cmdlet **Get-AzureStorageFile** para listar o diretório.

## OS

### -ClientTimeoutPerRequest
Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.
Se a chamada anterior falhar dentro do intervalo especificado, esse cmdlet tentará novamente a solicitação.
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
Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Diretório
Especifica uma pasta como um objeto **CloudFileDirectory** .
Esse cmdlet obtém a pasta que esse parâmetro especifica.
Para obter um diretório, use o cmdlet New-AzureStorageDirectory.
Você também pode usar o cmdlet **Get-AzureStorageFile** para obter um diretório.

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Caminho
Especifica o caminho de uma pasta.

Se você omitir o parâmetro *Path* , **Get-AzureStorageFile** lista as pastas e arquivos no compartilhamento de arquivos ou diretório especificado.
Se você incluir o parâmetro *Path* , **Get-AzureStorageFile** retornará uma instância de um diretório ou arquivo no caminho especificado.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Especifica o intervalo de tempo limite do lado do serviço, em segundos, para uma solicitação.
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

### -Compartilhar
Especifica um objeto **CloudFileShare** .
Esse cmdlet obtém um arquivo ou diretório do compartilhamento de arquivos que esse parâmetro especifica.
Para obter um objeto **CloudFileShare** , use o cmdlet Get-AzureStorageShare.
Esse objeto contém o contexto de armazenamento.
Se você especificar esse parâmetro, não especifique o parâmetro *Context* .

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ShareName
Especifica o nome do compartilhamento de arquivos.
Esse cmdlet obtém um arquivo ou diretório do compartilhamento de arquivos que esse parâmetro especifica.

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
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

[Get-AzureStorageFileContent](./Get-AzureStorageFileContent.md)

[New-AzureStorageDirectory](./New-AzureStorageDirectory.md)

[Remove-AzureStorageDirectory](./Remove-AzureStorageDirectory.md)

[Remove-AzureStorageFile](./Remove-AzureStorageFile.md)

[Set-AzureStorageFileContent](./Set-AzureStorageFileContent.md)


