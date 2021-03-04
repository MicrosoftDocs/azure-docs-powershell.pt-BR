---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 12967d69e1886b6446db906e5822fd10bbad0037
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892061"
---
# Set-AzNetworkSecurityRuleConfig

## SYNOPSIS
Atualiza uma configuração de regra de segurança de rede para um grupo de segurança de rede.

## SINTAXE

### SetByResource (Padrão)
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Set-AzNetworkSecurityRuleConfig** atualiza uma configuração de regra de segurança de rede para um grupo de segurança de rede.

## EXEMPLOS

### Exemplo 1: Alterar a configuração de acesso em uma regra de segurança de rede
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

O primeiro comando obtém o grupo de segurança de rede chamado NSG-FrontEnd e o armazena na variável $nsg.
O segundo comando usa o operador de pipeline para passar o grupo de segurança no $nsg para Get-AzNetworkSecurityRuleConfig, que obtém a configuração de regra de segurança denominada rdp-rule.
O terceiro comando altera a configuração de acesso do rdp-rule para Negar. No entanto, isso substitui a regra e define apenas os parâmetros que são passados para a função Set-AzNetworkSecurityRuleConfig.   OBSERVAÇÃO: Não há como alterar um único atributo

### Exemplo 2

Atualiza uma configuração de regra de segurança de rede para um grupo de segurança de rede. (gerado automaticamente)

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## PARÂMETROS

### -Access
Especifica se o tráfego de rede é permitido ou negado. Os valores aceitáveis para este parâmetro são: Permitir e Negar.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.

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

### -Description
Especifica uma descrição para uma configuração de regra.
O tamanho máximo é de 140 caracteres.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationAddressPrefix
Especifica um prefixo de endereço de destino.
Os valores aceitáveis para este parâmetro são:
- Um Roteamento entre Domínios sem Classificação (CIDR) 
- Um intervalo de endereços IP de destino 
- Um caractere curinga (*) para corresponder a qualquer endereço IP Você pode usar marcas como VirtualNetwork, AzureLoadBalancer e Internet.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationApplicationSecurityGroup
O grupo de segurança do aplicativo definido como destino da regra. Ele não pode ser usado com o parâmetro 'DestinationAddressPrefix'.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationApplicationSecurityGroupId
O grupo de segurança do aplicativo definido como destino da regra. Ele não pode ser usado com o parâmetro 'DestinationAddressPrefix'.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPortRange
Especifica uma porta de destino ou intervalo.
Os valores aceitáveis para este parâmetro são:
- Um inteiro 
- Um intervalo de inteiros entre 0 e 65535
- Um caractere curinga (*) para corresponder a qualquer porta

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Direction
Especifica se uma regra é avaliada para tráfego de entrada ou saída.
Os valores aceitáveis para este parâmetro são: Entrada e Saída.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Especifica o nome da configuração de regra de segurança de rede que este cmdlet define.

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

### -NetworkSecurityGroup
Especifica o **objeto NetworkSecurityGroup** que contém a configuração de regra de segurança de rede a ser definida.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Priority
Especifica a prioridade de uma configuração de regra.
Os valores aceitáveis para este parâmetro são: Um inteiro entre 100 e 4096.
O número de prioridade deve ser exclusivo para cada regra na coleção.
Quanto menor for o número de prioridade, maior será a prioridade da regra.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
Especifica o protocolo de rede ao que uma configuração de regra se aplica.
Os valores aceitáveis para este parâmetro são: --Tcp
- Udp
- Um caractere curinga (*) para corresponder a ambos

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAddressPrefix
Especifica um prefixo de endereço de origem.
Os valores aceitáveis para este parâmetro são:
- A CIDR
- Um intervalo IP de origem
- Um caractere curinga (*) para corresponder a qualquer endereço IP Você também pode usar marcas como VirtualNetwork, AzureLoadBalancer e Internet.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceApplicationSecurityGroup
O grupo de segurança do aplicativo definido como fonte da regra. Ele não pode ser usado com o parâmetro 'SourceAddressPrefix'.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceApplicationSecurityGroupId
O grupo de segurança do aplicativo definido como fonte da regra. Ele não pode ser usado com o parâmetro 'SourceAddressPrefix'.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourcePortRange
Especifica a porta de origem ou intervalo.
Os valores aceitáveis para este parâmetro são:
- Um inteiro
- Um intervalo de inteiros entre 0 e 65535
- Um caractere curinga (*) para corresponder a qualquer porta

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup

## SAÍDAS

### Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup

## NOTES

## LINKS RELACIONADOS

[Add-AzNetworkSecurityRuleConfig](./Add-AzNetworkSecurityRuleConfig.md)

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[New-AzNetworkSecurityRuleConfig](./New-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)


