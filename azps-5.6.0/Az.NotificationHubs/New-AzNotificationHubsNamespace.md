---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 20a4da67030962a238838247a7dcf137208e56b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885293"
---
# New-AzNotificationHubsNamespace

## SYNOPSIS
Cria um namespace de hub de notificação.

## SINTAXE

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **New-AzNotificationHubsNamespace** cria um namespace de hub de notificação.
Namespaces são contêineres lógicos que ajudam você a organizar e gerenciar seus hubs de notificação.
Você deve ter pelo menos um namespace de hub de notificação.
Um único namespace pode abrigar vários hubs.
Você pode ter vários namespaces para organizar seus hubs ou para dar permissão a indivíduos específicos para gerenciar um subconjunto selecionado de seus hubs.
Para criar um namespace, certifique-se de especificar um nome exclusivo para o namespace; especifique o datacenter onde o namespace estará localizado; e, especifique o grupo de recursos ao qual o namespace será atribuído.
Depois que o namespace tiver sido criado, você poderá usar o cmdlet New-AzNotificationHubsNamespaceAuthorizationRules para atribuir regras de autorização a esse namespace.
As regras de autorização são usadas para gerenciar permissões para o namespace.

## EXEMPLOS

### Exemplo 1: Criar um hub de notificação
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

Este comando cria um hub de notificação chamado ContosoPartners.
O namespace estará localizado no datacenter dos EUA Ocidental e será atribuído ao grupo de recursos ContosoNotificationsGroup.

### Exemplo 2: Criar um hub de notificação com marcas
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

Este comando cria um hub de notificação chamado ContosoPartners.
O namespace estará localizado no datacenter dos EUA Ocidental e será atribuído ao grupo de recursos ContosoNotificationsGroup.
Além disso, este comando cria uma marca com o nome Público e o valor PartnerOrganizations e é atribuído ao namespace.
Isso garante que o namespace seja exibido sempre que você filtrar itens em que a marca Audience está definida como PartnerOrganizations.

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

### -Location
Especifica o nome de exibição do datacenter que hospedará o Namespace.
Embora você possa definir esse parâmetro para qualquer local válido, para um desempenho ideal, talvez você queira usar um datacenter localizado perto da maioria dos usuários.

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
Os namespaces fornecem uma maneira de agrupar e categorizar hubs de notificação.

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
Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente inventariá-los e a administração.

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
Camada Sku do namespace

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
Especifica pares de valores de nome que podem ser usados para categorizar e organizar itens do Azure.
Marcas funcionam como palavras-chave e operam em uma implantação.
Por exemplo, se você pesquisar todos os itens com a marca Department:IT, a pesquisa retornará todos os itens do Azure que têm essa marca, independentemente de coisas como tipo de item, local ou grupo de recursos.
Uma marca individual consiste em duas partes: *o Nome* e, opcionalmente, o *Valor*.
Por exemplo, no Departamento:IT, o nome da marca é Department e o valor da marca é IT.
Para adicionar uma marca, use uma sintaxe de tabela de hash semelhante a esta, que cria a marca CalendarYear:2016:

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

### -Confirm
Solicita a confirmação antes de executar o cmdlet.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### System.Collections.Hashtable

## SAÍDAS

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## NOTES

## LINKS RELACIONADOS

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


