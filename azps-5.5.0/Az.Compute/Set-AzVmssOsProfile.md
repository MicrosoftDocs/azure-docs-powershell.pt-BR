---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 71bd8ca26755118a4bb9c075ae89bad765922f3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117806"
---
# <span data-ttu-id="44602-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="44602-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="44602-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44602-102">SYNOPSIS</span></span>
<span data-ttu-id="44602-103">Define as propriedades de perfil do sistema operacional VMSS.</span><span class="sxs-lookup"><span data-stu-id="44602-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="44602-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44602-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44602-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="44602-105">DESCRIPTION</span></span>
<span data-ttu-id="44602-106">O **cmdlet Set-AzVmssOsProfile** define as propriedades de perfil do sistema operacional Conjunto de Escala de Máquina Virtual.</span><span class="sxs-lookup"><span data-stu-id="44602-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="44602-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="44602-107">EXAMPLES</span></span>

### <span data-ttu-id="44602-108">Exemplo 1: Definir as propriedades de perfil do sistema operacional para um VMSS</span><span class="sxs-lookup"><span data-stu-id="44602-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="44602-109">Esse comando define as propriedades de perfil do sistema operacional para as máquinas virtuais que pertencem ao VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="44602-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="44602-110">O comando define o prefixo de nome de computador para todas as instâncias de computador virtual no VMSS para Testar e fornece o nome de usuário e a senha do administrador.</span><span class="sxs-lookup"><span data-stu-id="44602-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="44602-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44602-111">PARAMETERS</span></span>

### <span data-ttu-id="44602-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="44602-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="44602-113">Especifica um objeto de conteúdo autônoma.</span><span class="sxs-lookup"><span data-stu-id="44602-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="44602-114">Você pode usar o Add-AzVMAdditionalUnattendContent para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="44602-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

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

### <span data-ttu-id="44602-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="44602-115">-AdminPassword</span></span>
<span data-ttu-id="44602-116">Especifica a senha de administrador a ser usada para todas as instâncias de computador virtual no VMSS.</span><span class="sxs-lookup"><span data-stu-id="44602-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="44602-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="44602-117">-AdminUsername</span></span>
<span data-ttu-id="44602-118">Especifica o nome da conta de administrador a ser usada para todas as instâncias de máquina virtual no VMSS.</span><span class="sxs-lookup"><span data-stu-id="44602-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span> <br>
<span data-ttu-id="44602-119">**Restrição somente para Windows:** Não é possível terminar \" em .\"</span><span class="sxs-lookup"><span data-stu-id="44602-119">**Windows-only restriction:** Cannot end in \".\"</span></span> <br>
<span data-ttu-id="44602-120">**Valores não permitidos:** \" \"administrador, \" \" administrador, \" \" usuário, \" \" usuário1, \" \" teste, \" usuário2 , \" \" \" teste1, \" \" usuário3, \" \" administrador1, \" \" 1, \" 123, \" a , \" \" \" actuser, \" \" adm, \" \" \" admin2, \" aspnet, \" \" \" \" backup, console, \" \" davi, \" \" \" convidado, \" john, proprietário, raiz, servidor, \" \" \" \" \" \" \" \" sql, \" \" \" suporte, \" \" support_388945a0, \" sys, \" \" \" teste2, \" \" teste3, \" \" usuário4, \" \" usuário5.</span><span class="sxs-lookup"><span data-stu-id="44602-120">**Disallowed values:** \"administrator\", \"admin\", \"user\", \"user1\", \"test\", \"user2\", \"test1\", \"user3\", \"admin1\", \"1\", \"123\", \"a\", \"actuser\", \"adm\", \"admin2\", \"aspnet\", \"backup\", \"console\", \"david\", \"guest\", \"john\", \"owner\", \"root\", \"server\", \"sql\", \"support\", \"support_388945a0\", \"sys\", \"test2\", \"test3\", \"user4\", \"user5\".</span></span> <br>
<span data-ttu-id="44602-121">**Comprimento mínimo (Linux):** 1 caractere</span><span class="sxs-lookup"><span data-stu-id="44602-121">**Minimum-length (Linux):** 1  character</span></span> <br>
<span data-ttu-id="44602-122">**Comprimento máximo (Linux):** 64 caracteres</span><span class="sxs-lookup"><span data-stu-id="44602-122">**Max-length (Linux):** 64 characters</span></span> <br>
<span data-ttu-id="44602-123">**Comprimento máximo (Windows):** 20 caracteres</span><span class="sxs-lookup"><span data-stu-id="44602-123">**Max-length (Windows):** 20 characters</span></span>  <br>
<li> <span data-ttu-id="44602-124">Para ter acesso raiz ao VM do Linux, consulte Usando privilégios raiz em [máquinas virtuais do Linux no Azure.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="44602-124">For root access to the Linux VM, see [Using root privileges on Linux virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span><br>
<li> <span data-ttu-id="44602-125">Para ver uma lista de usuários integrados do sistema no Linux que não devem ser usados nesse campo, consulte Selecionar Nomes de Usuário para [Linux no Azure.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="44602-125">For a list of built-in system users on Linux that should not be used in this field, see [Selecting User Names for Linux on Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="44602-126">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="44602-126">-ComputerNamePrefix</span></span>
<span data-ttu-id="44602-127">Especifica o prefixo de nome de computador para todas as instâncias de máquina virtual no VMSS.</span><span class="sxs-lookup"><span data-stu-id="44602-127">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="44602-128">Os nomes de computador devem ter de 1 a 15 caracteres.</span><span class="sxs-lookup"><span data-stu-id="44602-128">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="44602-129">-CustomData</span><span class="sxs-lookup"><span data-stu-id="44602-129">-CustomData</span></span>
<span data-ttu-id="44602-130">Especifica uma cadeia de caracteres codificada de base 64 de dados personalizados.</span><span class="sxs-lookup"><span data-stu-id="44602-130">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="44602-131">Isso é decodificado para uma matriz binária que é salva como um arquivo na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="44602-131">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="44602-132">O comprimento máximo da matriz binária é de 65535 bytes.</span><span class="sxs-lookup"><span data-stu-id="44602-132">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="44602-133">Para usar o cloud-init para seu VM, consulte [Usando o cloud-init para personalizar um VM do Linux durante a criação.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="44602-133">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="44602-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44602-134">-DefaultProfile</span></span>
<span data-ttu-id="44602-135">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="44602-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44602-136">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="44602-136">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="44602-137">Indica que esse cmdlet desabilita a autenticação de senha.</span><span class="sxs-lookup"><span data-stu-id="44602-137">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="44602-138">-Ouvinte</span><span class="sxs-lookup"><span data-stu-id="44602-138">-Listener</span></span>
<span data-ttu-id="44602-139">Especifica os ouvintes do Windows Remote Management (WinRM).</span><span class="sxs-lookup"><span data-stu-id="44602-139">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="44602-140">Isso habilita o Windows PowerShell remoto.</span><span class="sxs-lookup"><span data-stu-id="44602-140">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="44602-141">Você pode usar o cmdlet Add-AzVmssWinRMListener para criar o ouvinte.</span><span class="sxs-lookup"><span data-stu-id="44602-141">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

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

### <span data-ttu-id="44602-142">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="44602-142">-PublicKey</span></span>
<span data-ttu-id="44602-143">Especifica o objeto de chave pública SSH (Secure Shell).</span><span class="sxs-lookup"><span data-stu-id="44602-143">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="44602-144">Você pode usar o cmdlet Add-AzVMSshPublicKey para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="44602-144">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

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

### <span data-ttu-id="44602-145">-Secret</span><span class="sxs-lookup"><span data-stu-id="44602-145">-Secret</span></span>
<span data-ttu-id="44602-146">Especifica o objeto de segredos que contém as referências de certificado para colocar na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="44602-146">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="44602-147">Você pode usar o cmdlet Add-AzVmssSecret para criar o objeto secreto.</span><span class="sxs-lookup"><span data-stu-id="44602-147">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

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

### <span data-ttu-id="44602-148">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="44602-148">-TimeZone</span></span>
<span data-ttu-id="44602-149">Especifica o fuso horário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="44602-149">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="44602-150">por exemplo, Hora \" Padrão do \" Pacífico.</span><span class="sxs-lookup"><span data-stu-id="44602-150">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="44602-151">Os valores possíveis podem [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) de fusos horário retornados pelo [TimeZoneInfo.GetSystemTimeZones.](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)</span><span class="sxs-lookup"><span data-stu-id="44602-151">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="44602-152">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="44602-152">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="44602-153">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="44602-153">Specifies the VMSS object.</span></span>
<span data-ttu-id="44602-154">Você pode usar o cmdlet New-AzVmssConfig para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="44602-154">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="44602-155">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="44602-155">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="44602-156">Indica se as máquinas virtuais no VMSS estão habilitadas para atualizações automáticas.</span><span class="sxs-lookup"><span data-stu-id="44602-156">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="44602-157">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="44602-157">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="44602-158">Indica se o agente de máquina virtual deve ser provisionado nas máquinas virtuais no VMSS.</span><span class="sxs-lookup"><span data-stu-id="44602-158">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="44602-159">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="44602-159">-Confirm</span></span>
<span data-ttu-id="44602-160">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44602-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44602-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44602-161">-WhatIf</span></span>
<span data-ttu-id="44602-162">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="44602-162">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44602-163">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44602-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44602-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44602-164">CommonParameters</span></span>
<span data-ttu-id="44602-165">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44602-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44602-166">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44602-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44602-167">Entradas</span><span class="sxs-lookup"><span data-stu-id="44602-167">INPUTS</span></span>

### <span data-ttu-id="44602-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="44602-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="44602-169">System.String</span><span class="sxs-lookup"><span data-stu-id="44602-169">System.String</span></span>

### <span data-ttu-id="44602-170">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="44602-170">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="44602-171">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span><span class="sxs-lookup"><span data-stu-id="44602-171">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span></span>

### <span data-ttu-id="44602-172">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span><span class="sxs-lookup"><span data-stu-id="44602-172">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span></span>

### <span data-ttu-id="44602-173">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span><span class="sxs-lookup"><span data-stu-id="44602-173">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span></span>

### <span data-ttu-id="44602-174">Microsoft.Azure.Management.Compute.Models.VaultSecgroup[]</span><span class="sxs-lookup"><span data-stu-id="44602-174">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span></span>

## <span data-ttu-id="44602-175">Saídas</span><span class="sxs-lookup"><span data-stu-id="44602-175">OUTPUTS</span></span>

### <span data-ttu-id="44602-176">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="44602-176">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="44602-177">Notas</span><span class="sxs-lookup"><span data-stu-id="44602-177">NOTES</span></span>

## <span data-ttu-id="44602-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44602-178">RELATED LINKS</span></span>

[<span data-ttu-id="44602-179">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="44602-179">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="44602-180">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="44602-180">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="44602-181">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="44602-181">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="44602-182">Add-AzVmssSecsec</span><span class="sxs-lookup"><span data-stu-id="44602-182">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="44602-183">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="44602-183">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


