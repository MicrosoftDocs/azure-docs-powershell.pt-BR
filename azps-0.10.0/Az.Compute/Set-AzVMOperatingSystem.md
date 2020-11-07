---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 874045a510c8ab87143e25994fd5f15d5be7e741
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776825"
---
# <span data-ttu-id="d6edb-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="d6edb-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="d6edb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6edb-102">SYNOPSIS</span></span>
<span data-ttu-id="d6edb-103">Define as propriedades do sistema operacional para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d6edb-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="d6edb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6edb-104">SYNTAX</span></span>

### <span data-ttu-id="d6edb-105">Windows (padrão)</span><span class="sxs-lookup"><span data-stu-id="d6edb-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6edb-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="d6edb-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6edb-107">Linux</span><span class="sxs-lookup"><span data-stu-id="d6edb-107">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6edb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d6edb-108">DESCRIPTION</span></span>
<span data-ttu-id="d6edb-109">O cmdlet **set-AzVMOperatingSystem** define as propriedades do sistema operacional para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d6edb-109">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="d6edb-110">Você pode especificar as credenciais de logon, o nome do computador e o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d6edb-110">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="d6edb-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6edb-111">EXAMPLES</span></span>

### <span data-ttu-id="d6edb-112">Exemplo 1: definir propriedades do sistema operacional para uma nova máquina virtual</span><span class="sxs-lookup"><span data-stu-id="d6edb-112">Example 1: Set operating system properties for a new virtual machines</span></span>
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

<span data-ttu-id="d6edb-113">O primeiro comando converte uma senha em uma cadeia de caracteres segura e, em seguida, armazena-a na variável $SecurePassword.</span><span class="sxs-lookup"><span data-stu-id="d6edb-113">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="d6edb-114">Para obter mais informações, digite `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="d6edb-114">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>

<span data-ttu-id="d6edb-115">O segundo comando cria uma credencial para o usuário FullerP e a senha armazenada no $SecurePassword e, em seguida, armazena a credencial na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="d6edb-115">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="d6edb-116">Para obter mais informações, digite `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="d6edb-116">For more information, type `Get-Help New-Object`.</span></span>

<span data-ttu-id="d6edb-117">O terceiro comando obtém o conjunto de disponibilidade chamado AvailablitySet03 no grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="d6edb-117">The third command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="d6edb-118">O quarto comando cria um objeto de máquina virtual e, em seguida, armazena-o na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="d6edb-118">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="d6edb-119">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d6edb-119">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="d6edb-120">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="d6edb-120">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="d6edb-121">Os próximos quatro comandos atribuem valores a variáveis a serem usadas no comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="d6edb-121">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="d6edb-122">Como você pode especificar essas cadeias de caracteres diretamente no comando **set-AzVMOperatingSystem** , essa abordagem é usada somente para fins de legibilidade.</span><span class="sxs-lookup"><span data-stu-id="d6edb-122">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="d6edb-123">No entanto, você pode usar uma abordagem como esta em scripts.</span><span class="sxs-lookup"><span data-stu-id="d6edb-123">However, you might use an approach such as this in scripts.</span></span>

<span data-ttu-id="d6edb-124">O comando final define as propriedades do sistema operacional da máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="d6edb-124">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="d6edb-125">O comando usa as credenciais armazenadas em $Credential.</span><span class="sxs-lookup"><span data-stu-id="d6edb-125">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="d6edb-126">O comando usa variáveis atribuídas nos comandos anteriores para alguns parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d6edb-126">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="d6edb-127">OS</span><span class="sxs-lookup"><span data-stu-id="d6edb-127">PARAMETERS</span></span>

### <span data-ttu-id="d6edb-128">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="d6edb-128">-ComputerName</span></span>
<span data-ttu-id="d6edb-129">Especifica o nome do computador.</span><span class="sxs-lookup"><span data-stu-id="d6edb-129">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="d6edb-130">-Credential</span><span class="sxs-lookup"><span data-stu-id="d6edb-130">-Credential</span></span>
<span data-ttu-id="d6edb-131">Especifica o nome de usuário e a senha da máquina virtual como um objeto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="d6edb-131">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="d6edb-132">Para obter uma credencial, use o cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="d6edb-132">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="d6edb-133">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="d6edb-133">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="d6edb-134">-CustomData</span><span class="sxs-lookup"><span data-stu-id="d6edb-134">-CustomData</span></span>
<span data-ttu-id="d6edb-135">Especifica uma cadeia de caracteres de dados personalizados codificada como base-64.</span><span class="sxs-lookup"><span data-stu-id="d6edb-135">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="d6edb-136">Isso é decodificado para uma matriz binária salva como um arquivo na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d6edb-136">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="d6edb-137">O comprimento máximo da matriz binária é de 65535 bytes.</span><span class="sxs-lookup"><span data-stu-id="d6edb-137">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="d6edb-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6edb-138">-DefaultProfile</span></span>
<span data-ttu-id="d6edb-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d6edb-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6edb-140">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="d6edb-140">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="d6edb-141">Indica que esse cmdlet desabilita a autenticação de senha.</span><span class="sxs-lookup"><span data-stu-id="d6edb-141">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="d6edb-142">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="d6edb-142">-EnableAutoUpdate</span></span>
<span data-ttu-id="d6edb-143">Indica que esse cmdlet habilita a atualização automática.</span><span class="sxs-lookup"><span data-stu-id="d6edb-143">Indicates that this cmdlet enables auto update.</span></span>

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

### <span data-ttu-id="d6edb-144">-Linux</span><span class="sxs-lookup"><span data-stu-id="d6edb-144">-Linux</span></span>
<span data-ttu-id="d6edb-145">Indica que o tipo de sistema operacional é o Linux.</span><span class="sxs-lookup"><span data-stu-id="d6edb-145">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="d6edb-146">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="d6edb-146">-ProvisionVMAgent</span></span>
<span data-ttu-id="d6edb-147">Indica que as configurações exigem que o agente da máquina virtual seja instalado na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d6edb-147">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="d6edb-148">-Fuso horário</span><span class="sxs-lookup"><span data-stu-id="d6edb-148">-TimeZone</span></span>
<span data-ttu-id="d6edb-149">Especifica o fuso horário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d6edb-149">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="d6edb-150">-VM</span><span class="sxs-lookup"><span data-stu-id="d6edb-150">-VM</span></span>
<span data-ttu-id="d6edb-151">Especifica o objeto da máquina virtual local no qual definir propriedades do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d6edb-151">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="d6edb-152">Para obter um objeto de máquina virtual, use o cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="d6edb-152">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="d6edb-153">Crie um objeto de máquina virtual usando o cmdlet New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="d6edb-153">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="d6edb-154">-Windows</span><span class="sxs-lookup"><span data-stu-id="d6edb-154">-Windows</span></span>
<span data-ttu-id="d6edb-155">Indica que o tipo de sistema operacional é Windows.</span><span class="sxs-lookup"><span data-stu-id="d6edb-155">Indicates that the type of operating system is Windows.</span></span>

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

### <span data-ttu-id="d6edb-156">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="d6edb-156">-WinRMCertificateUrl</span></span>
<span data-ttu-id="d6edb-157">Especifica o URI de um certificado WinRM.</span><span class="sxs-lookup"><span data-stu-id="d6edb-157">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="d6edb-158">Isso precisa ser armazenado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="d6edb-158">This needs to be stored in a Key Vault.</span></span>

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

### <span data-ttu-id="d6edb-159">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="d6edb-159">-WinRMHttp</span></span>
<span data-ttu-id="d6edb-160">Indica que esse sistema operacional usa o WinRM HTTP.</span><span class="sxs-lookup"><span data-stu-id="d6edb-160">Indicates that this operating system uses HTTP WinRM.</span></span>

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

### <span data-ttu-id="d6edb-161">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="d6edb-161">-WinRMHttps</span></span>
<span data-ttu-id="d6edb-162">Indica que esse sistema operacional usa WinRM HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d6edb-162">Indicates that this operating system uses HTTPS WinRM.</span></span>

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

### <span data-ttu-id="d6edb-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6edb-163">CommonParameters</span></span>
<span data-ttu-id="d6edb-164">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6edb-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6edb-165">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6edb-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6edb-166">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d6edb-166">INPUTS</span></span>

### <span data-ttu-id="d6edb-167">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d6edb-167">PSVirtualMachine</span></span>
<span data-ttu-id="d6edb-168">O parâmetro ' VM ' aceita o valor do tipo ' PSVirtualMachine ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d6edb-168">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="d6edb-169">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d6edb-169">OUTPUTS</span></span>

### <span data-ttu-id="d6edb-170">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d6edb-170">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d6edb-171">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d6edb-171">NOTES</span></span>

## <span data-ttu-id="d6edb-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6edb-172">RELATED LINKS</span></span>

[<span data-ttu-id="d6edb-173">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d6edb-173">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="d6edb-174">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="d6edb-174">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


