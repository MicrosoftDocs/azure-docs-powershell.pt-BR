---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F94584BC-EC02-412D-B089-B98A6FF8F505
online version: ''
schema: 2.0.0
ms.openlocfilehash: a5b7758a7316fa6c34ffe6b5225cd252f39c5d7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945909"
---
# <span data-ttu-id="93eff-101">New-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="93eff-101">New-AzureQuickVM</span></span>

## <span data-ttu-id="93eff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93eff-102">SYNOPSIS</span></span>
<span data-ttu-id="93eff-103">Configura e cria uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="93eff-103">Configures and creates an Azure virtual machine.</span></span>

## <span data-ttu-id="93eff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93eff-104">SYNTAX</span></span>

### <span data-ttu-id="93eff-105">Windows (padrão)</span><span class="sxs-lookup"><span data-stu-id="93eff-105">Windows (Default)</span></span>
```
New-AzureQuickVM [-Windows] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-AdminUsername <String>]
 [-Certificates <CertificateSettingList>] [-WaitForBoot] [-DisableWinRMHttps] [-EnableWinRMHttp]
 [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey]
 [-NoWinRMEndpoint] [-VNetName <String>] [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>]
 [-HostCaching <String>] [-AvailabilitySetName <String>] [-InstanceSize <String>] [-MediaLocation <String>]
 [-DisableGuestAgent] [-CustomDataFile <String>] [-ReservedIPName <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="93eff-106">Linux</span><span class="sxs-lookup"><span data-stu-id="93eff-106">Linux</span></span>
```
New-AzureQuickVM [-Linux] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-LinuxUser <String>] [-WaitForBoot]
 [-SSHPublicKeys <SSHPublicKeyList>] [-SSHKeyPairs <SSHKeyPairList>] [-VNetName <String>]
 [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>] [-HostCaching <String>] [-AvailabilitySetName <String>]
 [-InstanceSize <String>] [-MediaLocation <String>] [-DisableGuestAgent] [-CustomDataFile <String>]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="93eff-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93eff-107">DESCRIPTION</span></span>
<span data-ttu-id="93eff-108">O cmdlet **New-AzureQuickVM** configura e cria uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="93eff-108">The **New-AzureQuickVM** cmdlet configures and creates an Azure virtual machine.</span></span>
<span data-ttu-id="93eff-109">Este cmdlet pode implantar uma máquina virtual em um serviço do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="93eff-109">This cmdlet can deploy a virtual machine into an existing Azure service.</span></span>
<span data-ttu-id="93eff-110">Esse cmdlet pode, opcionalmente, criar um serviço do Azure que hospede a nova máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93eff-110">This cmdlet can alternatively create an Azure service that hosts the new virtual machine.</span></span>

## <span data-ttu-id="93eff-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93eff-111">EXAMPLES</span></span>

### <span data-ttu-id="93eff-112">Exemplo 1: criar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="93eff-112">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzureQuickVM -Windows -ServiceName "ContosoService17" -Name "VirutalMachine01" -ImageName "Image07" -Password "password" -AdminUsername "AdminMain" -WaitForBoot
```

<span data-ttu-id="93eff-113">Esse comando cria uma máquina virtual que executa o sistema operacional Windows em um serviço existente.</span><span class="sxs-lookup"><span data-stu-id="93eff-113">This command creates a virtual machine that runs the Windows operating system in an existing service.</span></span>
<span data-ttu-id="93eff-114">O cmdlet baseia a máquina virtual na imagem especificada.</span><span class="sxs-lookup"><span data-stu-id="93eff-114">The cmdlet bases the virtual machine on the specified image.</span></span>
<span data-ttu-id="93eff-115">O comando especifica o parâmetro *WaitForBoot* .</span><span class="sxs-lookup"><span data-stu-id="93eff-115">The command specifies the *WaitForBoot* parameter.</span></span>
<span data-ttu-id="93eff-116">Portanto, o cmdlet aguarda a máquina virtual iniciar.</span><span class="sxs-lookup"><span data-stu-id="93eff-116">Therefore, the cmdlet waits for the virtual machine to start.</span></span>

### <span data-ttu-id="93eff-117">Exemplo 2: criar uma máquina virtual que usa certificados</span><span class="sxs-lookup"><span data-stu-id="93eff-117">Example 2: Create a virtual machine that by using certificates</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
PS C:\> New-AzureQuickVM -Windows -ServiceName "MySvc1" -name "MyWinVM1" -ImageName "Image07" -Password "password" -AdminUserName "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] -WaitForBoot
```

<span data-ttu-id="93eff-118">O primeiro comando obtém certificados de uma loja e os armazena na variável $certs.</span><span class="sxs-lookup"><span data-stu-id="93eff-118">The first command gets certificates from a store, and stores them in the $certs variable.</span></span>

<span data-ttu-id="93eff-119">O segundo comando cria uma máquina virtual que executa o sistema operacional do Windows em um serviço existente de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="93eff-119">The second command creates a virtual machine that runs the Windows operating system in an existing service from an image.</span></span>
<span data-ttu-id="93eff-120">Por padrão, o ouvinte do WinRM HTTPS está habilitado na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93eff-120">By default, WinRM Https listener is enabled on the virtual machine.</span></span>
<span data-ttu-id="93eff-121">O comando especifica o parâmetro *WaitForBoot* .</span><span class="sxs-lookup"><span data-stu-id="93eff-121">The command specifies the *WaitForBoot* parameter.</span></span>
<span data-ttu-id="93eff-122">Portanto, o cmdlet aguarda a máquina virtual iniciar.</span><span class="sxs-lookup"><span data-stu-id="93eff-122">Therefore, the cmdlet waits for the virtual machine to start.</span></span>
<span data-ttu-id="93eff-123">O comando carrega um certificado WinRM e X509Certificates para o serviço hospedado.</span><span class="sxs-lookup"><span data-stu-id="93eff-123">The command uploads a WinRM Certificate and X509Certificates to the hosted service.</span></span>

### <span data-ttu-id="93eff-124">Exemplo 3: criar uma máquina virtual que executa o sistema operacional Linux</span><span class="sxs-lookup"><span data-stu-id="93eff-124">Example 3: Create a virtual machine that runs the Linux operating system</span></span>
```
PS C:\> New-AzureQuickVM -Linux -ServiceName "ContosoServiceLinux01" -Name "LinuxVirtualMachine01" -ImageName "LinuxImage01" -LinuxUser "RootMain" -Password "password" -Location "Central US"
```

<span data-ttu-id="93eff-125">Esse comando cria uma máquina virtual que executa o sistema operacional Linux a partir de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="93eff-125">This command creates a virtual machine that runs the Linux operating system from an image.</span></span>
<span data-ttu-id="93eff-126">Esse comando cria um serviço para hospedar a nova máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93eff-126">This command creates a service to host the new virtual machine.</span></span>
<span data-ttu-id="93eff-127">O comando especifica um local para o serviço.</span><span class="sxs-lookup"><span data-stu-id="93eff-127">The command specifies a location for the service.</span></span>

### <span data-ttu-id="93eff-128">Exemplo 4: criar uma máquina virtual e criar um serviço para hospedar a nova máquina virtual</span><span class="sxs-lookup"><span data-stu-id="93eff-128">Example 4: Create a virtual machine and create a service to host the new virtual machine</span></span>
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService03" -Name " VirtualMachine25" -ImageName $images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name
```

<span data-ttu-id="93eff-129">O primeiro comando obtém locais usando o cmdlet **Get-AzureLocation** e, em seguida, armazena-os na variável de matriz $Locations.</span><span class="sxs-lookup"><span data-stu-id="93eff-129">The first command gets locations by using the **Get-AzureLocation** cmdlet, and then stores them in the $Locations array variable.</span></span>

<span data-ttu-id="93eff-130">O segundo comando obtém as imagens disponíveis usando o cmdlet **Get-AzureVMImage** e, em seguida, as armazena na variável de matriz $images.</span><span class="sxs-lookup"><span data-stu-id="93eff-130">The second command gets available images by using the **Get-AzureVMImage** cmdlet, and then stores them in the $Images array variable.</span></span>

<span data-ttu-id="93eff-131">O comando final cria uma grande máquina virtual chamada VirtualMachine25.</span><span class="sxs-lookup"><span data-stu-id="93eff-131">The final command creates a large virtual machine named VirtualMachine25.</span></span>
<span data-ttu-id="93eff-132">A máquina virtual executa o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="93eff-132">The virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="93eff-133">Ele é baseado em uma das imagens no $Images.</span><span class="sxs-lookup"><span data-stu-id="93eff-133">It is based on one of the images in $Images.</span></span>
<span data-ttu-id="93eff-134">O comando cria um serviço denominado ContosoService03 para a nova máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93eff-134">The command creates a service named ContosoService03 for the new virtual machine.</span></span>
<span data-ttu-id="93eff-135">O serviço está em um local no $Locations.</span><span class="sxs-lookup"><span data-stu-id="93eff-135">The service is in a location in $Locations.</span></span>

### <span data-ttu-id="93eff-136">Exemplo 5: criar uma máquina virtual com um nome de IP reservado</span><span class="sxs-lookup"><span data-stu-id="93eff-136">Example 5: Create a virtual machine that has a reserved IP name</span></span>
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService04" -Name "VirtualMachine27" -ImageName $Images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name -ReservedIPName $ipName
```

<span data-ttu-id="93eff-137">O primeiro comando obtém locais e, em seguida, armazena-os na variável de matriz de $Locations.</span><span class="sxs-lookup"><span data-stu-id="93eff-137">The first command gets locations, and then stores them in the $Locations array variable.</span></span>

<span data-ttu-id="93eff-138">O segundo comando obtém as imagens disponíveis e as armazena na variável de matriz de $Images.</span><span class="sxs-lookup"><span data-stu-id="93eff-138">The second command gets available images, and then stores them in the $Images array variable.</span></span>

<span data-ttu-id="93eff-139">O comando final cria uma máquina virtual chamada VirtualMachine27 com base em uma das imagens no $Images.</span><span class="sxs-lookup"><span data-stu-id="93eff-139">The final command creates a virtual machine named VirtualMachine27 based on one of the images in $Images.</span></span>
<span data-ttu-id="93eff-140">O comando cria um serviço em um local no $Locations.</span><span class="sxs-lookup"><span data-stu-id="93eff-140">The command creates a service in a location in $Locations.</span></span>
<span data-ttu-id="93eff-141">A máquina virtual tem um nome de IP reservado, anteriormente armazenado na variável $ipName.</span><span class="sxs-lookup"><span data-stu-id="93eff-141">The virtual machine has a reserved IP name, previously stored in the $ipName variable.</span></span>

## <span data-ttu-id="93eff-142">OS</span><span class="sxs-lookup"><span data-stu-id="93eff-142">PARAMETERS</span></span>

### <span data-ttu-id="93eff-143">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="93eff-143">-AdminUsername</span></span>
<span data-ttu-id="93eff-144">Especifica o nome de usuário da conta de administrador que esse cmdlet cria na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93eff-144">Specifies the user name of the Administrator account that this cmdlet creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93eff-145">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="93eff-145">-AffinityGroup</span></span>
<span data-ttu-id="93eff-146">Especifica o grupo de afinidade para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93eff-146">Specifies the affinity group for the virtual machine.</span></span>
<span data-ttu-id="93eff-147">Especifique esse parâmetro ou o parâmetro de *local* somente se esse cmdlet criar um serviço do Azure para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93eff-147">Specify this parameter or the *Location* parameter only if this cmdlet creates an Azure service for the virtual machine.</span></span>

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

### <span data-ttu-id="93eff-148">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="93eff-148">-AvailabilitySetName</span></span>
<span data-ttu-id="93eff-149">Especifica o nome do conjunto de disponibilidade em que esse cmdlet cria a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93eff-149">Specifies the name of the availability set in which this cmdlet creates the virtual machine.</span></span>

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

### <span data-ttu-id="93eff-150">-Certificados</span><span class="sxs-lookup"><span data-stu-id="93eff-150">-Certificates</span></span>
<span data-ttu-id="93eff-151">Especifica uma lista de certificados que este cmdlet usa para criar o serviço.</span><span class="sxs-lookup"><span data-stu-id="93eff-151">Specifies a list of certificates that this cmdlet uses to create the service.</span></span>

```yaml
Type: CertificateSettingList
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93eff-152">-CustomDatafile</span><span class="sxs-lookup"><span data-stu-id="93eff-152">-CustomDataFile</span></span>
<span data-ttu-id="93eff-153">Especifica um arquivo de dados para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93eff-153">Specifies a data file for the virtual machine.</span></span>
<span data-ttu-id="93eff-154">Esse cmdlet codifica o conteúdo do arquivo como Base64.</span><span class="sxs-lookup"><span data-stu-id="93eff-154">This cmdlet encodes the contents of the file as Base64.</span></span>
<span data-ttu-id="93eff-155">O arquivo deve ter menos de 64 kilobytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="93eff-155">The file must be less than 64 kilobytes long.</span></span>

<span data-ttu-id="93eff-156">Se o sistema operacional convidado for o sistema operacional do Windows, esse cmdlet salvará esses dados como um arquivo binário chamado%SYSTEMDRIVE%\AzureData\CustomData.bin.</span><span class="sxs-lookup"><span data-stu-id="93eff-156">If the guest operating system is the Windows operating system, this cmdlet saves this data as a binary file that is named %SYSTEMDRIVE%\AzureData\CustomData.bin.</span></span>

<span data-ttu-id="93eff-157">Se o sistema operacional convidado for Linux, esse cmdlet passará os dados usando o arquivo ovf-env.xml.</span><span class="sxs-lookup"><span data-stu-id="93eff-157">If the guest operating system is Linux, this cmdlet passes the data by using the ovf-env.xml file.</span></span>
<span data-ttu-id="93eff-158">A instalação copia o arquivo para o diretório/var/lib/waagent.</span><span class="sxs-lookup"><span data-stu-id="93eff-158">Installation copies that file to the /var/lib/waagent directory.</span></span>
<span data-ttu-id="93eff-159">O agente também armazena os dados codificados em base64 no/var/lib/waagent/CustomData.</span><span class="sxs-lookup"><span data-stu-id="93eff-159">The agent also stores the Base64 encoded data in /var/lib/waagent/CustomData.</span></span>

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

### <span data-ttu-id="93eff-160">-DisableGuestAgent</span><span class="sxs-lookup"><span data-stu-id="93eff-160">-DisableGuestAgent</span></span>
<span data-ttu-id="93eff-161">Indica que esse cmdlet desabilita o agente convidado de provisionamento da infraestrutura como serviço (IaaS).</span><span class="sxs-lookup"><span data-stu-id="93eff-161">Indicates that this cmdlet disables the infrastructure as a service (IaaS) provision guest agent.</span></span>

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

### <span data-ttu-id="93eff-162">-DisableWinRMHttps</span><span class="sxs-lookup"><span data-stu-id="93eff-162">-DisableWinRMHttps</span></span>
<span data-ttu-id="93eff-163">Indica que esse cmdlet desabilita o gerenciamento remoto do Windows (WinRM) no HTTPS.</span><span class="sxs-lookup"><span data-stu-id="93eff-163">Indicates that this cmdlet disables Windows Remote Management (WinRM) on HTTPS.</span></span>
<span data-ttu-id="93eff-164">Por padrão, o WinRM está habilitado no HTTPS.</span><span class="sxs-lookup"><span data-stu-id="93eff-164">By default, WinRM is enabled over HTTPS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93eff-165">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="93eff-165">-DnsSettings</span></span>
<span data-ttu-id="93eff-166">Especifica uma matriz de objetos do servidor DNS que define as configurações de DNS para a nova implantação.</span><span class="sxs-lookup"><span data-stu-id="93eff-166">Specifies an array of DNS server objects that defines the DNS settings for the new deployment.</span></span>
<span data-ttu-id="93eff-167">Para criar um objeto **DnsServer** , use o cmdlet **New-AzureDns** .</span><span class="sxs-lookup"><span data-stu-id="93eff-167">To create a **DnsServer** object, use the **New-AzureDns** cmdlet.</span></span>

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93eff-168">-EnableWinRMHttp</span><span class="sxs-lookup"><span data-stu-id="93eff-168">-EnableWinRMHttp</span></span>
<span data-ttu-id="93eff-169">Indica que esse cmdlet habilita o WinRM sobre HTTP.</span><span class="sxs-lookup"><span data-stu-id="93eff-169">Indicates that this cmdlet enables WinRM over HTTP.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93eff-170">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="93eff-170">-HostCaching</span></span>
<span data-ttu-id="93eff-171">Especifica o modo de cache do host para o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="93eff-171">Specifies the host caching mode for the operating system disk.</span></span>
<span data-ttu-id="93eff-172">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="93eff-172">Valid values are:</span></span> 

- <span data-ttu-id="93eff-173">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="93eff-173">ReadOnly</span></span>
- <span data-ttu-id="93eff-174">Leitura</span><span class="sxs-lookup"><span data-stu-id="93eff-174">ReadWrite</span></span>

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

### <span data-ttu-id="93eff-175">-ImageName</span><span class="sxs-lookup"><span data-stu-id="93eff-175">-ImageName</span></span>
<span data-ttu-id="93eff-176">Especifica o nome da imagem de disco que esse cmdlet usa para criar o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="93eff-176">Specifies the name of the disk image this cmdlet uses to create the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93eff-177">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="93eff-177">-InformationAction</span></span>
<span data-ttu-id="93eff-178">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="93eff-178">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="93eff-179">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="93eff-179">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="93eff-180">Contínuo</span><span class="sxs-lookup"><span data-stu-id="93eff-180">Continue</span></span>
- <span data-ttu-id="93eff-181">Ignorar</span><span class="sxs-lookup"><span data-stu-id="93eff-181">Ignore</span></span>
- <span data-ttu-id="93eff-182">Inquire</span><span class="sxs-lookup"><span data-stu-id="93eff-182">Inquire</span></span>
- <span data-ttu-id="93eff-183">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="93eff-183">SilentlyContinue</span></span>
- <span data-ttu-id="93eff-184">Finaliza</span><span class="sxs-lookup"><span data-stu-id="93eff-184">Stop</span></span>
- <span data-ttu-id="93eff-185">Suspensão</span><span class="sxs-lookup"><span data-stu-id="93eff-185">Suspend</span></span>

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

### <span data-ttu-id="93eff-186">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="93eff-186">-InformationVariable</span></span>
<span data-ttu-id="93eff-187">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="93eff-187">Specifies an information variable.</span></span>

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

### <span data-ttu-id="93eff-188">-Instanceize</span><span class="sxs-lookup"><span data-stu-id="93eff-188">-InstanceSize</span></span>
<span data-ttu-id="93eff-189">Especifica o tamanho da instância.</span><span class="sxs-lookup"><span data-stu-id="93eff-189">Specifies the size of the instance.</span></span>
<span data-ttu-id="93eff-190">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="93eff-190">Valid values are:</span></span> 

- <span data-ttu-id="93eff-191">ExtraSmall</span><span class="sxs-lookup"><span data-stu-id="93eff-191">ExtraSmall</span></span>
- <span data-ttu-id="93eff-192">Versalete</span><span class="sxs-lookup"><span data-stu-id="93eff-192">Small</span></span>
- <span data-ttu-id="93eff-193">Port</span><span class="sxs-lookup"><span data-stu-id="93eff-193">Medium</span></span>
- <span data-ttu-id="93eff-194">Muita</span><span class="sxs-lookup"><span data-stu-id="93eff-194">Large</span></span>
- <span data-ttu-id="93eff-195">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="93eff-195">ExtraLarge</span></span>
- <span data-ttu-id="93eff-196">A5</span><span class="sxs-lookup"><span data-stu-id="93eff-196">A5</span></span>
- <span data-ttu-id="93eff-197">A6</span><span class="sxs-lookup"><span data-stu-id="93eff-197">A6</span></span>
- <span data-ttu-id="93eff-198">A7</span><span class="sxs-lookup"><span data-stu-id="93eff-198">A7</span></span>
- <span data-ttu-id="93eff-199">A8</span><span class="sxs-lookup"><span data-stu-id="93eff-199">A8</span></span>
- <span data-ttu-id="93eff-200">A9</span><span class="sxs-lookup"><span data-stu-id="93eff-200">A9</span></span>
- <span data-ttu-id="93eff-201">Basic_A0</span><span class="sxs-lookup"><span data-stu-id="93eff-201">Basic_A0</span></span>
- <span data-ttu-id="93eff-202">Basic_A1</span><span class="sxs-lookup"><span data-stu-id="93eff-202">Basic_A1</span></span>
- <span data-ttu-id="93eff-203">Basic_A2</span><span class="sxs-lookup"><span data-stu-id="93eff-203">Basic_A2</span></span>
- <span data-ttu-id="93eff-204">Basic_A3</span><span class="sxs-lookup"><span data-stu-id="93eff-204">Basic_A3</span></span>
- <span data-ttu-id="93eff-205">Basic_A4</span><span class="sxs-lookup"><span data-stu-id="93eff-205">Basic_A4</span></span>
- <span data-ttu-id="93eff-206">Standard_D1</span><span class="sxs-lookup"><span data-stu-id="93eff-206">Standard_D1</span></span>
- <span data-ttu-id="93eff-207">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="93eff-207">Standard_D2</span></span>
- <span data-ttu-id="93eff-208">Standard_D3</span><span class="sxs-lookup"><span data-stu-id="93eff-208">Standard_D3</span></span>
- <span data-ttu-id="93eff-209">Standard_D4</span><span class="sxs-lookup"><span data-stu-id="93eff-209">Standard_D4</span></span>
- <span data-ttu-id="93eff-210">Standard_D11</span><span class="sxs-lookup"><span data-stu-id="93eff-210">Standard_D11</span></span>
- <span data-ttu-id="93eff-211">Standard_D12</span><span class="sxs-lookup"><span data-stu-id="93eff-211">Standard_D12</span></span>
- <span data-ttu-id="93eff-212">Standard_D13</span><span class="sxs-lookup"><span data-stu-id="93eff-212">Standard_D13</span></span>
- <span data-ttu-id="93eff-213">Standard_D14</span><span class="sxs-lookup"><span data-stu-id="93eff-213">Standard_D14</span></span>

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

### <span data-ttu-id="93eff-214">-Linux</span><span class="sxs-lookup"><span data-stu-id="93eff-214">-Linux</span></span>
<span data-ttu-id="93eff-215">Indica que esse cmdlet cria uma máquina virtual baseada em Linux.</span><span class="sxs-lookup"><span data-stu-id="93eff-215">Indicates that this cmdlet creates a Linux based virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93eff-216">-LinuxUser</span><span class="sxs-lookup"><span data-stu-id="93eff-216">-LinuxUser</span></span>
<span data-ttu-id="93eff-217">Especifica o nome de usuário da conta administrativa do Linux que esse cmdlet cria na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93eff-217">Specifies the user name of the Linux administrative account that this cmdlet creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93eff-218">-Local</span><span class="sxs-lookup"><span data-stu-id="93eff-218">-Location</span></span>
<span data-ttu-id="93eff-219">Especifica o datacenter do Azure que hospeda a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93eff-219">Specifies the Azure datacenter that hosts the virtual machine.</span></span>
<span data-ttu-id="93eff-220">Se você especificar esse parâmetro, o cmdlet criará um serviço do Azure no local especificado.</span><span class="sxs-lookup"><span data-stu-id="93eff-220">If you specify this parameter, the cmdlet creates an Azure service in the specified location.</span></span>
<span data-ttu-id="93eff-221">Especifique esse parâmetro ou o parâmetro *AffinityGroup* somente se esse cmdlet criar um serviço do Azure para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93eff-221">Specify this parameter or the *AffinityGroup* parameter only if this cmdlet creates an Azure service for the virtual machine.</span></span>

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

### <span data-ttu-id="93eff-222">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="93eff-222">-MediaLocation</span></span>
<span data-ttu-id="93eff-223">Especifica o local de armazenamento do Azure em que esse cmdlet cria discos de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="93eff-223">Specifies the Azure Storage location where this cmdlet creates the virtual machines disks.</span></span>

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

### <span data-ttu-id="93eff-224">-Nome</span><span class="sxs-lookup"><span data-stu-id="93eff-224">-Name</span></span>
<span data-ttu-id="93eff-225">Especifica o nome da máquina virtual que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="93eff-225">Specifies the name of the virtual machine that this cmdlet creates.</span></span>

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

### <span data-ttu-id="93eff-226">-NoExportPrivateKey</span><span class="sxs-lookup"><span data-stu-id="93eff-226">-NoExportPrivateKey</span></span>
<span data-ttu-id="93eff-227">Indica que essa configuração não carrega a chave privada.</span><span class="sxs-lookup"><span data-stu-id="93eff-227">Indicates that this configuration does not upload the private key.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93eff-228">-NoWinRMEndpoint</span><span class="sxs-lookup"><span data-stu-id="93eff-228">-NoWinRMEndpoint</span></span>
<span data-ttu-id="93eff-229">Indica que esse cmdlet não adiciona um ponto de extremidade WinRM para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93eff-229">Indicates that this cmdlet does not add a WinRM endpoint for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93eff-230">-Senha</span><span class="sxs-lookup"><span data-stu-id="93eff-230">-Password</span></span>
<span data-ttu-id="93eff-231">Especifica a senha da conta administrativa.</span><span class="sxs-lookup"><span data-stu-id="93eff-231">Specifies the password for the administrative account.</span></span>

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

### <span data-ttu-id="93eff-232">-Perfil</span><span class="sxs-lookup"><span data-stu-id="93eff-232">-Profile</span></span>
<span data-ttu-id="93eff-233">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="93eff-233">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="93eff-234">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="93eff-234">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="93eff-235">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="93eff-235">-ReservedIPName</span></span>
<span data-ttu-id="93eff-236">Especifica o nome do IP reservado.</span><span class="sxs-lookup"><span data-stu-id="93eff-236">Specifies the reserved IP name.</span></span>

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

### <span data-ttu-id="93eff-237">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="93eff-237">-ReverseDnsFqdn</span></span>
<span data-ttu-id="93eff-238">Especifica o nome de domínio totalmente qualificado para a pesquisa reversa de DNS.</span><span class="sxs-lookup"><span data-stu-id="93eff-238">Specifies the fully qualified domain name for reverse DNS look up.</span></span>

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

### <span data-ttu-id="93eff-239">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="93eff-239">-ServiceName</span></span>
<span data-ttu-id="93eff-240">Especifica o nome de um serviço do Azure novo ou existente ao qual esse cmdlet adiciona a nova máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93eff-240">Specifies the name of a new or existing Azure service to which this cmdlet adds the new virtual machine.</span></span>

<span data-ttu-id="93eff-241">Se você especificar um novo serviço, este cmdlet o criará.</span><span class="sxs-lookup"><span data-stu-id="93eff-241">If you specify a new service, this cmdlets creates it.</span></span>
<span data-ttu-id="93eff-242">Para criar um novo serviço, você deve especificar o *local* ou o parâmetro *AffinityGroup* .</span><span class="sxs-lookup"><span data-stu-id="93eff-242">To create a new service, you must specify the *Location* or *AffinityGroup* parameter.</span></span>

<span data-ttu-id="93eff-243">Se você especificar um serviço existente, não especifique *local* ou *AffinityGroup*.</span><span class="sxs-lookup"><span data-stu-id="93eff-243">If you specify an existing service, do not specify *Location* or *AffinityGroup*.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93eff-244">-SSHKeyPairs</span><span class="sxs-lookup"><span data-stu-id="93eff-244">-SSHKeyPairs</span></span>
<span data-ttu-id="93eff-245">Especifica os pares de chaves SSH.</span><span class="sxs-lookup"><span data-stu-id="93eff-245">Specifies SSH key pairs.</span></span>

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93eff-246">-SSHPublicKeys</span><span class="sxs-lookup"><span data-stu-id="93eff-246">-SSHPublicKeys</span></span>
<span data-ttu-id="93eff-247">Especifica as chaves públicas SSH.</span><span class="sxs-lookup"><span data-stu-id="93eff-247">Specifies SSH public keys.</span></span>

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93eff-248">-Subnetnames</span><span class="sxs-lookup"><span data-stu-id="93eff-248">-SubnetNames</span></span>
<span data-ttu-id="93eff-249">Especifica uma matriz de nomes de sub-rede para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93eff-249">Specifies an array of names of subnet for the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93eff-250">-VNetName</span><span class="sxs-lookup"><span data-stu-id="93eff-250">-VNetName</span></span>
<span data-ttu-id="93eff-251">Especifica o nome de uma rede virtual para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93eff-251">Specifies the name of a virtual network for the virtual machine.</span></span>

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

### <span data-ttu-id="93eff-252">-WaitForBoot</span><span class="sxs-lookup"><span data-stu-id="93eff-252">-WaitForBoot</span></span>
<span data-ttu-id="93eff-253">Indica que esse cmdlet aguarda que a máquina virtual atinja o estado ReadyRole.</span><span class="sxs-lookup"><span data-stu-id="93eff-253">Indicates that this cmdlet waits for the virtual machine to reach the state ReadyRole.</span></span>
<span data-ttu-id="93eff-254">Se a máquina virtual alcançar um dos seguintes Estados, o cmdlet falha: FailedStartingVM, ProvisioningFailed ou ProvisioningTimeout.</span><span class="sxs-lookup"><span data-stu-id="93eff-254">If the virtual machine reaches one of the following states, the cmdlet fails: FailedStartingVM, ProvisioningFailed, or ProvisioningTimeout.</span></span>

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

### <span data-ttu-id="93eff-255">-Windows</span><span class="sxs-lookup"><span data-stu-id="93eff-255">-Windows</span></span>
<span data-ttu-id="93eff-256">Indica que esse cmdlet cria um computador virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="93eff-256">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93eff-257">-WinRMCertificate</span><span class="sxs-lookup"><span data-stu-id="93eff-257">-WinRMCertificate</span></span>
<span data-ttu-id="93eff-258">Especifica um certificado que este cmdlet associa a um ponto de extremidade do WinRM.</span><span class="sxs-lookup"><span data-stu-id="93eff-258">Specifies a certificate that this cmdlet associates to a WinRM endpoint.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93eff-259">-X509Certificates</span><span class="sxs-lookup"><span data-stu-id="93eff-259">-X509Certificates</span></span>
<span data-ttu-id="93eff-260">Especifica uma matriz de certificados X509 que são implantados em um serviço hospedado.</span><span class="sxs-lookup"><span data-stu-id="93eff-260">Specifies an array of X509 certificates that are deployed to a hosted service.</span></span>

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93eff-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93eff-261">CommonParameters</span></span>
<span data-ttu-id="93eff-262">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93eff-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93eff-263">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93eff-263">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93eff-264">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93eff-264">INPUTS</span></span>

## <span data-ttu-id="93eff-265">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93eff-265">OUTPUTS</span></span>

## <span data-ttu-id="93eff-266">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93eff-266">NOTES</span></span>

## <span data-ttu-id="93eff-267">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93eff-267">RELATED LINKS</span></span>

[<span data-ttu-id="93eff-268">Get-AzureLocation</span><span class="sxs-lookup"><span data-stu-id="93eff-268">Get-AzureLocation</span></span>](./Get-AzureLocation.md)

[<span data-ttu-id="93eff-269">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="93eff-269">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="93eff-270">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="93eff-270">New-AzureDns</span></span>](./New-AzureDns.md)


