---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: 3f70df791964f6b60385b6c12be46ce15f63a469
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601272"
---
# <span data-ttu-id="64678-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="64678-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="64678-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64678-102">SYNOPSIS</span></span>
<span data-ttu-id="64678-103">Remove um disco de dados do VMSS.</span><span class="sxs-lookup"><span data-stu-id="64678-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="64678-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64678-104">SYNTAX</span></span>

### <span data-ttu-id="64678-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="64678-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64678-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="64678-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64678-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64678-107">DESCRIPTION</span></span>
<span data-ttu-id="64678-108">O cmdlet **Remove-AzVmssDataDisk** remove um disco de dados da instância VMSS (conjunto de dimensionamento de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="64678-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="64678-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64678-109">EXAMPLES</span></span>

### <span data-ttu-id="64678-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="64678-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="64678-111">Esse comando Remove o disco de dados chamado ' datadisk1 ' do objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="64678-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="64678-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="64678-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="64678-113">Esse comando Remove o disco de dados do LUN 0 do objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="64678-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="64678-114">OS</span><span class="sxs-lookup"><span data-stu-id="64678-114">PARAMETERS</span></span>

### <span data-ttu-id="64678-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64678-115">-DefaultProfile</span></span>
<span data-ttu-id="64678-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64678-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64678-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="64678-117">-Lun</span></span>
<span data-ttu-id="64678-118">Especifica o número de unidade lógica do disco.</span><span class="sxs-lookup"><span data-stu-id="64678-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LunParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64678-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="64678-119">-Name</span></span>
<span data-ttu-id="64678-120">Especifica o nome do disco.</span><span class="sxs-lookup"><span data-stu-id="64678-120">Specifies the name of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64678-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="64678-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="64678-122">Especifique o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="64678-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="64678-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="64678-123">-Confirm</span></span>
<span data-ttu-id="64678-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64678-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64678-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64678-125">-WhatIf</span></span>
<span data-ttu-id="64678-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="64678-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64678-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="64678-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64678-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64678-128">CommonParameters</span></span>
<span data-ttu-id="64678-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64678-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64678-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64678-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64678-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64678-131">INPUTS</span></span>

### <span data-ttu-id="64678-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="64678-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="64678-133">System. String</span><span class="sxs-lookup"><span data-stu-id="64678-133">System.String</span></span>

### <span data-ttu-id="64678-134">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="64678-134">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="64678-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64678-135">OUTPUTS</span></span>

### <span data-ttu-id="64678-136">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="64678-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="64678-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64678-137">NOTES</span></span>

## <span data-ttu-id="64678-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64678-138">RELATED LINKS</span></span>
