---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 587e42ac4c9f318ff46381fdef5b09fa7ce55b63
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111901"
---
# Get-AzEventGridSubscription

## Sinopse
Obtém os detalhes de uma assinatura de evento ou obtém uma lista de todas as assinaturas de eventos na assinatura atual do Azure.

## Sintaxe

### EventSubscriptionTopicNameParameterSet (Padrão)
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainNameParameterSet
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionTopicTypeNameParameterSet
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
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

## Descrição
O Get-AzEventGridSubscription cmdlet obtém os detalhes de uma assinatura de Grade de Evento especificada ou uma lista de todas as assinaturas de Grade de Evento no grupo de recursos ou assinatura atual do Azure.
Se o nome da assinatura do evento for fornecido, os detalhes de uma única assinatura de Grade de Evento serão retornados.
Se o nome da assinatura do evento não for fornecido, uma lista de todas as assinaturas do evento será retornada. O número de elementos retornados nesta lista é controlado pelo parâmetro Superior. Se o valor Superior não for especificado ou $null, a lista conterá todos os itens da assinatura do evento. Caso contrário, a parte superior indicará o número máximo de elementos a serem retornados na lista.
Se mais assinaturas de eventos ainda estão disponíveis, o valor no NextLink deve ser usado na próxima chamada para obter a próxima página de assinaturas de eventos.
Por fim, o parâmetro ODataQuery é usado para executar a filtragem dos resultados da pesquisa. A consulta de filtragem segue a sintaxe OData usando apenas a propriedade Nome. As operações com suporte incluem: CONTAINS, eq (para igual), ne (para não igual), AND, OR e NOT.

## Exemplos

### Exemplo 1
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

Obtém os detalhes da assinatura do evento EventSubscription1 criada para tópico Tópico1 no grupo de recursos \` \` \` \` \` MyResourceGroupName. \`

### Exemplo 2
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

Obtém os detalhes da assinatura do evento EventSubscription1 criada para tópico1 no grupo de recursos \` \` \` \` \` MyResourceGroupName, incluindo \` a URL do ponto de extremidade completa se for uma assinatura de evento baseada na Web.

### Exemplo 3
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

Obter uma lista de todas as assinaturas de evento criadas para tópico Tópico1 no grupo de recursos \` \` \` MyResourceGroupName \` sem paginação.

### Exemplo 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Liste as 10 primeiras assinaturas de eventos (se alguma) criadas para tópico Tópico1 no grupo de recursos \` \` \` MyResourceGroupName que satisfaça a consulta \` $odataFilter edição. Se mais resultados estão disponíveis, a $result. O NextLink não será $null. Para obter as próximas páginas de assinaturas de eventos, espera-se que o usuário ligue Get-AzEventGridSubscription e use o resultado. NextLink obtido da chamada anterior. O chamador deve parar quando o resultado for. O NextLink se torna $null.

### Exemplo 5
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

Obtém os detalhes da assinatura do \` evento EventSubscription1 criada para o \` grupo de recursos \` MyResourceGroupName. \`

### Exemplo 6
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

Obtém os detalhes da assinatura \` do evento EventSubscription1 criada \` para a assinatura do Azure selecionada no momento.

### Exemplo 7
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

Obtém a lista de todas as assinaturas de eventos globais criadas no grupo de recursos \` MyResourceGroupName \` sem paginação.

### Exemplo 8
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Liste as cinco primeiras assinaturas de evento (se alguma) criadas no grupo de recursos MyResourceGroupName que satisfaça a $odataFilter \` \` consulta. Se mais resultados estão disponíveis, a $result. O NextLink não será $null. Para obter as próximas páginas de assinaturas de eventos, espera-se que o usuário ligue Get-AzEventGridSubscription e use o resultado. NextLink obtido da chamada anterior. O chamador deve parar quando o resultado for. O NextLink se torna $null.

### Exemplo 9
```powershell
PS C:\> Get-AzEventGridSubscription
```

Obtém a lista de todas as assinaturas de eventos globais criadas sob a assinatura do Azure selecionada no momento sem paginação.

### Exemplo 10
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Liste as primeiras 15 assinaturas globais de eventos (se alguma) criadas sob a assinatura do Azure selecionada no momento que satisfaz a $odataFilter consulta. Se mais resultados estão disponíveis, a $result. O NextLink não será $null. Para obter as próximas páginas de assinaturas de eventos, espera-se que o usuário ligue Get-AzEventGridSubscription e use o resultado. NextLink obtido da chamada anterior. O chamador deve parar quando o resultado for. O NextLink se torna $null.

### Exemplo 11
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

Obtém a lista de todas as assinaturas de eventos regionais criadas no grupo de recursos \` MyResourceGroupName no local \` especificado \` westus2 \` sem paginação.

### Exemplo 12
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Liste as primeiras 15 assinaturas de eventos regionais (se alguma) criadas no grupo de recursos MyResourceGroupName no local especificado \` westus2 que satisfaça a $odataFilter \` \` \` consulta. Se mais resultados estão disponíveis, a $result. O NextLink não será $null. Para obter as próximas páginas de assinaturas de eventos, espera-se que o usuário ligue Get-AzEventGridSubscription e use o resultado. NextLink obtido da chamada anterior. O chamador deve parar quando o resultado for. O NextLink se torna $null.

### Exemplo 13
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

Obtém a lista de todas as assinaturas de eventos criadas para o namespace do EventHub especificado sem paginação.

### Exemplo 14
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Liste as primeiras 25 assinaturas de evento (se alguma) criadas para o namespace de EventHub especificado que satisfaça a $odataFilter consulta. Se mais resultados estão disponíveis, a $result. O NextLink não será $null. Para obter as próximas páginas de assinaturas de eventos, espera-se que o usuário ligue Get-AzEventGridSubscription e use o resultado. NextLink obtido da chamada anterior. O chamador deve parar quando o resultado for. O NextLink se torna $null.

### Exemplo 15
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

Obtém a lista de todas as assinaturas de eventos criadas para o tipo de tópico especificado (namespaces do EventHub) no local especificado sem paginação.

### Exemplo 16
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Liste as primeiras 15 assinaturas de evento (se alguma) criadas para o tipo de tópico especificado (namespaces do EventHub) no local especificado que satisfaça a $odataFilter consulta. Se mais resultados estão disponíveis, a $result. O NextLink não será $null. Para obter as próximas páginas de assinaturas de eventos, espera-se que o usuário ligue Get-AzEventGridSubscription e use o resultado. NextLink obtido da chamada anterior. O chamador deve parar quando o resultado for. O NextLink se torna $null.

### Exemplo 17
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

Obtém a lista de todas as assinaturas de eventos criadas para o grupo de recursos específico sem paginação.

### Exemplo 18
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Liste as primeiras 100 assinaturas de eventos (se alguma) criadas para o grupo de recursos específico que satisfaça a $odataFilter consulta. Se mais resultados estão disponíveis, a $result. O NextLink não será $null. Para obter as próximas páginas de assinaturas de eventos, espera-se que o usuário ligue Get-AzEventGridSubscription e use o resultado. NextLink obtido da chamada anterior. O chamador deve parar quando o resultado for. O NextLink se torna $null.

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure

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
Objeto EventGrid Domain.

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
Objeto Tópico de Domínio do EventGrid.

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
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeFullEndpointUrl
Inclua a URL de ponto de extremidade completa do destino da assinatura do evento.

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
Objeto De Tópico do EventGrid.

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
Localização

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextLink
O link para a próxima página de recursos a ser obtido. Esse valor é obtido com a primeira chamada Get-AzEventGrid cmdlet quando mais recursos ainda estão disponíveis para consulta.

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
A consulta OData usada para filtrar os resultados da lista. No momento, a filtragem é permitida somente na propriedade Nome. As operações com suporte incluem: CONTAINS, eq (para igual), ne (para não igual), AND, OR e NOT.

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
Position: Named
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

### -Superior
A consulta OData usada para filtrar os resultados da lista. No momento, a filtragem é permitida somente na propriedade Nome. As operações com suporte incluem: CONTAINS, eq (para igual), ne (para não igual), AND, OR e NOT.

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

### -Nomedo Tópico
Nome do tópico do EventGrid.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicTypeName
Nome do TipoDo Tópico

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### System.String

### Microsoft.Azure.Commands.EventGrid.Models.PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSDomain

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic

### System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## Saídas

### Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription

## Notas

## LINKS RELACIONADOS
