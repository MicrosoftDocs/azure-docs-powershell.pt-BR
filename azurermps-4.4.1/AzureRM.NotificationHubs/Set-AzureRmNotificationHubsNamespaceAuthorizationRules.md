---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: a25e318aca1bca33c309a6f24b862e98c02659e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429191"
---
# Set-AzureRmNotificationHubsNamespaceAuthorizationRules

## Sinopse
Define regras de autorização para um namespace do hub de notificação.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### InputFileParameterSet
```
Set-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SASRuleParameterSet
```
Set-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmNotificationHubsNamespaceAuthorizationRules** modifica uma regra de autorização de assinatura de acesso compartilhado (SAS) atribuída a um namespace do hub de notificação.
As regras de autorização gerenciam os direitos do usuário para o namespace e para os hubs de notificação contidos nesse namespace.

Esse cmdlet fornece duas maneiras de modificar uma regra de autorização atribuída a um namespace.
Para um, você pode criar uma instância do objeto **SharedAccessAuthorizationRuleAttributes** e, em seguida, configurar esse objeto com os valores de propriedade que você deseja que a regra possua.
Você pode usar o .NET Framework para fazer isso.
Em seguida, você pode copiar esses valores de propriedades para a regra por meio do parâmetro *SASRule* .

Você também pode criar um arquivo JSON (JavaScript Object Notation) contendo os valores de configuração relevantes e, em seguida, aplicar esses valores por meio do parâmetro *InputFile* .
Um arquivo JSON é um arquivo de texto que usa uma sintaxe semelhante a esta:

{  
    "Nome": "ContosoAuthorizationRule",  
    "PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",  
    "Direitos": \[  
        "Ouvir",  
        Envio  
    \]  
}

Quando usado em conjunto com o cmdlet **set-AzureRmNotificationHubsNamespaceAuthorizationRules** , o exemplo de JSON anterior modifica uma regra de autorização chamada ContosoAuthorizationRule para conceder aos usuários a permissão de escuta e envio para o namespace.

## EXEMPLOS

### Exemplo 1: modificar uma regra de autorização atribuída a um namespace
```
PS C:\>Set-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

Esse comando modifica uma regra de autorização atribuída ao namespace chamado ContosoNamespace.
Você deve especificar o grupo de recursos ao qual o namespace está atribuído.
As informações sobre a regra de autorização não estão incluídas no próprio comando.
Em vez disso, essas informações são obtidas do arquivo de entrada C:\Configuration\AuthorizationRules.js.

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
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
Especifica o namespace que contém as regras de autorização que esse cmdlet modifica.
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

### -SASRule
Especifica o objeto **SharedAccessAuthorizationRuleAttributes** que contém informações de configuração para as regras de autorização que esse cmdlet modifica.

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

[Get-AzureRmNotificationHubsNamespaceAuthorizationRules](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[New-AzureRmNotificationHubsNamespaceAuthorizationRules](./New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[Remove-AzureRmNotificationHubsNamespaceAuthorizationRules](./Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


