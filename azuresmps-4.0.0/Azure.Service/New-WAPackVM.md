---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA7BD103-5C91-4E3B-9E46-2CAEDA5BA615
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5643756cfad93399664298378e97264dedc2f
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947398"
---
# <span data-ttu-id="367d1-101">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="367d1-101">New-WAPackVM</span></span>

## <span data-ttu-id="367d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="367d1-102">SYNOPSIS</span></span>
<span data-ttu-id="367d1-103">Cria uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="367d1-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="367d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="367d1-104">SYNTAX</span></span>

### <span data-ttu-id="367d1-105">CreateVMFromTemplate (padrão)</span><span class="sxs-lookup"><span data-stu-id="367d1-105">CreateVMFromTemplate (Default)</span></span>
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>]
 [-ProductKey <String>] [-Windows] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="367d1-106">CreateLinuxVMFromTemplate</span><span class="sxs-lookup"><span data-stu-id="367d1-106">CreateLinuxVMFromTemplate</span></span>
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>] [-Linux]
 [-AdministratorSSHKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="367d1-107">CreateVMFromOSDisk</span><span class="sxs-lookup"><span data-stu-id="367d1-107">CreateVMFromOSDisk</span></span>
```
New-WAPackVM -Name <String> [-VNet <VMNetwork>] -OSDisk <VirtualHardDisk> -VMSizeProfile <HardwareProfile>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="367d1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="367d1-108">DESCRIPTION</span></span>
<span data-ttu-id="367d1-109">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="367d1-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="367d1-110">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="367d1-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="367d1-111">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="367d1-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="367d1-112">O cmdlet **New-WAPackVM** cria uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="367d1-112">The **New-WAPackVM** cmdlet creates a virtual machine.</span></span>

## <span data-ttu-id="367d1-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="367d1-113">EXAMPLES</span></span>

### <span data-ttu-id="367d1-114">Exemplo 1: criar uma máquina virtual para o sistema operacional Windows usando um modelo</span><span class="sxs-lookup"><span data-stu-id="367d1-114">Example 1: Create a virtual machine for the Windows operating system by using a template</span></span>
```
PS C:\> $Credentials = Get-Credential PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate04"PS C:\> New-WAPackVM -Name "ContosoV023" -Template $Template -VMCredential $Credentials -Windows
```

<span data-ttu-id="367d1-115">O primeiro comando cria um objeto **PSCredential** e, em seguida, armazena-o na variável $Credentials.</span><span class="sxs-lookup"><span data-stu-id="367d1-115">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>
<span data-ttu-id="367d1-116">O cmdlet solicita uma conta e uma senha.</span><span class="sxs-lookup"><span data-stu-id="367d1-116">The cmdlet prompts you for an account and password.</span></span>
<span data-ttu-id="367d1-117">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="367d1-117">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="367d1-118">O segundo comando obtém o modelo de máquina virtual chamado ContosoTemplate04 usando o cmdlet **Get-WAPackVMTemplate** e, em seguida, armazena-o na variável $template.</span><span class="sxs-lookup"><span data-stu-id="367d1-118">The second command gets the virtual machine template named ContosoTemplate04 by using the **Get-WAPackVMTemplate** cmdlet, and then stores it in the $Template variable.</span></span>

<span data-ttu-id="367d1-119">O comando final cria uma máquina virtual chamada ContosoV023, com base no modelo armazenado na variável $Template.</span><span class="sxs-lookup"><span data-stu-id="367d1-119">The final command creates a virtual machine named ContosoV023, based on the template stored in the $Template variable.</span></span>
<span data-ttu-id="367d1-120">O comando especifica o parâmetro *Windows* e, portanto, a máquina virtual deve executar uma versão do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="367d1-120">The command specifies the *Windows* parameter, and, therefore, the virtual machine must run a version of the Windows operating system.</span></span>

### <span data-ttu-id="367d1-121">Exemplo 2: criar uma máquina virtual para o sistema operacional Linux usando um modelo</span><span class="sxs-lookup"><span data-stu-id="367d1-121">Example 2: Create a virtual machine for the Linux operating system by using a template</span></span>
```
PS C:\> $Credentials = Get-Credential
PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate19"
PS C:\> New-WAPackVM -Linux -Name "ContosoV028" -Template $Template -VMCredential $Credentials
```

<span data-ttu-id="367d1-122">O primeiro comando cria um objeto **PSCredential** e, em seguida, armazena-o na variável $Credentials.</span><span class="sxs-lookup"><span data-stu-id="367d1-122">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>

<span data-ttu-id="367d1-123">O segundo comando obtém o modelo de máquina virtual chamado ContosoTemplate19 usando o cmdlet **Get-WAPackVMTemplate** e, em seguida, armazena-o na variável $template.</span><span class="sxs-lookup"><span data-stu-id="367d1-123">The second command gets the virtual machine template named ContosoTemplate19 by using the **Get-WAPackVMTemplate** cmdlet, and then stores it in the $Template variable.</span></span>

<span data-ttu-id="367d1-124">O comando final cria uma máquina virtual chamada ContosoV028, com base no modelo armazenado na variável $Template.</span><span class="sxs-lookup"><span data-stu-id="367d1-124">The final command creates a virtual machine named ContosoV028, based on the template stored in the $Template variable.</span></span>
<span data-ttu-id="367d1-125">O comando especifica o parâmetro *Linux* e, portanto, a máquina virtual deve executar uma versão do sistema operacional Linux.</span><span class="sxs-lookup"><span data-stu-id="367d1-125">The command specifies the *Linux* parameter, and, therefore, the virtual machine must run a version of the Linux operating system.</span></span>

### <span data-ttu-id="367d1-126">Exemplo 3: criar uma máquina virtual a partir de um disco de sistema operacional e dimensionar o perfil</span><span class="sxs-lookup"><span data-stu-id="367d1-126">Example 3: Create a virtual machine from an operating system disk and size profile</span></span>
```
PS C:\> $OSDisk = Get-WAPackVMOSDisk -Name "ContosoDiskOS"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> New-WAPackVM -Name "ContosoV073" -OSDisk $OSDisk -VMSizeProfile $SizeProfile
```

<span data-ttu-id="367d1-127">O primeiro comando obtém um disco do sistema operacional chamado ContosoDiskOS usando o cmdlet **Get-WAPackVMOSDisk** e, em seguida, armazena-o na variável $OSDisk.</span><span class="sxs-lookup"><span data-stu-id="367d1-127">The first command gets an operating system disk named ContosoDiskOS by using the **Get-WAPackVMOSDisk** cmdlet, and then stores it in the $OSDisk variable.</span></span>

<span data-ttu-id="367d1-128">O segundo comando obtém o perfil de tamanho chamado MediumSizeVM usando o cmdlet **Get-WAPackVMSizeProfile** e, em seguida, armazena-o na variável $SizeProfile.</span><span class="sxs-lookup"><span data-stu-id="367d1-128">The second command gets the size profile named MediumSizeVM by using the **Get-WAPackVMSizeProfile** cmdlet, and then stores it in the $SizeProfile variable.</span></span>

<span data-ttu-id="367d1-129">O comando final cria uma máquina virtual nomeada ContosoV073 a partir do disco do sistema operacional armazenado no $OSDisk e o perfil de tamanho armazenado no $SizeProfile.</span><span class="sxs-lookup"><span data-stu-id="367d1-129">The final command creates a virtual machine named ContosoV073 from the operating system disk stored in $OSDisk and the size profile stored in $SizeProfile.</span></span>

## <span data-ttu-id="367d1-130">OS</span><span class="sxs-lookup"><span data-stu-id="367d1-130">PARAMETERS</span></span>

### <span data-ttu-id="367d1-131">-AdministratorSSHKey</span><span class="sxs-lookup"><span data-stu-id="367d1-131">-AdministratorSSHKey</span></span>
<span data-ttu-id="367d1-132">Especifica a chave do Secure Shell (SSH) para a conta de administrador.</span><span class="sxs-lookup"><span data-stu-id="367d1-132">Specifies the Secure Shell (SSH) key for the Administrator account.</span></span>

```yaml
Type: String
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="367d1-133">-Linux</span><span class="sxs-lookup"><span data-stu-id="367d1-133">-Linux</span></span>
<span data-ttu-id="367d1-134">Indica que o cmdlet cria uma máquina virtual para executar o sistema operacional Linux.</span><span class="sxs-lookup"><span data-stu-id="367d1-134">Indicates that the cmdlet creates a virtual machine to run the Linux operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="367d1-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="367d1-135">-Name</span></span>
<span data-ttu-id="367d1-136">Especifica um nome para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="367d1-136">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="367d1-137">-OSDisk</span><span class="sxs-lookup"><span data-stu-id="367d1-137">-OSDisk</span></span>
<span data-ttu-id="367d1-138">Especifica um disco do sistema operacional como um objeto **VirtualHardDisk** .</span><span class="sxs-lookup"><span data-stu-id="367d1-138">Specifies an operating system disk as a **VirtualHardDisk** object.</span></span>
<span data-ttu-id="367d1-139">Para obter um disco do sistema operacional, use o cmdlet **Get-WAPackVMOSDisk** .</span><span class="sxs-lookup"><span data-stu-id="367d1-139">To obtain an operating system disk, use the **Get-WAPackVMOSDisk** cmdlet.</span></span>

```yaml
Type: VirtualHardDisk
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="367d1-140">-ProductKey</span><span class="sxs-lookup"><span data-stu-id="367d1-140">-ProductKey</span></span>
<span data-ttu-id="367d1-141">Especifica uma chave do produto (Product Key).</span><span class="sxs-lookup"><span data-stu-id="367d1-141">Specifies a product key.</span></span>
<span data-ttu-id="367d1-142">A chave do produto (Product Key) é um número de 25 dígitos que identifica a licença do produto.</span><span class="sxs-lookup"><span data-stu-id="367d1-142">The product key is a 25 digit number that identifies the product license.</span></span>
<span data-ttu-id="367d1-143">Use uma chave do produto (Product Key) para um sistema operacional que você planeja instalar em uma máquina virtual ou host.</span><span class="sxs-lookup"><span data-stu-id="367d1-143">Use a product key for an operating system that you plan to install on a virtual machine or host.</span></span>

```yaml
Type: String
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="367d1-144">-Perfil</span><span class="sxs-lookup"><span data-stu-id="367d1-144">-Profile</span></span>
<span data-ttu-id="367d1-145">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="367d1-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="367d1-146">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="367d1-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="367d1-147">-Modelo</span><span class="sxs-lookup"><span data-stu-id="367d1-147">-Template</span></span>
<span data-ttu-id="367d1-148">Especifica um modelo.</span><span class="sxs-lookup"><span data-stu-id="367d1-148">Specifies a template.</span></span>
<span data-ttu-id="367d1-149">O cmdlet cria uma máquina virtual com base no modelo que você especificar.</span><span class="sxs-lookup"><span data-stu-id="367d1-149">The cmdlet creates a virtual machine based on the template that you specify.</span></span>
<span data-ttu-id="367d1-150">Para obter um objeto de modelo, use o cmdlet Get-WAPackVMTemplate.</span><span class="sxs-lookup"><span data-stu-id="367d1-150">To obtain a template object, use the Get-WAPackVMTemplate cmdlet.</span></span>

```yaml
Type: VMTemplate
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="367d1-151">-VMCredential</span><span class="sxs-lookup"><span data-stu-id="367d1-151">-VMCredential</span></span>
<span data-ttu-id="367d1-152">Especifica a credencial para a conta de administrador local.</span><span class="sxs-lookup"><span data-stu-id="367d1-152">Specifies the credential for the local Administrator account.</span></span>
<span data-ttu-id="367d1-153">Para obter um objeto **PSCredential** , use o cmdlet **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="367d1-153">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="367d1-154">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="367d1-154">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="367d1-155">-VMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="367d1-155">-VMSizeProfile</span></span>
<span data-ttu-id="367d1-156">Especifica um perfil de tamanho para uma máquina virtual como um objeto **HardwareProfile** .</span><span class="sxs-lookup"><span data-stu-id="367d1-156">Specifies a size profile for a virtual machine as a **HardwareProfile** object.</span></span>
<span data-ttu-id="367d1-157">Para obter um perfil de tamanho, use o cmdlet **Get-WAPackVMSizeProfile** .</span><span class="sxs-lookup"><span data-stu-id="367d1-157">To obtain a size profile, use the **Get-WAPackVMSizeProfile** cmdlet.</span></span>

```yaml
Type: HardwareProfile
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="367d1-158">-VNet</span><span class="sxs-lookup"><span data-stu-id="367d1-158">-VNet</span></span>
<span data-ttu-id="367d1-159">Especifica uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="367d1-159">Specifies a virtual network.</span></span>
<span data-ttu-id="367d1-160">O cmdlet conecta a máquina virtual à rede virtual que você especificar.</span><span class="sxs-lookup"><span data-stu-id="367d1-160">The cmdlet connects the virtual machine to the virtual network that you specify.</span></span>
<span data-ttu-id="367d1-161">Para obter uma rede virtual, use o cmdlet **Get-WAPackVNet** .</span><span class="sxs-lookup"><span data-stu-id="367d1-161">To obtain a virtual network, use the **Get-WAPackVNet** cmdlet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="367d1-162">-Windows</span><span class="sxs-lookup"><span data-stu-id="367d1-162">-Windows</span></span>
<span data-ttu-id="367d1-163">Indica que o cmdlet cria uma máquina virtual para executar o sistema operacional do Windows.</span><span class="sxs-lookup"><span data-stu-id="367d1-163">Indicates that the cmdlet creates a virtual machine to run the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="367d1-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="367d1-164">CommonParameters</span></span>
<span data-ttu-id="367d1-165">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="367d1-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="367d1-166">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="367d1-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="367d1-167">SENSORES</span><span class="sxs-lookup"><span data-stu-id="367d1-167">INPUTS</span></span>

## <span data-ttu-id="367d1-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="367d1-168">OUTPUTS</span></span>

## <span data-ttu-id="367d1-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="367d1-169">NOTES</span></span>

## <span data-ttu-id="367d1-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="367d1-170">RELATED LINKS</span></span>

[<span data-ttu-id="367d1-171">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="367d1-171">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="367d1-172">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="367d1-172">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="367d1-173">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="367d1-173">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="367d1-174">Currículo-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="367d1-174">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="367d1-175">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="367d1-175">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="367d1-176">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="367d1-176">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="367d1-177">Parar-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="367d1-177">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="367d1-178">Suspender-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="367d1-178">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="367d1-179">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="367d1-179">Get-WAPackVMSizeProfile</span></span>](./Get-WAPackVMSizeProfile.md)

[<span data-ttu-id="367d1-180">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="367d1-180">Get-WAPackVMTemplate</span></span>](./Get-WAPackVMTemplate.md)

[<span data-ttu-id="367d1-181">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="367d1-181">Get-WAPackVMOSDisk</span></span>](./Get-WAPackVMOSDisk.md)


