---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 1e7438195b0749dabc5206238a32bc00be03ea31
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890881"
---
# Disable-AzBatchComputeNodeScheduling

## SYNOPSIS
Desabilita o agendamento de tarefas no nó de computação especificado.

## SINTAXE

### ID (Padrão)
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Disable-AzBatchComputeNodeScheduling** desabilita o agendamento de tarefas no nó de computação especificado.
Um nó de computação é uma máquina virtual do Azure dedicada a uma carga de trabalho de aplicativo específica.
Quando você desabilita o agendamento de tarefas em um nó de computação, você também terá a opção de determinar o que fazer sobre os trabalhos atualmente na fila de tarefas do nó.
**Disable-AzBatchComputeNodeScheduling** permite que você faça o seguinte: 
- Termine as tarefas e coloque-as novamente na fila de trabalho.
Isso permite que essas tarefas sejam reagendadas em outro nó de computação. 
- Termine as tarefas e remova-as da fila de trabalho.
As tarefas paradas dessa maneira não serão reagendadas. 
- Aguarde que todas as tarefas que estão sendo executadas sejam concluídas e desabilite o agendamento de tarefas no nó de computação. 
- Aguarde que todas as tarefas em execução sejam concluídas e todos os períodos de retenção de dados expirem e desabilite o agendamento de tarefas no nó de computação.

## EXEMPLOS

### Exemplo 1: Desabilitar o agendamento de tarefas em um nó de computação
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Esses comandos desabilitam o agendamento de tarefas no nó de computação tvm-1783593343_34-2015117t222514z.
Para fazer isso, o primeiro comando no exemplo cria uma referência de objeto às chaves de conta da conta em lotes contosobatchaccount.
Essa referência de objeto é armazenada em uma variável chamada $context.
O segundo comando usa essa referência de objeto e o cmdlet **Disable-AzBatchComputeNodeScheduling** para se conectar ao pool myPool e desabilitar o agendamento de tarefas no nó tvm-1783593343_34-2015117t222514z.
Como o *parâmetro DisableComputeNodeSchedulingOptions* não foi incluído, nenhuma tarefa em execução no nó de computação será remarcada.

### Exemplo 2: Desabilitar o agendamento de tarefas em todos os nós de computação em um pool
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

Esses comandos desabilitam o agendamento de tarefas em todos os nós do computador no pool de lotes Pool06.
Para executar essa tarefa, o primeiro comando no exemplo cria uma referência de objeto às chaves de conta da conta em lotes contosobatchaccount.
Essa referência de objeto é armazenada em uma variável chamada $context.
O segundo comando no exemplo usa essa referência de objeto e **Get-AzBatchComputeNode** para retornar uma coleção de todos os nós de computação encontrados no Pool06.
Essa coleção é então canalada para o cmdlet **Disable-AzBatchComputeNodeScheduling** para desabilitar o agendamento de tarefas em cada nó de computação na coleção.
Como o *parâmetro DisableComputeNodeSchedulingOptions* não foi incluído, nenhuma tarefa em execução nos nós de computação será requeriada.

## PARÂMETROS

### -BatchContext
Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.
Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch. Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas. Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão. Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.

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
Especifica uma referência de objeto ao nó de computação onde o agendamento de tarefas está desabilitado.
Essa referência de objeto é criada usando o cmdlet Get-AzBatchComputeNode e armazenar o objeto de nó de computação retornado em uma variável.

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
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.

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

### -DisableSchedulingOption
Especifica como esse cmdlet lida com todas as tarefas em execução no nó do computador onde o agendamento está sendo desabilitado.
Os valores aceitáveis para este parâmetro são:
- Requeue.
As tarefas são interrompidas imediatamente e retornadas à fila de trabalho.
Isso permite que as tarefas sejam reagendadas em outro nó de computação.
Esse é o valor padrão. 
- Encerrar.
As tarefas são interrompidas imediatamente e removidas da fila de trabalho.
Essas tarefas não serão reagendadas. 
- TaskCompletion.
Atualmente, as tarefas em execução poderão ser concluídas antes que o agendamento de tarefas seja desabilitado no nó de computação.
Nenhuma nova tarefa será agendada neste nó. 
- RetainedData.
Atualmente, as tarefas em execução poderão ser concluídas e os períodos de retenção de dados poderão expirar antes que o agendamento de tarefas seja desabilitado no nó de computação.
Nenhuma nova tarefa será agendada neste nó.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.DisableComputeNodeSchedulingOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
Especifica a ID do nó de computação onde o agendamento de tarefas está desabilitado.

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

### -PoolId
Especifica a ID do pool de lotes que contém o nó de computação onde o agendamento de tarefas está desabilitado.
Se você usar o *parâmetro PoolId,* não use o parâmetro *ComputeNode* nesse mesmo comando.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.Commands.Batch. Models.PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## SAÍDAS

### System.Void

## NOTES

## LINKS RELACIONADOS

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Enable-AzBatchComputeNodeScheduling](./Enable-AzBatchComputeNodeScheduling.md)


