---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
ms.openlocfilehash: 92c485a743372eff7ddb8725172ac4d9bb030d22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610027"
---
# Get-AzureBatchNodeFileContent

## Sinopse
Obtém um arquivo de nó de lote.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Task_Id_Path
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Name] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Task_Id_Stream
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Name] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ComputeNode_Id_Path
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ComputeNode_Id_Stream
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject_Path
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject_Stream
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureBatchNodeFileContent** Obtém um arquivo de nó de lote do Azure e o salva como um arquivo ou em um Stream.

## EXEMPLOS

### Exemplo 1: obter um arquivo de nó de lote associado a uma tarefa e salvar o arquivo
```
PS C:\>Get-AzureBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Name "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Esse comando obtém o arquivo de nó chamado StdOut.txt e salva-o no caminho do arquivo E:\PowerShell\StdOut.txt no computador local.
O arquivo de nó StdOut.txt está associado a uma tarefa que tem a ID Task01 para o trabalho que tem a ID Job01.
Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.

### Exemplo 2: obter um arquivo de nó de lote e salvá-lo em um caminho de arquivo especificado usando o pipeline
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job02" -TaskId "Task02" -Name "StdErr.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Esse comando obtém o arquivo de nó chamado StdErr.txt usando o cmdlet Get-AzureBatchNodeFile.
O comando passa esse arquivo para o cmdlet atual usando o operador pipeline.
O cmdlet atual salva esse arquivo no caminho do arquivo E:\PowerShell\StdOut.txt no computador local.
O arquivo de nó StdOut.txt está associado à tarefa que tem a ID Task02 para o trabalho que tem a ID Job02.

### Exemplo 3: obter um arquivo de nó de lote associado a uma tarefa e direcioná-lo a um fluxo
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Name "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

O primeiro comando cria um Stream usando o cmdlet New-Object e, em seguida, armazena-o na variável $Stream.

O segundo comando obtém o arquivo de nó chamado StdOut.txt da tarefa que tem a ID Task11 para o trabalho que tem a ID Job03.
O comando direciona o conteúdo do arquivo para o fluxo no $Stream.

### Exemplo 4: obter um arquivo de nó de um nó de computação e salvá-lo
```
PS C:\>Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Esse comando obtém o arquivo de nó Startup\StdOut.txt do nó de computação que tem a ID ComputeNode01 no pool que tem a ID Pool01.
O comando salva o arquivo no caminho do arquivo E:\PowerShell\StdOut.txt no computador local.

### Exemplo 5: obter um arquivo de nó de um nó de computação e salvá-lo usando o pipeline
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "Startup\StdOut.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Esse comando obtém o arquivo de nó Startup\StdOut.txt usando Get-AzureBatchNodeFile do nó de computação que tem a ID ComputeNode01.
O nó de computação está no pool que tem a ID Pool01.
O comando passa esse arquivo de nó para o cmdlet atual.
Esse cmdlet salva o arquivo para o caminho do arquivo E:\PowerShell\StdOut.txt no computador local.

### Exemplo 6: obter um arquivo de nó de um nó de computação e direcioná-lo para um fluxo
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

O primeiro comando cria um Stream usando o cmdlet New-Object e, em seguida, armazena-o na variável $Stream.

O segundo comando obtém o arquivo de nó chamado StdOut.txt do nó de computação que tem a ID ComputeNode01 no pool que tem a ID Pool01.
O comando direciona o conteúdo do arquivo para o fluxo no $Stream.

## OS

### -BatchContext
Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.
Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ByteRangeEnd
O final do intervalo de bytes a ser baixado.
```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ByteRangeStart
O início do intervalo de bytes a ser baixado.
```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputeNodeId
Especifica a ID do nó de computação que contém o arquivo de nó que este cmdlet retorna.

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DestinationPath
Especifica o caminho do arquivo em que esse cmdlet salva o arquivo de nó.

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, ComputeNode_Id_Path, InputObject_Path
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationStream
Especifica o fluxo em que esse cmdlet grava o conteúdo do arquivo de nó.
Esse cmdlet não fecha ou rebobina o fluxo.

```yaml
Type: System.IO.Stream
Parameter Sets: Task_Id_Stream, ComputeNode_Id_Stream, InputObject_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Especifica o arquivo que esse cmdlet obtém, como um objeto **PSNodeFile** .
Para obter um objeto de arquivo de nó, use o cmdlet Get-AzureBatchNodeFile.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Especifica a ID do trabalho que contém a tarefa de destino.

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome do arquivo de nó que este cmdlet recupera.
Não é possível especificar caracteres curinga.

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Poolid
Especifica a ID do pool que contém o nó de computação que contém o arquivo de nó que este cmdlet obtém.

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TaskId
Especifica a ID da tarefa.

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### BatchAccountContext
O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline

### PSNodeFile
O parâmetro ' InputObject ' aceita o valor do tipo ' PSNodeFile ' do pipeline

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchNodeFile](./Get-AzureBatchNodeFile.md)

[Cmdlets do Azure batch](./AzureRM.Batch.md)


