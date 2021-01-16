---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 744618bb2cc12b4d57bfb1ed42267fcbbe7a86ab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260607"
---
# Get-AzPolicyEvent

## Sinopse
Obtém eventos de avaliação de política gerados à medida que os recursos são criados ou atualizados.

## SYNTAX

### SubscriptionScope (padrão)
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

### ResourceScope
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
Obtém eventos de avaliação de política gerados à medida que os recursos são criados ou atualizados. Registros de eventos de política podem ser consultados em vários escopos com base no intervalo de tempo especificado (o padrão é o último dia). Os resultados podem ser calculados, agrupados e as agregações de grupo podem ser calculadas.

## EXEMPLOS

### Exemplo 1: obter eventos de política no escopo de assinatura atual
```powershell
PS C:\> Get-AzPolicyEvent
```

Obtém os registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.

### Exemplo 2: obter eventos de política no escopo de assinatura especificado
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Obtém os registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura especificada.

### Exemplo 3: obter eventos de política no escopo do grupo de gerenciamento
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

Obtém registros de eventos de política gerados no último dia para todos os recursos dentro do grupo de gerenciamento especificado.

### Exemplo 4: obter eventos de política no escopo do grupo de recursos na assinatura atual
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

Obtém registros de eventos de política gerados no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura no contexto de sessão atual).

### Exemplo 5: obter eventos de política no escopo do grupo de recursos na assinatura especificada
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Obtém registros de eventos de política gerados no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura especificada).

### Exemplo 6: obter eventos de política para um recurso
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Obtém os registros de eventos de política gerados no último dia do recurso especificado.

### Exemplo 7: obter eventos de política para uma definição de conjunto de políticas na assinatura atual
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Obtém os registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela definição do conjunto de políticas especificado (que existe na assinatura no contexto atual da sessão).

### Exemplo 8: obter eventos de política para uma definição de política definida na assinatura especificada
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Obtém os registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela definição do conjunto de políticas especificado (que existe na assinatura especificada).

### Exemplo 9: obter eventos de política para uma definição de política na assinatura atual
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Obtém os registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela definição de política especificada (que existe na assinatura no contexto de sessão atual).

### Exemplo 10: obter eventos de política para uma definição de política na assinatura especificada
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Obtém os registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela definição de política especificada (que existe na assinatura especificada).

### Exemplo 11: obter eventos de política para uma atribuição de política na assinatura atual
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Obtém os registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela atribuição de política especificada (que existe na assinatura no contexto da sessão atual).

### Exemplo 12: obter eventos de política para uma atribuição de política na assinatura especificada
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Obtém os registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela atribuição de política especificada (que existe na assinatura especificada).

### Exemplo 13: obter eventos de política para uma atribuição de política no grupo de recursos especificado na assinatura atual
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Obtém registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela atribuição de política especificada (que existe no grupo de recursos na assinatura do contexto de sessão atual).

### Exemplo 14: obter eventos de política em escopo de assinatura atual, com as opções de consulta OrderBy, Top e Select
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

Obtém os registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual. O comando ordena os resultados por carimbos de data/hora e propriedades de nome da atribuição de política e leva apenas as cinco primeiras das primeiras listadas nesta ordem.
Ele também seleciona para listar apenas um subconjunto de colunas para cada registro.

### Exemplo 15: obter eventos de política no escopo de assinatura atual, com as opções de consulta de e até
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Obtém registros de eventos de política gerados dentro do intervalo de datas especificado para todos os recursos dentro da assinatura no contexto de sessão atual.

### Exemplo 16: obter eventos de política em escopo de assinatura atual, com opção de consulta de filtro
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Obtém os registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.
O comando limita os resultados retornados pela filtragem com base na ação de definição da política (inclui ações de negação ou auditoria) e local do recurso (exclui o local do lesteus).

### Exemplo 17: obter eventos de política no escopo atual da assinatura, com aplicar especificando a agregação de contagem de linhas
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

Obtém o número de registros de eventos de política gerado no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.
O comando retorna a contagem dos registros de eventos de política apenas, que é retornada dentro da propriedade AdditionalProperties.

### Exemplo 18: obter eventos de política no escopo de assinatura atual, com aplicar ao agrupamento de agrupamento com agregação
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

Obtém os registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual. O comando limita os resultados retornados pela filtragem com base na ação de definição da política (inclui apenas eventos Audit e Deny).
Ele agrupa os resultados com base em atribuição de política, definição de política, ação de definição de política e ID do recurso e calcula o número de registros em cada grupo, que é retornado dentro da propriedade AdditionalProperties.
Ele ordena os resultados pela agregação Count em ordem decrescente e leva apenas 5 principais daqueles listados nessa ordem.

### Exemplo 19: obter eventos de política no escopo de assinatura atual, com aplicar ao agrupamento sem agregação
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

Obtém os registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual. O comando limita os resultados retornados pela filtragem com base na ação de definição da política (inclui apenas eventos Audit e Deny).
Ele agrupa os resultados com base na ID do recurso. Isso gera a lista de todos os recursos dentro da assinatura que gerou um evento de política para pelo menos uma política de auditoria ou negação.

### Exemplo 20: obter eventos de política no escopo atual da assinatura, com aplicar vários agrupamentos
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

Obtém os registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual. O comando limita os resultados retornados pela filtragem com base na ação de definição da política (inclui apenas eventos Deny).
Ele agrupa os resultados primeiro com base na atribuição da política, na definição da política e na ID do recurso. Em seguida, ele agrupa ainda mais os resultados desse Agrupamento com as mesmas propriedades, exceto para ID do recurso, e calcula o número de registros em cada um desses grupos, que é retornado dentro da propriedade AdditionalProperties.
Ele ordena os resultados pela agregação Count em ordem decrescente e leva apenas 5 principais daqueles listados nessa ordem.
Isso gera as cinco principais políticas de negação com o maior número de recursos negados.

## OS

### -Aplicar
Aplicar expressão para agregações usando a notação OData.

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

### -Filtro
Expressão de filtro usando a notação OData.

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
Marca de data/hora formatada ISO 8601 especificando a hora de início do intervalo para consulta.
Quando não especificado, o padrão é o valor do parâmetro ' para ' menos 1 dia.

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
Expressão de ordenação usando a notação OData.
Um ou mais nomes de coluna separados por vírgula com um ' DESC ' opcional (o padrão) ou ' ASC '.

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
Nome da definição da política.

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
Nome da definição do conjunto de políticas.

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
ID do recurso.

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

### -Selecione
Selecione a expressão usando a notação do OData.
Um ou mais nomes de coluna separados por vírgula.
Limita as colunas em cada registro a apenas aquelas solicitadas.

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

### -To
Marca de data/hora formatada ISO 8601 especificando a hora de término do intervalo para consulta.
Quando não especificado, o padrão é a hora da solicitação.

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

### -Início
Número máximo de registros a serem retornados.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. PolicyInsights. Models. PolicyEvent

## INFORMA

## LINKS RELACIONADOS
