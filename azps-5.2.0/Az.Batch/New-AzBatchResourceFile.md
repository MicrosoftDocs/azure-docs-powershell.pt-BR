---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262814"
---
# New-AzBatchResourceFile

## Sinopse
Cria um arquivo de recursos para uso `New-AzBatchTask` .

## SYNTAX

### HttpUrl (padrão)
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### StorageContainerUrl
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AutoStorageContainerName
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
Cria um arquivo de recursos para uso `New-AzBatchTask` .

## EXEMPLOS

### Exemplo 1: criar um arquivo de recurso a partir de uma URL HTTP apontando para um único arquivo
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Cria uma `PSResourceFile` referência a uma URL http.

### Exemplo 2: criar um arquivo de recursos a partir de uma URL do contêiner de armazenamento do Azure
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Cria uma `PSResourceFile` referência a uma URL do contêiner de armazenamento do Azure. Todos os arquivos no contêiner serão baixados para a pasta especificada.

### Exemplo 3: criar um arquivo de recurso a partir de um nome de contêiner de armazenamento automático
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Cria uma `PSResourceFile` referência a um nome de contêiner de armazenamento automático. Todos os arquivos no contêiner serão baixados para a pasta especificada.

## OS

### -AutoStorageContainerName
O nome do contêiner de armazenamento na conta de armazenamento automático.

```yaml
Type: System.String
Parameter Sets: AutoStorageContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlobPrefix
Obtém o prefixo de blob a ser usado ao baixar blobs de um contêiner de armazenamento do Azure.
Somente os BLOBs cujos nomes começam com o prefixo especificado serão baixados.
Esse prefixo pode ser um nome de arquivo parcial ou um subdiretório.
Se um prefixo não for especificado, todos os arquivos no contêiner serão baixados.

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileMode
Obtém o atributo do modo de permissão de arquivo em formato octal.
Essa propriedade é aplicável apenas se o arquivo de recurso é baixado para um nó Linux.
Se essa propriedade não for especificada para um nó Linux, o valor padrão será 0770.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FilePath
O local no nó de computação para o qual baixar o (s) arquivo (s), em relação ao diretório de trabalho da tarefa. Se o parâmetro HttpUrl for especificado, o FilePath será necessário e descreverá o caminho para o qual o arquivo será baixado, incluindo o nome do arquivo. Caso contrário, se os parâmetros AutoStorageContainerName ou StorageContainerUrl forem especificados, FilePath será opcional e será o diretório para o qual baixar os arquivos. Caso o FilePath seja usado como um diretório, qualquer estrutura de diretório já associada aos dados de entrada será mantida em total e acrescentada ao diretório FilePath especificado. O caminho relativo especificado não pode ser desfeito do diretório de trabalho da tarefa (por exemplo, usando '.. ').

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpUrl
A URL do arquivo a ser baixado.
Se a URL for Azure Blob Storage, ela deverá ser legível usando o acesso anônimo; ou seja, o serviço em lotes não apresenta nenhuma credencial durante o download do blob.
Há duas maneiras de obter tal URL para um blob no armazenamento do Azure: inclua uma assinatura de acesso compartilhado (SAS) que conceda permissões de leitura ao BLOB ou defina a ACL para o BLOB ou seu contêiner para permitir acesso público.

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContainerUrl
A URL do contêiner de blob no armazenamento do blob do Azure.
Esta URL deve ser legível e ser listada usando o acesso anônimo; ou seja, o serviço em lotes não apresenta nenhuma credencial durante o download de BLOBs do contêiner.
Há duas maneiras de obter tal URL para um contêiner no armazenamento do Azure: inclua uma assinatura de acesso compartilhado (SAS) que conceda permissões de leitura no contêiner ou defina a ACL do contêiner para permitir acesso público.

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Nenhuma

## EXIBE

### Microsoft.Azure.Commands.Batch. Modelos. PSResourceFile

## INFORMA

## LINKS RELACIONADOS

[New-AzBatchTask](./New-AzBatchTask.md)