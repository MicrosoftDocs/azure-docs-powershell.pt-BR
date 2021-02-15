---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 24a42fba23427f437cb064e1915c19e36e7a71bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114595"
---
# New-AzNotificationHubsNamespace

## Sinopse
Cria um namespace do hub de notificação.

## Sintaxe

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Descrição
O **cmdlet New-AzNotificationHubsNamespace** cria um namespace do hub de notificação.
Os namespaces são contêineres lógicos que ajudam você a organizar e gerenciar seus hubs de notificação.
Você deve ter pelo menos um espaço de nome do hub de notificação.
Um único namespace pode ter vários hubs.
Você pode ter vários namespaces para organizar seus hubs ou para dar permissão a indivíduos específicos para gerenciar um subconjunto selecionado de seus hubs.
Para criar um namespace, especifique um nome exclusivo para o namespace; especifique o datacenter onde o namespace estará localizado; e especifique o grupo de recursos ao qual o namespace será atribuído.
Depois que o namespace tiver sido criado, você poderá usar o cmdlet New-AzNotificationHubsNamespaceAuthorizationRules para atribuir regras de autorização a esse namespace.
As regras de autorização são usadas para gerenciar permissões para o namespace.

## Exemplos

### Exemplo 1: Criar um hub de notificação
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

Esse comando cria um hub de notificação chamado ContosoPartners.
O namespace será localizado no datacenter do Oeste dos EUA e será atribuído ao grupo de recursos ContosoNotificationsGroup.

### Exemplo 2: Criar um hub de notificação com marcas
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

Esse comando cria um hub de notificação chamado ContosoPartners.
O namespace será localizado no datacenter do Oeste dos EUA e será atribuído ao grupo de recursos ContosoNotificationsGroup.
Além disso, esse comando cria uma marca com o nome Audiência e o valor PartnerOrganizations e é atribuído ao namespace.
Isso garante que o namespace seja exibido sempre que você filtrar itens em que a marca Audiência está definida como PartnerOrganizações.

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

### -Local
Especifica o nome de exibição do datacenter que hospedará o Namespace.
Embora você possa definir esse parâmetro para qualquer local válido, para obter um desempenho ideal, talvez você queira usar um datacenter localizado próximo à maioria dos seus usuários.

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
Os namespaces oferecem uma maneira de agrupar e categorizar os hubs de notificação.

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

### -ResourceGroup
Especifica o grupo de recursos ao qual o namespace será atribuído.
Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento e administração de estoques.

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
Camada SKU do namespace

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

### -Tag
Especifica pares de nome e valor que podem ser usados para categorizar e organizar itens do Azure.
As marcas são semelhantes às palavras-chave e operam em uma implantação.
Por exemplo, se você pesquisar todos os itens com a marca Departamento:TI, a pesquisa retornará todos os itens do Azure que têm essa marca, independentemente de itens como tipo de item, local ou grupo de recursos.
Uma marca individual consiste em duas partes: o *Nome* e, opcionalmente, o *Valor.*
Por exemplo, em Departamento:IT, o nome da marca é Departamento e o valor da marca é IT.
Para adicionar uma marca, use a sintaxe da tabela hash semelhante a esta, que cria a marca CalendarYear:2016:

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

### -Confirmar
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
Mostra o que acontece se o cmdlet for executado. O cmdlet não é executado.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### System.String

### System.Collections.Hashtable

## Saídas

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## Notas

## LINKS RELACIONADOS

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


