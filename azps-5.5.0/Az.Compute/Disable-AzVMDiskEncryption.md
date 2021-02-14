---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: 1aad073ebd1f1a5e14abfd728ba6e6266a2d6fb8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115484"
---
# <span data-ttu-id="f5a82-101">Disable-AzVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="f5a82-101">Disable-AzVMDiskEncryption</span></span>

## <span data-ttu-id="f5a82-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5a82-102">SYNOPSIS</span></span>
<span data-ttu-id="f5a82-103">Desabilita a criptografia em uma máquina virtual IaaS.</span><span class="sxs-lookup"><span data-stu-id="f5a82-103">Disables encryption on an IaaS virtual machine.</span></span>

## <span data-ttu-id="f5a82-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5a82-104">SYNTAX</span></span>

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5a82-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5a82-105">DESCRIPTION</span></span>
<span data-ttu-id="f5a82-106">O cmdlet **Disable-AzVMDiskEncryption** desabilita a criptografia em uma infraestrutura como um computador virtual (IaaS).</span><span class="sxs-lookup"><span data-stu-id="f5a82-106">The **Disable-AzVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="f5a82-107">Este cmdlet só tem suporte em máquinas virtuais do Windows e não em máquinas virtuais do Linux.</span><span class="sxs-lookup"><span data-stu-id="f5a82-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="f5a82-108">Este cmdlet instala uma extensão no computador virtual para desabilitar a criptografia.</span><span class="sxs-lookup"><span data-stu-id="f5a82-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="f5a82-109">Se o *parâmetro Nome* não for especificado, será criada uma extensão com o nome padrão "AzureDiskEncryption para VMs do Windows".</span><span class="sxs-lookup"><span data-stu-id="f5a82-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="f5a82-110">Cuidado: este cmdlet reinicia a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f5a82-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="f5a82-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f5a82-111">EXAMPLES</span></span>

### <span data-ttu-id="f5a82-112">Exemplo 1: Desabilitar a criptografia para todos os volumes em uma máquina virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="f5a82-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="f5a82-113">Esse comando desabilita a criptografia para volumes de tipo todos para a máquina virtual chamada VM002 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="f5a82-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="f5a82-114">Como o *parâmetro VolumeType* não é especificado, o cmdlet define o valor como Tudo.</span><span class="sxs-lookup"><span data-stu-id="f5a82-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="f5a82-115">Exemplo 2: Desabilitar a criptografia para volumes de dados em uma máquina virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="f5a82-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002"
PS C:\> $VMName = "VM004"
PS C:\> $VolumeType = "Data"
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName $ResourceGroup -VMName $VMName -VolumeType $VolumeType
```

<span data-ttu-id="f5a82-116">Esse comando desabilita a criptografia para volumes de dados do tipo para a máquina virtual chamada VM004 que pertence ao grupo de recursos chamado Group002.</span><span class="sxs-lookup"><span data-stu-id="f5a82-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="f5a82-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5a82-117">PARAMETERS</span></span>

### <span data-ttu-id="f5a82-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5a82-118">-DefaultProfile</span></span>
<span data-ttu-id="f5a82-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f5a82-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5a82-120">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f5a82-120">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="f5a82-121">Indica que esse cmdlet desabilita a atualização automática da versão secundária da extensão.</span><span class="sxs-lookup"><span data-stu-id="f5a82-121">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5a82-122">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="f5a82-122">-ExtensionPublisherName</span></span>
<span data-ttu-id="f5a82-123">O nome do editor de extensão.</span><span class="sxs-lookup"><span data-stu-id="f5a82-123">The extension publisher name.</span></span> <span data-ttu-id="f5a82-124">Especifique esse parâmetro apenas para substituir o valor padrão de "Microsoft.Azure.Security".</span><span class="sxs-lookup"><span data-stu-id="f5a82-124">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="f5a82-125">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="f5a82-125">-ExtensionType</span></span>
<span data-ttu-id="f5a82-126">O tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="f5a82-126">The extension type.</span></span> <span data-ttu-id="f5a82-127">Especifique este parâmetro para substituir seu valor padrão de "AzureDiskEncryption" para VMs do Windows e "AzureDiskEncryptionForLinux" para VMs do Linux.</span><span class="sxs-lookup"><span data-stu-id="f5a82-127">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="f5a82-128">-Forçar</span><span class="sxs-lookup"><span data-stu-id="f5a82-128">-Force</span></span>
<span data-ttu-id="f5a82-129">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f5a82-129">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5a82-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5a82-130">-Name</span></span>
<span data-ttu-id="f5a82-131">Especifica o nome do recurso ARM (Gerenciador de Recursos do Azure) que representa a extensão.</span><span class="sxs-lookup"><span data-stu-id="f5a82-131">Specifies the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="f5a82-132">Se esse parâmetro não for especificado, esse cmdlet será padrão para "VMs do AzureDiskEncryption para Windows".</span><span class="sxs-lookup"><span data-stu-id="f5a82-132">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5a82-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5a82-133">-ResourceGroupName</span></span>
<span data-ttu-id="f5a82-134">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f5a82-134">Specifies the resource group name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5a82-135">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f5a82-135">-TypeHandlerVersion</span></span>
<span data-ttu-id="f5a82-136">Especifica a versão da extensão de criptografia.</span><span class="sxs-lookup"><span data-stu-id="f5a82-136">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="f5a82-137">Se você não especificar um valor para esse parâmetro, a versão mais recente da extensão será usada.</span><span class="sxs-lookup"><span data-stu-id="f5a82-137">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5a82-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="f5a82-138">-VMName</span></span>
<span data-ttu-id="f5a82-139">Especifica o nome da máquina virtual em que esse cmdlet desabilita a criptografia.</span><span class="sxs-lookup"><span data-stu-id="f5a82-139">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5a82-140">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="f5a82-140">-VolumeType</span></span>
<span data-ttu-id="f5a82-141">Especifica o tipo de volumes de máquina virtual para executar a operação de criptografia.</span><span class="sxs-lookup"><span data-stu-id="f5a82-141">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="f5a82-142">Para máquinas virtuais do Windows, os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="f5a82-142">For Windows virtual machines, valid values are:</span></span> 
- <span data-ttu-id="f5a82-143">Todos</span><span class="sxs-lookup"><span data-stu-id="f5a82-143">All</span></span>
- <span data-ttu-id="f5a82-144">SO</span><span class="sxs-lookup"><span data-stu-id="f5a82-144">OS</span></span>
- <span data-ttu-id="f5a82-145">Dados.</span><span class="sxs-lookup"><span data-stu-id="f5a82-145">Data.</span></span>
<span data-ttu-id="f5a82-146">Se você não especificar um valor para esse parâmetro, o valor padrão será Tudo.</span><span class="sxs-lookup"><span data-stu-id="f5a82-146">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="f5a82-147">No momento, não há suporte para desabilitar a criptografia para o Linux.</span><span class="sxs-lookup"><span data-stu-id="f5a82-147">Disable encryption is not currently supported for Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5a82-148">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f5a82-148">-Confirm</span></span>
<span data-ttu-id="f5a82-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5a82-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5a82-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5a82-150">-WhatIf</span></span>
<span data-ttu-id="f5a82-151">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f5a82-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5a82-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f5a82-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5a82-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5a82-153">CommonParameters</span></span>
<span data-ttu-id="f5a82-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5a82-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5a82-155">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5a82-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5a82-156">Entradas</span><span class="sxs-lookup"><span data-stu-id="f5a82-156">INPUTS</span></span>

### <span data-ttu-id="f5a82-157">System.String</span><span class="sxs-lookup"><span data-stu-id="f5a82-157">System.String</span></span>

### <span data-ttu-id="f5a82-158">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f5a82-158">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f5a82-159">Saídas</span><span class="sxs-lookup"><span data-stu-id="f5a82-159">OUTPUTS</span></span>

### <span data-ttu-id="f5a82-160">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f5a82-160">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f5a82-161">Notas</span><span class="sxs-lookup"><span data-stu-id="f5a82-161">NOTES</span></span>

## <span data-ttu-id="f5a82-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5a82-162">RELATED LINKS</span></span>

[<span data-ttu-id="f5a82-163">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="f5a82-163">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="f5a82-164">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="f5a82-164">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="f5a82-165">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="f5a82-165">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


