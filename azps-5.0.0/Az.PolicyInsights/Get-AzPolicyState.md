---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 04600529ded8b95da578d59f0b2f46cd396594ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116869"
---
# Get-AzPolicyState

## Sinopse
Obtém os Estados de conformidade de política para recursos.

## SYNTAX

### SubscriptionScope (padrão)
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-Expand <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
Obtém os Estados de conformidade de política para recursos. Os registros de estado da política podem ser consultados em vários escopos. Com base no intervalo de tempo especificado (o padrão é o último dia), os Estados da política mais recente ou todas as transições de estado da política podem ser consultadas. Os resultados podem ser calculados, agrupados e as agregações de grupo podem ser calculadas.

## EXEMPLOS

### Exemplo 1: obter os Estados da política mais recentes no escopo da assinatura atual
```powershell
PS C:\> Get-AzPolicyState
```

Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.

### Exemplo 2: obter os Estados da política mais recentes no escopo de assinatura especificado
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos dentro da assinatura especificada.

### Exemplo 3: obter todos os Estados de política no escopo de assinatura atual
```powershell
PS C:\> Get-AzPolicyState -All
```

Obtém todos os registros de estado do estado da política (incluindo o mais recente) gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.

### Exemplo 4: obter os Estados da política mais recentes no escopo do grupo de gerenciamento
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos dentro do grupo de gerenciamento especificado.

### Exemplo 5: obter os Estados da política mais recentes no escopo do grupo de recursos na assinatura atual
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura no contexto atual da sessão).

### Exemplo 6: obter os Estados da política mais recentes no escopo do grupo de recursos na assinatura especificada
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura especificada).

### Exemplo 7: obter os Estados da política mais recentes para um recurso
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Obtém os registros de estado da política mais recentes gerados no último dia do recurso especificado.

### Exemplo 8: obter os Estados da política mais recentes para uma definição de conjunto de políticas na assinatura atual
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Obtém os últimos registros de estado da política gerados no último dia para todos os recursos (dentro do locatário no contexto da sessão atual) afetados pela definição do conjunto de políticas especificado (que existe na assinatura no contexto atual da sessão).

### Exemplo 9: obter os Estados da política mais recentes para uma definição de política definida na assinatura especificada
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto da sessão atual) afetados pela definição do conjunto de políticas especificado (que existe na assinatura especificada).

### Exemplo 10: obter os Estados da política mais recentes para uma definição de política na assinatura atual
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Obtém os últimos registros de estado da política gerados no último dia para todos os recursos (dentro do locatário no contexto da sessão atual) afetados pela definição de política especificada (que existe na assinatura no contexto atual da sessão).

### Exemplo 11: obter os Estados da política mais recentes para uma definição de política na assinatura especificada
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela definição de política especificada (que existe na assinatura especificada).

### Exemplo 12: obter os Estados da política mais recentes para uma atribuição de política na assinatura atual
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Obtém os últimos registros de estado da política gerados no último dia para todos os recursos (dentro do locatário no contexto da sessão atual) afetados pela atribuição de política especificada (que existe na assinatura no contexto atual da sessão).

### Exemplo 13: obter os Estados da política mais recentes para uma atribuição de política na assinatura especificada
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto da sessão atual) afetados pela atribuição de política especificada (que existe na assinatura especificada).

### Exemplo 14: obter os Estados da política mais recentes para uma atribuição de política no grupo de recursos especificado na assinatura atual
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto da sessão atual) afetados pela atribuição de política especificada (que existe no grupo de recursos na assinatura do contexto da sessão atual).

### Exemplo 15: obter os Estados da política mais recentes em escopo de assinatura atual, com as opções de consulta OrderBy, Top e Select
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual. O comando ordena os resultados por carimbos de data/hora e propriedades de nome da atribuição de política e leva apenas as cinco primeiras das primeiras listadas nesta ordem.
Ele também seleciona para listar apenas um subconjunto de colunas para cada registro.

### Exemplo 16: obter os Estados da política mais recentes no escopo de assinatura atual, com as opções de consulta de e até
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Obtém os registros de estado da política mais recentes gerados dentro do intervalo de datas especificado para todos os recursos dentro da assinatura no contexto de sessão atual.

### Exemplo 17: obter os Estados da política mais recentes em escopo de assinatura atual, com opção de consulta de filtro
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.
O comando limita os resultados retornados pela filtragem com base na ação de definição da política (inclui ações de negação ou auditoria), status de conformidade (inclui apenas status não compatível) e local do recurso (exclui a localização do lesteus).

### Exemplo 18: obter os Estados da política mais recentes no escopo atual da assinatura, com aplicar especificando a agregação de contagem de linhas
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

Obtém o número de registros de estado da política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.
O comando retorna a contagem dos registros de estado da política apenas, que é retornada dentro da propriedade AdditionalProperties.

### Exemplo 19: obter os Estados da política mais recentes no escopo de assinatura atual, com aplicar ao agrupamento de agrupamento com agregação
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual. O comando limita os resultados retornados pela filtragem com base no status de conformidade (inclui apenas status não compatível).
Ele agrupa os resultados com base em atribuição de política, definição de conjunto de políticas e definição de política e calcula o número de registros em cada grupo, que é retornado dentro da propriedade AdditionalProperties.
Ele ordena os resultados pela agregação Count em ordem decrescente e leva apenas 5 principais daqueles listados nessa ordem.

### Exemplo 20: obter os Estados da política mais recentes no escopo de assinatura atual, com aplicar ao agrupamento sem agregação
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual. O comando limita os resultados retornados pela filtragem com base no status de conformidade (inclui apenas status não compatível).
Ele agrupa os resultados com base na ID do recurso. Isso gera a lista de todos os recursos dentro da assinatura que não está em conformidade em pelo menos uma política.

### Exemplo 21: obter os Estados da política mais recentes no escopo de assinatura atual, com aplicar ao mesmo tempo especificando vários agrupamentos
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### Exemplo 22: obter Estados de política mais recentes incluindo detalhes de avaliação de política de um recurso
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual. O comando limita os resultados retornados pela filtragem com base no status de conformidade (inclui apenas status não compatível).
Ele agrupa os resultados primeiro com base na atribuição da política, definição do conjunto de políticas, definição da política e ID do recurso. Em seguida, ele agrupa ainda mais os resultados desse Agrupamento com as mesmas propriedades, exceto para ID do recurso, e calcula o número de registros em cada um desses grupos, que é retornado dentro da propriedade AdditionalProperties.
Ele ordena os resultados pela agregação Count em ordem decrescente e leva apenas 5 principais daqueles listados nessa ordem.
Isso gera as cinco principais políticas com a maior quantidade de recursos não compatíveis.

## OS

### -Tudo
Dentro do intervalo de tempo especificado, obtenha todos os Estados da política em vez do mais recente.

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

### -Expandir
Expanda a expressão usando a notação do OData.

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

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

### Microsoft. Azure. Commands. PolicyInsights. Models. Policystate

## INFORMA

## LINKS RELACIONADOS

[Get-AzPolicyStateSummary](./Get-AzPolicyStateSummary.md)
