---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 82aa08a3d4b4eb42638e1b9def55b5d936f176b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890107"
---
# Get-AzPolicyState

## SYNOPSIS
Obtém estados de conformidade de política para recursos.

## SINTAXE

### SubscriptionScope (Padrão)
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

## DESCRIPTION
Obtém estados de conformidade de política para recursos. Os registros de estado de política podem ser consultados em vários escopos. Com base no intervalo de tempo especificado (padrões para o último dia), os estados de política mais recentes ou todas as transições de estado de política podem ser consultadas. Os resultados podem ser filtrados, agrupados e agregaçãos de grupo podem ser computados.

## EXEMPLOS

### Exemplo 1: Obter estados de política mais recentes no escopo de assinatura atual
```powershell
PS C:\> Get-AzPolicyState
```

Obtém os registros de estado de política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto atual da sessão.

### Exemplo 2: Obter estados de política mais recentes no escopo de assinatura especificado
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Obtém os registros de estado de política mais recentes gerados no último dia para todos os recursos dentro da assinatura especificada.

### Exemplo 3: Obter todos os estados de política no escopo de assinatura atual
```powershell
PS C:\> Get-AzPolicyState -All
```

Obtém todos os registros de estado de política histórica (incluindo os mais recentes) gerados no último dia para todos os recursos dentro da assinatura no contexto atual da sessão.

### Exemplo 4: Obter estados de política mais recentes no escopo do grupo de gerenciamento
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

Obtém os registros de estado de política mais recentes gerados no último dia para todos os recursos dentro do grupo de gerenciamento especificado.

### Exemplo 5: Obter estados de política mais recentes no escopo do grupo de recursos na assinatura atual
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

Obtém os registros de estado de política mais recentes gerados no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura no contexto atual da sessão).

### Exemplo 6: Obter estados de política mais recentes no escopo do grupo de recursos na assinatura especificada
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Obtém os registros de estado de política mais recentes gerados no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura especificada).

### Exemplo 7: Obter estados de política mais recentes para um recurso
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Obtém os registros de estado de política mais recentes gerados no último dia do recurso especificado.

### Exemplo 8: Obter estados de política mais recentes para uma definição de conjunto de políticas na assinatura atual
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Obtém os registros de estado de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto atual da sessão) e efetivados pela definição do conjunto de políticas especificado (que existe na assinatura no contexto da sessão atual).

### Exemplo 9: Obter estados de política mais recentes para uma definição de conjunto de políticas na assinatura especificada
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Obtém os registros de estado de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) efetivados pela definição de conjunto de políticas especificado (que existe na assinatura especificada).

### Exemplo 10: Obter estados de política mais recentes para uma definição de política na assinatura atual
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Obtém os registros de estado de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela definição de política especificada (que existe na assinatura no contexto da sessão atual).

### Exemplo 11: Obter estados de política mais recentes para uma definição de política na assinatura especificada
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Obtém os registros de estado de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela definição de política especificada (que existe na assinatura especificada).

### Exemplo 12: Obter estados de política mais recentes para uma atribuição de política na assinatura atual
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Obtém os registros de estado de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela atribuição de política especificada (que existe na assinatura no contexto da sessão atual).

### Exemplo 13: Obter estados de política mais recentes para uma atribuição de política na assinatura especificada
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Obtém os registros de estado de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto atual da sessão) e efetivados pela atribuição de política especificada (que existe na assinatura especificada).

### Exemplo 14: Obter estados de política mais recentes para uma atribuição de política no grupo de recursos especificado na assinatura atual
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Obtém os registros de estado de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela atribuição de política especificada (que existe no grupo de recursos na assinatura no contexto de sessão atual).

### Exemplo 15: Obter estados de política mais recentes no escopo de assinatura atual, com opções de consulta OrderBy, Top e Select
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

Obtém os registros de estado de política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto atual da sessão. O comando ordena os resultados por propriedades de nome de atribuição de data e hora e assume apenas o top 5 daqueles listados nessa ordem.
Ele também seleciona listar apenas um subconjunto das colunas para cada registro.

### Exemplo 16: Obter estados de política mais recentes no escopo de assinatura atual, com opções de consulta De e Para
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Obtém os registros de estado de política mais recentes gerados dentro do intervalo de datas especificado para todos os recursos dentro da assinatura no contexto atual da sessão.

### Exemplo 17: Obter estados de política mais recentes no escopo de assinatura atual, com a opção De consulta filter
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

Obtém os registros de estado de política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto atual da sessão.
O comando limita os resultados retornados pela filtragem com base na ação de definição de política (inclui ações de negação ou auditoria), status de conformidade (inclui apenas status não compatível) e local do recurso (exclui o local do eastus).

### Exemplo 18: Obter estados de política mais recentes no escopo de assinatura atual, com Aplicar especificando agregação de contagem de linhas
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

Obtém o número de registros de estado de política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto atual da sessão.
O comando retorna a contagem apenas dos registros de estado da política, que é retornada dentro da propriedade AdditionalProperties.

### Exemplo 19: Obter estados de política mais recentes no escopo de assinatura atual, com Aplicar especificando o grupo com agregação
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

Obtém os registros de estado de política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto atual da sessão. O comando limita os resultados retornados pela filtragem com base no status de conformidade (inclui apenas o status não compatível).
Ele agrupa os resultados com base na atribuição de política, definição de conjunto de políticas e definição de política e calcula o número de registros em cada grupo, que é retornado dentro da propriedade AdditionalProperties.
Ele ordena os resultados pela agregação de contagem em ordem decrescente e leva apenas o top 5 dos listados nessa ordem.

### Exemplo 20: Obter estados de política mais recentes no escopo de assinatura atual, com Aplicar especificando agrupação sem agregação
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

Obtém os registros de estado de política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto atual da sessão. O comando limita os resultados retornados pela filtragem com base no status de conformidade (inclui apenas o status não compatível).
Ele grupos os resultados com base na ID do recurso. Isso gera a lista de todos os recursos dentro da assinatura que não são compatíveis com pelo menos uma política.

### Exemplo 21: Obter estados de política mais recentes no escopo de assinatura atual, com Aplicar especificando vários agrupamentos
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### Exemplo 22: Obter estados de política mais recentes, incluindo detalhes de avaliação de política para um recurso
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

Obtém os registros de estado de política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto atual da sessão. O comando limita os resultados retornados pela filtragem com base no status de conformidade (inclui apenas o status não compatível).
Ele grupos os resultados primeiro com base na atribuição de política, definição de conjunto de políticas, definição de política e id de recurso. Em seguida, ele agrupa ainda mais os resultados desse grupo com as mesmas propriedades, exceto a ID do recurso, e calcula o número de registros em cada um desses grupos, que é retornado dentro da propriedade AdditionalProperties.
Ele ordena os resultados pela agregação de contagem em ordem decrescente e leva apenas o top 5 dos listados nessa ordem.
Isso gera as cinco principais políticas com o maior número de recursos não compatíveis.

## PARÂMETROS

### -All
Dentro do intervalo de tempo especificado, obter todos os estados de política em vez do somente mais recente.

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

### -Apply
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

### -Expand
Expanda a expressão usando a notação OData.

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

### -Filter
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

### -From
Data/hora formatada da ISO 8601 especificando a hora de início do intervalo a ser consultado.
Quando não especificado, o valor do parâmetro 'To' é padrão menos 1 dia.

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

### -Select
Selecione expressão usando a notação OData.
Um ou mais nomes de coluna separados por vírgulas.
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

### -To
Data/hora formatada da ISO 8601 especificando a hora de término do intervalo a ser consultado.
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

### -Top
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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## SAÍDAS

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState

## NOTES

## LINKS RELACIONADOS

[Get-AzPolicyStateSummary](./Get-AzPolicyStateSummary.md)
