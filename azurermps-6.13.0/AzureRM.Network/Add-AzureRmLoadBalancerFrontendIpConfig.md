---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 245129e314bc5fd9cfe81d6d9f218a011ffef55d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428083"
---
# Add-AzureRmLoadBalancerFrontendIpConfig

## Sinopse
Adiciona uma configuração de IP front-end a um balanceador de carga.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### SetByResourceSubnet (padrão)
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByResourceIdSubnet
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByResourceIdPublicIpAddress
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByResourcePublicIpAddress
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzureRmLoadBalancerFrontendIpConifg** adiciona uma configuração de IP de front-end a um balanceador de carga do Azure.

## EXEMPLOS

### Exemplo 1 adicionar uma configuração de IP de front-end com um endereço IP dinâmico
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzureRmLoadBalancer
```

O primeiro comando obtém a rede virtual do Azure chamada MyVnet e passa o resultado usando o pipeline para o cmdlet **Get-AzureRmVirtualNetworkSubnetConfig** para obter a sub-rede chamada mysubnet.
Em seguida, o comando armazena o resultado na variável chamada $Subnet.
O segundo comando obtém o balanceador de carga chamado MyLB e passa o resultado para o cmdlet **Add-AzureRmLoadBalancerFrontendIpConfig** que adiciona uma configuração de IP front-end ao balanceador de carga com um endereço IP privado dinâmico da sub-rede armazenada na variável chamada $MySubnet.

### Exemplo 2 adicionar uma configuração de IP de front-end com um endereço IP estático
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzureRmLoadBalancer
```

O primeiro comando obtém a rede virtual do Azure chamada MyVnet e passa o resultado usando o pipeline para o cmdlet **Get-AzureRmVirtualNetworkSubnetConfig** para obter a sub-rede chamada mysubnet.
Em seguida, o comando armazena o resultado na variável chamada $Subnet.
O segundo comando obtém o balanceador de carga chamado MyLB e passa o resultado para o cmdlet **Add-AzureRmLoadBalancerFrontendIpConfig** que adiciona uma configuração de IP front-end ao balanceador de carga com um endereço IP privado estático da sub-rede armazenada na variável chamada $subnet.

### Exemplo 3 adicionar uma configuração de IP de front-end com um endereço IP público
```
PS C:\>$PublicIp = Get-AzureRmPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzureRmLoadBalancer
```

O primeiro comando obtém o endereço IP público do Azure chamado MyPub e armazena o resultado na variável chamada $PublicIp.
O segundo comando obtém o balanceador de carga chamado MyLB e passa o resultado para o cmdlet **Add-AzureRmLoadBalancerFrontendIpConfig** que adiciona uma configuração de IP front-end ao balanceador de carga com endereço IP público armazenado na variável chamada $PublicIp.

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

### -Loadbalancer
Especifica um objeto **Loadbalancer** .
Esse cmdlet adiciona uma configuração de IP de front-end para o balanceador de carga que esse parâmetro especifica.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Nome
Especifica o nome da configuração de IP de front-end a ser adicionada.

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

### -PrivateIpAddress
Especifica o endereço IP privado a ser associado a uma configuração de IP de front-end.

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIpAddress
Especifica o endereço IP público para associar a uma configuração de IP de front-end.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIpAddressId
Especifica a ID do endereço IP público no qual adicionar uma configuração de IP de front-end.

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subnet
Especifica o objeto de sub-rede no qual adicionar uma configuração de IP de front-end.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subnetid
Especifica a ID da sub-rede na qual adicionar uma configuração de IP de front-end.

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. Network. Models. PSLoadBalancer
Parâmetros: loadbalancer (ByValue)

### System. Collections. Generic. List \` 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSLoadBalancer

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmLoadBalancerFrontendIpConfig](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)

[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[New-AzureRmLoadBalancerFrontendIpConfig](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[Remove-AzureRmLoadBalancerFrontendIpConfig](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[Set-AzureRmLoadBalancerFrontendIpConfig](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


