---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterface.md
ms.openlocfilehash: 8403a2e26bbc149db35c9c20cdea3075adb88492
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429231"
---
# Set-AzureRmNetworkInterface

## Sinopse
Define o estado da meta para uma interface de rede.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmNetworkInterface -NetworkInterface <PSNetworkInterface> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O **set-AzureRmNetworkInterface** define o estado da meta para uma interface de rede do Azure.

## EXEMPLOS

### Exemplo 1: configurar uma interface de rede
```
$Nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzureRmNetworkInterface -NetworkInterface $Nic
```

Este exemplo configura uma interface de rede.
O primeiro comando obtém uma interface de rede chamada NetworkInterface1 na ResourceGroup1 do grupo de recursos.
O segundo comando define o endereço IP privado da configuração de IP.
O terceiro comando define o método de alocação de IP particular como estático.
O quarto comando define uma marca na interface de rede.
O quinto comando usa as informações armazenadas na variável $Nic para definir a interface de rede.

### Exemplo 2: alterar as configurações de DNS em uma interface de rede
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzureRmNetworkInterface
```

O primeiro comando obtém uma interface de rede chamada NetworkInterface1 que existe dentro do grupo de ResourceGroup1 de recursos. O segundo comando adiciona o servidor DNS 192.168.1.100 a essa interface. O terceiro comando aplica essas alterações à interface de rede. Para remover um servidor DNS, siga os comandos listados acima, mas substitua ". Adicionar "com". Remover "no segundo comando.

### Exemplo 3: ativar o IP forwading em uma interface de rede
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzureRmNetworkInterface
```

O primeiro comando obtém uma interface de rede existente chamada NetworkInterface1 e a armazena na variável $nic. O segundo comando altera o valor de encaminhamento de IP para true. Por fim, o terceiro comando aplica as alterações à interface de rede. Para desativar o encaminhamento de IP em uma interface de rede, siga o exemplo de exemplo, mas certifique-se de alterar o segundo comando para "$nic. EnableIPForwarding = 0 ".

### Exemplo 4: alterar a sub-rede de uma interface de rede
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzureRmVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzureRmVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzureRmNetworkInterface
```

O primeiro comando obtém a interface de rede NetworkInterface1 e a armazena na variável $nic. O segundo comando obtém a rede virtual associada à sub-rede à qual a interface de rede vai ser associada. O segundo comando obtém a sub-rede e a armazena na variável $subnet 2. O terceiro comando associado ao endereço IP privado primário da interface de rede com a nova sub-rede. Por fim, o último comando aplicou essas alterações na interface de rede.

>[!NOTE] 
>As configurações de IP devem ser dinâmicas para que você possa alterar a sub-rede. Se você tiver configurações de IP estático, altere para dinâmico antes de prosseguir. 

>[!NOTE]
>Se a interface de rede tiver várias configurações de IP, o comando para trás deve ser feito para todas essas configurações de IP antes do comando Set-AzureRmNetworkInterface final ser executado. Isso pode ser feito no comando em diante, mas substituindo "0" pelo número apropriado. Se uma interface de rede tem N configurações de IP, N-1 desses comandos devem existir.

### Exemplo 5: associar/dissociar um grupo de segurança de rede a uma interface de rede
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzureRmNetworkInterface
```

O primeiro comando obtém uma interface de rede existente chamada NetworkInterface1 e a armazena na variável $nic. O segundo comando obtém um grupo de segurança de rede existente chamado MyNSG e o armazena na variável $nsg. O comando avançar atribui a $nsg à $nic. Por fim, o quinto comando aplica as alterações à interface de rede. Para dissociar grupos de segurança de rede de uma interface de rede, $nsg de substituição simples no comando por diante com $null.

## OS

### -NetworkInterface
Especifica um objeto **NetworkInterface** que representa o estado da meta para uma interface de rede.

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

### PSNetworkInterface
O parâmetro ' NetworkInterface ' aceita o valor do tipo ' PSNetworkInterface ' do pipeline

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSNetworkInterface

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmNetworkInterface](./Get-AzureRmNetworkInterface.md)

[Get-AzureRmNetworkInterface](./Get-AzureRmNetworkInterface.md)

[New-AzureRmNetworkInterface](./New-AzureRmNetworkInterface.md)

[Remove-AzureRmNetworkInterface](./Remove-AzureRmNetworkInterface.md)
