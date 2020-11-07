---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 98ebce4e139d230607da77536492d0ba40d0760f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776809"
---
# <span data-ttu-id="32307-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="32307-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="32307-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32307-102">SYNOPSIS</span></span>
<span data-ttu-id="32307-103">Define as propriedades do perfil do sistema operacional do VMSS.</span><span class="sxs-lookup"><span data-stu-id="32307-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="32307-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32307-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32307-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="32307-105">DESCRIPTION</span></span>
<span data-ttu-id="32307-106">O cmdlet **set-AzVmssOsProfile** define as propriedades do perfil do sistema operacional do conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="32307-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="32307-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32307-107">EXAMPLES</span></span>

### <span data-ttu-id="32307-108">Exemplo 1: definir as propriedades de perfil do sistema operacional para um VMSS</span><span class="sxs-lookup"><span data-stu-id="32307-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="32307-109">Este comando define as propriedades do perfil do sistema operacional das máquinas virtuais que pertencem ao VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="32307-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="32307-110">O comando define o prefixo do nome do computador para todas as instâncias da máquina virtual no VMSS para testar e fornece o nome de usuário e a senha do administrador.</span><span class="sxs-lookup"><span data-stu-id="32307-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="32307-111">OS</span><span class="sxs-lookup"><span data-stu-id="32307-111">PARAMETERS</span></span>

### <span data-ttu-id="32307-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="32307-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="32307-113">Especifica um objeto de conteúdo autônomo.</span><span class="sxs-lookup"><span data-stu-id="32307-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="32307-114">Você pode usar o Add-AzVMAdditionalUnattendContent para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="32307-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

```yaml
Type: AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32307-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="32307-115">-AdminPassword</span></span>
<span data-ttu-id="32307-116">Especifica a senha de administrador a ser usada para todas as instâncias de máquina virtual no VMSS.</span><span class="sxs-lookup"><span data-stu-id="32307-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32307-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="32307-117">-AdminUsername</span></span>
<span data-ttu-id="32307-118">Especifica o nome da conta de administrador a ser usado para todas as instâncias de máquina virtual no VMSS.</span><span class="sxs-lookup"><span data-stu-id="32307-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32307-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="32307-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="32307-120">Especifica o prefixo do nome do computador para todas as instâncias da máquina virtual no VMSS.</span><span class="sxs-lookup"><span data-stu-id="32307-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="32307-121">Os nomes de computador devem ter de 1 a 15 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="32307-121">Computer names must be 1 to 15 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32307-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="32307-122">-CustomData</span></span>
<span data-ttu-id="32307-123">Especifica uma cadeia de caracteres de dados personalizados codificada como base-64.</span><span class="sxs-lookup"><span data-stu-id="32307-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="32307-124">Isso é decodificado para uma matriz binária salva como um arquivo na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="32307-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="32307-125">O comprimento máximo da matriz binária é de 65535 bytes.</span><span class="sxs-lookup"><span data-stu-id="32307-125">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="32307-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32307-126">-DefaultProfile</span></span>
<span data-ttu-id="32307-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="32307-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32307-128">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="32307-128">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="32307-129">Indica que esse cmdlet desabilita a autenticação de senha.</span><span class="sxs-lookup"><span data-stu-id="32307-129">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32307-130">-Listener</span><span class="sxs-lookup"><span data-stu-id="32307-130">-Listener</span></span>
<span data-ttu-id="32307-131">Especifica os ouvintes do Windows Remote Management (WinRM).</span><span class="sxs-lookup"><span data-stu-id="32307-131">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="32307-132">Isso permite que o Windows PowerShell remoto seja reativado.</span><span class="sxs-lookup"><span data-stu-id="32307-132">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="32307-133">Você pode usar o cmdlet Add-AzVmssWinRMListener para criar o ouvinte.</span><span class="sxs-lookup"><span data-stu-id="32307-133">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

```yaml
Type: WinRMListener[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32307-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="32307-134">-PublicKey</span></span>
<span data-ttu-id="32307-135">Especifica o objeto de chave pública SSH (Secure Shell).</span><span class="sxs-lookup"><span data-stu-id="32307-135">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="32307-136">Você pode usar o cmdlet Add-AzVMSshPublicKey para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="32307-136">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

```yaml
Type: SshPublicKey[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32307-137">-Segredo</span><span class="sxs-lookup"><span data-stu-id="32307-137">-Secret</span></span>
<span data-ttu-id="32307-138">Especifica o objeto segredos que contém as referências de certificado a serem colocadas na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="32307-138">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="32307-139">Você pode usar o cmdlet Add-AzVmssSecret para criar o objeto de segredos.</span><span class="sxs-lookup"><span data-stu-id="32307-139">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

```yaml
Type: VaultSecretGroup[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32307-140">-Fuso horário</span><span class="sxs-lookup"><span data-stu-id="32307-140">-TimeZone</span></span>
<span data-ttu-id="32307-141">Especifica o fuso horário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="32307-141">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32307-142">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="32307-142">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="32307-143">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="32307-143">Specifies the VMSS object.</span></span>
<span data-ttu-id="32307-144">Você pode usar o cmdlet New-AzVmssConfig para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="32307-144">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32307-145">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="32307-145">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="32307-146">Indica se as máquinas virtuais no VMSS estão habilitadas para atualizações automáticas.</span><span class="sxs-lookup"><span data-stu-id="32307-146">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32307-147">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="32307-147">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="32307-148">Indica se o agente da máquina virtual deve ser provisionado nas máquinas virtuais no VMSS.</span><span class="sxs-lookup"><span data-stu-id="32307-148">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32307-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="32307-149">-Confirm</span></span>
<span data-ttu-id="32307-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32307-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32307-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32307-151">-WhatIf</span></span>
<span data-ttu-id="32307-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="32307-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32307-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="32307-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32307-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32307-154">CommonParameters</span></span>
<span data-ttu-id="32307-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32307-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32307-156">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32307-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32307-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="32307-157">INPUTS</span></span>

### <span data-ttu-id="32307-158">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="32307-158">VirtualMachineScaleSet</span></span>
<span data-ttu-id="32307-159">O parâmetro ' VirtualMachineScaleSet ' aceita o valor do tipo ' VirtualMachineScaleSet ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="32307-159">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="32307-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="32307-160">OUTPUTS</span></span>

### <span data-ttu-id="32307-161">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="32307-161">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="32307-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="32307-162">NOTES</span></span>

## <span data-ttu-id="32307-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32307-163">RELATED LINKS</span></span>

[<span data-ttu-id="32307-164">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="32307-164">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="32307-165">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="32307-165">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="32307-166">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="32307-166">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="32307-167">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="32307-167">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="32307-168">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="32307-168">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


