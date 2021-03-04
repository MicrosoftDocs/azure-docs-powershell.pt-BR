---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 8bdfa0afeb5b558faa91d82df9ccdc64a0b4433c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889564"
---
# <span data-ttu-id="d3295-101">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="d3295-101">Remove-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="d3295-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3295-102">SYNOPSIS</span></span>
<span data-ttu-id="d3295-103">Remove a extensão de criptografia de disco de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d3295-103">Removes the disk encryption extension from a virtual machine.</span></span>

## <span data-ttu-id="d3295-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d3295-104">SYNTAX</span></span>

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3295-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d3295-105">DESCRIPTION</span></span>
<span data-ttu-id="d3295-106">O cmdlet **Remove-AzVMDiskEncryptionExtension** remove a extensão de criptografia de disco e a configuração de extensão associada de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d3295-106">The **Remove-AzVMDiskEncryptionExtension** cmdlet removes the disk encryption extension and the associated extension configuration from a virtual machine.</span></span> <span data-ttu-id="d3295-107">Se nenhum nome de extensão for especificado, esse cmdlet removerá a extensão com o nome padrão AzureDiskEncryption para máquinas virtuais que executem o sistema operacional Windows ou a AzureDiskEncryptionForLinux para máquinas virtuais baseadas em Linux.</span><span class="sxs-lookup"><span data-stu-id="d3295-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span> 

<span data-ttu-id="d3295-108">Esse cmdlet falhará se a criptografia na máquina virtual não tiver sido desabilitada pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="d3295-108">This cmdlet will fail if encryption on the virtual machine has not been first disabled.</span></span>  <span data-ttu-id="d3295-109">Para desabilitar a criptografia em uma máquina virtual, use [Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md).</span><span class="sxs-lookup"><span data-stu-id="d3295-109">To disable encryption on a virtual machine, use [Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md).</span></span> 

## <span data-ttu-id="d3295-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3295-110">EXAMPLES</span></span>

### <span data-ttu-id="d3295-111">Exemplo 1: Remover a extensão de criptografia de disco de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d3295-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="d3295-112">Este comando remove a extensão com o nome padrão AzureDiskEncryption para uma máquina virtual que executa o sistema operacional Windows ou a AzureDiskEncryptionForLinux para máquina virtual baseada em Linux chamada MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="d3295-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="d3295-113">Exemplo 2: Remover uma extensão de criptografia de disco específica de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d3295-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="d3295-114">Este comando remove a extensão de criptografia chamada MyDiskEncryptionExtension da máquina virtual chamada MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="d3295-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="d3295-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d3295-115">PARAMETERS</span></span>

### <span data-ttu-id="d3295-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3295-116">-DefaultProfile</span></span>
<span data-ttu-id="d3295-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d3295-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3295-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d3295-118">-Force</span></span>
<span data-ttu-id="d3295-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="d3295-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d3295-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d3295-120">-Name</span></span>
<span data-ttu-id="d3295-121">Especifica o nome do recurso Gerenciador de Recursos do Azure que representa a extensão.</span><span class="sxs-lookup"><span data-stu-id="d3295-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="d3295-122">O cmdlet Set-AzVMDiskEncryptionExtension define esse nome como AzureDiskEncryption para máquinas virtuais que executem o sistema operacional Windows e a AzureDiskEncryptionForLinux para máquinas virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="d3295-122">The Set-AzVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="d3295-123">Especifique esse parâmetro somente se você alterou o nome padrão no cmdlet **Set-AzVMDiskEncryptionExtension** ou usou um nome de recurso diferente em um modelo do Gerenciador de Recursos.</span><span class="sxs-lookup"><span data-stu-id="d3295-123">Specify this parameter only if you changed the default name in the **Set-AzVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3295-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d3295-124">-NoWait</span></span>
<span data-ttu-id="d3295-125">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="d3295-125">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="d3295-126">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="d3295-126">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="d3295-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3295-127">-ResourceGroupName</span></span>
<span data-ttu-id="d3295-128">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d3295-128">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="d3295-129">-VMName</span><span class="sxs-lookup"><span data-stu-id="d3295-129">-VMName</span></span>
<span data-ttu-id="d3295-130">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d3295-130">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="d3295-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3295-131">-Confirm</span></span>
<span data-ttu-id="d3295-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3295-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3295-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3295-133">-WhatIf</span></span>
<span data-ttu-id="d3295-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d3295-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3295-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d3295-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3295-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3295-136">CommonParameters</span></span>
<span data-ttu-id="d3295-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3295-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3295-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3295-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3295-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3295-139">INPUTS</span></span>

### <span data-ttu-id="d3295-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d3295-140">System.String</span></span>

## <span data-ttu-id="d3295-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d3295-141">OUTPUTS</span></span>

### <span data-ttu-id="d3295-142">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d3295-142">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d3295-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="d3295-143">NOTES</span></span>

## <span data-ttu-id="d3295-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3295-144">RELATED LINKS</span></span>

[<span data-ttu-id="d3295-145">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="d3295-145">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="d3295-146">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="d3295-146">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


