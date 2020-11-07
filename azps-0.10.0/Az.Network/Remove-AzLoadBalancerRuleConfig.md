---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 9c50452acd832c7ac7ca0c4bc2827b8f320115b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775287"
---
# Remove-AzLoadBalancerRuleConfig

## Sinopse
Remove uma configuração de regra para um balanceador de carga.

## SYNTAX

```
Remove-AzLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzLoadBalancerRuleConfig** remove uma configuração de regra para um balanceador de carga do Azure.

## EXEMPLOS

### Exemplo 1: remover uma configuração de regra de um balanceador de carga
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $loadbalancer.

O segundo comando Remove a configuração de regra nomeada MyLBruleName do balanceador de carga em $loadbalancer.

## OS

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

### -Loadbalancer
Especifica o objeto **Loadbalancer** que contém a configuração de regra que este cmdlet Remove.

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Especifica o nome da configuração de regra de balanceamento de carga que este cmdlet Remove.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### PSLoadBalancer
O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSLoadBalancer

## INFORMA

## LINKS RELACIONADOS

[Add-AzLoadBalancerRuleConfig](./Add-AzLoadBalancerRuleConfig.md)

[Get-AzLoadBalancer](./Get-AzLoadBalancer.md)

[Get-AzLoadBalancerRuleConfig](./Get-AzLoadBalancerRuleConfig.md)

[New-AzLoadBalancerRuleConfig](./New-AzLoadBalancerRuleConfig.md)

[Set-AzLoadBalancerRuleConfig](./Set-AzLoadBalancerRuleConfig.md)


