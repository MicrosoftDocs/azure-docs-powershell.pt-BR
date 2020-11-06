---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssOsProfile.md
ms.openlocfilehash: 45deca60451f79dd0d20a0b1238f32e91d8ef2ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430345"
---
# <span data-ttu-id="ff6f4-101">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="ff6f4-101">Set-AzureRmVmssOsProfile</span></span>

## <span data-ttu-id="ff6f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff6f4-102">SYNOPSIS</span></span>
<span data-ttu-id="ff6f4-103">Define as propriedades do perfil do sistema operacional do VMSS.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-103">Sets the VMSS operating system profile properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff6f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff6f4-104">SYNTAX</span></span>

```
Set-AzureRmVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff6f4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff6f4-105">DESCRIPTION</span></span>
<span data-ttu-id="ff6f4-106">O cmdlet **set-AzureRmVmssOsProfile** define as propriedades do perfil do sistema operacional do conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-106">The **Set-AzureRmVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="ff6f4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff6f4-107">EXAMPLES</span></span>

### <span data-ttu-id="ff6f4-108">Exemplo 1: definir as propriedades de perfil do sistema operacional para um VMSS</span><span class="sxs-lookup"><span data-stu-id="ff6f4-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzureRmVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="ff6f4-109">Este comando define as propriedades do perfil do sistema operacional das máquinas virtuais que pertencem ao VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="ff6f4-110">O comando define o prefixo do nome do computador para todas as instâncias da máquina virtual no VMSS para testar e fornece o nome de usuário e a senha do administrador.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="ff6f4-111">OS</span><span class="sxs-lookup"><span data-stu-id="ff6f4-111">PARAMETERS</span></span>

### <span data-ttu-id="ff6f4-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="ff6f4-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="ff6f4-113">Especifica um objeto de conteúdo autônomo.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="ff6f4-114">Você pode usar o Add-AzureRmVMAdditionalUnattendContent para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-114">You can use the Add-AzureRmVMAdditionalUnattendContent to create the object.</span></span>

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

### <span data-ttu-id="ff6f4-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="ff6f4-115">-AdminPassword</span></span>
<span data-ttu-id="ff6f4-116">Especifica a senha de administrador a ser usada para todas as instâncias de máquina virtual no VMSS.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="ff6f4-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="ff6f4-117">-AdminUsername</span></span>
<span data-ttu-id="ff6f4-118">Especifica o nome da conta de administrador a ser usado para todas as instâncias de máquina virtual no VMSS.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="ff6f4-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="ff6f4-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="ff6f4-120">Especifica o prefixo do nome do computador para todas as instâncias da máquina virtual no VMSS.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="ff6f4-121">Os nomes de computador devem ter de 1 a 15 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-121">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="ff6f4-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="ff6f4-122">-CustomData</span></span>
<span data-ttu-id="ff6f4-123">Especifica uma cadeia de caracteres de dados personalizados codificada como base-64.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="ff6f4-124">Isso é decodificado para uma matriz binária salva como um arquivo na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="ff6f4-125">O comprimento máximo da matriz binária é de 65535 bytes.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-125">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="ff6f4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff6f4-126">-DefaultProfile</span></span>
<span data-ttu-id="ff6f4-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff6f4-128">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="ff6f4-128">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="ff6f4-129">Indica que esse cmdlet desabilita a autenticação de senha.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-129">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="ff6f4-130">-Listener</span><span class="sxs-lookup"><span data-stu-id="ff6f4-130">-Listener</span></span>
<span data-ttu-id="ff6f4-131">Especifica os ouvintes do Windows Remote Management (WinRM).</span><span class="sxs-lookup"><span data-stu-id="ff6f4-131">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="ff6f4-132">Isso permite que o Windows PowerShell remoto seja reativado.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-132">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="ff6f4-133">Você pode usar o cmdlet Add-AzureRmVmssWinRMListener para criar o ouvinte.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-133">You can use the Add-AzureRmVmssWinRMListener cmdlet to create the listener.</span></span>

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

### <span data-ttu-id="ff6f4-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="ff6f4-134">-PublicKey</span></span>
<span data-ttu-id="ff6f4-135">Especifica o objeto de chave pública SSH (Secure Shell).</span><span class="sxs-lookup"><span data-stu-id="ff6f4-135">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="ff6f4-136">Você pode usar o cmdlet Add-AzureRmVMSshPublicKey para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-136">You can use the Add-AzureRmVMSshPublicKey cmdlet to create the object.</span></span>

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

### <span data-ttu-id="ff6f4-137">-Segredo</span><span class="sxs-lookup"><span data-stu-id="ff6f4-137">-Secret</span></span>
<span data-ttu-id="ff6f4-138">Especifica o objeto segredos que contém as referências de certificado a serem colocadas na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-138">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="ff6f4-139">Você pode usar o cmdlet Add-AzureRmVmssSecret para criar o objeto de segredos.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-139">You can use the Add-AzureRmVmssSecret cmdlet to create the secrets object.</span></span>

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

### <span data-ttu-id="ff6f4-140">-Fuso horário</span><span class="sxs-lookup"><span data-stu-id="ff6f4-140">-TimeZone</span></span>
<span data-ttu-id="ff6f4-141">Especifica o fuso horário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-141">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="ff6f4-142">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ff6f4-142">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ff6f4-143">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-143">Specifies the VMSS object.</span></span>
<span data-ttu-id="ff6f4-144">Você pode usar o cmdlet New-AzureRmVmssConfig para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-144">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="ff6f4-145">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="ff6f4-145">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="ff6f4-146">Indica se as máquinas virtuais no VMSS estão habilitadas para atualizações automáticas.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-146">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="ff6f4-147">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="ff6f4-147">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="ff6f4-148">Indica se o agente da máquina virtual deve ser provisionado nas máquinas virtuais no VMSS.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-148">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="ff6f4-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ff6f4-149">-Confirm</span></span>
<span data-ttu-id="ff6f4-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff6f4-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff6f4-151">-WhatIf</span></span>
<span data-ttu-id="ff6f4-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff6f4-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff6f4-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff6f4-154">CommonParameters</span></span>
<span data-ttu-id="ff6f4-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff6f4-156">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff6f4-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff6f4-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff6f4-157">INPUTS</span></span>

### <span data-ttu-id="ff6f4-158">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ff6f4-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="ff6f4-159">System. String</span><span class="sxs-lookup"><span data-stu-id="ff6f4-159">System.String</span></span>

### <span data-ttu-id="ff6f4-160">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ff6f4-160">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="ff6f4-161">Microsoft. Azure. Management. COMPUTE. Models. AdditionalUnattendContent []</span><span class="sxs-lookup"><span data-stu-id="ff6f4-161">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span></span>

### <span data-ttu-id="ff6f4-162">Microsoft. Azure. Management. COMPUTE. Models. WinRMListener []</span><span class="sxs-lookup"><span data-stu-id="ff6f4-162">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span></span>

### <span data-ttu-id="ff6f4-163">Microsoft. Azure. Management. COMPUTE. Models. SshPublicKey []</span><span class="sxs-lookup"><span data-stu-id="ff6f4-163">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span></span>

### <span data-ttu-id="ff6f4-164">Microsoft. Azure. Management. COMPUTE. Models. VaultSecretGroup []</span><span class="sxs-lookup"><span data-stu-id="ff6f4-164">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span></span>

## <span data-ttu-id="ff6f4-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff6f4-165">OUTPUTS</span></span>

### <span data-ttu-id="ff6f4-166">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ff6f4-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ff6f4-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff6f4-167">NOTES</span></span>

## <span data-ttu-id="ff6f4-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff6f4-168">RELATED LINKS</span></span>

[<span data-ttu-id="ff6f4-169">Add-AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="ff6f4-169">Add-AzureRmVMAdditionalUnattendContent</span></span>](./Add-AzureRmVMAdditionalUnattendContent.md)

[<span data-ttu-id="ff6f4-170">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="ff6f4-170">Add-AzureRmVmssWinRMListener</span></span>](./Add-AzureRmVmssWinRMListener.md)

[<span data-ttu-id="ff6f4-171">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="ff6f4-171">Add-AzureRmVMSshPublicKey</span></span>](./Add-AzureRmVMSshPublicKey.md)

[<span data-ttu-id="ff6f4-172">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="ff6f4-172">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)

[<span data-ttu-id="ff6f4-173">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ff6f4-173">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


