---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 125B6865-0022-4F88-BB0F-DDDDB2EDFF00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a1f1d033c3e8bae708310d12a1c4cb2b581bf80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945800"
---
# Set-AzureNetworkSecurityRule

## Sinopse
Adiciona ou modifica uma regra de segurança de rede em um grupo de segurança de rede.

## SYNTAX

```
Set-AzureNetworkSecurityRule -Name <String> -Type <String> -Priority <Int32> -Action <String>
 -SourceAddressPrefix <String> -SourcePortRange <String> -DestinationAddressPrefix <String>
 -DestinationPortRange <String> -Protocol <String> -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureNetworkSecurityRule** adiciona ou modifica uma regra de segurança de rede do Azure em um grupo de segurança de rede.

## EXEMPLOS

## OS

### -Ação
Especifica a ação para uma regra de segurança de rede.
Os valores válidos são: allow e Deny.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationAddressPrefix
Especifica o endereço de roteamento interdomain sem classe (CIDR) do intervalo de IP de destino para a regra de segurança de rede.
Um asterisco (*) Especifica qualquer endereço IP.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPortRange
Especifica um intervalo de porta de destino para a regra de segurança de rede.
Os valores válidos consistem em números inteiros de 0 a 65535.
Você pode especificar um valor individual ou especificar um intervalo no formato LowerNumber-HigherNumber.
Um hífen separa os dois valores.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome da regra de segurança de rede que este cmdlet adiciona ou modifica.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkSecurityGroup
Especifica o grupo de segurança de rede que esse cmdlet modifica.
Para obter um objeto **INetworkSecurityGroup** , use o cmdlet Get-AzureNetworkSecurityGroup.

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Priority
Especifica a prioridade para a regra de segurança de rede.
Os valores válidos são: inteiros de 100 a 4096.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê. Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocolo
Especifica o protocolo para a regra de segurança de rede.
Os valores válidos são: 

- Protocol 
- GRAMA 
- *

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAddressPrefix
Especifica o endereço CIDR do intervalo de IP de origem para a regra de segurança de rede.
Um asterisco (*) Especifica qualquer endereço IP.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourcePortRange
Especifica um intervalo de porta de origem para a regra de segurança de rede.
Os valores válidos consistem em números inteiros de 0 a 65535.
Você pode especificar um valor individual ou especificar um intervalo no formato LowerNumber-HigherNumber.
Um hífen separa os dois valores.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Digite
Especifica o tipo de conexão para a regra de segurança de rede.
Os valores válidos são: de entrada e de saída.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Remove-AzureNetworkSecurityRule](./Remove-AzureNetworkSecurityRule.md)


