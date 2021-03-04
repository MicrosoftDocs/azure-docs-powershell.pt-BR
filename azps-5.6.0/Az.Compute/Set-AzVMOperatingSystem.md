---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 75eb0ef60443cdbf2dfe3fa53202d3c8141d4888
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890300"
---
# <span data-ttu-id="bd733-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="bd733-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="bd733-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd733-102">SYNOPSIS</span></span>
<span data-ttu-id="bd733-103">Define as propriedades do sistema operacional para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bd733-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="bd733-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bd733-104">SYNTAX</span></span>

### <span data-ttu-id="bd733-105">Windows (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bd733-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd733-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="bd733-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd733-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="bd733-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd733-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="bd733-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd733-109">Linux</span><span class="sxs-lookup"><span data-stu-id="bd733-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-PatchMode <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd733-110">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bd733-110">DESCRIPTION</span></span>
<span data-ttu-id="bd733-111">O cmdlet **Set-AzVMOperatingSystem** define propriedades do sistema operacional para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bd733-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="bd733-112">Você pode especificar credenciais de logon, nome do computador e tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="bd733-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="bd733-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bd733-113">EXAMPLES</span></span>

### <span data-ttu-id="bd733-114">Exemplo 1: Definir propriedades do sistema operacional para uma nova máquina virtual</span><span class="sxs-lookup"><span data-stu-id="bd733-114">Example 1: Set operating system properties for a new virtual machine</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="bd733-115">O primeiro comando converte uma senha em uma cadeia de caracteres segura e a armazena na variável $SecurePassword segurança.</span><span class="sxs-lookup"><span data-stu-id="bd733-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="bd733-116">Para obter mais informações, digite `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="bd733-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="bd733-117">O segundo comando cria uma credencial para o usuário FullerP e a senha armazenada no $SecurePassword e armazena a credencial na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="bd733-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="bd733-118">Para obter mais informações, digite `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="bd733-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="bd733-119">O terceiro comando obtém o conjunto de disponibilidade chamado AvailabilitySet03 no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="bd733-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="bd733-120">O quarto comando cria um objeto de máquina virtual e o armazena na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="bd733-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="bd733-121">O comando atribui um nome e tamanho à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bd733-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="bd733-122">A máquina virtual pertence ao conjunto de disponibilidade armazenado $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="bd733-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="bd733-123">Os quatro comandos a seguir atribuem valores a variáveis a ser usadas no comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="bd733-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="bd733-124">Como você pode especificar essas cadeias de caracteres diretamente no comando **Set-AzVMOperatingSystem,** essa abordagem é usada apenas para leitura.</span><span class="sxs-lookup"><span data-stu-id="bd733-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="bd733-125">No entanto, você pode usar uma abordagem como esta em scripts.</span><span class="sxs-lookup"><span data-stu-id="bd733-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="bd733-126">O comando final define as propriedades do sistema operacional para a máquina virtual armazenada $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="bd733-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="bd733-127">O comando usa as credenciais armazenadas em $Credential.</span><span class="sxs-lookup"><span data-stu-id="bd733-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="bd733-128">O comando usa variáveis atribuídas em comandos anteriores para alguns parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bd733-128">The command uses variables assigned in previous commands for some parameters.</span></span>

### <span data-ttu-id="bd733-129">Exemplo 2: Definir propriedades do sistema operacional para uma nova máquina virtual com patch de hot patch habilitado</span><span class="sxs-lookup"><span data-stu-id="bd733-129">Example 2: Set operating system properties for a new virtual machine with hot patching enabled</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform" -EnableHotPatching
```

<span data-ttu-id="bd733-130">O primeiro comando converte uma senha em uma cadeia de caracteres segura e a armazena na variável $SecurePassword segurança.</span><span class="sxs-lookup"><span data-stu-id="bd733-130">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="bd733-131">Para obter mais informações, digite `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="bd733-131">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="bd733-132">O segundo comando cria uma credencial para o usuário FullerP e a senha armazenada no $SecurePassword e armazena a credencial na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="bd733-132">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="bd733-133">Para obter mais informações, digite `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="bd733-133">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="bd733-134">O terceiro comando obtém o conjunto de disponibilidade chamado AvailabilitySet03 no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="bd733-134">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="bd733-135">O quarto comando cria um objeto de máquina virtual e o armazena na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="bd733-135">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="bd733-136">O comando atribui um nome e tamanho à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bd733-136">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="bd733-137">A máquina virtual pertence ao conjunto de disponibilidade armazenado $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="bd733-137">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="bd733-138">Os quatro comandos a seguir atribuem valores a variáveis a ser usadas no comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="bd733-138">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="bd733-139">Como você pode especificar essas cadeias de caracteres diretamente no comando **Set-AzVMOperatingSystem,** essa abordagem é usada apenas para leitura.</span><span class="sxs-lookup"><span data-stu-id="bd733-139">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="bd733-140">No entanto, você pode usar uma abordagem como esta em scripts.</span><span class="sxs-lookup"><span data-stu-id="bd733-140">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="bd733-141">O comando final define as propriedades do sistema operacional para a máquina virtual armazenada $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="bd733-141">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="bd733-142">O comando usa as credenciais armazenadas em $Credential.</span><span class="sxs-lookup"><span data-stu-id="bd733-142">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="bd733-143">O comando usa variáveis atribuídas em comandos anteriores para alguns parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bd733-143">The command uses variables assigned in previous commands for some parameters.</span></span>
<span data-ttu-id="bd733-144">O comando habilita o Hotpatching na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bd733-144">The command enables Hotpatching on the virtual machine.</span></span>

### <span data-ttu-id="bd733-145">Exemplo 3: Definir propriedades do sistema operacional para uma nova máquina virtual Linux</span><span class="sxs-lookup"><span data-stu-id="bd733-145">Example 3: Set operating system properties for a new Linux virtual machine</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="bd733-146">O primeiro comando converte uma senha em uma cadeia de caracteres segura e a armazena na variável $SecurePassword segurança.</span><span class="sxs-lookup"><span data-stu-id="bd733-146">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="bd733-147">Para obter mais informações, digite `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="bd733-147">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="bd733-148">O segundo comando cria uma credencial para o usuário FullerP e a senha armazenada no $SecurePassword e armazena a credencial na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="bd733-148">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="bd733-149">Para obter mais informações, digite `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="bd733-149">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="bd733-150">O terceiro comando obtém o conjunto de disponibilidade chamado AvailabilitySet03 no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="bd733-150">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="bd733-151">O quarto comando cria um objeto de máquina virtual e o armazena na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="bd733-151">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="bd733-152">O comando atribui um nome e tamanho à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bd733-152">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="bd733-153">A máquina virtual pertence ao conjunto de disponibilidade armazenado $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="bd733-153">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="bd733-154">Os dois comandos a seguir atribuem valores a variáveis a ser usadas no comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="bd733-154">The next two commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="bd733-155">O comando final define as propriedades do sistema operacional para a máquina virtual armazenada $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="bd733-155">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="bd733-156">O comando usa as credenciais armazenadas em $Credential.</span><span class="sxs-lookup"><span data-stu-id="bd733-156">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="bd733-157">O comando usa variáveis atribuídas em comandos anteriores para alguns parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bd733-157">The command uses variables assigned in previous commands for some parameters.</span></span>
<span data-ttu-id="bd733-158">O comando define o valor do modo de patch na máquina virtual como "AutomaticByPlatform".</span><span class="sxs-lookup"><span data-stu-id="bd733-158">The command sets the patch mode value on the virtual machine to "AutomaticByPlatform".</span></span>

## <span data-ttu-id="bd733-159">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bd733-159">PARAMETERS</span></span>

### <span data-ttu-id="bd733-160">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="bd733-160">-ComputerName</span></span>
<span data-ttu-id="bd733-161">Especifica o nome do computador.</span><span class="sxs-lookup"><span data-stu-id="bd733-161">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="bd733-162">-Credential</span><span class="sxs-lookup"><span data-stu-id="bd733-162">-Credential</span></span>
<span data-ttu-id="bd733-163">Especifica o nome de usuário e a senha da máquina virtual como um **objeto PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="bd733-163">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="bd733-164">Para obter uma credencial, use Get-Credential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd733-164">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="bd733-165">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="bd733-165">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="bd733-166">-CustomData</span><span class="sxs-lookup"><span data-stu-id="bd733-166">-CustomData</span></span>
<span data-ttu-id="bd733-167">Especifica uma cadeia de caracteres a ser passada para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bd733-167">Specifies a string to be passed to the virtual machine.</span></span> <span data-ttu-id="bd733-168">Para obter mais informações, [consulte Dados Personalizados em VMs do Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/custom-data).</span><span class="sxs-lookup"><span data-stu-id="bd733-168">For more information see [Custom Data on Azure VMs](https://docs.microsoft.com/en-us/azure/virtual-machines/custom-data).</span></span>
<span data-ttu-id="bd733-169">**Observação: não é recomendável armazenar informações confidenciais em dados personalizados.**</span><span class="sxs-lookup"><span data-stu-id="bd733-169">**Note: It is not recommended to store sensitive information in custom data.**</span></span>


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

### <span data-ttu-id="bd733-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd733-170">-DefaultProfile</span></span>
<span data-ttu-id="bd733-171">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="bd733-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd733-172">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="bd733-172">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="bd733-173">Indica que esse cmdlet desabilita a autenticação de senha.</span><span class="sxs-lookup"><span data-stu-id="bd733-173">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="bd733-174">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="bd733-174">-DisableVMAgent</span></span>
<span data-ttu-id="bd733-175">Desabilitar o Agente de VM de Provisionamento.</span><span class="sxs-lookup"><span data-stu-id="bd733-175">Disable Provision VM Agent.</span></span>

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

### <span data-ttu-id="bd733-176">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="bd733-176">-EnableAutoUpdate</span></span>
<span data-ttu-id="bd733-177">Indica que esse cmdlet habilita a atualização automática.</span><span class="sxs-lookup"><span data-stu-id="bd733-177">Indicates that this cmdlet enables auto update.</span></span>

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

### <span data-ttu-id="bd733-178">-EnableHotpatching</span><span class="sxs-lookup"><span data-stu-id="bd733-178">-EnableHotpatching</span></span>
<span data-ttu-id="bd733-179">Permite que os clientes patch suas VMs do Azure sem exigir uma reinicialização.</span><span class="sxs-lookup"><span data-stu-id="bd733-179">Enables customers to patch their Azure VMs without requiring a reboot.</span></span> <span data-ttu-id="bd733-180">Para enableHotpatching, o 'provisionVMAgent' deve ser definido como true e 'patchMode' deve ser definido como 'AutomaticByPlatform'.</span><span class="sxs-lookup"><span data-stu-id="bd733-180">For enableHotpatching, the 'provisionVMAgent' must be set to true and 'patchMode' must be set to 'AutomaticByPlatform'.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd733-181">-Linux</span><span class="sxs-lookup"><span data-stu-id="bd733-181">-Linux</span></span>
<span data-ttu-id="bd733-182">Indica que o tipo de sistema operacional é Linux.</span><span class="sxs-lookup"><span data-stu-id="bd733-182">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="bd733-183">-PatchMode</span><span class="sxs-lookup"><span data-stu-id="bd733-183">-PatchMode</span></span>
<span data-ttu-id="bd733-184">Especifica o modo de patch no convidado para a máquina virtual IaaS.</span><span class="sxs-lookup"><span data-stu-id="bd733-184">Specifies the mode of in-guest patching to IaaS virtual machine.</span></span><br><br>
<span data-ttu-id="bd733-185">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="bd733-185">Possible values are:</span></span><br>
<span data-ttu-id="bd733-186">**Manual** - Você controla a aplicação de patches em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bd733-186">**Manual** - You  control the application of patches to a virtual machine.</span></span> <span data-ttu-id="bd733-187">Faça isso aplicando patches manualmente dentro da VM.</span><span class="sxs-lookup"><span data-stu-id="bd733-187">You do this by applying patches manually inside the VM.</span></span> <span data-ttu-id="bd733-188">Nesse modo, as atualizações automáticas são desabilitadas; a propriedade WindowsConfiguration.enableAutomaticUpdates deve ser false</span><span class="sxs-lookup"><span data-stu-id="bd733-188">In this mode, automatic updates are disabled; the property WindowsConfiguration.enableAutomaticUpdates must be false</span></span><br>
<span data-ttu-id="bd733-189">**AutomaticByOS** - A máquina virtual será atualizada automaticamente pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="bd733-189">**AutomaticByOS** - The virtual machine will automatically be updated by the OS.</span></span> <span data-ttu-id="bd733-190">A propriedade WindowsConfiguration.enableAutomaticUpdates deve ser true.</span><span class="sxs-lookup"><span data-stu-id="bd733-190">The property WindowsConfiguration.enableAutomaticUpdates must be true.</span></span> <br >
<span data-ttu-id="bd733-191">**AutomaticByPlatform** - a máquina virtual será atualizada automaticamente pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="bd733-191">**AutomaticByPlatform** - the virtual machine will automatically updated by the OS.</span></span> <span data-ttu-id="bd733-192">As propriedades provisionVMAgent e WindowsConfiguration.enableAutomaticUpdates devem ser verdadeiras</span><span class="sxs-lookup"><span data-stu-id="bd733-192">The properties provisionVMAgent and WindowsConfiguration.enableAutomaticUpdates must be true</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd733-193">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="bd733-193">-ProvisionVMAgent</span></span>
<span data-ttu-id="bd733-194">Indica que as configurações exigem que o agente da máquina virtual seja instalado na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bd733-194">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="bd733-195">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="bd733-195">-TimeZone</span></span>
<span data-ttu-id="bd733-196">Especifica o fuso horário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bd733-196">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="bd733-197">Por exemplo, Hora \" Padrão do Pacífico \" .</span><span class="sxs-lookup"><span data-stu-id="bd733-197">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="bd733-198">Os valores possíveis podem [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) de fusos horário retornados por [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones).</span><span class="sxs-lookup"><span data-stu-id="bd733-198">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="bd733-199">-VM</span><span class="sxs-lookup"><span data-stu-id="bd733-199">-VM</span></span>
<span data-ttu-id="bd733-200">Especifica o objeto da máquina virtual local no qual definir as propriedades do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="bd733-200">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="bd733-201">Para obter um objeto de máquina virtual, use Get-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd733-201">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="bd733-202">Crie um objeto de máquina virtual usando o New-AzVMConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd733-202">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="bd733-203">-Windows</span><span class="sxs-lookup"><span data-stu-id="bd733-203">-Windows</span></span>
<span data-ttu-id="bd733-204">Indica que o tipo de sistema operacional é o Windows.</span><span class="sxs-lookup"><span data-stu-id="bd733-204">Indicates that the type of operating system is Windows.</span></span>

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

### <span data-ttu-id="bd733-205">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="bd733-205">-WinRMCertificateUrl</span></span>
<span data-ttu-id="bd733-206">Especifica o URI de um certificado WinRM.</span><span class="sxs-lookup"><span data-stu-id="bd733-206">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="bd733-207">Isso precisa ser armazenado em um Cofre de Chaves.</span><span class="sxs-lookup"><span data-stu-id="bd733-207">This needs to be stored in a Key Vault.</span></span>

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

### <span data-ttu-id="bd733-208">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="bd733-208">-WinRMHttp</span></span>
<span data-ttu-id="bd733-209">Indica que esse sistema operacional usa HTTP WinRM.</span><span class="sxs-lookup"><span data-stu-id="bd733-209">Indicates that this operating system uses HTTP WinRM.</span></span>

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

### <span data-ttu-id="bd733-210">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="bd733-210">-WinRMHttps</span></span>
<span data-ttu-id="bd733-211">Indica que esse sistema operacional usa HTTPS WinRM.</span><span class="sxs-lookup"><span data-stu-id="bd733-211">Indicates that this operating system uses HTTPS WinRM.</span></span>

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

### <span data-ttu-id="bd733-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd733-212">CommonParameters</span></span>
<span data-ttu-id="bd733-213">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd733-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd733-214">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd733-214">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd733-215">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd733-215">INPUTS</span></span>

### <span data-ttu-id="bd733-216">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="bd733-216">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="bd733-217">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bd733-217">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="bd733-218">System.String</span><span class="sxs-lookup"><span data-stu-id="bd733-218">System.String</span></span>

### <span data-ttu-id="bd733-219">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="bd733-219">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="bd733-220">System.Uri</span><span class="sxs-lookup"><span data-stu-id="bd733-220">System.Uri</span></span>

## <span data-ttu-id="bd733-221">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bd733-221">OUTPUTS</span></span>

### <span data-ttu-id="bd733-222">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="bd733-222">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="bd733-223">NOTES</span><span class="sxs-lookup"><span data-stu-id="bd733-223">NOTES</span></span>

## <span data-ttu-id="bd733-224">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd733-224">RELATED LINKS</span></span>

[<span data-ttu-id="bd733-225">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="bd733-225">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="bd733-226">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="bd733-226">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


