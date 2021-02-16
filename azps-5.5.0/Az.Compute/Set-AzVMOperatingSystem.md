---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: c22e1a09f20eca32cb21056ae45334f0d55ce14b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117812"
---
# <span data-ttu-id="159b2-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="159b2-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="159b2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="159b2-102">SYNOPSIS</span></span>
<span data-ttu-id="159b2-103">Define as propriedades do sistema operacional para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="159b2-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="159b2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="159b2-104">SYNTAX</span></span>

### <span data-ttu-id="159b2-105">Windows (Padrão)</span><span class="sxs-lookup"><span data-stu-id="159b2-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="159b2-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="159b2-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="159b2-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="159b2-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="159b2-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="159b2-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="159b2-109">Linux</span><span class="sxs-lookup"><span data-stu-id="159b2-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="159b2-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="159b2-110">DESCRIPTION</span></span>
<span data-ttu-id="159b2-111">O **cmdlet Set-AzVMOperatingSystem** define propriedades do sistema operacional para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="159b2-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="159b2-112">Você pode especificar credenciais de logon, nome do computador e tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="159b2-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="159b2-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="159b2-113">EXAMPLES</span></span>

### <span data-ttu-id="159b2-114">Exemplo 1: Definir propriedades do sistema operacional para novas máquinas virtuais</span><span class="sxs-lookup"><span data-stu-id="159b2-114">Example 1: Set operating system properties for a new virtual machines</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="159b2-115">O primeiro comando converte uma senha em uma cadeia de caracteres segura e a armazena na variável $SecurePassword dados.</span><span class="sxs-lookup"><span data-stu-id="159b2-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="159b2-116">Para obter mais informações, digite `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="159b2-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="159b2-117">O segundo comando cria uma credencial para o usuário– TimeP e a senha armazenada no $SecurePassword e armazena a credencial na variável $Credential usuário.</span><span class="sxs-lookup"><span data-stu-id="159b2-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="159b2-118">Para obter mais informações, digite `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="159b2-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="159b2-119">O terceiro comando obtém o conjunto de disponibilidade chamado AvailabilitySet03 no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="159b2-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="159b2-120">O quarto comando cria um objeto virtual de máquina e, em seguida, o armazena na variável $VirtualMachine dados.</span><span class="sxs-lookup"><span data-stu-id="159b2-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="159b2-121">O comando atribui um nome e um tamanho à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="159b2-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="159b2-122">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="159b2-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="159b2-123">Os quatro comandos a seguir atribuem valores a variáveis a ser usadas no comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="159b2-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="159b2-124">Como você pode especificar essas cadeias de caracteres diretamente no comando **Set-AzVMOperatingSystem,** essa abordagem é usada somente para acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="159b2-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="159b2-125">No entanto, você pode usar uma abordagem como esta em scripts.</span><span class="sxs-lookup"><span data-stu-id="159b2-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="159b2-126">O comando final define as propriedades do sistema operacional para a máquina virtual armazenada no $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="159b2-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="159b2-127">O comando usa as credenciais armazenadas $Credential.</span><span class="sxs-lookup"><span data-stu-id="159b2-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="159b2-128">O comando usa variáveis atribuídas em comandos anteriores para alguns parâmetros.</span><span class="sxs-lookup"><span data-stu-id="159b2-128">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="159b2-129">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="159b2-129">PARAMETERS</span></span>

### <span data-ttu-id="159b2-130">-NomedoCompr computador</span><span class="sxs-lookup"><span data-stu-id="159b2-130">-ComputerName</span></span>
<span data-ttu-id="159b2-131">Especifica o nome do computador.</span><span class="sxs-lookup"><span data-stu-id="159b2-131">Specifies the name of the computer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159b2-132">-Credencial</span><span class="sxs-lookup"><span data-stu-id="159b2-132">-Credential</span></span>
<span data-ttu-id="159b2-133">Especifica o nome de usuário e a senha da máquina virtual como um **objeto PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="159b2-133">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="159b2-134">Para obter uma credencial, use o Get-Credential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="159b2-134">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="159b2-135">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="159b2-135">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159b2-136">-CustomData</span><span class="sxs-lookup"><span data-stu-id="159b2-136">-CustomData</span></span>
<span data-ttu-id="159b2-137">Especifica uma cadeia de caracteres codificada de base 64 de dados personalizados.</span><span class="sxs-lookup"><span data-stu-id="159b2-137">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="159b2-138">Isso é decodificado para uma matriz binária que é salva como um arquivo na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="159b2-138">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="159b2-139">O comprimento máximo da matriz binária é de 65535 bytes.</span><span class="sxs-lookup"><span data-stu-id="159b2-139">The maximum length of the binary array is 65535 bytes.</span></span><br>
<span data-ttu-id="159b2-140">**Observação: não passe segredos ou senhas na propriedade CustomData**</span><span class="sxs-lookup"><span data-stu-id="159b2-140">**Note: Do not pass any secrets or passwords in customData property**</span></span><br>
<span data-ttu-id="159b2-141">Essa propriedade não pode ser atualizada depois que o VM é criado.</span><span class="sxs-lookup"><span data-stu-id="159b2-141">This property cannot be updated after the VM is created.</span></span> <br>
<span data-ttu-id="159b2-142">customData is passed to the VM to be saved as a file, for more information see [Custom Data on Azure VMs](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/)</span><span class="sxs-lookup"><span data-stu-id="159b2-142">customData is passed to the VM to be saved as a file, for more information see [Custom Data on Azure VMs](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/)</span></span> <br>
<span data-ttu-id="159b2-143">Para usar o cloud-init para seu VM do Linux, consulte [Usando o cloud-init para personalizar](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init) um VM do Linux durante a criação</span><span class="sxs-lookup"><span data-stu-id="159b2-143">For using cloud-init for your Linux VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159b2-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="159b2-144">-DefaultProfile</span></span>
<span data-ttu-id="159b2-145">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="159b2-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="159b2-146">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="159b2-146">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="159b2-147">Indica que esse cmdlet desabilita a autenticação de senha.</span><span class="sxs-lookup"><span data-stu-id="159b2-147">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159b2-148">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="159b2-148">-DisableVMAgent</span></span>
<span data-ttu-id="159b2-149">Desabilitar o Provision VM Agent.</span><span class="sxs-lookup"><span data-stu-id="159b2-149">Disable Provision VM Agent.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="159b2-150">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="159b2-150">-EnableAutoUpdate</span></span>
<span data-ttu-id="159b2-151">Indica que esse cmdlet habilita a atualização automática.</span><span class="sxs-lookup"><span data-stu-id="159b2-151">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159b2-152">-Linux</span><span class="sxs-lookup"><span data-stu-id="159b2-152">-Linux</span></span>
<span data-ttu-id="159b2-153">Indica que o tipo de sistema operacional é o Linux.</span><span class="sxs-lookup"><span data-stu-id="159b2-153">Indicates that the type of operating system is Linux.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159b2-154">-PatchMode</span><span class="sxs-lookup"><span data-stu-id="159b2-154">-PatchMode</span></span>
<span data-ttu-id="159b2-155">Especifica o modo de patch in-guest para a máquina virtual IaaS.</span><span class="sxs-lookup"><span data-stu-id="159b2-155">Specifies the mode of in-guest patching to IaaS virtual machine.</span></span><br><br>
<span data-ttu-id="159b2-156">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="159b2-156">Possible values are:</span></span><br>
<span data-ttu-id="159b2-157">**Manual** – Você controla a aplicação de patches em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="159b2-157">**Manual** - You  control the application of patches to a virtual machine.</span></span> <span data-ttu-id="159b2-158">Faça isso aplicando patches manualmente dentro do VM.</span><span class="sxs-lookup"><span data-stu-id="159b2-158">You do this by applying patches manually inside the VM.</span></span> <span data-ttu-id="159b2-159">Nesse modo, as atualizações automáticas são desabilitadas; a propriedade WindowsConfiguration.enableAutomaticUpdates deve ser falsa</span><span class="sxs-lookup"><span data-stu-id="159b2-159">In this mode, automatic updates are disabled; the property WindowsConfiguration.enableAutomaticUpdates must be false</span></span><br>
<span data-ttu-id="159b2-160">**AutomaticByOS** : a máquina virtual será atualizada automaticamente pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="159b2-160">**AutomaticByOS** - The virtual machine will automatically be updated by the OS.</span></span> <span data-ttu-id="159b2-161">A propriedade WindowsConfiguration.enableAutomaticUpdates deve ser verdadeira.</span><span class="sxs-lookup"><span data-stu-id="159b2-161">The property WindowsConfiguration.enableAutomaticUpdates must be true.</span></span> <br >
<span data-ttu-id="159b2-162">**AutomaticByPlatform:** a máquina virtual será atualizada automaticamente pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="159b2-162">**AutomaticByPlatform** - the virtual machine will automatically updated by the OS.</span></span> <span data-ttu-id="159b2-163">As propriedades provisionVMAgent e WindowsConfiguration.enableAutomaticUpdates devem ser verdadeiras</span><span class="sxs-lookup"><span data-stu-id="159b2-163">The properties provisionVMAgent and WindowsConfiguration.enableAutomaticUpdates must be true</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159b2-164">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="159b2-164">-ProvisionVMAgent</span></span>
<span data-ttu-id="159b2-165">Indica que as configurações exigem que o agente de máquina virtual seja instalado na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="159b2-165">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159b2-166">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="159b2-166">-TimeZone</span></span>
<span data-ttu-id="159b2-167">Especifica o fuso horário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="159b2-167">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="159b2-168">por exemplo, Hora \" Padrão do \" Pacífico.</span><span class="sxs-lookup"><span data-stu-id="159b2-168">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="159b2-169">Os valores possíveis podem [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) de fusos horário retornados pelo [TimeZoneInfo.GetSystemTimeZones.](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)</span><span class="sxs-lookup"><span data-stu-id="159b2-169">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159b2-170">-VM</span><span class="sxs-lookup"><span data-stu-id="159b2-170">-VM</span></span>
<span data-ttu-id="159b2-171">Especifica o objeto de máquina virtual local no qual definir as propriedades do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="159b2-171">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="159b2-172">Para obter um objeto virtual de máquina, use o cmdlet Get-AzVM computador.</span><span class="sxs-lookup"><span data-stu-id="159b2-172">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="159b2-173">Crie um objeto virtual usando o cmdlet New-AzVMConfig computador.</span><span class="sxs-lookup"><span data-stu-id="159b2-173">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="159b2-174">-Windows</span><span class="sxs-lookup"><span data-stu-id="159b2-174">-Windows</span></span>
<span data-ttu-id="159b2-175">Indica que o tipo de sistema operacional é o Windows.</span><span class="sxs-lookup"><span data-stu-id="159b2-175">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159b2-176">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="159b2-176">-WinRMCertificateUrl</span></span>
<span data-ttu-id="159b2-177">Especifica o URI de um certificado WinRM.</span><span class="sxs-lookup"><span data-stu-id="159b2-177">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="159b2-178">Isso precisa ser armazenado em um Cofre de Teclas.</span><span class="sxs-lookup"><span data-stu-id="159b2-178">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159b2-179">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="159b2-179">-WinRMHttp</span></span>
<span data-ttu-id="159b2-180">Indica que esse sistema operacional usa HTTP WinRM.</span><span class="sxs-lookup"><span data-stu-id="159b2-180">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159b2-181">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="159b2-181">-WinRMHttps</span></span>
<span data-ttu-id="159b2-182">Indica que esse sistema operacional usa HTTPS WinRM.</span><span class="sxs-lookup"><span data-stu-id="159b2-182">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159b2-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="159b2-183">CommonParameters</span></span>
<span data-ttu-id="159b2-184">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="159b2-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="159b2-185">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="159b2-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="159b2-186">Entradas</span><span class="sxs-lookup"><span data-stu-id="159b2-186">INPUTS</span></span>

### <span data-ttu-id="159b2-187">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="159b2-187">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="159b2-188">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="159b2-188">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="159b2-189">System.String</span><span class="sxs-lookup"><span data-stu-id="159b2-189">System.String</span></span>

### <span data-ttu-id="159b2-190">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="159b2-190">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="159b2-191">System.Uri</span><span class="sxs-lookup"><span data-stu-id="159b2-191">System.Uri</span></span>

## <span data-ttu-id="159b2-192">Saídas</span><span class="sxs-lookup"><span data-stu-id="159b2-192">OUTPUTS</span></span>

### <span data-ttu-id="159b2-193">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="159b2-193">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="159b2-194">Notas</span><span class="sxs-lookup"><span data-stu-id="159b2-194">NOTES</span></span>

## <span data-ttu-id="159b2-195">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="159b2-195">RELATED LINKS</span></span>

[<span data-ttu-id="159b2-196">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="159b2-196">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="159b2-197">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="159b2-197">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


