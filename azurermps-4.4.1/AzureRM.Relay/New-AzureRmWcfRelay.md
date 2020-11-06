---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
ms.openlocfilehash: a7a8734395b08c906b84cc4465528434fcb31eb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609575"
---
# New-AzureRmWcfRelay

## Sinopse
Cria um WcfRelay no namespace de retransmissão especificado.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### WcfRelayInputObjectSet
```
New-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### WcfRelayPropertiesSet
```
New-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String> [-WcfRelayType <String>]
 [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>] [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet New-AzureRmWcfRelay cria um WcfRelay no namespace de retransmissão especificado.

## EXEMPLOS

### Exemplo 1-InputObject
```
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject
```

Cria um novo WcfRelay \` TestWCFRelay2 \` no namespace de retransmissão especificado \` TestNameSpace-Relay \` .

### Exemplo 2: Propriedades
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"
```

Cria um novo WcfRelay \` TestWCFRelay \` no namespace de retransmissão especificado \` TestNameSpace-Relay1 \` .

## OS

### -RequiresClientAuthorization
verdadeiro se for necessária a autorização do cliente para este retransmissor; caso contrário, false

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RequiresTransportSecurity
verdadeiro se a segurança de transporte for necessária para esse retransmissor; caso contrário, false

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Metadata usermetadata
Obtém ou define usermetadata é um espaço reservado para armazenar dados de cadeia de caracteres definidos pelo usuário para o ponto de extremidade HybridConnection. por exemplo, Ele pode ser usado para armazenar dados descritivos, como a lista de equipes e suas informações de contato também podem ser armazenadas nas configurações definidas pelo usuário.

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WcfRelayType
Tipo de WcfRelay.
Os valores possíveis incluem: ' NetTcp ' ou ' http '

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases: 
Accepted values: NetTcp, Http

Required: False
Position: Named
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Objeto WcfRelay.

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Nome do WcfRelay.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

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
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### -ResourceGroupName
System. String

### -NamespaceName
System. String

### -WcfRelayName
System. String

### -InputObject
Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes

### -WcfRelayType
System. String

### -RequiresClientAuthorization
System. Boolean

### -RequiresTransportSecurity
System. Boolean

### -Metadata usermetadata
System. String

## EXIBE

### Exemplo 1-InputObject

### Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes
Relaytype: http CreatedAt: 4/26/2017 5:14:46 PM UpdatedAt: 4/26/2017 5:14:46 PM ListenerCount: RequiresClientAuthorization: false RequiresTransportSecurity: true IsDynamic: false usermetadatas: TestWCFRelay2 ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ou namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name: TestWCFRelay2 tipo: Microsoft. Relay/WcfRelays

### Exemplo 2: Propriedades

### Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes
Relaytype: NetTcp CreatedAt: 4/26/2017 5:20:08 PM UpdatedAt: 4/26/2017 5:20:08 PM ListenerCount: RequiresClientAuthorization: true RequiresTransportSecurity: true IsDynamic: false usermetadata: ID de metadados do usuário:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel de espaços/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay nome: TestWCFRelay tipo: Microsoft. Relay/WcfRelays

## INFORMA

## LINKS RELACIONADOS

