---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 2fb349628a686bb96df5685bff8a4329c0173212
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430108"
---
# Set-AzureRmNotificationHubsNamespace

## Sinopse
Define valores de propriedade para um namespace do hub de notificação.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmNotificationHubsNamespace** define os valores de propriedade de um namespace de Hub de notificação existente.
Namespaces são recipientes lógicos que ajudam você a organizar e gerenciar seus hubs de notificação.
Você deve ter pelo menos um namespace de Hub de notificação.
Além disso, todos os hubs de notificação devem ter um namespace atribuído.
Esse cmdlet é usado principalmente para habilitar e desabilitar um namespace.
Quando um namespace está desabilitado, os usuários não podem se conectar a nenhum dos hubs de notificação no namespace, nem os administradores podem usar esses hubs para enviar notificações por push.
Para habilitar novamente um namespace desabilitado, use esse cmdlet para definir a propriedade **State** do namespace como active.
Você também pode usar esse cmdlet para marcar um namespace como crítico.
Isso impede que o namespace seja excluído.
Para remover um namespace crítico, primeiro você deve remover a marca crítica.

## EXEMPLOS

### Exemplo 1: desabilitar um namespace
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

Esse comando desabilita o namespace chamado ContosoPartners localizado no datacenter dos EUA e atribuído ao grupo de recursos ContosoNotificationsGroup.

### Exemplo 2: habilitar um namespace
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

Esse comando habilita o namespace chamado ContosoPartners localizado no datacenter dos EUA e atribuído ao grupo de recursos ContosoNotificationsGroup.

## OS

### -Crítica
Indica se o namespace é um namespace crítico.
Namespaces críticos não podem ser excluídos.
Para excluir um namespace crítico, você deve definir o valor dessa propriedade como false para marcar o namespace como não crítico.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Não peça confirmação.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Local
Especifica o nome de exibição do datacenter que hospeda o namespace.
Embora você possa definir esse parâmetro para qualquer local válido do Azure, para desempenho ideal, você deve usar um Datacenter localizado próximo à maioria dos seus usuários.
Para obter uma lista atualizada dos locais do Azure, execute o seguinte comando: `Get-AzureLocation | Select-Object DisplayName`

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
Especifica o namespace que esse cmdlet modifica.
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
Especifica o grupo de recursos ao qual o namespace está atribuído.
Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.

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

### -Estado
Especifica o estado atual do namespace.
Os valores aceitáveis para esse parâmetro são: active e Disabled.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Marca
Especifica pares de nomes e valores que podem ser usados para categorizar e organizar os itens do Azure.
A função marcas é semelhante a palavras-chave e operam em uma implantação.
Por exemplo, se você Pesquisar todos os itens com o departamento de marcas: ele a pesquisa retornará todos os itens do Azure que têm essa marca, independentemente de itens como tipo de item, local ou grupo de recursos.
Uma marca individual consiste em duas partes: o *nome* e (opcionalmente) o *valor*.
Por exemplo, no departamento: ele, o nome da marca é departamento e o valor da marca é.
Para adicionar uma marca, use a sintaxe de tabela de hash semelhante a isso, que cria a marca CalendarYear: 2016:-Tags @ {Name = "CalendarYear"; Valor = "2016"} para adicionar várias marcas no mesmo comando, separe as marcas individuais usando vírgulas:-marca @ {Name = "CalendarYear"; Valor = "2016"}, @ {Name = "FiscalYear"; Valor = "2017"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

### Microsoft. Azure. Commands. NotificationHubs. Models. Namespacestate

### System. Boolean

### System. Collections. Hashtable

## EXIBE

### Microsoft. Azure. Commands. NotificationHubs. Models. Namespaceattributes

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmNotificationHubsNamespace](./Get-AzureRmNotificationHubsNamespace.md)

[New-AzureRmNotificationHubsNamespace](./New-AzureRmNotificationHubsNamespace.md)

[Remove-AzureRmNotificationHubsNamespace](./Remove-AzureRmNotificationHubsNamespace.md)


