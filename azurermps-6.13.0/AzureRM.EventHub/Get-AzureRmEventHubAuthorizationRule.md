---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 70b5ac9eb40bf6c50ebb6d09849e8185c23927e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429546"
---
# Get-AzureRmEventHubAuthorizationRule

## Sinopse
Obtém os detalhes de uma regra de autorização ou obtém uma lista de regras de autorização.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### NamespaceAuthorizationRuleSet (padrão)
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventhubAuthorizationRuleSet
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AliasAuthoRuleSet
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Get-AzureRmEventHubAuthorizationRule Obtém os detalhes de uma regra de autorização ou uma lista de todas as regras de autorização para um hub de eventos especificado.
Se o nome de uma regra de autorização for fornecido, os detalhes dessa única regra de autorização serão retornados.
Se o nome de uma regra de autorização não for fornecido, uma lista de todas as regras de autorização para o Hub de eventos especificado será retornada.
Se o nome do alias fornecido (recuperação de desastre) fornecido, os detalhes da regra de autorização do namespace para alias configurado serão retornados.

## EXEMPLOS

### Exemplo 1,0-AuthorizationRule para namespace
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

Obtém a regra de autorização \` MyAuthRuleName \` no namespace \` mynamespacename \` .

### Exemplo 1,1-AuthorizationRules para namespace
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

Obtém uma lista de todas as regras de autorização no namespace \` Mynamespacename \` .

### Exemplo 2,0-AuthorizationRule para EventHub
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

Obtém a regra de autorização \` MyAuthRuleName \` no Hub de eventos \` MyEventHubName \` , cujo escopo é o namespace \` mynamespacename \` .

### Exemplo 2,1-AuthorizationRules para EventHub
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

Obtém as regras de autorização de lista no Hub de eventos \` MyEventHubName \` , cujo escopo é o namespace \` mynamespacename \` .

### Exemplo 3,0-AuthorizationRule para alias (configuração georecuperação)
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

Obtém a regra de autorização \` MyAuthRuleName \` no namespace \` mynamespacename \` .

### Exemplo 3,1-AuthorizationRules para alias (configuração georecuperação)
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

Obtém uma lista de todos os MyAuthRuleName de regra de autorização \` \` no namespace \` mynamespacename \` .

## OS

### -Aliasname
Nome do alias

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Eventhub
Nome do Eventhub

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Nome do AuthorizationRule

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Nome do namespace

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes

## INFORMA

## LINKS RELACIONADOS
