---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 01d1b07ec861b5eeb02d4590001e304936bde395
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944624"
---
# <span data-ttu-id="98fb3-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="98fb3-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="98fb3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98fb3-102">SYNOPSIS</span></span>
<span data-ttu-id="98fb3-103">Define as propriedades do sistema operacional para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="98fb3-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="98fb3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98fb3-104">SYNTAX</span></span>

### <span data-ttu-id="98fb3-105">Windows (padrão)</span><span class="sxs-lookup"><span data-stu-id="98fb3-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98fb3-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="98fb3-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98fb3-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="98fb3-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98fb3-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="98fb3-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98fb3-109">Linux</span><span class="sxs-lookup"><span data-stu-id="98fb3-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98fb3-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="98fb3-110">DESCRIPTION</span></span>
<span data-ttu-id="98fb3-111">O cmdlet **set-AzVMOperatingSystem** define as propriedades do sistema operacional para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="98fb3-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="98fb3-112">Você pode especificar as credenciais de logon, o nome do computador e o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="98fb3-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="98fb3-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98fb3-113">EXAMPLES</span></span>

### <span data-ttu-id="98fb3-114">Exemplo 1: definir propriedades do sistema operacional para uma nova máquina virtual</span><span class="sxs-lookup"><span data-stu-id="98fb3-114">Example 1: Set operating system properties for a new virtual machines</span></span>
```
PS C:\> $SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $ComputerName = "ContosoVM122"
PS C:\> $WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
PS C:\> $TimeZone = "Pacific Standard Time"
PS C:\> $CustomData = "echo 'Hello World'"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone
```

<span data-ttu-id="98fb3-115">O primeiro comando converte uma senha em uma cadeia de caracteres segura e, em seguida, armazena-a na variável $SecurePassword.</span><span class="sxs-lookup"><span data-stu-id="98fb3-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="98fb3-116">Para obter mais informações, digite `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="98fb3-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="98fb3-117">O segundo comando cria uma credencial para o usuário FullerP e a senha armazenada no $SecurePassword e, em seguida, armazena a credencial na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="98fb3-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="98fb3-118">Para obter mais informações, digite `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="98fb3-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="98fb3-119">O terceiro comando obtém o conjunto de disponibilidade chamado AvailabilitySet03 no grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="98fb3-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="98fb3-120">O quarto comando cria um objeto de máquina virtual e, em seguida, armazena-o na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="98fb3-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="98fb3-121">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="98fb3-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="98fb3-122">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="98fb3-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="98fb3-123">Os próximos quatro comandos atribuem valores a variáveis a serem usadas no comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="98fb3-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="98fb3-124">Como você pode especificar essas cadeias de caracteres diretamente no comando **set-AzVMOperatingSystem** , essa abordagem é usada somente para fins de legibilidade.</span><span class="sxs-lookup"><span data-stu-id="98fb3-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="98fb3-125">No entanto, você pode usar uma abordagem como esta em scripts.</span><span class="sxs-lookup"><span data-stu-id="98fb3-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="98fb3-126">O comando final define as propriedades do sistema operacional da máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="98fb3-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="98fb3-127">O comando usa as credenciais armazenadas em $Credential.</span><span class="sxs-lookup"><span data-stu-id="98fb3-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="98fb3-128">O comando usa variáveis atribuídas nos comandos anteriores para alguns parâmetros.</span><span class="sxs-lookup"><span data-stu-id="98fb3-128">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="98fb3-129">OS</span><span class="sxs-lookup"><span data-stu-id="98fb3-129">PARAMETERS</span></span>

### <span data-ttu-id="98fb3-130">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="98fb3-130">-ComputerName</span></span>
<span data-ttu-id="98fb3-131">Especifica o nome do computador.</span><span class="sxs-lookup"><span data-stu-id="98fb3-131">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="98fb3-132">-Credential</span><span class="sxs-lookup"><span data-stu-id="98fb3-132">-Credential</span></span>
<span data-ttu-id="98fb3-133">Especifica o nome de usuário e a senha da máquina virtual como um objeto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="98fb3-133">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="98fb3-134">Para obter uma credencial, use o cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="98fb3-134">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="98fb3-135">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="98fb3-135">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="98fb3-136">-CustomData</span><span class="sxs-lookup"><span data-stu-id="98fb3-136">-CustomData</span></span>
<span data-ttu-id="98fb3-137">Especifica uma cadeia de caracteres de dados personalizados codificada como base-64.</span><span class="sxs-lookup"><span data-stu-id="98fb3-137">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="98fb3-138">Isso é decodificado para uma matriz binária salva como um arquivo na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="98fb3-138">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="98fb3-139">O comprimento máximo da matriz binária é de 65535 bytes.</span><span class="sxs-lookup"><span data-stu-id="98fb3-139">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="98fb3-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98fb3-140">-DefaultProfile</span></span>
<span data-ttu-id="98fb3-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98fb3-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98fb3-142">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="98fb3-142">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="98fb3-143">Indica que esse cmdlet desabilita a autenticação de senha.</span><span class="sxs-lookup"><span data-stu-id="98fb3-143">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="98fb3-144">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="98fb3-144">-DisableVMAgent</span></span>
<span data-ttu-id="98fb3-145">Desabilitar o agente de VM de provisionamento.</span><span class="sxs-lookup"><span data-stu-id="98fb3-145">Disable Provision VM Agent.</span></span>

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

### <span data-ttu-id="98fb3-146">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="98fb3-146">-EnableAutoUpdate</span></span>
<span data-ttu-id="98fb3-147">Indica que esse cmdlet habilita a atualização automática.</span><span class="sxs-lookup"><span data-stu-id="98fb3-147">Indicates that this cmdlet enables auto update.</span></span>

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

### <span data-ttu-id="98fb3-148">-Linux</span><span class="sxs-lookup"><span data-stu-id="98fb3-148">-Linux</span></span>
<span data-ttu-id="98fb3-149">Indica que o tipo de sistema operacional é o Linux.</span><span class="sxs-lookup"><span data-stu-id="98fb3-149">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="98fb3-150">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="98fb3-150">-ProvisionVMAgent</span></span>
<span data-ttu-id="98fb3-151">Indica que as configurações exigem que o agente da máquina virtual seja instalado na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="98fb3-151">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="98fb3-152">-Fuso horário</span><span class="sxs-lookup"><span data-stu-id="98fb3-152">-TimeZone</span></span>
<span data-ttu-id="98fb3-153">Especifica o fuso horário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="98fb3-153">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="98fb3-154">-VM</span><span class="sxs-lookup"><span data-stu-id="98fb3-154">-VM</span></span>
<span data-ttu-id="98fb3-155">Especifica o objeto da máquina virtual local no qual definir propriedades do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="98fb3-155">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="98fb3-156">Para obter um objeto de máquina virtual, use o cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="98fb3-156">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="98fb3-157">Crie um objeto de máquina virtual usando o cmdlet New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="98fb3-157">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="98fb3-158">-Windows</span><span class="sxs-lookup"><span data-stu-id="98fb3-158">-Windows</span></span>
<span data-ttu-id="98fb3-159">Indica que o tipo de sistema operacional é Windows.</span><span class="sxs-lookup"><span data-stu-id="98fb3-159">Indicates that the type of operating system is Windows.</span></span>

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

### <span data-ttu-id="98fb3-160">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="98fb3-160">-WinRMCertificateUrl</span></span>
<span data-ttu-id="98fb3-161">Especifica o URI de um certificado WinRM.</span><span class="sxs-lookup"><span data-stu-id="98fb3-161">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="98fb3-162">Isso precisa ser armazenado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="98fb3-162">This needs to be stored in a Key Vault.</span></span>

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

### <span data-ttu-id="98fb3-163">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="98fb3-163">-WinRMHttp</span></span>
<span data-ttu-id="98fb3-164">Indica que esse sistema operacional usa o WinRM HTTP.</span><span class="sxs-lookup"><span data-stu-id="98fb3-164">Indicates that this operating system uses HTTP WinRM.</span></span>

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

### <span data-ttu-id="98fb3-165">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="98fb3-165">-WinRMHttps</span></span>
<span data-ttu-id="98fb3-166">Indica que esse sistema operacional usa WinRM HTTPS.</span><span class="sxs-lookup"><span data-stu-id="98fb3-166">Indicates that this operating system uses HTTPS WinRM.</span></span>

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

### <span data-ttu-id="98fb3-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98fb3-167">CommonParameters</span></span>
<span data-ttu-id="98fb3-168">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98fb3-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98fb3-169">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98fb3-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98fb3-170">SENSORES</span><span class="sxs-lookup"><span data-stu-id="98fb3-170">INPUTS</span></span>

### <span data-ttu-id="98fb3-171">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="98fb3-171">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="98fb3-172">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="98fb3-172">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="98fb3-173">System. String</span><span class="sxs-lookup"><span data-stu-id="98fb3-173">System.String</span></span>

### <span data-ttu-id="98fb3-174">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="98fb3-174">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="98fb3-175">System. URI</span><span class="sxs-lookup"><span data-stu-id="98fb3-175">System.Uri</span></span>

## <span data-ttu-id="98fb3-176">EXIBE</span><span class="sxs-lookup"><span data-stu-id="98fb3-176">OUTPUTS</span></span>

### <span data-ttu-id="98fb3-177">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="98fb3-177">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="98fb3-178">INFORMA</span><span class="sxs-lookup"><span data-stu-id="98fb3-178">NOTES</span></span>

## <span data-ttu-id="98fb3-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98fb3-179">RELATED LINKS</span></span>

[<span data-ttu-id="98fb3-180">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="98fb3-180">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="98fb3-181">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="98fb3-181">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


