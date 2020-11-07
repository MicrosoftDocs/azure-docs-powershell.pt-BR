---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: 348732794a0cf16233f9a139e86ed89658fc5ac2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786253"
---
# Set-AzureRmNetworkSecurityGroup

## Sinopse
Define o estado da meta para um grupo de segurança de rede.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmNetworkSecurityGroup** define o estado da meta para um grupo de segurança de rede do Azure.

## EXEMPLOS

### Exemplo 1: definir o estado da meta para um grupo de segurança de rede
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

Esse comando obtém o grupo de segurança de rede do Azure chamado Nsg1 e adiciona uma regra de segurança de rede chamada Rdp-Rule para permitir o tráfego de Internet na porta 3389 para o objeto do grupo de segurança de rede recuperada usando Add-AzureRmNetworkSecurityRuleConfig.
O comando persiste o grupo de segurança de rede do Azure modificado usando **set-AzureRmNetworkSecurityGroup**.

## OS

### -AsJob
Executar o cmdlet em segundo plano

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
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

### -NetworkSecurityGroup
Um objeto de grupo de segurança de rede que representa o estado da meta à qual o cmdlet define o grupo de segurança de rede.

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### PSNetworkSecurityGroup
O parâmetro ' NetworkSecurityGroup ' aceita o valor do tipo ' PSNetworkSecurityGroup ' do pipeline

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmNetworkSecurityGroup](./Get-AzureRmNetworkSecurityGroup.md)

[New-AzureRmNetworkSecurityGroup](./New-AzureRmNetworkSecurityGroup.md)

[Remove-AzureRmNetworkSecurityGroup](./Remove-AzureRmNetworkSecurityGroup.md)


