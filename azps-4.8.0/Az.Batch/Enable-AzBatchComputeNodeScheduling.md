---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9969388d51abb337030a8a732805ee1a15368ea7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954440"
---
# Enable-AzBatchComputeNodeScheduling

## Sinopse
Habilita o agendamento de tarefas no nó de computação especificado.

## SYNTAX

### ID (padrão)
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Enable-AzBatchComputeNodeScheduling** habilita o agendamento de tarefas no nó de computação especificado.
Um nó de computação é uma máquina virtual do Azure dedicada a uma carga de trabalho específica do aplicativo.

## EXEMPLOS

### Exemplo 1: habilitar o agendamento de tarefas em um nó de computação
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Esses comandos permitem o agendamento de tarefas no nó de computação TVM-1783593343_34-20151117t222514z.
Para fazer isso, o primeiro comando do exemplo cria uma referência de objeto contendo as chaves de conta para o contosobatchaccount da conta em lotes.
Essa referência de objeto é armazenada em uma variável chamada $context.
Em seguida, o segundo comando usa essa referência de objeto e o cmdlet **Enable-AzBatchComputeNodeScheduling** para se conectar ao pool mypool e habilitar o agendamento de tarefas no TVM-1783593343_34-20151117t222514z.

### Exemplo 2: habilitar o agendamento de tarefas em nós de computação em um pool
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

Esses comandos permitem o agendamento de tarefas em todos os nós de computação encontrados na Pool06 do pool.
Para executar essa tarefa, o primeiro comando do exemplo cria uma referência de objeto que contém as chaves de conta do contosobatchaccount da conta em lotes.
Essa referência de objeto é armazenada em uma variável chamada $context.
O segundo comando no exemplo usa essa referência de objeto e **Get-AzBatchComputeNode** para retornar uma coleção de todos os nós de computação encontrados em Pool06.
Essa coleção é então canalizada para o cmdlet **Enable-AzBatchComputeNodeScheduling** , que permite o agendamento de tarefas em cada nó de computação na coleção.

## OS

### -BatchContext
Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.
Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes. Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas. Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão. Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.

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

### -ComputeNode
Especifica uma referência de objeto para o nó de computação em que o agendamento de tarefas está habilitado.
Essa referência de objeto é criada usando-se o cmdlet Get-AzBatchComputeNode e armazenando o objeto do nó de computação retornado em uma variável.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### -ID
Especifica a ID do nó de computação em que o agendamento da tarefa está habilitado.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Poolid
Especifica a ID do pool de lotes que contém o nó de computação no qual o agendamento de tarefas está habilitado.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Microsoft.Azure.Commands.Batch. Modelos. PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## EXIBE

### System. void

## INFORMA

## LINKS RELACIONADOS

[Disable-AzBatchComputeNodeScheduling](./Disable-AzBatchComputeNodeScheduling.md)


