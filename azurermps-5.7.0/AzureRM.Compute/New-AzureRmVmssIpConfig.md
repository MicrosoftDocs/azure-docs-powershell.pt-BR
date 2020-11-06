---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssIpConfig.md
ms.openlocfilehash: 448f6236f5c9545ff1a1194c8103463f78a8fefd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429866"
---
# New-AzureRmVmssIpConfig

## Sinopse
Cria uma configuração de IP para uma interface de rede de um VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmVmssIpConfig** cria um objeto de configuração de IP para uma interface de rede de um conjunto de escala de máquina virtual (VMSS).
Especifique a configuração deste cmdlet como o parâmetro *IPConfiguration* do cmdlet Add-AzureRmVmssNetworkInterfaceConfiguration.

## EXEMPLOS

### Exemplo 1: criar um objeto de configuração de IP para uma interface VMSS
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

Esse comando cria um objeto de configuração de IP chamado ContosoVmssInterface02.
O comando usa uma ID de sub-rede previamente definida armazenada em $SubnetId.
O comando armazena as definições de configuração na variável $IPConfiguration para uso posterior com **Add-AzureRmVmssNetworkInterfaceConfiguration**.

### Exemplo 2: criar um objeto de configuração de IP que inclua as configurações de pool NAT
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

Esse comando cria um objeto de configuração de IP chamado ContosoVmssInterface03 e, em seguida, armazena-o na variável $IPConfiguration para uso posterior.
O comando usa uma ID de sub-rede previamente definida armazenada em $SubnetId.
O comando armazena as definições de configuração na variável $IPConfiguration para uso posterior.
O comando especifica valores para os parâmetros *LoadBalancerInboundNatPoolsId* e *LoadBalancerBackendAddressPoolsId* .

## OS

### -ApplicationGatewayBackendAddressPoolsId
Especifica uma matriz de referências a pools de endereços de back-end de balanceadores de carga.
Um conjunto de escala pode fazer referência A pools de endereços de back-end de um balanceador de carga público e um interno.
Vários conjuntos de escala não podem usar o mesmo balanceador de carga.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DnsSetting
As configurações de DNS a serem aplicadas nos endereços publicIP.
O rótulo do nome do domínio das configurações de DNS a ser aplicado aos endereços publicIP.
A concatenação do rótulo de nome de domínio e do índice de VM será os rótulos de nome de domínio dos recursos de endereço IP público que serão criados.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ID
Especifica uma ID.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPoolsId
Especifica uma matriz de referências a pools de conversão de endereços de rede (NAT) de entrada dos balanceadores de carga.
Um conjunto de escala pode fazer referência A pools de NAT de entrada de um balanceador de carga público e um interno.
Vários conjuntos de escala não podem usar o mesmo balanceador de carga.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatPoolsId
Especifica uma matriz de referências a pools de NAT de entrada dos balanceadores de carga.
Um conjunto de escala pode fazer referência A pools de NAT de entrada de um balanceador de carga público e um interno.
Vários conjuntos de escala não podem usar o mesmo balanceador de carga.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome da configuração de IP.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PrivateIPAddressVersion
Especifique a configuração de IP como IPv4 ou IPv6. O padrão é considerado IPv4.  Os valores possíveis são: ' IPv4 ' e ' IPv6 '.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationIdleTimeoutInMinutes
O tempo limite de ociosidade do endereço IP público.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationName
O nome de configuração do endereço publicIP.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subnetid
Especifica a ID de sub-rede na qual a configuração cria a interface de rede VMSS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

```yaml
Type: SwitchParameter
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

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Add-AzureRmVmssNetworkInterfaceConfiguration](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)


