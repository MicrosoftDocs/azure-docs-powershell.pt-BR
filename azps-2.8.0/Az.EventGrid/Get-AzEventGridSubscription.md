---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 987882928ee215ed2da842e924386f5dec8b862f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596536"
---
# Get-AzEventGridSubscription

## Sinopse
Obtém os detalhes de uma assinatura de evento ou obtém uma lista de todas as assinaturas de evento na assinatura atual do Azure.

## SYNTAX

### EventSubscriptionTopicNameParameterSet (padrão)
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### EventSubscriptionDomainNameParameterSet
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionTopicTypeNameParameterSet
```
Get-AzEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>] [[-Location] <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### EventSubscriptionCustomTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainInputObjectParameterSet
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Get-AzEventGridSubscription Obtém os detalhes de uma assinatura de grade de eventos especificada ou uma lista de todas as assinaturas de grade de eventos na assinatura atual do Azure ou no grupo de recursos.
Se o nome da assinatura do evento for fornecido, os detalhes de uma única assinatura de grade de eventos serão retornados.
Se o nome da assinatura do evento não for fornecido, uma lista de todas as assinaturas de eventos será retornada. O número de elementos retornados nessa lista é controlado pelo parâmetro Top. Se o valor superior não for especificado ou $null, a lista conterá todos os itens de assinatura do evento. Caso contrário, o superior indicará o número máximo de elementos a serem retornados na lista.
Se mais assinaturas de evento ainda estiverem disponíveis, o valor em NextLink deve ser usado na próxima chamada para obter a próxima página de assinaturas de evento.
Por fim, o parâmetro ODataQuery é usado para executar a filtragem dos resultados da pesquisa. A consulta filtragem segue a sintaxe OData usando somente a propriedade Name. As operações com suporte incluem: CONTAINS, EQ (para igual), ne (para não igual) e, ou e não.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

Obtém os detalhes da assinatura de evento \` EventSubscription1 \` criado para o tópico \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .

### Exemplo 2
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

Obtém os detalhes da assinatura de evento \` EventSubscription1 \` criado para \` o tópico tópico1 \` no grupo de recursos \` MyResourceGroupName \` , incluindo a URL de ponto de extremidade completa se for uma assinatura de evento baseada em webhook.

### Exemplo 3
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

Obtenha uma lista de todas as assinaturas de evento criadas para o tópico \` tópico1 \` no grupo de \` MyResourceGroupName de recursos \` sem paginação.

### Exemplo 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Liste as 10 primeiras assinaturas de evento (se houver) criadas para \` o tópico tópico1 \` no grupo de MyResourceGroupName de recursos \` \` que satisfaz a consulta $odataFilter. Se houver mais resultados disponíveis, o $result. NextLink não será $null. Para obter próxima página (s) de assinaturas de evento, espera-se que o usuário chame novamente Get-AzEventGridSubscription e use o resultado. NextLink obtidos na chamada anterior. O chamador deve parar quando o resultado for. NextLink se torna $null.

### Exemplo 5
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

Obtém os detalhes da assinatura de evento \` EventSubscription1 \` criado para o grupo de MyResourceGroupName de recursos \` \` .

### Exemplo 6
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

Obtém os detalhes da assinatura de evento \` EventSubscription1 \` criada para a assinatura do Azure selecionada no momento.

### Exemplo 7
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

Obtém a lista de todas as assinaturas de eventos globais criadas sob a MyResourceGroupName do grupo de recursos \` \` sem paginação.

### Exemplo 8
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Liste as cinco primeiras assinaturas de evento (se houver) criadas em MyResourceGroupName do grupo de recursos \` \` que satisfaçam a consulta $odataFilter. Se houver mais resultados disponíveis, o $result. NextLink não será $null. Para obter próxima página (s) de assinaturas de evento, espera-se que o usuário chame novamente Get-AzEventGridSubscription e use o resultado. NextLink obtidos na chamada anterior. O chamador deve parar quando o resultado for. NextLink se torna $null.

### Exemplo 9
```powershell
PS C:\> Get-AzEventGridSubscription
```

Obtém a lista de todas as assinaturas de eventos globais criadas sob a assinatura do Azure selecionada atualmente, sem paginação.

### Exemplo 10
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Liste as 15 primeiras assinaturas de evento global (se houver) criadas sob a assinatura atualmente selecionada do Azure que satisfaz a consulta $odataFilter. Se houver mais resultados disponíveis, o $result. NextLink não será $null. Para obter próxima página (s) de assinaturas de evento, espera-se que o usuário chame novamente Get-AzEventGridSubscription e use o resultado. NextLink obtidos na chamada anterior. O chamador deve parar quando o resultado for. NextLink se torna $null.

### Exemplo 11
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

Obtém a lista de todas as assinaturas de eventos regionais criadas em MyResourceGroupName do grupo de recursos \` \` no local especificado \` westus2 \` sem paginação.

### Exemplo 12
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Liste as 15 primeiras assinaturas de evento regional (se houver) criadas em MyResourceGroupName de \` grupo \` de recursos no local especificado \` westus2 \` que satisfaz a consulta $odataFilter. Se houver mais resultados disponíveis, o $result. NextLink não será $null. Para obter próxima página (s) de assinaturas de evento, espera-se que o usuário chame novamente Get-AzEventGridSubscription e use o resultado. NextLink obtidos na chamada anterior. O chamador deve parar quando o resultado for. NextLink se torna $null.

### Exemplo 13
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

Obtém a lista de todas as assinaturas de evento criadas para o namespace do EventHub especificado sem paginação.

### Exemplo 14
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Liste as 25 primeiras assinaturas de evento (se houver) criadas para o namespace do EventHub especificado que satisfaz o $odataFilter consulta. Se houver mais resultados disponíveis, o $result. NextLink não será $null. Para obter próxima página (s) de assinaturas de evento, espera-se que o usuário chame novamente Get-AzEventGridSubscription e use o resultado. NextLink obtidos na chamada anterior. O chamador deve parar quando o resultado for. NextLink se torna $null.

### Exemplo 15
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

Obtém a lista de todas as assinaturas de evento criadas para o tipo de tópico especificado (namespaces do EventHub) no local especificado sem paginação.

### Exemplo 16
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Liste as 15 primeiras assinaturas de evento (se houver) criadas para o tipo de tópico especificado (namespaces do EventHub) no local especificado que satisfaz a consulta $odataFilter. Se houver mais resultados disponíveis, o $result. NextLink não será $null. Para obter próxima página (s) de assinaturas de evento, espera-se que o usuário chame novamente Get-AzEventGridSubscription e use o resultado. NextLink obtidos na chamada anterior. O chamador deve parar quando o resultado for. NextLink se torna $null.

### Exemplo 17
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

Obtém a lista de todas as assinaturas de evento criadas para o grupo de recursos específico sem paginação.

### Exemplo 18
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Liste as primeiras 100 assinaturas de evento (se houver) criadas para o grupo de recursos específico que satisfaz a consulta $odataFilter. Se houver mais resultados disponíveis, o $result. NextLink não será $null. Para obter próxima página (s) de assinaturas de evento, espera-se que o usuário chame novamente Get-AzEventGridSubscription e use o resultado. NextLink obtidos na chamada anterior. O chamador deve parar quando o resultado for. NextLink se torna $null.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### -DomainInputObject
Objeto de domínio EventGrid.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DomainName
Nome de domínio EventGrid.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DomainTopicInputObject
Objeto de tópico do domínio EventGrid.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DomainTopicName
Nome do tópico do domínio EventGrid.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventSubscriptionName
O nome da assinatura do evento

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeFullEndpointUrl
Inclua a URL completa de ponto de extremidade do destino da assinatura do evento.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Objeto de tópico EventGrid.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Local
Ponto

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextLink
O link para a próxima página de recursos a ser obtida. Esse valor é obtido com a primeira chamada de cmdlet Get-AzEventGrid quando mais recursos ainda estão disponíveis para consulta.

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ODataQuery
A consulta OData usada para filtrar os resultados da lista. Atualmente, a filtragem só é permitida na propriedade Name. As operações com suporte incluem: CONTAINS, EQ (para igual), ne (para não igual) e, ou e não.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Identificador do recurso para o qual as assinaturas de eventos foram criadas.

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Início
A consulta OData usada para filtrar os resultados da lista. Atualmente, a filtragem só é permitida na propriedade Name. As operações com suporte incluem: CONTAINS, EQ (para igual), ne (para não igual) e, ou e não.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Topicname
Nome do tópico EventGrid.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicTypeName
Nome do tópico

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

### Microsoft. Azure. Commands. EventGrid. Models. PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSDomain

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic

### System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

## EXIBE

### Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription

## INFORMA

## LINKS RELACIONADOS
