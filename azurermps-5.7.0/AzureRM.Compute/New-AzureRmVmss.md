---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmss.md
ms.openlocfilehash: e94cc565c2f22134f6bd4092247fbfa1f5a98b8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428976"
---
# New-AzureRmVmss

## Sinopse
Cria um VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmVmss [-ResourceGroupName] <String> -VMScaleSetName <String>
 [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmVmss** cria um VMSS (conjunto de escala de máquina virtual) no Azure.
Esse cmdlet leva um objeto **VirtualMachineScaleSet** como entrada.

## EXEMPLOS

### Exemplo 1: criar um VMSS
```
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzureRmResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzureRmVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzureRmVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzureRmVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzureRmPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzureRmPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzureRmLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzureRmLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzureRmLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName

# New VMSS Parameters
$VMSSName = "VMSS" + $RGName;

$AdminUsername = "Admin01";
$AdminPassword = "p4ssw0rd@123" + $RGName;

$PublisherName = "MicrosoftWindowsServer" 
$Offer         = "WindowsServer" 
$Sku           = "2012-R2-Datacenter" 
$Version       = "latest"
        
$VHDContainer = "https://" + $STOName + ".blob.core.contoso.net/" + $VMSSName;

$ExtName = "CSETest";
$Publisher = "Microsoft.Compute";
$ExtType = "BGInfo";
$ExtVer = "2.1";

#IP Config for the NIC
$IPCfg = New-AzureRmVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzureRmVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_A2" -UpgradePolicyMode "Automatic" `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzureRmVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzureRmVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

O exemplo complexo a seguir cria um VMSS.
O primeiro comando cria um grupo de recursos com o nome e o local especificados.
O segundo comando usa o cmdlet **New-AzureRmStorageAccount** para criar uma conta de armazenamento.
Em seguida, o terceiro comando usa o cmdlet **Get-AzureRmStorageAccount** para obter a conta de armazenamento criada no segundo comando e armazena o resultado na variável $STOAccount.
O quinto comando usa o cmdlet **New-AzureRmVirtualNetworkSubnetConfig** para criar uma sub-rede e armazena o resultado na variável chamada $SubNet.
O sexto comando usa o cmdlet **New-AzureRmVirtualNetwork** para criar uma rede virtual e armazena o resultado na variável chamada $VNet.
O sétimo comando usa o **Get-AzureRmVirtualNetwork** para obter informações sobre a rede virtual criada no sexto comando e armazena as informações na variável chamada $VNet.
O oitavo e nono comando usam os **novos-AzureRmPublicIpAddress** e **Get-AzureRmPublicIpAddress** para criar e obter informações desse endereço IP público.
Os comandos armazenam as informações na variável chamada $PubIP.
O comando décimo usa o cmdlet **New-AzureRmLoadBalancerFrontendIpConfig** para criar um balanceador de carga de front-end e armazena o resultado na variável chamada $frontend.
O décimo primeiro comando usa o **New-AzureRmLoadBalancerBackendAddressPoolConfig** para criar uma configuração de pool de endereços back-end e armazena o resultado na variável chamada $BackendAddressPool.
O décimo segundo comando usa o **New-AzureRmLoadBalancerProbeConfig** para criar um teste e armazena as informações da investigação na variável chamada $Probe.
O décimo terceiro comando usa o cmdlet **New-AzureRmLoadBalancerInboundNatPoolConfig** para criar uma configuração de pool NAT (conversão de endereços de rede) de balanceador de carga.
O comando fourteenth usa o **New-AzureRmLoadBalancerRuleConfig** para criar uma configuração de regra de balanceador de carga e armazena o resultado na variável chamada $LBRule.
O comando Fifteenth usa o cmdlet **New-AzureRmLoadBalancer** para criar um balanceador de carga e armazena o resultado na variável chamada $ActualLb.
O comando dezesseis usa o **Get-AzureRmLoadBalancer** para obter informações sobre o balanceador de carga que foi criado no comando Fifteenth e armazena as informações na variável chamada $ExpectedLb.
O comando seventeenth usa o cmdlet **New-AzureRmVmssIPConfig** para criar uma configuração de IP VMSS e armazena as informações na variável chamada $IPCfg.
O comando décimo oitavo usa o cmdlet **New-AzureRmVmssConfig** para criar um objeto de configuração VMSS e armazena o resultado na variável chamada $VMSS.
O comando XIX usa o cmdlet **New-AzureRmVmss** para criar o VMSS.

## OS

### -ResourceGroupName
Especifica o nome do grupo de recursos do VMSS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Especifica o objeto **VirtualMachineScaleSet** que contém as propriedades do VMSS que esse cmdlet cria.

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VMScaleSetName
Especifica o nome do VMSS que este cmdlet cria.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
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

### Esse cmdlet não gera nenhuma saída.

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmVmss](./Get-AzureRmVmss.md)

[Remove-AzureRmVmss](./Remove-AzureRmVmss.md)

[Restart-AzureRmVmss](./Restart-AzureRmVmss.md)

[Set-AzureRmVmss](./Set-AzureRmVmss.md)

[Start-AzureRmVmss](./Start-AzureRmVmss.md)

[Parar-AzureRmVmss](./Stop-AzureRmVmss.md)

[Update-AzureRmVmss](./Update-AzureRmVmss.md)


