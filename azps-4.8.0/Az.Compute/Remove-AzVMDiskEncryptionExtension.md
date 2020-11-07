---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 4c9e66d751b5465f4112b7cb6d971022e43fa023
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948401"
---
# <span data-ttu-id="a079c-101">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="a079c-101">Remove-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="a079c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a079c-102">SYNOPSIS</span></span>
<span data-ttu-id="a079c-103">Remove a extensão de criptografia de disco de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a079c-103">Removes the disk encryption extension from a virtual machine.</span></span>

## <span data-ttu-id="a079c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a079c-104">SYNTAX</span></span>

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a079c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a079c-105">DESCRIPTION</span></span>
<span data-ttu-id="a079c-106">O cmdlet **Remove-AzVMDiskEncryptionExtension** remove a extensão de criptografia de disco e a configuração de extensão associada de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a079c-106">The **Remove-AzVMDiskEncryptionExtension** cmdlet removes the disk encryption extension and the associated extension configuration from a virtual machine.</span></span> <span data-ttu-id="a079c-107">Se nenhum nome de extensão for especificado, esse cmdlet removerá a extensão com o nome padrão AzureDiskEncryption para máquinas virtuais que executam o sistema operacional Windows ou o AzureDiskEncryptionForLinux para máquinas virtuais com base em Linux.</span><span class="sxs-lookup"><span data-stu-id="a079c-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span> 

<span data-ttu-id="a079c-108">Esse cmdlet falhará se a criptografia na máquina virtual não tiver sido desabilitada primeiro.</span><span class="sxs-lookup"><span data-stu-id="a079c-108">This cmdlet will fail if encryption on the virtual machine has not been first disabled.</span></span>  <span data-ttu-id="a079c-109">Para desabilitar a criptografia em uma máquina virtual, use [Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md).</span><span class="sxs-lookup"><span data-stu-id="a079c-109">To disable encryption on a virtual machine, use [Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md).</span></span> 

## <span data-ttu-id="a079c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a079c-110">EXAMPLES</span></span>

### <span data-ttu-id="a079c-111">Exemplo 1: remover a extensão de criptografia de disco de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a079c-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="a079c-112">Esse comando Remove a extensão com o nome padrão AzureDiskEncryption para uma máquina virtual que executa o sistema operacional Windows ou o AzureDiskEncryptionForLinux para máquina virtual com base em Linux chamado MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="a079c-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="a079c-113">Exemplo 2: remover uma extensão de criptografia de disco específica de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a079c-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="a079c-114">Esse comando Remove a extensão de criptografia chamada MyDiskEncryptionExtension da máquina virtual nomeada MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="a079c-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="a079c-115">OS</span><span class="sxs-lookup"><span data-stu-id="a079c-115">PARAMETERS</span></span>

### <span data-ttu-id="a079c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a079c-116">-DefaultProfile</span></span>
<span data-ttu-id="a079c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a079c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a079c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a079c-118">-Force</span></span>
<span data-ttu-id="a079c-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a079c-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a079c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a079c-120">-Name</span></span>
<span data-ttu-id="a079c-121">Especifica o nome do recurso do Gerenciador de recursos do Azure que representa a extensão.</span><span class="sxs-lookup"><span data-stu-id="a079c-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="a079c-122">O cmdlet Set-AzVMDiskEncryptionExtension define esse nome para AzureDiskEncryption para máquinas virtuais que executam o sistema operacional Windows e o AzureDiskEncryptionForLinux para máquinas virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="a079c-122">The Set-AzVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="a079c-123">Especifique esse parâmetro somente se você tiver alterado o nome padrão no cmdlet **set-AzVMDiskEncryptionExtension** ou usado um nome de recurso diferente em um modelo do Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="a079c-123">Specify this parameter only if you changed the default name in the **Set-AzVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="a079c-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a079c-124">-NoWait</span></span>
<span data-ttu-id="a079c-125">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="a079c-125">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="a079c-126">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="a079c-126">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="a079c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a079c-127">-ResourceGroupName</span></span>
<span data-ttu-id="a079c-128">Especifica o nome do grupo de recursos para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a079c-128">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="a079c-129">-VMName</span><span class="sxs-lookup"><span data-stu-id="a079c-129">-VMName</span></span>
<span data-ttu-id="a079c-130">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a079c-130">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="a079c-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a079c-131">-Confirm</span></span>
<span data-ttu-id="a079c-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a079c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a079c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a079c-133">-WhatIf</span></span>
<span data-ttu-id="a079c-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a079c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a079c-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a079c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a079c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a079c-136">CommonParameters</span></span>
<span data-ttu-id="a079c-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a079c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a079c-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a079c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a079c-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a079c-139">INPUTS</span></span>

### <span data-ttu-id="a079c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a079c-140">System.String</span></span>

## <span data-ttu-id="a079c-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a079c-141">OUTPUTS</span></span>

### <span data-ttu-id="a079c-142">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a079c-142">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a079c-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a079c-143">NOTES</span></span>

## <span data-ttu-id="a079c-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a079c-144">RELATED LINKS</span></span>

[<span data-ttu-id="a079c-145">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="a079c-145">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="a079c-146">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="a079c-146">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


