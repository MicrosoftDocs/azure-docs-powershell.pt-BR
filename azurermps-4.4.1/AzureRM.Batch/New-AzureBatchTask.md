---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
ms.openlocfilehash: dd8825be6491b0a0c8c8589f77180b38f9f230d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431149"
---
# New-AzureBatchTask

## Sinopse
Cria uma tarefa em lotes em um trabalho.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### JobId_Single (padrão)
```
New-AzureBatchTask -JobId <String> -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### JobId_Bulk
```
New-AzureBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### JobObject_Bulk
```
New-AzureBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### JobObject_Single
```
New-AzureBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureBatchTask** cria uma tarefa em lotes do Azure sob o trabalho especificado pelo parâmetro *JobID* ou o parâmetro *Job* .

## EXEMPLOS

### Exemplo 1: criar uma tarefa em lote
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

Esse comando cria uma tarefa com a ID Task23 sob o trabalho que tem o ID Job-000001.
A tarefa executa o comando especificado.
Use o cmdlet **Get-AzureRmBatchAccountKeys** para atribuir um contexto para a variável $Context.

### Exemplo 2: criar uma tarefa em lote
```
PS C:\>Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -RunElevated -BatchContext $Context
```

Esse comando obtém o trabalho em lotes que tem o ID Job-000001 usando o cmdlet **Get-AzureBatchJob** .
O comando passa aquele trabalho para o cmdlet atual usando o operador pipeline.
O comando cria uma tarefa com a ID Task26 sob esse trabalho.
A tarefa executa o comando especificado usando permissões elevadas.

### Exemplo 3: adicionar um conjunto de tarefas ao trabalho especificado usando o pipeline
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

O primeiro comando cria uma referência de objeto para as chaves de conta da conta em lotes chamada ContosoBatchAccount usando **Get-AzureRmBatchAccountKeys**.
O comando armazena essa referência de objeto na variável $Context.

Os próximos dois comandos criam objetos **PSCloudTask** usando o cmdlet New-Object.
Os comandos armazenam as tarefas nas variáveis $Task 01 e $Task 02.

O comando final Obtém o trabalho em lotes com o ID Job-000001 usando **Get-AzureBatchJob**.
Em seguida, o comando passa esse trabalho para o cmdlet atual usando o operador pipeline.
O comando adiciona uma coleção de tarefas sob esse trabalho.
O comando usa o contexto armazenado em $Context.

### Exemplo 4: adicionar um conjunto de tarefas ao trabalho especificado
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzureBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

O primeiro comando cria uma referência de objeto para as chaves de conta da conta em lotes chamada ContosoBatchAccount usando **Get-AzureRmBatchAccountKeys**.
O comando armazena essa referência de objeto na variável $Context.

Os próximos dois comandos criam objetos **PSCloudTask** usando o cmdlet New-Object.
Os comandos armazenam as tarefas nas variáveis $Task 01 e $Task 02.

O comando final adiciona as tarefas armazenadas em $Task 01 e $Task 02 sob o trabalho que tem o job ID-000001.

## OS

### -AffinityInformation
Especifica uma dica de localidade que o serviço de lote usa para selecionar um nó no qual executar a tarefa.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAffinityInformation
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationPackageReferences
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -CommandLine
Especifica a linha de comando para a tarefa.

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Restrições
Especifica as restrições de execução que se aplicam a essa tarefa.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Depende
Especifica que a tarefa depende de outras tarefas.
A tarefa não será agendada até que todas as tarefas depends tenham sido concluídas com êxito.

```yaml
Type: Microsoft.Azure.Batch.TaskDependencies
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Especifica o nome de exibição da tarefa.

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnvironmentSettings
Especifica as configurações de ambiente, como pares de chave/valor, que esse cmdlet adiciona à tarefa.
A chave é o nome da configuração do ambiente.
O valor é a configuração do ambiente.

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExitConditions
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSExitConditions
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Especifica a ID da tarefa.

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Trabalho
Especifica o trabalho sob o qual esse cmdlet cria a tarefa.
Para obter um objeto **PSCloudJob** , use o cmdlet Get-AzureBatchJob.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: JobObject_Bulk, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Especifica a ID do trabalho sob a qual esse cmdlet cria a tarefa.

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobId_Bulk
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MultiInstanceSettings
Especifica informações sobre como executar uma tarefa de várias instâncias.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceFiles
Especifica os arquivos de recurso, como pares chave/valor, que a tarefa requer.
A chave é o caminho do arquivo de recurso.
O valor é a fonte de blob do arquivo de recurso.

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunElevated
Indica que o processo da tarefa é executado com privilégios de administrador.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tarefas
Especifica a coleção de tarefas a serem adicionadas.
Cada tarefa deve ter uma ID exclusiva.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask[]
Parameter Sets: JobId_Bulk, JobObject_Bulk
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

### PSCloudJob
O parâmetro ' Job ' aceita o valor do tipo ' PSCloudJob ' da pipeline

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchJob](./Get-AzureBatchJob.md)

[Get-AzureBatchTask](./Get-AzureBatchTask.md)

[New-AzureBatchTask](./New-AzureBatchTask.md)

[Remove-AzureBatchTask](./Remove-AzureBatchTask.md)

[Parar-AzureBatchTask](./Stop-AzureBatchTask.md)

[Cmdlets do Azure batch](./AzureRM.Batch.md)


