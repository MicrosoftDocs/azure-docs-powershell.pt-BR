---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
ms.openlocfilehash: a697ead2f971191d108d4fb348a213e35b363d63
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890877"
---
# <span data-ttu-id="e75c1-101">Get-AzVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="e75c1-101">Get-AzVmssVMDiskEncryption</span></span>

## <span data-ttu-id="e75c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e75c1-102">SYNOPSIS</span></span>
<span data-ttu-id="e75c1-103">Mostra o status de criptografia de disco de VMs em um conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="e75c1-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

## <span data-ttu-id="e75c1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e75c1-104">SYNTAX</span></span>

```
Get-AzVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String>]
 [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e75c1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e75c1-105">DESCRIPTION</span></span>
<span data-ttu-id="e75c1-106">Mostra o status de criptografia de disco do conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="e75c1-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="e75c1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e75c1-107">EXAMPLES</span></span>

### <span data-ttu-id="e75c1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e75c1-108">Example 1</span></span>
```
PS C:\> Get-AzVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="e75c1-109">Mostra o status de criptografia de disco da instância VM 1 no conjunto de escala VM chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="e75c1-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="e75c1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e75c1-110">PARAMETERS</span></span>

### <span data-ttu-id="e75c1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e75c1-111">-DefaultProfile</span></span>
<span data-ttu-id="e75c1-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e75c1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e75c1-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="e75c1-113">-ExtensionName</span></span>
<span data-ttu-id="e75c1-114">O nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="e75c1-114">The extension name.</span></span>
<span data-ttu-id="e75c1-115">Se esse parâmetro não for especificado, os valores padrão usados serão AzureDiskEncryption para VMs windows e AzureDiskEncryptionForLinux para VMs Linux.</span><span class="sxs-lookup"><span data-stu-id="e75c1-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="e75c1-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="e75c1-116">-InstanceId</span></span>
<span data-ttu-id="e75c1-117">Especifica a ID da instância.</span><span class="sxs-lookup"><span data-stu-id="e75c1-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="e75c1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e75c1-118">-ResourceGroupName</span></span>
<span data-ttu-id="e75c1-119">Nome do grupo de recursos do conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e75c1-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="e75c1-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e75c1-120">-VMScaleSetName</span></span>
<span data-ttu-id="e75c1-121">O nome do conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e75c1-121">The virtual machine scale set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e75c1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e75c1-122">CommonParameters</span></span>
<span data-ttu-id="e75c1-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e75c1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e75c1-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e75c1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e75c1-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e75c1-125">INPUTS</span></span>

### <span data-ttu-id="e75c1-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e75c1-126">System.String</span></span>

## <span data-ttu-id="e75c1-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e75c1-127">OUTPUTS</span></span>

### <span data-ttu-id="e75c1-128">Microsoft.Azure.Commands.Compute.Models.PSVmsSVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="e75c1-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="e75c1-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="e75c1-129">NOTES</span></span>

## <span data-ttu-id="e75c1-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e75c1-130">RELATED LINKS</span></span>
