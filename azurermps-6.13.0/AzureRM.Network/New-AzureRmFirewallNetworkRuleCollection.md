---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRuleCollection.md
ms.openlocfilehash: 79ead5ac618b4631c3ec790156fe1a75e4169882
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431353"
---
# New-AzureRmFirewallNetworkRuleCollection

## Sinopse
Cria um conjunto de regras de rede do firewall do Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmFirewallNetworkRuleCollection -Name <String> -Priority <UInt32>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmFirewallNetworkRuleCollection** cria um conjunto de regras de rede de firewall.

## EXEMPLOS

### 1: criar uma coleção de rede com duas regras
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzureRmFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

Este exemplo cria uma coleção que permitirá todo o tráfego que corresponda a qualquer uma das duas regras.
A primeira regra é para todo o tráfego UDP.
A segunda regra se refere ao tráfego de TCP de 10.0.0.0 a 60.1.5.0:4040.
Se houver outro conjunto de regras de rede com prioridade mais alta (número menor) que também corresponda ao tráfego identificado no $rule 1 ou $rule 2, a ação da coleção de regras com prioridade mais alta terá efeito em vez disso. 

### 2: adicionar uma regra a uma coleção de regras
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

Este exemplo cria um novo conjunto de regras de rede com uma regra e, em seguida, adiciona uma segunda regra à coleção de regras usando addrule no objeto da coleção Rule. Cada nome de regra em um determinado conjunto de regras deve ter um nome exclusivo e não diferencia maiúsculas de minúsculas.

### 3: obter uma regra a partir de uma coleção de regras
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

Este exemplo cria um novo conjunto de regras de rede com uma regra e, em seguida, obtém a regra por nome, método de chamada GetRuleByName no objeto da coleção de regras. O nome da regra para o método GetRuleByName não diferencia maiúsculas de minúsculas.

### 4: remover uma regra de uma coleção de regras
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

Este exemplo cria um novo conjunto de regras de rede com duas regras e, em seguida, remove a primeira regra da coleção de regras chamando o método RemoveRuleByName no objeto da coleção Rule. O nome da regra para o método RemoveRuleByName não diferencia maiúsculas de minúsculas.

## OS

### -ActionType
Especifica a ação a ser tomada para as condições de correspondência de tráfego dessa regra. As ações aceitas são "Allow" ou "Deny".

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome da coleção de regras de rede. O nome deve ser exclusivo em todas as coleções de regras de rede.

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

### -Priority
Especifica a prioridade dessa coleção de regras. Priority é um número entre 100 e 65000. Quanto menor o número, maior a prioridade.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Regra
Especifica a lista de regras a serem agrupadas nesta coleção.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSFirewallNetworkRuleCollection

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmFirewallNetworkRule](./New-AzureRmFirewallNetworkRule.md)

[New-AzureRmFirewall](./New-AzureRmFirewall.md)

[Get-AzureRmFirewall](./Get-AzureRmFirewall.md)
