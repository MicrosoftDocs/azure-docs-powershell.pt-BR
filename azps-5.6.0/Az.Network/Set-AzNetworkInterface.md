---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 0afd299103f1595afd100a7e9a72c4045896419d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889908"
---
# Set-AzNetworkInterface

## SYNOPSIS
Atualiza uma interface de rede.

## SINTAXE

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O **Set-AzNetworkInterface** atualiza uma interface de rede.

## EXEMPLOS

### Exemplo 1: Configurar uma interface de rede
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

Este exemplo configura uma interface de rede.
O primeiro comando obtém uma interface de rede chamada NetworkInterface1 no grupo de recursos ResourceGroup1.
O segundo comando define o endereço IP privado da configuração IP.
O terceiro comando define o método de alocação de IP privado como Static.
O quarto comando define uma marca na interface de rede.
O quinto comando usa as informações armazenadas na variável $Nic para definir a interface de rede.

### Exemplo 2: Alterar configurações dns em uma interface de rede
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

O primeiro comando obtém uma interface de rede chamada NetworkInterface1 que existe no grupo de recursos ResourceGroup1. O segundo comando adiciona o servidor DNS 192.168.1.100 a essa interface. O terceiro comando aplica essas alterações à interface de rede. Para remover um servidor DNS, siga os comandos listados acima, mas substitua ". Adicionar" com ". Remover" no segundo comando.

### Exemplo 3: Habilitar o encaminhamento ip em uma interface de rede
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

O primeiro comando obtém uma interface de rede existente chamada NetworkInterface1 e a armazena na $nic variável. O segundo comando altera o valor de encaminhamento de IP como true. Por fim, o terceiro comando aplica as alterações à interface de rede. Para desabilitar o encaminhamento de IP em uma interface de rede, siga o exemplo de exemplo, mas não se esqueça de alterar o segundo comando para "$nic. EnableIPForwarding = 0".

### Exemplo 4: Alterar a sub-rede de uma interface de rede
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

O primeiro comando obtém a interface de rede NetworkInterface1 e o armazena na variável $nic de rede. O segundo comando obtém a rede virtual associada à sub-rede à que a interface de rede será associada. O segundo comando obtém a sub-rede e a armazena na variável $subnet 2. O terceiro comando associou o endereço IP privado principal da interface de rede à nova sub-rede. Por fim, o último comando aplicou essas alterações na interface de rede.
>[!NOTE] 
>As configurações ip devem ser dinâmicas antes de você poder alterar a sub-rede. Se você tiver configurações IP estáticas, altere para dinâmica antes de prosseguir. 
>[!NOTE]
>Se a interface de rede tiver várias configurações IP, o comando forth deverá ser feito para todas essas configurações DE IP antes que o comando final Set-AzNetworkInterface seja executado. Isso pode ser feito como no comando forth, mas substituindo "0" pelo número apropriado. Se uma interface de rede tiver configurações de IP N, então n-1 desses comandos deve existir.

### Exemplo 5: Associar/dissociar um grupo de segurança de rede a uma interface de rede
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

O primeiro comando obtém uma interface de rede existente chamada NetworkInterface1 e a armazena na $nic variável. O segundo comando obtém um grupo de segurança de rede existente chamado MyNSG e o armazena na variável $nsg de rede. O terceiro comando atribui o $nsg à $nic. Por fim, o comando forth aplica as alterações à interface de rede. Para dissociar grupos de segurança de rede de uma interface de rede, substitua $nsg no terceiro comando por $null.

## PARÂMETROS

### -AsJob
Executar cmdlet em segundo plano

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

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

### -NetworkInterface
Especifica um objeto de interface de rede que representa o estado ao qual a interface de rede deve ser definida.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

## SAÍDAS

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

## NOTES

## LINKS RELACIONADOS

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[New-AzNetworkInterface](./New-AzNetworkInterface.md)

[Remove-AzNetworkInterface](./Remove-AzNetworkInterface.md)
