---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdiskencryptionextension
schema: 2.0.0
ms.openlocfilehash: 6c580b862ed2c8a420e8f203131ff9d18d187443
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785980"
---
# <span data-ttu-id="1289d-101">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="1289d-101">Remove-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="1289d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1289d-102">SYNOPSIS</span></span>
<span data-ttu-id="1289d-103">Remove a extensão de criptografia de disco de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1289d-103">Removes the disk encryption extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1289d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1289d-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1289d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1289d-105">DESCRIPTION</span></span>
<span data-ttu-id="1289d-106">O cmdlet **Remove-AzureRmVMDiskEncryptionExtension** remove a extensão de criptografia de disco de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1289d-106">The **Remove-AzureRmVMDiskEncryptionExtension** cmdlet removes the disk encryption extension from a virtual machine.</span></span>
<span data-ttu-id="1289d-107">Se nenhum nome de extensão for especificado, esse cmdlet removerá a extensão com o nome padrão AzureDiskEncryption para máquinas virtuais que executam o sistema operacional Windows ou o AzureDiskEncryptionForLinux para máquinas virtuais com base em Linux.</span><span class="sxs-lookup"><span data-stu-id="1289d-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span>
<span data-ttu-id="1289d-108">Esse cmdlet não desabilita a criptografia na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1289d-108">This cmdlet does not disable encryption on the virtual machine.</span></span>
<span data-ttu-id="1289d-109">Ele remove a extensão e a configuração de extensão associada da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1289d-109">It removes the extension and the associated extension configuration from the virtual machine.</span></span>

## <span data-ttu-id="1289d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1289d-110">EXAMPLES</span></span>

### <span data-ttu-id="1289d-111">Exemplo 1: remover a extensão de criptografia de disco de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1289d-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="1289d-112">Esse comando Remove a extensão com o nome padrão AzureDiskEncryption para uma máquina virtual que executa o sistema operacional Windows ou o AzureDiskEncryptionForLinux para máquina virtual com base em Linux chamado MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="1289d-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="1289d-113">Exemplo 2: remover uma extensão de criptografia de disco específica de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1289d-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="1289d-114">Esse comando Remove a extensão de criptografia chamada MyDiskEncryptionExtension da máquina virtual nomeada MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="1289d-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="1289d-115">OS</span><span class="sxs-lookup"><span data-stu-id="1289d-115">PARAMETERS</span></span>

### <span data-ttu-id="1289d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1289d-116">-DefaultProfile</span></span>
<span data-ttu-id="1289d-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1289d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1289d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1289d-118">-Force</span></span>
<span data-ttu-id="1289d-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="1289d-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1289d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="1289d-120">-Name</span></span>
<span data-ttu-id="1289d-121">Especifica o nome do recurso do Gerenciador de recursos do Azure que representa a extensão.</span><span class="sxs-lookup"><span data-stu-id="1289d-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="1289d-122">O cmdlet Set-AzureRmVMDiskEncryptionExtension define esse nome para AzureDiskEncryption para máquinas virtuais que executam o sistema operacional Windows e o AzureDiskEncryptionForLinux para máquinas virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="1289d-122">The Set-AzureRmVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="1289d-123">Especifique esse parâmetro somente se você tiver alterado o nome padrão no cmdlet **set-AzureRmVMDiskEncryptionExtension** ou usado um nome de recurso diferente em um modelo do Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="1289d-123">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1289d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1289d-124">-ResourceGroupName</span></span>
<span data-ttu-id="1289d-125">Especifica o nome do grupo de recursos para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1289d-125">Specifies the name of the resource group for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1289d-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="1289d-126">-VMName</span></span>
<span data-ttu-id="1289d-127">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1289d-127">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1289d-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1289d-128">-Confirm</span></span>
<span data-ttu-id="1289d-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1289d-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1289d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1289d-130">-WhatIf</span></span>
<span data-ttu-id="1289d-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1289d-131">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="1289d-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1289d-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1289d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1289d-133">CommonParameters</span></span>
<span data-ttu-id="1289d-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1289d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1289d-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1289d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1289d-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1289d-136">INPUTS</span></span>

### <span data-ttu-id="1289d-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1289d-137">None</span></span>
<span data-ttu-id="1289d-138">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="1289d-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1289d-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1289d-139">OUTPUTS</span></span>

### <span data-ttu-id="1289d-140">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1289d-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1289d-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1289d-141">NOTES</span></span>

## <span data-ttu-id="1289d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1289d-142">RELATED LINKS</span></span>

[<span data-ttu-id="1289d-143">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="1289d-143">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="1289d-144">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="1289d-144">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


