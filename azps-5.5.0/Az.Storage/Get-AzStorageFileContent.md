---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 3c90e02194fa761bbb0fc00e11ea09d03ca00c1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110881"
---
# Get-AzStorageFileContent

## Sinopse
Baixa o conteúdo de um arquivo.

## Sintaxe

### ShareName (Padrão)
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### Compartilhar
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### Diretório
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### Arquivo
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## Descrição
O cmdlet **Get-AzStorageFileContent** baixa o conteúdo de um arquivo e o salva em um destino especificado por você.
Este cmdlet não retorna o conteúdo do arquivo.

## Exemplos

### Exemplo 1: Baixar um arquivo de uma pasta
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

Esse comando baixa um arquivo chamado CurrentDataFile na pasta ContosoWorkingFolder do compartilhamento de arquivos ContosoShare06 para a pasta atual.

### Exemplo 2: baixa os arquivos em exemplo de compartilhamento de arquivos
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

Este exemplo baixa os arquivos em exemplo de compartilhamento de arquivos

### Exemplo 3: baixe um arquivo do Azure para um arquivo local e mantenha as propriedades SMB do Arquivo do Azure (Arquivo Atribuído, Hora de Criação de Arquivo, Hora da Última Gravação do Arquivo) no arquivo local.
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

Este exemplo baixa um arquivo do Azure para um arquivo local e conserva as propriedades SMB do Arquivo do Azure (Azure File Attributtes, Tempo de Criação de Arquivo, Hora da Última Gravação do Arquivo) no arquivo local.

## Parâmetros

### -AsJob
Executar cmdlet em segundo plano.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckMd5
Especifica se você deve verificar a soma Md5 do arquivo baixado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientTimeoutPerRequest
Especifica o intervalo de tempo de tempo no lado do cliente, em segundos, para uma solicitação de serviço. Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação. Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esvaia, este cmdlet retornará um erro.

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
Especifica o máximo de chamadas de rede simultâneas. Você pode usar esse parâmetro para limitar a capacidade de limitar o uso local de CPU e largura de banda, especificando o número máximo de chamadas de rede simultâneas. O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal. Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo. O valor padrão é 10.

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
Especifica um contexto de Armazenamento do Azure. Para obter um contexto, use o New-AzStorageContext cmdlet.

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

### -Destino
Especifica o caminho de destino.
Este cmdlet baixa o conteúdo do arquivo para o local especificado por esse parâmetro.
Se você especificar o caminho de um arquivo que não existe, esse cmdlet criará esse arquivo e salvará o conteúdo no novo arquivo.
Se você especificar um caminho de um arquivo  que já existe e especificar o parâmetro Force, o cmdlet substituirá o arquivo.
Se você especificar um caminho de um arquivo existente e não especificar *Forçar,* o cmdlet solicitará antes que ele continue.
Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Directory
Especifica uma pasta como um objeto **CloudFileDirectory.**
Este cmdlet obtém conteúdo para um arquivo na pasta especificada por esse parâmetro.
Para obter um diretório, use o New-AzStorageDirectory cmdlet.
Você também pode usar o cmdlet Get-AzStorageFile para obter um diretório.

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

### -Arquivo
Especifica um arquivo como um objeto **CloudFile.**
Este cmdlet obtém o arquivo especificado por esse parâmetro.
Para obter um **objeto CloudFile,** use o cmdlet Get-AzStorageFile nuvem.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Forçar
Se você especificar o caminho de um arquivo que não existe, esse cmdlet criará esse arquivo e salvará o conteúdo no novo arquivo.
Se você especificar um caminho de um arquivo  que já existe e especificar o parâmetro Force, o cmdlet substituirá o arquivo.
Se você especificar um caminho de um arquivo existente e não especificar *Forçar,* o cmdlet solicitará antes que ele continue.
Se você especificar o caminho de uma pasta, esse cmdlet tentará criar um arquivo que tenha o nome do arquivo de armazenamento do Azure.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Indica que esse cmdlet retorna o objeto **AzureStorageFile** baixado.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Este cmdlet obtém o conteúdo do arquivo especificado por esse parâmetro.
Se o arquivo não existir, esse cmdlet retornará um erro.

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreserveSMBAttribute
Mantenha as propriedades SMB de arquivo de origem (Arquivo autribuções, Hora de Criação de Arquivo, Hora da Última Gravação do Arquivo) no Arquivo de destino. Este parâmetro só está disponível no Windows.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Especifica o intervalo de tempo de tempo de serviço, em segundos, para uma solicitação. Se o intervalo especificado se elapse antes que o serviço processe a solicitação, o serviço de armazenamento retornará um erro.

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
Este cmdlet baixa o conteúdo do arquivo no compartilhamento especificado por este parâmetro.
Para obter um **objeto CloudFileShare,** use o cmdlet Get-AzStorageShare nuvem.
Este objeto contém o contexto de armazenamento.
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
Este cmdlet baixa o conteúdo do arquivo no compartilhamento especificado por este parâmetro.

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

### -Confirmar
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que acontece se o cmdlet for executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Microsoft.Azure.Storage.File.CloudFileShare

### Microsoft.Azure.Storage.File.CloudFileDirectory

### Microsoft.Azure.Storage.File.CloudFile

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## Saídas

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile

## Notas

## LINKS RELACIONADOS

[Get-AzStorageFile](./Get-AzStorageFile.md)

[Set-AzStorageFileContent](./Set-AzStorageFileContent.md)


