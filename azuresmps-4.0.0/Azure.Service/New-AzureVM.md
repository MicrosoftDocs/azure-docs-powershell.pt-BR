---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1999C880-F8F9-4CED-91A9-33E9BBDFE27D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09a3d7be7bf71e73443dcbb31464ee6f7f19b43a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946200"
---
# <span data-ttu-id="be860-101">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="be860-101">New-AzureVM</span></span>

## <span data-ttu-id="be860-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="be860-102">SYNOPSIS</span></span>
<span data-ttu-id="be860-103">Cria uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="be860-103">Creates an Azure virtual machine.</span></span>

## <span data-ttu-id="be860-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be860-104">SYNTAX</span></span>

### <span data-ttu-id="be860-105">ExistingService (padrão)</span><span class="sxs-lookup"><span data-stu-id="be860-105">ExistingService (Default)</span></span>
```
New-AzureVM -ServiceName <String> [-DeploymentLabel <String>] [-DeploymentName <String>] [-VNetName <String>]
 [-DnsSettings <DnsServer[]>] [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]>
 [-WaitForBoot] [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="be860-106">CreateService</span><span class="sxs-lookup"><span data-stu-id="be860-106">CreateService</span></span>
```
New-AzureVM -ServiceName <String> [-Location <String>] [-AffinityGroup <String>] [-ServiceLabel <String>]
 [-ReverseDnsFqdn <String>] [-ServiceDescription <String>] [-DeploymentLabel <String>]
 [-DeploymentName <String>] [-VNetName <String>] [-DnsSettings <DnsServer[]>]
 [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]> [-WaitForBoot]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="be860-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="be860-107">DESCRIPTION</span></span>
<span data-ttu-id="be860-108">O cmdlet **New-AzureVM** adiciona uma nova máquina virtual a um serviço do Azure existente ou cria uma máquina virtual e um serviço na assinatura atual se o *local* ou *AffinityGroup* for especificado.</span><span class="sxs-lookup"><span data-stu-id="be860-108">The **New-AzureVM** cmdlet adds a new virtual machine to an existing Azure service, or creates a virtual machine and service in the current subscription if either the *Location* or *AffinityGroup* is specified.</span></span>

## <span data-ttu-id="be860-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="be860-109">EXAMPLES</span></span>

### <span data-ttu-id="be860-110">Exemplo 1: criar uma máquina virtual para uma configuração do Windows</span><span class="sxs-lookup"><span data-stu-id="be860-110">Example 1: Create a virtual machine for a Windows configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine07" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername PsTestAdmin | New-AzureVM -ServiceName "ContosoService" -AffinityGroup "Contoso" -WaitForBoot
```

<span data-ttu-id="be860-111">Esse comando cria uma configuração de provisionamento com base em uma configuração de máquina virtual para o sistema operacional Windows e a usa para criar uma máquina virtual em um grupo de afinidade especificado.</span><span class="sxs-lookup"><span data-stu-id="be860-111">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine in a specified affinity group.</span></span>

### <span data-ttu-id="be860-112">Exemplo 2: criar uma máquina virtual para uma configuração Linux</span><span class="sxs-lookup"><span data-stu-id="be860-112">Example 2: Create a virtual machine for a Linux configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "SUSEVM02" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[7].ImageName | Add-AzureProvisioningConfig -Linux -LinuxUser "RootMain" -Password "password" -AdminUsername PsTestAdmin | New-AzureVM
```

<span data-ttu-id="be860-113">Esse comando cria uma configuração de provisionamento com base em uma configuração de máquina virtual para Linux e a usa para criar uma máquina virtual em um grupo de afinidade especificado.</span><span class="sxs-lookup"><span data-stu-id="be860-113">This command creates a provisioning configuration based on a virtual machine configuration for Linux, and uses it to create a virtual machine in a specified affinity group.</span></span>

### <span data-ttu-id="be860-114">Exemplo 3: criar uma máquina virtual e adicionar um disco de dados</span><span class="sxs-lookup"><span data-stu-id="be860-114">Example 3: Create a virtual machine and add a data disk</span></span>
```
PS C:\> $Images = Get-AzureVMImage
PS C:\> $Image = $Images[4]
PS C:\> $VirtualMachine02 = New-AzureVMConfig -Name "VirtualMachine02" -InstanceSize ExtraSmall -ImageName $myImage.ImageName | Add-AzureProvisioningConfig -Windows -Password "password" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "DataDisk50" -LUN 0
```

<span data-ttu-id="be860-115">Os primeiros dois comandos recebem imagens disponíveis usando o cmdlet **Get-AzureVMImage** e armazenam uma delas na variável $image.</span><span class="sxs-lookup"><span data-stu-id="be860-115">The first two commands get available images by using the **Get-AzureVMImage** cmdlet, and stores one of them in the $Image variable.</span></span>

<span data-ttu-id="be860-116">Esse comando cria uma configuração de provisionamento com base em uma configuração de máquina virtual para o sistema operacional Windows e a usa para criar uma máquina virtual com um disco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="be860-116">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine with an Azure data disk.</span></span>

### <span data-ttu-id="be860-117">Exemplo 4: criar uma máquina virtual com um endereço IP reservado</span><span class="sxs-lookup"><span data-stu-id="be860-117">Example 4: Create a virtual machine with a reserved IP address</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine06" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService02" -AffinityGroup "Contoso" -ReservedIPName $ipName
```

<span data-ttu-id="be860-118">Esse comando cria uma configuração de provisionamento com base em uma configuração de máquina virtual para o sistema operacional Windows e a usa para criar uma máquina virtual com um endereço IP reservado.</span><span class="sxs-lookup"><span data-stu-id="be860-118">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine with a reserved IP address.</span></span>

## <span data-ttu-id="be860-119">OS</span><span class="sxs-lookup"><span data-stu-id="be860-119">PARAMETERS</span></span>

### <span data-ttu-id="be860-120">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="be860-120">-AffinityGroup</span></span>
<span data-ttu-id="be860-121">Especifica o grupo de afinidade do Azure no qual o serviço de nuvem reside.</span><span class="sxs-lookup"><span data-stu-id="be860-121">Specifies the Azure affinity group in which the cloud service resides.</span></span>
<span data-ttu-id="be860-122">Esse parâmetro é obrigatório apenas quando esse cmdlet cria um serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="be860-122">This parameter is required only when this cmdlet creates a cloud service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be860-123">-DeploymentLabel</span><span class="sxs-lookup"><span data-stu-id="be860-123">-DeploymentLabel</span></span>
<span data-ttu-id="be860-124">Especifica um rótulo para a implantação.</span><span class="sxs-lookup"><span data-stu-id="be860-124">Specifies a label for the deployment.</span></span>

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

### <span data-ttu-id="be860-125">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="be860-125">-DeploymentName</span></span>
<span data-ttu-id="be860-126">Especifica um nome de implantação.</span><span class="sxs-lookup"><span data-stu-id="be860-126">Specifies a deployment name.</span></span>
<span data-ttu-id="be860-127">Se não for especificado, esse cmdlet usará o nome do serviço como o nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="be860-127">If not specified, this cmdlet uses the service name as the deployment name.</span></span>

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

### <span data-ttu-id="be860-128">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="be860-128">-DnsSettings</span></span>
<span data-ttu-id="be860-129">Especifica um objeto de servidor DNS que define as configurações de DNS para a nova implantação.</span><span class="sxs-lookup"><span data-stu-id="be860-129">Specifies a DNS Server object that defines the DNS settings for the new deployment.</span></span>

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be860-130">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="be860-130">-InformationAction</span></span>
<span data-ttu-id="be860-131">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="be860-131">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="be860-132">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="be860-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="be860-133">Contínuo</span><span class="sxs-lookup"><span data-stu-id="be860-133">Continue</span></span>
- <span data-ttu-id="be860-134">Ignorar</span><span class="sxs-lookup"><span data-stu-id="be860-134">Ignore</span></span>
- <span data-ttu-id="be860-135">Inquire</span><span class="sxs-lookup"><span data-stu-id="be860-135">Inquire</span></span>
- <span data-ttu-id="be860-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="be860-136">SilentlyContinue</span></span>
- <span data-ttu-id="be860-137">Finaliza</span><span class="sxs-lookup"><span data-stu-id="be860-137">Stop</span></span>
- <span data-ttu-id="be860-138">Suspensão</span><span class="sxs-lookup"><span data-stu-id="be860-138">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be860-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="be860-139">-InformationVariable</span></span>
<span data-ttu-id="be860-140">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="be860-140">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be860-141">-InternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="be860-141">-InternalLoadBalancerConfig</span></span>
<span data-ttu-id="be860-142">Especifica um balanceador de carga interno.</span><span class="sxs-lookup"><span data-stu-id="be860-142">Specifies an internal load balancer.</span></span>
<span data-ttu-id="be860-143">Esse parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="be860-143">This parameter is not used.</span></span>

```yaml
Type: InternalLoadBalancerConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be860-144">-Local</span><span class="sxs-lookup"><span data-stu-id="be860-144">-Location</span></span>
<span data-ttu-id="be860-145">Especifica o local que hospeda o novo serviço.</span><span class="sxs-lookup"><span data-stu-id="be860-145">Specifies the location that hosts the new service.</span></span>
<span data-ttu-id="be860-146">Se o serviço já existir, não especifique esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="be860-146">If the service already exists, do not specify this parameter.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be860-147">-Perfil</span><span class="sxs-lookup"><span data-stu-id="be860-147">-Profile</span></span>
<span data-ttu-id="be860-148">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="be860-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="be860-149">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="be860-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be860-150">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="be860-150">-ReservedIPName</span></span>
<span data-ttu-id="be860-151">Especifica o nome do endereço IP reservado.</span><span class="sxs-lookup"><span data-stu-id="be860-151">Specifies the name of the reserved IP address.</span></span>

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

### <span data-ttu-id="be860-152">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="be860-152">-ReverseDnsFqdn</span></span>
<span data-ttu-id="be860-153">Especifica o nome de domínio totalmente qualificado para DNS reverso.</span><span class="sxs-lookup"><span data-stu-id="be860-153">Specifies the fully-qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be860-154">-ServiceDescription</span><span class="sxs-lookup"><span data-stu-id="be860-154">-ServiceDescription</span></span>
<span data-ttu-id="be860-155">Especifica uma descrição para o novo serviço.</span><span class="sxs-lookup"><span data-stu-id="be860-155">Specifies a description for the new service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be860-156">-Inlabel</span><span class="sxs-lookup"><span data-stu-id="be860-156">-ServiceLabel</span></span>
<span data-ttu-id="be860-157">Especifica um rótulo para o novo serviço.</span><span class="sxs-lookup"><span data-stu-id="be860-157">Specifies a label for the new service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be860-158">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="be860-158">-ServiceName</span></span>
<span data-ttu-id="be860-159">Especifica o nome do serviço novo ou existente.</span><span class="sxs-lookup"><span data-stu-id="be860-159">Specifies the new or existing service name.</span></span>

<span data-ttu-id="be860-160">Se o serviço não existir, esse cmdlet o cria para você.</span><span class="sxs-lookup"><span data-stu-id="be860-160">If the service does not exist, this cmdlet creates it for you.</span></span>
<span data-ttu-id="be860-161">Use o parâmetro *Location* ou *AffinityGroup* para especificar onde criar o serviço.</span><span class="sxs-lookup"><span data-stu-id="be860-161">Use the *Location* or *AffinityGroup* parameter to specify where to create the service.</span></span>

<span data-ttu-id="be860-162">Se o serviço existir, o parâmetro *Location* ou *AffinityGroup* não será necessário.</span><span class="sxs-lookup"><span data-stu-id="be860-162">If the service exists, the *Location* or *AffinityGroup* parameter is not needed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be860-163">-VMs</span><span class="sxs-lookup"><span data-stu-id="be860-163">-VMs</span></span>
<span data-ttu-id="be860-164">Especifica uma lista de objetos de máquina virtual a serem criados.</span><span class="sxs-lookup"><span data-stu-id="be860-164">Specifies a list of virtual machine objects to create.</span></span>

```yaml
Type: PersistentVM[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be860-165">-VNetName</span><span class="sxs-lookup"><span data-stu-id="be860-165">-VNetName</span></span>
<span data-ttu-id="be860-166">Especifica o nome da rede virtual em que esse cmdlet implanta a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="be860-166">Specifies the virtual network name where this cmdlet deploys the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be860-167">-WaitForBoot</span><span class="sxs-lookup"><span data-stu-id="be860-167">-WaitForBoot</span></span>
<span data-ttu-id="be860-168">Especifica que esse cmdlet aguarda que a máquina virtual atinja o estado **ReadyRole** .</span><span class="sxs-lookup"><span data-stu-id="be860-168">Specifies that this cmdlet waits for the virtual machine to reach the **ReadyRole** state.</span></span>
<span data-ttu-id="be860-169">Esse cmdlet falha se a máquina virtual cai em um dos seguintes Estados enquanto aguarda: FailedStartingVM, ProvisioningFailed, ProvisioningTimeout.</span><span class="sxs-lookup"><span data-stu-id="be860-169">This cmdlet fails if the virtual machine falls in one of the following states while waiting: FailedStartingVM, ProvisioningFailed, ProvisioningTimeout.</span></span>

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

### <span data-ttu-id="be860-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be860-170">CommonParameters</span></span>
<span data-ttu-id="be860-171">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be860-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be860-172">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be860-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be860-173">SENSORES</span><span class="sxs-lookup"><span data-stu-id="be860-173">INPUTS</span></span>

## <span data-ttu-id="be860-174">EXIBE</span><span class="sxs-lookup"><span data-stu-id="be860-174">OUTPUTS</span></span>

## <span data-ttu-id="be860-175">INFORMA</span><span class="sxs-lookup"><span data-stu-id="be860-175">NOTES</span></span>

## <span data-ttu-id="be860-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be860-176">RELATED LINKS</span></span>

[<span data-ttu-id="be860-177">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="be860-177">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="be860-178">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="be860-178">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="be860-179">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="be860-179">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="be860-180">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="be860-180">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)


