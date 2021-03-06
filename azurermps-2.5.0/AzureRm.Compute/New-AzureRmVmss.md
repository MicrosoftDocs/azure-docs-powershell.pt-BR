---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmss
schema: 2.0.0
ms.openlocfilehash: f93e05448278e2aaa70ff226a5d3618fdad0e6b4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786164"
---
# New-AzureRmVmss

## Sinopse
Cria um VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Defaultparameter (padrão)
```
New-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SimpleParameterSet
```
New-AzureRmVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
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

### -AllocationMethod
Método de alocação para o endereço IP público do conjunto de escala (estático ou dinâmico).  Se nenhum valor for fornecido, a alocação será estática.

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.

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

### -BackendPoolName
O nome do pool de endereços de back-end a ser usado no balanceador de carga para este conjunto de escala.  Se nenhum valor for fornecido, um novo pool de backend será criado, com o mesmo nome do conjunto de escala.

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendPort
Números de porta de back-end usados pelo balanceador de carga do conjunto de escala para se comunicar com VMs no conjunto de escala.  Se nenhum valor for especificado, as portas 3389 e 5985 serão usadas para VMS do Windows, e a porta 22 será usada para VMs Linux.

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
As credenciais de administrador (nome de usuário e senha) para VMs neste conjunto de escala.

```yaml
Type: PSCredential
Parameter Sets: SimpleParameterSet
Aliases: 

Required: True
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

### -DomainNameLabel
O rótulo de nome de domínio para o nome de domínio do Fully-Qualified público (FQDN) desse conjunto de escala. Este é o primeiro componente do nome de domínio que é atribuído automaticamente ao conjunto de escala. Os nomes de domínio atribuídos automaticamente usam o formulário ( <DomainNameLabel> . <Location> . cloudapp.azure.com). Se nenhum valor for fornecido, o rótulo de nome de domínio padrão será a concatenação de <ScaleSetName> e <ResourceGroupName> .

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontendPoolName
O nome do pool de endereços de front-end a ser usado no balanceador de carga do conjunto de escala.  Se nenhum valor for fornecido, um novo pool de endereços de front-end será criado com o mesmo nome do conjunto de escala.

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageName
O nome da imagem para VMs neste conjunto de escala. Se nenhum valor for fornecido, a imagem "Windows Server 2016 datacenter" será usada.

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceCount
O número de imagens de VM no conjunto de escala.  Se nenhum valor for fornecido, 2 instâncias serão criadas.

```yaml
Type: Int32
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoadBalancerName
O nome do balanceador de carga a ser usado com esse conjunto de escala.  Um novo balanceador de carga usando o mesmo nome que o conjunto de escala será criado se nenhum valor for especificado.

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Local
O local do Azure onde esse conjunto de escala será criado.  Se nenhum valor for especificado, o local será inferido da localização de outros recursos referenciados nos parâmetros.

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NatBackendPort
Porta back-end para conversão de endereços de rede de entrada.

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddressName
O nome do endereço IP público a ser usado com esse conjunto de escala.  Um novo IPAddress público com o mesmo nome que o conjunto de escala será criado se nenhum valor for fornecido.

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos do VMSS.  Se nenhum valor for especificado, um novo grupo de nova fonte será criado usando o mesmo nome que o conjunto de escala.

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SecurityGroupName
O nome do grupo de segurança de rede a ser aplicado a este conjunto de escala.  Se nenhum valor for fornecido, um grupo de segurança de rede padrão com o mesmo nome do conjunto de escala será criado e aplicado ao conjunto de escala.

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetAddressPrefix
O prefixo do endereço da sub-rede que será usada por ScaleMode. As configurações de sub-rede padrão (192.168.1.0/24) serão aplicadas se nenhum valor for fornecido.

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetName
O nome da sub-rede a ser usada com esse conjunto de escala.  Uma nova sub-rede será criada com o mesmo nome que o conjunto de escala, se nenhum valor for fornecido.

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradePolicyMode
O modo de política de atualização para instâncias de VM neste conjunto de escala.  A política de atualização pode especificar atualizações automáticas, manuais ou sem interrupção.

```yaml
Type: UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Especifica o objeto **VirtualMachineScaleSet** que contém as propriedades do VMSS que esse cmdlet cria.

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkName
O nome da rede virtual a ser usada com esse conjunto de escala.  Se nenhum valor for fornecido, uma nova rede virtual com o mesmo nome que o conjunto de escala será criada.

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMScaleSetName
Especifica o nome do VMSS que este cmdlet cria.

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmSize
O tamanho das instâncias de VM nesse conjunto de escala.  Um tamanho padrão (Standard_DS1_v2) será usado se nenhum tamanho for especificado.

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### -VnetAddressPrefix
O prefixo do endereço para a rede virtual usada com esse conjunto de escala.  As configurações de prefixo de endereço de rede virtual padrão (192.168.0.0/16) serão usadas se nenhum valor for fornecido.

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### -Zone
Uma lista de zonas de disponibilidade que indicam o IP alocado para o qual o recurso precisa se originar.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SimpleParameterSet
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

### VirtualMachineScaleSet
O parâmetro ' VirtualMachineScaleSet ' aceita o valor do tipo ' VirtualMachineScaleSet ' do pipeline

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


