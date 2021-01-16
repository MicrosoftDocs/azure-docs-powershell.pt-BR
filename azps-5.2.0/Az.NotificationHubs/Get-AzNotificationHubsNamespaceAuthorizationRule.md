---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: f3ba8428a6f6a9e618872e1292234751979b3c4b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258750"
---
# Get-AzNotificationHubsNamespaceAuthorizationRule

## Sinopse
Obtém informações sobre as regras de autorização associadas a um namespace do hub de notificação.

## SYNTAX

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzNotificationHubsNamespaceAuthorizationRule** retorna informações sobre as regras de autorização de assinatura de acesso compartilhado (SAS) associadas a um namespace de Hub de notificação.
Você pode retornar informações sobre todas as regras associadas ao namespace.
Ou, como alternativa, incluindo o parâmetro *AuthorizationRule* , você pode retornar informações para uma regra específica.
Regras de autorização gerenciem o acesso a namespaces.
Isso é feito por meio da criação de links, como URIs, com base em diferentes níveis de permissão.
Os níveis de plataforma podem ser um dos seguintes: 
- Ouvir
- Enviar
- Gerenciar clientes são direcionados para um desses URIs com base no nível de permissão apropriado.
Por exemplo, um cliente que recebeu a permissão de escuta será direcionado para o URI dessa permissão.
Este cmdlet obtém apenas as regras de autorização associadas a um namespace.
Para obter informações sobre o próprio namespace, use Get-AzNotificationHubsNamespace.

## EXEMPLOS

### Exemplo 1: obter informações sobre todas as regras de autorização atribuídas a namespaces
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

Esse comando obtém informações sobre todas as regras de autorização atribuídas ao namespace ContosoNamespace e ao grupo de recursos ContosoNotificationsGroup.

### Exemplo 2: obter informações sobre uma regra de autorização
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

Esse comando obtém informações sobre uma única regra de autorização de namespace chamada ListenRule.
Você deve incluir o namespace e o grupo de recursos quando obter informações para uma regra de autorização específica.

## OS

### -AuthorizationRule
Especifica o nome de uma regra de autenticação SAS.
Essas regras determinam o tipo de acesso que os usuários têm ao namespace.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Namespace
Especifica o namespace para o qual as regras de autorização são atribuídas.
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
Especifica o grupo de recursos ao qual as regras de autorização são atribuídas.
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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes

## INFORMA

## LINKS RELACIONADOS

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


