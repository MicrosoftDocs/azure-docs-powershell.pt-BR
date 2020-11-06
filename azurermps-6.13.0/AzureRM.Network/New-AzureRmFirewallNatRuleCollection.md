---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRuleCollection.md
ms.openlocfilehash: 12b45dd5fd62dabb2650f121f52a539962315513
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428469"
---
# New-AzureRmFirewallNatRuleCollection

## Sinopse
Cria uma coleção de regras NAT de firewall.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmFirewallNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmFirewallNatRuleCollection** cria uma coleção de regras NAT de firewall.

## EXEMPLOS

### 1: criar uma coleção com uma regra
```
$rule1 = New-AzureRmFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
New-AzureRmFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 1000 -Rule $rule1
```

Este exemplo cria uma coleção com uma regra. Todo o tráfego que corresponde às condições identificadas em $rule 1 será DNAT'ed para o endereço e a porta traduzidos.

### 2: adicionar uma regra a uma coleção de regras
```
$rule1 = New-AzureRmFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule2 = New-AzureRmFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection.AddRule($rule2)
```

Este exemplo cria uma nova coleção de regras NAT com uma regra e, em seguida, adiciona uma segunda regra à coleção de regras usando addrule no objeto da coleção Rule. Cada nome de regra em um determinado conjunto de regras deve ter um nome exclusivo e não diferencia maiúsculas de minúsculas.

### 3: obter uma regra a partir de uma coleção de regras
```
$rule1 = New-AzureRmFirewallNatRule -Name R1 -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.0.1.0/24" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule=$ruleCollection.GetRuleByName("r1")
```

Este exemplo cria uma nova coleção de regras NAT com uma regra e, em seguida, obtém a regra por nome, método de chamada GetRuleByName no objeto da coleção de regras. O nome da regra para o método GetRuleByName não diferencia maiúsculas de minúsculas.

### 4: remover uma regra de uma coleção de regras
```
$rule1 = New-AzureRmFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$rule2 = New-AzureRmFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1, $rule2
$ruleCollection.RemoveRuleByName("r1")
```

Este exemplo cria uma nova coleção de regras NAT com duas regras e, em seguida, remove a primeira regra da coleção Rule chamando o método RemoveRuleByName no objeto da coleção Rule. O nome da regra para o método RemoveRuleByName não diferencia maiúsculas de minúsculas.

## OS

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
Especifica o nome da regra NAT. O nome deve ser exclusivo dentro de uma coleção de regras.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority
Especifica a prioridade dessa regra. Priority é um número entre 100 e 65000. Quanto menor o número, maior a prioridade.

```yaml
Type: System.UInt32
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
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule]
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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSFirewallNatRuleCollection

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmFirewallNatRule](./New-AzureRmFirewallNatRule.md)

[New-AzureRmFirewall](./New-AzureRmFirewall.md)

[Get-AzureRmFirewall](./Get-AzureRmFirewall.md)
