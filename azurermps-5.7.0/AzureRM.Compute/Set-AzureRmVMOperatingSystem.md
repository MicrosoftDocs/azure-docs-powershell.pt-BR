---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
ms.openlocfilehash: 01f9d007d54e7e96ac28e81b5081dc696d3af406
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431051"
---
# <span data-ttu-id="e8e8a-101">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="e8e8a-101">Set-AzureRmVMOperatingSystem</span></span>

## <span data-ttu-id="e8e8a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e8e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="e8e8a-103">Define as propriedades do sistema operacional para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-103">Sets operating system properties for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8e8a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8e8a-104">SYNTAX</span></span>

### <span data-ttu-id="e8e8a-105">Windows (padrão)</span><span class="sxs-lookup"><span data-stu-id="e8e8a-105">Windows (Default)</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [<CommonParameters>]
```

### <span data-ttu-id="e8e8a-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="e8e8a-106">WindowsWinRmHttps</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [<CommonParameters>]
```

### <span data-ttu-id="e8e8a-107">Linux</span><span class="sxs-lookup"><span data-stu-id="e8e8a-107">Linux</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisablePasswordAuthentication] [<CommonParameters>]
```

## <span data-ttu-id="e8e8a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e8e8a-108">DESCRIPTION</span></span>
<span data-ttu-id="e8e8a-109">O cmdlet **set-AzureRmVMOperatingSystem** define as propriedades do sistema operacional para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-109">The **Set-AzureRmVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="e8e8a-110">Você pode especificar as credenciais de logon, o nome do computador e o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-110">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="e8e8a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8e8a-111">EXAMPLES</span></span>

### <span data-ttu-id="e8e8a-112">Exemplo 1: definir propriedades do sistema operacional para uma nova máquina virtual</span><span class="sxs-lookup"><span data-stu-id="e8e8a-112">Example 1: Set operating system properties for a new virtual machines</span></span>
```
PS C:\> $SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $ComputerName = "ContosoVM122"
PS C:\> $WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
PS C:\> $TimeZone = "Pacific Standard Time"
PS C:\> $CustomData = "echo 'Hello World'"
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone
```

<span data-ttu-id="e8e8a-113">O primeiro comando converte uma senha em uma cadeia de caracteres segura e, em seguida, armazena-a na variável $SecurePassword.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-113">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="e8e8a-114">Para obter mais informações, digite `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="e8e8a-114">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>

<span data-ttu-id="e8e8a-115">O segundo comando cria uma credencial para o usuário FullerP e a senha armazenada no $SecurePassword e, em seguida, armazena a credencial na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-115">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="e8e8a-116">Para obter mais informações, digite `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="e8e8a-116">For more information, type `Get-Help New-Object`.</span></span>

<span data-ttu-id="e8e8a-117">O terceiro comando obtém o conjunto de disponibilidade chamado AvailablitySet03 no grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-117">The third command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="e8e8a-118">O quarto comando cria um objeto de máquina virtual e, em seguida, armazena-o na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-118">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e8e8a-119">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-119">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="e8e8a-120">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-120">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="e8e8a-121">Os próximos quatro comandos atribuem valores a variáveis a serem usadas no comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-121">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="e8e8a-122">Como você pode especificar essas cadeias de caracteres diretamente no comando **set-AzureRmVMOperatingSystem** , essa abordagem é usada somente para fins de legibilidade.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-122">Because you could specify these strings directly in the **Set-AzureRmVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="e8e8a-123">No entanto, você pode usar uma abordagem como esta em scripts.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-123">However, you might use an approach such as this in scripts.</span></span>

<span data-ttu-id="e8e8a-124">O comando final define as propriedades do sistema operacional da máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-124">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="e8e8a-125">O comando usa as credenciais armazenadas em $Credential.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-125">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="e8e8a-126">O comando usa variáveis atribuídas nos comandos anteriores para alguns parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-126">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="e8e8a-127">OS</span><span class="sxs-lookup"><span data-stu-id="e8e8a-127">PARAMETERS</span></span>

### <span data-ttu-id="e8e8a-128">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="e8e8a-128">-ComputerName</span></span>
<span data-ttu-id="e8e8a-129">Especifica o nome do computador.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-129">Specifies the name of the computer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e8a-130">-Credential</span><span class="sxs-lookup"><span data-stu-id="e8e8a-130">-Credential</span></span>
<span data-ttu-id="e8e8a-131">Especifica o nome de usuário e a senha da máquina virtual como um objeto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="e8e8a-131">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="e8e8a-132">Para obter uma credencial, use o cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-132">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="e8e8a-133">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="e8e8a-133">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e8a-134">-CustomData</span><span class="sxs-lookup"><span data-stu-id="e8e8a-134">-CustomData</span></span>
<span data-ttu-id="e8e8a-135">Especifica uma cadeia de caracteres de dados personalizados codificada como base-64.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-135">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="e8e8a-136">Isso é decodificado para uma matriz binária salva como um arquivo na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-136">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="e8e8a-137">O comprimento máximo da matriz binária é de 65535 bytes.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-137">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="e8e8a-138">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="e8e8a-138">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="e8e8a-139">Indica que esse cmdlet desabilita a autenticação de senha.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-139">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e8a-140">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="e8e8a-140">-EnableAutoUpdate</span></span>
<span data-ttu-id="e8e8a-141">Indica que esse cmdlet habilita a atualização automática.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-141">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e8a-142">-Linux</span><span class="sxs-lookup"><span data-stu-id="e8e8a-142">-Linux</span></span>
<span data-ttu-id="e8e8a-143">Indica que o tipo de sistema operacional é o Linux.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-143">Indicates that the type of operating system is Linux.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e8a-144">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="e8e8a-144">-ProvisionVMAgent</span></span>
<span data-ttu-id="e8e8a-145">Indica que as configurações exigem que o agente da máquina virtual seja instalado na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-145">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e8a-146">-Fuso horário</span><span class="sxs-lookup"><span data-stu-id="e8e8a-146">-TimeZone</span></span>
<span data-ttu-id="e8e8a-147">Especifica o fuso horário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-147">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e8a-148">-VM</span><span class="sxs-lookup"><span data-stu-id="e8e8a-148">-VM</span></span>
<span data-ttu-id="e8e8a-149">Especifica o objeto da máquina virtual local no qual definir propriedades do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-149">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="e8e8a-150">Para obter um objeto de máquina virtual, use o cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-150">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="e8e8a-151">Crie um objeto de máquina virtual usando o cmdlet New-AzureRmVMConfig.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-151">Create a virtual machine object by using the New-AzureRmVMConfig cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e8a-152">-Windows</span><span class="sxs-lookup"><span data-stu-id="e8e8a-152">-Windows</span></span>
<span data-ttu-id="e8e8a-153">Indica que o tipo de sistema operacional é Windows.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-153">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e8a-154">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="e8e8a-154">-WinRMCertificateUrl</span></span>
<span data-ttu-id="e8e8a-155">Especifica o URI de um certificado WinRM.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-155">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="e8e8a-156">Isso precisa ser armazenado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-156">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: Uri
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e8a-157">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="e8e8a-157">-WinRMHttp</span></span>
<span data-ttu-id="e8e8a-158">Indica que esse sistema operacional usa o WinRM HTTP.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-158">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e8a-159">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="e8e8a-159">-WinRMHttps</span></span>
<span data-ttu-id="e8e8a-160">Indica que esse sistema operacional usa WinRM HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-160">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e8a-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8e8a-161">CommonParameters</span></span>
<span data-ttu-id="e8e8a-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8e8a-163">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8e8a-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8e8a-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e8e8a-164">INPUTS</span></span>

### <span data-ttu-id="e8e8a-165">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e8e8a-165">None</span></span>
<span data-ttu-id="e8e8a-166">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e8e8a-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e8e8a-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e8e8a-167">OUTPUTS</span></span>

## <span data-ttu-id="e8e8a-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e8e8a-168">NOTES</span></span>

## <span data-ttu-id="e8e8a-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8e8a-169">RELATED LINKS</span></span>

[<span data-ttu-id="e8e8a-170">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e8e8a-170">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="e8e8a-171">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="e8e8a-171">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


