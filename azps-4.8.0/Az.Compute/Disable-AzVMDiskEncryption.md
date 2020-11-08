---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: 1aad073ebd1f1a5e14abfd728ba6e6266a2d6fb8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112571"
---
# <span data-ttu-id="e408a-101">Disable-AzVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="e408a-101">Disable-AzVMDiskEncryption</span></span>

## <span data-ttu-id="e408a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e408a-102">SYNOPSIS</span></span>
<span data-ttu-id="e408a-103">Desabilita a criptografia em uma máquina virtual IaaS.</span><span class="sxs-lookup"><span data-stu-id="e408a-103">Disables encryption on an IaaS virtual machine.</span></span>

## <span data-ttu-id="e408a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e408a-104">SYNTAX</span></span>

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e408a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e408a-105">DESCRIPTION</span></span>
<span data-ttu-id="e408a-106">O cmdlet **Disable-AzVMDiskEncryption** desabilita a criptografia em uma máquina virtual de infraestrutura como serviço (IaaS).</span><span class="sxs-lookup"><span data-stu-id="e408a-106">The **Disable-AzVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="e408a-107">Este cmdlet tem suporte apenas em máquinas virtuais do Windows e não em máquinas virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="e408a-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="e408a-108">Este cmdlet instala uma extensão na máquina virtual para desabilitar a criptografia.</span><span class="sxs-lookup"><span data-stu-id="e408a-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="e408a-109">Se o parâmetro *Name* não for especificado, será criada uma extensão com o nome padrão "AzureDiskEncryption para VMs do Windows".</span><span class="sxs-lookup"><span data-stu-id="e408a-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="e408a-110">Cuidado: esse cmdlet reinicializa a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e408a-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="e408a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e408a-111">EXAMPLES</span></span>

### <span data-ttu-id="e408a-112">Exemplo 1: desabilitar a criptografia para todos os volumes em um computador virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="e408a-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="e408a-113">Esse comando desabilita a criptografia para volumes do tipo tudo para a máquina virtual nomeada VM002 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="e408a-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="e408a-114">Como o parâmetro *volumetype* não é especificado, o cmdlet define o valor para All.</span><span class="sxs-lookup"><span data-stu-id="e408a-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="e408a-115">Exemplo 2: desabilitar a criptografia de volumes de dados em um computador virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="e408a-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002"
PS C:\> $VMName = "VM004"
PS C:\> $VolumeType = "Data"
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName $ResourceGroup -VMName $VMName -VolumeType $VolumeType
```

<span data-ttu-id="e408a-116">Esse comando desabilita a criptografia de volumes do tipo dados para a máquina virtual nomeada VM004 que pertence ao grupo de recursos chamado Group002.</span><span class="sxs-lookup"><span data-stu-id="e408a-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="e408a-117">OS</span><span class="sxs-lookup"><span data-stu-id="e408a-117">PARAMETERS</span></span>

### <span data-ttu-id="e408a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e408a-118">-DefaultProfile</span></span>
<span data-ttu-id="e408a-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e408a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e408a-120">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="e408a-120">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="e408a-121">Indica que esse cmdlet desabilita a atualização automática da versão secundária da extensão.</span><span class="sxs-lookup"><span data-stu-id="e408a-121">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="e408a-122">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="e408a-122">-ExtensionPublisherName</span></span>
<span data-ttu-id="e408a-123">O nome do fornecedor da extensão.</span><span class="sxs-lookup"><span data-stu-id="e408a-123">The extension publisher name.</span></span> <span data-ttu-id="e408a-124">Especifique esse parâmetro somente para substituir o valor padrão de "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="e408a-124">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="e408a-125">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="e408a-125">-ExtensionType</span></span>
<span data-ttu-id="e408a-126">O tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="e408a-126">The extension type.</span></span> <span data-ttu-id="e408a-127">Especifique esse parâmetro para substituir o valor padrão de "AzureDiskEncryption" para VMs do Windows e "AzureDiskEncryptionForLinux" para VMs Linux.</span><span class="sxs-lookup"><span data-stu-id="e408a-127">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="e408a-128">-Force</span><span class="sxs-lookup"><span data-stu-id="e408a-128">-Force</span></span>
<span data-ttu-id="e408a-129">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e408a-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e408a-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="e408a-130">-Name</span></span>
<span data-ttu-id="e408a-131">Especifica o nome do recurso ARM (Azure Resource Manager) que representa a extensão.</span><span class="sxs-lookup"><span data-stu-id="e408a-131">Specifies the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="e408a-132">Se esse parâmetro não for especificado, o padrão do cmdlet será "AzureDiskEncryption para VMs do Windows".</span><span class="sxs-lookup"><span data-stu-id="e408a-132">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

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

### <span data-ttu-id="e408a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e408a-133">-ResourceGroupName</span></span>
<span data-ttu-id="e408a-134">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e408a-134">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="e408a-135">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="e408a-135">-TypeHandlerVersion</span></span>
<span data-ttu-id="e408a-136">Especifica a versão da extensão de criptografia.</span><span class="sxs-lookup"><span data-stu-id="e408a-136">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="e408a-137">Se você não especificar um valor para esse parâmetro, a versão mais recente da extensão será usada.</span><span class="sxs-lookup"><span data-stu-id="e408a-137">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

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

### <span data-ttu-id="e408a-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="e408a-138">-VMName</span></span>
<span data-ttu-id="e408a-139">Especifica o nome da máquina virtual em que esse cmdlet desabilita a criptografia.</span><span class="sxs-lookup"><span data-stu-id="e408a-139">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

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

### <span data-ttu-id="e408a-140">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="e408a-140">-VolumeType</span></span>
<span data-ttu-id="e408a-141">Especifica o tipo de volumes da máquina virtual para executar a operação de criptografia.</span><span class="sxs-lookup"><span data-stu-id="e408a-141">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="e408a-142">Para máquinas virtuais do Windows, os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="e408a-142">For Windows virtual machines, valid values are:</span></span> 
- <span data-ttu-id="e408a-143">Todo</span><span class="sxs-lookup"><span data-stu-id="e408a-143">All</span></span>
- <span data-ttu-id="e408a-144">OS</span><span class="sxs-lookup"><span data-stu-id="e408a-144">OS</span></span>
- <span data-ttu-id="e408a-145">Dados.</span><span class="sxs-lookup"><span data-stu-id="e408a-145">Data.</span></span>
<span data-ttu-id="e408a-146">Se você não especificar um valor para esse parâmetro, o valor padrão será ALL.</span><span class="sxs-lookup"><span data-stu-id="e408a-146">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="e408a-147">Não há suporte para a desativação da criptografia no momento para Linux.</span><span class="sxs-lookup"><span data-stu-id="e408a-147">Disable encryption is not currently supported for Linux.</span></span>

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

### <span data-ttu-id="e408a-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e408a-148">-Confirm</span></span>
<span data-ttu-id="e408a-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e408a-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e408a-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e408a-150">-WhatIf</span></span>
<span data-ttu-id="e408a-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e408a-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e408a-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e408a-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e408a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e408a-153">CommonParameters</span></span>
<span data-ttu-id="e408a-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e408a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e408a-155">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e408a-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e408a-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e408a-156">INPUTS</span></span>

### <span data-ttu-id="e408a-157">System. String</span><span class="sxs-lookup"><span data-stu-id="e408a-157">System.String</span></span>

### <span data-ttu-id="e408a-158">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e408a-158">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e408a-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e408a-159">OUTPUTS</span></span>

### <span data-ttu-id="e408a-160">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e408a-160">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e408a-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e408a-161">NOTES</span></span>

## <span data-ttu-id="e408a-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e408a-162">RELATED LINKS</span></span>

[<span data-ttu-id="e408a-163">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="e408a-163">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="e408a-164">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="e408a-164">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="e408a-165">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="e408a-165">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


