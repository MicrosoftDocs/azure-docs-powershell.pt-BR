---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: 8251c18acad2da881c3215df6a2e743b6804af6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116108"
---
# Get-AzStorageFile

## Sinopse
Lista diretórios e arquivos para um caminho.

## Sintaxe

### ShareName (Padrão)
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### Compartilhar
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### Diretório
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## Descrição
O **cmdlet Get-AzStorageFile** lista diretórios e arquivos para o compartilhamento ou diretório especificado por você.
*Especifique o* parâmetro Caminho para obter uma instância de um diretório ou arquivo no caminho especificado.
Este cmdlet retorna **objetos AzureStorageFile** **e AzureStorageDirectory.**
Você pode usar a propriedade **IsDirectory** para distinguir entre pastas e arquivos.

## Exemplos

### Exemplo 1: Listar diretórios em um compartilhamento
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "AzureStorageFileDirectory"}
```

Esse comando lista apenas os diretórios no compartilhamento ContosoShare06.
Primeiro, ele recupera arquivos e diretórios,  passa-os para o operador de onde usando o operador de pipeline e, em seguida, descarta todos os objetos cujo tipo não é "AzureStorageFileDirectory".

### Exemplo 2: Listar um Diretório de Arquivos
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

Esse comando lista os arquivos e pastas no diretório ContosoWorkingFolder no compartilhamento ContosoShare06.
Primeiro, ele obtém a instância de diretório e, em seguida, a pipelinea para o cmdlet **Get-AzStorageFile** para listar o diretório.

## Parâmetros

### -ClientTimeoutPerRequest
Especifica o intervalo de tempo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.
Se a chamada anterior falhar dentro do intervalo especificado, esse cmdlet recuperará a solicitação.
Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esvaia, este cmdlet retornará um erro.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Especifica o máximo de chamadas de rede simultâneas.
Você pode usar esse parâmetro para limitar a capacidade de limitar o uso local de CPU e largura de banda, especificando o número máximo de chamadas de rede simultâneas.
O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.
Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.
O valor padrão é 10.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Contexto
Especifica um contexto de Armazenamento do Azure.
Para obter um contexto de Armazenamento, use New-AzStorageContext cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Directory
Especifica uma pasta como um objeto **CloudFileDirectory.**
Este cmdlet obtém a pasta especificada por esse parâmetro.
Para obter um diretório, use o New-AzStorageDirectory cmdlet.
Você também pode usar **o cmdlet Get-AzStorageFile** para obter um diretório.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Caminho
Especifica o caminho de uma pasta.
Se você omitir *o* parâmetro Caminho, **Get-AzStorageFile** lista os diretórios e arquivos no compartilhamento de arquivos ou diretório especificado.
Se você incluir o parâmetro *Caminho,* **Get-AzStorageFile** retornará uma instância de um diretório ou arquivo no caminho especificado.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Especifica o intervalo de tempo de tempo de serviço, em segundos, para uma solicitação.
Se o intervalo especificado se elapse antes que o serviço processe a solicitação, o serviço de armazenamento retornará um erro.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Compartilhar
Especifica um **objeto CloudFileShare.**
Este cmdlet obtém um arquivo ou diretório do compartilhamento de arquivos especificado por esse parâmetro.
Para obter um **objeto CloudFileShare,** use o cmdlet Get-AzStorageShare nuvem.
Este objeto contém o contexto armazenamento.
Se você especificar esse parâmetro, não especifique o *parâmetro De* contexto.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ShareName
Especifica o nome do compartilhamento de arquivo.
Este cmdlet obtém um arquivo ou diretório do compartilhamento de arquivos especificado por esse parâmetro.

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Microsoft.Azure.Storage.File.CloudFileShare

### Microsoft.Azure.Storage.File.CloudFileDirectory

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## Saídas

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile

## Notas

## LINKS RELACIONADOS

[Get-AzStorageFileContent](./Get-AzStorageFileContent.md)

[New-AzStorageDirectory](./New-AzStorageDirectory.md)

[Remove-AzStorageDirectory](./Remove-AzStorageDirectory.md)

[Remove-AzStorageFile](./Remove-AzStorageFile.md)

[Set-AzStorageFileContent](./Set-AzStorageFileContent.md)


