---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
ms.openlocfilehash: 293bb0f314b82ed2318684996f9b18c79a3b81d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602033"
---
# <span data-ttu-id="9a11b-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="9a11b-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="9a11b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9a11b-102">SYNOPSIS</span></span>
<span data-ttu-id="9a11b-103">Remove um disco de dados do VMSS.</span><span class="sxs-lookup"><span data-stu-id="9a11b-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a11b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a11b-104">SYNTAX</span></span>

### <span data-ttu-id="9a11b-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a11b-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Name] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a11b-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a11b-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Lun] <Int32> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a11b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9a11b-107">DESCRIPTION</span></span>
<span data-ttu-id="9a11b-108">O cmdlet **Remove-AzureRmVmssDataDisk** remove um disco de dados da instância VMSS (conjunto de dimensionamento de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="9a11b-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="9a11b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9a11b-109">EXAMPLES</span></span>

### <span data-ttu-id="9a11b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9a11b-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="9a11b-111">Esse comando Remove o disco de dados chamado ' datadisk1 ' do objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="9a11b-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="9a11b-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9a11b-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="9a11b-113">Esse comando Remove o disco de dados do LUN 0 do objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="9a11b-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="9a11b-114">OS</span><span class="sxs-lookup"><span data-stu-id="9a11b-114">PARAMETERS</span></span>

### <span data-ttu-id="9a11b-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="9a11b-115">-Lun</span></span>
<span data-ttu-id="9a11b-116">Especifica o número de unidade lógica do disco.</span><span class="sxs-lookup"><span data-stu-id="9a11b-116">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: LunParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a11b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="9a11b-117">-Name</span></span>
<span data-ttu-id="9a11b-118">Especifica o nome do disco.</span><span class="sxs-lookup"><span data-stu-id="9a11b-118">Specifies the name of the disk.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a11b-119">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9a11b-119">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="9a11b-120">Especifique o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="9a11b-120">Specify the VMSS object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a11b-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9a11b-121">-Confirm</span></span>
<span data-ttu-id="9a11b-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a11b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a11b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a11b-123">-WhatIf</span></span>
<span data-ttu-id="9a11b-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9a11b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a11b-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9a11b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a11b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a11b-126">CommonParameters</span></span>
<span data-ttu-id="9a11b-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a11b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a11b-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a11b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a11b-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9a11b-129">INPUTS</span></span>

### <span data-ttu-id="9a11b-130">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9a11b-130">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="9a11b-131">System. String System. Nullable ' 1 [System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9a11b-131">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="9a11b-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9a11b-132">OUTPUTS</span></span>

### <span data-ttu-id="9a11b-133">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9a11b-133">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="9a11b-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9a11b-134">NOTES</span></span>

## <span data-ttu-id="9a11b-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a11b-135">RELATED LINKS</span></span>

