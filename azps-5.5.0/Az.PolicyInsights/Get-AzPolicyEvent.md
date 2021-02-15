---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 744618bb2cc12b4d57bfb1ed42267fcbbe7a86ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115013"
---
# Get-AzPolicyEvent

## Sinopse
Obtém eventos de avaliação de política gerados à medida que os recursos são criados ou atualizados.

## Sintaxe

### SubscriptionScope (Padrão)
```
Get-AzPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Resourcescope
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrição
Obtém eventos de avaliação de política gerados à medida que os recursos são criados ou atualizados. Os registros de eventos de política podem ser consultados em vários escopos com base no intervalo de tempo especificado (padrões para o último dia). Os resultados podem ser filtrados, agrupados e agregados de grupo podem ser computados.

## Exemplos

### Exemplo 1: Obter eventos de política no escopo da assinatura atual
```powershell
PS C:\> Get-AzPolicyEvent
```

Obtém registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.

### Exemplo 2: Obter eventos de política no escopo de assinatura especificado
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Obtém registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura especificada.

### Exemplo 3: Obter eventos de política no escopo do grupo de gerenciamento
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

Obtém registros de eventos de política gerados no último dia para todos os recursos do grupo de gerenciamento especificado.

### Exemplo 4: Obter eventos de política no escopo do grupo de recursos na assinatura atual
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

Obtém registros de eventos de política gerados no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura no contexto da sessão atual).

### Exemplo 5: Obter eventos de política no escopo do grupo de recursos na assinatura especificada
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Obtém registros de eventos de política gerados no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura especificada).

### Exemplo 6: Obter eventos de política para um recurso
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Obtém registros de eventos de política gerados no último dia para o recurso especificado.

### Exemplo 7: Obter eventos de política para uma definição de conjunto de políticas na assinatura atual
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Obtém registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) efetivados pela definição de conjunto de política especificado (que existe na assinatura no contexto de sessão atual).

### Exemplo 8: Obter eventos de política para uma definição de conjunto de políticas na assinatura especificada
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Obtém registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela definição de conjunto de política especificada (que existe na assinatura especificada).

### Exemplo 9: Obter eventos de política para uma definição de política na assinatura atual
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Obtém registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela definição de política especificada (que existe na assinatura no contexto de sessão atual).

### Exemplo 10: Obter eventos de política para uma definição de política na assinatura especificada
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Obtém registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela definição de política especificada (que existe na assinatura especificada).

### Exemplo 11: Obter eventos de política para uma atribuição de política na assinatura atual
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Obtém registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela atribuição de política especificada (que existe na assinatura no contexto de sessão atual).

### Exemplo 12: Obter eventos de política para uma atribuição de política na assinatura especificada
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Obtém registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela atribuição de política especificada (que existe na assinatura especificada).

### Exemplo 13: Obter eventos de política para uma atribuição de política no grupo de recursos especificado na assinatura atual
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Obtém registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela atribuição de política especificada (que existe no grupo de recursos na assinatura no contexto de sessão atual).

### Exemplo 14: Obter eventos de política no escopo da assinatura atual, com as opções de consulta OrderBy, Top e Select
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

Obtém registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual. O comando ordena os resultados por data/hora e propriedades de nome de atribuição de política e leva apenas 5 dos 5 primeiros listados nessa ordem.
Ele também seleciona para listar apenas um subconjunto das colunas para cada registro.

### Exemplo 15: Obter eventos de política no escopo da assinatura atual, com opções de consulta De e Para
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Obtém registros de eventos de política gerados dentro do intervalo de datas especificado para todos os recursos dentro da assinatura no contexto de sessão atual.

### Exemplo 16: Obter eventos de política no escopo da assinatura atual, com a opção de consulta Filtro
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Obtém registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.
O comando limita os resultados retornados pela filtragem com base na ação de definição de política (inclui ações de negação ou auditoria) e local do recurso (exclui o local do leste).

### Exemplo 17: Obter eventos de política no escopo da assinatura atual, com Aplicar especificando agregação de contagem de linhas
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

Obtém o número de registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.
O comando retorna a contagem apenas dos registros de eventos de política, que são retornados dentro da propriedade AdditionalProperties.

### Exemplo 18: Obter eventos de política no escopo da assinatura atual, com Aplicar especificando o agrupamento com agregação
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

Obtém registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual. O comando limita os resultados retornados pela filtragem com base na ação de definição de política (inclui apenas eventos de auditoria e negação).
Ele agrupa os resultados com base na atribuição de política, definição de política, ação de definição de política e ID de recurso, e calcula o número de registros em cada grupo, que é retornado dentro da propriedade AdditionalProperties.
Ele ordena os resultados pela agregação de contagem em ordem decrescente e leva apenas 5 dos 5 primeiros listados nessa ordem.

### Exemplo 19: Obter eventos de política no escopo da assinatura atual, com Aplicar especificando o agrupamento sem agregação
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

Obtém registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual. O comando limita os resultados retornados pela filtragem com base na ação de definição de política (inclui apenas eventos de auditoria e negação).
Ele grupos os resultados com base na ID do recurso. Isso gera a lista de todos os recursos dentro da assinatura que gerou um evento de política para pelo menos uma política de auditoria ou negação.

### Exemplo 20: Obter eventos de política no escopo da assinatura atual, com Aplicar especificando vários grupos
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

Obtém registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual. O comando limita os resultados retornados pela filtragem com base na ação de definição de política (inclui apenas negar eventos).
Ele grupos os resultados primeiro com base na atribuição de política, na definição da política e na ID do recurso. Em seguida, agrupa ainda mais os resultados desse grupo com as mesmas propriedades, exceto a ID do recurso, e calcula o número de registros em cada um desses grupos, que é retornado dentro da propriedade AdditionalProperties.
Ele ordena os resultados pela agregação de contagem em ordem decrescente e leva apenas 5 dos 5 primeiros listados nessa ordem.
Isso gera as cinco principais políticas de negação com o maior número de recursos negados.

## Parâmetros

### -Aplicar
Aplicar expressão para agregação usando notação OData.

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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

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

### -Filtro
Expressão de filtro usando notação OData.

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

### -De
O data/hora formatado iso 8601 especifica a hora de início do intervalo a ser consultado.
Quando não especificado, o padrão é o valor do parâmetro 'Para' menos 1 dia.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementGroupName
Nome do grupo de gerenciamento.

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OrderBy
Expressão de ordenação usando notação OData.
Um ou mais nomes de coluna separados por vírgulas com um "desc" opcional (o padrão) ou "asc".

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

### -PolicyAssignmentName
Nome da atribuição de política.

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyDefinitionName
Nome da definição de política.

```yaml
Type: System.String
Parameter Sets: PolicyDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicySetDefinitionName
Nome de definição de conjunto de políticas.

```yaml
Type: System.String
Parameter Sets: PolicySetDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
ID do Recurso.

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Selecionar
Selecione a expressão usando notação OData.
Um ou mais nomes de coluna separados por vírgula.
Limita as colunas em cada registro apenas às solicitadas.

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

### -SubscriptionId
ID da assinatura.

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, ResourceGroupScope, PolicySetDefinitionScope, PolicyDefinitionScope, SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Para
ÉO 8601 data/hora formatada especificando a hora de término do intervalo para consulta.
Quando não especificado, o padrão é o horário da solicitação.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Superior
Número máximo de registros a retornar.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### System.String

## Saídas

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent

## Notas

## LINKS RELACIONADOS
