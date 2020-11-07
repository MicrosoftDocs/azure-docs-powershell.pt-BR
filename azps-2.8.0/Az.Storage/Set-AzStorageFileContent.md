---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
ms.openlocfilehash: 4bec3773b4446e7467346acd4701fbe75298eac5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774294"
---
# Set-AzStorageFileContent

## Sinopse
Carrega o conteúdo de um arquivo.

## SYNTAX

### Nome_do_compartilhamento (padrão)
```
Set-AzStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### Compartilhar
```
Set-AzStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### Diretório
```
Set-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzStorageFileContent** carrega o conteúdo de um arquivo em um arquivo em um compartilhamento especificado.

## EXEMPLOS

### Exemplo 1: carregar um arquivo na pasta atual
```
PS C:\>Set-AzStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

Esse comando carrega um arquivo chamado DataFile37 na pasta atual como um arquivo chamado CurrentDataFile na pasta denominada ContosoWorkingFolderme.

### Exemplo 2: carregar todos os arquivos na pasta atual
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

Este exemplo usa vários cmdlets comuns do Windows PowerShell e o cmdlet atual para carregar todos os arquivos da pasta atual para a pasta raiz do contêiner ContosoShare06.
O primeiro comando obtém o nome da pasta atual e a armazena na variável $CurrentFolder.
O segundo comando usa o cmdlet **Get-AzStorageShare** para obter o compartilhamento de arquivos chamado ContosoShare06 e, em seguida, armazena-o na variável $container.
O comando final Obtém o conteúdo da pasta atual e passa cada um para o cmdlet Where-Object usando o operador pipeline.
Esse cmdlet filtra objetos que não são arquivos e, em seguida, passa os arquivos para o cmdlet ForEach-Object.
Esse cmdlet executa um bloco de script para cada arquivo que cria o caminho apropriado para ele e, em seguida, usa o cmdlet atual para carregar o arquivo.
O resultado tem o mesmo nome e a mesma posição relativa em relação aos outros arquivos que este exemplo carrega.
Para obter mais informações sobre blocos de script, digite `Get-Help about_Script_Blocks` .

### Exemplo 3: carregue um arquivo local em um arquivo do Azure e perpreserve as propriedades SMB do arquivo local (arquivo Attributtes, hora da criação do arquivo, hora da última gravação do arquivo) no arquivo do Azure.
```
PS C:\>Get-AzStorageFileContent -source $localFilePath -ShareName sample -Path "dir1/file1" -PreserveSMBAttribute
```

Este exemplo carrega um arquivo local em um arquivo do Azure e perservindo as propriedades SMB do arquivo local (arquivo Attributtes, hora da criação do arquivo, hora da última gravação do arquivo) no arquivo do Azure.

## OS

### -AsJob
Execute o cmdlet em segundo plano.

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
Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.
Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.
Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.

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
Especifica o número máximo de chamadas de rede simultâneas.
Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.
O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.
Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.
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
Especifica um contexto de armazenamento do Azure.
Para obter um contexto de armazenamento, use o cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .

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
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -Diretório
Especifica uma pasta como um objeto **CloudFileDirectory** .
Esse cmdlet carrega o arquivo para a pasta que esse parâmetro especifica.
Para obter um diretório, use o cmdlet New-AzStorageDirectory.
Você também pode usar o cmdlet Get-AzStorageFile para obter um diretório.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
Indica que esse cmdlet substitui um arquivo de armazenamento do Azure existente.

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
Indica que esse cmdlet retorna o objeto **AzureStorageFile** que ele cria ou carrega.

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
Especifica o caminho de um arquivo ou pasta.
Esse cmdlet carrega o conteúdo para o arquivo que esse parâmetro especifica ou para um arquivo na pasta que esse parâmetro especifica.
Se você especificar uma pasta, esse cmdlet criará um arquivo com o mesmo nome do arquivo de origem.
Se você especificar um caminho para um arquivo que não existe, esse cmdlet cria esse arquivo e salva o conteúdo nesse arquivo.
Se você especificar um arquivo que já existe e especificar o parâmetro _Force_ , esse cmdlet substituirá o conteúdo do arquivo.
Se você especificar um arquivo que já existe e não especificar _Force_ , esse cmdlet não fará nenhuma alteração e retornará um erro.
Se você especificar um caminho para uma pasta que não existe, esse cmdlet não fará nenhuma alteração e retornará um erro.

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

### -PreserveSMBAttribute
Mantenha as propriedades SMB do arquivo de origem (arquivo Attributtes, hora da criação do arquivo, hora da última gravação do arquivo) no arquivo de destino. Este parâmetro só está disponível no Windows.

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
Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.

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
Especifica um objeto **CloudFileShare** .
Esse cmdlet é carregado em um arquivo no compartilhamento de arquivos que esse parâmetro especifica.
Para obter um objeto **CloudFileShare** , use o cmdlet Get-AzStorageShare.
Esse objeto contém o contexto de armazenamento.
Se você especificar esse parâmetro, não especifique o parâmetro *Context* .

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
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
Esse cmdlet é carregado em um arquivo no compartilhamento de arquivos que esse parâmetro especifica.

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

### -Fonte
Especifica o arquivo de origem que esse cmdlet carregará.
Se você especificar um arquivo que não existe, esse cmdlet retornará um erro.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirme
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
Mostra o que aconteceria se o cmdlet fosse executado.
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Storage. File. CloudFileShare

### Microsoft. Azure. Storage. File. CloudFileDirectory

### System. String

### Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext

## EXIBE

### Microsoft. Azure. Storage. File. Cloudfile

## INFORMA

## LINKS RELACIONADOS

[Remove-AzStorageDirectory](./Remove-AzStorageDirectory.md)

[New-AzStorageDirectory](./New-AzStorageDirectory.md)

[Get-AzStorageFileContent](./Get-AzStorageFileContent.md)
