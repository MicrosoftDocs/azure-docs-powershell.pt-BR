---
title: Introdução ao Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 11/15/2017
ms.openlocfilehash: 5354a75e969e084d6457d0566a516705f365476f
ms.sourcegitcommit: fd11600079ee3844986552bccc4e274a231332b6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/02/2018
ms.locfileid: "39368306"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="ee364-102">Introdução ao Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee364-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="ee364-103">O Azure PowerShell foi projetado para gerenciar e administrar os recursos do Azure da linha de comando e para a compilação de scripts de automação que funcionam no Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="ee364-103">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="ee364-104">Você pode usá-lo em seu navegador com o [Azure Cloud Shell](/azure/cloud-shell/overview), ou pode instalá-lo em seu computador local.</span><span class="sxs-lookup"><span data-stu-id="ee364-104">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview) or you install it on your local machine.</span></span> <span data-ttu-id="ee364-105">Este artigo ajuda você a começar com o Azure PowerShell, além de ensinar os conceitos básicos por trás dele.</span><span class="sxs-lookup"><span data-stu-id="ee364-105">This article helps get you started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="ee364-106">Instalar o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee364-106">Install Azure PowerShell</span></span>

<span data-ttu-id="ee364-107">A primeira etapa é certificar-se de que você tem a versão mais recente do Azure PowerShell instalada.</span><span class="sxs-lookup"><span data-stu-id="ee364-107">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="ee364-108">Para saber mais sobre a versão mais recente, veja as [notas de versão](./release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="ee364-108">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="ee364-109">[Instale o Azure PowerShell](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="ee364-109">[Install Azure PowerShell](install-azurerm-ps.md).</span></span>

2. <span data-ttu-id="ee364-110">Para verificar se a instalação foi bem-sucedida, execute `Get-Module AzureRM -ListAvailable` na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="ee364-110">To verify the installation was successful, run `Get-Module AzureRM -ListAvailable` from your command line.</span></span>

## <a name="azure-cloud-shell"></a><span data-ttu-id="ee364-111">Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="ee364-111">Azure Cloud Shell</span></span>

<span data-ttu-id="ee364-112">A maneira mais simples de começar é [iniciar o Cloud Shell](/azure/cloud-shell/quickstart).</span><span class="sxs-lookup"><span data-stu-id="ee364-112">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="ee364-113">Inicie o Cloud Shell no painel de navegação superior do portal do Azure.</span><span class="sxs-lookup"><span data-stu-id="ee364-113">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Ícone do Shell](~/media/get-started-azureps/shell-icon.png)

2. <span data-ttu-id="ee364-115">Escolha a assinatura que você deseja usar e crie uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ee364-115">Choose the subscription you want to use and create a storage account.</span></span>

   ![Criar uma conta de armazenamento](~/media/get-started-azureps/storage-prompt.png)

<span data-ttu-id="ee364-117">Quando o armazenamento tiver sido criado, o Cloud Shell abrirá uma sessão do PowerShell no navegador.</span><span class="sxs-lookup"><span data-stu-id="ee364-117">Once your storage has been created, the Cloud Shell will open a PowerShell session in the browser.</span></span>

![Cloud Shell para PowerShell](~/media/get-started-azureps/cloud-powershell.png)

<span data-ttu-id="ee364-119">Você também pode instalar o Azure PowerShell e usá-lo localmente em uma sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ee364-119">You can also install Azure PowerShell and use it locally in a PowerShell session.</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="ee364-120">Entrar no Azure</span><span class="sxs-lookup"><span data-stu-id="ee364-120">Sign in to Azure</span></span>

<span data-ttu-id="ee364-121">Logon interativo:</span><span class="sxs-lookup"><span data-stu-id="ee364-121">Sign on interactively:</span></span>

1. <span data-ttu-id="ee364-122">Digite `Connect-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="ee364-122">Type `Connect-AzureRmAccount`.</span></span> <span data-ttu-id="ee364-123">Será exibida a caixa de diálogo solicitando as credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="ee364-123">You will get dialog box asking for your Azure credentials.</span></span> <span data-ttu-id="ee364-124">A opção “-Environment” pode permitir que você se autentique no Azure China ou no Azure Alemanha.</span><span class="sxs-lookup"><span data-stu-id="ee364-124">Option '-Environment' can let you authenticate for Azure China or Azure Germany.</span></span>

   <span data-ttu-id="ee364-125">Por exemplo, Connect-AzureRmAccount -Environment AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="ee364-125">e.g. Connect-AzureRmAccount -Environment AzureChinaCloud</span></span>

2. <span data-ttu-id="ee364-126">Digite o endereço de e-mail e a senha associada à sua conta.</span><span class="sxs-lookup"><span data-stu-id="ee364-126">Type the email address and password associated with your account.</span></span> <span data-ttu-id="ee364-127">O Azure autentica e salva as informações de credenciais e, em seguida, fecha a janela.</span><span class="sxs-lookup"><span data-stu-id="ee364-127">Azure authenticates and saves the credential information, and then closes the window.</span></span>

<span data-ttu-id="ee364-128">Depois de entrar em uma conta do Azure, use os cmdlets do Azure PowerShell para acessar e gerenciar os recursos em sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="ee364-128">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manage the resources in your subscription.</span></span>

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a><span data-ttu-id="ee364-129">Criar uma máquina virtual do Windows usando padrões simples</span><span class="sxs-lookup"><span data-stu-id="ee364-129">Create a Windows virtual machine using simple defaults</span></span>

<span data-ttu-id="ee364-130">O cmdlet `New-AzureRmVM` fornece uma sintaxe simplificada, facilitando a criação de uma nova máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ee364-130">The `New-AzureRmVM` cmdlet provides a simplified syntax making it easy to create a new virtual machine.</span></span> <span data-ttu-id="ee364-131">Há apenas dois valores de parâmetro que você deve fornecer: o nome da VM e um conjunto de credenciais para a conta de administrador local na VM.</span><span class="sxs-lookup"><span data-stu-id="ee364-131">There are only two parameter values you must provide: the name of the VM and a set of credentials for the local administrator account on the VM.</span></span>

<span data-ttu-id="ee364-132">Primeiro, crie o objeto da credencial.</span><span class="sxs-lookup"><span data-stu-id="ee364-132">First, create the credential object.</span></span>

```azurepowershell-interactive
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

```output
Windows PowerShell credential request.
Enter a username and password for the virtual machine.
User: localAdmin
Password for user localAdmin: *********
```

<span data-ttu-id="ee364-133">Depois, crie a VM.</span><span class="sxs-lookup"><span data-stu-id="ee364-133">Next, create the VM.</span></span>

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

<span data-ttu-id="ee364-134">Foi fácil.</span><span class="sxs-lookup"><span data-stu-id="ee364-134">That was easy.</span></span> <span data-ttu-id="ee364-135">No entanto, você deve estar imaginando o que mais é criado e como a VM é configurada.</span><span class="sxs-lookup"><span data-stu-id="ee364-135">But, you may wonder what else is created and how is the VM configured.</span></span> <span data-ttu-id="ee364-136">Primeiro, vamos examinar nossos grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="ee364-136">First, let's look at our resource groups.</span></span>

```azurepowershell-interactive
Get-AzureRmResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

<span data-ttu-id="ee364-137">O grupo de recursos **cloud-shell-storage-westus** é criado na primeira vez que você usar o Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="ee364-137">The **cloud-shell-storage-westus** resource group is created the first time you use the Cloud Shell.</span></span> <span data-ttu-id="ee364-138">O grupo de recursos **SampleVM** foi criado pelo cmdlet `New-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="ee364-138">The **SampleVM** resource group was created by the `New-AzureRmVM` cmdlet.</span></span>

<span data-ttu-id="ee364-139">Agora, quais outros recursos foram criados nesse novo grupo de recursos?</span><span class="sxs-lookup"><span data-stu-id="ee364-139">Now, what other resources were created in this new resource group?</span></span>

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

<span data-ttu-id="ee364-140">Vamos obter mais detalhes sobre a VM.</span><span class="sxs-lookup"><span data-stu-id="ee364-140">Let's get some more details about the VM.</span></span> <span data-ttu-id="ee364-141">Este exemplo mostra como recuperar informações sobre a imagem do sistema operacional usada para criar a VM.</span><span class="sxs-lookup"><span data-stu-id="ee364-141">This examples shows how to retrieve information about the OS Image used to create the VM.</span></span>

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

## <a name="create-a-fully-configured-linux-virtual-machine"></a><span data-ttu-id="ee364-142">Criar uma máquina virtual do Linux totalmente configurada</span><span class="sxs-lookup"><span data-stu-id="ee364-142">Create a fully configured Linux Virtual Machine</span></span>

<span data-ttu-id="ee364-143">O exemplo anterior usou os valores simplificados de sintaxe e parâmetro padrão para criar uma máquina virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="ee364-143">The previous example used the simplified syntax and default parameter values to create a Windows virtual machine.</span></span> <span data-ttu-id="ee364-144">Neste exemplo, fornecemos valores para todas as opções da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ee364-144">In this example, we provide values for all options of the virtual machine.</span></span>

### <a name="create-a-resource-group"></a><span data-ttu-id="ee364-145">Criar um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ee364-145">Create a resource group</span></span>

<span data-ttu-id="ee364-146">Neste exemplo, queremos criar um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ee364-146">For this example we want to create a Resource Group.</span></span> <span data-ttu-id="ee364-147">Os Grupos de recursos no Azure fornecem uma maneira de gerenciar vários recursos que você deseja agrupar logicamente.</span><span class="sxs-lookup"><span data-stu-id="ee364-147">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="ee364-148">Por exemplo, você pode criar um Grupo de recursos para um aplicativo ou projeto e adicionar uma máquina virtual, um banco de dados e um serviço CDN dentro dele.</span><span class="sxs-lookup"><span data-stu-id="ee364-148">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="ee364-149">Vamos criar um grupo de recursos chamado "MyResourceGroup" na região Europa Ocidental do Azure.</span><span class="sxs-lookup"><span data-stu-id="ee364-149">Let's create a resource group named "MyResourceGroup" in the westeurope region of Azure.</span></span> <span data-ttu-id="ee364-150">Para fazer isso, digite o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="ee364-150">To do so type the following command:</span></span>

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

<span data-ttu-id="ee364-151">Esse novo grupo de recursos será usado para conter todos os recursos necessários para a nova VM criada.</span><span class="sxs-lookup"><span data-stu-id="ee364-151">This new resource group will be used to contain all of the resources needed for the new VM we create.</span></span> <span data-ttu-id="ee364-152">Para criar uma nova VM do Linux, primeiro crie os outros recursos necessários e atribua-os a uma configuração.</span><span class="sxs-lookup"><span data-stu-id="ee364-152">To create a new Linux VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="ee364-153">Em seguida, podemos usar essa configuração para criar a VM.</span><span class="sxs-lookup"><span data-stu-id="ee364-153">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="ee364-154">Além disso, você precisará ter uma chave pública SSH chamada `id_rsa.pub` no diretório .ssh do perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="ee364-154">Also, you will need to have an SSH public key named `id_rsa.pub` in the .ssh directory of your user profile.</span></span>

#### <a name="create-the-required-network-resources"></a><span data-ttu-id="ee364-155">Criar os recursos de rede necessários</span><span class="sxs-lookup"><span data-stu-id="ee364-155">Create the required network resources</span></span>

<span data-ttu-id="ee364-156">Primeiro, precisamos criar uma configuração de sub-rede para usar com o processo de criação da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="ee364-156">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="ee364-157">Também criamos um endereço IP público para que possamos nos conectar a essa VM.</span><span class="sxs-lookup"><span data-stu-id="ee364-157">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="ee364-158">Criamos um grupo de segurança de rede para proteger o acesso ao endereço público.</span><span class="sxs-lookup"><span data-stu-id="ee364-158">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="ee364-159">Finalmente, criamos a NIC virtual usando todos os recursos anteriores.</span><span class="sxs-lookup"><span data-stu-id="ee364-159">Finally we create the virtual NIC using all of the previous resources.</span></span>

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

### <a name="create-the-vm-configuration"></a><span data-ttu-id="ee364-160">Criar a configuração da VM</span><span class="sxs-lookup"><span data-stu-id="ee364-160">Create the VM configuration</span></span>

<span data-ttu-id="ee364-161">Agora que temos os recursos necessários, podemos criar o objeto de configuração da VM.</span><span class="sxs-lookup"><span data-stu-id="ee364-161">Now that we have the required resources we can create the VM configuration object.</span></span>

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

### <a name="create-the-virtual-machine"></a><span data-ttu-id="ee364-162">Criar a máquina virtual</span><span class="sxs-lookup"><span data-stu-id="ee364-162">Create the virtual machine</span></span>

<span data-ttu-id="ee364-163">Agora podemos criar a VM usando o objeto de configuração da VM.</span><span class="sxs-lookup"><span data-stu-id="ee364-163">Now we can create the VM using the VM configuration object.</span></span>

```azurepowershell-interactive
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="ee364-164">Agora que a VM foi criada, faça logon em sua nova VM do Linux usando SSH com o endereço IP público da VM criada:</span><span class="sxs-lookup"><span data-stu-id="ee364-164">Now that the VM has been created, you can log on to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

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

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="ee364-165">Criar outros recursos no Azure</span><span class="sxs-lookup"><span data-stu-id="ee364-165">Creating other resources in Azure</span></span>

<span data-ttu-id="ee364-166">Agora percorremos a criação de um Grupo de recursos, uma VM do Linux e uma VM do Windows Server.</span><span class="sxs-lookup"><span data-stu-id="ee364-166">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="ee364-167">Você também pode criar vários outros tipos de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="ee364-167">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="ee364-168">Por exemplo, para criar um Balanceador de carga de rede do Azure que poderíamos associar às nossas VMs recém-criadas, podemos usar o seguinte comando create:</span><span class="sxs-lookup"><span data-stu-id="ee364-168">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```azurepowershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

<span data-ttu-id="ee364-169">Também poderíamos criar uma nova Rede Virtual privada (conhecida como "VNet" no Azure) para nossa infraestrutura usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="ee364-169">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```azurepowershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="ee364-170">O que torna o Azure e o Azure PowerShell tão poderosos é que podemos usar isso não apenas para obter a infraestrutura baseada em nuvem, mas também para criar serviços de plataforma gerenciados.</span><span class="sxs-lookup"><span data-stu-id="ee364-170">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="ee364-171">Os serviços de plataforma gerenciados também podem ser combinados com a infraestrutura para compilar soluções ainda mais eficientes.</span><span class="sxs-lookup"><span data-stu-id="ee364-171">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="ee364-172">Por exemplo, é possível usar o Azure PowerShell para criar um Serviço de Aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="ee364-172">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="ee364-173">Serviço de Aplicativo do Azure é um serviço de plataforma gerenciado que fornece uma ótima maneira para hospedar aplicativos Web sem precisar se preocupar com a infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="ee364-173">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="ee364-174">Depois de criar o Serviço de Aplicativo do Azure, você pode criar dois novos Aplicativos Web do Azure dentro do Serviço de Aplicativo usando os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="ee364-174">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```azurepowershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="ee364-175">Listar os recursos implantados</span><span class="sxs-lookup"><span data-stu-id="ee364-175">Listing deployed resources</span></span>

<span data-ttu-id="ee364-176">Usar o cmdlet `Get-AzureRmResource` para listar os recursos em execução no Azure.</span><span class="sxs-lookup"><span data-stu-id="ee364-176">You can use the `Get-AzureRmResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="ee364-177">O exemplo a seguir mostra os recursos que acabamos de criar no novo grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ee364-177">The following example shows the resources we just created in the new resource group.</span></span>

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

## <a name="deleting-resources"></a><span data-ttu-id="ee364-178">Excluir os recursos</span><span class="sxs-lookup"><span data-stu-id="ee364-178">Deleting resources</span></span>

<span data-ttu-id="ee364-179">Para limpar sua conta do Azure, convém remover os recursos que criamos neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="ee364-179">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="ee364-180">Usar os cmdlets `Remove-AzureRm*` para excluir os recursos desnecessários.</span><span class="sxs-lookup"><span data-stu-id="ee364-180">You can use the `Remove-AzureRm*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="ee364-181">Para remover a VM do Windows que criamos, use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="ee364-181">To remove the Windows VM we created, using the following command:</span></span>

```azurepowershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="ee364-182">Você receberá uma solicitação para confirmar se deseja remover os recursos.</span><span class="sxs-lookup"><span data-stu-id="ee364-182">You will be prompted to confirm that you want to remove the resource.</span></span>

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="ee364-183">Também é possível usar a exclusão de vários recursos ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="ee364-183">You can also use the delete many resources at one time.</span></span> <span data-ttu-id="ee364-184">Por exemplo, o comando a seguir exclui todo o grupo de recursos "MyResourceGroup" que usamos para todos os exemplos neste tutorial de Introdução.</span><span class="sxs-lookup"><span data-stu-id="ee364-184">For example, the following command deletes all the resource group "MyResourceGroup" that we've used for all the samples in this Get Started tutorial.</span></span> <span data-ttu-id="ee364-185">Isso remove o grupo de recursos e todos os recursos contidos nele.</span><span class="sxs-lookup"><span data-stu-id="ee364-185">This removes the resource group and all of the resources in it.</span></span>

```azurepowershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="ee364-186">Isso pode demorar vários minutos.</span><span class="sxs-lookup"><span data-stu-id="ee364-186">This can take several minutes to complete.</span></span>

## <a name="get-samples"></a><span data-ttu-id="ee364-187">Obter exemplos</span><span class="sxs-lookup"><span data-stu-id="ee364-187">Get samples</span></span>

<span data-ttu-id="ee364-188">Para saber mais sobre como usar o Azure PowerShell, confira nossos scripts mais comuns para [VMs do Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [VMs do Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Aplicativos Web](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) e [Bancos de Dados SQL](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="ee364-188">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="ee364-189">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="ee364-189">Next steps</span></span>

* [<span data-ttu-id="ee364-190">Entrar com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee364-190">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="ee364-191">Gerenciar as assinaturas do Azure com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee364-191">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="ee364-192">Criar entidades de serviço no Azure usando o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee364-192">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="ee364-193">Leia as Notas de versão sobre como migrar a partir de uma versão mais antiga: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span><span class="sxs-lookup"><span data-stu-id="ee364-193">Read the Release notes about migrating from an older release: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span></span>
* <span data-ttu-id="ee364-194">Obtenha ajuda da comunidade:</span><span class="sxs-lookup"><span data-stu-id="ee364-194">Get help from the community:</span></span>
  * [<span data-ttu-id="ee364-195">Fórum do Azure no MSDN</span><span class="sxs-lookup"><span data-stu-id="ee364-195">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="ee364-196">Stackoverflow</span><span class="sxs-lookup"><span data-stu-id="ee364-196">stackoverflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
