---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
ms.openlocfilehash: 2d742a70f1ae95d362d5ceafcc117f1296dc2cb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441390"
---
# <span data-ttu-id="46ea2-101">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="46ea2-101">Set-AzureRmVMOperatingSystem</span></span>

## <span data-ttu-id="46ea2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46ea2-102">SYNOPSIS</span></span>
<span data-ttu-id="46ea2-103">Define as propriedades do sistema operacional para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="46ea2-103">Sets operating system properties for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46ea2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46ea2-104">SYNTAX</span></span>

### <span data-ttu-id="46ea2-105">Windows (padrão)</span><span class="sxs-lookup"><span data-stu-id="46ea2-105">Windows (Default)</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46ea2-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="46ea2-106">WindowsWinRmHttps</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46ea2-107">Linux</span><span class="sxs-lookup"><span data-stu-id="46ea2-107">Linux</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46ea2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="46ea2-108">DESCRIPTION</span></span>
<span data-ttu-id="46ea2-109">O cmdlet **set-AzureRmVMOperatingSystem** define as propriedades do sistema operacional para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="46ea2-109">The **Set-AzureRmVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="46ea2-110">Você pode especificar as credenciais de logon, o nome do computador e o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="46ea2-110">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="46ea2-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46ea2-111">EXAMPLES</span></span>

### <span data-ttu-id="46ea2-112">Exemplo 1: definir propriedades do sistema operacional para uma nova máquina virtual</span><span class="sxs-lookup"><span data-stu-id="46ea2-112">Example 1: Set operating system properties for a new virtual machines</span></span>
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

<span data-ttu-id="46ea2-113">O primeiro comando converte uma senha em uma cadeia de caracteres segura e, em seguida, armazena-a na variável $SecurePassword.</span><span class="sxs-lookup"><span data-stu-id="46ea2-113">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="46ea2-114">Para obter mais informações, digite `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="46ea2-114">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>

<span data-ttu-id="46ea2-115">O segundo comando cria uma credencial para o usuário FullerP e a senha armazenada no $SecurePassword e, em seguida, armazena a credencial na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="46ea2-115">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="46ea2-116">Para obter mais informações, digite `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="46ea2-116">For more information, type `Get-Help New-Object`.</span></span>

<span data-ttu-id="46ea2-117">O terceiro comando obtém o conjunto de disponibilidade chamado AvailablitySet03 no grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="46ea2-117">The third command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="46ea2-118">O quarto comando cria um objeto de máquina virtual e, em seguida, armazena-o na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="46ea2-118">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="46ea2-119">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="46ea2-119">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="46ea2-120">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="46ea2-120">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="46ea2-121">Os próximos quatro comandos atribuem valores a variáveis a serem usadas no comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="46ea2-121">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="46ea2-122">Como você pode especificar essas cadeias de caracteres diretamente no comando **set-AzureRmVMOperatingSystem** , essa abordagem é usada somente para fins de legibilidade.</span><span class="sxs-lookup"><span data-stu-id="46ea2-122">Because you could specify these strings directly in the **Set-AzureRmVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="46ea2-123">No entanto, você pode usar uma abordagem como esta em scripts.</span><span class="sxs-lookup"><span data-stu-id="46ea2-123">However, you might use an approach such as this in scripts.</span></span>

<span data-ttu-id="46ea2-124">O comando final define as propriedades do sistema operacional da máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="46ea2-124">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="46ea2-125">O comando usa as credenciais armazenadas em $Credential.</span><span class="sxs-lookup"><span data-stu-id="46ea2-125">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="46ea2-126">O comando usa variáveis atribuídas nos comandos anteriores para alguns parâmetros.</span><span class="sxs-lookup"><span data-stu-id="46ea2-126">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="46ea2-127">OS</span><span class="sxs-lookup"><span data-stu-id="46ea2-127">PARAMETERS</span></span>

### <span data-ttu-id="46ea2-128">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="46ea2-128">-ComputerName</span></span>
<span data-ttu-id="46ea2-129">Especifica o nome do computador.</span><span class="sxs-lookup"><span data-stu-id="46ea2-129">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="46ea2-130">-Credential</span><span class="sxs-lookup"><span data-stu-id="46ea2-130">-Credential</span></span>
<span data-ttu-id="46ea2-131">Especifica o nome de usuário e a senha da máquina virtual como um objeto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="46ea2-131">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="46ea2-132">Para obter uma credencial, use o cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="46ea2-132">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="46ea2-133">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="46ea2-133">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="46ea2-134">-CustomData</span><span class="sxs-lookup"><span data-stu-id="46ea2-134">-CustomData</span></span>
<span data-ttu-id="46ea2-135">Especifica uma cadeia de caracteres de dados personalizados codificada como base-64.</span><span class="sxs-lookup"><span data-stu-id="46ea2-135">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="46ea2-136">Isso é decodificado para uma matriz binária salva como um arquivo na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="46ea2-136">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="46ea2-137">O comprimento máximo da matriz binária é de 65535 bytes.</span><span class="sxs-lookup"><span data-stu-id="46ea2-137">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="46ea2-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46ea2-138">-DefaultProfile</span></span>
<span data-ttu-id="46ea2-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46ea2-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46ea2-140">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="46ea2-140">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="46ea2-141">Indica que esse cmdlet desabilita a autenticação de senha.</span><span class="sxs-lookup"><span data-stu-id="46ea2-141">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="46ea2-142">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="46ea2-142">-EnableAutoUpdate</span></span>
<span data-ttu-id="46ea2-143">Indica que esse cmdlet habilita a atualização automática.</span><span class="sxs-lookup"><span data-stu-id="46ea2-143">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46ea2-144">-Linux</span><span class="sxs-lookup"><span data-stu-id="46ea2-144">-Linux</span></span>
<span data-ttu-id="46ea2-145">Indica que o tipo de sistema operacional é o Linux.</span><span class="sxs-lookup"><span data-stu-id="46ea2-145">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="46ea2-146">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="46ea2-146">-ProvisionVMAgent</span></span>
<span data-ttu-id="46ea2-147">Indica que as configurações exigem que o agente da máquina virtual seja instalado na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="46ea2-147">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="46ea2-148">-Fuso horário</span><span class="sxs-lookup"><span data-stu-id="46ea2-148">-TimeZone</span></span>
<span data-ttu-id="46ea2-149">Especifica o fuso horário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="46ea2-149">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46ea2-150">-VM</span><span class="sxs-lookup"><span data-stu-id="46ea2-150">-VM</span></span>
<span data-ttu-id="46ea2-151">Especifica o objeto da máquina virtual local no qual definir propriedades do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="46ea2-151">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="46ea2-152">Para obter um objeto de máquina virtual, use o cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="46ea2-152">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="46ea2-153">Crie um objeto de máquina virtual usando o cmdlet New-AzureRmVMConfig.</span><span class="sxs-lookup"><span data-stu-id="46ea2-153">Create a virtual machine object by using the New-AzureRmVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="46ea2-154">-Windows</span><span class="sxs-lookup"><span data-stu-id="46ea2-154">-Windows</span></span>
<span data-ttu-id="46ea2-155">Indica que o tipo de sistema operacional é Windows.</span><span class="sxs-lookup"><span data-stu-id="46ea2-155">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46ea2-156">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="46ea2-156">-WinRMCertificateUrl</span></span>
<span data-ttu-id="46ea2-157">Especifica o URI de um certificado WinRM.</span><span class="sxs-lookup"><span data-stu-id="46ea2-157">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="46ea2-158">Isso precisa ser armazenado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="46ea2-158">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46ea2-159">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="46ea2-159">-WinRMHttp</span></span>
<span data-ttu-id="46ea2-160">Indica que esse sistema operacional usa o WinRM HTTP.</span><span class="sxs-lookup"><span data-stu-id="46ea2-160">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46ea2-161">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="46ea2-161">-WinRMHttps</span></span>
<span data-ttu-id="46ea2-162">Indica que esse sistema operacional usa WinRM HTTPS.</span><span class="sxs-lookup"><span data-stu-id="46ea2-162">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46ea2-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46ea2-163">CommonParameters</span></span>
<span data-ttu-id="46ea2-164">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46ea2-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46ea2-165">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46ea2-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46ea2-166">SENSORES</span><span class="sxs-lookup"><span data-stu-id="46ea2-166">INPUTS</span></span>

## <span data-ttu-id="46ea2-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="46ea2-167">OUTPUTS</span></span>

## <span data-ttu-id="46ea2-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="46ea2-168">NOTES</span></span>

## <span data-ttu-id="46ea2-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46ea2-169">RELATED LINKS</span></span>

[<span data-ttu-id="46ea2-170">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="46ea2-170">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="46ea2-171">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="46ea2-171">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

