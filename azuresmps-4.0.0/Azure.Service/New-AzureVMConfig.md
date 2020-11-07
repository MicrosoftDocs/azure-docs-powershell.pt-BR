---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C6DFD49F-26A5-4199-A844-CA0FC405BEDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f9fc407e2cf7375708fe82253f3d2fb40eb78f60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946197"
---
# <span data-ttu-id="b0293-101">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="b0293-101">New-AzureVMConfig</span></span>

## <span data-ttu-id="b0293-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0293-102">SYNOPSIS</span></span>
<span data-ttu-id="b0293-103">Cria um objeto de configuração de máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="b0293-103">Creates an Azure virtual machine configuration object.</span></span>

## <span data-ttu-id="b0293-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0293-104">SYNTAX</span></span>

### <span data-ttu-id="b0293-105">ImageName (padrão)</span><span class="sxs-lookup"><span data-stu-id="b0293-105">ImageName (Default)</span></span>
```
New-AzureVMConfig [-Name] <String> [-InstanceSize] <String> [[-HostCaching] <String>]
 [[-AvailabilitySetName] <String>] [[-Label] <String>] [-ImageName] <String> [[-MediaLocation] <String>]
 [[-DiskLabel] <String>] [-DisableBootDiagnostics] [-LicenseType <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b0293-106">Diskname</span><span class="sxs-lookup"><span data-stu-id="b0293-106">DiskName</span></span>
```
New-AzureVMConfig [-Name] <String> [-InstanceSize] <String> [[-HostCaching] <String>]
 [[-AvailabilitySetName] <String>] [[-Label] <String>] [-DiskName] <String> [-DisableBootDiagnostics]
 [-LicenseType <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b0293-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0293-107">DESCRIPTION</span></span>
<span data-ttu-id="b0293-108">O cmdlet **New-AzureVMConfig** cria um objeto de configuração de máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="b0293-108">The **New-AzureVMConfig** cmdlet creates an Azure  virtual machine configuration object.</span></span>
<span data-ttu-id="b0293-109">Você pode usar esse objeto para executar uma nova implantação e adicionar uma nova máquina virtual a uma implantação existente.</span><span class="sxs-lookup"><span data-stu-id="b0293-109">You can use this object to perform a new deployment and add a new virtual machine to an existing deployment.</span></span>

## <span data-ttu-id="b0293-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0293-110">EXAMPLES</span></span>

### <span data-ttu-id="b0293-111">Exemplo 1: criar uma configuração de máquina virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="b0293-111">Example 1: Create a Windows virtual machine configuration</span></span>
```
PS C:\> $Image = (Get-AzureVMImage)[4].ImageName 
C:\PS> New-AzureVMConfig -Name "MyVM1" -InstanceSize ExtraSmall -ImageName $Image | Add-AzureProvisioningConfig -Windows -Password $AdminPassword | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "Datadisk1" -LUN 0 | New-AzureVM -ServiceName "MySvc1"
```

<span data-ttu-id="b0293-112">Esse comando cria uma configuração de máquina virtual do Windows com disco do sistema operacional, disco de dados e configuração do provisionamento.</span><span class="sxs-lookup"><span data-stu-id="b0293-112">This command creates a Windows virtual machine configuration with operating system disk, data disk and provisioning configuration.</span></span>
<span data-ttu-id="b0293-113">Essa configuração é usada para criar uma nova máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b0293-113">This configuration is then used to create a new virtual machine.</span></span>

### <span data-ttu-id="b0293-114">Exemplo 2: criar uma configuração de máquina virtual do Linux</span><span class="sxs-lookup"><span data-stu-id="b0293-114">Example 2: Create a Linux virtual machine configuration</span></span>
```
PS C:\> $Image = (Get-AzureVMImage)[7].ImageName
C:\PS> New-AzureVMConfig -Name "MyVM1" -InstanceSize ExtraSmall -ImageName $Image | Add-AzureProvisioningConfig -Linux -LinuxUser $LinuxUser -Password $AdminPassword | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "Datadisk1" -LUN 0 | New-AzureVM -ServiceName "MySvc1"
```

<span data-ttu-id="b0293-115">Esse comando cria uma nova configuração de máquina virtual Linux com disco do sistema operacional, configuração de disco de dados e provisionamento.</span><span class="sxs-lookup"><span data-stu-id="b0293-115">This command creates a new Linux virtual machine configuration with operating system disk, data disk and provisioning configuration.</span></span>
<span data-ttu-id="b0293-116">Essa configuração é usada para criar uma nova máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b0293-116">This configuration is then used to create a new virtual machine.</span></span>

## <span data-ttu-id="b0293-117">OS</span><span class="sxs-lookup"><span data-stu-id="b0293-117">PARAMETERS</span></span>

### <span data-ttu-id="b0293-118">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="b0293-118">-AvailabilitySetName</span></span>
<span data-ttu-id="b0293-119">Especifica o nome do conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="b0293-119">Specifies the name of the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0293-120">-DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="b0293-120">-DisableBootDiagnostics</span></span>
<span data-ttu-id="b0293-121">Indica que a configuração desabilita o diagnóstico de inicialização.</span><span class="sxs-lookup"><span data-stu-id="b0293-121">Indicates that the configuration disables boot diagnostics.</span></span>
<span data-ttu-id="b0293-122">Por padrão, o diagnóstico de inicialização está habilitado na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b0293-122">By default, boot diagnostics are enabled on the virtual machine.</span></span>

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

### <span data-ttu-id="b0293-123">-DiskLabel</span><span class="sxs-lookup"><span data-stu-id="b0293-123">-DiskLabel</span></span>
<span data-ttu-id="b0293-124">Especifica um rótulo para o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b0293-124">Specifies a label for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0293-125">-Diskname</span><span class="sxs-lookup"><span data-stu-id="b0293-125">-DiskName</span></span>
<span data-ttu-id="b0293-126">Especifica um nome para o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b0293-126">Specifies a name for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: DiskName
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0293-127">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="b0293-127">-HostCaching</span></span>
<span data-ttu-id="b0293-128">Especifica o modo de cache do host para o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b0293-128">Specifies the host caching mode for the operating system disk.</span></span>

<span data-ttu-id="b0293-129">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="b0293-129">Valid values are:</span></span>

- <span data-ttu-id="b0293-130">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b0293-130">ReadOnly</span></span>
- <span data-ttu-id="b0293-131">Leitura</span><span class="sxs-lookup"><span data-stu-id="b0293-131">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0293-132">-ImageName</span><span class="sxs-lookup"><span data-stu-id="b0293-132">-ImageName</span></span>
<span data-ttu-id="b0293-133">Especifica o nome da imagem da máquina virtual a ser usada para o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b0293-133">Specifies the name of the virtual machine image to use for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0293-134">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="b0293-134">-InformationAction</span></span>
<span data-ttu-id="b0293-135">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="b0293-135">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b0293-136">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b0293-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b0293-137">Contínuo</span><span class="sxs-lookup"><span data-stu-id="b0293-137">Continue</span></span>
- <span data-ttu-id="b0293-138">Ignorar</span><span class="sxs-lookup"><span data-stu-id="b0293-138">Ignore</span></span>
- <span data-ttu-id="b0293-139">Inquire</span><span class="sxs-lookup"><span data-stu-id="b0293-139">Inquire</span></span>
- <span data-ttu-id="b0293-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b0293-140">SilentlyContinue</span></span>
- <span data-ttu-id="b0293-141">Finaliza</span><span class="sxs-lookup"><span data-stu-id="b0293-141">Stop</span></span>
- <span data-ttu-id="b0293-142">Suspensão</span><span class="sxs-lookup"><span data-stu-id="b0293-142">Suspend</span></span>

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

### <span data-ttu-id="b0293-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b0293-143">-InformationVariable</span></span>
<span data-ttu-id="b0293-144">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="b0293-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b0293-145">-Instanceize</span><span class="sxs-lookup"><span data-stu-id="b0293-145">-InstanceSize</span></span>
<span data-ttu-id="b0293-146">Especifica o tamanho da instância.</span><span class="sxs-lookup"><span data-stu-id="b0293-146">Specifies the size of the instance.</span></span>

<span data-ttu-id="b0293-147">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b0293-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b0293-148">ExtraSmall</span><span class="sxs-lookup"><span data-stu-id="b0293-148">ExtraSmall</span></span>
- <span data-ttu-id="b0293-149">Versalete</span><span class="sxs-lookup"><span data-stu-id="b0293-149">Small</span></span>
- <span data-ttu-id="b0293-150">Port</span><span class="sxs-lookup"><span data-stu-id="b0293-150">Medium</span></span>
- <span data-ttu-id="b0293-151">Muita</span><span class="sxs-lookup"><span data-stu-id="b0293-151">Large</span></span>
- <span data-ttu-id="b0293-152">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="b0293-152">ExtraLarge</span></span>
- <span data-ttu-id="b0293-153">A5</span><span class="sxs-lookup"><span data-stu-id="b0293-153">A5</span></span>
- <span data-ttu-id="b0293-154">A6</span><span class="sxs-lookup"><span data-stu-id="b0293-154">A6</span></span>
- <span data-ttu-id="b0293-155">A7</span><span class="sxs-lookup"><span data-stu-id="b0293-155">A7</span></span>
- <span data-ttu-id="b0293-156">A8</span><span class="sxs-lookup"><span data-stu-id="b0293-156">A8</span></span>
- <span data-ttu-id="b0293-157">A9</span><span class="sxs-lookup"><span data-stu-id="b0293-157">A9</span></span>
- <span data-ttu-id="b0293-158">Basic_A0</span><span class="sxs-lookup"><span data-stu-id="b0293-158">Basic_A0</span></span>
- <span data-ttu-id="b0293-159">Basic_A1</span><span class="sxs-lookup"><span data-stu-id="b0293-159">Basic_A1</span></span>
- <span data-ttu-id="b0293-160">Basic_A2</span><span class="sxs-lookup"><span data-stu-id="b0293-160">Basic_A2</span></span>
- <span data-ttu-id="b0293-161">Basic_A3</span><span class="sxs-lookup"><span data-stu-id="b0293-161">Basic_A3</span></span>
- <span data-ttu-id="b0293-162">Basic_A4</span><span class="sxs-lookup"><span data-stu-id="b0293-162">Basic_A4</span></span>
- <span data-ttu-id="b0293-163">Standard_D1</span><span class="sxs-lookup"><span data-stu-id="b0293-163">Standard_D1</span></span>
- <span data-ttu-id="b0293-164">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="b0293-164">Standard_D2</span></span>
- <span data-ttu-id="b0293-165">Standard_D3</span><span class="sxs-lookup"><span data-stu-id="b0293-165">Standard_D3</span></span>
- <span data-ttu-id="b0293-166">Standard_D4</span><span class="sxs-lookup"><span data-stu-id="b0293-166">Standard_D4</span></span>
- <span data-ttu-id="b0293-167">Standard_D11</span><span class="sxs-lookup"><span data-stu-id="b0293-167">Standard_D11</span></span>
- <span data-ttu-id="b0293-168">Standard_D12</span><span class="sxs-lookup"><span data-stu-id="b0293-168">Standard_D12</span></span>
- <span data-ttu-id="b0293-169">Standard_D13</span><span class="sxs-lookup"><span data-stu-id="b0293-169">Standard_D13</span></span>
- <span data-ttu-id="b0293-170">Standard_D14</span><span class="sxs-lookup"><span data-stu-id="b0293-170">Standard_D14</span></span>

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

### <span data-ttu-id="b0293-171">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="b0293-171">-Label</span></span>
<span data-ttu-id="b0293-172">Especifica um rótulo a ser atribuído à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b0293-172">Specifies a label to assign to the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0293-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b0293-173">-LicenseType</span></span>
<span data-ttu-id="b0293-174">Especifica o tipo de licença para uma imagem ou um disco licenciado no local.</span><span class="sxs-lookup"><span data-stu-id="b0293-174">Specifies the type of license for an image or disk that is licensed on-premises.</span></span>
<span data-ttu-id="b0293-175">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b0293-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b0293-176">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="b0293-176">Windows_Client</span></span>
- <span data-ttu-id="b0293-177">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="b0293-177">Windows_Server</span></span> 

<span data-ttu-id="b0293-178">Especifique esse parâmetro somente para imagens que contenham o sistema operacional Windows Server.</span><span class="sxs-lookup"><span data-stu-id="b0293-178">Specify this parameter only for images that contain the Windows Server operating system.</span></span>

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

### <span data-ttu-id="b0293-179">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="b0293-179">-MediaLocation</span></span>
<span data-ttu-id="b0293-180">Especifica o local de armazenamento do Azure para o novo disco da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b0293-180">Specifies the Azure storage location for the new virtual machine disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0293-181">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0293-181">-Name</span></span>
<span data-ttu-id="b0293-182">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b0293-182">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0293-183">-Perfil</span><span class="sxs-lookup"><span data-stu-id="b0293-183">-Profile</span></span>
<span data-ttu-id="b0293-184">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="b0293-184">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b0293-185">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="b0293-185">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b0293-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0293-186">CommonParameters</span></span>
<span data-ttu-id="b0293-187">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0293-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0293-188">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0293-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0293-189">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0293-189">INPUTS</span></span>

## <span data-ttu-id="b0293-190">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0293-190">OUTPUTS</span></span>

## <span data-ttu-id="b0293-191">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0293-191">NOTES</span></span>

## <span data-ttu-id="b0293-192">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0293-192">RELATED LINKS</span></span>

