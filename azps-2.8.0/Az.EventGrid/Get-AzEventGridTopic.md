---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: 2bae39bb6a3e0c08a86118ce9ed8f9c6fadf82c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596533"
---
# Get-AzEventGridTopic

## Sinopse
Obtém os detalhes de um tópico de grade de evento ou obtém uma lista de todos os tópicos de grade de eventos na assinatura atual do Azure.

## SYNTAX

### ResourceGroupNameParameterSet (padrão)
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

## DESCRITIVO
O cmdlet Get-AzEventGridTopic Obtém os detalhes de um tópico de grade de evento especificado ou uma lista de todos os tópicos de grade de eventos na assinatura atual do Azure.
Se o nome do tópico for fornecido, os detalhes de um único tópico da grade do evento serão retornados.
Se o nome do tópico não for fornecido, uma lista de tópicos será retornada. O número de elementos retornados nessa lista é controlado pelo parâmetro Top. Se o valor superior não for especificado ou $null, a lista conterá todos os itens de tópicos. Caso contrário, o superior indicará o número máximo de elementos a serem retornados na lista.
Se mais tópicos ainda estiverem disponíveis, o valor em NextLink deve ser usado na próxima chamada para obter a próxima página de tópicos.
Por fim, o parâmetro ODataQuery é usado para executar a filtragem dos resultados da pesquisa. A consulta filtragem segue a sintaxe OData usando somente a propriedade Name. As operações com suporte incluem: CONTAINS, EQ (para igual), ne (para não igual) e, ou e não.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

Obtém os detalhes do tópico de grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .

### Exemplo 2
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

Obtém os detalhes do tópico de grade de eventos \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .

### Exemplo 3
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

Listar todos os tópicos da grade de eventos no grupo de MyResourceGroupName de recursos \` \` sem paginação.

### Exemplo 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

Liste os 10 primeiros tópicos de grade de eventos (se houver) no grupo de MyResourceGroupName de grupo \` \` que satisfaz a $odataFilter consulta. Se houver mais resultados disponíveis, o $result. NextLink não será $null. Para obter a próxima página (s) de tópicos, espera-se que o usuário chame novamente Get-AzEventGridTopic e use o resultado. NextLink obtidos na chamada anterior. O chamador deve parar quando o resultado for. NextLink se torna $null.

### Exemplo 5
```powershell
PS C:\> Get-AzEventGridTopic
```

Liste todos os tópicos da grade de eventos na assinatura sem paginação.

### Exemplo 6
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

Liste os 10 primeiros tópicos de grade de eventos (se houver) na assinatura que satisfaz o $odataFilter consulta. Se houver mais resultados disponíveis, o $result. NextLink não será $null. Para obter a próxima página (s) de tópicos, espera-se que o usuário chame novamente Get-AzEventGridTopic e use o resultado. NextLink obtidos na chamada anterior. O chamador deve parar quando o resultado for. NextLink se torna $null.

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

### -Nome
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
Identificador de recurso que representa o tópico da grade do evento.

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

### -Início
O número máximo de recursos a serem obtidos. O valor válido é entre 1 e 100. Se o valor principal for especificado e mais resultados ainda estiverem disponíveis, o resultado conterá um link para a próxima página a ser consultada no NextLink. Se o valor principal não for especificado, a lista completa de recursos será retornada ao mesmo tempo.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

### System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

## EXIBE

### Microsoft. Azure. Commands. EventGrid. Models. PSTopic

### Microsoft. Azure. Commands. EventGrid. Models. PSTopicListInstance

## INFORMA

## LINKS RELACIONADOS
