---
title: Introdução ao Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 09/11/2018
ms.openlocfilehash: 9150089860f0934cb7344cac2cef38546cac28ad
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/18/2018
ms.locfileid: "49399324"
---
# <a name="get-started-with-azure-powershell"></a>Introdução ao Azure PowerShell

O Azure PowerShell foi projetado para gerenciar e administrar os recursos do Azure da linha de comando e para a compilação de scripts de automação que funcionam no Azure Resource Manager. Você pode usá-lo em seu navegador com o [Azure Cloud Shell](/azure/cloud-shell/overview), ou pode instalá-lo em seu computador local. Este artigo ajuda você a começar com o Azure PowerShell, além de ensinar os conceitos básicos por trás dele.

## <a name="install-azure-powershell"></a>Instalar o Azure PowerShell

A primeira etapa é certificar-se de que você tem a versão mais recente do Azure PowerShell instalada. Para saber mais sobre a versão mais recente, veja as [notas de versão](./release-notes-azureps.md).

1. [Instale o Azure PowerShell](install-azurerm-ps.md).

2. Para verificar se a instalação foi bem-sucedida, execute `Get-Module AzureRM -ListAvailable` na linha de comando.

## <a name="azure-cloud-shell"></a>Azure Cloud Shell

A maneira mais simples de começar é [iniciar o Cloud Shell](/azure/cloud-shell/quickstart).

1. Inicie o Cloud Shell no painel de navegação superior do portal do Azure.

   ![Ícone do Shell](~/media/get-started-azureps/shell-icon.png)

2. Escolha a assinatura que você deseja usar e crie uma conta de armazenamento.

   ![Criar uma conta de armazenamento](~/media/get-started-azureps/storage-prompt.png)

Quando o armazenamento tiver sido criado, o Cloud Shell abrirá uma sessão do PowerShell no navegador.

![Cloud Shell para PowerShell](~/media/get-started-azureps/cloud-powershell.png)

Você também pode instalar o Azure PowerShell e usá-lo localmente em uma sessão do PowerShell.

## <a name="sign-in-to-azure"></a>Entrar no Azure

Logon interativo:

1. Digite `Connect-AzureRmAccount`. Será exibida uma caixa de diálogo solicitando as credenciais do Azure. A opção “-Environment” pode permitir que você se autentique no Azure China ou no Azure Alemanha.

   Por exemplo, Connect-AzureRmAccount -Environment AzureChinaCloud

2. Digite o endereço de e-mail e a senha associada à sua conta. O Azure autentica e salva as informações de credenciais e, em seguida, fecha a janela.

Depois de entrar em uma conta do Azure, use os cmdlets do Azure PowerShell para acessar e gerenciar os recursos em sua assinatura.

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a>Criar uma máquina virtual do Windows usando padrões simples

O cmdlet `New-AzureRmVM` fornece uma sintaxe simplificada, facilitando a criação de uma nova máquina virtual. Há apenas dois valores de parâmetro que você deve fornecer: o nome da VM e um conjunto de credenciais para a conta de administrador local na VM.

Primeiro, crie o objeto da credencial.

```azurepowershell-interactive
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

```output
Windows PowerShell credential request.
Enter a username and password for the virtual machine.
User: localAdmin
Password for user localAdmin: *********
```

Depois, crie a VM.

```azurepowershell-interactive
New-AzureRmVM -Name SampleVM -Credential $cred
```

```output
ResourceGroupName        : SampleVM
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/SampleVM/providers/Microsoft.Compute/virtualMachines/SampleVM
VmId                     : 43f6275d-ce50-49c8-a831-5d5974006e63
Name                     : SampleVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : samplevm-2c0867.eastus.cloudapp.azure.com
```

Você deve estar imaginando o que mais é criado e como a VM é configurada. Primeiro, vamos examinar nossos grupos de recursos.

```azurepowershell-interactive
Get-AzureRmResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

O grupo de recursos **cloud-shell-storage-westus** é criado na primeira vez que você usar o Cloud Shell. O grupo de recursos **SampleVM** foi criado pelo cmdlet `New-AzureRmVM`.

Agora, quais outros recursos foram criados nesse novo grupo de recursos?

```azurepowershell-interactive
Get-AzureRmResource |
  Where ResourceGroupName -eq SampleVM |
    Select-Object ResourceGroupName,Location,ResourceType,Name
```

```output
ResourceGroupName          Location ResourceType                            Name
-----------------          -------- ------------                            ----
SAMPLEVM                   eastus   Microsoft.Compute/disks                 SampleVM_OsDisk_1_9b286c54b168457fa1f8c47...
SampleVM                   eastus   Microsoft.Compute/virtualMachines       SampleVM
SampleVM                   eastus   Microsoft.Network/networkInterfaces     SampleVM
SampleVM                   eastus   Microsoft.Network/networkSecurityGroups SampleVM
SampleVM                   eastus   Microsoft.Network/publicIPAddresses     SampleVM
SampleVM                   eastus   Microsoft.Network/virtualNetworks       SampleVM
```

Vamos obter mais detalhes sobre a VM. Este exemplo mostra como recuperar informações sobre a imagem do sistema operacional usada para criar a VM.

```azurepowershell-interactive
Get-AzureRmVM -Name SampleVM -ResourceGroupName SampleVM |
  Select-Object -ExpandProperty StorageProfile |
    Select-Object -ExpandProperty ImageReference
```

```output
Publisher : MicrosoftWindowsServer
Offer     : WindowsServer
Sku       : 2016-Datacenter
Version   : latest
Id        :
```

## <a name="create-a-fully-configured-linux-virtual-machine"></a>Criar uma máquina virtual do Linux totalmente configurada

O exemplo anterior usou os valores simplificados de sintaxe e parâmetro padrão para criar uma máquina virtual do Windows. Neste exemplo, fornecemos valores para todas as opções da máquina virtual.

### <a name="create-a-resource-group"></a>Criar um grupo de recursos

Neste exemplo, queremos criar um grupo de recursos. Os Grupos de recursos no Azure fornecem uma maneira de gerenciar vários recursos que você deseja agrupar logicamente. Por exemplo, você pode criar um Grupo de recursos para um aplicativo ou projeto e adicionar uma máquina virtual, um banco de dados e um serviço CDN dentro dele.

Vamos criar um grupo de recursos chamado "MyResourceGroup" na região Europa Ocidental do Azure. Para fazer isso, digite o seguinte comando:

```azurepowershell-interactive
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

Esse novo grupo de recursos será usado para conter todos os recursos necessários para a nova VM criada. Para criar uma nova VM do Linux, primeiro crie os outros recursos necessários e atribua-os a uma configuração. Em seguida, podemos usar essa configuração para criar a VM. Além disso, você precisará ter uma chave pública SSH chamada `id_rsa.pub` no diretório .ssh do perfil do usuário.

#### <a name="create-the-required-network-resources"></a>Criar os recursos de rede necessários

Primeiro, precisamos criar uma configuração de sub-rede para usar com o processo de criação da rede virtual. Também criamos um endereço IP público para que possamos nos conectar a essa VM. Criamos um grupo de segurança de rede para proteger o acesso ao endereço público. Finalmente, criamos a NIC virtual usando todos os recursos anteriores.

```azurepowershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString 'azurepassword' -AsPlainText -Force
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

### <a name="create-the-vm-configuration"></a>Criar a configuração da VM

Agora que temos os recursos necessários, podemos criar o objeto de configuração da VM.

```azurepowershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content -Raw "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"
```

### <a name="create-the-virtual-machine"></a>Criar a máquina virtual

Agora podemos criar a VM usando o objeto de configuração da VM.

```azurepowershell-interactive
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

Agora que a VM foi criada, entre em sua nova VM do Linux usando SSH com o endereço IP público da VM criada:

```bash
ssh xx.xxx.xxx.xxx
```

```output
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

```azurepowershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

Também poderíamos criar uma nova Rede Virtual privada (conhecida como "VNet" no Azure) para nossa infraestrutura usando o seguinte comando:

```azurepowershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

O que torna o Azure e o Azure PowerShell tão poderosos é que podemos usar isso não apenas para obter a infraestrutura baseada em nuvem, mas também para criar serviços de plataforma gerenciados. Os serviços de plataforma gerenciados também podem ser combinados com a infraestrutura para compilar soluções ainda mais eficientes.

Por exemplo, é possível usar o Azure PowerShell para criar um Serviço de Aplicativo do Azure. Serviço de Aplicativo do Azure é um serviço de plataforma gerenciado que fornece uma ótima maneira para hospedar aplicativos Web sem precisar se preocupar com a infraestrutura. Depois de criar o Serviço de Aplicativo do Azure, você pode criar dois novos Aplicativos Web do Azure dentro do Serviço de Aplicativo usando os seguintes comandos:

```azurepowershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a>Listar os recursos implantados

Usar o cmdlet `Get-AzureRmResource` para listar os recursos em execução no Azure. O exemplo a seguir mostra os recursos que criamos no novo grupo de recursos.

```azurepowershell-interactive
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```output
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

```azurepowershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

Você receberá uma solicitação para confirmar se deseja remover os recursos.

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Também é possível excluir vários recursos ao mesmo tempo. Por exemplo, o comando a seguir exclui o grupo de recursos "MyResourceGroup" que usamos para todos os exemplos até agora.
Todos os recursos no grupo também são excluídos.

```azurepowershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

A tarefa pode demorar vários minutos para ser concluída, dependendo do número e do tipo de recursos.

## <a name="get-samples"></a>Obter exemplos

Para saber mais sobre como usar o Azure PowerShell, confira nossos scripts mais comuns para [VMs do Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [VMs do Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Aplicativos Web](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) e [Bancos de Dados SQL](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).

## <a name="next-steps"></a>Próximas etapas

* [Entrar com o Azure PowerShell](authenticate-azureps.md)
* [Gerenciar as assinaturas do Azure com o Azure PowerShell](manage-subscriptions-azureps.md)
* [Criar entidades de serviço no Azure usando o Azure PowerShell](create-azure-service-principal-azureps.md)
* Leia as notas de versão sobre como migrar a partir de uma versão mais antiga: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).
* Obtenha ajuda da comunidade:
  * [Fórum do Azure no MSDN](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [Stackoverflow](http://go.microsoft.com/fwlink/?LinkId=320213)
