---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
ms.openlocfilehash: 1dc1e95e2ecf085faad664f624e7595acd9ab607
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430588"
---
# Get-AzureStorageFileContent

## Sinopse
Baixa o conteúdo de um arquivo.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Nome_do_compartilhamento (padrão)
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Compartilhar
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Diretório
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Arquivos
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureStorageFileContent** faz o download do conteúdo de um arquivo e, em seguida, o salva em um destino que você especificar.
Esse cmdlet não retorna o conteúdo do arquivo.

## EXEMPLOS

### Exemplo 1: baixar um arquivo de uma pasta
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

Esse comando baixa um arquivo chamado CurrentDataFile na pasta ContosoWorkingFolder do compartilhamento de arquivos ContosoShare06 para a pasta atual.

### Exemplo 2: baixar os arquivos em compartilhamento de arquivo de exemplo
```
PS C:\>Get-AzureStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzureStorageFileContent
```

Este exemplo baixa os arquivos em um exemplo de compartilhamento de arquivo

## OS

### -CheckMd5
Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.
Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.
Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.

Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.

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

### -ClientTimeoutPerRequest
Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.
Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.
Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.

Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.

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
Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.
Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.
Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.

Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.

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
Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.
Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.
Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.

Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.

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

### -Destino
Especifica o caminho de destino.
Esse cmdlet baixa o conteúdo do arquivo para o local que esse parâmetro especifica.

Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.
Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.
Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.

Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Diretório
Especifica uma pasta como um objeto **CloudFileDirectory** .
Esse cmdlet obtém conteúdo para um arquivo na pasta que esse parâmetro especifica.
Para obter um diretório, use o cmdlet New-AzureStorageDirectory.
Você também pode usar o cmdlet Get-AzureStorageFile para obter um diretório.

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

### -Arquivo
Especifica um arquivo como um objeto **cloudfile** .
Esse cmdlet obtém o arquivo que esse parâmetro especifica.
Para obter um objeto **cloudfile** , use o cmdlet Get-AzureStorageFile.

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.
Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.
Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.

Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.

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

### -PassThru
Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.
Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.
Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.

Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.

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

### -Caminho
Especifica o caminho de um arquivo.
Esse cmdlet obtém o conteúdo do arquivo que esse parâmetro especifica.
Se o arquivo não existir, esse cmdlet retornará um erro.

```yaml
Type: String
Parameter Sets: ShareName, Share, Directory
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Se você especificar o caminho de um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo no novo arquivo.
Se você especificar um caminho para um arquivo que já existe e especificar o parâmetro *Force* , o cmdlet substituirá o arquivo.
Se você especificar um caminho para um arquivo existente e não especificar *forçar* , o cmdlet o solicitará antes de continuar.

Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.

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
Esse cmdlet baixa o conteúdo do arquivo no compartilhamento que esse parâmetro especifica.
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
Esse cmdlet baixa o conteúdo do arquivo no compartilhamento que esse parâmetro especifica.

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
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

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

### IStorageContext

O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline

### CloudFileDirectory

O parâmetro ' Directory ' aceita o valor do tipo ' CloudFileDirectory ' da pipeline

### Cloudfile

O parâmetro ' file ' aceita o valor do tipo ' Cloudfile ' do pipeline

### CloudFileShare

O parâmetro ' Share ' aceita o valor do tipo ' CloudFileShare ' da pipeline

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureStorageFile](./Get-AzureStorageFile.md)

[Set-AzureStorageFileContent](./Set-AzureStorageFileContent.md)


