---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: eaf34373cb17fea94c498e16f623cef4bf65e937
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118238"
---
# New-AzNotificationHubsNamespaceAuthorizationRule

## Sinopse
Cria uma regra de autorização e atribui essa regra a um namespace do hub de notificação.

## Sintaxe

### InputFileParameterSet
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SASRuleParameterSet
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Descrição
O cmdlet **New-AzNotificationHubsNamespaceAuthorizationRule** cria uma regra de autorização de Assinatura de Acesso Compartilhado (SAS) e a atribui a um namespace do hub de notificação.
As regras de autorização gerenciam direitos de usuário para o namespace e para os hubs de notificação contidos com esse namespace.
Este cmdlet fornece duas maneiras de criar uma nova regra de autorização e atribuí-la a um namespace.
Você pode criar uma instância do objeto **SharedAccessAuthorizationRuleAttributes** e configurar esse objeto com os valores de propriedade que você deseja que a nova regra possua.
Isso pode ser feito usando o .NET Framework.
Em seguida, você pode copiar esses valores de propriedade para a nova regra usando o parâmetro *SASRule.*
Como alternativa, você pode criar um arquivo JSON (Notação de Objeto JavaScript) contendo os valores de configuração relevantes e aplicar esses valores usando o parâmetro *InputFile.*
Um arquivo JSON é um arquivo de texto que usa sintaxe semelhante à seguinte: {  
    "Nome": "ContosoAuthorizationRule",  
    "PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",  
    "Direitos": \[  
        "Ouça",  
        "Enviar"  
    \]  
} Quando usado em conjunto com o cmdlet **New-AzNotificationHubsNamespaceAuthorizationRule,** a amostra JSON anterior cria uma regra de autorização chamada ContosoAuthorizationRule que dá aos usuários direitos de Ouvir e Enviar para o namespace.
A *PrimaryKey* usada para autenticação pode ser gerada aleatoriamente usando o seguinte comando do Windows PowerShell: \[ Converter \] ::ToBase64String((1,32 |% { \[ byte/](Get-Random -Minimum 0 -Maximum 255) }))

## Exemplos

### Exemplo 1: Criar uma regra de autorização e atribuí-la a um namespace
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

Esse comando cria uma regra de autorização e atribui essa regra ao namespace ContosoNamespace.
Ao criar essa regra, você deve especificar o namespace apropriado e o grupo de recursos ao qual o namespace está atribuído.
No entanto, você não precisa especificar nenhuma informação sobre a regra em si: as informações da regra serão retiradas do arquivo de entrada C:\Configuration\NamespaceAuthorizationRules.jsem.

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

### -InputFile
Especifica o caminho para um arquivo JSON que contém informações de configuração para a nova regra de autorização.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
Especifica o namespace ao qual as regras de autorização serão atribuídas.
Os namespaces oferecem uma maneira de agrupar e categorizar os hubs de notificação.
As novas regras devem ser atribuídas a um espaço de nome existente.
O **cmdlet New-AzNotificationHubsNamespaceAuthorizationRule** não pode criar um novo namespace.

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
Especifica o grupo de recursos ao qual o namespace é atribuído.
Os grupos de recursos organizam itens como namespaces, hubs de notificação e regras de autorização de maneiras que ajudam a simplesmente o gerenciamento de estoque e a administração do Azure.
Você deve usar um grupo de recursos existente.
Este cmdlet não pode criar um novo grupo de recursos.

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
Especifica o **objeto SharedAccessAuthorizationRuleAttributes** contendo informações de configuração para as novas regras.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
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

## Saídas

### Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes

## Notas

## LINKS RELACIONADOS

[Get-AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)

[Set-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


