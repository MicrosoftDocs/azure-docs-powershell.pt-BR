---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 5396605719908d468399c126fbeca116060c25b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429198"
---
# Set-AzureRmNotificationHubAuthorizationRules

## Sinopse
Define regras de autorização para um hub de notificação.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### InputFileParameterSet
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SASRuleParameterSet
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmNotificationHubAuthorizationRules** modifica uma regra de autorização de assinatura de acesso compartilhado (SAS) atribuída a um hub de notificação.

As regras de autorização gerenciam o acesso aos seus hubs de notificação pela criação de links, como URIs, com base em diferentes níveis de permissão.
Os níveis de permissão podem ser um dos seguintes: 

- Ouvir
- Enviar
- Gerencia

Os clientes são direcionados para um desses URIs com base no nível de permissão apropriado.
Por exemplo, um cliente que recebeu a permissão de escuta será direcionado para o URI dessa permissão.

Esse cmdlet fornece duas maneiras de modificar uma regra de autorização atribuída a um hub de notificação.
Para um, você pode criar uma instância do objeto **SharedAccessAuthorizationRuleAttributes** e, em seguida, configurar esse objeto com os valores de propriedade que você deseja que a regra possua.
Você pode configurar o objeto por meio do .NET Framework.
Em seguida, você pode copiar esses valores de propriedade para sua regra usando o parâmetro *SASRule* .

Você também pode criar um arquivo JSON (JavaScript Object Notation) contendo os valores de configuração relevantes e, em seguida, aplicar esses valores por meio do parâmetro *InputFile* .
Um arquivo JSON é um arquivo de texto que usa uma sintaxe semelhante a esta:

{"Nome": "ContosoAuthorizationRule",  
    "PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",  
    "Direitos": \[  
        "Ouvir",  
        Envio  
    \]  
}

Quando usado em conjunto com o cmdlet New-AzureRmNotificationHubAuthorizationRules, o exemplo JSON anterior modifica uma regra de autorização chamada ContosoAuthorizationRule para permitir que os usuários escutem e enviem direitos ao Hub.

## EXEMPLOS

### Exemplo 1: modificar uma regra de autorização atribuída a um hub de notificação
```
PS C:\>Set-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

Esse comando modifica uma regra de autorização atribuída ao Hub de notificação chamado ContosoExternalHub.
Você deve especificar o namespace no qual o Hub está localizado, bem como o grupo de recursos ao qual o Hub está atribuído.
As informações sobre a regra que é modificada não estão incluídas no próprio comando.
Em vez disso, essas informações são encontradas no arquivo de entrada C:\Configuration\AuthorizationRules.js.

## OS

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

### -InputFile
Especifica o caminho para um arquivo JSON contendo informações de configuração para a nova regra.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
Especifica o namespace ao qual o Hub de notificações está atribuído.
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

### -NotificationHub
Especifica o Hub de notificação ao qual esse cmdlet atribui regras de autorização.
Os hubs de notificação são usados para enviar notificações por push para vários clientes, independentemente do usado por esses clientes.

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

### -Resource
Especifica o grupo de recursos ao qual o Hub de notificações está atribuído. Grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente gerenciamento de inventário e administração do Azure.

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

### -SASRule
Especifica o objeto **SharedAccessAuthorizationRuleAttributes** que contém informações de configuração para as regras de autorização que são modificadas.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmNotificationHubAuthorizationRules](./Get-AzureRmNotificationHubAuthorizationRules.md)

[New-AzureRmNotificationHubAuthorizationRules](./New-AzureRmNotificationHubAuthorizationRules.md)

[Remove-AzureRmNotificationHubAuthorizationRules](./Remove-AzureRmNotificationHubAuthorizationRules.md)


