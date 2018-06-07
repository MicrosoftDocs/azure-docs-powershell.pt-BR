---
title: Introdução aos cmdlets do Azure PowerShell | Microsoft Docs
description: ''
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 11/15/2017
ms.openlocfilehash: c7e5584ead961c8d3c598c31330f18d1c95d91b1
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821744"
---
# <a name="getting-started-with-azure-powershell"></a><span data-ttu-id="daca0-102">Introdução ao Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="daca0-102">Getting started with Azure PowerShell</span></span>

<span data-ttu-id="daca0-103">O Azure PowerShell foi projetado para gerenciar e administrar os recursos do Azure da linha de comando e para a compilação de scripts de automação que funcionam no Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="daca0-103">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="daca0-104">Você pode usá-lo em seu navegador com o [Azure Cloud Shell](/azure/cloud-shell/overview), ou você pode instalá-lo em seu computador local e usá-lo em qualquer sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="daca0-104">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span> <span data-ttu-id="daca0-105">Este artigo ajuda você a começar a usá-lo, além de ensinar os conceitos básicos por trás dele.</span><span class="sxs-lookup"><span data-stu-id="daca0-105">This article helps get you started using it, and teaches you the core concepts behind it.</span></span>

## <a name="connect"></a><span data-ttu-id="daca0-106">Connect</span><span class="sxs-lookup"><span data-stu-id="daca0-106">Connect</span></span>

<span data-ttu-id="daca0-107">A maneira mais simples de começar é [iniciar o Cloud Shell](/azure/cloud-shell/quickstart).</span><span class="sxs-lookup"><span data-stu-id="daca0-107">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="daca0-108">Inicie o Cloud Shell no painel de navegação superior do portal do Azure.</span><span class="sxs-lookup"><span data-stu-id="daca0-108">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Ícone do Shell](~/media/get-started-azureps/shell-icon.png)

2. <span data-ttu-id="daca0-110">Escolha a assinatura que você deseja usar e crie uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="daca0-110">Choose the subscription you want to use and create a storage account.</span></span>

   ![Criar uma conta de armazenamento](~/media/get-started-azureps/storage-prompt.png)

<span data-ttu-id="daca0-112">Quando o armazenamento tiver sido criado, o Cloud Shell abrirá uma sessão do PowerShell no navegador.</span><span class="sxs-lookup"><span data-stu-id="daca0-112">Once your storage has been created, the Cloud Shell will open a PowerShell session in the browser.</span></span>

![Cloud Shell para PowerShell](~/media/get-started-azureps/cloud-powershell.png)

<span data-ttu-id="daca0-114">Você também pode instalar o Azure PowerShell e usá-lo localmente em uma sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="daca0-114">You can also install Azure PowerShell and use it locally in a PowerShell session.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="daca0-115">Instalar o Azure Powershell</span><span class="sxs-lookup"><span data-stu-id="daca0-115">Install Azure PowerShell</span></span>

<span data-ttu-id="daca0-116">A primeira etapa é certificar-se de que você tem a versão mais recente do Azure PowerShell instalada.</span><span class="sxs-lookup"><span data-stu-id="daca0-116">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="daca0-117">Para saber mais sobre a versão mais recente, veja as [notas de versão](./release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="daca0-117">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="daca0-118">[Instale o Azure PowerShell](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="daca0-118">[Install Azure PowerShell](install-azurerm-ps.md).</span></span>

2. <span data-ttu-id="daca0-119">Para verificar se a instalação foi bem-sucedida, execute `Get-Module AzureRM -ListAvailable` na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="daca0-119">To verify the installation was successful, run `Get-Module AzureRM -ListAvailable` from your command line.</span></span>

## <a name="log-in-to-azure"></a><span data-ttu-id="daca0-120">Fazer logon no Azure</span><span class="sxs-lookup"><span data-stu-id="daca0-120">Log in to Azure</span></span>

<span data-ttu-id="daca0-121">Logon interativo:</span><span class="sxs-lookup"><span data-stu-id="daca0-121">Sign on interactively:</span></span>

1. <span data-ttu-id="daca0-122">Digite `Login-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="daca0-122">Type `Login-AzureRmAccount`.</span></span> <span data-ttu-id="daca0-123">Será exibida a caixa de diálogo solicitando as credenciais do Azure.</span><span class="sxs-lookup"><span data-stu-id="daca0-123">You will get dialog box asking for your Azure credentials.</span></span> <span data-ttu-id="daca0-124">A opção '-EnvironmentName' pode permitir que você faça logon no Azure China ou Azure Alemanha.</span><span class="sxs-lookup"><span data-stu-id="daca0-124">Option '-EnvironmentName' can let you login in Azure China or Azure Germany.</span></span>

   <span data-ttu-id="daca0-125">Por exemplo, Login-AzureRmAccount -EnvironmentName AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="daca0-125">e.g. Login-AzureRmAccount -EnvironmentName AzureChinaCloud</span></span>

2. <span data-ttu-id="daca0-126">Digite o endereço de e-mail e a senha associada à sua conta.</span><span class="sxs-lookup"><span data-stu-id="daca0-126">Type the email address and password associated with your account.</span></span> <span data-ttu-id="daca0-127">O Azure autentica e salva as informações de credenciais e, em seguida, fecha a janela.</span><span class="sxs-lookup"><span data-stu-id="daca0-127">Azure authenticates and saves the credential information, and then closes the window.</span></span>

<span data-ttu-id="daca0-128">Depois de entrar em uma conta do Azure, use os cmdlets do Azure PowerShell para acessar e gerenciar os recursos em sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="daca0-128">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manager the resources in your subscription.</span></span>

## <a name="create-a-resource-group"></a><span data-ttu-id="daca0-129">Criar um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="daca0-129">Create a resource group</span></span>

<span data-ttu-id="daca0-130">Agora que tudo foi configurado, vamos usar o Azure PowerShell para criar recursos no Azure.</span><span class="sxs-lookup"><span data-stu-id="daca0-130">Now that we've got everything set up, let's use Azure PowerShell to create resources within Azure.</span></span>

<span data-ttu-id="daca0-131">Primeiro, crie um Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="daca0-131">First, create a Resource Group.</span></span> <span data-ttu-id="daca0-132">Os Grupos de recursos no Azure fornecem uma maneira de gerenciar vários recursos que você deseja agrupar logicamente.</span><span class="sxs-lookup"><span data-stu-id="daca0-132">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="daca0-133">Por exemplo, você pode criar um Grupo de recursos para um aplicativo ou projeto e adicionar uma máquina virtual, um banco de dados e um serviço CDN dentro dele.</span><span class="sxs-lookup"><span data-stu-id="daca0-133">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="daca0-134">Vamos criar um grupo de recursos chamado "MyResourceGroup" na região Europa Ocidental do Azure.</span><span class="sxs-lookup"><span data-stu-id="daca0-134">Let's create a resource group named "MyResourceGroup" in the westeurope region of Azure.</span></span> <span data-ttu-id="daca0-135">Para fazer isso, digite o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="daca0-135">To do so type the following command:</span></span>

```powershell
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```Output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

## <a name="create-a-windows-virtual-machine"></a><span data-ttu-id="daca0-136">Criar uma máquina virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="daca0-136">Create a Windows Virtual Machine</span></span>

<span data-ttu-id="daca0-137">Agora que temos nosso grupo de recursos, vamos criar uma VM do Windows dentro dele.</span><span class="sxs-lookup"><span data-stu-id="daca0-137">Now that we have our resource group, let's create a Windows VM within it.</span></span> <span data-ttu-id="daca0-138">Para criar uma nova VM, primeiro crie os outros recursos necessários e atribua-os a uma configuração.</span><span class="sxs-lookup"><span data-stu-id="daca0-138">To create a new VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="daca0-139">Em seguida, podemos usar essa configuração para criar a VM.</span><span class="sxs-lookup"><span data-stu-id="daca0-139">Then we can use that configuration to create the VM.</span></span>

### <a name="create-the-required-network-resources"></a><span data-ttu-id="daca0-140">Criar os recursos de rede necessários</span><span class="sxs-lookup"><span data-stu-id="daca0-140">Create the required network resources</span></span>

<span data-ttu-id="daca0-141">Primeiro, precisamos criar uma configuração de sub-rede para usar com o processo de criação da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="daca0-141">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="daca0-142">Também criamos um endereço IP público para que possamos nos conectar a essa VM.</span><span class="sxs-lookup"><span data-stu-id="daca0-142">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="daca0-143">Criamos um grupo de segurança de rede para proteger o acesso ao endereço público.</span><span class="sxs-lookup"><span data-stu-id="daca0-143">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="daca0-144">Finalmente, criamos a NIC virtual usando todos os recursos anteriores.</span><span class="sxs-lookup"><span data-stu-id="daca0-144">Finally we create the virtual NIC using all of the previous resources.</span></span>

```powershell
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

### <a name="create-the-virtual-machine"></a><span data-ttu-id="daca0-145">Criar a máquina virtual</span><span class="sxs-lookup"><span data-stu-id="daca0-145">Create the virtual machine</span></span>

<span data-ttu-id="daca0-146">Primeiro, precisamos de um conjunto de credenciais para o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="daca0-146">First we need a set of credentials for the OS.</span></span>

```powershell
# Create user object
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

<span data-ttu-id="daca0-147">Agora que temos os recursos necessários, podemos criar a VM.</span><span class="sxs-lookup"><span data-stu-id="daca0-147">Now that we have the required resources we can create the VM.</span></span> <span data-ttu-id="daca0-148">Para esta etapa, criamos um objeto de configuração da VM, depois, usamos a configuração para criar a VM.</span><span class="sxs-lookup"><span data-stu-id="daca0-148">For this step, we create a VM configuration object, then we use the configuration to create the VM.</span></span>

```powershell
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Windows -ComputerName $vmName -Credential $cred |
  Set-AzureRmVMSourceImage -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="daca0-149">O comando `New-AzureRmVM` gera resultados após a VM ter sido totalmente criada e estar pronta para ser usada.</span><span class="sxs-lookup"><span data-stu-id="daca0-149">The `New-AzureRmVM` command outputs results once the VM has been fully created and is ready to be used.</span></span>

```Output
RequestId IsSuccessStatusCode StatusCode ReasonPhrase
--------- ------------------- ---------- ------------
                         True         OK OK
```

<span data-ttu-id="daca0-150">Agora faça logon em sua VM do Windows Server criada recentemente usando a Área de Trabalho Remota e o endereço IP público da VM.</span><span class="sxs-lookup"><span data-stu-id="daca0-150">Now log on to your newly created Windows Server VM using Remote Desktop and the public IP address of the VM.</span></span> <span data-ttu-id="daca0-151">O comando a seguir exibe o endereço IP público criado no script anterior.</span><span class="sxs-lookup"><span data-stu-id="daca0-151">The following command displays the public IP address created in the previous script.</span></span>

```powershell
$publicIp | Select-Object Name,IpAddress
```

```Output
Name                  IpAddress
----                  ---------
mypublicdns1400512543 xx.xx.xx.xx
```

<span data-ttu-id="daca0-152">Se você estiver em um sistema baseado em Windows, faça isso na linha de comando usando o comando mstsc:</span><span class="sxs-lookup"><span data-stu-id="daca0-152">If you are on a Windows-based system, you can do this from the command line using the mstsc command:</span></span>

```powershell
mstsc /v:xx.xxx.xx.xxx
```

<span data-ttu-id="daca0-153">Forneça a mesma combinação de nome de usuário/senha usada ao criar a VM para efetuar o logon.</span><span class="sxs-lookup"><span data-stu-id="daca0-153">Supply the same username/password combination you used when creating the VM to log in.</span></span>

## <a name="create-a-linux-virtual-machine"></a><span data-ttu-id="daca0-154">Criar uma máquina virtual do Linux</span><span class="sxs-lookup"><span data-stu-id="daca0-154">Create a Linux Virtual Machine</span></span>

<span data-ttu-id="daca0-155">Para criar uma nova VM do Linux, primeiro crie os outros recursos necessários e atribua-os a uma configuração.</span><span class="sxs-lookup"><span data-stu-id="daca0-155">To create a new Linux VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="daca0-156">Em seguida, podemos usar essa configuração para criar a VM.</span><span class="sxs-lookup"><span data-stu-id="daca0-156">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="daca0-157">Isso pressupõe que você já criou o grupo de recursos conforme mostrado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="daca0-157">This assumes that you have already created the resource group as previously shown.</span></span> <span data-ttu-id="daca0-158">Além disso, você precisará ter uma chave pública SSH chamada `id_rsa.pub` no diretório .ssh do perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="daca0-158">Also, you will need to have an SSH public key named `id_rsa.pub` in the .ssh directory of your user profile.</span></span>

### <a name="create-the-required-network-resources"></a><span data-ttu-id="daca0-159">Criar os recursos de rede necessários</span><span class="sxs-lookup"><span data-stu-id="daca0-159">Create the required network resources</span></span>

<span data-ttu-id="daca0-160">Primeiro, precisamos criar uma configuração de sub-rede para usar com o processo de criação da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="daca0-160">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="daca0-161">Também criamos um endereço IP público para que possamos nos conectar a essa VM.</span><span class="sxs-lookup"><span data-stu-id="daca0-161">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="daca0-162">Criamos um grupo de segurança de rede para proteger o acesso ao endereço público.</span><span class="sxs-lookup"><span data-stu-id="daca0-162">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="daca0-163">Finalmente, criamos a NIC virtual usando todos os recursos anteriores.</span><span class="sxs-lookup"><span data-stu-id="daca0-163">Finally we create the virtual NIC using all of the previous resources.</span></span>

```powershell
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

### <a name="create-the-virtual-machine"></a><span data-ttu-id="daca0-164">Criar a máquina virtual</span><span class="sxs-lookup"><span data-stu-id="daca0-164">Create the virtual machine</span></span>

<span data-ttu-id="daca0-165">Agora que temos os recursos necessários, podemos criar a VM.</span><span class="sxs-lookup"><span data-stu-id="daca0-165">Now that we have the required resources we can create the VM.</span></span> <span data-ttu-id="daca0-166">Para esta etapa, criamos um objeto de configuração da VM, depois, usamos a configuração para criar a VM.</span><span class="sxs-lookup"><span data-stu-id="daca0-166">For this step, we create a VM configuration object, then we use the configuration to create the VM.</span></span>

```powershell
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

<span data-ttu-id="daca0-167">Agora que a VM foi criada, faça logon em sua nova VM do Linux usando SSH com o endereço IP público da VM criada:</span><span class="sxs-lookup"><span data-stu-id="daca0-167">Now that the VM has been created, you can log on to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

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

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="daca0-168">Criar outros recursos no Azure</span><span class="sxs-lookup"><span data-stu-id="daca0-168">Creating other resources in Azure</span></span>

<span data-ttu-id="daca0-169">Agora percorremos a criação de um Grupo de recursos, uma VM do Linux e uma VM do Windows Server.</span><span class="sxs-lookup"><span data-stu-id="daca0-169">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="daca0-170">Você também pode criar vários outros tipos de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="daca0-170">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="daca0-171">Por exemplo, para criar um Balanceador de carga de rede do Azure que poderíamos associar às nossas VMs recém-criadas, podemos usar o seguinte comando create:</span><span class="sxs-lookup"><span data-stu-id="daca0-171">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```powershell
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

<span data-ttu-id="daca0-172">Também poderíamos criar uma nova Rede Virtual privada (conhecida como "VNet" no Azure) para nossa infraestrutura usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="daca0-172">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```powershell
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="daca0-173">O que torna o Azure e o Azure PowerShell tão poderosos é que podemos usar isso não apenas para obter a infraestrutura baseada em nuvem, mas também para criar serviços de plataforma gerenciados.</span><span class="sxs-lookup"><span data-stu-id="daca0-173">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="daca0-174">Os serviços de plataforma gerenciados também podem ser combinados com a infraestrutura para compilar soluções ainda mais eficientes.</span><span class="sxs-lookup"><span data-stu-id="daca0-174">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="daca0-175">Por exemplo, é possível usar o Azure PowerShell para criar um Serviço de Aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="daca0-175">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="daca0-176">Serviço de Aplicativo do Azure é um serviço de plataforma gerenciado que fornece uma ótima maneira para hospedar aplicativos Web sem precisar se preocupar com a infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="daca0-176">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="daca0-177">Depois de criar o Serviço de Aplicativo do Azure, você pode criar dois novos Aplicativos Web do Azure dentro do Serviço de Aplicativo usando os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="daca0-177">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```powershell
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="daca0-178">Listar os recursos implantados</span><span class="sxs-lookup"><span data-stu-id="daca0-178">Listing deployed resources</span></span>

<span data-ttu-id="daca0-179">Usar o cmdlet `Get-AzureRmResource` para listar os recursos em execução no Azure.</span><span class="sxs-lookup"><span data-stu-id="daca0-179">You can use the `Get-AzureRmResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="daca0-180">O exemplo a seguir mostra os recursos que acabamos de criar no novo grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="daca0-180">The following example shows the resources we just created in the new resource group.</span></span>

```powershell
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

## <a name="deleting-resources"></a><span data-ttu-id="daca0-181">Excluir os recursos</span><span class="sxs-lookup"><span data-stu-id="daca0-181">Deleting resources</span></span>

<span data-ttu-id="daca0-182">Para limpar sua conta do Azure, convém remover os recursos que criamos neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="daca0-182">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="daca0-183">Usar os cmdlets `Remove-AzureRm*` para excluir os recursos desnecessários.</span><span class="sxs-lookup"><span data-stu-id="daca0-183">You can use the `Remove-AzureRm*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="daca0-184">Para remover a VM do Windows que criamos, use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="daca0-184">To remove the Windows VM we created, using the following command:</span></span>

```powershell
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="daca0-185">Você receberá uma solicitação para confirmar se deseja remover os recursos.</span><span class="sxs-lookup"><span data-stu-id="daca0-185">You will be prompted to confirm that you want to remove the resource.</span></span>

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="daca0-186">Também é possível usar a exclusão de vários recursos ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="daca0-186">You can also use the delete many resources at one time.</span></span> <span data-ttu-id="daca0-187">Por exemplo, o comando a seguir exclui todo o grupo de recursos "MyResourceGroup" que usamos para todos os exemplos neste tutorial de Introdução.</span><span class="sxs-lookup"><span data-stu-id="daca0-187">For example, the following command deletes all the resource group "MyResourceGroup" that we've used for all the samples in this Get Started tutorial.</span></span> <span data-ttu-id="daca0-188">Isso remove o grupo de recursos e todos os recursos contidos nele.</span><span class="sxs-lookup"><span data-stu-id="daca0-188">This removes the resource group and all of the resources in it.</span></span>

```powershell
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="daca0-189">Isso pode demorar vários minutos.</span><span class="sxs-lookup"><span data-stu-id="daca0-189">This can take several minutes to complete.</span></span>

## <a name="get-samples"></a><span data-ttu-id="daca0-190">Obter exemplos</span><span class="sxs-lookup"><span data-stu-id="daca0-190">Get samples</span></span>

<span data-ttu-id="daca0-191">Para saber mais sobre como usar o Azure PowerShell, confira nossos scripts mais comuns para [VMs do Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [VMs do Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Aplicativos Web](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) e [Bancos de Dados SQL](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="daca0-191">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="daca0-192">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="daca0-192">Next steps</span></span>

* [<span data-ttu-id="daca0-193">Logon com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="daca0-193">Login with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="daca0-194">Gerenciar as assinaturas do Azure com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="daca0-194">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="daca0-195">Criar entidades de serviço no Azure usando o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="daca0-195">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="daca0-196">Leia as Notas de versão sobre como migrar a partir de uma versão mais antiga: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span><span class="sxs-lookup"><span data-stu-id="daca0-196">Read the Release notes about migrating from an older release: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span></span>
* <span data-ttu-id="daca0-197">Obtenha ajuda da comunidade:</span><span class="sxs-lookup"><span data-stu-id="daca0-197">Get help from the community:</span></span>
  * [<span data-ttu-id="daca0-198">Fórum do Azure no MSDN</span><span class="sxs-lookup"><span data-stu-id="daca0-198">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="daca0-199">Stackoverflow</span><span class="sxs-lookup"><span data-stu-id="daca0-199">stackoverflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
