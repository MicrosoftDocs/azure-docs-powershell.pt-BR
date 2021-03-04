---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: 2af8125f91618cd929a9389d9327532376e92af1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890427"
---
# Get-AzEventGridTopic

## SYNOPSIS
Obtém os detalhes de um tópico de Grade de Eventos ou obtém uma lista de todos os tópicos da Grade de Eventos na assinatura atual do Azure.

## SINTAXE

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

## DESCRIPTION
O Get-AzEventGridTopic cmdlet obtém os detalhes de um Tópico de Grade de Eventos especificado ou uma lista de todos os tópicos da Grade de Eventos na assinatura atual do Azure.
Se o nome do tópico for fornecido, os detalhes de um único Tópico de Grade de Eventos serão retornados.
Se o nome do tópico não for fornecido, uma lista de tópicos será retornada. O número de elementos retornados nesta lista é controlado pelo parâmetro Top. Se o valor Top não for especificado ou $null, a lista conterá todos os itens de tópicos. Caso contrário, Top indicará o número máximo de elementos a serem retornados na lista.
Se mais tópicos ainda estão disponíveis, o valor em NextLink deve ser usado na próxima chamada para obter a próxima página de tópicos.
Por fim, o parâmetro ODataQuery é usado para executar a filtragem dos resultados da pesquisa. A consulta de filtragem segue a sintaxe OData usando apenas a propriedade Name. As operações com suporte incluem: CONTAINS, eq (para igual), ne (para não igual), AND, OR e NOT.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

Obtém os detalhes do tópico de Grade de Eventos1 no grupo de recursos \` \` \` MyResourceGroupName \` .

### Exemplo 2
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

Obtém os detalhes do tópico de Grade de Eventos1 no grupo de recursos \` \` \` MyResourceGroupName \` .

### Exemplo 3
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

Listar todos os tópicos da Grade de Eventos no grupo de recursos \` MyResourceGroupName \` sem paginação.

### Exemplo 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

Listar os primeiros 10 tópicos da Grade de Eventos (se for o caso) no grupo de recursos MyResourceGroupName que atenda ao $odataFilter \` \` consulta. Se mais resultados estão disponíveis, a $result. O NextLink não será $null. Para obter as próximas páginas de tópicos, espera-se que o usuário chame Get-AzEventGridTopic e use o resultado. NextLink obtido da chamada anterior. O chamador deve parar quando o resultado. O NextLink se torna $null.

### Exemplo 5
```powershell
PS C:\> Get-AzEventGridTopic
```

Listar todos os tópicos da Grade de Eventos na assinatura sem paginação.

### Exemplo 6
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

Listar os primeiros 10 tópicos da Grade de Eventos (se algum) na assinatura que atenda ao $odataFilter consulta. Se mais resultados estão disponíveis, a $result. O NextLink não será $null. Para obter as próximas páginas de tópicos, espera-se que o usuário chame Get-AzEventGridTopic e use o resultado. NextLink obtido da chamada anterior. O chamador deve parar quando o resultado. O NextLink se torna $null.

## PARÂMETROS

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure

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

### -Name
Nome do tópico EventGrid.

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
O link para a próxima página de recursos a serem obtidos. Esse valor é obtido com a primeira chamada Get-AzEventGrid cmdlet quando mais recursos ainda estão disponíveis para consulta.

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
A consulta OData usada para filtrar os resultados da lista. Atualmente, a filtragem é permitida somente na propriedade Name. As operações com suporte incluem: CONTAINS, eq (para igual), ne (para não igual), AND, OR e NOT.

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
Nome do Grupo de Recursos.

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
Identificador de Recurso que representa o Tópico da Grade de Eventos.

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

### -Top
O número máximo de recursos a serem obtidos. O valor válido está entre 1 e 100. Se o valor superior for especificado e mais resultados ainda estão disponíveis, o resultado conterá um link para a próxima página a ser consultada no NextLink. Se o valor Top não for especificado, a lista completa de recursos será retornada de uma só vez.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

### System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## SAÍDAS

### Microsoft.Azure.Commands.EventGrid.Models.PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance

## NOTES

## LINKS RELACIONADOS
