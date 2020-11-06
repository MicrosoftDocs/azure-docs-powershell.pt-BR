---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
ms.openlocfilehash: 0524a55284d5c93db006248c12aa5a44f40deee7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428591"
---
# New-AzureBatchJobSchedule

## Sinopse
Cria um plano de trabalho no serviço de lote.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureBatchJobSchedule** cria um cronograma de trabalho no serviço de lote do Azure.
O parâmetro *BatchAccountContext* especifica a conta na qual esse cmdlet cria o cronograma.

## EXEMPLOS

### Exemplo 1: criar um plano de trabalho
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzureBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

Este exemplo cria um plano de trabalho.
Os cinco primeiros comandos criam e modificam objetos **PSSchedule** , **PSJobSpecification** e **PSPoolInformation** .
Os comandos usam o cmdlet New-Object e a sintaxe padrão do PowerShell do Azure.
Os comandos armazenam esses objetos nas variáveis $Schedule e $JobSpecification.
O comando final cria um plano de trabalho com a ID JobSchedule17.
Esse cronograma cria trabalhos com um intervalo de recorrência de um dia.
Os trabalhos são executados no pool que tem a ID ContosoPool06, conforme especificado no quinto comando.
Use o cmdlet **Get-AzureRmBatchAccountKeys** para atribuir um contexto para a variável $Context.

## OS

### -BatchContext
Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.
Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes. Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas. Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão. Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.

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

### -DisplayName
Especifica um nome de exibição para o plano de trabalho.

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

### -ID
Especifica a ID do agendamento de trabalho que este cmdlet cria.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobSpecification
Especifica os detalhes dos trabalhos que este cmdlet inclui no cronograma do trabalho.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Metadados
Especifica os metadados, como pares de chave/valor, a serem adicionados ao plano de trabalho.
A chave é o nome dos metadados.
O valor é o valor dos metadados.

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Cronograma
Especifica o cronograma que determina quando criar trabalhos.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

### Microsoft.Azure.Commands.Batch.BatchAccountContext
Parâmetros: BatchContext (ByValue)

## EXIBE

### System. void

## INFORMA

## LINKS RELACIONADOS

[Disable-AzureBatchJobSchedule](./Disable-AzureBatchJobSchedule.md)

[Enable-AzureBatchJobSchedule](./Enable-AzureBatchJobSchedule.md)

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchJobSchedule](./Get-AzureBatchJobSchedule.md)

[Remove-AzureBatchJobSchedule](./Remove-AzureBatchJobSchedule.md)

[Parar-AzureBatchJobSchedule](./Stop-AzureBatchJobSchedule.md)

[Cmdlets do Azure batch](./AzureRM.Batch.md)


