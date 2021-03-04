---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: f8df4d49f0181b7cf8abf2581a522f953f3f2df7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892569"
---
# New-AzBatchResourceFile

## SYNOPSIS
Cria um Arquivo de Recursos para uso por `New-AzBatchTask` .

## SINTAXE

### HttpUrl (Padrão)
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

## DESCRIPTION
Cria um Arquivo de Recursos para uso por `New-AzBatchTask` .

## EXEMPLOS

### Exemplo 1: Criar um arquivo de recurso a partir de uma URL HTTP apontando para um único arquivo
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Cria uma `PSResourceFile` referência a uma URL HTTP.

### Exemplo 2: Criar um arquivo de recurso a partir de uma URL de contêiner de armazenamento do Azure
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Cria uma referência a uma URL de `PSResourceFile` contêiner de armazenamento do Azure. Todos os arquivos no contêiner serão baixados para a pasta especificada.

### Exemplo 3: Criar um arquivo de recurso a partir de um nome de contêiner de Armazenamento Automático
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Cria uma `PSResourceFile` referência a um nome de contêiner de Armazenamento Automático. Todos os arquivos no contêiner serão baixados para a pasta especificada.

## PARÂMETROS

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
Obtém o prefixo blob a ser usado ao baixar blobs de um contêiner de Armazenamento do Azure.
Somente os blobs cujos nomes começam com o prefixo especificado serão baixados.
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
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

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
Obtém o atributo modo de permissão de arquivo no formato octal.
Essa propriedade só será aplicável se o arquivo de recurso for baixado para um nó Linux.
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
O local no nó de computação para o qual baixar os arquivos, em relação ao diretório de trabalho da tarefa. Se o parâmetro HttpUrl for especificado, o FilePath será necessário e descreverá o caminho para o qual o arquivo será baixado, incluindo o nome do arquivo. Caso contrário, se os parâmetros AutoStorageContainerName ou StorageContainerUrl são especificados, FilePath será opcional e será o diretório para o qual baixar os arquivos. No caso em que FilePath for usado como um diretório, qualquer estrutura de diretório já associada aos dados de entrada será mantida completa e anexada ao diretório FilePath especificado. O caminho relativo especificado não pode sair do diretório de trabalho da tarefa (por exemplo, usando '..').

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
Se a URL for Armazenamento de Blob do Azure, ela deverá ser acessível usando o acesso anônimo; ou seja, o serviço Batch não apresenta credenciais ao baixar o blob.
Há duas maneiras de obter essa URL para um blob no armazenamento do Azure: incluir uma Assinatura de Acesso Compartilhado (SAS) concedendo permissões de leitura no blob ou definir a ACL para o blob ou seu contêiner para permitir o acesso público.

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
A URL do contêiner blob no Armazenamento de Blob do Azure.
Essa URL deve ser acessível e listável usando o acesso anônimo; ou seja, o serviço Batch não apresenta credenciais ao baixar blobs do contêiner.
Há duas maneiras de obter essa URL para um contêiner no armazenamento do Azure: incluir uma Assinatura de Acesso Compartilhado (SAS) concedendo permissões de leitura no contêiner ou definir a ACL do contêiner para permitir o acesso público.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Nenhum

## SAÍDAS

### Microsoft.Azure.Commands.Batch. Models.PSResourceFile

## NOTES

## LINKS RELACIONADOS

[New-AzBatchTask](./New-AzBatchTask.md)