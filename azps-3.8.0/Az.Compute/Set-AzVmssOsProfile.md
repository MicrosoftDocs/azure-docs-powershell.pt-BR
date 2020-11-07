---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 3d3fdb53bf6dd0338f89bd03f11786bc9942acaa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944610"
---
# <span data-ttu-id="17a39-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="17a39-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="17a39-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="17a39-102">SYNOPSIS</span></span>
<span data-ttu-id="17a39-103">Define as propriedades do perfil do sistema operacional do VMSS.</span><span class="sxs-lookup"><span data-stu-id="17a39-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="17a39-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17a39-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17a39-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="17a39-105">DESCRIPTION</span></span>
<span data-ttu-id="17a39-106">O cmdlet **set-AzVmssOsProfile** define as propriedades do perfil do sistema operacional do conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="17a39-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="17a39-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17a39-107">EXAMPLES</span></span>

### <span data-ttu-id="17a39-108">Exemplo 1: definir as propriedades de perfil do sistema operacional para um VMSS</span><span class="sxs-lookup"><span data-stu-id="17a39-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="17a39-109">Este comando define as propriedades do perfil do sistema operacional das máquinas virtuais que pertencem ao VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="17a39-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="17a39-110">O comando define o prefixo do nome do computador para todas as instâncias da máquina virtual no VMSS para testar e fornece o nome de usuário e a senha do administrador.</span><span class="sxs-lookup"><span data-stu-id="17a39-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="17a39-111">OS</span><span class="sxs-lookup"><span data-stu-id="17a39-111">PARAMETERS</span></span>

### <span data-ttu-id="17a39-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="17a39-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="17a39-113">Especifica um objeto de conteúdo autônomo.</span><span class="sxs-lookup"><span data-stu-id="17a39-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="17a39-114">Você pode usar o Add-AzVMAdditionalUnattendContent para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="17a39-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

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

### <span data-ttu-id="17a39-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="17a39-115">-AdminPassword</span></span>
<span data-ttu-id="17a39-116">Especifica a senha de administrador a ser usada para todas as instâncias de máquina virtual no VMSS.</span><span class="sxs-lookup"><span data-stu-id="17a39-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="17a39-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="17a39-117">-AdminUsername</span></span>
<span data-ttu-id="17a39-118">Especifica o nome da conta de administrador a ser usado para todas as instâncias de máquina virtual no VMSS.</span><span class="sxs-lookup"><span data-stu-id="17a39-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="17a39-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="17a39-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="17a39-120">Especifica o prefixo do nome do computador para todas as instâncias da máquina virtual no VMSS.</span><span class="sxs-lookup"><span data-stu-id="17a39-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="17a39-121">Os nomes de computador devem ter de 1 a 15 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="17a39-121">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="17a39-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="17a39-122">-CustomData</span></span>
<span data-ttu-id="17a39-123">Especifica uma cadeia de caracteres de dados personalizados codificada como base-64.</span><span class="sxs-lookup"><span data-stu-id="17a39-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="17a39-124">Isso é decodificado para uma matriz binária salva como um arquivo na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="17a39-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="17a39-125">O comprimento máximo da matriz binária é de 65535 bytes.</span><span class="sxs-lookup"><span data-stu-id="17a39-125">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="17a39-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17a39-126">-DefaultProfile</span></span>
<span data-ttu-id="17a39-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17a39-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17a39-128">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="17a39-128">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="17a39-129">Indica que esse cmdlet desabilita a autenticação de senha.</span><span class="sxs-lookup"><span data-stu-id="17a39-129">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="17a39-130">-Listener</span><span class="sxs-lookup"><span data-stu-id="17a39-130">-Listener</span></span>
<span data-ttu-id="17a39-131">Especifica os ouvintes do Windows Remote Management (WinRM).</span><span class="sxs-lookup"><span data-stu-id="17a39-131">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="17a39-132">Isso permite que o Windows PowerShell remoto seja reativado.</span><span class="sxs-lookup"><span data-stu-id="17a39-132">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="17a39-133">Você pode usar o cmdlet Add-AzVmssWinRMListener para criar o ouvinte.</span><span class="sxs-lookup"><span data-stu-id="17a39-133">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

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

### <span data-ttu-id="17a39-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="17a39-134">-PublicKey</span></span>
<span data-ttu-id="17a39-135">Especifica o objeto de chave pública SSH (Secure Shell).</span><span class="sxs-lookup"><span data-stu-id="17a39-135">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="17a39-136">Você pode usar o cmdlet Add-AzVMSshPublicKey para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="17a39-136">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

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

### <span data-ttu-id="17a39-137">-Segredo</span><span class="sxs-lookup"><span data-stu-id="17a39-137">-Secret</span></span>
<span data-ttu-id="17a39-138">Especifica o objeto segredos que contém as referências de certificado a serem colocadas na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="17a39-138">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="17a39-139">Você pode usar o cmdlet Add-AzVmssSecret para criar o objeto de segredos.</span><span class="sxs-lookup"><span data-stu-id="17a39-139">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

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

### <span data-ttu-id="17a39-140">-Fuso horário</span><span class="sxs-lookup"><span data-stu-id="17a39-140">-TimeZone</span></span>
<span data-ttu-id="17a39-141">Especifica o fuso horário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="17a39-141">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="17a39-142">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="17a39-142">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="17a39-143">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="17a39-143">Specifies the VMSS object.</span></span>
<span data-ttu-id="17a39-144">Você pode usar o cmdlet New-AzVmssConfig para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="17a39-144">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="17a39-145">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="17a39-145">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="17a39-146">Indica se as máquinas virtuais no VMSS estão habilitadas para atualizações automáticas.</span><span class="sxs-lookup"><span data-stu-id="17a39-146">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="17a39-147">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="17a39-147">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="17a39-148">Indica se o agente da máquina virtual deve ser provisionado nas máquinas virtuais no VMSS.</span><span class="sxs-lookup"><span data-stu-id="17a39-148">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="17a39-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="17a39-149">-Confirm</span></span>
<span data-ttu-id="17a39-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17a39-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17a39-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17a39-151">-WhatIf</span></span>
<span data-ttu-id="17a39-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="17a39-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17a39-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="17a39-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17a39-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17a39-154">CommonParameters</span></span>
<span data-ttu-id="17a39-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17a39-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17a39-156">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17a39-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17a39-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="17a39-157">INPUTS</span></span>

### <span data-ttu-id="17a39-158">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="17a39-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="17a39-159">System. String</span><span class="sxs-lookup"><span data-stu-id="17a39-159">System.String</span></span>

### <span data-ttu-id="17a39-160">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="17a39-160">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="17a39-161">Microsoft. Azure. Management. COMPUTE. Models. AdditionalUnattendContent []</span><span class="sxs-lookup"><span data-stu-id="17a39-161">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span></span>

### <span data-ttu-id="17a39-162">Microsoft. Azure. Management. COMPUTE. Models. WinRMListener []</span><span class="sxs-lookup"><span data-stu-id="17a39-162">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span></span>

### <span data-ttu-id="17a39-163">Microsoft. Azure. Management. COMPUTE. Models. SshPublicKey []</span><span class="sxs-lookup"><span data-stu-id="17a39-163">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span></span>

### <span data-ttu-id="17a39-164">Microsoft. Azure. Management. COMPUTE. Models. VaultSecretGroup []</span><span class="sxs-lookup"><span data-stu-id="17a39-164">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span></span>

## <span data-ttu-id="17a39-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="17a39-165">OUTPUTS</span></span>

### <span data-ttu-id="17a39-166">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="17a39-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="17a39-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="17a39-167">NOTES</span></span>

## <span data-ttu-id="17a39-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17a39-168">RELATED LINKS</span></span>

[<span data-ttu-id="17a39-169">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="17a39-169">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="17a39-170">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="17a39-170">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="17a39-171">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="17a39-171">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="17a39-172">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="17a39-172">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="17a39-173">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="17a39-173">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


