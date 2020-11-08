---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: ad622662615e74908c3d34c513e8570286b76297
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118069"
---
# Get-AzPolicyStateSummary

## Sinopse
Obtém o resumo dos Estados mais recentes de conformidade com a política para recursos.

## SYNTAX

### SubscriptionScope (padrão)
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
Obtém um resumo dos números de estado de conformidade da política mais recentes em vários escopos, divididos em atribuições de política e definições de política. Ele inclui apenas Estados de política não compatíveis.

## EXEMPLOS

### Exemplo 1: obter o resumo dos Estados mais recentes da política não compatível com o escopo atual da assinatura
```powershell
PS C:\> Get-AzPolicyStateSummary
```

Obtém a exibição resumida dos últimos Estados de conformidade com a política gerado no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.

### Exemplo 2: obter o resumo de Estados da política sem conformidade mais recente no escopo de assinatura especificado
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Obtém a exibição resumida dos últimos Estados de conformidade com a política gerado no último dia para todos os recursos dentro da assinatura especificada.

### Exemplo 3: obter o resumo dos Estados da política não compatível mais recentes no escopo do grupo de gerenciamento
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

Obtém a exibição resumida dos últimos Estados de conformidade com a política gerado no último dia para todos os recursos dentro do grupo de gerenciamento especificado.

### Exemplo 4: obter o resumo dos Estados da política não compatível mais recentes no escopo do grupo de recursos na assinatura atual
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

Obtém a exibição resumida dos últimos Estados de conformidade com a política gerado no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura no contexto atual da sessão).

### Exemplo 5: obter o resumo dos Estados da política não compatível mais recentes no escopo do grupo de recursos na assinatura especificada
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Obtém a exibição resumida dos últimos Estados de conformidade com a política gerado no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura especificada).

### Exemplo 6: obter o resumo de Estados da política não compatível mais recente para um recurso
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Obtém a exibição resumida dos últimos Estados de conformidade com a política gerado no último dia do recurso especificado.

### Exemplo 7: obter o resumo de Estados da política não compatível mais recente para uma definição de conjunto de políticas na assinatura atual
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Obtém a exibição de resumo dos últimos Estados de conformidade de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela definição do conjunto de políticas especificado (que existe na assinatura no contexto atual da sessão).

### Exemplo 8: obter o resumo de Estados da política não compatível mais recente para uma definição de conjunto de políticas na assinatura especificada
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Obtém a exibição de resumo dos últimos Estados de conformidade de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela definição do conjunto de políticas especificado (que existe na assinatura especificada).

### Exemplo 9: obter o resumo de Estados da política não compatível mais recentes para uma definição de política na assinatura atual
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Obtém a exibição de resumo dos últimos Estados de conformidade com a política gerado no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela definição de política especificada (que existe na assinatura do contexto de sessão atual).

### Exemplo 10: obter o resumo de Estados da política não compatível mais recente para uma definição de política na assinatura especificada
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Obtém a exibição de resumo dos últimos Estados de conformidade com a política gerado no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela definição de política especificada (que existe na assinatura especificada).

### Exemplo 11: obter o resumo de Estados da política sem conformidade mais recente para uma atribuição de política na assinatura atual
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Obtém a exibição de resumo dos últimos Estados de conformidade com a política gerado no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela atribuição de política especificada (que existe na assinatura no contexto da sessão atual).

### Exemplo 12: obter o resumo de Estados da política não compatível mais recente para uma atribuição de política na assinatura especificada
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Obtém a exibição de resumo dos últimos Estados de conformidade com a política gerado no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela atribuição de política especificada (que existe na assinatura especificada).

### Exemplo 13: obter o resumo de Estados da política sem conformidade mais recente para uma atribuição de política no grupo de recursos especificado na assinatura atual
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Obtém a exibição de resumo dos últimos Estados de conformidade com a política gerado no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela atribuição de política especificada (que existe no grupo de recursos na assinatura do contexto de sessão atual).

### Exemplo 14: obter o resumo dos Estados mais recentes da política não compatível com o escopo atual da assinatura, com a opção de consulta superior
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

Obtém a exibição resumida dos últimos Estados de conformidade com a política gerado no último dia para todos os recursos dentro da assinatura no contexto de sessão atual. O comando ordena os resumos da atribuição de política nos resultados por conta de recurso não compatível em ordem decrescente, e usa apenas 5 principais dos resumos da atribuição de política.

### Exemplo 15: obter o resumo de Estados da política sem conformidade mais recente no escopo atual da assinatura, com opções de consulta de e até
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Obtém a exibição de resumo dos últimos Estados de conformidade de política gerado dentro do intervalo de datas especificado para todos os recursos dentro da assinatura no contexto de sessão atual.

### Exemplo 16: obter o resumo dos Estados mais recentes da política não compatível com o escopo atual da assinatura, com a opção filtrar consulta
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Obtém a exibição resumida dos últimos Estados de conformidade com a política gerado no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.
O comando limita os resultados retornados pela filtragem com base na ação de definição da política (inclui ações de negação ou auditoria) e local do recurso (exclui o local do lesteus).

## OS

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

### Microsoft. Azure. Commands. PolicyInsights. Models. PolicyStateSummary

## INFORMA

## LINKS RELACIONADOS

[Get-AzPolicyState](./Get-AzPolicyState.md)
