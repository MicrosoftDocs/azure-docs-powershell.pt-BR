---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 24a42fba23427f437cb064e1915c19e36e7a71bf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258745"
---
# New-AzNotificationHubsNamespace

## Sinopse
Cria um namespace do hub de notificação.

## SYNTAX

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzNotificationHubsNamespace** cria um namespace Hub de notificação.
Namespaces são recipientes lógicos que ajudam você a organizar e gerenciar seus hubs de notificação.
Você deve ter pelo menos um namespace de Hub de notificação.
Um único namespace pode alojar vários hubs.
Você pode ter vários namespaces para organizar seus hubs ou para dar a pessoas específicas permissão para gerenciar um subconjunto selecionado de seus hubs.
Para criar um namespace, certifique-se de especificar um nome exclusivo para o namespace; Especifique o datacenter onde o namespace será localizado; e especifique o grupo de recursos ao qual o namespace será atribuído.
Após a criação do namespace, você pode usar o cmdlet New-AzNotificationHubsNamespaceAuthorizationRules para atribuir regras de autorização a esse namespace.
Regras de autorização são usadas para gerenciar permissões para o namespace.

## EXEMPLOS

### Exemplo 1: criar um hub de notificação
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

Esse comando cria um hub de notificação chamado ContosoPartners.
O namespace estará localizado no centro de data do oeste dos EUA e será atribuído ao grupo de recursos ContosoNotificationsGroup.

### Exemplo 2: criar um hub de notificação com marcas
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

Esse comando cria um hub de notificação chamado ContosoPartners.
O namespace estará localizado no centro de data do oeste dos EUA e será atribuído ao grupo de recursos ContosoNotificationsGroup.
Além disso, esse comando cria uma marca com o nome Audience e o valor PartnerOrganizations e é atribuído ao namespace.
Isso garante que o namespace será exibido sempre que você filtrar itens em que a marca de audiência estiver definida como PartnerOrganizations.

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

### -Local
Especifica o nome de exibição do datacenter que irá hospedar o namespace.
Embora você possa definir esse parâmetro como qualquer local válido para obter um desempenho ideal, talvez queira usar um Datacenter localizado próximo à maioria dos usuários.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Especifica o nome do novo namespace.
Os namespaces fornecem uma maneira de agrupar e categorizar os hubs de notificação.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Resource
Especifica o grupo de recursos ao qual o namespace será atribuído.
Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento e administração de inventário.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkuTier
Nível de SKU do namespace

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Marca
Especifica pares de nomes e valores que podem ser usados para categorizar e organizar os itens do Azure.
A função marcas é semelhante a palavras-chave e operam em uma implantação.
Por exemplo, se você Pesquisar todos os itens com o departamento de marcas: ele a pesquisa retornará todos os itens do Azure que têm essa marca, independentemente de itens como tipo de item, local ou grupo de recursos.
Uma marca individual consiste em duas partes: o *nome* e, opcionalmente, o *valor*.
Por exemplo, no departamento: ele, o nome da marca é departamento e o valor da marca é.
Para adicionar uma marca, use a sintaxe de tabela de hash semelhante a essa, que cria a marca CalendarYear: 2016:

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

### System. Collections. Hashtable

## EXIBE

### Microsoft. Azure. Commands. NotificationHubs. Models. Namespaceattributes

## INFORMA

## LINKS RELACIONADOS

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


