---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: df3f6673729a868e7aeb349a34fba32b2033862e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115324"
---
# Get-AzEventGridTopic

## Sinopse
Obtém os detalhes de um tópico de Grade do Evento ou obtém uma lista de todos os tópicos da Grade do Evento na assinatura atual do Azure.

## Sintaxe

### ResourceGroupNameParameterSet (Padrão)
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### TopicNameParameterSet
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O Get-AzEventGridTopic cmdlet obtém os detalhes de um Tópico de Grade de Evento especificado ou uma lista de todos os tópicos da Grade do Evento na assinatura atual do Azure.
Se o nome do tópico for fornecido, os detalhes de um único Tópico da Grade do Evento serão retornados.
Se o nome do tópico não for fornecido, uma lista de tópicos será retornada. O número de elementos retornados nesta lista é controlado pelo parâmetro Superior. Se o valor Superior não for especificado ou $null, a lista conterá todos os itens de tópicos. Caso contrário, a parte superior indicará o número máximo de elementos a serem retornados na lista.
Se mais tópicos ainda estão disponíveis, o valor no NextLink deve ser usado na próxima chamada para obter a próxima página de tópicos.
Por fim, o parâmetro ODataQuery é usado para executar a filtragem dos resultados da pesquisa. A consulta de filtragem segue a sintaxe OData usando apenas a propriedade Nome. As operações com suporte incluem: CONTAINS, eq (para igual), ne (para não igual), AND, OR e NOT.

## Exemplos

### Exemplo 1
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

Obtém os detalhes do tópico da Grade do Evento1 no grupo \` \` de recursos \` MyResourceGroupName. \`

### Exemplo 2
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

Obtém os detalhes do tópico da Grade do Evento1 no grupo \` \` de recursos \` MyResourceGroupName. \`

### Exemplo 3
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

Liste todos os tópicos da Grade do Evento no grupo de recursos \` MyResourceGroupName \` sem paginação.

### Exemplo 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

Liste os primeiros 10 tópicos da Grade do Evento (se for o caso) no grupo de recursos MyResourceGroupName que satisfaça a $odataFilter \` \` consulta. Se mais resultados estão disponíveis, a $result. O NextLink não será $null. Para obter as próximas páginas de tópicos, espera-se que o usuário ligue Get-AzEventGridTopic e use o resultado. NextLink obtido da chamada anterior. O chamador deve parar quando o resultado for. O NextLink se torna $null.

### Exemplo 5
```powershell
PS C:\> Get-AzEventGridTopic
```

Liste todos os tópicos da Grade do Evento na assinatura sem paginação.

### Exemplo 6
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

Liste os primeiros 10 tópicos da Grade do Evento (se for o caso) na assinatura que satisfaça a $odataFilter consulta. Se mais resultados estão disponíveis, a $result. O NextLink não será $null. Para obter as próximas páginas de tópicos, espera-se que o usuário ligue Get-AzEventGridTopic e use o resultado. NextLink obtido da chamada anterior. O chamador deve parar quando o resultado for. O NextLink se torna $null.

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

### -Nome
Nome do tópico do EventGrid.

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
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
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
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
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Identificador de Recurso representando o Tópico da Grade do Evento.

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Superior
O número máximo de recursos a serem obtidos. O valor válido está entre 1 e 100. Se o valor superior for especificado e mais resultados ainda estarão disponíveis, o resultado conterá um link para a próxima página a ser consultada no NextLink. Se o valor Superior não for especificado, a lista completa de recursos será retornada ao mesmo tempo.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
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

### System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## Saídas

### Microsoft.Azure.Commands.EventGrid.Models.PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance

## Notas

## LINKS RELACIONADOS
