---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 71bd8ca26755118a4bb9c075ae89bad765922f3d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430153"
---
# <span data-ttu-id="3ffd1-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="3ffd1-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="3ffd1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ffd1-102">SYNOPSIS</span></span>
<span data-ttu-id="3ffd1-103">Define as propriedades do perfil do sistema operacional do VMSS.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="3ffd1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ffd1-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ffd1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3ffd1-105">DESCRIPTION</span></span>
<span data-ttu-id="3ffd1-106">O cmdlet **set-AzVmssOsProfile** define as propriedades do perfil do sistema operacional do conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="3ffd1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ffd1-107">EXAMPLES</span></span>

### <span data-ttu-id="3ffd1-108">Exemplo 1: definir as propriedades de perfil do sistema operacional para um VMSS</span><span class="sxs-lookup"><span data-stu-id="3ffd1-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="3ffd1-109">Este comando define as propriedades do perfil do sistema operacional das máquinas virtuais que pertencem ao VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="3ffd1-110">O comando define o prefixo do nome do computador para todas as instâncias da máquina virtual no VMSS para testar e fornece o nome de usuário e a senha do administrador.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="3ffd1-111">OS</span><span class="sxs-lookup"><span data-stu-id="3ffd1-111">PARAMETERS</span></span>

### <span data-ttu-id="3ffd1-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="3ffd1-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="3ffd1-113">Especifica um objeto de conteúdo autônomo.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="3ffd1-114">Você pode usar o Add-AzVMAdditionalUnattendContent para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ffd1-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="3ffd1-115">-AdminPassword</span></span>
<span data-ttu-id="3ffd1-116">Especifica a senha de administrador a ser usada para todas as instâncias de máquina virtual no VMSS.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ffd1-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="3ffd1-117">-AdminUsername</span></span>
<span data-ttu-id="3ffd1-118">Especifica o nome da conta de administrador a ser usado para todas as instâncias de máquina virtual no VMSS.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span> <br>
<span data-ttu-id="3ffd1-119">**Restrição somente do Windows:** Não pode terminar em \" .\"</span><span class="sxs-lookup"><span data-stu-id="3ffd1-119">**Windows-only restriction:** Cannot end in \".\"</span></span> <br>
<span data-ttu-id="3ffd1-120">**Valores não permitidos:** \" administrador \" , \" administrador \" , \" usuário \" , \" Usuário1 \" , \" teste \" , \" user2 \" , \" Test1 \" , \" usuário3 \" , \" admin1 \" , \" 1 \" , \" 123 \" , \" a \" , \" actuser \" , \" ADM \" , \" admin2 \" , \" ASPNET \" , \" backup \" , \" console \" , \" David \" , \" convidado \" , \" John \" , \" proprietário \" , \" raiz \" , \" servidor \" , \" SQL \" , \" suporte \" , \" Support_388945a0 \" , \" Sys \" , \" test2 \" , \" test3 \" , \" User4 \" , \" User5 \" .</span><span class="sxs-lookup"><span data-stu-id="3ffd1-120">**Disallowed values:** \"administrator\", \"admin\", \"user\", \"user1\", \"test\", \"user2\", \"test1\", \"user3\", \"admin1\", \"1\", \"123\", \"a\", \"actuser\", \"adm\", \"admin2\", \"aspnet\", \"backup\", \"console\", \"david\", \"guest\", \"john\", \"owner\", \"root\", \"server\", \"sql\", \"support\", \"support_388945a0\", \"sys\", \"test2\", \"test3\", \"user4\", \"user5\".</span></span> <br>
<span data-ttu-id="3ffd1-121">**Comprimento mínimo (Linux):** 1 caractere</span><span class="sxs-lookup"><span data-stu-id="3ffd1-121">**Minimum-length (Linux):** 1  character</span></span> <br>
<span data-ttu-id="3ffd1-122">**Tamanho máximo (Linux):** 64 caracteres</span><span class="sxs-lookup"><span data-stu-id="3ffd1-122">**Max-length (Linux):** 64 characters</span></span> <br>
<span data-ttu-id="3ffd1-123">**Tamanho máximo (Windows):** 20 caracteres</span><span class="sxs-lookup"><span data-stu-id="3ffd1-123">**Max-length (Windows):** 20 characters</span></span>  <br>
<li> <span data-ttu-id="3ffd1-124">Para ter acesso à raiz à VM Linux, consulte [usando privilégios de raiz em máquinas virtuais Linux no Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="3ffd1-124">For root access to the Linux VM, see [Using root privileges on Linux virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span><br>
<li> <span data-ttu-id="3ffd1-125">Para obter uma lista de usuários internos do sistema no Linux que não devem ser usados neste campo, consulte [selecionando nomes de usuário para Linux no Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="3ffd1-125">For a list of built-in system users on Linux that should not be used in this field, see [Selecting User Names for Linux on Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ffd1-126">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="3ffd1-126">-ComputerNamePrefix</span></span>
<span data-ttu-id="3ffd1-127">Especifica o prefixo do nome do computador para todas as instâncias da máquina virtual no VMSS.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-127">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="3ffd1-128">Os nomes de computador devem ter de 1 a 15 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-128">Computer names must be 1 to 15 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ffd1-129">-CustomData</span><span class="sxs-lookup"><span data-stu-id="3ffd1-129">-CustomData</span></span>
<span data-ttu-id="3ffd1-130">Especifica uma cadeia de caracteres de dados personalizados codificada como base-64.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-130">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="3ffd1-131">Isso é decodificado para uma matriz binária salva como um arquivo na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-131">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="3ffd1-132">O comprimento máximo da matriz binária é de 65535 bytes.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-132">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="3ffd1-133">Para usar init-init para a sua VM, consulte [usar o Cloud-init para personalizar uma VM Linux durante a criação](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="3ffd1-133">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="3ffd1-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ffd1-134">-DefaultProfile</span></span>
<span data-ttu-id="3ffd1-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ffd1-136">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="3ffd1-136">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="3ffd1-137">Indica que esse cmdlet desabilita a autenticação de senha.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-137">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ffd1-138">-Listener</span><span class="sxs-lookup"><span data-stu-id="3ffd1-138">-Listener</span></span>
<span data-ttu-id="3ffd1-139">Especifica os ouvintes do Windows Remote Management (WinRM).</span><span class="sxs-lookup"><span data-stu-id="3ffd1-139">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="3ffd1-140">Isso permite que o Windows PowerShell remoto seja reativado.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-140">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="3ffd1-141">Você pode usar o cmdlet Add-AzVmssWinRMListener para criar o ouvinte.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-141">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.WinRMListener[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ffd1-142">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="3ffd1-142">-PublicKey</span></span>
<span data-ttu-id="3ffd1-143">Especifica o objeto de chave pública SSH (Secure Shell).</span><span class="sxs-lookup"><span data-stu-id="3ffd1-143">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="3ffd1-144">Você pode usar o cmdlet Add-AzVMSshPublicKey para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-144">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.SshPublicKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ffd1-145">-Segredo</span><span class="sxs-lookup"><span data-stu-id="3ffd1-145">-Secret</span></span>
<span data-ttu-id="3ffd1-146">Especifica o objeto segredos que contém as referências de certificado a serem colocadas na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-146">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="3ffd1-147">Você pode usar o cmdlet Add-AzVmssSecret para criar o objeto de segredos.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-147">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ffd1-148">-Fuso horário</span><span class="sxs-lookup"><span data-stu-id="3ffd1-148">-TimeZone</span></span>
<span data-ttu-id="3ffd1-149">Especifica o fuso horário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-149">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="3ffd1-150">por exemplo, \" hora padrão do Pacífico \" .</span><span class="sxs-lookup"><span data-stu-id="3ffd1-150">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="3ffd1-151">Os valores possíveis podem ser [TimeZoneInfo.ID](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) valor a partir de fusos horários retornados por [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span><span class="sxs-lookup"><span data-stu-id="3ffd1-151">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ffd1-152">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3ffd1-152">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="3ffd1-153">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-153">Specifies the VMSS object.</span></span>
<span data-ttu-id="3ffd1-154">Você pode usar o cmdlet New-AzVmssConfig para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-154">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ffd1-155">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="3ffd1-155">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="3ffd1-156">Indica se as máquinas virtuais no VMSS estão habilitadas para atualizações automáticas.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-156">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ffd1-157">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="3ffd1-157">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="3ffd1-158">Indica se o agente da máquina virtual deve ser provisionado nas máquinas virtuais no VMSS.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-158">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ffd1-159">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3ffd1-159">-Confirm</span></span>
<span data-ttu-id="3ffd1-160">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-160">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ffd1-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ffd1-161">-WhatIf</span></span>
<span data-ttu-id="3ffd1-162">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-162">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ffd1-163">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-163">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ffd1-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ffd1-164">CommonParameters</span></span>
<span data-ttu-id="3ffd1-165">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ffd1-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ffd1-166">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ffd1-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ffd1-167">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3ffd1-167">INPUTS</span></span>

### <span data-ttu-id="3ffd1-168">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3ffd1-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="3ffd1-169">System. String</span><span class="sxs-lookup"><span data-stu-id="3ffd1-169">System.String</span></span>

### <span data-ttu-id="3ffd1-170">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3ffd1-170">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3ffd1-171">Microsoft. Azure. Management. COMPUTE. Models. AdditionalUnattendContent []</span><span class="sxs-lookup"><span data-stu-id="3ffd1-171">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span></span>

### <span data-ttu-id="3ffd1-172">Microsoft. Azure. Management. COMPUTE. Models. WinRMListener []</span><span class="sxs-lookup"><span data-stu-id="3ffd1-172">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span></span>

### <span data-ttu-id="3ffd1-173">Microsoft. Azure. Management. COMPUTE. Models. SshPublicKey []</span><span class="sxs-lookup"><span data-stu-id="3ffd1-173">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span></span>

### <span data-ttu-id="3ffd1-174">Microsoft. Azure. Management. COMPUTE. Models. VaultSecretGroup []</span><span class="sxs-lookup"><span data-stu-id="3ffd1-174">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span></span>

## <span data-ttu-id="3ffd1-175">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3ffd1-175">OUTPUTS</span></span>

### <span data-ttu-id="3ffd1-176">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3ffd1-176">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="3ffd1-177">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3ffd1-177">NOTES</span></span>

## <span data-ttu-id="3ffd1-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ffd1-178">RELATED LINKS</span></span>

[<span data-ttu-id="3ffd1-179">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="3ffd1-179">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="3ffd1-180">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="3ffd1-180">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="3ffd1-181">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="3ffd1-181">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="3ffd1-182">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="3ffd1-182">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="3ffd1-183">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="3ffd1-183">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


