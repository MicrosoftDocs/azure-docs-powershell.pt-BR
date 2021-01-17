---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: e2ca08746ab9b4dc2ef2265a59cdab00ac42cf33
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434297"
---
# New-AzVmssIpConfig

## Sinopse
Cria uma configuração de IP para uma interface de rede de um VMSS.

## SYNTAX

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-PublicIPAddressVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzVmssIpConfig** cria um objeto de configuração de IP para uma interface de rede de um conjunto de escala de máquina virtual (VMSS).
Especifique a configuração deste cmdlet como o parâmetro *IPConfiguration* do cmdlet Add-AzVmssNetworkInterfaceConfiguration.

## EXEMPLOS

### Exemplo 1: criar um objeto de configuração de IP para uma interface VMSS
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

Esse comando cria um objeto de configuração de IP chamado ContosoVmssInterface02.
O comando usa uma ID de sub-rede previamente definida armazenada em $SubnetId.
O comando armazena as definições de configuração na variável $IPConfiguration para uso posterior com **Add-AzVmssNetworkInterfaceConfiguration**.

### Exemplo 2: criar um objeto de configuração de IP que inclua as configurações de pool NAT
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
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
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -DnsSetting
As configurações de DNS a serem aplicadas nos endereços publicIP.
O rótulo do nome do domínio das configurações de DNS a ser aplicado aos endereços publicIP.
A concatenação do rótulo de nome de domínio e do índice de VM será os rótulos de nome de domínio dos recursos de endereço IP público que serão criados.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ID
Especifica uma ID.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpTag
Especifica uma matriz de objetos de marca IP.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPoolsId
Especifica uma matriz de referências a pools de conversão de endereços de rede (NAT) de entrada dos balanceadores de carga.
Um conjunto de escala pode fazer referência A pools de NAT de entrada de um balanceador de carga público e um interno.
Vários conjuntos de escala não podem usar o mesmo balanceador de carga.

```yaml
Type: System.String[]
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
Type: System.String[]
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
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Principal
Especifica a configuração de IP primário em caso de a interface de rede ter mais de uma configuração de IP.

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

### -PrivateIPAddressVersion
Especifique a configuração de IP para o endereço IP privado.  O padrão é considerado IPv4.  Os valores possíveis são: ' IPv4 ' e ' IPv6 '.

```yaml
Type: System.String
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
Type: System.Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationName
O nome de configuração do endereço publicIP.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressVersion
Especifique a configuração de IP para o endereço IP público.  O padrão é considerado IPv4.  Os valores possíveis são: ' IPv4 ' e ' IPv6 '.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPPrefix
A ID do prefixo de IP público

```yaml
Type: System.String
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
Type: System.String
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### System. String

### System. String []

### System. Int32

### Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetIpTag []

## EXIBE

### Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetIPConfiguration

## INFORMA

## LINKS RELACIONADOS

[Add-AzVmssNetworkInterfaceConfiguration](./Add-AzVmssNetworkInterfaceConfiguration.md)


