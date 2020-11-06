---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicKey.md
ms.openlocfilehash: ed31934a75d9d6826a7e0464dccd43fd2d853daa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429109"
---
# New-AzureRmServiceBusTopicKey

## Sinopse
Regenera as cadeias de conexão primária ou secundária para o tópico de barramento do serviço.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmServiceBusTopicKey [-ResourceGroup] <String> -Namespace <String> -Topic <String> -Name <String>
 [-RegenerateKeys] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmServiceBusTopicKey** gera uma nova cadeia de conexão primária ou secundária para o tópico de barramento de serviço especificado e a regra de autorização.

## EXEMPLOS

### Exemplo 1
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -RegenerateKeys PrimaryKey
```

Regenera a cadeia de caracteres de conexão principal para o namespace.

### Exemplo 2
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -RegenerateKeys SecondaryKey
```

Regenera a cadeia de conexão secundária para o namespace.

## OS

### -RegenerateKeys
Especifica se deve regenerar as chaves primárias ou secundárias.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Resource
O nome do grupo de recursos.

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
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

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

### -Nome
Nome da regra de autorização.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Nome do namespace.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tópico
Nome do tópico.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### -Resource
 System. String
 

### -NamespaceName
 System. String
 

### -AuthorizationRuleName
 System. String
 

### -Topicname
 System. String
 

### -RegenerateKeys
 System. String

## EXIBE

### Microsoft. Azure. Commands. ServiceBus. Models. ListKeysAttributes
PrimaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Topi c_exampl1 SecondaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Topi c_exampl1 PrimaryKey: {PrimaryKey valor} SecondaryKey: {SecondaryKey Value} KeyName: SBTopicAuthoRule1

## INFORMA

## LINKS RELACIONADOS

