---
title: Introdução aos cmdlets do Azure PowerShell | Microsoft Docs
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 11/15/2017
ms.openlocfilehash: 3114f9e9b36dc374f9fb2d402c448cff7fef0aa3
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2018
ms.locfileid: "51211444"
---
# <a name="getting-started-with-azure-powershell"></a>Introdução ao Azure PowerShell

O Azure PowerShell foi projetado para gerenciar e administrar os recursos do Azure da linha de comando e para a compilação de scripts de automação que funcionam no Azure Resource Manager. Você pode usá-lo em seu navegador com o [Azure Cloud Shell](/azure/cloud-shell/overview), ou você pode instalá-lo em seu computador local e usá-lo em qualquer sessão do PowerShell. Este artigo ajuda você a começar a usá-lo, além de ensinar os conceitos básicos por trás dele.

## <a name="connect"></a>Connect

A maneira mais simples de começar é [iniciar o Cloud Shell](/azure/cloud-shell/quickstart).

1. Inicie o Cloud Shell no painel de navegação superior do portal do Azure.

   ![Ícone do Shell](~/media/get-started-azureps/shell-icon.png)

2. Escolha a assinatura que você deseja usar e crie uma conta de armazenamento.

   ![Criar uma conta de armazenamento](~/media/get-started-azureps/storage-prompt.png)

Quando o armazenamento tiver sido criado, o Cloud Shell abrirá uma sessão do PowerShell no navegador.

![Cloud Shell para PowerShell](~/media/get-started-azureps/cloud-powershell.png)

Você também pode instalar o Azure PowerShell e usá-lo localmente em uma sessão do PowerShell.

## <a name="install-azure-powershell"></a>Instalar o Azure PowerShell

A primeira etapa é certificar-se de que você tem a versão mais recente do Azure PowerShell instalada. Para saber mais sobre a versão mais recente, veja as [notas de versão](./release-notes-azureps.md).

1. [Instale o Azure PowerShell](install-azurerm-ps.md).

2. Para verificar se a instalação foi bem-sucedida, execute `Get-Module AzureRM -ListAvailable` na linha de comando.

## <a name="log-in-to-azure"></a>Fazer logon no Azure

Logon interativo:

1. Digite `Login-AzureRmAccount`. Será exibida a caixa de diálogo solicitando as credenciais do Azure. A opção '-EnvironmentName' pode permitir que você faça logon no Azure China ou Azure Alemanha.

   Por exemplo, Login-AzureRmAccount -EnvironmentName AzureChinaCloud

2. Digite o endereço de e-mail e a senha associada à sua conta. O Azure autentica e salva as informações de credenciais e, em seguida, fecha a janela.

Depois de entrar em uma conta do Azure, use os cmdlets do Azure PowerShell para acessar e gerenciar os recursos em sua assinatura.

## <a name="create-a-resource-group"></a>Criar um grupo de recursos

Agora que tudo foi configurado, vamos usar o Azure PowerShell para criar recursos no Azure.

Primeiro, crie um Grupo de Recursos. Os Grupos de recursos no Azure fornecem uma maneira de gerenciar vários recursos que você deseja agrupar logicamente. Por exemplo, você pode criar um Grupo de recursos para um aplicativo ou projeto e adicionar uma máquina virtual, um banco de dados e um serviço CDN dentro dele.

Vamos criar um grupo de recursos chamado "MyResourceGroup" na região Europa Ocidental do Azure. Para fazer isso, digite o seguinte comando:

```powershell-interactive
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```Output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

## <a name="create-a-windows-virtual-machine"></a>Criar uma máquina virtual do Windows

Agora que temos nosso grupo de recursos, vamos criar uma VM do Windows dentro dele. Para criar uma nova VM, primeiro crie os outros recursos necessários e atribua-os a uma configuração. Em seguida, podemos usar essa configuração para criar a VM.

### <a name="create-the-required-network-resources"></a>Criar os recursos de rede necessários

Primeiro, precisamos criar uma configuração de sub-rede para usar com o processo de criação da rede virtual. Também criamos um endereço IP público para que possamos nos conectar a essa VM. Criamos um grupo de segurança de rede para proteger o acesso ao endereço público. Finalmente, criamos a NIC virtual usando todos os recursos anteriores.

```powershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myWindowsVM"

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet1 -AddressPrefix 192.168.1.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET1 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 3389
$nsgRuleRDP = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleRDP  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 3389 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup1 -SecurityRules $nsgRuleRDP

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic1 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-virtual-machine"></a>Criar a máquina virtual

Primeiro, precisamos de um conjunto de credenciais para o sistema operacional.

```powershell-interactive
# Create user object
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

Agora que temos os recursos necessários, podemos criar a VM. Para esta etapa, criamos um objeto de configuração da VM, depois, usamos a configuração para criar a VM.

```powershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Windows -ComputerName $vmName -Credential $cred |
  Set-AzureRmVMSourceImage -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

O comando `New-AzureRmVM` gera resultados após a VM ter sido totalmente criada e estar pronta para ser usada.

```Output
RequestId IsSuccessStatusCode StatusCode ReasonPhrase
--------- ------------------- ---------- ------------
                         True         OK OK
```

Agora faça logon em sua VM do Windows Server criada recentemente usando a Área de Trabalho Remota e o endereço IP público da VM. O comando a seguir exibe o endereço IP público criado no script anterior.

```powershell-interactive
$publicIp | Select-Object Name,IpAddress
```

```Output
Name                  IpAddress
----                  ---------
mypublicdns1400512543 xx.xx.xx.xx
```

Se você estiver em um sistema baseado em Windows, faça isso na linha de comando usando o comando mstsc:

```powershell-interactive
mstsc /v:xx.xxx.xx.xxx
```

Forneça a mesma combinação de nome de usuário/senha usada ao criar a VM para efetuar o logon.

## <a name="create-a-linux-virtual-machine"></a>Criar uma máquina virtual do Linux

Para criar uma nova VM do Linux, primeiro crie os outros recursos necessários e atribua-os a uma configuração. Em seguida, podemos usar essa configuração para criar a VM. Isso pressupõe que você já criou o grupo de recursos conforme mostrado anteriormente. Além disso, você precisará ter uma chave pública SSH chamada `id_rsa.pub` no diretório .ssh do perfil do usuário.

### <a name="create-the-required-network-resources"></a>Criar os recursos de rede necessários

Primeiro, precisamos criar uma configuração de sub-rede para usar com o processo de criação da rede virtual. Também criamos um endereço IP público para que possamos nos conectar a essa VM. Criamos um grupo de segurança de rede para proteger o acesso ao endereço público. Finalmente, criamos a NIC virtual usando todos os recursos anteriores.

```powershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString ' ' -AsPlainText -Force
$cred = New-Object System.Management.Automation.PSCredential ("azureuser", $securePassword)

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 192.168.2.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET2 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 22
$nsgRuleSSH = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleSSH  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 22 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup2 -SecurityRules $nsgRuleSSH

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic2 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-virtual-machine"></a>Criar a máquina virtual

Agora que temos os recursos necessários, podemos criar a VM. Para esta etapa, criamos um objeto de configuração da VM, depois, usamos a configuração para criar a VM.

```powershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

Agora que a VM foi criada, faça logon em sua nova VM do Linux usando SSH com o endereço IP público da VM criada:

```bash
ssh xx.xxx.xxx.xxx
```

```Output
Welcome to Ubuntu 14.04.4 LTS (GNU/Linux 3.19.0-65-generic x86_64)

 * Documentation:  https://help.ubuntu.com/

  System information as of Sun Feb 19 00:32:28 UTC 2017

  System load: 0.31              Memory usage: 3%   Processes:       89
  Usage of /:  39.6% of 1.94GB   Swap usage:   0%   Users logged in: 0

  Graph this data and manage this system at:
    https://landscape.canonical.com/

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

my-login@MyLinuxVM:../../..$
```

## <a name="creating-other-resources-in-azure"></a>Criar outros recursos no Azure

Agora percorremos a criação de um Grupo de recursos, uma VM do Linux e uma VM do Windows Server. Você também pode criar vários outros tipos de recursos do Azure.

Por exemplo, para criar um Balanceador de carga de rede do Azure que poderíamos associar às nossas VMs recém-criadas, podemos usar o seguinte comando create:

```powershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

Também poderíamos criar uma nova Rede Virtual privada (conhecida como "VNet" no Azure) para nossa infraestrutura usando o seguinte comando:

```powershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

O que torna o Azure e o Azure PowerShell tão poderosos é que podemos usar isso não apenas para obter a infraestrutura baseada em nuvem, mas também para criar serviços de plataforma gerenciados. Os serviços de plataforma gerenciados também podem ser combinados com a infraestrutura para compilar soluções ainda mais eficientes.

Por exemplo, é possível usar o Azure PowerShell para criar um Serviço de Aplicativo do Azure. Serviço de Aplicativo do Azure é um serviço de plataforma gerenciado que fornece uma ótima maneira para hospedar aplicativos Web sem precisar se preocupar com a infraestrutura. Depois de criar o Serviço de Aplicativo do Azure, você pode criar dois novos Aplicativos Web do Azure dentro do Serviço de Aplicativo usando os seguintes comandos:

```powershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a>Listar os recursos implantados

Usar o cmdlet `Get-AzureRmResource` para listar os recursos em execução no Azure. O exemplo a seguir mostra os recursos que acabamos de criar no novo grupo de recursos.

```powershell-interactive
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```Output
Name                                                  Location   ResourceType
----                                                  --------   ------------
myLinuxVM_OsDisk_1_36ca038791f642ba91270879088c249a   westeurope Microsoft.Compute/disks
myWindowsVM_OsDisk_1_f627e6e2bb454c72897d72e9632adf9a westeurope Microsoft.Compute/disks
myLinuxVM                                             westeurope Microsoft.Compute/virtualMachines
myWindowsVM                                           westeurope Microsoft.Compute/virtualMachines
myWindowsVM/BGInfo                                    westeurope Microsoft.Compute/virtualMachines/extensions
myNic1                                                westeurope Microsoft.Network/networkInterfaces
myNic2                                                westeurope Microsoft.Network/networkInterfaces
myNetworkSecurityGroup1                               westeurope Microsoft.Network/networkSecurityGroups
myNetworkSecurityGroup2                               westeurope Microsoft.Network/networkSecurityGroups
mypublicdns245369171                                  westeurope Microsoft.Network/publicIPAddresses
mypublicdns779537141                                  westeurope Microsoft.Network/publicIPAddresses
MYvNET1                                               westeurope Microsoft.Network/virtualNetworks
MYvNET2                                               westeurope Microsoft.Network/virtualNetworks
micromyresomywi032907510                              westeurope Microsoft.Storage/storageAccounts
```

## <a name="deleting-resources"></a>Excluir os recursos

Para limpar sua conta do Azure, convém remover os recursos que criamos neste exemplo. Usar os cmdlets `Remove-AzureRm*` para excluir os recursos desnecessários. Para remover a VM do Windows que criamos, use o seguinte comando:

```powershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

Você receberá uma solicitação para confirmar se deseja remover os recursos.

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Também é possível usar a exclusão de vários recursos ao mesmo tempo. Por exemplo, o comando a seguir exclui todo o grupo de recursos "MyResourceGroup" que usamos para todos os exemplos neste tutorial de Introdução. Isso remove o grupo de recursos e todos os recursos contidos nele.

```powershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Isso pode demorar vários minutos.

## <a name="get-samples"></a>Obter exemplos

Para saber mais sobre como usar o Azure PowerShell, confira nossos scripts mais comuns para [VMs do Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [VMs do Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Aplicativos Web](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) e [Bancos de Dados SQL](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).

## <a name="next-steps"></a>Próximas etapas

* [Logon com o Azure PowerShell](authenticate-azureps.md)
* [Gerenciar as assinaturas do Azure com o Azure PowerShell](manage-subscriptions-azureps.md)
* [Criar entidades de serviço no Azure usando o Azure PowerShell](create-azure-service-principal-azureps.md)
* Leia as Notas de versão sobre como migrar a partir de uma versão mais antiga: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).
* Obtenha ajuda da comunidade:
  * [Fórum do Azure no MSDN](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [Stackoverflow](http://go.microsoft.com/fwlink/?LinkId=320213)
