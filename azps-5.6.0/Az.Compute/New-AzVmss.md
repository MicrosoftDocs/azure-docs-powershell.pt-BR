---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: f80441cb3555d78974c5a838e829cb2ab350183f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890014"
---
# New-AzVmss

## SYNOPSIS
Cria um VMSS.

## SINTAXE

### DefaultParameter (Padrão)
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SimpleParameterSet
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-EnableUltraSSD]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-ProximityPlacementGroupId <String>] [-HostGroupId <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-ScaleInPolicy <String[]>]
 [-SkipExtensionsOnOverprovisionedVMs] [-EncryptionAtHost] [-PlatformFaultDomainCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **New-AzVmss** cria um Conjunto de Escala de Máquina Virtual (VMSS) no Azure.
Use o conjunto de parâmetros simples ( ) para criar rapidamente um `SimpleParameterSet` VMSS pré-definido e recursos associados. Use o conjunto de parâmetros padrão ( ) para cenários mais avançados quando você precisar configurar com precisão cada componente do VMSS e cada recurso associado antes da `DefaultParameter` criação.

## EXEMPLOS

### Exemplo 1: Criar um VMSS usando o **`SimpleParameterSet`**
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

O comando acima cria o seguinte com o nome `$vmssName` :
* Um grupo de recursos
* Uma rede virtual
* Um balanceador de carga
* Um IP público
* o VMSS com duas instâncias

A imagem padrão escolhida para as VMs no VMSS é `2016-Datacenter Windows Server` e o SKU é `Standard_DS1_v2`

### Exemplo 2: Criar um VMSS usando o **`DefaultParameterSet`**
```powershell
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName

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
$IPCfg = New-AzVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_E4-2ds_v4" -UpgradePolicyMode "Automatic" `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

O exemplo complexo acima cria um VMSS, a seguir está uma explicação do que está acontecendo:
* O primeiro comando cria um grupo de recursos com o nome e o local especificados.
* O segundo comando usa o cmdlet **New-AzStorageAccount** para criar uma conta de armazenamento.
* O terceiro comando usa o cmdlet **Get-AzStorageAccount** para obter a conta de armazenamento criada no segundo comando e armazena o resultado na variável $STOAccount.
* O quinto comando usa o cmdlet **New-AzVirtualNetworkSubnetConfig** para criar uma sub-rede e armazena o resultado na variável chamada $SubNet.
* O sexto comando usa o cmdlet **New-AzVirtualNetwork** para criar uma rede virtual e armazena o resultado na variável chamada $VNet.
* O sétimo comando usa **o Get-AzVirtualNetwork** para obter informações sobre a rede virtual criada no sexto comando e armazena as informações na variável denominada $VNet.
* O oitavo e nono comando usa **o New-AzPublicIpAddress** e **Get- AzureRmPublicIpAddress** para criar e obter informações desse endereço IP público.
* Os comandos armazenam as informações na variável chamada $PubIP.
* O décimo comando usa o cmdlet **New- AzureRmLoadBalancerFrontendIpConfig** para criar um balanceador de carga front-end e armazena o resultado na variável denominada $Frontend.
* O décimo primeiro comando usa o **New-AzLoadBalancerBackendAddressPoolConfig** para criar uma configuração de pool de endereços back-end e armazena o resultado na variável chamada $BackendAddressPool.
* O décimo segundo comando usa o **New-AzLoadBalancerProbeConfig** para criar uma sonda e armazena as informações da sonda na variável denominada $Probe.
* O décimo terceiro comando usa o cmdlet **New-AzLoadBalancerInboundNatPoolConfig** para criar uma configuração de pool nat (conversão de endereço de rede de entrada) do balanceador de carga.
* O décimo quarto comando usa o **New-AzLoadBalancerRuleConfig** para criar uma configuração de regra de balanceador de carga e armazena o resultado na variável denominada $LBRule.
* O décimo quinto comando usa o cmdlet **New-AzLoadBalancer** para criar um balanceador de carga e armazena o resultado na variável chamada $ActualLb.
* O décimo sexto comando usa **o Get-AzLoadBalancer** para obter informações sobre o balanceador de carga criado no décimo quinto comando e armazena as informações na variável denominada $ExpectedLb.
* O décimo sétimo comando usa o cmdlet **New-AzVmssIPConfig** para criar uma configuração de IP VMSS e armazena as informações na variável chamada $IPCfg.
* O décimo oitavo comando usa o cmdlet **New-AzVmssConfig** para criar um objeto de configuração VMSS e armazena o resultado na variável chamada $VMSS.
* O comando décimo nona usa o cmdlet **New-AzVmss** para criar o VMSS.

## PARÂMETROS

### -AllocationMethod
Método de alocação para o Endereço IP Público do Conjunto de Escalas (Estático ou Dinâmico).  Se nenhum valor for fornecido, a alocação será estática.

```yaml
Type: System.String
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
Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.

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

### -BackendPoolName
O nome do pool de endereços de back-end a ser usado no balanceador de carga para este Conjunto de Escalas.  Se nenhum valor for fornecido, um novo pool de back-end será criado, com o mesmo nome do Conjunto de Escala.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendPort
Números de porta back-end usados pelo balanceador de carga Scale Set para se comunicar com VMs no Conjunto de Escala.  Se nenhum valor for especificado, as portas 3389 e 5985 serão usadas para Windows VMS e a porta 22 será usada para VMs Linux.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
As credenciais de administrador (nome de usuário e senha) para VMs neste Conjunto de Escalas.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataDiskSizeInGb
Especifica os tamanhos de discos de dados em GB.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
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

### -DomainNameLabel
O rótulo de nome de domínio para o FQDN (nome Fully-Qualified domínio) público para este Conjunto de Escalas. Este é o primeiro componente do nome de domínio atribuído automaticamente ao Conjunto de Escalas. Os nomes de domínio atribuídos automaticamente usam o formulário ( <DomainNameLabel> <Location> . . cloudapp.azure.com). Se nenhum valor for fornecido, o rótulo de nome de domínio padrão será a concatenação <ScaleSetName> de e <ResourceGroupName> .

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableUltraSSD
Use discos UltraSSD para as VMs no conjunto de escala.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionAtHost
Esse parâmetro habilitará a criptografia para todos os discos, incluindo o disco Resource/Temp no próprio host. Padrão: a Criptografia no host será desabilitada, a menos que essa propriedade seja definida como true para o recurso.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EvictionPolicy
A política de despejo para o conjunto de escala de máquina virtual de baixa prioridade.  Somente os valores com suporte são 'Deallocate' e 'Delete'.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontendPoolName
O nome do pool de endereços front-end a ser usado no balanceador de carga Scale Set.  Se nenhum valor for fornecido, um novo Pool de Endereços Frontend será criado, com o mesmo nome do conjunto de escala.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostGroupId
Especifica o grupo de host dedicado em que o conjunto de escala de máquina virtual irá residir.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: HostGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -ImageName
O nome da imagem para VMs neste Conjunto de Escalas. Se nenhum valor for fornecido, a imagem "DataCenter do Windows Server 2016" será usada.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceCount
O número de imagens de VM no Conjunto de Escalas.  Se nenhum valor for fornecido, duas instâncias serão criadas.

```yaml
Type: System.Int32
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoadBalancerName
O nome do balanceador de carga a ser usado com este Conjunto de Escalas.  Um novo balanceador de carga usando o mesmo nome que o Conjunto de Escala será criado se nenhum valor for especificado.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
O local do Azure onde este Conjunto de Escalas será criado.  Se nenhum valor for especificado, o local será inferido a partir do local de outros recursos referenciados nos parâmetros.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPrice
O preço máximo da cobrança de um conjunto de escala de máquina virtual de baixa prioridade.

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NatBackendPort
Porta back-end para conversão de endereço de rede de entrada.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlatformFaultDomainCount
Contagem de domínios de falha para cada grupo de posicionamento.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Priority
A prioridade para a máquina virtual no conjunto de escala.  Somente os valores com suporte são 'Regular', 'Spot' e 'Low'.
'Regular' é para máquina virtual regular.
'Spot' é para máquina virtual local.
'Baixo' também é para máquina virtual local, mas é substituído por 'Spot'. Use 'Spot' em vez de 'Low'.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProximityPlacementGroupId
A id de recurso do Grupo de Posicionamento de Proximidade a ser usado com esse conjunto de escala.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ProximityPlacementGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddressName
O nome do Endereço IP público a ser usado com esse conjunto de escala.  Um novo IPAddress público com o mesmo nome que o Conjunto de Escalas será criado se nenhum valor for fornecido.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos do VMSS.  Se nenhum valor for especificado, um novo ResourceGroup será criado usando o mesmo nome que o Conjunto de Escalas.

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScaleInPolicy
As regras a serem seguidas ao dimensionar um conjunto de escala de máquina virtual.  Os valores possíveis são: 'Default', 'OldestVM' e 'NewestVM'.  'Padrão' quando um conjunto de escala de máquina virtual é dimensionado, o conjunto de escala será balanceado primeiro entre zonas se for um conjunto de escala zonal.  Em seguida, ele será balanceado entre domínios de falha o mais longe possível.  Dentro de cada Domínio de Falha, as máquinas virtuais escolhidas para remoção serão as mais novas que não estão protegidas de dimensionar.  "OldestVM" quando um conjunto de escalas de máquina virtual está sendo dimensionado, as máquinas virtuais mais antigas que não estão protegidas contra a escala serão escolhidas para remoção.  Para conjuntos de escala de máquina virtual zonal, o conjunto de escalas primeiro será balanceado entre zonas.  Dentro de cada zona, as máquinas virtuais mais antigas que não estão protegidas serão escolhidas para remoção.  "NewestVM" quando um conjunto de escalas de máquina virtual está sendo dimensionado, as máquinas virtuais mais novas que não estão protegidas contra dimensionar serão escolhidas para remoção.  Para conjuntos de escala de máquina virtual zonal, o conjunto de escalas primeiro será balanceado entre zonas.  Dentro de cada zona, as máquinas virtuais mais novas que não estão protegidas serão escolhidas para remoção.

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityGroupName
O nome do grupo de segurança de rede a ser aplicado a este Conjunto de Escalas.  Se nenhum valor for fornecido, um grupo de segurança de rede padrão com o mesmo nome que o Conjunto de Escala será criado e aplicado ao Conjunto de Escalas.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SinglePlacementGroup
Use isso para criar o conjunto Scale em um único grupo de posicionamento, o padrão é vários grupos

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipExtensionsOnOverprovisionedVMs
Especifica que as extensões não são executados nas VMs sobreprovisionadas extras.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetAddressPrefix
O prefixo de endereço da Sub-rede que este ScaleSet usará. As configurações padrão da sub-rede (192.168.1.0/24) serão aplicadas se nenhum valor for fornecido.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetName
O nome da sub-rede a ser usada com este Conjunto de Escalas.  Uma nova Sub-rede será criada com o mesmo nome que o Conjunto de Escala se nenhum valor for fornecido.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SystemAssignedIdentity
Se o parâmetro estiver presente, as VMs no conjunto de escala serão atribuídas a uma identidade do sistema gerenciada gerada automaticamente.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradePolicyMode
O modo de política de atualização para instâncias de VM neste Conjunto de Escalas.  A política de atualização pode especificar atualizações automáticas, manuais ou de rolagem.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserAssignedIdentity
O nome de uma identidade de serviço gerenciado que deve ser atribuída às VMs no conjunto de escala.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Especifica o **objeto VirtualMachineScaleSet** que contém as propriedades do VMSS que este cmdlet cria.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkName
O nome para a Rede Virtual a ser usada com esse conjunto de escala.  Se nenhum valor for fornecido, uma nova rede virtual com o mesmo nome do Conjunto de Escalas será criada.

```yaml
Type: System.String
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
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmSize
O tamanho das instâncias de VM neste conjunto de escala.  Um tamanho padrão (Standard_DS1_v2) será usado se nenhum Size for especificado.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### -VnetAddressPrefix
O prefixo de endereço da rede virtual usada com este Conjunto de Escalas.  As configurações padrão de prefixo de endereço de rede virtual (192.168.0.0/16) serão usadas se nenhum valor for fornecido.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### -Zone
Uma lista de zonas de disponibilidade que denotam o IP alocado para o recurso precisa vir.

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

### -Confirm
Solicita a confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

### System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## SAÍDAS

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## NOTES

## LINKS RELACIONADOS

[Get-AzVmss](./Get-AzVmss.md)

[Remove-AzVmss](./Remove-AzVmss.md)

[Restart-AzVmss](./Restart-AzVmss.md)

[Set-AzVmss](./Set-AzVmss.md)

[Start-AzVmss](./Start-AzVmss.md)

[Stop-AzVmss](./Stop-AzVmss.md)

[Update-AzVmss](./Update-AzVmss.md)


