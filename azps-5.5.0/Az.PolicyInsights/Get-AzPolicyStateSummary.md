---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: ad622662615e74908c3d34c513e8570286b76297
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118200"
---
# Get-AzPolicyStateSummary

## Sinopse
Obtém um resumo dos estados de conformidade de política mais recentes para os recursos.

## Sintaxe

### SubscriptionScope (Padrão)
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

### Resourcescope
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
Obtém uma exibição resumo dos números de estado de conformidade de política mais recentes em vários escopos, divididos em atribuições de política e definições de política. Ele inclui apenas estados de política não compatíveis.

## Exemplos

### Exemplo 1: Obter o resumo mais recente dos estados de política não compatíveis no escopo da assinatura atual
```powershell
PS C:\> Get-AzPolicyStateSummary
```

Obtém a exibição resumo dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto da sessão atual.

### Exemplo 2: Obter o resumo mais recente dos estados de política não compatíveis no escopo de assinatura especificado
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Obtém a exibição resumo dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos dentro da assinatura especificada.

### Exemplo 3: Obter o resumo mais recente dos estados de política não compatíveis no escopo do grupo de gerenciamento
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

Obtém a exibição resumo dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos do grupo de gerenciamento especificado.

### Exemplo 4: Obter o resumo mais recente dos estados de política não compatíveis no escopo do grupo de recursos na assinatura atual
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

Obtém a exibição resumo dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura no contexto de sessão atual).

### Exemplo 5: Obter o resumo mais recente dos estados de política não compatíveis no escopo do grupo de recursos na assinatura especificada
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Obtém a exibição resumo dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura especificada).

### Exemplo 6: Obter o resumo mais recente dos estados de política não compatíveis para um recurso
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Obtém a exibição resumo dos estados de conformidade de política mais recentes gerados no último dia para o recurso especificado.

### Exemplo 7: Obter o resumo mais recente dos estados de política não compatíveis para uma definição de conjunto de políticas na assinatura atual
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Obtém a exibição resumo dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela definição de conjunto de política especificada (que existe na assinatura no contexto de sessão atual).

### Exemplo 8: Obter o resumo mais recente dos estados de política não compatíveis para uma definição de conjunto de políticas na assinatura especificada
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Obtém a exibição resumo dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela definição de conjunto de política especificada (que existe na assinatura especificada).

### Exemplo 9: Obter o resumo mais recente dos estados de política não compatíveis para uma definição de política na assinatura atual
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Obtém a exibição resumo dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela definição de política especificada (que existe na assinatura no contexto de sessão atual).

### Exemplo 10: Obter o resumo mais recente dos estados de política não compatíveis para uma definição de política na assinatura especificada
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Obtém a exibição resumo dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela definição de política especificada (que existe na assinatura especificada).

### Exemplo 11: Obter o resumo mais recente dos estados de política não compatíveis para uma atribuição de política na assinatura atual
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Obtém a exibição resumo dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela atribuição de política especificada (que existe na assinatura no contexto de sessão atual).

### Exemplo 12: Obter o resumo mais recente dos estados de política não compatíveis para uma atribuição de política na assinatura especificada
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Obtém a exibição resumo dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela atribuição de política especificada (que existe na assinatura especificada).

### Exemplo 13: Obter o resumo mais recente dos estados de política não compatíveis para uma atribuição de política no grupo de recursos especificado na assinatura atual
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Obtém a exibição resumo dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela atribuição de política especificada (que existe no grupo de recursos na assinatura no contexto de sessão atual).

### Exemplo 14: Obter o resumo mais recente dos estados de política não compatíveis no escopo da assinatura atual, com a opção De consulta Superior
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

Obtém a exibição resumo dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto da sessão atual. O comando ordena os resumos de atribuição de política nos resultados por contagens de recursos não compatíveis em ordem decrescente e leva apenas os cinco primeiros resumos dessas atribuições de política.

### Exemplo 15: Obter o resumo mais recente dos estados de política não compatíveis no escopo da assinatura atual, com as opções de consulta De e Para
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Obtém a exibição resumo dos estados de conformidade de política mais recentes gerados dentro do intervalo de datas especificado para todos os recursos dentro da assinatura no contexto da sessão atual.

### Exemplo 16: Obter o resumo mais recente dos estados de política não compatíveis no escopo da assinatura atual, com a opção de consulta Filtro
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Obtém a exibição resumo dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto da sessão atual.
O comando limita os resultados retornados pela filtragem com base na ação de definição de política (inclui ações de negação ou auditoria) e local do recurso (exclui o local do leste).

## Parâmetros

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
ISO 8601 data/hora formatada especificando a hora de término do intervalo para consulta.
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

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary

## Notas

## LINKS RELACIONADOS

[Get-AzPolicyState](./Get-AzPolicyState.md)
